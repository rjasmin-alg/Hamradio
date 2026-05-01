# Tvoja prva veza (First QSO)

Dobili ste dozvolu, kupili transciiver, postavili antenu — a onda... mikrofon. I tišina. Ovo je "mic fright" (strah od mikrofona) koji doživljava gotovo svaki početnički radioamater. Normalno je, i ovaj vodič će vam pomoći da prekoračite taj prag.

!!! tip "Važna istina"
    Svaki iskusni operator na opsegu bio je jednom tamo gdje ste vi sada. Svi su imali prvu vezu. Nitko vas neće kritizirati za početnički QSO — radioamaterska zajednica je gostoljubiva prema novim operatorima.

---

## Priprema — provjera stanice

Prije prve veze, provjerite sve s ovom listom:

### Hardver

- [ ] **Antena spojena** i SWR izmjeren (ispod 2:1)
- [ ] **Mikrofon priključen** i prepoznat od strane radija
- [ ] **PTT gumb radi** (pritisnite i slušajte — čujete li ton sidetone ili ALC pomak?)
- [ ] **Snaga podešena** na 10–25 W za prvu vezu
- [ ] **Transciiver na USB** (za 40 m: 7.050–7.200 MHz, za 80 m: 3.600–3.800 MHz)
- [ ] **Headset ili zvučnik** — čujete li opseg?

### Softver / logbook

- [ ] **Logbook spreman** — barem papir i olovka s callsign, datum, frekvencija
- [ ] **Ham2K**, **LoTW** ili **QRZ logbook** ako koristite digitalni log

---

## Opcija 1: Repetitorski QSO (Najlakši start)

Repetitor je idealan za prvu vezu jer:
*   Ne treba odlazni DX signal
*   Uvijek ima netko tko sluša
*   Greške su prihvatljive i kolege će vam pomoći

### Korak 1: Pronađite lokalni repetitor

Koristite RepeaterBook app ili pitajte u vašem radioklub. Unesite:
*   Output frekvenciju (npr. 145.800 MHz)
*   Offset: −600 kHz
*   CTCSS ton (npr. 88.5 Hz)

### Korak 2: Unesite u radio i provjerite prijem

Podesite radio, slušajte. Čujete li aktivnost? Dobro. Aktivni repetitor znači da radi.

### Korak 3: Kratki check-in

Pritisnite PTT i kratko recite:
```
"[Vaš callsign] is listening" ili
"9A1ABC, checking in."
```

Ako netko sluša i odgovori — imate prvu vezu! Razgovarajte normalno.

Ako nema odgovora — normalno, pokušajte u večernjim satima kad je aktivnost veća.

---

## Opcija 2: Club Net

Mnogi radioklubovi imaju redovne "net" sesije — sastanak na opsegu u određeno vrijeme.

*   Pratite HRS glasnik za termine neta
*   Pridružite se skupini — Net Control (NC) vodi sesiju
*   Kad dođe red na vas: `"9A1ABC, checking in, ovo je [ime], [lokacija]."`

Net je izvrsna praksa jer imate strukturu i voditelja koji kontrolira tko govori.

---

## Opcija 3: Odgovoriti na CQ (Reagiranje na poziv)

Ovo je klasičan scenarij — čujete nekoga tko zove CQ i odgovorite.

### Korak 1: Slušajte

Podesite na aktivni opseg (20 m: 14.150–14.350 MHz USB) i slušajte. Čut ćete CQ pozive.

### Korak 2: Odaberite prikladni CQ

Počnite s jakim, razumljivim signalom (S7 ili bolje). DX veze ostavite za later.

### Korak 3: Odgovorite jednostavno

Kad stanete s pritiskom PTT-a, odmah pritisnite i recite **samo vaš callsign**:
```
"9A1ABC"
```

Nemojte dodavati ništa — stanite i čekajte. Ako vas ne čuje, pokušajte opet.

### Korak 4: Kad vas pozvana stanica odgovori

```
"9A1ABC, ovdje DL1BBB, dobar dan, tvoj signal je 58."
```

Vi odgovarate:
```
"DL1BBB, ovdje 9A1ABC, dobar dan Hansu! Tvoj signal je 57.
Moje ime je Ivan, lokacija je Zagreb. 9A1ABC K."
```

### Korak 5: Kratki QSO

Razmijenite:
*   Ime (name)
*   Lokaciju (QTH) ili lokator (grid)
*   RST raport
*   Opcijsko: antenu, opremu, vremenske uvjete

### Korak 6: Završite vezu

```
"Hvala na lijepom QSO, Hansu. 73 i čujemo se. DL1BBB de 9A1ABC SK."
```

---

## Opcija 4: Zovite vlastiti CQ

Kada se osjećate samouzdano:

### Provjera frekvencije

```
"QRL? Jeste li zauzeti?" (ili na engleskom: "Is the frequency in use?")
```

Pričekajte 5–10 sekundi.

### CQ poziv

```
"CQ CQ CQ, ovo je 9A1ABC, 9A1ABC, 9A1ABC, zovim i slušam. K."
```

Na engleskom:
```
"CQ CQ CQ, this is 9A1ABC, Nine Alpha 1 Alpha Bravo Charlie, calling CQ and listening."
```

Pričekajte 10–15 sekundi. Ako nema odgovora, ponovite. Ako nema odgovora ni nakon 3–5 pokušaja, promijenite frekvenciju.

!!! tip "Kada zvati CQ?"
    HF popularni aktivni sati su:
    - 40 m: večer 18:00–23:00 UTC
    - 20 m: cijeli dan (08:00–20:00 UTC)
    - 80 m: večer i noć (18:00–06:00 UTC)

---

## Česti scenariji i kako reagirati

### "Ne razumijem što govori sugovornik"

*   Recite: `"QRS PSE"` — zamolite ih da govore sporije
*   Ili: `"Could you repeat please? QRM here."` — QRM = smetnje

### "Napravili ste grešku u callsignu"

Bez panike — ispravite mirno:
```
"Opravka — moj callsign je 9 Alpha 1 Alpha Bravo Charlie, 9A1ABC."
```

### "Ne znate odgovor na pitanje koje vam postavljaju"

```
"Bojim se da to ne znam, ali ću provjeriti. Hvala na pitanju!"
```

### "Netko vas prekida mid-QSO"

Ignorirajte i nastavite s partnerom. Ako je previše QRM:
```
"QSY — prijedlažem da se preselimo na [frekvencija]. K."
```

### "Drugi vas zovu dok razgovarate"

Na kraju svog prijenosa:
```
"K, i pozivam 9A2DEF i sve ostale koji čekaju."
```

---

## Checklist za prvu vezu

### Tehničko

- [ ] SWR < 2:1 na planiranoj frekvenciji
- [ ] Mikrofon radi — testni govor producira ALC pokret na metru
- [ ] Slušate/čujete signal na opsegu (ne samo šum)
- [ ] Radio identificira mic input (NE line in!)
- [ ] Znate lokator vašeg QTH: `JN___`

### Operativno

- [ ] Znate vaš callsign napamet (phonetički: 9 Alpha 1 Alpha Bravo Charlie)
- [ ] Znate osnove RST sustava (59 = odlično)
- [ ] Imate biljeznicu/logbook spreman
- [ ] Znate Q-kodove: QRL, QSY, QSL, QTH
- [ ] Znate kako završiti vezu: "73, SK"

### Mentalni

- [ ] Prihvaćate da ćete griješiti — normalno je
- [ ] Zamolili ste Elmera da bude prisutan ili dostupan telefonom
- [ ] Počinjete s lakim scenarijem (repetitor ili odgovor na CQ, ne vlastiti CQ DX)

---

## Transkripti za vježbu

Naučite ove fraze napamet — bit će vam baza za improvizaciju:

**Kratki QSO na engleskom (najčešći jezik na HF):**
```
"[Callsign of who called you], this is [your callsign].
Good [morning/afternoon/evening].
Your signal is [RS rapport], [RS].
My name is [name], my QTH is [city], Croatia.
Antenna is a [antenna type].
[Your callsign], over."
```

**Odgovor drugoj strani:**
```
"Thank you [name]. Your signal is also [RS rapport].
This is [your callsign].
[73 / Best regards and] [see you again / cheers].
[Their callsign] de [your callsign] SK."
```

---

## Nakon prve veze

1.  **Zapišite u logbook**: Datum, UTC, frekvencija, callsign, rapport, ime, QTH
2.  **eQSL ili LoTW**: Pošaljite digitalne QSL kartice za potvrdu veze
3.  **DXCC lookup**: Provjerite je li sugovornik iz zanimljive DXCC entitete
4.  **Pohvalite sebe**: Uspjeli ste! Svaki sljedeći QSO bit će lakši.

---

## Resursi i podrška

*   [**Phonetska abeceda**](../resources/phonetic_alphabet.md) — Naučite sva slova
*   [**Q-kodovi i prosignali**](procedures.md) — Sve što trebate znati
*   [**Vaš lokalni radioklub**](https://www.hamradio.hr/) — Elmer koji će vam pomoći
*   [**HRS forum**](https://www.hamradio.hr/) — Pitajte na forumu, zajednica je prijateljska

---

## Povezane teme

*   [Procedure veze](procedures.md) — Kompletni QSO vodič
*   [Modovi rada](modes.md) — Koji mod za prvu vezu
*   [Frekvencijski planovi](bandplans.md) — Gdje zvati CQ
*   [Radioamaterska etika](../regulations/ethics.md) — Ponašanje na opsegu
