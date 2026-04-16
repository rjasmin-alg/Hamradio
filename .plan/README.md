# 📁 .plan — Plan proširenja priručnika

Ovaj direktorij sadrži svu dokumentaciju potrebnu za sustavno proširenje Radioamaterskog priručnika korištenjem AI agenata.

## Tri dokumenta

| Dokument | Svrha |
|----------|-------|
| `01_VIZIJA_I_STANDARDI.md` | **"Ustav"** projekta — format, ton, kvaliteta. Čitati PRVO. |
| `02_MAPA_MODULA.md` | **Popis svih 113 modula** — status, prioritet, ovisnosti |
| `03_RAZRADA_MODULA.md` | **Detaljan zadatak za svaki modul** s prompt templateima |

## Kako početi novi sprint (s bilo kojeg računala)

1. Otvori `02_MAPA_MODULA.md` — nađi slobodan P1 modul (🔴 ili 🟢)
2. Otvori `03_RAZRADA_MODULA.md` — pronađi taj modul i kopiraj **prompt template**
3. Pokrni agenta s tim promptom (Antigravity ili drugi)
4. Agent čita, istražuje i zapisuje sadržaj u `docs/`
5. Kad je gotovo — označi status u `02_MAPA_MODULA.md` (promijeni 🔴 u ✅)

## Prioriteti

```
P1 Val 1 (proširi postojeće) → P1 Val 2 (kreiraj novo) → P2 → P3
```

## Statistika projekta

- **Ukupno modula**: 113
- **Već postoji** (treba proširiti): 37
- **Potpuno novo**: 76
- **Procijenjeno** ukupno: ~150.000 riječi
