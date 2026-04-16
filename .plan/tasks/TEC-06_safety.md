# TEC-06 — Sigurnost

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/technical/safety.md` |
| **Status** | 🟢 Postoji, treba proširiti |
| **Prioritet** | P1 — Val 1 |
| **Složenost** | 🔧 Srednja |
| **Ovisnosti** | — |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati postojeći `docs/technical/safety.md` (~980 bajtova)
- [ ] Web search: "ICNIRP electromagnetic field exposure limits 2020"
- [ ] Web search: "ham radio RF safety exposure limits power distance"
- [ ] Web search: "electrical safety high voltage capacitor danger"
- [ ] Web search: "lightning protection ham radio antenna system"
- [ ] Web search: "antenna work height safety outdoor"

### Sadržaj koji treba dodati
- [ ] **RF sigurnost — detaljno:**
  - [ ] ICNIRP smjernice za neionizirajuće zračenje
  - [ ] Tablica sigurnih udaljenosti: Snaga (W) | Frekvencija | Min. udaljenost od antene
  - [ ] MPE (Maximum Permissible Exposure) — što je, kako izračunati
  - [ ] Praktični primjeri: 100W / dipol / 14 MHz — sigurna udaljenost?
  - [ ] Zašto UHF/mikrovalovi su opasniji na kratkim udaljenostima
- [ ] **Električna sigurnost — detaljno:**
  - [ ] Visoki naponi u PA stupnjevima — stvarne opasnosti
  - [ ] Kondenzatori u PSU koji ostaju napunjeni i nakon isključivanja
  - [ ] Pravilo "jedne ruke" pri radu s naponom
  - [ ] Pravilno uzemljenje svih metalnih kućišta
  - [ ] Osigurači — dimenzioniranje, zašto NE premostiti
- [ ] **Zaštita od groma — detaljno:**
  - [ ] Sustav arrestora (odvodnika prenapona) — gdje i kako montirati
  - [ ] Fizičko odvajanje antene — zašto je jedina 100% zaštita
  - [ ] Ground rod i veza na uzemljenje (link na grounding.md)
  - [ ] Što napraviti kad vidite grmljavinu (odmah!)
- [ ] **Sigurnost pri radu na anteni:**
  - [ ] Rad na visini — pravila, sidra, sigurnosne naramenice
  - [ ] Blizina dalekovoda — pravne i fizičke sigurnosne udaljenosti
  - [ ] RF opeklina — ne dirajte antenu dok odašiljete
- [ ] **Prva pomoć kod strujnog udara:**
  - [ ] Što napraviti (redoslijed koraka)
  - [ ] Što NE raditi (sam postati žrtva)
  - [ ] Kad zvati hitnu (112)
- [ ] **Admonitions** — OBILATO koristiti DANGER i WARNING (ovo je sigurnosna stranica)

### Kontrola kvalitete
- [ ] Minimalno 2000 riječi ukupno
- [ ] Tablica MPE/sigurnih udaljenosti prisutna
- [ ] DANGER admonition za svaki stvarni smrtni rizik
- [ ] Vanjski linkovi: ICNIRP, ARRL safety page
- [ ] Interni link na grounding.md
- [ ] `.en.md` stub
- [ ] `mkdocs.yml` ne treba mijenjati

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Proširi stranicu docs/technical/safety.md — KRITIČNA STRANICA!

KORAK 1 — Pročitaj:
- docs/technical/safety.md  (ZADRŽI SAV POSTOJEĆI SADRŽAJ!)
- .plan/01_VIZIJA_I_STANDARDI.md

KORAK 2 — Istraži web:
- "ICNIRP 2020 exposure limits non-ionizing radiation table"
- "ham radio RF exposure maximum permissible exposure calculator"
- "amateur radio power supply capacitor danger discharge"
- "lightning protection amateur radio antenna grounding"

KORAK 3 — ZADRŽI sve postojeće, dodaj minimalno 1500 novih riječi:

## RF sigurnost (PEM)
- ICNIRP smjernice — što su i zašto su bitne
- Tablica: Frekvencija | Snaga | Min. udaljenost od antene (sigurna zona)
- MPE definicija, kako izračunati za svoju stanicu
- Primjer: 100W SSB, dipol 14 MHz — koliko dalje stajati?
- Zašto UHF/SHF je opasniji na kratkim udaljenostima (zagrijavanje tkiva)
- !!! danger "RF opeklina" — ne dirajte antenu dok odašiljate!

## Električna sigurnost (detaljno)
- Visoki naponi u PA: anodne napone lampi (>1000V)
- !!! danger "Kondenzatori ostaju napunjeni" — i do 30 minuta nakon isključivanja napajanja!
- Pravilo "jedne ruke" pri radu u blizini napona
- Pravilno uzemljenje metalnih kućišta
- Osigurači: kako dimenzionirati, zašto nikad ne premostiti!

## Zaštita od groma (detaljno)
- !!! danger tipično "gromobransko uzemljenje" nije dovoljno za antene!
- Arrestori (odvodnici prenapona) — gdje, koji, kako montirati
- Fizičko odvajanje antene kada se ne koristi — jedina 100% zaštita
- Što napraviti čim se pojavi grmljavina (odmah odvojiš koaksijalku!)

## Sigurnost pri radu na anteni
- Rad na visini: zahtjevi, pribor, sigurnosna naramenica
- Udaljenost od dalekovoda — zakonska udaljenost u HR
- RF opeklina — što je, kako liječiti

## Prva pomoć kod strujnog udara
Redoslijed koraka:
1. NE dotičite žrtvu golim rukama!
2. Isključi napajanje (prekidač, osigurač)
3. Tek onda pomozi žrtvi
4. Zovi 112
5. CPR ako nema disanja

KORAK 4 — Tehničke smjernice:
- Koristiti `!!! danger` za svaki smrtni rizik
- Koristiti `!!! warning` za ozbiljne, ali ne smrtonosne rizike
- Tablica MPE sigurnih udaljenosti je OBAVEZNA
- Linkovi: ICNIRP.org, grounding.md (interni)

KORAK 5 — Spremi u docs/technical/safety.md
```

---

## Bilješke o napretku

- 
