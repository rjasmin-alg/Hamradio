# Modovi rada (Vrste komunikacije)

Svaki način prijenosa informacija u radioamaterizmu naziva se "mod" (mode). Izbor pravog moda za pravu situaciju razlika je između frustrantne sesije i sjajnog DX-a. Ova stranica pokriva sve popularne modove — od starog CW-a do FT8 revolucije.

## Pregled svih modova

| Mod | Tip | Širina pojasa | SNR limit | Popularnost | Primjena |
|-----|-----|--------------|-----------|-------------|---------|
| **CW** | Analogni | 100–500 Hz | −10 dB | ⭐⭐⭐⭐ | HF DX, natjecanja, slabi signali |
| **SSB** | Analogni | 2.7 kHz | 0 dB | ⭐⭐⭐⭐⭐ | HF DX, europske veze, natjecanja |
| **AM** | Analogni | 6–8 kHz | +3 dB | ⭐⭐ | Zrakoplovstvo, retro radio |
| **FM** | Analogni | 12–16 kHz | +5 dB | ⭐⭐⭐⭐⭐ | VHF/UHF lokalne veze, repetitori |
| **FT8** | Digitalni | ~50 Hz | −24 dB | ⭐⭐⭐⭐⭐ | HF DX, slabi propagacijski uvjeti |
| **FT4** | Digitalni | ~83 Hz | −17 dB | ⭐⭐⭐ | Bržji FT8, contestovi |
| **JS8Call** | Digitalni | ~50 Hz | −24 dB | ⭐⭐⭐ | Chat-style digitalni QSO |
| **PSK31** | Digitalni | ~31 Hz | −5 dB | ⭐⭐⭐ | Tipkovnica-u-tipkovnicu, tekst |
| **WSPR** | Digitalni | ~6 Hz | −28 dB | ⭐⭐⭐ | Propagacijski beacon |
| **RTTY** | Digitalni | 250–500 Hz | 0 dB | ⭐⭐ | Natjecanja, klasični digitalni |
| **Olivia** | Digitalni | 500 Hz–2 kHz | −12 dB | ⭐⭐ | Otpornost na QRM |
| **ATV** | Video | Široki | — | ⭐ | Analogna televizija |
| **DATV** | Video | Varijabilni | — | ⭐⭐ | Digitalna televizija |

---

## CW — Telegrafija

![CW Taster](https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/J-38_telegraph_key.jpg/320px-J-38_telegraph_key.jpg)

CW (Continuous Wave) je najstariji radioamaterski mod i još uvijek jedan od najefikasnijih. Morseov kod — točke i crtice — prenosi informacije jednostavnim uključivanjem i isključivanjem nosioca (OOK — On/Off Keying).

**Zašto CW i danas?**
*   Uska širina pojasa (100–500 Hz) = bolji SNR u šumu
*   Prolazi tamo gdje ni SSB ne može
*   Na natjecanjima: jedan SSB kanal = 5–10 CW stanica istovremeno
*   Jednostavna oprema (jednoelementni taster je dovoljno)
*   Tradicija i sportski izazov

**Brzine rada (WPM — Words Per Minute):**

| Razina | WPM | Opis |
|--------|-----|------|
| Početnik | 5–10 | Sporo ali razumljivo |
| Prolaz CEPT | 12 | Minimalni zahtjev (bivši standard) |
| Prosječan operator | 15–20 | Standardni QSO |
| Contestnik | 25–35 | Natjecatelji, DX peditions |
| Top contestnici | 40+ | Rekorderi, memorijsko primanje |

**Zvuk**: Ritmično piskanje, muzikalno kada se nauči.
*   [**Poslušajte CW**](https://www.youtube.com/results?search_query=cw+ham+radio+sound)

Više o učenju CW: [Učenje Morseovog koda](cw_learning.md)

---

## SSB — Single Sideband

SSB je "lingua franca" radioamaterizma — najčešći mod za razgovor na HF. Uklanjanjem jednog bočnog pojasa i nosioca iz AM signala dobiva se 3× učinkovitiji prijenos.

**LSB vs USB konvencija:**
*   **LSB** (Lower Sideband): Opsezi ispod 10 MHz (40 m, 80 m, 160 m)
*   **USB** (Upper Sideband): Opsezi iznad 10 MHz (20 m, 17 m, 15 m, 12 m, 10 m), VHF/UHF, svi digitalni modovi

**Prepoznavanje SSB-a na waterfallu**: Široka "oblak" traka, 2–3 kHz, mijenja oblik s govorom.

**Šta SSB zvuči "krivo"?** Ako ste na pogrešnoj frekvenciji za ±500 Hz, glas zvuči kao "Donald Duck". Tone na točnu frekvenciju dok zvuk postane normalan.

**Snaga**: Izražava se u PEP (Peak Envelope Power) — vršna snaga za trajanja samoglasnika. 100 W PEP = standardni transciiver.

*   [**Poslušajte SSB**](https://www.youtube.com/results?search_query=ssb+ham+radio+qso)

---

## AM — Amplitudna modulacija

AM je "pradjedica" radioamaterskih veza — i jedina modulacija originalnih radija 1920-ih.

**Zašto AM gotovo nestaje na HF?**
*   Zahtijeva 3× širi pojas od SSB
*   Neefikasna — 2/3 snage "izgori" u nosioc koji ne nosi informaciju
*   Slabiji SNR od SSB pri istoj izlaznoj snazi

**Gdje AM preživljava:**
*   Zrakoplovna komunikacija (118–137 MHz) — obavezna (laka detekcija)
*   AM broadcast (540 kHz – 1.7 MHz) — komercijalne postaje
*   Retro AM net-ovi na 10 m (29.0 MHz) — hobistički

!!! note "WAM — Wide AM"
    Entuzijasti vintage radija koriste AM s punom devijacijom na 10 m i 80 m. Zvukovni kvalitet je odličan, ali zauzima puno spektra.

---

## FM — Frekvencijska modulacija

FM je standard za lokalne VHF/UHF veze — jasnoća zvuka, jednostavnost korištenja, i squelch koji sprječava šum u tišini.

**Karakteristike:**
*   Narrow FM (amaterski): ±2.5 kHz deviacija, 12–16 kHz propusni pojas
*   Capture effect: U prisustvu dva signala, FM "hvata" jači i ignorira slabiji

**Primjene:**
*   FM simplex (direktna veza bez repetitora): pozivni kanal 145.500 MHz (EU)
*   FM repetitori: standardni ulaz/izlaz parovi
*   APRS: Telemetrija, GPS tracking na 144.800 MHz (EU)

**Offset za FM repetitore:**
*   2 m: −600 kHz (ulaz 600 kHz niže od izlaza)
*   70 cm: −7.6 MHz (ulaz 7.6 MHz niže od izlaza)

Više o repetitorima: [Repetitori](repeaters.md)

---

## Digitalni modovi — pregled

### FT8

FT8 (Franke-Taylor 8-FSK) je revolucionarni digitalni mod koji je 2017. promijenio radioamaterizam:
*   **15-sekundni ciklusi**: 15 s TX, 15 s RX — izmjenični ritmovi
*   **SNR limit**: −24 dB (čuje što je 15 dB ispod razine šuma!)
*   **Automatski**: Softver WSJT-X automatski dekodira, odabire i šalje
*   **Popularnost**: Više QSO-a u jednoj večeri nego SSB za godinu dana

Frekvencije FT8 (USB dial):
*   80 m: 3.573 MHz; 40 m: 7.074 MHz; 20 m: 14.074 MHz
*   17 m: 18.100 MHz; 15 m: 21.074 MHz; 10 m: 28.074 MHz

Detalje pogledajte na: [FT8 praktični vodič](ft8_guide.md)

### FT4

FT4 je bržja verzija FT8 (7.5-sekundni ciklusi) — SNR limit −17 dB. Koristi se na contestovima gdje je brzina ključna.

### JS8Call

JS8Call koristi FT8 infrastrukturu, ali dodaje "chat" funkciju — možete pisati slobodan tekst! Popularan za emergency communications i ragchew digitalni.

### PSK31

PSK31 (Phase Shift Keying, 31 baud) je digitalni mod za razmjenu teksta tipkovnicom u realnom vremenu:
*   Samo ~31 Hz širine pojasa — "uzak kao laser"
*   Čitljivost pri −5 dB SNR
*   Koristi se na 14.070 MHz (20 m), 7.070 MHz (40 m)
*   Softver: fldigi, Ham Radio Deluxe

### WSPR — Propagacijski beacon

WSPR (Weak Signal Propagation Reporter) je automatski beacon mod:
*   SNR limit: −28 dB (nevjerovatno osjetljiv!)
*   2-minutni ciklusi, samo 6 Hz propusni pojas
*   Svrha: Testiranje propagacije — WSPR mapa pokazuje gdje se vaš signal čuo
*   [WSPRnet.org](https://www.wsprnet.org) — globalna mapa WSPR stanica

!!! tip "WSPR za propagacijska testiranja"
    Ostavite WSPR-X da radi noć, a ujutro pogledajte kartu na WSPRnet-u. Vidjet ćete gdje su čuli vaš signal — izvrsno za optimizaciju antene.

### RTTY — Radioteletype

Stari digitalni mod koji i danas ima vjernu zajednicu, posebno na natjecanjima:
*   FSK (Frequency Shift Keying): 2 tona, 170 Hz razmak
*   ASCII znakovi prenose se kao niz bita
*   Contestovi: ARRL RTTY Roundup, CQ WW RTTY
*   Softver: MMTTY, fldigi, N1MM+

### Olivia

Olivia je digitalni mod dizajniran za rad u teškim uvjetima (QRM, slabi signali):
*   Varijabilni parametri: Olivia 8/250, 16/500, 32/1000 itd.
*   SNR limit do −12 dB
*   Otporniji na selektivno fedanje nego FT8
*   Popularan za EmComm i čuvanje veza u DX expeditionima

---

## Videо modovi

### ATV — Amateur Television

Analogna TV prijenos video signala na UHF/mikrovalnim opsezima:
*   Koristi PAL/NTSC video standard
*   Popularan na 70 cm i 23 cm opsezima
*   Zahtijeva pojačala i Yagi antene za domet

### DATV — Digital Amateur Television

Digitalna TV (DVB-S, DVB-T standard) — bolja slika, manje snage:
*   Radi od 23 cm (1.2 GHz) prema gore
*   Hardver: Adalm-Pluto SDR, DARC modul
*   Europska DATV zajednica: [batc.org.uk](https://www.batc.org.uk)

---

## Dijagram odluke — koji mod odabrati?

```
Gdje radite?
├── VHF/UHF (144+ MHz)?
│   ├── Lokalna veza → FM (repetitor ili simplex)
│   ├── DX veza → SSB (144.300 MHz)
│   └── Tropo/Es → SSB ili FT8 (144.174 MHz)
└── HF (< 30 MHz)?
    ├── Je li signalizacija slaba?
    │   ├── Da → FT8 (automatski) ili CW (ručno)
    │   └── Ne → SSB (razgovor) ili CW (vještina/DX)
    ├── Natjecanje?
    │   ├── SSB contest → SSB
    │   ├── CW contest → CW
    │   └── Digitalni contest → FT8/FT4/RTTY
    └── Eksperimentiranje?
        ├── Propagacija → WSPR
        ├── Tekst u realnom vremenu → PSK31 ili JS8Call
        └── Slabi signali + chat → JS8Call
```

---

## Softveri za digitalne modove

| Softver | Modovi | Platform | Link |
|---------|--------|---------|------|
| **WSJT-X** | FT8, FT4, JS8, WSPR, MSK144, JT65 | Win/Mac/Linux | [physics.princeton.edu](https://physics.princeton.edu/pulsar/k1jt/wsjtx.html) |
| **fldigi** | PSK31, RTTY, Olivia, MFSK, CW, + 20 | Win/Mac/Linux | [w1hkj.com](https://w1hkj.com) |
| **JS8Call** | JS8 | Win/Mac/Linux | [js8call.com](http://js8call.com) |
| **MMTTY** | RTTY | Windows | [hamsoft.ca](http://hamsoft.ca) |
| **Ham Radio Deluxe** | Više modova | Windows | [hamradiodeluxe.com](https://www.hamradiodeluxe.com) |
| **SDR-Console** | Digitalni via SDR | Windows | [sdr-radio.com](https://www.sdr-radio.com) |

---

## Waterfall — čitanje vizualnog spektra

Waterfall (vodopad) je frekvencijsko-vremenski prikaz koji vam pokazuje sve signale na opsegu odjednom.

Brzo prepoznavanje modova na waterfall-u:

| Mod | Izgled |
|-----|--------|
| **CW** | Uska crta, ritmički trepće (ton-pauza-ton) |
| **SSB** | Širi "oblak" 2–3 kHz, mijenja oblik s govorom |
| **FM** | Ravnomjerni pravokutnik 12–16 kHz |
| **FT8** | 8 uskih crtica u 50 Hz, pale se svakih 15 s |
| **PSK31** | Jedna uska crtica, stalna, 31 Hz široka |
| **WSPR** | Gotovo nevidljiv, 4 crte, jednom u 2 minute |
| **RTTY** | 2 paralelne crte, 170 Hz razmak |

---

## Povezane teme

*   [Modulacija i demodulacija](../technical/modulation.md) — Teorija svakog moda
*   [FT8 praktični vodič](ft8_guide.md) — Konfiguracija i rad
*   [Učenje CW](cw_learning.md) — Koch metoda i resursi
*   [Frekvencijski planovi](bandplans.md) — Gdje koristiti koji mod
