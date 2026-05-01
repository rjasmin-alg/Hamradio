# Procedura veze (QSO)

QSO je radioamaterska veza — svaki uspostavljeni razgovor između dvije ili više stanica. Procedure su međunarodne, razumljive svima bez obzira na jezik, i omogućuju efikasnu komunikaciju u loše uvjete signala.

## Osnovna terminologija

| Pojam | Značenje |
|-------|---------|
| **QSO** | Radioveza (kontakt) |
| **CQ** | Opći poziv (Calling Any Station) |
| **DE** | "Od" (Identifikacija pošiljatelja; u CW i digitalnim) |
| **K** | Prelazim na prijem (Over) |
| **KN** | Samo vi prelazite (Over to you only) |
| **AR** | Kraj poruke (Sve prenijeto) |
| **SK** | Kraj veze (Silent Key / Sign Off) |
| **CL** | Zatvaranje stanice (Closing) |
| **73** | Pozdrav (Best Regards) — nikada "73s"! |
| **88** | Ljubav i poljupci (Love and Kisses) — koristite oprezno! |

---

## Kompletna SSB veza — korak po korak

### Korak 1: Provjera frekvencije

Prije pozivanja, uvijek preslušajte frekvenciju i pitajte:
`"Is the frequency in use? QRL?"` ili na hrvatskom: `"Je li frekvencija zauzeta?"`

Pričekajte 5–10 sekundi. Ako nema odgovora — slobodno.

### Korak 2: CQ poziv (traženje veze)

```
"CQ CQ CQ, ovo je 9A1ABC, 9A1ABC, 9A1ABC, pozivam i slušam."
```

Na engleskom:
```
"CQ CQ CQ, this is 9A1ABC, 9 Alpha 1 Alpha Bravo Charlie, calling CQ and listening."
```

!!! tip "Duljina CQ poziva"
    Za standardni rad: 3× CQ, callsign 2–3 puta.
    Za DX traženje: 2× CQ DX, callsign 1–2 puta, kratko i jasno.
    Nikada nemojte zvati CQ predugo (> 30 sekundi) bez pauze za slušanje.

### Korak 3: Odgovor na CQ

Kada čujete CQ koji vas zanima:
```
"9A1ABC, ovo je DL1BBB, DL1BBC, Delta Lima 1 Bravo Bravo Charlie."
```

Ne dodajte ništa drugo u prvom javljanju — samo callsign.

### Korak 4: Uspostava veze

Stanica koja je zvala CQ odgovara:
```
"DL1BBB, ovdje 9A1ABC. Dobar dan, hvala na pozivu.
Tvoj signal je 59, 5-9. Moje ime je Ivan, gradić je Zagreb, lokator JN75ET.
Predajem. 9A1ABC K."
```

### Korak 5: Razmjena rapporta

Sugovornik odgovara:
```
"9A1ABC, hvala Ivane, dobar dan! Tvoj signal je 58, 5-8.
Moje ime je Hans, lokacija je München, Njemačka, lokator JN58UD.
Predajem DL1BBB K."
```

### Korak 6: Nastavak QSO (ragchew)

Nakon razmjene rapporta, QSO može biti kratki kontakt (contest: 1–2 izmjene) ili dugački razgovor (ragchew: 10–60 minuta). Koristite K (over) svaki put kad predajete.

### Korak 7: Završetak veze

```
"DL1BBB, hvala na veselom QSO. Tvoj signal je sada 57, 5-7.
73, čujemo se. DL1BBB de 9A1ABC SK."
```

---

## RST sustav rapporta

RST (Readability, Signal Strength, Tone) je standardni sustav ocjene kvalitete veze.

### R — Čitljivost (Readability)

| R | Opis |
|---|------|
| **1** | Nečitljivo |
| **2** | Jedva čitljivo — povremene riječi |
| **3** | Čitljivo s teškoćom |
| **4** | Čitljivo, ponekad nejasno |
| **5** | Savršeno čitljivo |

### S — Jačina signala (Signal Strength)

| S | dBm (aprox.) | Opis |
|---|-------------|------|
| **1** | −121 dBm | Jedva primjetan signal |
| **2** | −115 dBm | Vrlo slab signal |
| **3** | −109 dBm | Slab signal |
| **4** | −103 dBm | Srednji signal |
| **5** | −97 dBm | Jasan signal |
| **6** | −91 dBm | Dobri signali |
| **7** | −85 dBm | Jaki signal |
| **8** | −79 dBm | Vrlo jak signal |
| **9** | −73 dBm ili jači | Izuzetan signal |

!!! note "S-metar u praksi"
    Svaki S-stupanj = 6 dB = 4× razlika u snazi. S9 je referentna točka na većini transciivera (−73 dBm ili bolje). Raporte poput "S9+20 dB" znači signal 20 dB iznad S9 skale.

### T — Ton (Tone) — samo CW

| T | Opis |
|---|------|
| **1** | Ekstremno loš ton, neprepoznatljiv |
| **3** | Grub ton, DC modulacija |
| **5** | Modulirani zvuk s nazalom |
| **7** | Gotovo čist ton, blaga modulacija |
| **9** | Savršen ton, čist kao zvižduk |

**Za SSB**: Raport je samo R i S (npr. `"59"` = pet-devet).  
**Za CW**: Tri znamenke (npr. `"599"` = pet-devet-devet).  
**Uobičajeni contest raport**: `59(9)` — uvijek daje maksimum, stvaran ili ne.

---

## Q-kodovi

Q-kodovi su standardizirane kratice izvorno razvijene za CW telegrafiju, ali se koriste govorom i digitalnim putevima.

### Najvažniji Q-kodovi

| Kod | Kao pitanje | Kao izjava |
|-----|------------|------------|
| **QRL?** | Je li frekvencija u upotrebi? | Frekvencija je zauzeta |
| **QRM** | Imate li smetnje? | Imam smetnje (1–5) |
| **QRN** | Imate li atmosferske smetnje? | Imam atmosferski šum |
| **QRO** | Trebam li povećati snagu? | Povećajte snagu |
| **QRP** | Trebam li smanjiti snagu? | Smanjite snagu / Radim QRP |
| **QRQ** | Trebam li slati brže? | Šaljite brže |
| **QRS** | Trebam li slati sporije? | Šaljite sporije |
| **QRT** | Trebam li prestati s radom? | Prestajem raditi |
| **QRV?** | Jeste li spremni? | Spreman sam |
| **QRX** | Kada ćete me ponovo zvati? | Pričekajte — zvat ću vas u X sati |
| **QRZ?** | Tko me zove? | Zove vas X (na Y kHz) |
| **QSB** | Vari li moj signal? | Vaš signal varira |
| **QSK?** | Mogu li slati između vaših znakova? | Možete (full-break-in CW) |
| **QSL?** | Možete li potvrditi? | Potvrđujem / QSL karta |
| **QSO** | — | Radioveza |
| **QSP?** | Možete li prenijeti poruku? | Prenosim poruku |
| **QSY?** | Trebam li promijeniti frekvenciju? | Promijenite na X kHz |
| **QTH?** | Gdje se nalazite? | Moja lokacija je X |
| **QTR?** | Koliko je sati? | Točno je X UTC |

### Širi popis Q-kodova

| Kod | Značenje |
|-----|---------|
| **QRA** | Ime stanice |
| **QRB** | Udaljenost |
| **QRD** | Odredište |
| **QRG** | Točna frekvencija |
| **QRH** | Varira li moja frekvencija? |
| **QRI** | Ton signala |
| **QRK** | Čitljivost |
| **QRU** | Imate li što za mene? |
| **QRW** | Trebam li obavijestiti X? |
| **QRY** | Koji sam po redu? |
| **QSA** | Jačina signala |
| **QSD** | Ključanje je neispravno |
| **QSM** | Ponovite zadnju poruku |
| **QSN** | Jeste li me čuli? |
| **QST** | Obavijest svim radioamaterima |
| **QSU** | Trebam li slati na ovoj frekvenciji? |
| **QSW** | Hoćete li slati na ovoj frekvenciji? |
| **QTA** | Poništite poruku |
| **QTC** | Imate li poruke? |
| **QTR** | Točno vrijeme |

---

## NATO fonetska abeceda

Za jasnu identifikaciju slova u loše uvjete signala:

| Slovo | NATO naziv | Izgovor |
|-------|-----------|---------|
| A | **Alfa** | AL-fah |
| B | **Bravo** | BRAH-voh |
| C | **Charlie** | CHAR-lee |
| D | **Delta** | DELL-tah |
| E | **Echo** | ECK-oh |
| F | **Foxtrot** | FOKS-trot |
| G | **Golf** | Golf |
| H | **Hotel** | hoh-TELL |
| I | **India** | IN-dee-ah |
| J | **Juliett** | JEW-lee-ett |
| K | **Kilo** | KEY-loh |
| L | **Lima** | LEE-mah |
| M | **Mike** | Myke |
| N | **November** | no-VEM-ber |
| O | **Oscar** | OSS-car |
| P | **Papa** | pah-PAH |
| Q | **Quebec** | keh-BECK |
| R | **Romeo** | ROW-me-oh |
| S | **Sierra** | see-AIR-rah |
| T | **Tango** | TANG-go |
| U | **Uniform** | YOU-nee-form |
| V | **Victor** | VIK-tah |
| W | **Whiskey** | WISS-key |
| X | **X-ray** | ECKS-ray |
| Y | **Yankee** | YANG-key |
| Z | **Zulu** | ZOO-loo |

!!! note "Numeričko fonetika"
    Brojevi u lošim uvjetima: 0=Zero, 1=One (wun), 2=Two (too), 3=Three (tree), 4=Four (fow-er), 5=Five (fife), 6=Six, 7=Seven (SEV-en), 8=Eight (ate), 9=Nine (niner)

---

## Procedura za pile-up (DX veza)

Kada radite DX ekspediciju ili rijetku staniciju koja prima puno poziva:

### Za raritetnu DX postaju

1.  **Jasno najavite "UP 5"** ili "SPLIT, listening 14.205–14.210" — slušate 5+ kHz više
2.  Radite sistematično — zvovite samo ona slova koja tražite: `"Zovim samo 9A"` ili `"Zovim slova K–M"`
3.  Dajte kratke rapporte — samo što treba za log
4.  Potvrdite callsign jasno: `"9A1ABC, 59, QSL?"`

### Za staniciju koja zove rijetki DX

1.  **Slušajte gdje DX sluša** — ne zovite na TX frekvenciji!
2.  Identificirajte samo s callsignom — bez `"73"`, bez `"de"`, samo: `"9A1ABC"`
3.  Strpljivo čekajte — ne probijajte drugima
4.  Ne zovite ako DX traži drugu regiju ili slova koja nisu vaša

---

## Mayday i hitne procedure

Prioritet iznad svakog QSO-a.

**Signali opasnosti:**
*   **MAYDAY, MAYDAY, MAYDAY** (govor) — opasnost po život
*   **SOS (··· − − − ···)** (CW) — isti prioritet
*   **PAN-PAN, PAN-PAN, PAN-PAN** (govor) — hitnost bez neposredne opasnosti

**Format MAYDAY poziva:**
```
"MAYDAY, MAYDAY, MAYDAY.
Ovo je [callsign/ime broda/ime osobe].
MAYDAY [callsign].
Nalazim se na [lokacija].
[Opis problema].
Ima nas [broj osoba].
[Zahtjev za pomoć].
Over."
```

!!! danger "Hitno"
    Ako čujete MAYDAY: odmah prestanite s odašiljanjem, slušajte, zabilježite sve podatke i koordinirajte s hitnim službama. Nemojte zauzimati frekvenciju nepotrebnim odgovorima ako već postoji koordinator.

---

## Lokatorski sustav (Maidenhead Grid)

Maidenhead Grid Locator je sustav koji opisuje geografsku lokaciju dvjema slovima i dvama brojevima (i opcijskim dvama slovima za preciznost):

`JN75ET` = polje 10×20 km u okolici Zagreba

*   Koristi se u contestovima, za izračun udaljenosti (km), u VHF/UHF radu
*   [**Kalkulator lokatora**](https://www.levinecentral.com/ham/grid_square.php)
*   [**QRZ lookup lokator**](https://www.qrz.com) — svaka callsign stranica prikazuje lokator

---

## Povezane teme

*   [Modovi rada](modes.md) — Koji mod za koji tip veze
*   [Logbook (dnevnik rada)](logbook.md) — Bilježenje veza
*   [DX rad](../activities/dxing.md) — DX etiketa i pile-up
*   [Radioamaterska etika](../regulations/ethics.md) — Ponašanje na opsegu
