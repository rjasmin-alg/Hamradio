# OPR-02 — Frekvencijski planovi

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/operating/bandplans.md` |
| **Status** | 🟢 Postoji, treba proširiti |
| **Prioritet** | P1 — Val 1 |
| **Složenost** | 🔧 Srednja |
| **Ovisnosti** | — |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati postojeći `docs/operating/bandplans.md` (~2262 bajtova — pokriva 160m, 80m, 40m, 20m, 2m, 70cm)
- [ ] Web search: "IARU Region 1 band plan 2021 HF VHF UHF"
- [ ] Web search: "60m amateur band waiver special IARU"
- [ ] Web search: "6m fifty MHz magic band propagation"
- [ ] Web search: "amateur radio 23cm 1296 MHz band plan"
- [ ] Preuzeti/pregledati: [IARU R1 bandplan PDF](https://www.iaru-r1.org/on-the-air/band-plans/)

### Opsezi koji nedostaju — treba dodati svaki s tablicom
- [ ] **60m (5 MHz)** — status u HR, kanalni plan (5 kanala), IARU preporuke
- [ ] **30m (10 MHz)** — WARC, samo CW i WSPR/FT8, bez SSB phone
- [ ] **17m (18 MHz)** — WARC, odličan DX opseg, FT8 frekvencija
- [ ] **15m (21 MHz)** — dnevni DX, sličan 20m ali ovisi o ciklusu
- [ ] **12m (24 MHz)** — WARC, samo kad je SFI visok
- [ ] **10m (28 MHz)** — ogromno, FM simplex, AM, SSB, CW, digitalni
- [ ] **6m (50 MHz)** — "Magic Band", sporadic-E, beacon frekvencija, FM simplex
- [ ] **4m (70 MHz)** — nije svugdje dostupan, kratko napomenuti
- [ ] **23cm (1296 MHz)** — SSB/CW DX, ATV, digitalni
- [ ] **Mikrovalni opsezi** — pregled (3cm, 2cm, 1.25cm) — kratko

### Poboljšanja u postojećim opsezima
- [ ] Za svaki opseg dodati: **karakteristike propagacije** (1-2 rečenice)
- [ ] Za svaki opseg dodati: **beacon frekvencija** ako postoji
- [ ] Za svaki opseg dodati: **FM pozivni kanal** ako postoji (VHF/UHF)
- [ ] Dodati napomenu o **WARC opsezima** (30m, 17m, 12m) — bez natjecanja!
- [ ] Dodati link na **IARU R1 PDF** za kompletan plan
- [ ] **Admonitions** — minimalno 2 (note za WARC pravilo, tip za monitoring frekvencije)
- [ ] **Interni linkovi** — propagation.md, modes.md, license_classes.md

### Kontrola kvalitete
- [ ] Svi opsezi od 160m do 23cm prisutni
- [ ] Svaki opseg ima tablicu s EU i USA razlikama
- [ ] WARC opsezi jasno označeni kao "bez natjecanja"
- [ ] `.en.md` ažuriran ili stub
- [ ] `mkdocs.yml` ne treba mijenjati

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Proširi stranicu docs/operating/bandplans.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- docs/operating/bandplans.md  (ZADRŽI SVE POSTOJEĆE — Proširi i dodaj!)
- .plan/01_VIZIJA_I_STANDARDI.md

KORAK 2 — Istraži web:
- "IARU Region 1 HF band plan 2021"
- "amateur radio 60m 5MHz band plan channels"
- "6m 50MHz magic band propagation sporadic-E"
- "WARC bands 30m 17m 12m no contests rule"
- "amateur radio 23cm 1296MHz band plan"

KORAK 3 — ZADRŽI sve postojeće opsege (160m, 80m, 40m, 20m, 2m, 70cm).
Za svaki postojeći opseg dodaj: 1-2 rečenice o propagaciji i beacon frekvenciju.
Zatim dodaj NOVE opsege s tablicama (EU vs USA):

### 60m (5 MHz)
- Status u HR (poseban pravilnik), 5 kanala, max snaga, samo USB/CW/digitalni

### 30m (10 MHz) — WARC opseg
- Samo CW i digitalni modovi (FT8 @ 10.136, WSPR @ 10.140), bez SSB!
- Odličan za dugi domet noću

### 17m (18 MHz) — WARC opseg
- FT8 @ 18.100, SSB @ 18.068-18.168
- Odličan DX opseg, manje gužve od 20m

### 15m (21 MHz)
- Dnevni opseg, ovisi o SFI (otvoren samo pri višim SFI)
- FT8 @ 21.074, SSB/CW plan

### 12m (24 MHz) — WARC opseg
- "Spava" kad je SFI nizak, otvara se pri SFI>120
- FT8 @ 24.915

### 10m (28 MHz)
- Ogroman opseg (2 MHz!), ima i FM simplex (29.600)
- Sjajan kada je otvoren, ali ovisi o sunčevom ciklusu
- FT8 @ 28.074, AM, FM simplex, satelitski

### 6m (50 MHz) — "Magic Band"
- Sporadic-E sezona (svibanj-srpanj), DX do 2000 km iznenada!
- Beacon frekvencija: 50.000-50.100 MHz (CW beacons)
- FM pozivni: 51.510 (EU) / 52.525 (USA)
- SSB DX: 50.150 MHz

### 23cm (1296 MHz)
- Kratki opis: SSB/CW DX @ 1296.200, ATV, digitalni modovi
- Posebna oprema potrebna (konverteri, parabolične antene)

### Mikrovalni opsezi — pregled
- 3cm (10 GHz), 2cm (24 GHz), Kortka tabela s opsezima

## Napomena o WARC opsezima
!!! warning "WARC opsezi — bez natjecanja!"
  30m, 17m i 12m su WARC opsezi (dodijeljeni 1979.). 
  Na njima su zabranjena radioamaterska natjecanja po IARU pravilima.

KORAK 4 — Tehničke smjernice:
- Tablice za svaki opseg (EU vs USA razlike)
- Admonitions: note za WARC pravilo, tip za propagaciju
- Interni linkovi: propagation.md, modes.md, license_classes.md

KORAK 5 — Spremi u docs/operating/bandplans.md
```

---

## Bilješke o napretku

- 
