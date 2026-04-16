# REG-03 — Hrvatski propisi

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/regulations/croatian_regs.md` |
| **Status** | 🟢 Postoji, treba proširiti |
| **Prioritet** | P1 — Val 1 |
| **Složenost** | 🏗️ Velika |
| **Ovisnosti** | — |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati postojeći `docs/regulations/croatian_regs.md`
- [ ] Web search: "Pravilnik o amaterskim radijskim komunikacijama Narodne novine"
- [ ] Web search: "HAKOM radioamaterske dozvole frekvencije snaga"
- [ ] Web search: "hrvatski radioamaterski propisi 2022 2023 2024"
- [ ] Web search: "HRS radioamaterske pozivne oznake 9A Hrvatska"

### Sadržaj koji treba napisati
- [ ] **Uvodni paragraf** — regulatorni okvir
- [ ] **Zakon o elektroničkim komunikacijama** — sažetak relevantnih dijelova
- [ ] **Pravilnik o amaterskim radijskim komunikacijama** — sažetak + link
- [ ] **Tablica razreda i frekvencija** — Razred | Band | Frekvencije | Max snaga
- [ ] **Tablica modova po razredima** — što smije koji razred
- [ ] **Pravila za pozivne oznake** — formiranje, posebne oznake (9A/P, 9A/MM...)
- [ ] **Obveze operatora** — dnevnik, identifikacija, prijava postaje
- [ ] **HAKOM sekcija** — uloga, nadležnosti, web linkovi
- [ ] **HRS sekcija** — uloga, nadležnosti, web linkovi
- [ ] **Kronologija izmjena propisa** — tablica važnih datuma i promjena
- [ ] **Admonitions** — minimalno 3
- [ ] **Interni linkovi** — license_classes.md, callsigns.md, exams.md

### Kontrola kvalitete
- [ ] Minimalno 1500 riječi
- [ ] Tablica frekvencija i snaga potpuna i točna
- [ ] Vanjski linkovi: Narodne novine, HAKOM.hr, hamradio.hr
- [ ] `.en.md` stub
- [ ] `mkdocs.yml` ne treba mijenjati

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Proširi stranicu docs/regulations/croatian_regs.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- docs/regulations/croatian_regs.md  (postojeći sadržaj)
- .plan/01_VIZIJA_I_STANDARDI.md

KORAK 2 — Istraži web:
- "Pravilnik o amaterskim radijskim komunikacijama Hrvatska Narodne novine"
- "HAKOM radioamaterske dozvole frekvencije snaga razredi"
- "9A pozivne oznake formiranje Hrvatska"
- "HRS QSL biro radioamaterski savez"

KORAK 3 — Proširi na minimalno 1500 riječi. Zadrži postojeći sadržaj, dodaj:
1. Sažetak Zakona o elektroničkim komunikacijama (relevantni dijelovi za RF)
2. Detaljan sažetak Pravilnika o amaterskim radijskim komunikacijama:
   - Tablica: Razred | Frekvencijski opsezi | Maks. snaga (W) | Modovi
   - Pravila za pozivne oznake (9AxXXX, posebni prefiksi: /P, /M, /MM)
   - Obveze operatora: vođenje dnevnika, identifikacija na opsegu, prijava postaje
3. HAKOM — nadležnosti, kako kontaktirati, linkovi
4. HRS — uloga, QSL biro, ispiti, linkovi
5. Nationalna tablica namjene RF spektra — kratki uvod s linkom
6. Kronologija: tablica važnih izmjena propisa (godina | što se promijenilo)

KORAK 4 — Tehničke smjernice:
- MkDocs admonitions: minimalno 3
- Tablice za sve strukturirane podatke
- Interni linkovi: license_classes.md, callsigns.md, exams.md
- Vanjski linkovi: nn.hr, hakom.hr, hamradio.hr

KORAK 5 — Spremi u docs/regulations/croatian_regs.md
KORAK 6 — Kreiraj stub docs/regulations/croatian_regs.en.md ako ne postoji
```

---

## Bilješke o napretku

- 
