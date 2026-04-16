# RES-08 — Priprema za ispit

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/resources/exam_prep.md` |
| **Status** | 🔴 Ne postoji — kreirati od nule |
| **Prioritet** | P1 — Val 2 |
| **Složenost** | 🏗️ Velika |
| **Ovisnosti** | REG-02, sve TEC moduli |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati `docs/regulations/exams.md`
- [ ] Pročitati `docs/regulations/croatian_regs.md`
- [ ] Web search: "radioamaterski ispit Hrvatska pitanja HAKOM gradivo"
- [ ] Web search: "ham radio exam questions training B license"
- [ ] Web search: "amateur radio exam preparation schedule study plan"
- [ ] Pregledati priručnik za gradivo — sve TEC i REG stranice

### Sadržaj koji treba napisati

#### Plan učenja
- [ ] **Vremenski raspored** — za 2-3 månader:
  - Tjedan 1-2: Propisi i dozvole
  - Tjedan 3-4: Osnove elektronike
  - Tjedan 5-6: Antene i propagacija
  - Tjedan 7-8: Modovi i procedura
  - Tjedan 9-10: Repeticija + online testovi
  - Tjedan 11-12: Proba ispita, slabe točke
  - Tablica: Tjedan | Tema | Stranice u priručniku | Cilj
- [ ] **Preporučeno dnevno**: 30-45 minuta, svaki dan

#### Sažetak gradiva po temama
Za svaku temu — kratki sažetak + link na stranicu priručnika:
- [ ] Propisi i dozvole (link na regulations/)
- [ ] Osnove elektronike (link na electronics.md)
- [ ] Antene (link na antennas.md)
- [ ] Propagacija (link na propagation.md)
- [ ] Modovi rada (link na modes.md)
- [ ] Sigurnost (link na safety.md)
- [ ] Procedura i etiketa (link na procedures.md)
- [ ] Frekvencijski planovi (link na bandplans.md)

#### Primjeri ispitnih pitanja (15-20 pitanja)
Za svaku kategoriju gradiva — 2-4 tipična pitanja s odgovorima:

**Propisi:**
- [ ] Koji razred dozvole smije koristiti sve amaterske opsege u HR?
- [ ] Što je CEPT dozvola i što omogućuje?
- [ ] Kolika je maksimalna snaga za razred B u HR?

**Elektronika:**
- [ ] Što se dogodi s rezonantnom frekvencijom ako povećamo induktivitet?
- [ ] Izračunaj: R1=100Ω, R2=200Ω spojena serijski — ukupni otpor?
- [ ] Što je impedancija i zašto je bitna za radio?

**Antene:**
- [ ] Kolika je duljina dipola za 14 MHz?
- [ ] Što je SWR 2:1 i što to znači za stanicu?
- [ ] Što je Balun i kdy se koristi?

**Propagacija:**
- [ ] Koji ionosferski sloj je najvažniji za HF DX?
- [ ] Što je MUF i što se dogodi kad je MUF ispod radne frekvencije?
- [ ] Što znači K-indeks 7 za radioamatere?

**Modovi i procedura:**
- [ ] Koji mod se koristi ispod 10 MHz za glasovnu vezu?
- [ ] Što znači "QSL" u radioamaterskom žargonu?
- [ ] Kako se provjeri je li frekvencija slobodna?

**Sigurnost:**
- [ ] Zašto kondenzatori ostaju napunjeni i nakon gašenja uređaja?
- [ ] Što je MPE i zašto je relevantan?

- [ ] **Svako pitanje mora imati:** točan odgovor + objašnjenje ZAŠTO (to je ključna razlika od pamćenja!)

#### Savjeti za dan ispita
- [ ] Što ponijeti (dokumenti, olovka, kalkulator?)
- [ ] Koliko vremena za svako pitanje
- [ ] Strategija za nesigurna pitanja
- [ ] Opuštanje — tehnika disanja

#### Online resursi za vježbu
- [ ] HAKOM baza pitanja (ako postoji javno)
- [ ] Ham radio exam practice websites (međunarodni)
- [ ] Mobilne aplikacije za vježbu
- [ ] Virtualni ispiti

- [ ] **Admonitions** — minimalno 3 (tip za plan učenja, note o gradivu, example za pitanje)
- [ ] **Interni linkovi** — barem 8 linkova na relevantne stranice priručnika

### Kontrola kvalitete
- [ ] Minimalno 2000 riječi
- [ ] Plan učenja u tablici
- [ ] 15+ pitanja s objašnjenjima
- [ ] Linkovi na sve relevantne stranice priručnika
- [ ] **mkdocs.yml** — dodati pod Resursi
- [ ] `.en.md` stub

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Kreiraj novu stranicu docs/resources/exam_prep.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- .plan/01_VIZIJA_I_STANDARDI.md
- docs/regulations/exams.md  (za kontekst ispitnog procesa)
- docs/regulations/croatian_regs.md  (za kontekst propisa)

KORAK 2 — Istraži web:
- "radioamaterski ispit Hrvatska gradivo HAKOM 2024"
- "ham radio exam study plan schedule weeks"
- "amateur radio license exam practice questions online"

KORAK 3 — Napiši stranicu s minimalno 2000 riječi:

# Priprema za radioamaterski ispit

## Uvod
Kratki opis pristupa: aktivno učenje, razumijevanje (ne pamćenje!), konzistentnost.

## Plan učenja (2-3 månader)
Tablica: Tjedan | Tema | Materijal u priručniku | Provjera
1-2 | Propisi i dozvole | regulations/ stranice | Znam razrede i opsege
3-4 | Osnove elektronike | technical/electronics.md | Znam Ohmov zakon, LC krug
5-6 | Antene i vodovi | technical/antennas.md, propagation.md | Znam dipol i SWR
7-8 | Modovi, procedura | operating/ stranice | Znam LSB/USB, Q-kodove
9-10 | Sigurnost i sigurnostno | technical/safety.md, grounding.md | Mogu prepoznati opasnosti
11-12 | Repeticija + probe | Svo gradivo | Rješavam probe ispite 80%+

!!! tip "30 minuta SVAKI dan bolje je od 4 sata vikendima!"

## Sažetak gradiva s linkovima

### Propisi i dozvole
- Razredi dozvola (N, B, A) → [Razredi dozvola](../regulations/license_classes.md)
- HAKOM i HRS → [Hrvatski propisi](../regulations/croatian_regs.md)
- CEPT i međunarodni → [Međunarodni propisi](../regulations/international_regs.md)
KLJUČNO: Razred A = CEPT = smijete raditi u svim CEPT zemlja bez posebne dozvole!

### Osnove elektronike
[Osnove elektronike](../technical/electronics.md)
KLJUČNE formule: Ohm (U=R·I), Snaga (P=U·I), Rezonanca (f=1/2π√LC)

### Antene itd... (slično za sve kategorije)

## Primjeri ispitnih pitanja (s objašnjenjima)

### Pitanja: Propisi
P: Koji razred dozvole u HR omogućuje rad na svim amaterskim opsezima?
O: Razred A (CEPT razred)
Zašto: Razred N i B imaju ograničenja na opsege i snagu. Samo razred A daje
pune privilegije uključujući CEPT status za međunarodnu upotrebu.

P: Što je maksimalna efektivna izračena snaga (ERP) za razred B u HR?
O: [Odgovor prema aktualnom pravilniku]
Zašto: [Objašnjenje]

P: Što je CEPT dozvola i što omogućuje nositelju?
O: CEPT T/R 61-01 = sporazum zemalja. A razred automatski vrijedi u ~50 CEPT zemlja.
Zašto: Znači možete raditi u Italiji, Austriji, Njemačkoj bez posebne prijave.

### Pitanja: Elektronika
P: Otpornici R1=100Ω i R2=150Ω spojeni su serijski. Koliki je ukupni otpor?
O: R = 100 + 150 = 250Ω (serijski se zbrajaju)
Zašto: U serijskom spoju isti tok struje prolazi kroz sve elemente.

P: Koji element u LC titrajnom krugu određuje rezonantnu frekvenciju?
O: Oba! f = 1 / (2π√(LC)) — ovisi o L i C zajedno
Zašto: Povećaj L → niža frekvencija. Povećaj C → niža frekvencija. Smanji jedno → viša.

P: Što je impedancija i zašto je bitna za radio stanice?
O: Impedancija je ukupni otpor AC struji (Z = R + jX). Bitna jer antena,
kabel i radio moraju imati iste impedancije (50Ω) — inače nastaju stojni valovi (SWR).

### Pitanja: Antene i propagacija
P: Kolika je duljina polu-valnog dipola za 14 MHz?
O: L = 143 / 14 ≈ 10.2 metra (ukupno), svaka grana ≈ 5.1m
Zašto: Praktički formula: 143/f(MHz) = duljina u metrima.

P: Koji ionosferski sloj je najvažniji za DX na HF?
O: F2 sloj (visina 250-400 km), posebno noću
Zašto: Najviši sloj, reflektira na najvećim dometima, traje i noću.

P: Što znači SWR 3:1?
O: Neslaganje impedancije: do 50% snage se vraća u radio
Zašto: Idealan SWR je 1:1. Do 1.5:1 je odlično. Iznad 2:1 treba tražiti uzrok.

### Pitanja: Modovi i procedura
P: Koji mod se koristi za glasovnu vezu ispod 10 MHz na HF-u?
O: LSB (Lower Sideband) — konvencija za 80m, 40m
Zašto: USB je konvencija za opsege iznad 10 MHz (20m, 15m, itd.)

P: Što znači "QSL" kao izjava (ne pitanje)?
O: "Potvrđujem primitak / razumio sam"
Zašto: Q-kodovi imaju dvojako značenje: kao pitanje i kao izjava.

P: Kolega na opsegu pita "QRL?" — što odgovarate ako je frekvencija zauzeta?
O: "QRL, QRL" ili "Yes, QRL" — frekvencija je zauzeta
Zašto: Ne odgovorite = frekvencija slobodna. Odgovorite = zauzeta.

### Pitanja: Sigurnost
P: Zašto su kondenzatori u napajanju opasni i nakon isključivanja?
O: Zadrže naboj (visoki napon) i do 30 minuta — mogu biti smrtonosni!
Zašto: Ispravljač puni kondenzatore na vršni napon AC-a (~325V za 230V mrežu),
a kondenzatori se isprazne tek kroz otpor opterećenja (koji ne postoji kad je isključeno).

P: Što je MPE i zašto je bitan?
O: Maximum Permissible Exposure — maksimalna dozvoljena razina RF polja za ljude.
Npr. ICNIRP smjernice ograničavaju izloženost na 10 W/m² za 900 MHz.
Zašto: Zakon nas obavezuje da antene postavimo da MPE nije prekoračen u dostupnim zonama.

## Savjeti za dan ispita
- Ponesi: osobnu iskaznicu, pozivnicu/potvrdu prijave, olovku
- Kalkulator: provjerite smiju li se koristiti
- Tehnika: čitaj SVAKO pitanje do kraja, pa eliminacija pogrešnih
- Nesigruno → Označi i vrati se poslije (ako ima runda)
- Opuštanje: duboki udah, sporo puštanje — snizi adrenalin

## Online resursi za vježbu
- (Linkovi na HR specifične resurse za vježbu pitanja ako postoje)
- Ham Test Online (hamstudy.org) — US fokus ali dobra logika
- RadioAmateur.eu — europski fokus

KORAK 4 — Tehničke smjernice:
- Tablica plana učenja OBAVEZNA
- 15+ pitanja s odgovorima i objašnjenjima (KLJUČNO: ne samo odgovor, nego ZAŠTO)
- Linkovi na 8+ stranica priručnika
- Admonitions: minimalno 3

KORAK 5 — Spremi u docs/resources/exam_prep.md (nova datoteka)
KORAK 6 — Dodaj u mkdocs.yml nav → Resursi:
  - Priprema za ispit: resources/exam_prep.md
KORAK 7 — Kreiraj stub docs/resources/exam_prep.en.md
```

---

## Bilješke o napretku

- 
