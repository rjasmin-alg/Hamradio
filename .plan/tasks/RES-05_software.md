# RES-05 — Softver za radioamatere

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/resources/software.md` |
| **Status** | 🔴 Ne postoji — kreirati od nule |
| **Prioritet** | P1 — Val 2 |
| **Složenost** | 🔧 Srednja |
| **Ovisnosti** | — |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Web search: "best ham radio logging software comparison 2024"
- [ ] Web search: "WSJT-X fldigi JS8Call download review"
- [ ] Web search: "SDR# SDRuno Gqrx HDSDR comparison"
- [ ] Web search: "MMANA-GAL 4NEC2 antenna modeling software"
- [ ] Web search: "ham radio apps Android iOS 2024"

### Kategorije i softver koji treba pokriti

#### Logiranje (Logging)
- [ ] N1MM+ — Windows, Free — contest logging
- [ ] Log4OM v2 — Windows, Free/Paid — general logging
- [ ] DXKeeper — Windows, Free, dio DXLab suite
- [ ] CloudLog — Web/PHP self-hosted, Free — moderan
- [ ] Ham Radio Deluxe — Windows, Paid (nekad Free)
- [ ] MacLoggerDX — Mac, Paid

#### Digitalni modovi (Digital Modes)
- [ ] WSJT-X — Windows/Mac/Linux, Free — FT8, FT4, WSPR, MSK144
- [ ] fldigi — Windows/Mac/Linux, Free — PSK31, RTTY, Olivia, MFSK
- [ ] JS8Call — Windows/Mac/Linux, Free — JS8 slobodni tekst
- [ ] Winlink Express — Windows, Free — email over radio
- [ ] MultiPSK — Windows, Shareware — sve digitalne modove

#### SDR (Software Defined Radio)
- [ ] SDR# (SDRSharp) — Windows, Free — popularan za RTL-SDR
- [ ] HDSDR — Windows, Free — dobar UI
- [ ] SDRuno — Windows, Free (za SDRPlay uređaje)
- [ ] Gqrx — Linux/Mac, Free, open source
- [ ] CubicSDR — Windows/Mac/Linux, Free, cross-platform
- [ ] OpenWebRX — Web, Free, za dijeljene SDR uređaje

#### Antene (Antenna Modeling)
- [ ] MMANA-GAL — Windows, Free — standard za žičane antene
- [ ] 4NEC2 — Windows, Free — NEC2 baziran, napredniji
- [ ] EZNEC (demo) — Windows, Paid — komercijalni standard
- [ ] Antenna Magus — Paid, enterprise

#### Propagacija (Propagation)
- [ ] VOACAP Online — Web, Free — HF propagacija
- [ ] HamClock — Linux/Pi/Web — all-in-one display
- [ ] DX Atlas — Windows, Paid — mapa i propagacija
- [ ] Solar Terrestrial Dispatch (SolarHam.com) — web

#### Sateliti (Satellites)
- [ ] Gpredict — Windows/Linux/Mac, Free — tracking i Doppler
- [ ] SatPC32 — Windows, Free — CAT integracija za Doppler

#### CW vježba
- [ ] LCWO.net — Web, Free — Koch method online
- [ ] Just Learn Morse Code — Windows, Free
- [ ] G4FON Koch Trainer — Windows, Free
- [ ] Morse Trainer (Android/iOS) — mobilna

#### Radio kontrol (CAT/Hamlib)
- [ ] Hamlib — multiplatform biblioteka (temelj svega)
- [ ] OmniRig — Windows COM biblioteka, koriste mnoge apps
- [ ] flrig — Windows/Mac/Linux, grafični frontend za Hamlib

#### Mobilne aplikacije
- [ ] HamAlert — iOS/Android — propagacija, DX spot notifikacije
- [ ] RepeaterBook — iOS/Android — baza repetitora
- [ ] APRS.fi — Web/iOS/Android — APRS tracking
- [ ] SOTA Goat / SOTA Spotter — iOS/Android — SOTA alarms/spotting
- [ ] POTA — iOS/Android — POTA management
- [ ] QRZ — iOS/Android/Web — callsign lookup
- [ ] Ham Clock — iOS/Android — sat za radioamatere

### Format svake kategorije
Za svaki softver:
- [ ] Naziv s linkom
- [ ] Opis (1-2 rečenice na HR)
- [ ] Platforma: Windows / Mac / Linux / Web / Android / iOS
- [ ] Cijena: Free / Donationware / Shareware / Paid ($xx)
- [ ] Preporučeno za: (tip korisnika)

### Ostalo
- [ ] **Uvodni paragraf** — zašto je softver bitan u modernom radioamaterizmu
- [ ] **Admonitions** — minimalno 2 (tip za preporučenu listu za početnike, note za licence)
- [ ] **"Starter pack" sekcija** — 5 programa za početnika (WSJT-X, N1MM/Log4OM, MMANA, Gpredict, LCWO)
- [ ] **Interni linkovi** — ft8_guide.md, contesting.md, satellites.md, cw_learning.md

### Kontrola kvalitete
- [ ] Minimalno 1500 riječi
- [ ] Svaka kategorija ima tablicu
- [ ] Minimalno 30 programa pokriveno
- [ ] **mkdocs.yml** — dodati pod Resursi
- [ ] `.en.md` stub

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Kreiraj novu stranicu docs/resources/software.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- .plan/01_VIZIJA_I_STANDARDI.md

KORAK 2 — Istraži web:
- "ham radio logging software comparison 2024 N1MM Log4OM CloudLog"
- "SDR software comparison SDRSharp HDSDR Gqrx 2024"
- "antenna modeling software ham radio free MMANA 4NEC2"
- "ham radio mobile apps Android iOS 2024 best"

KORAK 3 — Napiši stranicu s minimalno 1500 riječi, 30+ programa:

# Softver za radioamatere

## Uvod
Kratki opis zašto računalo postalo neodvojivi dio moderne ham radio stanice.

## Kako koristiti ovaj popis
- Kratki "Starter Pack": 5 programa za početnike (WSJT-X, Log4OM, MMANA-GAL, HamAlert, LCWO)

## Logiranje
Tablica: Naziv | Link | Opis (HR) | Platforma | Cijena | Za koga
N1MM+ | n1mm.hamdocs.com | Vodeći contest logger | Win | Free | Contesteri
Log4OM v2 | log4om.com | Kompletan general logger | Win | Free/Pro | Svi
DXKeeper | dxlabsuite.com | Dio DXLab paketa | Win | Free | DX lovci
CloudLog | github.com/magicbug/Cloudlog | Web-based, self-host | Web | Free | Modernisti
Ham Radio Deluxe | hamradiodeluxe.com | Sve-u-jednom | Win | Paid | Kompletan setup

## Digitalni modovi
Tablica:
WSJT-X | physics.princeton.edu | FT8/FT4/WSPR/MSK144 | Win/Mac/Linux | Free
fldigi | w1hkj.com | PSK31/RTTY/Olivia/MFSK | Win/Mac/Linux | Free
JS8Call | js8call.com | Slobodni tekst JS8 | Win/Mac/Linux | Free
Winlink Express | winlink.org | Email over radio | Win | Free
MultiPSK | f6cte.free.fr | 100+ modova | Win | Shareware

## SDR (Software Defined Radio)
Tablica: (SDR#, HDSDR, SDRuno, Gqrx, CubicSDR, OpenWebRX)

## Modeliranje antena
Tablica: (MMANA-GAL, 4NEC2, EZNEC demo)

## Propagacija
Tablica: (VOACAP, HamClock, DX Atlas, SolarHam)

## Sateliti
Tablica: (Gpredict, SatPC32)

## CW vježba
Tablica: (LCWO, Just Learn Morse Code, G4FON, mobilne)

## Radio kontrol (CAT)
Tablica: (Hamlib, OmniRig, flrig)

## Mobilne aplikacije
Tablica: Naziv | iOS | Android | Opis | Cijena
HamAlert | ✓ | ✓ | DX spot notifikacije | Free
RepeaterBook | ✓ | ✓ | Baza repetitora | Free
APRS.fi | ✓ | ✓ | APRS tracking | Free
SOTA Goat | ✓ | ✓ | SOTA alerts i spotting | Free/Paid
QRZ | ✓ | ✓ | Callsign lookup | Free/Premium

KORAK 4 — Tehničke smjernice:
- Svaka kategorija = zasebna tablica
- Admonitions: minimalno 2
- Interni linkovi: ft8_guide.md, contesting.md, satellites.md, cw_learning.md

KORAK 5 — Spremi u docs/resources/software.md (nova datoteka)
KORAK 6 — Dodaj u mkdocs.yml nav → Resursi:
  - Softver: resources/software.md
KORAK 7 — Kreiraj stub docs/resources/software.en.md
```

---

## Bilješke o napretku

- 
