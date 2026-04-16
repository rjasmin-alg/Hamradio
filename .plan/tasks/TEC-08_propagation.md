# TEC-08 — Propagacija radio valova

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/technical/propagation.md` |
| **Status** | 🔴 Ne postoji — kreirati od nule |
| **Prioritet** | P1 — Val 2 |
| **Složenost** | 🏗️ Velika |
| **Ovisnosti** | TEC-02 |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati `docs/technical/electronics.md` (ovisnost)
- [ ] Web search: "ionosphere layers D E F1 F2 explained ham radio"
- [ ] Web search: "MUF LUF maximum usable frequency explained"
- [ ] Web search: "HF propagation bands when use which day night"
- [ ] Web search: "solar cycle 25 SFI K-index A-index ham radio"
- [ ] Web search: "tropospheric ducting sporadic-E VHF propagation"
- [ ] Web search: "gray line propagation ham radio advantage"

### Sadržaj koji treba napisati
- [ ] **Uvodni paragraf** — zašto propagacija = srce radioamaterizma
- [ ] **3 mehanizma propagacije:**
  - [ ] Zemni val (ground wave) — frekvencije, domet, primjena
  - [ ] Ionosferski val (sky wave) — refleksija, skip zona
  - [ ] Linija vidljivosti (LOS) — VHF/UHF, efektivni domet
- [ ] **Ionosfera detaljno:**
  - [ ] D sloj — dnevni, apsorpcija, nestaje noću
  - [ ] E sloj — Sporadic-E, neočekivani DX
  - [ ] F1 sloj — dnevni, spaja se s F2 noću
  - [ ] F2 sloj — najvažniji za HF DX, visina, odraz
  - [ ] Vizualni dijagram slojeva s opisom
- [ ] **MUF i LUF** — definicija, kako ih odrediti, što kad je MUF niska
- [ ] **HF propagacija po opsezima** — tablica:
  - 160m, 80m, 40m, 30m, 20m, 17m, 15m, 12m, 10m, 6m
  - Stupci: Dnevna | Noćna | DX potencijal | Tipični domet
- [ ] **Sunčev ciklus:**
  - [ ] Što je Ciklus 25, gdje smo sada
  - [ ] SFI (Solar Flux Index) — što znači, raspon vrijednosti
  - [ ] K-indeks — geomagnetska aktivnost, skala 0-9
  - [ ] A-indeks — dnevni prosjek, što znači za DX
  - [ ] Praktični savjeti: SFI>120 + K<3 = odlični uvjeti
- [ ] **VHF/UHF propagacija:**
  - [ ] Troposferska difrakcija (Tropo) — dukt, E-skip, rain scatter
  - [ ] Sporadic-E (Es) — kad se pojavljuje, koji opsezi, koliko traje
  - [ ] Meteor scatter — kratki bursts, protokoli (MSK144)
  - [ ] Aurora — severni sjaj kao reflektor, zvuk "šamizena"
  - [ ] EME — Moon bounce (kratki spomen, link na moonbounce.md)
- [ ] **Gray Line:**
  - [ ] Što je, zašto je poseban
  - [ ] Kako iskoristiti (alati, vremenska zona)
- [ ] **Alati za praćenje i predikciju:**
  - [ ] VOACAP Online — HF predikcija, link
  - [ ] PSKReporter — tko čuje koga, vivo
  - [ ] DXMaps — real-time propagacija
  - [ ] SolarHam.com — sunčevi indeksi
  - [ ] HamClock — sve u jednom
- [ ] **Praktični savjeti** — "recepty" za različite situacije
- [ ] **Admonitions** — minimalno 4 (tip, info, note, example)
- [ ] **Interni linkovi** — antennas.md, bandplans.md, dxing.md, modes.md, ft8_guide.md

### Kontrola kvalitete
- [ ] Minimalno 3000 riječi
- [ ] Tablica HF propagacije po opsezima kompletna
- [ ] MathJax za formule (MUF, frekvencija)
- [ ] Linkovi na propagacijske alate funkcionalni
- [ ] **mkdocs.yml** — dodati pod Tehnika
- [ ] `.en.md` stub

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Kreiraj novu stranicu docs/technical/propagation.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- .plan/01_VIZIJA_I_STANDARDI.md
- docs/technical/electronics.md  (kontekst)

KORAK 2 — Istraži web:
- "ionosphere layers ham radio D E F1 F2 explained"
- "MUF maximum usable frequency LUF calculation"
- "solar cycle 25 current status SFI K-index ham radio"
- "sporadic-E propagation VHF explained"
- "gray line radio propagation explained"

KORAK 3 — Napiši stranicu s minimalno 3000 riječi:

# Propagacija radio valova

## Uvod
- Zašto propagacija određuje sve — što radio može i ne može

## Mehanizmi propagacije
### Zemni val (Ground Wave)
- Frekvencije, domet (do ~500km za MF/LF)
### Ionosferski val (Sky Wave)
- Refleksija, skip zona, višestruki skokovi
### Linija vidljivosti (Line-of-Sight)
- VHF/UHF, efektivni domet (> geometrijska LOS zbog refrakcije)

## Ionosfera
### Struktura i slojevi
- D sloj: dnevni, 60-90km, apsorpcija (posebno 80m i 160m)
- E sloj: 90-140km, sporadic-E pojava, srednji domet
- F1 sloj: 140-250km, dnevni, manje važan za DX
- F2 sloj: 250-400km, najvažniji za HF DX, noću spada
### Kritična frekvencija i skip zona
- Što je kritična frekvencija foF2
- Skip zona — mrtva zona između zemnog i ionosferskog vala

## MUF i LUF
- MUF: $f_{MUF} = f_{kritična} / \cos(\theta)$
- LUF: uvjetovan apsorpcijom (D sloj)
- Što napraviti kad je MUF ispod željene frekvencije

## HF propagacija po opsezima
Tablica: Opseg | Frekvencija | Dnevno | Noću | DX potencijal | Tipični domet EU

## Sunčev ciklus
- Ciklus 25 — gdje smo i kamo idemo
- SFI: <80 loše, 80-100 prosječno, >120 odlično za DX
- K-indeks: 0-3 dobro, 4+ problemi, 5+ geomagnetic storm
- A-indeks: dnevni prosjek K-indeksa
- Praktični "recept": SFI > 120, K < 3, A < 15 = open for DX!

## VHF/UHF propagacija
### Troposferska propagacija (Tropo)
- Duktno širenje, meteorološki uvjeti, Europa za 2m
### Sporadic-E (Es)
- Godišnja doba, opsezi (posebno 6m i 2m), YouTube primjeri
### Meteor scatter
- MSK144 protokol, Perseus pojava, sporadični
### Aurora
- Geomagnetic storm, aurora scatter, zvuk "raspalo staklo"
### EME (Earth-Moon-Earth)
- Kratki opis, link na moonbounce.md

## Gray Line
- Što je (prijelazna zona dan/noć na terminatoru)
- Zašto je posebna (F2 i zenith angle)
- Kako koristiti: alati za gray line, timing

## Alati
- VOACAP Online (voacap.com) — HF point-to-point predikcija
- PSKReporter (pskreporter.info) — real-time FT8/FT4 propagacija
- DXMaps (dxmaps.com) — cluster mapa veza
- SolarHam (solarham.com) — sunčevi indeksi
- HamClock — desktop/Pi all-in-one

## Praktični savjeti
- Jugo je otvoreno 20m, ne 40m? Provjeri SFI.
- "Grey line DXpedition" — kako iskoristiti
- Jesen/proljeće — F2 sezona za DXCC

KORAK 4 — Tehničke smjernice:
- MathJax za formule
- Tablica HF propagacije OBAVEZNA
- Admonitions: minimalno 4
- Interni linkovi: antennas.md, bandplans.md, dxing.md, modes.md

KORAK 5 — Spremi u docs/technical/propagation.md (nova datoteka)
KORAK 6 — Dodaj u mkdocs.yml nav → Tehnika:
  - Propagacija: technical/propagation.md
KORAK 7 — Kreiraj stub docs/technical/propagation.en.md
```

---

## Bilješke o napretku

- 
