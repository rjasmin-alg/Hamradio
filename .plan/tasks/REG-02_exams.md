# REG-02 — Kako postati radioamater

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/regulations/exams.md` |
| **Status** | 🟢 Postoji, treba proširiti |
| **Prioritet** | P1 — Val 1 |
| **Složenost** | 🔧 Srednja |
| **Ovisnosti** | — |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati postojeći `docs/regulations/exams.md`
- [ ] Web search: "kako postati radioamater Hrvatska 2024"
- [ ] Web search: "HAKOM radioamaterski ispit postupak prijave"
- [ ] Web search: "HRS ispit razredi A B N radioamater"
- [ ] Web search: "CEPT ham radio exam countries comparison"

### Sadržaj koji treba napisati
- [ ] **Uvodni paragraf** — što je dozvola i zašto je potrebna
- [ ] **Razredi dozvola** — N, B, A — kratki opis svakog (tablica)
- [ ] **Tko može pristupiti ispitu** — uvjeti, dob, predznanje
- [ ] **Gdje se prijavljuje** — HAKOM web, HRS, postupak prijave s linkom
- [ ] **Cijena i termini** — koliko košta, koliko često su termini
- [ ] **Kako izgleda ispit** — broj pitanja, trajanje, prolaznost, usmeni/pismeni
- [ ] **Ispitne teme** — popis kategorija (Propisi, Tehnika, Operativa)
- [ ] **Plan učenja** — savjeti, preporučeni materijali, vremenski okvir
- [ ] **Tabbed usporedba** — HR vs USA vs UK vs DE (razredi i uvjeti)
- [ ] **FAQ sekcija** — 5-7 najčešćih pitanja s odgovorima
- [ ] **Admonitions** — minimalno 3 (tip za savjet, note za napomenu, warning)
- [ ] **Interni linkovi** — barem 3 (license_classes.md, croatian_regs.md, exam_prep.md)
- [ ] **Vanjski linkovi** — HAKOM, HRS, barem 1 resurs za vježbu

### Kontrola kvalitete
- [ ] Minimalno 1500 riječi
- [ ] Tehnički termini na HR s engleskim u zagradi
- [ ] Barem 2 admonition bloka
- [ ] Barem 3 interna linka
- [ ] `.en.md` verzija (može biti stub)
- [ ] `mkdocs.yml` ne treba mijenjati (stranica već postoji)

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Proširi stranicu docs/regulations/exams.md u MkDocs priručniku za radioamatere.

KORAK 1 — Pročitaj ove datoteke iz projekta:
- docs/regulations/exams.md  (postojeći sadržaj koji treba proširiti)
- .plan/01_VIZIJA_I_STANDARDI.md  (ton, format i standardi pisanja)

KORAK 2 — Istraži web za:
- "kako postati radioamater Hrvatska"
- "HAKOM radioamaterski ispit prijava"
- "HRS ispit razredi A B N"
- "ham radio license classes Europe comparison"

KORAK 3 — Proširi stranicu na minimalno 1500 riječi. ZADRŽI sav postojeći sadržaj,
dodaj/proširi s ovim sekcijama:
1. Uvodni paragraf — što je dozvola, zašto je važna
2. Tablica razreda dozvola (N, B, A) s privilegijama
3. Uvjeti za pristup ispitu (dob, predznanje)
4. Gdje se prijavljuje — HAKOM/HRS, postupak korak po korak
5. Cijena i termini
6. Kako izgleda ispit (broj pitanja, trajanje, prolaznost)
7. Ispitne teme po kategorijama
8. Plan učenja — savjeti, materijali, vremenski okvir
9. Usporedba razreda HR / USA / UK / DE — koristi MkDocs tabbed format
10. FAQ sekcija (5-7 pitanja)

KORAK 4 — Poštuj ove tehničke zahtjeve:
- Koristi MkDocs Material admonitions: minimalno 3 (tip, note, warning)
- Dodaj interne linkove na: regulations/license_classes.md, regulations/croatian_regs.md, resources/exam_prep.md
- Tehnički termini: hrvatska riječ + (engleski u zagradi) pri prvom pojavljivanju
- Jezik: standardni hrvatski (ijekavica)

KORAK 5 — Spremi rezultat u docs/regulations/exams.md (prepiši datoteku)
KORAK 6 — Kreiraj stub docs/regulations/exams.en.md ako ne postoji
```

---

## Bilješke o napretku

*(Ovdje zapisuj napredak, probleme, odluke)*

- 
