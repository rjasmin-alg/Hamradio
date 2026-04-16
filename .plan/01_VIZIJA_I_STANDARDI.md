# 📘 Radioamaterski Priručnik — Vizija i Standardi

> **VAŽNO:** Ovo je **centralni dokument** koji svaki agent mora pročitati prije nego što počne raditi na bilo kojem modulu.
> Sav generirani sadržaj mora biti usklađen s ovim standardima.

---

## 1. Vizija projekta

### Što želimo postići?
Stvoriti **najopsežniji radioamaterski priručnik na hrvatskom jeziku** — koherentnu, modularnu, pretraživu online referencu koja pokriva:

- Sve što početnik treba znati da položi ispit i napravi prvu vezu
- Dovoljno dubine za iskusnog operatora da koristi kao referentni materijal
- Hrvatski kontekst (propisi, frekvencije, klubovi, savezi) uz međunarodni okvir
- Praktične upute (step-by-step), ne samo teoriju

### Ciljana publika (po prioritetu)
1. **Početnici** koji žele položiti amaterski ispit u HR
2. **Novi operatori** koji su upravo dobili pozivnu oznaku
3. **Iskusni amateri** koji trebaju referentni materijal
4. **CB korisnici** koji razmišljaju o prelasku na amaterski radio

### Ton pisanja
- **Prijateljski i pristupačan**, kao da iskusni OM objašnjava kolegi
- **Praktičan** — svaki koncept potkrijepiti primjerom iz prakse
- **Izbjegavati akademski ton** — ovo nije udžbenik ETF-a
- **Koristiti analogije** (voda u cijevi za struju, leća za Yagi, itd.)

---

## 2. Struktura pojedinačne stranice

Svaka stranica mora pratiti ovu strukturu (prilagoditi po potrebi):

```
# Naslov stranice

Uvodni paragraf (2-3 rečenice) — što je tema i zašto je važna za radioamatera.

## Glavne sekcije (H2)

### Podsekcije (H3)

Sadržaj s:
- Objašnjenjima
- Primjerima iz prakse
- Formulama (ako su relevantne)
- Slikama/dijagramima

## Praktični primjeri / Step-by-step
(Ako je primjenjivo)

## Česta pitanja / Tipične greške
(Ako je primjenjivo)

## Resursi za daljnje učenje
- Linkovi na kvalitetne vanjske resurse
- YouTube kanali
- Softverski alati
```

### Minimalna dubina sadržaja
- Svaka **glavna stranica** (ne index) mora imati minimalno **1500 riječi** kvalitetnog sadržaja
- Svaka stranica mora imati barem **2 admonition bloka** (tip, warning, note, itd.)
- Ako tema uključuje matematiku — koristiti MathJax formule
- Ako tema uključuje sheme — opisati ih tekstualno + link na simulator/alat

---

## 3. MkDocs Material — Tehničke smjernice

### Admonitions (obavezno koristiti!)
```markdown
!!! tip "Savjet iz prakse"
    Tekst savjeta...

!!! warning "Upozorenje"
    Tekst upozorenja...

!!! note "Napomena"
    Tekst napomene...

!!! example "Primjer"
    Tekst primjera...

!!! info "Jeste li znali?"
    Zanimljiva činjenica...

!!! danger "OPASNOST"
    Za sigurnosna upozorenja...
```

### Tabbed sadržaj (za usporedbe)
```markdown
=== "IARU Regija 1 (Europa)"
    Sadržaj za EU...

=== "IARU Regija 2 (Amerika)"
    Sadržaj za USA...
```

### MathJax formule
```markdown
Inline: $f = \frac{c}{\lambda}$

Blok:
$$ P_{dBm} = 10 \cdot \log_{10}\left(\frac{P_{mW}}{1}\right) $$
```

### Tablice
Koristiti za strukturirane podatke (frekvencije, usporedbe opreme, Q-kodovi, itd.)

### Slike
- Preferirati **Wikimedia Commons** (slobodna licenca)
- Ako nije dostupno, koristiti `![Opis](URL)` s jasnim alt-textom
- Dijagrami: opisati u tekstu, linkati na alat za vizualizaciju (Falstad, etc.)

---

## 4. Jezične smjernice (Hrvatski)

### Pravopis
- Koristiti **standardni hrvatski** (ijekavica)
- Tehničke termine pisati na **hrvatskom s engleskim u zagradi** pri prvom pojavljivanju:
  > "Omjer stojnih valova (SWR — Standing Wave Ratio) je mjera..."
- Kratice: pri prvom korištenju na stranici — puni naziv, zatim kratica

### Specifičnosti radioamaterskog žargona
- Koristiti uobičajeni ham žargon gdje je prikladno (OM, YL, 73, itd.)
- Ali uvijek objasniti žargon pri prvom korištenju

### Dvojezičnost
- Svaka `.md` datoteka mora imati i `.en.md` verziju
- Engleski prijevod može biti kraći / sažetiji
- Engleski prijevod se može raditi u zasebnom prolazu (niži prioritet)

---

## 5. Crosslinking strategija

### Pravila za interne linkove
- Svaka stranica mora linkati **barem 3 druge stranice** iz priručnika
- Koristiti kontekstualne linkove unutar teksta:
  > "Za više o tome kako radi [SSB modulacija](../operating/modes.md#ssb-single-sideband), pogledajte sekciju o modovima."
- Na kraju svake stranice dodati sekciju "Povezane teme":
  ```markdown
  ## Povezane teme
  - [Antene i vodovi](../technical/antennas.md)
  - [Frekvencijski planovi](../operating/bandplans.md)
  ```

### Linkovi na rječnik
- Tehnički pojmovi koji se pojavljuju prvi put trebaju linkati na rječnik:
  > "[SWR](../resources/glossary.md#s) je omjer stojnih valova..."

---

## 6. Kriteriji kvalitete (Checklist za review)

Prije nego se modul smatra "gotovim", mora zadovoljiti:

- [ ] **Sadržaj**: Minimalno 1500 riječi (glavne stranice)
- [ ] **Struktura**: Prati predložak iz sekcije 2
- [ ] **Admonitions**: Barem 2 po stranici
- [ ] **Crosslinks**: Barem 3 interna linka
- [ ] **Resursi**: Barem 2 vanjska linka na kvalitetne izvore
- [ ] **Formule**: Ako tema uključuje matematiku — MathJax
- [ ] **Tablice**: Ako postoje strukturirani podaci — tablični prikaz
- [ ] **Primjeri**: Barem 1 praktični primjer / scenario
- [ ] **Hrvatski**: Ispravna terminologija, engleski u zagradama
- [ ] **EN verzija**: `.en.md` datoteka postoji (može biti stub)

---

## 7. Konvencije za datoteke

### Imenovanje
- Sve malim slovima, riječi odvojene podvlakom: `antenna_tuners.md`
- Index datoteke za sekcije: `index.md`
- Engleska verzija: `filename.en.md`

### Direktorijska struktura
```
docs/
├── index.md
├── regulations/          # Propisi
├── technical/            # Tehnika
│   ├── fundamentals/     # Osnove (NOVO - poddirektoriji za dublje teme)
│   ├── rf/               # RF specifično
│   └── digital/          # Digitalna tehnika
├── operating/            # Rad na opsegu
├── activities/           # Aktivnosti
├── cb/                   # CB Radio
├── emcomm/               # Krizne situacije
├── community/            # Zajednica
├── projects/             # DIY projekti (NOVO)
├── history/              # Povijest (NOVO)
└── resources/            # Resursi
```

> **NAPOMENA:** Nove poddirektorije i sekcije dodavati **inkrementalno**. 
> Ne treba odmah sve reorganizirati — nove stranice se mogu dodavati u postojeće direktorije, 
> a reorganizacija u poddirektorije se radi tek kad sekcija naraste na 10+ stranica.
