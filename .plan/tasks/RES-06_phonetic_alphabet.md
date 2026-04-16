# RES-06 — NATO fonetska abeceda

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/resources/phonetic_alphabet.md` |
| **Status** | 🔴 Ne postoji — kreirati od nule |
| **Prioritet** | P1 — Val 2 |
| **Složenost** | ⚡ Brzo |
| **Ovisnosti** | OPR-04 |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Web search: "NATO phonetic alphabet complete table pronunciation"
- [ ] Web search: "ham radio phonetic alphabet numbers pronunciation"
- [ ] Web search: "radio prosigns AR SK KN BT DN explained"

### Sadržaj koji treba napisati
- [ ] **Uvodni paragraf** — zašto fonetska abeceda (razlikovanje lako-zamjenjivih slova)
- [ ] **Kompletna tablica abecede** (26 slova):
  Stupci: Slovo | NATO naziv | Izgovor (HR fonetski) | Primjer upotrebe
- [ ] **Brojevi (0-9):**
  - [ ] Uobičajeni radio izgovor (NINER za 9, FIFE za 5, etc.)
  - [ ] Tablica: Broj | Radio izgovor | Napomena
- [ ] **Primjer: Spelanje pozivne oznake:**
  - [ ] 9A1ZG = "Niner Alpha One Zulu Golf"
  - [ ] OE3XYZ = "Oscar Echo Three X-ray Yankee Zulu"
  - [ ] W1AW = "Whiskey One Alpha Whiskey"
- [ ] **Prosignali (procedurni znakovi):**
  - [ ] AR — end of message (svršetak poruke, ali ne i postaje)
  - [ ] SK — end of work (silencija, kraj aktivnosti)
  - [ ] BK — break (pauza, poziv za odgovor)
  - [ ] KN — over to named station only
  - [ ] K — over (poziv svim stanicama za odgovor)
  - [ ] DN — do not answer (ne odgovarajte)
  - [ ] Tablica: Prosignal | CW znakovi | Znači | Kada koristiti
- [ ] **Vježba tipovi:**
  - [ ] Spelaj auto registracije (npr. ZG-1234-AB)
  - [ ] Spelaj poštanske adrese
  - [ ] Spelaj tuđa imena i prezimena
  - [ ] 5 minuta dnevno → tjedan → automatsko!
- [ ] **Česte greške:**
  - [ ] "Victor" umjesto "Whiskey" za W
  - [ ] Govoriti "X" umjesto "X-ray"
  - [ ] Govoriti cijelu poruku bez pauze
- [ ] **Admonitions** — 2 (tip za vježbu, note za izgovor brojeva)
- [ ] **Interni linkovi** — procedures.md, cw_learning.md (prosignali)

### Kontrola kvalitete
- [ ] Kompletnih 26 slova u tablici
- [ ] Svi brojevi (0-9) u tablici
- [ ] Prosignali tablica kompletna
- [ ] Primjer spelanja pozivnih oznaka
- [ ] **mkdocs.yml** — dodati pod Resursi
- [ ] `.en.md` stub (može biti kraći)

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Kreiraj novu stranicu docs/resources/phonetic_alphabet.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- .plan/01_VIZIJA_I_STANDARDI.md

KORAK 2 — Istraži web:
- "NATO phonetic alphabet complete table all 26 letters pronunciation"
- "ham radio number pronunciation niner fife Oscar"
- "CW prosigns AR SK BK KN ham radio explained"

KORAK 3 — Napiši stranicu (minimalno 800 riječi):

# NATO fonetska abeceda

## Uvod (kratko)
Zašto B i V, M i N, F i S zvuče slično u lošim uvjetima → NATO abeceda rješava to.

## Kompletna tablica abecede
Tablica (26 redaka):
Slovo | NATO naziv | Izgovor (HR fonetski) | Primjer u HAM radiu
A | Alpha | AL-FA | Alpha za "A" u QTH
B | Bravo | BRA-VO | ...
C | Charlie | ČARLI | ...
D | Delta | DEL-TA | ...
E | Echo | EKO | ...
F | Foxtrot | FOKS-TROT | ...
G | Golf | GOLF | ...
H | Hotel | HO-TEL | ...
I | India | IN-DI-JA | ...
J | Juliet | DŽU-LI-ET | ...
K | Kilo | KI-LO | ...
L | Lima | LI-MA | ...
M | Mike | MAJK | ...
N | November | NO-VEM-BER | ...
O | Oscar | OS-KAR | ...
P | Papa | PA-PA | ...
Q | Quebec | KVI-BEK | ...
R | Romeo | RO-ME-O | ...
S | Sierra | SI-E-RA | ...
T | Tango | TAN-GO | ...
U | Uniform | JU-NI-FORM | ...
V | Victor | VIK-TOR | ...
W | Whiskey | VIS-KI | ...
X | X-ray | EKS-REJ | ...
Y | Yankee | JAN-KI | ...
Z | Zulu | ZU-LU | ...

## Brojevi u radio prometu
Tablica:
Broj | Standardni radio izgovor | Napomena
0 | Zero | Ili "Oh" u aviaciji
1 | One | —
2 | Two | —
3 | Three | —
4 | Four | —
5 | Fife | (ne "Five"!) — razlikuje se od "Nine"
6 | Six | —
7 | Seven | —
8 | Eight | —
9 | Niner | (ne "Nine"!) — razlikuje se od "Five" ili "Line"

!!! tip "Fife i Niner" — obavezno koristiti ove radio izgovore!

## Primjeri spelanja
Spelanje pozivnih oznaka:
- 9A1ZG → "Niner Alpha One Zulu Golf"
- OE3XYZ → "Oscar Echo Three X-ray Yankee Zulu"  
- W1AW → "Whiskey One Alpha Whiskey"

Spelanje u QSO-u:
"My name is JASMIN, Juliet Alpha Sierra Mike India November, over."

## Prosignali (CW i glasovni)
Tablica:
Prosignal | CW | Glasovni ekvivalent | Kada koristiti
AR | .-.-. | "End of message" | Kad završiš poruku, pozivas za odgovor
SK | ...-.- | "Silent Key / End of work" | Kraj rada, silencija
BK | -...-.- | "Break, over" | Brza pauza za odgovor
K | -.- | "Over" (poziva sve) | Kad završiš i pozivaš bilo koga
KN | -.-. | "Over to named only" | Samo tražena postaja neka odgovori
DN | -.. -. | "Do not answer" | Broadcast bez odgovora

## Vježba
- Vježbaj svaki dan 5 minuta! Uzmi auto tablica, adresar, račune — spelaj sve!
- Aplikacije: Military Alphabet Trainer (Android/iOS)
- Cilj: 10 sekundi → automatski bez razmišljanja

## Česte greške
- Govoriti "V kao Victor" umjesto "V kao Whiskey" ← GREŠKA! Whiskey počinje s W!
  Ispravno: "V kao Victor" — Victor JE za V
- Govoriti "X" umjesto "X-ray" — nije dovoljno jasno

KORAK 4 — Tehničke smjernice:
- Tablice za sva 26 slova, brojeve i prosignale — OBAVEZNO
- Admonitions: minimalno 2
- Interni linkovi: procedures.md, cw_learning.md

KORAK 5 — Spremi u docs/resources/phonetic_alphabet.md (nova datoteka)
KORAK 6 — Dodaj u mkdocs.yml nav → Resursi:
  - NATO fonetska abeceda: resources/phonetic_alphabet.md
KORAK 7 — Kreiraj stub docs/resources/phonetic_alphabet.en.md
```

---

## Bilješke o napretku

- 
