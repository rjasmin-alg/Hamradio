# TEC-15 — Modulacija i demodulacija

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/technical/modulation.md` |
| **Status** | 🔴 Ne postoji — kreirati od nule |
| **Prioritet** | P1 — Val 2 |
| **Složenost** | 🏗️ Velika |
| **Ovisnosti** | TEC-02 |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati `docs/technical/electronics.md` (ovisnost)
- [ ] Pročitati `docs/operating/modes.md` (za kontekst)
- [ ] Web search: "amplitude modulation explained simply sidebands"
- [ ] Web search: "single sideband SSB how it works filter method"
- [ ] Web search: "frequency modulation FM deviation Carson's rule"
- [ ] Web search: "FSK PSK digital modulation explained"

### Sadržaj koji treba napisati
- [ ] **Uvodni paragraf** — što je modulacija, zašto ne šaljemo izravno audio
- [ ] **Nosioc i modulirajući signal** — vizualna analogija (nosioc = prazna kutija, audio = sadržaj)
- [ ] **AM (Amplitudna modulacija):**
  - [ ] Princip — visina vala prati audio
  - [ ] Matematički izraz s MathJax
  - [ ] Spektar — nosioc + 2 bočna pojasa
  - [ ] Prednosti/mane, gdje se još koristi (zrakoplovni AM)
  - [ ] Širina pojasa: ~6-8 kHz
- [ ] **FM (Frekvencijska modulacija):**
  - [ ] Princip — frekvencija vala prati audio
  - [ ] Deviacija, Carsonovo pravilo za širinu pojasa
  - [ ] Prednosti (bez šuma), mane (puno šire)
  - [ ] FM šum naglo nestaje ispod praga (capture effect)
  - [ ] Širina pojasa: ~12-15 kHz za narrow FM
- [ ] **SSB (Jednobočna modulacija):**
  - [ ] Zašto je efikasnija od AM (3x manja širina pojasa, nema nosioca)
  - [ ] Filter metoda — phasing metoda
  - [ ] LSB vs USB — kada koji
  - [ ] PEP (Peak Envelope Power) — zašto za SSB
  - [ ] Širina pojasa: ~2.7 kHz
- [ ] **CW (Continuous Wave):**
  - [ ] OOK — On-Off Keying, najjednostavnija modulacija
  - [ ] Zašto ima best SNR i najmanji bandwidth
  - [ ] Širina pojasa: ~100-500 Hz
- [ ] **Digitalna modulacija — osnove:**
  - [ ] FSK (Frequency Shift Keying) — RTTY, telex
  - [ ] AFSK (Audio FSK) — FT8, PSK31 mode
  - [ ] PSK (Phase Shift Keying) — PSK31, BPSK
  - [ ] QAM (kvadraturna) — osnove, zašto nije u HAM-u
- [ ] **Usporedna tablica:** Mod | Vrsta modulacije | Bw (Hz) | SNR prednost | Tipična primjena
- [ ] **Vodopad (Waterfall) vizualizacija** — kako svaki mod izgleda na waterfallu
- [ ] **Admonitions** — minimalno 3
- [ ] **Interni linkovi** — modes.md, ft8_guide.md, electronics.md, bandplans.md

### Kontrola kvalitete
- [ ] Minimalno 2000 riječi
- [ ] MathJax za sve formule (AM, FM, reaktancija)
- [ ] Usporedna tablica kompletna
- [ ] **mkdocs.yml** — dodati pod Tehnika
- [ ] `.en.md` stub

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Kreiraj novu stranicu docs/technical/modulation.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- .plan/01_VIZIJA_I_STANDARDI.md
- docs/operating/modes.md  (za kontekst o modovima koje radioamateri koriste)

KORAK 2 — Istraži web:
- "amplitude modulation sidebands bandwidth explained"
- "SSB single sideband how it works vs AM"
- "FM frequency modulation deviation Carson rule"
- "PSK31 FSK digital modem modes explained"

KORAK 3 — Napiši stranicu s minimalno 2000 riječi:

# Modulacija i demodulacija

## Uvod
- Zašto ne šaljemo audio izravno (radio valovi, antene, elektromagnetski val)
- Nosioc (carrier) i modulirajući signal — analogija (kamion i teret)

## Amplitudna modulacija (AM)
- Princip: visina (amplituda) vala prati audio signal
- Matematički: s(t) = [1 + m·cos(2πfₘt)] · cos(2πfct) (MathJax)
- Spektar: nosioc + gornji bočni pojask + donji bočni pojas
- Šema spektra opisana tekstualno
- Prednosti i mane
- Gdje se koristi: zrakoplovni opseg (AM!), AM radio
- Širina pojasa: ~6-8 kHz

## Frekvencijska modulacija (FM)
- Princip: frekvencija vala se mijenja s audiom (amplituda konstantna)
- Deviacija (±5 kHz za "narrow" FM u VHF/UHF)
- Carsonovo pravilo: BW ≈ 2(Δf + fmax) (MathJax)
- Capture effect — zašto FM odbacuje slabiji signal
- Narrow FM vs Wide FM
- Prednosti: čist zvuk, bez atmospherics. Mane: širina pojasa

## Jednobočna modulacija (SSB)
- Zašto: uklonimo nosioc (gubi 2/3 snage) i jedan bočni pojas → 3x efikasnije
- Filter metoda: BPF reže jedan bočni pojas
- Phasing metoda: alternativni pristup bez filtra
- LSB (ispod 10 MHz) vs USB (iznad 10 MHz i VHF) — konvencija
- PEP snaga — zašto je mjera za SSB
- Širina pojasa: ~2.7 kHz (samo govor)

## CW (Telegrafija / Continuous Wave)
- OOK: On-Off Keying — najednostavnija digitalna modulacija
- Zašto prolazi gdje ništa drugo ne može: SNR prednost ~10-15 dB nad SSB
- Širina pojasa: filter 250-500 Hz (nasuprot 2700 Hz za SSB!)
- Zašto i danas 2.7+ milyuna aktivnih CW operatora

## Digitalna modulacija — osnove
- FSK (Frequency Shift Keying): RTTY, 2 tona (mark/space)
- AFSK: FSK generiran audiom, zvučna kartica + radio (FT8, PSK31)
- BPSK (Binary Phase Shift Keying): PSK31 — faza skače 180°
- QPSK: 4 faze, dvostruka bitska brzina
- QAM: kombinacija amplituda + faze, za LTE/WiFi ali ne za HAM

## Usporedna tablica
Mod | Vrsta modulacije | Tipična širina pojasa | SNR prednost | Primjena

## Kako izgledaju na waterfallu
- CW: uska vertikalna crta s ritmičkim prekidima
- SSB: širi "oblak" koji pulsira s govorom
- FM: široka crta, nema unutarnje strukture vidljive
- FT8: 8 uskih crtica u skupini, svakih 15 sekundi se pomiču

KORAK 4 — Tehničke smjernice:
- MathJax za SVE formule
- Usporedna tablica OBAVEZNA
- Admonitions: minimalno 3
- Interni linkovi: modes.md, ft8_guide.md, electronics.md

KORAK 5 — Spremi u docs/technical/modulation.md (nova datoteka)
KORAK 6 — Dodaj u mkdocs.yml nav → Tehnika:
  - Modulacija: technical/modulation.md
KORAK 7 — Kreiraj stub docs/technical/modulation.en.md
```

---

## Bilješke o napretku

- 
