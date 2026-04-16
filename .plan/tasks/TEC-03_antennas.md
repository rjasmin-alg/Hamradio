# TEC-03 — Antene i vodovi

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/technical/antennas.md` |
| **Status** | 🟢 Postoji, treba proširiti |
| **Prioritet** | P1 — Val 1 |
| **Složenost** | 🏗️ Velika |
| **Ovisnosti** | TEC-02 |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati postojeći `docs/technical/antennas.md` (~2570 bajtova)
- [ ] Pročitati `docs/technical/electronics.md` (ovisnost)
- [ ] Web search: "antenna radiation pattern explained simply"
- [ ] Web search: "antenna gain dBi dBd difference ham radio"
- [ ] Web search: "balun unun explanation ham radio"
- [ ] Web search: "end-fed antenna EFHW construction"
- [ ] Web search: "coax cable loss per 100m frequency table"

### Sadržaj koji treba dodati
- [ ] **Teorija antena — uvod** — kako antena pretvara struju u EM val
- [ ] **Polarizacija** — horizontalna, vertikalna, kružna — kad koja
- [ ] **Dijagram zračenja** — omni vs directional, lobes, front-to-back omjer
- [ ] **Dobitak antene** — dBi vs dBd, objašnjenje na primjeru, zašto nije "besplatna energija"
- [ ] **Impedancija antene** — 50Ω, 75Ω, 300Ω, zašto prilagodba
- [ ] **Nove vrste antena:**
  - [ ] End-Fed Half-Wave (EFHW) — s 49:1 transformatorom
  - [ ] Magnetic Loop — princip, prednosti za ograničen prostor
  - [ ] Quad antena — princip rada, prednosti nad Yagi
  - [ ] J-Pole / Slim Jim — VHF/UHF, DIY
  - [ ] Log-Periodic (LP) — multiband, broadcast stile
- [ ] **Balun i Unun** — razlika, kada koristiti koji, impedancijski omjeri (1:1, 4:1, 9:1, 49:1)
- [ ] **Koaksijalni kabel — detaljno:**
  - [ ] Usporedna tablica: RG-58, RG-213, LMR-400, Aircell-7 (gubitak dB/100m @ razne frekvencije)
  - [ ] Kako pravilno spojiti PL-259 konektor
- [ ] **Ladder line (dvožilni vod)** — 300Ω, 450Ω, prednosti za multiband
- [ ] **Praktični savjeti za antenu** — visina iznad tla, radijali za vertikalke, uzemljenje
- [ ] **Admonitions** — minimalno 3
- [ ] **Interni linkovi** — electronics.md, transmission_lines.md, safety.md, antenna_tuners.md

### Kontrola kvalitete
- [ ] Minimalno 2500 riječi ukupno
- [ ] Formule u MathJax: $\lambda/2$ dipol duljina $= \frac{143}{f_{MHz}}$ m
- [ ] Tablica gubitaka kabela kompletna
- [ ] `.en.md` ažuriran ili stub
- [ ] `mkdocs.yml` ne treba mijenjati

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Proširi stranicu docs/technical/antennas.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- docs/technical/antennas.md  (ZADRŽI SAV POSTOJEĆI SADRŽAJ!)
- .plan/01_VIZIJA_I_STANDARDI.md

KORAK 2 — Istraži web:
- "antenna radiation pattern explained"
- "dBi vs dBd antenna gain difference"
- "balun unun ham radio when to use"
- "end-fed half wave antenna EFHW 49:1 transformer"
- "coaxial cable loss table RG-58 RG-213 LMR-400 frequency"

KORAK 3 — ZADRŽI sve postojeće, proširi i dodaj sekcije:

## Teorija antena
- Kako antena pretvara AC struju u EM val
- Polarizacija: horizontalna / vertikalna / kružna — kada što koristiti
- Dijagram zračenja: omni vs usmjerena, lobes, F/B omjer

## Dobitak antene (Gain)
- dBi (referenca: izotropna antena) vs dBd (referenca: dipol)
- Konverzija: 0 dBd = 2.15 dBi
- Zašto dobitak nije "besplatna energija" — usmjeravanje, ne pojačavanje
- Praktični primjer: Yagi 10 dBd = 12.15 dBi

## Impedancija i prilagodba
- Zašto antenama treba 50Ω prilagodba
- SWR kao mjera neslaganja impedancije

## Nove vrste antena
- End-Fed Half-Wave (EFHW) — princip i 49:1 transformer
- Magnetic Loop — za ograničen prostor, visoki Q
- Quad — kvadratni dipol, prednosti vs Yagi
- J-Pole / Slim Jim — VHF/UHF simplex
- Log-Periodic — multiband direktiva

## Balun i Unun
- Balun (balanced-unbalanced): za dipole, omjeri 1:1 i 4:1
- Unun (unbalanced-unbalanced): za end-fed i vertikalke, omjeri 4:1, 9:1, 49:1
- Tablica: Situacija | Tip | Omjer

## Koaksijalni kabel — detaljno
- Tablica gubitaka: Kabel | Gubitak na 50MHz | 144MHz | 432MHz | 1296MHz (dB/100m)
- Tipovi: RG-58, RG-213, LMR-400, Aircell-7, H-2000
- Kako pravilno montirati PL-259

## Dvožilni vod (Ladder Line)
- 300Ω i 450Ω — prednosti za multiband s tunerom

## Praktični savjeti
- Optimalna visina dipola (λ/2 = 10m za 20m bend)
- Radijali za vertikalke
- Zaštita od groma (link na grounding.md)

KORAK 4 — Tehničke smjernice:
- MathJax za formule
- Tablice za kabele i balune
- Admonitions: minimalno 3
- Interni linkovi: electronics.md, safety.md

KORAK 5 — Spremi u docs/technical/antennas.md
```

---

## Bilješke o napretku

- 
