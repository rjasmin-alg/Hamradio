# OPR-06 — FT8 praktični vodič

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/operating/ft8_guide.md` |
| **Status** | 🔴 Ne postoji — kreirati od nule |
| **Prioritet** | P1 — Val 2 |
| **Složenost** | 🏗️ Velika |
| **Ovisnosti** | OPR-03, TEC-17 |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati `docs/operating/modes.md` (kontekst FT8)
- [ ] Web search: "WSJT-X FT8 setup guide Windows 2024"
- [ ] Web search: "FT8 audio interface CAT control radio PC"
- [ ] Web search: "FT8 waterfall decode screen explained"
- [ ] Web search: "FT8 etiquette power levels best practices"
- [ ] Web search: "LoTW ClubLog PSKReporter upload FT8 log"

### Sadržaj koji treba napisati
- [ ] **Uvodni paragraf** — što je FT8, revoliucija u hobiju
- [ ] **Kratka teorija** — 15-sekundni intervali, 8-FSK, SNR do -24dB, zašto je poseban
- [ ] **Što je K1JT/K9AN** — kratko o autorima, WSJT-X historija
- [ ] **Oprema — kompletna lista:**
  - [ ] Radio s CAT portom (serijski ili USB)
  - [ ] Računalo (Windows/Linux/Mac)
  - [ ] Zvučni kabel ili interna zvučna kartica
  - [ ] USB-Serial adapter ako nema COM porta
  - [ ] Preporučene kombinirane kartice (SignaLink, DigiRig, etc.)
- [ ] **Instalacija WSJT-X na Windows — step by step:**
  - [ ] Preuzimanje s physics.princeton.edu
  - [ ] Instalacija
  - [ ] Sinkronizacija vremena (KLJUČNO!)
  - [ ] Windows Time vs Meinberg NTP vs internet sync
- [ ] **Konfiguracija WSJT-X — svaki prozor:**
  - [ ] General: pozivna, grid locator (QTH locator!)
  - [ ] Radio: CAT (port, baud rate, tip handshaking)
  - [ ] Audio: ulazni i izlazni uređaj
  - [ ] PTT: putem CAT ili zasebni port
  - [ ] Reporting: Logger32, LoTW, ClubLog
- [ ] **QTH Locator (Grid Square)** — što je, kako ga pronaći
- [ ] **Tvoja prva FT8 veza — korak po korak:**
  - [ ] Uključiti radio na FT8 frekvenciju (npr. 14.074 za 20m USB)
  - [ ] Audio razina — kako podesiti (ALC na nuli!)
  - [ ] Slušati bez odašiljanja prvih 10 minuta
  - [ ] Kliknuti na signal u waterfallu
  - [ ] Enable Tx — promatrati auto sequence
  - [ ] Log QSO
- [ ] **Čitanje decode prozora** — što znači svaka kolona:
  - Datum, Čas (UTC), dB (SNR), DT (timing), frekvencija, mod, poruka
  - Boje: crna, zelena, crvena, žuta — što svaka znači
- [ ] **Čitanje waterfall prikaza:**
  - Frekvencija, boja = jačina, FT8 signal trajanje
- [ ] **FT8 etiketa:**
  - Koristiti razumnu snagu (25-50W više nego dovoljno u normalnim uvjetima!)
  - Ne pozivati CQ kad je frekvencija zauzeta
  - En-band vs određena frekvencija
- [ ] **Logiranje i upload:**
  - [ ] LoTW (Logbook of The World) — ARRL, za DXCC
  - [ ] ClubLog — statistike, OQRS
  - [ ] PSKReporter — propagacijska mapa (automatski)
  - [ ] eQSL — alternativa
- [ ] **Troubleshooting — česti problemi:**
  - [ ] "No CAT" — COM port, baud rate, driver
  - [ ] Nema decoda — audio razina, timing, frekvencija
  - [ ] Transmit ne radi — PTT, konfiguracija
  - [ ] Timing greška — sinkroniziraj sat
- [ ] **Admonitions** — minimalno 4 (tip, warning, note, danger za ALC)
- [ ] **Interni linkovi** — modes.md, logbook.md, awards.md, propagation.md

### Kontrola kvalitete
- [ ] Minimalno 3000 riječi
- [ ] Step-by-step instalacija kompletna
- [ ] Step-by-step prva veza kompletna
- [ ] Troubleshooting sekcija prisutna
- [ ] **mkdocs.yml** — dodati pod Rad na opsegu
- [ ] `.en.md` stub

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Kreiraj novu stranicu docs/operating/ft8_guide.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- .plan/01_VIZIJA_I_STANDARDI.md
- docs/operating/modes.md  (FT8 sekcija za kontekst)

KORAK 2 — Istraži web:
- "WSJT-X FT8 setup guide Windows step by step 2024"
- "FT8 CAT control audio interface options SignaLink DigiRig"
- "FT8 waterfall decode window explained columns colors"
- "FT8 power level etiquette ham radio"
- "LoTW ClubLog PSKReporter FT8 upload setup"

KORAK 3 — Napiši stranicu s minimalno 3000 riječi:

# FT8 — Praktični vodič

## Što je FT8 i zašto je revolucionaran
- Nastanak 2017 (K1JT Joe Taylor + K9AN Steve Franke)
- 15-sekundni intervali, SNR do -24dB (hears signals humans cannot!)
- Broj QSO-a eksplodirao — danas >50% svih HF QSO

## Kratka teorija
- 8-FSK modulacija, 15s intervali (parne/neparne minute)
- Poruka: 77 bita informacije, 60 bita forward error correction
- Zašto prolazi kad SSB ne može (narrow bandwidth + error correction)

## Potrebna oprema  
Tablica: Komponenta | Opis | Preporuka | Alternativa
- Radio s CAT sučeljem
- Računalo (bilo koji OS)
- Audio sučelje (kabel ili kartica)
  - Budget: direktni kabel audio in/out
  - Preporučeno: SignaLink USB, DigiRig Mobile, Kenwood IF-232C
- USB-Serial adapter (ako radio nema USB)

## Instalacija WSJT-X na Windows (step by step)
1. Preuzmi sa: https://physics.princeton.edu/pulsar/k1jt/wsjtx.html
2. Pokreni installer (Next, Next, Install...)
3. KRITIČNO: Sinkroniziraj sat na sekundi!
   - Preporučeno: Meinberg NTP ili Windows Time service na internet.time.server
   !!! warning "Sat mora biti točan na ±1 sekundu, inače nema decoda!"

## Konfiguracija WSJT-X
### Kartica General
- My Call: TVOJA pozivna oznaka (9A1ZG)
- My Grid: QTH locator (JN85...)
  !!! tip "Pronađi svoj grid na: https://www.qthlocator.com/"
### Kartica Radio
- Rig: odaberi model radija
- Serial Port: COM port (pronađi u Device Manager)
- Baud Rate: prema korisničkom priručniku radija (obično 9600 ili 19200)
### Kartica Audio
- Input: odaberi zvučnu karticu/audio sučelje koje prima iz radija
- Output: odaberi zvučnu karticu/audio sučelje koje šalje u radio
### Kartica PTT
- Koristiti CAT (preferred) ili RTS/DTR na serijskom portu

## Tvoja prva FT8 veza (korak po korak)
1. Podesi frekvenciju: 14.074 MHz, mod USB
2. Provjeri ALC: mora biti na NULI pri odašiljanju FT8!
   !!! danger "ALC aktivnost = iskrivljeni signal = smetnje susjednim stanicama!"
3. Slušaj 5-10 minuta, promatraj waterfall
4. Klikni na zanimljivi CQ signal
5. Double-click → automatski se postavi Tx poruka
6. Klikni "Enable Tx" u 0 ili 15 sekundi intervala
7. Promatraj auto-sequence (6 razmjena, završava s 73)
8. Log QSO, čestitamo!

## Čitanje decode prozora
Tablica: Kolona | Opis | Primjer
- UTC | Čas poruke | 143045 = 14:30:45
- dB | SNR (Signal-to-Noise Ratio) | -12 dB
- DT | Vremenski offset od intervala | +0.3
- Freq | Audio frekvencija | 1247 Hz
- Msg | Sadržaj poruke | CQ DX 9A1ZG JN85

Boje u prozoru:
- Crna: normalne poruke
- Zelena: netko zove tebe
- Crvena: moja odlazna poruka
- Žuta: DX (udaljena zemlja)

## Waterfall prikaz
- X os: frekvencija (audio, 200-3000 Hz)
- Y os: vrijeme (5-10 sekundi vidljivo unazad)
- Boja: intenzitet signala (plava = slab, crvena = jak)
- FT8 signal: skupina 8 paralelnih linija, 12.64 sekundi vidljivi

## Etiketa
- Snaga: 25-50W je obično dovoljno, ne koristite 100W na europskim opsezima!
- Ne koristiti Auto-Seq bez nadzora
- Paziite na DX windows (14.090-14.100 MHz samo za beacon)

## Logiranje i upload
- LoTW: službeni za DXCC diplome (zahtijeva certifikat)
- ClubLog: automatski upload iz WSJT-X, OQRS
- PSKReporter: propagacijska mapa, automatski u pozadini
- eQSL: alternativa LoTW-u

## Troubleshooting
Tablica: Problem | Uzrok | Rješenje
- No CAT → Com port, Driver, Baud rate
- Nema decoda → Razina audija, Timing, Frekvencija
- Transmit ne radi → PTT postavke, Vox/CAT
- Timing greška → Sinhronizacija sata

KORAK 4 — Tehničke smjernice:
- Code blokovi za primjere poruka
- Tablice za opremu, decode prozor, troubleshooting
- Admonitions: minimalno 4 (!!! danger za ALC i timing, !!! tip za grid)
- Interni linkovi: modes.md, logbook.md, propagation.md

KORAK 5 — Spremi u docs/operating/ft8_guide.md (nova datoteka)
KORAK 6 — Dodaj u mkdocs.yml nav → Rad na opsegu:
  - FT8 vodič (WSJT-X): operating/ft8_guide.md
KORAK 7 — Kreiraj stub docs/operating/ft8_guide.en.md
```

---

## Bilješke o napretku

- 
