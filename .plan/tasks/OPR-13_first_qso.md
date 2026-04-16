# OPR-13 — Tvoja prva veza

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/operating/first_qso.md` |
| **Status** | 🔴 Ne postoji — kreirati od nule |
| **Prioritet** | P1 — Val 2 |
| **Složenost** | 🔧 Srednja |
| **Ovisnosti** | OPR-04, TEC-05 |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati `docs/operating/procedures.md` (ovisnost)
- [ ] Web search: "ham radio first QSO tips beginners"
- [ ] Web search: "ham radio mic fright overcome tips"
- [ ] Web search: "ham radio first contact SSB example script"
- [ ] Web search: "ham radio listening week before transmitting advice"

### Sadržaj koji treba napisati
- [ ] **Uvodni paragraf** — ohrabrujući ton: svi smo bili na ovom koraku
- [ ] **Checklist priprema:**
  - [ ] Dozvola i pozivna oznaka (ne smijete bez nje!)
  - [ ] Radio (konfiguriran, baterija/napajanje)
  - [ ] Antena spojena i SWR provjeren
  - [ ] Dnevnik veza spreman (papirnat ili software)
  - [ ] Slušalice ili zvučnik
  - [ ] Mirna prostorija (za početak)
- [ ] **Faza 1: Slušanje (prvi tjedan!):**
  - [ ] Zašto tjedan slušanja? Naučiti ritam, prepoznati QSO strukturu
  - [ ] Što slušati: FM repetitor (najjasnije), SSB na 20m, FT8 waterfall
  - [ ] Kako prepoznati CQ poziv
  - [ ] Prepoznati QSO tijek (izmjena i kraj)
- [ ] **Faza 2: Prva veza na repetitoru (najlakši start):**
  - [ ] Zašto repetitor? FM, jasan zvuk, lokalni partneri, nema problema s dopirom
  - [ ] Step by step: programiriraj, slušaj, identificiraj ("9A1ZG monitoring")
  - [ ] Česti scenariji: netko te pozove, ti pozivaš
  - [ ] Transkript primjera u code bloku
- [ ] **Faza 3: Odgovaranje na HF CQ:**
  - [ ] Pronalaženje slobodne frekvencije za slušanje
  - [ ] DX cluster kako pratiti (DX Summit, DXMaps)
  - [ ] Čujete CQ — kako odgovoriti, punom pozivnom, jasno
  - [ ] Transkript u code bloku
- [ ] **Faza 4: Tvoj prvi CQ:**
  - [ ] Provjera frekvencije ("QRL? QRL?" — je li frekvencija slobodna)
  - [ ] Format CQ poziva, ne predugo
  - [ ] Što raditi ako nitko ne odgovori (probati drugi band, drugi termin)
- [ ] **Kompletni SSB QSO transkript (detaljno annotiran):**
  - Svaka linija s objašnjenjem u komentaru
  - Varijante (kratki vs duži QSO)
- [ ] **Strah od mikrofona:**
  - [ ] Normalno je — svi su ga imali
  - [ ] Praktični savjeti: vježbaj sam, zapiši što ćeš reći
  - [ ] Lako okruženje: repetitor prijatelja, lokalni klub
  - [ ] Niko ne ocjenjuje početnika surovo (elmer tradicija!)
- [ ] **Česte greške početnika:**
  - [ ] Preslabe S/N — ne čuju te
  - [ ] Premala pauza za odgovor
  - [ ] Zaboraviti na identificiranje
  - [ ] "Uhm" pauze — snimaj se i slušaj
  - [ ] CQ bez provjere frekvencije
- [ ] **Što zapisati u dnevnik:** UTC, pozivna, frekvencija, mod, RST
- [ ] **Admonitions** — minimalno 4 (tip za ohrabrenje, warning za bez dozvole, note za dnevnik, example za transkript)
- [ ] **Interni linkovi** — procedures.md, repeaters.md, logbook.md, exams.md

### Kontrola kvalitete
- [ ] Minimalno 2000 riječi
- [ ] Ton OHRABRUJUĆI kroz cijelu stranicu
- [ ] Kompletni SSB transkript u code bloku
- [ ] Checklist priprema prisutan
- [ ] Strah od mikrofona sekcija prisutna
- [ ] **mkdocs.yml** — dodati pod Rad na opsegu
- [ ] `.en.md` stub

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Kreiraj novu stranicu docs/operating/first_qso.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- .plan/01_VIZIJA_I_STANDARDI.md
- docs/operating/procedures.md  (za kontekst procedure i QSO primjera)

KORAK 2 — Istraži web:
- "ham radio first QSO beginners guide tips"
- "ham radio microphone fright overcome shy"
- "ham radio listening week advice before transmitting"

KORAK 3 — Napiši stranicu s minimalno 2000 riječi. TON MORA biti prijateljski i ohrabrujući!

# Tvoja prva veza (First QSO)

## Uvod
- Svi smo bili tu — i svi smo preživjeli prvu vezu!
- Kratka priča o tome što se zapravo dogodi pri prvoj vezi

## Priprema — checklist
- [ ] Dozvola i pozivna oznaka (bez nje nema predaje!)
- [ ] Radio spojen, napajanje OK
- [ ] Antena spojena, SWR < 2:1 provjeren
- [ ] Dnevnik spreman (barem papir i olovka)
- [ ] Slušalice/zvučnik podešeni
!!! tip "Ne mora biti savršeno — dovoljno je funkcionalno"

## Faza 1: Tjedan slušanja
Zašto? Naučiti "jezik" radio veza slušajući
Što slušati:
- FM repetitor: najjasniji, lokalni, idealan za početak
- 20m SSB (14.150-14.350): veze na engleskom
- FT8 waterfall: vizualno razumijevanje izmjena
Prepoznaj: CQ poziv, odgovor, razmjena, 73 kraj

## Faza 2: Prva veza na repetitoru
Zašto repetitor? Najmanji rizik: lokalni partneri razumiju početnike!
Step-by-step:
1. Programiraj: output frekvencija, offset, CTCSS ton
2. Slušaj 5 minuta
3. Pritisni PTT, identificiraj se: "9A1ZG monitoring"
4. Čekaj odgovor ili zovi direktno poznatog OM-a

Primjer transkript (code blok):
```
9A1ZG: "9A1ZG radi, ima li koga?"
9A3XY: "9A3XY slušam"  
9A1ZG: "Dobar dan, 9A1ZG, Jasmin iz Zagreba, 73"
9A3XY: "73, Jasmin, lijep signal, 9A3XY"
```

## Faza 3: Odgovaranje na HF CQ
Pronađi CQ na 20m (14.150-14.350 MHz, USB):
1. Čujete: "CQ CQ CQ de OE3XYZ OE3XYZ K"
2. Provjerite: je li signal jak? Razumijete ga?
3. Odgovorite punom pozivnom: "OE3XYZ de 9A1ZG 9A1ZG"
4. Pričekajte

Transkript (kompletni, annotiran):
```
OE3XYZ: "CQ CQ de OE3XYZ OE3XYZ K"          # on zove
9A1ZG: "OE3XYZ de 9A1ZG 9A1ZG"               # tvoj odgovor
OE3XYZ: "9A1ZG de OE3XYZ, nice to meet you,  
   UR 59, name is Hans, QTH Vienna, over"     # razmjena info
9A1ZG: "OE3XYZ de 9A1ZG, also 59 for you,
   name is Jasmin, QTH Zagreb, thanks Hans, 73 de 9A1ZG" # tvoja razmjena
OE3XYZ: "73 Jasmin, nice QSO, OE3XYZ clear"  # kraj
```

## Faza 4: Tvoj prvi CQ poziv
Provjera frekvencije: "QRL? QRL?" — pričekaj 10 sekundi
Format CQ: "CQ CQ de 9A1ZG 9A1ZG 9A1ZG kilo"
Trajanje: 2-3 puta, ne više od 30 sekundi
Ako nema odgovora: probaj drugi band, drugi termin

## Strah od mikrofona
- [ ] Potpuno normalan — gotovo svaki radioamater ga je imao
Praktični savjeti:
1. Vježbaj SAM — izgovori vezu pred ogledalom
2. Najprije pozovi prijatelja (OM iz kluba) koji te čeka
3. Snimi se na telefon i preslušaj — zvučiš bolje nego misliš
4. Repetitor = sigurniji prostor od HF pile-up-a
!!! tip "Radioamaterska zajednica je iznimno ljubazna prema početnicima. Niko te ne ocjenjuje!"

## Česte greške
Tablica: Greška | Zašto se događa | Rješenje
- Premala snaga → Preslabo se čuješ → Podesi ALC, provjeri SWR
- Zaboraviš se identificirati → Uzbuđenje → Napiši si podsjetnik
- Prekraća pauza → Žurba → Pričekaj 3-5 sekundi
- QRL provjera preskočena → Neoprezan start → Uvijek provjeri!

## Što zapisati u dnevnik
Obavezno: UTC, pozivna korespondenta, frekvencija (ili band), mod, RST sent/rcvd, ime i QTH (ako razmijenjeno)

KORAK 4 — Tehničke smjernice:
- Code blokovi za SVE transkripte
- Checkliste za pripremu i greške
- Tablice gdje je prikladno
- Admonitions: minimalno 4 (mix od tip, note, warning)
- Ton UVIJEK ohrabrujući i prijateljski

KORAK 5 — Spremi u docs/operating/first_qso.md (nova datoteka)
KORAK 6 — Dodaj u mkdocs.yml nav → Rad na opsegu (ISPRED procedures.md):
  - Tvoja prva veza: operating/first_qso.md
KORAK 7 — Kreiraj stub docs/operating/first_qso.en.md
```

---

## Bilješke o napretku

- 
