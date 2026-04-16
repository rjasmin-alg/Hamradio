# OPR-08 — Repetitori

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/operating/repeaters.md` |
| **Status** | 🔴 Ne postoji — kreirati od nule |
| **Prioritet** | P1 — Val 2 |
| **Složenost** | 🔧 Srednja |
| **Ovisnosti** | OPR-03 |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Web search: "ham radio repeater how it works offset CTCSS"
- [ ] Web search: "CTCSS DCS tone squelch table frequencies"
- [ ] Web search: "EchoLink IRLP Allstar ham radio internet linking"
- [ ] Web search: "DMR digital repeater talkgroups hotspot"
- [ ] Web search: "D-STAR repeater reflector DCS explained"
- [ ] Web search: "repeater database Croatia 9A amateur radio"

### Sadržaj koji treba napisati
- [ ] **Uvodni paragraf** — što je repetitor, zašto postoji
- [ ] **Princip rada:**
  - [ ] Simultano primanje i odašiljanje na različitim frekvencijama
  - [ ] Offset — razlika između ulazne i izlazne frekvencije
  - [ ] Analogija: "Radio relej" za produženje dometa
- [ ] **Offset — detaljno:**
  - [ ] 2m: standardni offset -600 kHz (u EU i USA)
  - [ ] 70cm: standardni offset -7.6 MHz (EU) / -5 MHz (USA razlikuje)
  - [ ] Tablica standardnih offseta po opsezima i regijama
- [ ] **CTCSS (Continuous Tone Coded Squelch System):**
  - [ ] Što je, zašto se koristi (više repetitora na sličnoj frekvenciji)
  - [ ] Frekvencijski subtonovi (67.0 Hz - 254.1 Hz)
  - [ ] Kompletna tablica CTCSS tonova
  - [ ] Kako programirati u radio
- [ ] **DCS (Digital Coded Squelch):**
  - [ ] Modernija alternativa CTCSS
  - [ ] Digitalni kodovi (3-znamenkasti)
- [ ] **DTMF:**
  - [ ] Tonovi putem tastera (1-9, *, #, A-D)
  - [ ] Kontrola repetitora (autopatch, IRLP, EchoLink node aktivacija)
- [ ] **Internet linking — pregled:**
  - [ ] EchoLink — što je, kako koristiti, web i mobilna app, link node
  - [ ] IRLP — stariji, robustniji, samo hardware
  - [ ] Allstar / HamVoIP — open source, Node number
  - [ ] Svaki s linkom i kratkim opisom
- [ ] **Digitalni repetitori:**
  - [ ] D-STAR (Icom) — registracija, reflektori, DCS gateway
  - [ ] DMR — talkgroups, brandmeister, hotspots, code plugs
  - [ ] C4FM/Fusion (Yaesu) — Rooms, WIRES-X
  - [ ] Tablica usporedbe: Sustav | Oprema | Prednosti | Zajednica
- [ ] **Repetitori u HR:**
  - [ ] Kako ih pronaći: RepeaterBook.com, HRS lista
  - [ ] Primjer: Zagreb 2m repetitori, 70cm repetitori
- [ ] **Etiketa na repetitoru:**
  - [ ] Kratko identificiranje (ne cijela lozinka svaki puta!)
  - [ ] Pauziranje između rečenica (30-60 sekundi za hitne pozive)
  - [ ] Lokalni vs prolazni (traveling)
  - [ ] Kada NE koristiti repetitor (simplex je bolji kratko)
- [ ] **Procedura veze kroz repetitor — step by step:**
  - [ ] Programirati frekevnciju, offset i CTCSS
  - [ ] Pritisnuti PTT i identifikirati se
  - [ ] Kratki CQ ili direktan poziv
- [ ] **Admonitions** — minimalno 3 (tip za programiranje, note za etiketu, info za EchoLink)
- [ ] **Interni linkovi** — modes.md, bandplans.md, first_qso.md, dmr.md

### Kontrola kvalitete
- [ ] Minimalno 2000 riječi
- [ ] Tablica offseta kompletna
- [ ] Tablica CTCSS tonova prisutna
- [ ] Tablica digitalnih sustava prisutna
- [ ] **mkdocs.yml** — dodati pod Rad na opsegu
- [ ] `.en.md` stub

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Kreiraj novu stranicu docs/operating/repeaters.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- .plan/01_VIZIJA_I_STANDARDI.md
- docs/operating/bandplans.md  (za kontekst frekvencija)

KORAK 2 — Istraži web:
- "ham radio repeater how it works offset frequency"
- "CTCSS tone squelch complete frequency table"
- "EchoLink IRLP Allstar ham radio internet linking comparison"
- "DMR repeater talkgroup brandmeister explained"
- "ham radio repeater etiquette best practices"

KORAK 3 — Napiši stranicu s minimalno 2000 riječi:

# Repetitori (Releji)

## Što je repetitor i zašto postoji
- Produžuje domet ručnih/mobilnih stanica
- Lokacija: visoko (planina, toranj)
- Primjer: 2m handheld ~5km simplex vs repetitor ~100km!

## Princip rada
- Simultano prima (ulaz/input) i odašilje (izlaz/output)
- Uvijek sluša na ULAZNOJ frekvenciji, odašilje na IZLAZNOJ

## Offset
Tablica: Opseg | Standardni offset (EU) | Standardni offset (USA)
- 2m (144 MHz): -600 kHz
- 70cm (432 MHz): -7.6 MHz
- 10m (29 MHz): -100 kHz
...

## CTCSS (Subtonovi)
- Što je: nečujni ton (67-254 Hz) koji otvara squelch repetitora
- Zašto: više repetitora u oblasti, ne žele čuti jedni druge
Kompletna tablica CTCSS tonova (67.0 Hz - 254.1 Hz, ~50 tonova)

## DCS
- Digitalni Coded Squelch — 3-znamenkasti kod umjesto tona
- Moderniji, ali rjeđi

## DTMF kontrola
- Touchtone tonovi za kontrolu: autopatch, aktivacija EchoLink noda
- Primjer: *123# za aktivaciju

## Internet linking
Tablica: Sustav | Osnovan | Mrežni protokol | Kako koristiti
EchoLink | 2002 | VoIP | Web/app ili DTMF node broj
IRLP | 2000 | VoIP | Hardware only, DTMF node broj
Allstar | 2004 | AsteriskVoIP | Open source, node broj

## Digitalni repetitori
Tablica: Sustav | Proizvođač | Ključne značajke | Kako početi
D-STAR | Icom | Registracija (https://www.dstarinfo.com), reflektori (DCS/XRF/REF)
DMR | Otvoreni std. | Talkgroups, Brandmeister mreža, code plug
C4FM/Fusion | Yaesu | Rooms, WIRES-X, kompatibilnost s analognima (AMS)

## Repetitori u HR
- RepeaterBook: https://www.repeaterbook.com/repeaters/index.php/Croatia
- HRS lista: https://www.hamradio.hr/  
- Primjeri popularnih HR repetitora (Zagreb, Split, Rijeka)

## Etiketa na repetitoru
- Identificiraj se kratko: barem jednom na 10 min i na kraju veze
- Pauziraj između prijenosa: 30-60 sekundi — hitni pozivi imaju prioritet!
  !!! warning "Bez pauze = blokirate hitne komunikacije!"
- Lokalni razgovor: ne blokiraj repetitor satima

## Procedura veze (step by step)
1. Programiraj radio: Rx frekvencija (=output rep.), Offset, CTCSS ton
2. Provjeri: čujemo li repetitor (otvaranje squelcha s tonom)
3. Pritisni PTT, identificiraj se: "9A1ZG slušam" ili "9A1ZG monitoring"
4. Odgovori ako netko zove ili zovi CQ
5. Završi: "9A1ZG clear" ili "9A1ZG, 73"

KORAK 4 — Tehničke smjernice:
- Tablice za offset, CTCSS, digitalne sustave
- Code blokovi za procedure kad je prikladno
- Admonitions: minimalno 3
- Interni linkovi: modes.md, bandplans.md, first_qso.md

KORAK 5 — Spremi u docs/operating/repeaters.md (nova datoteka)
KORAK 6 — Dodaj u mkdocs.yml nav → Rad na opsegu:
  - Repetitori: operating/repeaters.md
KORAK 7 — Kreiraj stub docs/operating/repeaters.en.md
```

---

## Bilješke o napretku

- 
