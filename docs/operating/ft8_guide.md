# FT8 — Praktični vodič

FT8 je digitalni mod koji je 2017. promijenio radioamaterizam. U samo nekoliko godina postao je najpopularniji mod na HF — više od SSB-a i CW-a zajedno po broju veza. Razlog: nevjerojatna osjetljivost pri slabim signalima i jednostavnost korištenja.

## Što je FT8?

FT8 (Franke-Taylor 8-Frequency Shift Keying) razvili su Joe Taylor K1JT i Steve Franke K9AN. Ključne karakteristike:

*   **SNR limit**: −24 dB — dekodira signale koji su 15 dB ispod razine šuma!
*   **Širina pojasa**: ~50 Hz po kanalu — 40+ FT8 veza u SSB kanalu od 2.7 kHz
*   **Ciklus**: 15 sekundi TX, 15 sekundi RX — izmjenično
*   **Sadržaj veze**: Callsign + lokator + rapport (59 sekundi ukupno za kompletni QSO)
*   **Automatizacija**: WSJT-X softver auto-dekodira i predlaže odgovor

!!! tip "FT8 nije 'cheat'"
    Kritičari kažu da FT8 ne zahtijeva vještinu. No, optimizacija antene, razumijevanje propagacije, i efikasno korištenje pile-up-a su i dalje vještine. FT8 samo uklanja prepreku šuma između vašeg signala i partnera.

---

## Instalacija i konfiguracija WSJT-X

### Što trebate

*   **Računalo**: Windows 7+ ili Linux ili macOS
*   **Softver**: WSJT-X (besplatno) — [physics.princeton.edu/pulsar/k1jt/wsjtx.html](https://physics.princeton.edu/pulsar/k1jt/wsjtx.html)
*   **Transciiver**: Bilo koji SSB radio s CAT interfacom (USB, CI-V, RS-232)
*   **Audio interface**: CAT kabel (Signalink, RigBlaster, ili ugrađeni USB audio u moderni TRX)
*   **GPS ili NTP**: Za **točno vrijeme** — FT8 ne radi s pomeranjem > 1 sekunde!

### Korak po korak instalacija (Windows)

**Korak 1**: Preuzmite i instalirajte WSJT-X s gore navedene poveznice.

**Korak 2**: Spojite radio s računalom:
*   CAT kabel za upravljanje radija (frekvencija, PTT)
*   Audio kabel za zvuk (ili USB audio) — LINE IN/OUT, nikad MIC/headphone

**Korak 3**: Pokrenite WSJT-X → **File → Settings**

**Korak 4**: Kartica "General":
*   **My Call**: Unesite vaš callsign (npr. `9A1ABC`)
*   **My Grid**: Vaš lokator (npr. `JN75ET`) — [pronađite lokator](https://www.levinecentral.com/ham/grid_square.php)

**Korak 5**: Kartica "Radio":
*   **Rig**: Odaberite vaš radio iz liste (Kenwood, Icom, Yaesu, itd.)
*   **Serial Port**: Odaberite COM port vašeg CAT kabela
*   **Baud Rate**: Ovisi o radiju (9600 ili 115200 za moderne)
*   **PTT Method**: `CAT` ili `DTR/RTS` ovisno o konfiguraciji

**Korak 6**: Kartica "Audio":
*   **Soundcard Input**: Odaberite audio interface (NE built-in mikrofon!)
*   **Soundcard Output**: Isti audio interface (LINE OUT)

**Korak 7**: Testiranje:
*   Tuning → "Tune" gumb — radio treba odašiljati carrier
*   Provjera prijema: Idite na 14.074 MHz USB, trebate vidjeti FT8 signale

!!! warning "Točno vrijeme je KRITIČNO!"
    FT8 ciklusi su vremenski sinkronizirani. Računalo mora imati točno UTC vrijeme unutar ±1 sekunde.
    
    Instalirajte **Meinberg NTP Client** (Windows) ili koristite `w32tm /resync` u naredbenoj liniji. Bez točnog vremena, FT8 **NE FUNKCIONIRA!**

---

## Sučelje WSJT-X

### Waterfall prikaz

Waterfall pokazuje frekvencijski spektar u realnom vremenu:
*   **Crvena vertikalna crta**: Vaša TX frekvencija
*   **Žute/zelene crte**: Drugi FT8 signali koji se dekodiraju
*   **Skala desno**: Frekvencija unutar passmand-a (0–3000 Hz)

!!! tip "Odabir TX frekvencije"
    Kliknite na slobodan prostor na waterfall-u da postavite TX frekvenciju. Izbjegavajte frekvencije gdje su već drugi signali (> 200 Hz odmaka). Idealno: između 500–2500 Hz unutar audio pojasa.

### Popis dekodiranih signala

Sve stanice koje se mogu dekodirati prikazane su u listi s:
*   Vremenom (UTC)
*   dB (signal quality)
*   DT (timing error u sekundama — treba biti < 1.0)
*   Frekvencijom (Hz unutar pojasa)
*   Poruka

### Statusi veze

| Boja u WSJT-X | Značenje |
|--------------|---------|
| Bijela pozadina | Normalna dekodirana poruka |
| Žuta pozadina | Vaš callsign je u poruci |
| Crvena pozadina | Hinting: poruka je za vas |
| Zelena | Veza je u tijeku (Auto Seq radi) |

---

## FT8 QSO — anatomija veze

Standardna FT8 veza traje 75 sekundi (5 izmjena × 15 sekundi):

```
0:00 → Stanica A zove:  CQ 9A1ABC JN75
0:15 → Stanica B odg.:  9A1ABC G0ABC IO91
0:30 → Stanica A šalje: G0ABC 9A1ABC -07
0:45 → Stanica B šalje: 9A1ABC G0ABC R-12
1:00 → Stanica A šalje: G0ABC 9A1ABC RRR
1:15 → Stanica B šalje: 9A1ABC G0ABC 73
```

!!! example "Interpretacija"
    `CQ 9A1ABC JN75` — Opći poziv od 9A1ABC, lokator JN75  
    `9A1ABC G0ABC IO91` — G0ABC odgovara, u lokaciji IO91  
    `G0ABC 9A1ABC -07` — 9A1ABC potvrđuje G0ABC-a s SNR −7 dB  
    `9A1ABC G0ABC R-12` — G0ABC potvrđuje prijemanje s SNR −12 dB  
    `G0ABC 9A1ABC RRR` — 9A1ABC potvrđuje sve (Received)  
    `9A1ABC G0ABC 73` — G0ABC završava vezu

### Automatski sekvencer (AutoSeq)

"Enable Tx" + "AutoSeq" → WSJT-X automatski:
1.  Prepoznaje poziv koji vam je upućen
2.  Šalje odgovarajuću poruku u pravo X sekundi
3.  Vodi vezu do kraja bez vašeg uplitanja

Alternativa: Ručno kliknete na dekodiranu stanicu i WSJT-X predlaže poruku.

---

## FT8 frekvencije (USB dial frequency)

| Opseg | Frekvencija | Bilješka |
|-------|------------|---------|
| 160 m | 1.840 MHz | |
| 80 m | 3.573 MHz | |
| 60 m | 5.357 MHz | (Gdje je dopušteno) |
| 40 m | 7.074 MHz | Najpopularniji noćni |
| 30 m | 10.136 MHz | Tihi WARC opseg |
| 20 m | 14.074 MHz | ⭐ Najpopularniji dnevni |
| 17 m | 18.100 MHz | |
| 15 m | 21.074 MHz | |
| 12 m | 24.915 MHz | |
| 10 m | 28.074 MHz | Broji DX uz visok SFI |
| 6 m | 50.313 MHz | Sporadični E love |

---

## Praćenje na PSKReporter

[PSKReporter.info](https://pskreporter.info) je globalna mapa koja prikazuje gdje se čuju FT8 signali.

**Kako koristiti:**
1.  Idite na PSKReporter.info
2.  Upišite vaš callsign
3.  Kliknite "Show Me" — vidite gdje su vas čule druge stanice i gdje ste vi čuli druge
4.  Izvrsno za testiranje antene i propagacije

!!! example "Test antene"
    Odašiljite WSPR ili FT8 CQ 10 minuta, zatim provjerite PSKReporter. Ako vas čuje samo Slovenija i Austrija, a ne Američka ili Azijska, antena ili položaj treba optimizaciju.

---

## FT8 napredni savjeti

### DXing s FT8

*   Koristite "DX only" filter u WSJT-X (ne prikazuje EU stanice)
*   "Fox & Hound" mod za DX ekspedicije: DX postaja šalje višestruke odgovore istovremeno (Fox), vi zovete posebnom "Hound" sekvencom
*   Pratite DX klastere (DXwatch, DXHeat) + PSKReporter za otvorene propagacijske puteve

### Postavljanje razine audio

*   **ALC treba biti minimalan ili isključen** — FT8 je osjetljiv na nelinearno pojačalo
*   Izlazna snaga: Počnite s 25% i smanjite koliko možete uz QSO
*   Zvučna kartica: Ulazni nivo ~50% na Windows mikseru

### FT8 i contest

FT8 contestovi (ARRL FT8 Roundup, World Wide Digi DX Contest) imaju posebna pravila. Koristite **N1MM+** ili **JTDX** za logging u contestima.

---

## JTDX vs WSJT-X

JTDX je alternativni klijent koji neke operatore preferiraju:

| Stavka | WSJT-X | JTDX |
|--------|--------|------|
| Razvijač | K1JT + K9AN | UA3DJY i drugi |
| Osjetljivost | Referentna | ~0.5–1 dB bolja dekodacija |
| Sučelje | Standardno | Malo drugačije raspoređeno |
| Prednosti | Oficijalni, podržan | Malo napredniji dekoder |

---

## Connecting to a Cluster

DX klasteri pokazuju aktivne DX postaje na opsegu — korisno za Fox&Hound targeting:

*   **DX Summit**: [dxsummit.fi](https://www.dxsummit.fi)
*   **DXWatch**: [dxwatch.com](https://www.dxwatch.com)
*   **DXHeat**: [dxheat.com](https://dxheat.com)

U WSJT-X: Settings → Reporting → "Enable PSK Reporter Spotting" (automatski šalje spotove)

---

## Solucija uobičajenih problema

| Problem | Uzrok | Rješenje |
|---------|-------|---------|
| Nema dekodiranja | Pogrešan audio ili nema signala | Provjerite audio ulaz, SWR, antenu |
| DT > 1.0 s | Netočno sistemsko vrijeme | Sinkronizirajte NTP |
| Visok ALC | Previše audio razine | Smanjite audio izlaz na 50% |
| Radio ne odašilje | PTT problem | Provjerite CAT postavke |
| Vidim signale, ne dekodiram | Previsok ulazni audio | Smanjite ulaz na ~60% |
| Stanica ne odgovara meni | Frekvencija je zauzeta | Promijenite TX frekvenciju |

---

## Povezane teme

*   [Modovi rada](modes.md) — Usporedba FT8 s ostalim modovima
*   [Frekvencijski planovi](bandplans.md) — FT8 frekvencije po opsezima
*   [Propagacija](../technical/propagation.md) — Kada FT8 radi DX
*   [DX rad](../activities/dxing.md) — Fox & Hound i DX pile-up
