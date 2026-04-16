# REG-06 — Razredi dozvola

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/regulations/license_classes.md` |
| **Status** | 🔴 Ne postoji — kreirati od nule |
| **Prioritet** | P1 — Val 2 |
| **Složenost** | 🔧 Srednja |
| **Ovisnosti** | REG-03, REG-04 |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati `docs/regulations/croatian_regs.md` (ovisnost)
- [ ] Pročitati `docs/regulations/international_regs.md` (ovisnost)
- [ ] Web search: "CEPT T/R 61-01 ham radio license"
- [ ] Web search: "ham radio license classes Europe comparison 2024"
- [ ] Web search: "FCC ham radio Technician General Amateur Extra"
- [ ] Web search: "UK Foundation Intermediate Full amateur radio"

### Sadržaj koji treba napisati
- [ ] **Uvodni paragraf** — zašto postoje razredi, princip napredovanja
- [ ] **Hrvatski razredi — N (Novajlija)** — uvjeti, frekvencije, snaga, modovi
- [ ] **Hrvatski razredi — B** — uvjeti, frekvencije, snaga, modovi
- [ ] **Hrvatski razredi — A (CEPT)** — uvjeti, frekvencije, snaga, modovi, međunarodni status
- [ ] **Tablica privilegija** — Razred | HF | VHF/UHF | Max snaga | CEPT
- [ ] **CEPT sustav** — T/R 61-01, što znači za putovanje, koja zemlja prihvaća
- [ ] **CEPT Novice Licence** — što je, koje privilegije daje
- [ ] **Tabbed usporedba** — HR / USA (Tech/Gen/Extra) / UK (Found/Inter/Full) / DE (Klasse E/A)
- [ ] **Napredovanje** — kako prijeći iz N → B → A (uvjeti, postupak)
- [ ] **Admonitions** — minimalno 3
- [ ] **Interni linkovi** — exams.md, croatian_regs.md, callsigns.md

### Kontrola kvalitete
- [ ] Minimalno 1500 riječi
- [ ] Tablica privilegija kompletna
- [ ] Tabbed sadržaj za usporedbu zemalja
- [ ] **mkdocs.yml** — dodati u `nav` pod `Propisi i Dozvole`
- [ ] `.en.md` stub

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Kreiraj novu stranicu docs/regulations/license_classes.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- .plan/01_VIZIJA_I_STANDARDI.md
- docs/regulations/croatian_regs.md  (za kontekst o HR propisima)
- docs/regulations/international_regs.md  (za kontekst o međunarodnim propisima)

KORAK 2 — Istraži web:
- "CEPT T/R 61-01 amateur radio"
- "ham radio license classes comparison Europe USA UK"
- "FCC Technician General Amateur Extra privileges"
- "UK Foundation Intermediate Full licence amateur radio"

KORAK 3 — Napiši stranicu s minimalno 1500 riječi pokrivajući:
1. Uvod — zašto razredi, princip napredovanja u radioamaterizmu
2. Hrvatski razredi:
   - N (Novajlija): uvjeti za polaganje, frekvencije, snaga, modovi
   - B: uvjeti, frekvencije, snaga, modovi
   - A (CEPT razred): uvjeti, pune privilegije, međunarodno priznanje
3. Tablica privilegija: Razred | HF opsezi | VHF/UHF | Max snaga | CEPT status
4. CEPT sustav — T/R 61-01: što znači, koje zemlje prihvaćaju, kako koristiti
5. CEPT Novice Licence — opis i razlika od pune CEPT dozvole
6. Usporedba s inozemstvom (MkDocs tabbed format):
   - USA: Technician / General / Amateur Extra
   - UK: Foundation / Intermediate / Full
   - Njemačka: Klasse E / Klasse A
7. Kako napredovati: uvjeti i postupak za N→B i B→A

KORAK 4 — Tehničke smjernice:
- Tablice za sve strukturirane podatke
- MkDocs tabbed format za usporedbu zemalja
- Admonitions: minimalno 3 (tip, note, info)
- Interni linkovi: exams.md, croatian_regs.md, callsigns.md

KORAK 5 — Spremi u docs/regulations/license_classes.md (nova datoteka)
KORAK 6 — Dodaj stranicu u mkdocs.yml pod nav → Propisi i Dozvole:
  - Razredi dozvola: regulations/license_classes.md
KORAK 7 — Kreiraj stub docs/regulations/license_classes.en.md
```

---

## Bilješke o napretku

- 
