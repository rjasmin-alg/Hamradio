# TEC-02 — Osnove elektronike

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/technical/electronics.md` |
| **Status** | 🟢 Postoji, treba proširiti |
| **Prioritet** | P1 — Val 1 |
| **Složenost** | 🏗️ Velika |
| **Ovisnosti** | — |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati postojeći `docs/technical/electronics.md` (100 linija, ~3900 bajtova)
- [ ] Web search: "AC DC electrical engineering basics explained simply"
- [ ] Web search: "impedance concept ham radio explained"
- [ ] Web search: "LC circuit resonant frequency formula explained"

### Sadržaj koji treba dodati (NE BRISATI postojeće!)
- [ ] **Serijski i paralelni spoj otpornika** — formula + MathJax + primjer izračuna
- [ ] **Serijski i paralelni spoj kondenzatora** — formula + primjer
- [ ] **AC vs DC** — izmjenična i istosmjerna struja, frekvencija, period, amplituda, RMS
- [ ] **Reaktancija** — kapacitivna ($X_C$) i induktivna ($X_L$) s formulama
- [ ] **Impedancija** — $Z = R + jX$, zašto je ključna za RF, prikaz u ravnini
- [ ] **LC titrajni krug** — rezonantna frekvencija $f = \frac{1}{2\pi\sqrt{LC}}$, Q faktor
- [ ] **Transformatori** — princip rada, omjer namotaja, galvanska izolacija
- [ ] **Čitanje elektroničkih shema** — tablica simbola (otpornik, kondenzator, zavojnica, dioda, tranzistor, napajanje, masa)
- [ ] **Praktični primjeri** — izračun otpornika za LED (s MathJax), dijelilo napona
- [ ] **Boja kodovi otpornika** — tablica boja → vrijednosti
- [ ] **Falstad simulator** — link na gotove primjere (LC krug, dijelilo napona)
- [ ] **Admonitions** — minimalno 3 (example za izračune, tip za simulator, note za napomene)
- [ ] **Interni linkovi** — antennas.md, modulation.md, safety.md

### Kontrola kvalitete
- [ ] Minimalno 2500 riječi ukupno (postojeće + novo)
- [ ] Sve formule napisane u MathJax sintaksi
- [ ] Barem 3 admonition bloka
- [ ] `.en.md` ažuriran (ili stub)
- [ ] `mkdocs.yml` ne treba mijenjati

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Proširi stranicu docs/technical/electronics.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- docs/technical/electronics.md  (ZADRŽI SAV POSTOJEĆI SADRŽAJ!)
- .plan/01_VIZIJA_I_STANDARDI.md

KORAK 2 — Istraži web:
- "AC DC basics electronics explained"
- "impedance reactance explained simply RF"
- "LC resonant circuit frequency formula"
- "resistor color code table"

KORAK 3 — ISPOD postojećeg sadržaja dodaj nove sekcije (minimalno 1500 novih riječi):

## Serijski i paralelni spojevi
- Otpornici serijski: $R_{uk} = R_1 + R_2 + ... + R_n$
- Otpornici paralelno: $\frac{1}{R_{uk}} = \frac{1}{R_1} + \frac{1}{R_2} + ...$
- Kondenzatori (obrnuto): paralelno se zbrajaju kapaciteti
- Praktični MathJax primjeri s izračunima

## Izmjenična struja (AC)
- Razlika AC/DC, frekvencija, period (T = 1/f), amplituda, RMS vrijednost
- Zašto radioamateri moraju razumjeti AC

## Reaktancija i impedancija
- Kapacitivna reaktancija: $X_C = \frac{1}{2\pi f C}$
- Induktivna reaktancija: $X_L = 2\pi f L$
- Impedancija: $Z = \sqrt{R^2 + X^2}$
- Zašto je 50 Ω standard u radioamaterizmu

## LC titrajni krug
- Rezonantna frekvencija: $f_r = \frac{1}{2\pi\sqrt{LC}}$
- Q faktor, primjena u filtrima i oscilatorima
- Link na Falstad simulator s LC primjerom

## Transformatori
- Princip indukcije, omjer namotaja, galvanska izolacija
- Primjena u napajanjima i RF transformatorima (Balun)

## Čitanje elektroničkih shema
- Tablica simbola: simbol | naziv | funkcija

## Praktični primjeri s MathJax
- Izračun otpornika za LED (primjer: 5V, LED Vf=2V, If=20mA)
- Dijelilo napona (voltage divider)

## Boja kod otpornika
- Tablica: boja → znamenka → množitelj → tolerancija

KORAK 4 — Tehničke smjernice:
- MathJax za SVE formule (inline $...$ i blok $$...$$)
- Admonitions: minimalno 3 (example za izračune, tip za Falstad link)
- Interni linkovi: antennas.md, modulation.md, safety.md

KORAK 5 — Spremi u docs/technical/electronics.md
```

---

## Bilješke o napretku

- 
