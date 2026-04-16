# ACT-02 — Natjecanja (Contesting)

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/activities/contesting.md` |
| **Status** | 🟢 Postoji, treba proširiti |
| **Prioritet** | P1 — Val 1 |
| **Složenost** | 🏗️ Velika |
| **Ovisnosti** | OPR-04 |
| **Završeno** | ☑ |

---

## Checklist

### Priprema
- [x] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [x] Pročitati postojeći `docs/activities/contesting.md` (~836 bajtova)
- [x] Web search: "CQ WW DX contest rules categories scoring 2024"
- [x] Web search: "ham radio contesting categories single op multi op QRP assisted"
- [x] Web search: "N1MM+ logging software setup contest"
- [x] Web search: "Cabrillo log format submission ham radio"
- [x] Web search: "ham radio contesting strategy rate vs multiplier"
- [x] Web search: "9A CW contest 9A activity contest rules"

### Sadržaj koji treba dodati
- [x] **Uvodni paragraf** — zašto natjecanja, "olimp" hobija
- [x] **Što je contest QSO** — brza razmjena, za razliku od normalnog QSO
- [x] **Kategorije operatora** (tablica kompletna):
  - [x] Single Operator (SO) — solo, bez pomoći
  - [x] Single Op Assisted (SOA) — solo ali s DX clusterom
  - [x] Multi Operator Single TX (M/S) — duet
  - [x] Multi Operator Two TX (M/2) — napredni tim
  - [x] Multi Operator Multi TX (M/M) — veliki timovi, ekspedicije
  - [x] Overlay kategorije: QRP (<5W), Rookie (<3g. licence), Classic (bez asistencije)
- [x] **Bodovanje — detaljno:**
  - [x] Multiplieri — što su, zašto vrijede više od QSO-a
  - [x] Primjer bodovanja CQ WW: QSO bodovi × (Zone multiplieri + DXCC multiplieri)
  - [x] Primjer izračuna: 100 QSO × 3 boda × 50 multipliera = 15.000 bodova
- [x] **Detaljni kalendar natjecanja** (tablica: Natjecanje | Termin | Mod | Napomena):
  - [x] CQ WW DX (SSB — listopad, CW — studeni)
  - [x] ARRL DX (SSB — veljača, CW — ožujak)
  - [x] IOTA Contest (srpanj)
  - [x] 9A CW Contest (prosinac)
  - [x] 9A Activity Contest (tjedni)
  - [x] WAE DX Contest (kolovoz SSB, listopad CW)
  - [x] CQ WPX (SSB — ožujak, CW — svibanj)
  - [x] RDXC (Russian DX — ožujak)
  - [x] DARC DLD (Digital)
- [x] **Softver za natjecanja** (tabbed usporedba):
  - [x] N1MM+ — najpopularniji, Windows, besplatan, CAT integracija
  - [x] DXLog.net — cross-platform, licenciran, moderne mogućnosti
  - [x] SkookumLogger — Mac
  - [x] Win-Test — profesionalni
- [x] **Strategija:**
  - [x] Rate vs Multiplier — kompromis
  - [x] Band hopping — što, kada, zašto skakati po opsezima
  - [x] Running vs S&P (Search & Pounce)
  - [x] When to call CQ, kada ići S&P
  - [x] Solar cycle i koji opseg kada
- [x] **Postavljanje stanice za contest:**
  - [x] Što poboljšati (antene, PA, filteri)
  - [x] Operatorski setup (dva monitora, headset, paddles)
  - [x] Preventivna provjera: SWR, keyer speed, macro setup
- [x] **Cabrillo log format:**
  - [x] Što je Cabrillo, przykład
  - [x] Kako generirati iz N1MM+ i DXLog
  - [x] Rokovi slanja, gdje slati
- [x] **9A specifičnosti:**
  - [x] 9A CW Contest — pravila, exchange (9A: okrug, ostali: RST+serijski)
  - [x] 9A Activity Contest — sedmični, svi modovi
  - [x] Memorijalni contestovi (check za aktualne)
- [x] **Kako početi s contesting-om:**
  - [x] Počni kao "Single Op All Band Low Power"
  - [x] Postavi N1MM+, proba setup unaprijed
  - [x] Sudjeluj par sati, ne 48h odmah
- [x] **Admonitions** — minimalno 3 (tip za početnike, note za pravila, info za Cabrillo)
- [x] **Interni linkovi** — procedures.md, logbook.md, bandplans.md, special_events.md

### Kontrola kvalitete
- [x] Minimalno 2000 riječi ukupno
- [x] Tablica kategorija kompletna
- [x] Tablica kalendara natjecanja kompletna
- [x] Tabbed usporedba softvera prisutna
- [x] Primjer bodovanja prisutan
- [x] `.en.md` ažuriran ili stub
- [x] `mkdocs.yml` ne treba mijenjati

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Proširi stranicu docs/activities/contesting.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- docs/activities/contesting.md  (ZADRŽI SAV POSTOJEĆI SADRŽAJ!)
- .plan/01_VIZIJA_I_STANDARDI.md

KORAK 2 — Istraži web:
- "CQ WW DX contest rules categories scoring multipliers"
- "ham radio contesting categories SO SOA MS MM QRP overlay"
- "N1MM+ vs DXLog contesting software comparison"
- "Cabrillo log format ham radio contest submission"
- "9A CW contest 9A activity contest Croatia rules"

KORAK 3 — ZADRŽI sve postojeće, proširi na minimalno 2000 riječi:

## Kako funkcionira contest QSO
- Brza razmjena: RST + nešto (zona, serijski, lokator...)
- Ne vrijedi normalni razgovor
- Primjer exchange transkript (code blok, SSB i CW)

## Kategorije (kompletna tablica)
Kategorija | Opis | Max TX | Asistencija | Prikladno za
Single Op | Solo | 1 | Ne | Početnike i iskusne
Single Op Assisted | Solo s clusterom | 1 | DX cluster | Početnike
Multi/Single | 2+ op, 1 TX | 1 | Da | Timski rad
Multi/Two | 2 TX simultano | 2 | Da | Klubovi
Multi/Multi | Neograničeno | Neogr. | Da | Ekspedicije
QRP | Maks 5W | 1 | Opcija | Entuzijasti

## Bodovanje (na primjeru CQ WW)
Tablica: Element | Kako se broji
QSO bodovi: EU ↔ EU = 1, EU ↔ drugi kontinent = 3
Zone multiplier: svaka ITU zona jednom po bandu
DXCC multiplier: svaka zemlja jednom po bandu
Formula: Ukupno = Σ QSO_bodova × Σ(Zone + DXCC) po bandu
Primjer: 500 QSO × 250 boda × 100 mult = 25.000.000 bodova

## Kalendar natjecanja (tablica)
Natjecanje | Mod | Termin | Razmjena | Link
CQ WW DX SSB | SSB | Listopad | RST + ITU zona | cqww.com
CQ WW DX CW | CW | Studeni | RST + ITU zona | cqww.com
ARRL DX SSB | SSB | Veljača | RST + State/Power | arrl.org
...9A CW, 9A Activity, IOTA, WAE, WPX...

## Softver (tabbed format)
=== "N1MM+"
    Najpopularniji, Windows, besplatan
    - CAT integracija, automatski macro
    - Podržava 1000+ contesta
    - Download: n1mm.hamdocs.com

=== "DXLog.net"
    Cross-platform, plaćeni
    - Moderne mogućnosti, cloud backup
    - Odličan za teamove

=== "Win-Test"    
    Profesionalni, Windows, plaćeni
    - Koriste top contesteri world-wide

## Strategija
- Rate vs Multiplier: kompromis — visoki multiplieru > rate na kraju benda
- Running (ostaj na freq i zovi CQ) vs S&P (tražiš po bendu)
- Band hopping: kada koji opseg otvoriti, koristiti propagacij.md
- Solar cycle utjecaj: visoki SFI → 10m i 15m; niski SFI → 40m i 80m

## Cabrillo log format
Primjer Cabrillo headera (code blok)
Kako generirati iz N1MM+ (Step: File → Export → Cabrillo)
Rok i adresa slanja za CQ WW

## 9A natjecanja
- 9A CW Contest: prosinac, razmjena za 9A postaje je HQ okrug
- 9A Activity Contest: tjedni, svaki utorak/petak/nedjelja
- Memorijalni contestovi: provjeriti HRS web

## Kako krenuti (za početnike)
1. Preuzmi i instaliraj N1MM+
2. Konfiguriraj: pozivna, rig CAT, audio za CW/voice keyer
3. Odaberi "meko" natjecanje (9A Activity, IOTA) za vježbu
4. Sudjeluj samo 3-4 sata (ne cijeli weekend na početku!)
5. Pošalji Cabrillo log (i gubitnici dobivaju certifikat!)

KORAK 4 — Tehničke smjernice:
- Tablice za kategorije i kalendar
- MkDocs tabbed format za softver
- Code blok za Cabrillo primjer
- Admonitions: minimalno 3

KORAK 5 — Spremi u docs/activities/contesting.md
```

---

## Bilješke o napretku

- 
