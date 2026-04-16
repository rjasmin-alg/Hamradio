# REG-10 — Radioamaterska etika

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/regulations/ethics.md` |
| **Status** | 🔴 Ne postoji — kreirati od nule |
| **Prioritet** | P1 — Val 2 |
| **Složenost** | 🔧 Srednja |
| **Ovisnosti** | — |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Web search: "The Amateur's Code Paul Segal W9EEA 1928"
- [ ] Web search: "ham radio operating ethics on-air behaviour"
- [ ] Web search: "radioamaterska etika ponašanje na opsegu"
- [ ] Web search: "intentional interference ham radio QRM reporting"

### Sadržaj koji treba napisati
- [ ] **Uvodni paragraf** — zašto etika u radioamaterizmu
- [ ] **The Amateur's Code** — original + prijevod na HR (7 načela)
- [ ] **Zlatna pravila** — 10+ konkretnih pravila ponašanja na opsegu
- [ ] **Što je zabranjeno** — komercijalno, glazba, vulgarni jezik, lažna identifikacija
- [ ] **Zakonske posljedice** — novčane kazne, oduzimanje dozvole
- [ ] **QRM i intencionalno ometanje** — kako reagirati (ne eskalirati!), gdje prijaviti
- [ ] **Prioritet hitnih veza** — MAYDAY, SOS, DISTRESS — sve mora biti tiho
- [ ] **Elmering** — tradicija mentorstva, kako biti dobar Elmer
- [ ] **DX etiketa** — posebna pravila za pile-up i DX expedition
- [ ] **Contest etiketa** — posebna pravila za natjecanja
- [ ] **Admonitions** — minimalno 4 (warning za zabranjeno, tip za savjete, danger za MAYDAY)
- [ ] **Interni linkovi** — procedures.md, contesting.md, dxing.md

### Kontrola kvalitete
- [ ] Minimalno 1500 riječi
- [ ] The Amateur's Code prijevod točan i atribuiran
- [ ] Zakonske kazne provjerene (HR propisi)
- [ ] **mkdocs.yml** — dodati u nav
- [ ] `.en.md` stub

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Kreiraj novu stranicu docs/regulations/ethics.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- .plan/01_VIZIJA_I_STANDARDI.md

KORAK 2 — Istraži web:
- "The Amateur's Code Paul M. Segal W9EEA 1928 text"
- "ham radio operating ethics band etiquette"
- "radioamaterska etika hrvatska"
- "intentional interference ham radio QRM report IARU"

KORAK 3 — Napiši stranicu s minimalno 1500 riječi:
1. Uvod — zašto etika čini radioamaterizam posebnim
2. The Amateur's Code (Paul M. Segal, W9EEA, 1928.):
   - Original tekst (citirat kao quote blok)
   - Prijevod na hrvatski — svih 7 načela
3. Zlatna pravila ponašanja na opsegu — minimalno 10 konkretnih pravila:
   - Identificiranje, dužina poruka, slušanje prije odašiljanja, itd.
4. Što je zabranjeno (prema HR propisima):
   - Komercijalna upotreba, emitiranje glazbe, vulgarni jezik, lažna identifikacija
   - Zakonske posljedice (novčane kazne, oduzimanje dozvole)
5. QRM i intencionalno ometanje:
   - Kako reagirati (ne eskalirati, ne odgovarati na provokacije)
   - Gdje prijaviti (HAKOM, HRS, IARU)
6. Prioritet hitnih veza:
   - MAYDAY/DISTRESS — sve stanice moraju prestati odašiljati
   - Kako reagirati kad čujete hitni poziv
7. Elmering — tradicija mentorstva:
   - Što je Elmer, zašto je tradicija važna
   - Kako postati dobar Elmer (savjeti)
8. DX etiketa — posebna pravila za pile-up
9. Contest etiketa — kratko

KORAK 4 — Tehničke smjernice:
- Koristiti `!!! danger` za hitne pozive i zabranjene radnje
- Koristiti `!!! warning` za pravna upozorenja
- Koristiti `!!! tip` za praktične savjete
- Interni linkovi: procedures.md, contesting.md, dxing.md

KORAK 5 — Spremi u docs/regulations/ethics.md (nova datoteka)
KORAK 6 — Dodaj u mkdocs.yml nav → Propisi i Dozvole:
  - Etika i ponašanje: regulations/ethics.md
KORAK 7 — Kreiraj stub docs/regulations/ethics.en.md
```

---

## Bilješke o napretku

- 
