# OPR-04 — Procedura veze

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/operating/procedures.md` |
| **Status** | 🟢 Postoji, treba proširiti |
| **Prioritet** | P1 — Val 1 |
| **Složenost** | 🔧 Srednja |
| **Ovisnosti** | — |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati postojeći `docs/operating/procedures.md` (~4451 bajtova — već opsežan)
- [ ] Web search: "SSB QSO example script ham radio transcript"
- [ ] Web search: "ham radio repeater procedure CTCSS access"
- [ ] Web search: "DX pileup procedure how to work DX station"
- [ ] Web search: "ham radio net procedure check-in control station"

### Sadržaj koji treba dodati
- [ ] **SSB QSO transkript** — kompletni primjer veze (code blok, annotiran):
  - CQ poziv, odgovor, razmjena, 73
  - Tipično trajanje i sadržaj
- [ ] **CW QSO transkript** — kompletni primjer s Morsovim simbolima u code bloku
- [ ] **Procedura za repetitor:**
  - Pristup (CTCSS/DCS tona), pozivanje, kratko identificiranje
  - Etiketa pauza za hitne pozive
  - Razlika od simplex procedure
- [ ] **Pile-up procedura:**
  - Lovač: kako se javiti (punom pozivnom, jednom, čekati)
  - DX stanica: split operacija ("UP 5"), listening window
  - Što NIKADA ne raditi u pileupu
- [ ] **Net procedura:**
  - Što je net, kontrolna stanica (NCS)
  - Check-in procedura, time-controlled, round table
  - Ekstra: traffic net, emergency net
- [ ] **Contest procedura:**
  - Brzi exchange — raport + zona ili serijski broj
  - Pozivanje CQ TEST
  - Kako se odgovoriti na CQ TEST
- [ ] **Proširiti Q-kodove** — dodati 20+ novih koji nedostaju, s primjerom rečenice:
  - QRM, QSB, QRN, QRP, QRT, QRZ, QSL, QSO, QSY, QTH... + još 15
- [ ] **NATO fonetska abeceda** — kompletna tablica (26 slova + brojevi + prosignali)
- [ ] **Prosignali (procedurni znakovi):**
  - AR (kraj poruke), SK (kraj rada), BK (break), KN (samo pozvani da odgovori)
- [ ] **Admonitions** — minimalno 3 (tip, note, warning za pile-up greške)
- [ ] **Interni linkovi** — ethics.md, phonetic_alphabet.md, qcodes.md, first_qso.md

### Kontrola kvalitete
- [ ] Minimalno 3000 riječi ukupno
- [ ] SSB i CW transkripti prisutni u code blokovima
- [ ] Fonetska abeceda kompletna
- [ ] Q-kodovi popis proširen
- [ ] `.en.md` ažuriran ili stub
- [ ] `mkdocs.yml` ne treba mijenjati

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Proširi stranicu docs/operating/procedures.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- docs/operating/procedures.md  (ZADRŽI SAV POSTOJEĆI SADRŽAJ!)
- .plan/01_VIZIJA_I_STANDARDI.md

KORAK 2 — Istraži web:
- "SSB ham radio QSO example transcript complete"
- "ham radio pileup procedure DX working techniques"
- "ham radio net procedure check-in NCS"
- "ham radio contest exchange procedure QSO"

KORAK 3 — ZADRŽI sve postojeće, dodaj sekcije:

## Primjeri kompletnih QSO-a
### SSB QSO (code blok, annotiran komentarima)
```
9A1ZG: "CQ CQ CQ de 9A1ZG 9A1ZG 9A1ZG, kilo"    # CQ poziv
DJ3AB: "9A1ZG de DJ3AB, DJ3AB, over"               # odgovor
9A1ZG: "DJ3AB de 9A1ZG, dobro te čujem, 59..."     # razmjena
...
9A1ZG: "73 de 9A1ZG, clear"                        # kraj
```

### CW QSO (Morse notacija u code bloku)
```
CQ CQ DE 9A1ZG 9A1ZG K
DJ3AB DE 9A1ZG RST 579 579 QTH ZAGREB BK
...
73 SK
```

## Procedura za repetitor
- Pristup s CTCSS tonom
- Kratko identificiranje, pauziranje za hitne pozive
- Razlika od simplex (ne treba "over", dovoljno QSO flow)

## Pile-up procedura
- Kao lovač: punom pozivnom, jednom, pričekati, ne "tutti"
- Split operacija: DX na jednoj frekvenciji, sluša UP 5-10
- Što NIKAD ne raditi: !!! warning "Nikad ne zovite na DX TX frekvenciji!"

## Net procedura  
- Check-in u net (NCS, round table, traffic)
- Disciplina: kontrolna stanica ima prioritet

## Contest procedura
- CQ TEST primjer, exchange format (59 001, 59 14, itd.)
- Brzi QSO tempo

## Proširena lista Q-kodova
Tablica: Q-kod | Upitnik znači | Izjava znači | Primjer korištenja
(Dodaj 25+ Q-kodova koji nedostaju uz primjere)

## NATO fonetska abeceda (kompletna tablica)
Slovo | NATO | Izgovor (HR fonetski) | Primjer

## Prosignali
Tablica: Prosignal | Puni naziv | Kada koristiti

KORAK 4 — Tehničke smjernice:
- Code blokovi za sve transkripte
- Tablice za Q-kodove i fonetiku
- !!! warning za pile-up greške
- Interni linkovi: ethics.md, first_qso.md, phonetic_alphabet.md
- Minimalno 3000 riječi ukupno

KORAK 5 — Spremi u docs/operating/procedures.md
```

---

## Bilješke o napretku

- 
