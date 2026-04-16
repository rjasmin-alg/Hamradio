# OPR-03 — Modovi rada

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/operating/modes.md` |
| **Status** | 🟢 Postoji, treba proširiti |
| **Prioritet** | P1 — Val 1 |
| **Složenost** | 🏗️ Velika |
| **Ovisnosti** | TEC-15 |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati postojeći `docs/operating/modes.md` (~2258 bajtova)
- [ ] Pročitati `docs/technical/modulation.md` ako postoji (ovisnost)
- [ ] Web search: "FT4 vs FT8 differences ham radio"
- [ ] Web search: "PSK31 ham radio mode explained"
- [ ] Web search: "WSPR beacon weak signal propagation reporter"
- [ ] Web search: "JS8Call ham radio digital mode"
- [ ] Web search: "D-STAR DMR C4FM comparison digital voice"
- [ ] Web search: "ATV amateur television radio explained"

### Sadržaj koji treba dodati
- [ ] **CW sekcija — proširiti:**
  - [ ] Kako se šalje (taster, keyer, paddle)
  - [ ] Brzina (WPM), tipične brzine za DX, natjecanja
  - [ ] Prednosti SNR-a (15 dB bolje od SSB!)
- [ ] **SSB sekcija — proširiti:**
  - [ ] LSB vs USB razlog (konvencija ispod/iznad 10 MHz)
  - [ ] Kako izgleda SSB signal na waterfallu
  - [ ] ALC i zašto ne smijete pregasiti
- [ ] **FM sekcija — proširiti:**
  - [ ] Narrow FM (±2.5 kHz) vs Wide FM (±5 kHz)
  - [ ] CTCSS tonovi — zašto trebaju za repetitore
- [ ] **FT8 sekcija — proširiti:**
  - [ ] Kako funkcionira 15-sekundni interval
  - [ ] SNR mogućnosti (-24 dB = nevjerojatno)
  - [ ] Link na detaljni vodič ft8_guide.md
- [ ] **Novi modi — AM:**
  - [ ] Gdje se koristi još (zrakoplovni opseg, 40m AM frekvencije)
  - [ ] Zašto radioamateri preferiraju SSB
- [ ] **Novi modi — FT4:**
  - [ ] Brži od FT8 (7.5s interval), za natjecanja
- [ ] **Novi modi — JS8Call:**
  - [ ] Slobodni tekst (za razliku od FT8 automated), chat over radio
- [ ] **Novi modi — PSK31:**
  - [ ] Popularnost 2000-2010, keyborad-to-keyboard razgovor
  - [ ] BPSK31 vs QPSK31
- [ ] **Novi modi — WSPR:**
  - [ ] Beacon mod, kartografija propagacije
  - [ ] PSKReporter website
- [ ] **Novi modi — RTTY:**
  - [ ] Stariji digitalni, popularan na natjecanjima (RTTY contesti)
- [ ] **Digitalni glasovni modovi (kratko):**
  - [ ] D-STAR (Icom), DMR (handhelds), C4FM/Fusion (Yaesu) — link na dmr.md
- [ ] **ATV/DATV — kratko:**
  - [ ] Analogni i digitalni TV prijenos
- [ ] **Usporedna tablica svih modova:**
  - Stupci: Mod | Vrsta | Širina pojasa | SNR prednost | Automatiziran? | Popularnost
- [ ] **Dijagram odluke** — "Koji mod?" flowchart u tekstu
  - Kratka veza lokalno → FM/Repetitor
  - DX HF → SSB/CW/FT8
  - Jako slab signal → FT8/CW
  - Keyboard chat → JS8Call/PSK31
- [ ] **Waterfall izgled** — opis kako svaki mod izgleda na vodopadu
- [ ] **Softver** — WSJT-X (FT8/FT4/WSPR/MSK144), fldigi (PSK31/RTTY), JS8Call
- [ ] **Admonitions** — minimalno 3
- [ ] **Interni linkovi** — modulation.md, ft8_guide.md, cw_learning.md, repeaters.md, dmr.md

### Kontrola kvalitete
- [ ] Minimalno 2500 riječi ukupno
- [ ] Usporedna tablica prisutna i kompletna
- [ ] Softver lista prisutna
- [ ] `.en.md` ažuriran ili stub
- [ ] `mkdocs.yml` ne treba mijenjati

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Proširi stranicu docs/operating/modes.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- docs/operating/modes.md  (ZADRŽI SAV POSTOJEĆI SADRŽAJ!)
- .plan/01_VIZIJA_I_STANDARDI.md

KORAK 2 — Istraži web:
- "FT4 vs FT8 differences speed uses"
- "JS8Call ham radio explained chat"
- "PSK31 BPSK31 digital mode ham radio"
- "WSPR weak signal propagation reporter how it works"
- "amateur television ATV DATV ham radio"
- "D-STAR DMR C4FM comparison digital voice"

KORAK 3 — ZADRŽI sve postojeće, proširi svaki mod i dodaj nove:

Proširi CW: taster/keyer/paddle, brzine (WPM), SNR prednost (15 dB vs SSB)
Proširi SSB: LSB/USB konvencija, ALC, waterfall izgled
Proširi FM: Narrow vs Wide, CTCSS tonovi za repetitore
Proširi FT8: 15s intervali, SNR -24dB, link na ft8_guide.md

Dodaj nove sekcije:
## AM (Amplitudna modulacija)
- Gdje se još koristi, zašto HAM preferira SSB

## FT4
- Brži od FT8 (7.5s), popularan za conteste

## JS8Call
- Slobodni tekst digitalno, "keyboard-to-keyboard" ali RF

## PSK31
- BPSK31 i QPSK31, peak popularnosti 2000-2010, tihi chat

## WSPR (Weak Signal Propagation Reporter)
- Beacon mod, automatska kartografija propagacije, PSKReporter

## RTTY (Radioteleprinter)
- Stariji digitalni, živ na natjecanjima (CQWW RTTY, itd.)

## Digitalni glasovni modovi
- D-STAR (Icom), DMR (otvoreni standard), C4FM/Fusion (Yaesu) — kratki opis, link na dmr.md

## ATV/DATV
- Amaterska televizija — analogna (ATV) i digitalna (DATV)

Napravi usporednu tablicu svih modova:
Mod | Vrsta modulacije | Širina pojasa | SNR prednost | Automatiziran | Softver

Napravi "Koji mod odabrati?" textual flowchart:
- Lokalni razgovor → FM / Repetitor
- DX na HF → SSB / CW / FT8
- Samo slabi signali → FT8 ili CW
- Chat s tekstom → JS8Call / PSK31

Dodaj sekciju o softveru:
- WSJT-X: FT8, FT4, WSPR, MSK144, JT65
- fldigi: PSK31, RTTY, MT63, Olivia
- JS8Call: JS8Call protokol
- Winlink Express: email over radio

KORAK 4 — Tehničke smjernice:
- Usporedna tablica je OBAVEZNA
- Admonitions: minimalno 3
- Interni linkovi: modulation.md, ft8_guide.md, cw_learning.md, repeaters.md
- Minimalno 2500 riječi ukupno

KORAK 5 — Spremi u docs/operating/modes.md
```

---

## Bilješke o napretku

- 
