# OPR-07 — Učenje CW (Morseov kod)

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/operating/cw_learning.md` |
| **Status** | 🔴 Ne postoji — kreirati od nule |
| **Prioritet** | P1 — Val 2 |
| **Složenost** | 🔧 Srednja |
| **Ovisnosti** | OPR-03 |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati `docs/operating/modes.md` (CW sekcija)
- [ ] Web search: "Koch method Morse code learning most efficient"
- [ ] Web search: "LCWO.net Morse code practice review"
- [ ] Web search: "straight key vs paddle vs bug Morse key differences"
- [ ] Web search: "Morse code prosigns abbreviations ham radio list"
- [ ] Web search: "CW QSO typical abbreviations RS RST"

### Sadržaj koji treba napisati
- [ ] **Uvodni paragraf** — zašto CW, tradicija, prednosti
- [ ] **Zašto naučiti CW:**
  - [ ] SNR prednost (15 dB > SSB, 10 dB > WSPR)
  - [ ] Domet — prolazi kad ništa drugo ne prolazi
  - [ ] Jednostavna oprema — odašiljač od 1W + dipol
  - [ ] Tradicija — Over 100 godina, živi i danas
  - [ ] Privilegije — A razred, CW-only opsezi (ispod 14.070)
- [ ] **Koch metoda:**
  - [ ] Princip — naučiti znakove pri PUNOJ brzini (20-25 WPM)
  - [ ] Zašto ne počinjati polako (muscle memory problem)
  - [ ] Redoslijed znakova (Koch preporučeni)
  - [ ] Korak po korak: svaki dan 15-20 minuta
- [ ] **Online tečajevi i alati:**
  - [ ] LCWO.net — najpoznatiji, besplatan, Koch online
  - [ ] MorseCode.World — vizualni, dobar za početnike
  - [ ] JustLearnMorseCode — Windows aplikacija
  - [ ] G4FON Koch trainer — Windows, dugo provjeren
  - [ ] Ham Morse (mobilna app)
  - [ ] CW Academy (ARRL/CWops) — strukturirani tečaj
- [ ] **Preporučeni redoslijed znakova (Koch)**
  - [ ] Kompletna tablica: redni broj | znak | brzina uvođenja
- [ ] **Razine napretka:**
  - [ ] 5 WPM — elementarno, može pratiti sporije QSO
  - [ ] 12 WPM — CEPT minimalni zahtjev (bivši)
  - [ ] 20 WPM — tečan DX QSO, natjecanje
  - [ ] 30+ WPM — contesting, top operatori
- [ ] **Taster (Key) — vrste:**
  - [ ] Straight Key — ravni taster, za učenje i nostalgiju
  - [ ] Paddle (Iambic) — elektronički keyer, automatske točke/crtice
  - [ ] Bug (Semi-automatic) — poluautomatski, vintage stil
  - [ ] Tablica usporedbe: Tip | Za koga | Prednosti | Mane
- [ ] **Keyer — što je, kako podesiti:**
  - [ ] Speed control, weight, ratio point/dash
  - [ ] Ugrađeni vs vanjski keyer
- [ ] **Skraćenice u CW QSO-u:**
  - [ ] Kompletna tablica najčešćih (GM, GA, GE, ES, DE, UR, RST, TNX, 73, 88...)
  - [ ] Prosignali: AR, SK, BK, KN, DN
- [ ] **Tipičan CW QSO — transkript:**
  - [ ] Primjer u code bloku s pojašnjenjima
- [ ] **Savjeti za napredak:**
  - [ ] Svakodnevno slušanje KLJUČNO (radio na CW porcijama)
  - [ ] CW Skimmer za vizualizaciju
  - [ ] Ne "gledati" u abecedu dok prima
- [ ] **Admonitions** — minimalno 3 (tip za Koch, note za redoslijed, info za alate)
- [ ] **Interni linkovi** — modes.md, procedures.md, first_qso.md

### Kontrola kvalitete
- [ ] Minimalno 2000 riječi
- [ ] Koch redoslijed tablica prisutna
- [ ] Tablica vrsta tastera prisutna
- [ ] Skraćenice tablica prisutna
- [ ] CW QSO transkript u code bloku
- [ ] **mkdocs.yml** — dodati pod Rad na opsegu
- [ ] `.en.md` stub

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Kreiraj novu stranicu docs/operating/cw_learning.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- .plan/01_VIZIJA_I_STANDARDI.md
- docs/operating/modes.md  (CW sekcija)

KORAK 2 — Istraži web:
- "Koch method Morse code learning order characters"
- "LCWO.net review Morse code practice"
- "straight key vs paddle vs bug iambic comparison"
- "CW QSO abbreviations prosigns ham radio list"

KORAK 3 — Napiši stranicu s minimalno 2000 riječi:

# Učenje Morseovog koda (CW)

## Zašto naučiti CW?
- SNR prednost: 15 dB bolje od SSB (+ prolazi uvjeti koji SSB ne mogu)
- Jednostavna oprema: 1W TX + žičana antena = interkontinentalni QSO
- Tradicija: najstariji radio mod, živi i dinamično se razvija

## Koch metoda — najefikasnija
- Princip: svaki znak uvode se pri PUNOJ brzini (20-25 WPM)
- Zašto ne polako: mozak piče "ritmičke obrasce", ne individualne zvukove
- Svaki dan 15-20 minuta, 2 nova znaka tjedno

Koch redoslijed (tablica: Redni br. | Znak | Zvuk)
K M R S U .... (kompletni Koch redoslijed 40 znakova)

## Alati i tečajevi
Tablica: Alat | Platforma | Cijena | Prednosti
- LCWO.net: Web, Free, Koch online, statistike
- MorseCode.World: Web, Free, vizualni pristup  
- JustLearnMorseCode: Windows, Free, Koch trainer
- G4FON: Windows, Free, provjeren klasik
- Ham Morse: Android/iOS, Paid, mobile
- CW Academy: Online tečaj (ARRL), strukturirani sa mentorom

## Razine napretka
Tablica: WPM | Opis | Što možeš
- 5-8: Sporo, svaki znak razdvojen, praćenje uz napor
- 10-12: Bivši CEPT minimum, uočljivo QSO
- 15-20: Tečan HF QSO, DX
- 20-25: Contesting, pile-up, DX expedition
- 30+: Top operatori, natjecanja

## Taster (Key)
Tablica: Tip | Opis | Za koga | Preporučeni model
- Straight key (ravni): Direkt veza, za učenje, nostalgija
- Paddle (iambic): Elektronički keyer, brže i lakše
- Bug (semi-auto): Automatske točke, ručne crtice — vitnage

Keyer: podesiti speed (WPM), weight (odnos punjenje/praznina)

## Skraćenice u CW QSO-u
Tablica: Kratica | Puni naziv | Primjer upotrebe
GM/GA/GE, ES, DE, UR, HR, BK, HW?, TU, TNX, 73, 88, AGN, PSE, QSL...
(Minimalno 30 kratica)

## Prosignali
Tablica: Prosignal | Znači | Kada koristiti
AR, SK, BK, KN, DN

## Primjer CW QSO (annotiran)
```
CQ CQ DE 9A1ZG 9A1ZG K     # CQ poziv (K = over)
DJ3AB DE 9A1ZG GE OM       # pozdrav
UR RST 599 599 NAME JASMIN  # RST i ime
QTH ZAGREB ZAGREB ES HW?   # QTH i pitanje
BK                          # pauza za odgovor
...
73 TU ES GL DE 9A1ZG SK    # kraj QSO (SK = end of work)
```

## Savjeti za brži napredak
- 15-20 min SVAKI DAN — konzistentnost je ključ
- Nikad ne gledaj u abecedu dok primaš — nauci sound-pattern
- Slušaj CW stanice na radijo — online (WebSDR), AFSK
- CW Skimmer — vizualizacija CW prometa na waterfall

KORAK 4 — Tehničke smjernice:
- Tablica Koch redoslijeda OBAVEZNA
- Tablica skraćenica OBAVEZNA
- Code blok za primjer QSO
- Admonitions: minimalno 3
- Interni linkovi: modes.md, procedures.md, first_qso.md

KORAK 5 — Spremi u docs/operating/cw_learning.md (nova datoteka)
KORAK 6 — Dodaj u mkdocs.yml nav → Rad na opsegu:
  - Učenje Morseovog koda: operating/cw_learning.md
KORAK 7 — Kreiraj stub docs/operating/cw_learning.en.md
```

---

## Bilješke o napretku

- 
