# 🔨 Razrada Modula — Zadaci za Agente

> **VAŽNO:** Ovaj dokument sadrži **detaljan opis zadataka** za svaki modul.
> Agent koji radi na modulu mora:
> 1. Pročitati `01_VIZIJA_I_STANDARDI.md` za format i ton
> 2. Pronaći svoj modul u `02_MAPA_MODULA.md` za kontekst i ovisnosti
> 3. Pratiti upute u ovom dokumentu za sadržaj

---

## Kako koristiti ovaj dokument

### Workflow za agenta
```
1. Odaberi modul iz popisa (ili dobij zadatak od korisnika)
2. Pročitaj postojeći .md fajl (ako postoji)
3. Istraži temu koristeći web search
4. Napiši/proširi sadržaj prema specificiranom predlošku
5. Provjeri checklist kvalitete iz 01_VIZIJA_I_STANDARDI.md
6. Spremi rezultat u docs/ direktorij
7. Ažuriraj mkdocs.yml ako je nova stranica
```

### Prompt template za agenta
Svaki modul ispod sadrži **prompt template** — predložak koji se može direktno koristiti kao zadatak za agenta. Template pretpostavlja da agent ima pristup:
- Web searchu (za istraživanje)
- Filesystemu (za čitanje/pisanje MkDocs sadržaja)
- Viziji i standardima (`01_VIZIJA_I_STANDARDI.md`)

---

# VAL 1: Proširenje postojećih P1 modula

> Ovi moduli **već postoje** ali su plitki (500–4000 bajtova). Cilj je proširiti ih na minimalno 1500 riječi kvalitetnog sadržaja.

---

## REG-02: Kako postati radioamater (`regulations/exams.md`)

### Trenutno stanje
~1750 bajtova, pokriva osnovne korake ali bez detalja.

### Što treba dodati
1. Detaljan opis ispitne procedure u Hrvatskoj — gdje se prijavljuje, cijena, termini, trajanje, prolaznost
2. Ispitne teme po razredima (A, B, N razred)
3. Praktični savjeti za učenje — knjige, online resursi, vremenski plan
4. Usporedba s drugim zemljama (tabbed: HR, USA, UK, DE)
5. FAQ sekcija — najčešća pitanja novih kandidata

### Prompt template
```
Proširi stranicu docs/regulations/exams.md u MkDocs priručniku za radioamatere.
Stranica trenutno ima ~1750 bajtova i pokriva samo osnove.

Zadatak:
1. Pročitaj postojeći sadržaj datoteke
2. Istraži web za: "kako postati radioamater u Hrvatskoj", "HAKOM radioamaterski ispit",
   "HRS ispit za radioamatere", "ham radio exam Croatia"
3. Proširi sadržaj na minimalno 1500 riječi pokrivajući:
   - Detaljan proces prijave i polaganja ispita u HR
   - Razredi dozvola (A, B, N) i njihove privilegije
   - Ispitne teme i gradivo po kategorijama
   - Praktični savjeti za pripremu (vremenski plan, resursi)
   - Usporedba s USA/UK/DE korištenjem MkDocs tabbed formata
   - FAQ sekcija
4. Koristi MkDocs admonitions (tip, warning, note, example) — minimalno 3
5. Dodaj interne linkove na barem 3 druge stranice priručnika
6. Jezik: Hrvatski, tehnički termini na HR s engleskim u zagradi
7. Spremi rezultat u docs/regulations/exams.md
```

---

## REG-03: Hrvatski propisi (`regulations/croatian_regs.md`)

### Trenutno stanje
~1200 bajtova, samo lista dokumenata i linkovi.

### Što treba dodati
1. Detaljni sažetak Pravilnika o amaterskim radijskim komunikacijama — razredi, frekvencije, snage, pozivne oznake, obveze
2. Uloga HAKOM-a i HRS-a — detaljno
3. Tablica: Razred → Frekvencije → Snaga → Modovi
4. Kronologija važnih izmjena propisa

### Prompt template
```
Proširi stranicu docs/regulations/croatian_regs.md.
Trenutno ima samo ~1200 bajtova s linkovima na zakone.

Zadatak:
1. Istraži web za: "Pravilnik o amaterskim radijskim komunikacijama Hrvatska",
   "HAKOM radioamaterske dozvole", "NN pravilnik radioamateri",
   "hrvatski radioamaterski propisi"
2. Napravi detaljan sažetak s tablicama:
   - Razredi dozvola i tko može polagati
   - Frekvencije po razredima (tablica: Razred | Band | Frekvencije | Max snaga)
   - Pravila za pozivne oznake
   - Obveze operatora (dnevnik, identifikacija, itd.)
3. Dodaj kronologiju važnih promjena propisa
4. Koristi MkDocs admonitions i tablice
5. Minimalno 1500 riječi
6. Spremi u docs/regulations/croatian_regs.md
```

---

## TEC-02: Osnove elektronike (`technical/electronics.md`)

### Trenutno stanje
~3900 bajtova. Pokriva osnovne komponente i Ohmov zakon. Dobar početak ali treba puno više.

### Što treba dodati
1. Serijski i paralelni spoj (otpornici, kondenzatori) + formule
2. AC vs DC — izmjenična i istosmjerna struja, frekvencija, period
3. Impedancija — ključni koncept za radioamatere
4. Rezonantni (titrajni) krug — LC krug, rezonantna frekvencija
5. Transformatori — princip rada, primjena
6. Više o poluvodičima — LED, Zener dioda, MOSFET
7. Čitanje shema — simboli, standardi (tablica)
8. Više praktičnih primjera — izračun otpornika za LED, dijelilo napona
9. Boja kodova otpornika

### Prompt template
```
Proširi stranicu docs/technical/electronics.md.
Trenutno ima ~3900 bajtova i pokriva samo osnovne komponente i Ohmov zakon.

Zadatak:
1. Zadrži sav postojeći sadržaj, dodaj nove sekcije ISPOD postojećih
2. Dodaj sekcije za:
   - Serijski/paralelni spoj (formule s MathJax)
   - AC vs DC, frekvencija, period, amplituda
   - Impedancija (Z = R + jX) — objasniti jednostavno za radioamatere
   - LC titrajni krug: f = 1/(2π√(LC))
   - Transformatori
   - Čitanje shema (simboli tablica)
   - Praktični primjeri (izračun otpornika za LED, dijelilo napona)
3. Koristi MathJax za sve formule
4. Koristi admonitions (example, tip, warning)
5. Linkaj na Falstad simulator za interaktivne primjere
6. Minimalno 2500 riječi ukupno
7. Spremi u docs/technical/electronics.md
```

---

## TEC-03: Antene i vodovi (`technical/antennas.md`)

### Trenutno stanje
~2570 bajtova. Pokriva dipol, Yagi, GP i koaksijalni kabel. Vrlo kratko.

### Što treba dodati
1. Teorija antena — kako antena zrači, polarizacija, dijagram zračenja
2. Dobitak antene (Gain) — dBi vs dBd, što znači u praksi
3. Impedancija antene — 50Ω standard, prilagodba
4. Više vrsta antena — End-Fed, Loop, Quad, J-Pole, Slim Jim, Log-Periodic
5. Balonski transformatori (Balun/Unun) — što su, zašto trebaju
6. Koaksijalni kabel detaljno — LMR-400, gubici po frekvenciji (tablica)
7. Dvožilni vod (Ladder Line) — prednosti za multiband antene
8. Praktični savjeti — postavljanje antene, sigurnost, radijali

### Prompt template
```
Proširi stranicu docs/technical/antennas.md.
Pokriva samo 3 vrste antena i osnove koaksijalnog kabela (~2570 bajtova).

Zadatak:
1. Zadrži postojeći sadržaj, proširi svaku sekciju i dodaj nove
2. Dodaj teoriju: dijagram zračenja, polarizacija, dobitak (dBi/dBd) s formulama
3. Dodaj nove antene: End-Fed, multiband dipol, Loop, Quad, J-Pole, Log-Periodic
4. Proširi vodove: LMR-400, gubici tablica, Ladder Line, Balun/Unun
5. Dodaj praktične savjete za postavljanje antena
6. Koristi MathJax za formule (duljina dipola, rezonantna frekvencija)
7. Minimum 2500 riječi ukupno
8. Spremi u docs/technical/antennas.md
```

---

## TEC-06: Sigurnost (`technical/safety.md`)

### Trenutno stanje
~980 bajtova. Tri kratke sekcije. Kritično važna tema treba PUNO više sadržaja.

### Što treba dodati
1. RF sigurnost detaljno — PEM proračuni, ICNIRP smjernice, sigurne udaljenosti (tablica)
2. Električna sigurnost detaljno — visoki naponi u PA, kondenzatori ubijaju!
3. Zaštita od groma detaljno — odvodnici, sustav uzemljenja, Lightning arrestor
4. Sigurnost pri radu na antenama — rad na visini, blizina dalekovoda
5. Prva pomoć — što napraviti kod strujnog udara
6. EMF izračuni — praktični primjeri za uobičajene snage i antene

### Prompt template
```
Proširi stranicu docs/technical/safety.md.
Kritično važna tema ali ima samo ~980 bajtova.

Zadatak:
1. Proširi na minimalno 2000 riječi — ovo je stranica koja može spasiti život!
2. Dodaj:
   - RF sigurnost: ICNIRP smjernice, sigurne udaljenosti (tablica po snagama)
   - Električna sigurnost: opasnosti visokog napona u PA/PSU, kondenzatori
   - Zaštita od groma: sustav uzemljenja, odvodnici, praktični dijagrami
   - Sigurnost antena: rad na visini, blizina dalekovoda
   - Prva pomoć kod strujnog udara
3. Koristi DANGER i WARNING admonitions obilato!
4. Linkaj na relevantne vanjske izvore (ARRL safety, ICNIRP)
5. Spremi u docs/technical/safety.md
```

---

## OPR-02: Frekvencijski planovi (`operating/bandplans.md`)

### Trenutno stanje
~2262 bajtova. Pokriva 160m, 80m, 40m, 20m, 2m, 70cm. Nedostaju mnogi opsezi.

### Što treba dodati
1. Svi HF opsezi — 60m, 30m (WARC), 17m (WARC), 15m, 12m (WARC), 10m
2. 6m (50 MHz) — "Magic Band"
3. 23cm (1296 MHz) i kratki pregled mikrovalnih opsega
4. Za svaki opseg: tipična propagacija, tipične aktivnosti
5. Beacon frekvencije i DX prozori
6. Linkovi na službene IARU bandplan dokumente

### Prompt template
```
Proširi stranicu docs/operating/bandplans.md.
Nedostaju opsezi: 60m, 30m, 17m, 15m, 12m, 10m, 6m, 23cm.

Zadatak:
1. Dodaj SVE radioamaterske HF opsege koji nedostaju s tablicama (EU vs USA)
2. Dodaj 6m (50 MHz) "Magic Band" s naglaskom na sporadic-E
3. Dodaj 23cm i kratki pregled mikrovalnih opsega
4. Za svaki opseg: karakteristike propagacije, tipične aktivnosti
5. Dodaj beacon frekvencije i DX prozore
6. Linkaj na službene IARU bandplan dokumente
7. Spremi u docs/operating/bandplans.md
```

---

## OPR-03: Modovi rada (`operating/modes.md`)

### Trenutno stanje
~2258 bajtova. Pokriva CW, SSB, FM i FT8 kratko.

### Što treba dodati
1. Svaki mod proširiti — kako točno radi modulacija (jednostavno)
2. AM — zrakoplovni opseg, WAM
3. Digitalni modovi detaljno — FT4, JS8Call, PSK31, WSPR, Olivia
4. Video modovi — ATV, DATV (kratko)
5. Usporedba modova (tablica: Mod | Širina pojasa | Domet | Složenost | Popularnost)
6. Softver za digitalne modove — WSJT-X, fldigi, etc.
7. Dijagram odluke — koji mod za koju situaciju

### Prompt template
```
Proširi stranicu docs/operating/modes.md.
Pokriva samo 4 moda u ~2258 bajtova.

Zadatak:
1. Proširi postojeće modove s tehničkim detaljima modulacije (jednostavno objašnjeno)
2. Dodaj: AM, FT4, JS8Call, PSK31, WSPR, Olivia, ATV/DATV
3. Napravi usporednu tablicu svih modova
4. Dodaj sekciju o softveru za digitalne modove
5. Dodaj "dijagram odluke" — koji mod za koju situaciju
6. Minimum 2500 riječi
7. Spremi u docs/operating/modes.md
```

---

## OPR-04: Procedura veze (`operating/procedures.md`)

### Trenutno stanje
~4451 bajtova — najopsežnija postojeća stranica. Može još rasti.

### Što treba dodati
1. Detaljniji primjeri QSO-a — SSB i CW transkripti u code blokovima
2. Procedura za repetitore — CTCSS, ponašanje, pristojnost
3. Pile-up procedura — kako se ponašati kao lovac i kao DX
4. Net procedure — kontrolna stanica, check-in, discipline
5. Procedura za natjecanja — exchange, serijski broj, brzi QSO
6. Fonetska abeceda — kompletna NATO tablica
7. Ponašanje na opsegu — etiketa, česte greške početnika

### Prompt template
```
Proširi stranicu docs/operating/procedures.md.
Već ima ~4451 bajtova ali može se značajno proširiti.

Zadatak:
1. Zadrži sav postojeći sadržaj
2. Dodaj detaljne primjere QSO-a (SSB i CW transkripti u code blokovima)
3. Dodaj proceduru za repetitore, pile-up, net, contest
4. Dodaj kompletnu NATO fonetsku abecedu (tablica)
5. Proširi Q-kodove s primjerima korištenja u rečenicama
6. Dodaj sekciju o etiketi i čestim greškama
7. Minimum 3000 riječi ukupno
8. Spremi u docs/operating/procedures.md
```

---

## ACT-02: Natjecanja (`activities/contesting.md`)

### Trenutno stanje
~836 bajtova. Kratki pregled.

### Što treba dodati
1. Kako početi s natjecanjima — step by step za početnike
2. Detaljniji kalendar — sva važna natjecanja kroz godinu (tablica)
3. Kategorije detaljno — Single OP, Multi OP, QRP, Assisted, Overlay
4. Softver za natjecanja — N1MM+, DXLog (usporedba, tabbed)
5. Strategija — rate vs multiplier, band strategy
6. Bodovanje — primjeri za diferentes natjecanja
7. Cabrillo format i slanje logova

### Prompt template
```
Proširi stranicu docs/activities/contesting.md.
Samo ~836 bajtova, površan pregled.

Zadatak:
1. Proširi na detaljan vodič za natjecanja (min 2000 riječi)
2. Dodaj: kako početi, detaljni kalendar (tablica), kategorije, softver, strategija
3. Objasni bodovanje na primjerima (CQ WW, ARRL DX, 9A CW)
4. Dodaj Cabrillo format i slanje logova
5. Koristi tabbed format za usporedbu N1MM+ i DXLog
6. Spremi u docs/activities/contesting.md
```

---

## ACT-04: Rad u pokretu (`activities/portable.md`)

### Trenutno stanje
~971 bajtova. Kratko o SOTA, POTA, IOTA.

### Što treba dodati
1. SOTA detaljno — pravila, bodovanje, HR vrhovi, alerts/spots
2. POTA detaljno — registracija, HR parkovi, pravila
3. IOTA detaljno — HR otoci, ekspedicije, Palagruža
4. Oprema detaljno — usporedna tablica QRP uređaja (FT-818, KX2, IC-705, TR-USDX)
5. Antene za portable — End-fed, linked dipol, vertikalka na štapu
6. Baterije — LiFePO4, Solar, kapaciteti i trajanje
7. Checklist za aktivaciju
8. Safety outdoor — grom na vrhu, vremenska nepogoda

### Prompt template
```
Proširi stranicu docs/activities/portable.md.
Samo ~971 bajtova, kratko o SOTA/POTA/IOTA.

Zadatak:
1. Za svaki program (SOTA, POTA, IOTA) dodaj:
   - Detaljna pravila, bodovanje, kategorije
   - HR specifičnosti (vrhovi, parkovi, otoci)
   - Registracija i kako početi
2. Oprema: usporedna tablica QRP uređaja (FT-818, KX2, IC-705, TR-USDX)
3. Antene za portable: End-fed, dipol na štapu, linked dipol
4. Baterije: usporedba tipa, kapaciteta, trajanja
5. Checklist za aktivaciju
6. Minimum 2500 riječi
7. Spremi u docs/activities/portable.md
```

---

# VAL 2: Novi P1 moduli (ne postoje)

> Ovi moduli su **kritični za kompletnost** priručnika ali još ne postoje.

---

## TEC-08: Propagacija radio valova (`technical/propagation.md`)

### Sadržaj koji treba pokriti
1. Što je propagacija — kako se radio valovi šire prostorom
2. Ionosfera — D, E, F1, F2 slojevi, ionizacija, refleksija
3. Zemni val — za niže frekvencije, lokalne veze
4. Ionosferski val — "skip", kritična frekvencija, MUF, LUF
5. HF propagacija po opsezima (tablica: Opseg | Dnevna/Noćna | Tipični domet)
6. Sunčev ciklus — SC25, SFI, K-indeks, A-indeks — što znače u praksi
7. VHF/UHF propagacija — tropo, sporadic-E, meteor scatter, aurora, EME
8. Gray Line — posebni uvjeti na prijelazu dan/noć
9. Alati — VOACAP, DXMaps, PSKReporter, SolarHam
10. Praktični savjeti — kad otvoriti koji opseg

### Prompt template
```
Kreiraj novu stranicu docs/technical/propagation.md za MkDocs priručnik.

Sadržaj mora pokrivati:
1. Teorija propagacije radio valova (zemni val, ionosferski val, line-of-sight)
2. Ionosfera detaljno: slojevi D/E/F1/F2, ionizacija, kritična frekvencija
3. MUF i LUF — kako ih odrediti i koristiti
4. HF propagacija po opsezima: tablica "Opseg | Dnevna/Noćna | Tipični domet"
5. Sunčev ciklus: SC25, SFI, K-indeks, A-indeks — što znače za amatere
6. VHF propagacija: tropo, sporadic-E, meteor scatter, EME, aurora
7. Gray Line propagacija i iskoristvanje
8. Alati za praćenje: VOACAP, PSKReporter, DXMaps, SolarHam
9. Praktični savjeti za optimalno korištenje uvjeta

Format: MkDocs Material s admonitions, MathJax formulama, tablicama.
Jezik: Hrvatski s engleskim terminima u zagradama.
Minimum 3000 riječi.
Dodaj interlinkove na: antennas.md, bandplans.md, dxing.md, modes.md
Ažurirati mkdocs.yml nav sekciju!
Spremi u docs/technical/propagation.md
```

---

## TEC-15: Modulacija i demodulacija (`technical/modulation.md`)

### Sadržaj koji treba pokriti
1. Zašto moduliramo — nosioce i modulirajući signal
2. AM — princip, matematika, spektar (bočni pojasovi)
3. FM — princip, deviacija, Carson's rule
4. SSB — zašto je efikasnija, filter/phasing metoda
5. CW — OOK (On-Off Keying), zašto ima best domet
6. Digitalna modulacija — FSK, PSK, AFSK, QAM (osnove za razumijevanje FT8/WSPR)
7. Usporedna tablica — svi modovi, širina pojasa, SNR prednosti

### Prompt template
```
Kreiraj novu stranicu docs/technical/modulation.md.

Objasni teoriju modulacije i demodulacije za radioamatere:
1. Zašto moduliramo: nosioc i modulirajući signal — vizualna analogija
2. AM: princip i matematika s MathJax, bočni pojasovi, spektar
3. FM: princip, deviacija, Carson's rule
4. SSB: zašto je efikasnija, kako funkcionira filter/phasing metoda
5. CW: OOK, zašto prolazi gdje ništa drugo ne može
6. Digitalna modulacija: FSK, PSK, QAM — osnove za razumijevanje FT8/WSPR
7. Usporedna tablica svih modulacija (Mod | Širina pojasa | SNR prednost | Tipična primjena)

Format: MkDocs, MathJax formule, admonitions, tablice
Minimum 2000 riječi. Hrvatski jezik.
Ažurirati mkdocs.yml!
Spremi u docs/technical/modulation.md
```

---

## TEC-20: Uzemljenje i zaštita od groma (`technical/grounding.md`)

### Sadržaj koji treba pokriti
1. Vrste uzemljenja — RF uzemljenje vs sigurnosno vs gromobransko
2. Kako napraviti RF uzemljenje — radijali, ground rod, counterpoise
3. Sustav zaštite od groma — single point ground, odvodnici, uzemljivači
4. Praktični dijagrami — sustav uzemljenja kućne stanice
5. Česte greške — ground loop, loše veze, nespojeni ekrani

### Prompt template
```
Kreiraj novu stranicu docs/technical/grounding.md.

Objasni uzemljenje i zaštitu od groma za radioamatere:
1. Razlika između RF, sigurnosnog i gromobranskog uzemljenja
2. Kako napraviti RF uzemljenje: radijali, counterpoise, ground rod
3. Sustav zaštite od groma: single point ground, odvodnici
4. Praktični dijagrami sustava uzemljenja kućne stanice
5. Česte greške i kako ih izbjeći

Format: MkDocs, DANGER admonitions za opasnosti
Minimum 2000 riječi. Hrvatski jezik.
Ažurirati mkdocs.yml!
Spremi u docs/technical/grounding.md
```

---

## OPR-06: FT8 praktični vodič (`operating/ft8_guide.md`)

### Sadržaj koji treba pokriti
1. Što je FT8 — nastanak, Joe Taylor K1JT/Steve Franke K9AN
2. Kako radi — 15s intervali, 8-FSK, SNR do -24dB
3. Oprema — radio + računalo + kabel, zvučna kartica ili CAT
4. Instalacija WSJT-X — step by step Windows
5. Konfiguracija — CAT control, audio, PTT
6. Prva FT8 veza — korak po korak (waterfall, odabir signala, CQ, QSO)
7. Decode i waterfall — čitanje zaslona, boje, kolone
8. FT8 etiketa — ne koristiti previše snage, ne koristiti Auto Seq bez nadzora
9. Logiranje i upload — LoTW, ClubLog, PSKReporter
10. Troubleshooting — česti problemi (audio, timing, CAT)

### Prompt template
```
Kreiraj novu stranicu docs/operating/ft8_guide.md.

Napiši kompletni praktični vodič za FT8:
1. Uvod: što je FT8, tko ga je napravio, zašto je revolucionaran
2. Teorija: 15-sekundni intervali, 8-FSK, SNR do -24dB
3. Potrebna oprema: kompletna lista s preporukama
4. Instalacija WSJT-X: step-by-step za Windows
5. Konfiguracija: CAT, Audio, PTT — svaki korak objašnjen
6. Tvoja prva veza: step-by-step walkthrough
7. Decode prozor i waterfall: što sve znače boje i kolone
8. Etiketa: koristiti razumnu snagu, ne koristiti Auto Seq bez nadzora
9. Logiranje: LoTW, ClubLog, PSKReporter
10. FAQ i troubleshooting

Format: MkDocs, admonitions (tip, warning), code blokovi za primjere
Minimum 3000 riječi. Hrvatski jezik.
Ažurirati mkdocs.yml!
Spremi u docs/operating/ft8_guide.md
```

---

## OPR-07: Učenje CW (`operating/cw_learning.md`)

### Sadržaj koji treba pokriti
1. Zašto naučiti CW — prednosti, domet, jednostavnost opreme
2. Koch metoda — najučinkovitija metoda učenja
3. Online resursi — LCWO, MorseCode.World, Just Learn Morse Code
4. Preporučeni redoslijed znakova
5. Taster (Key) — vrste (paddle, straight key, bug), što za početak
6. Od slova do QSO-a — razine napretka, koliko WPM za što
7. Skraćenice i prosign — kompletna lista
8. Softveri za vježbu — DXLab, CW Freak, MacLoggerDX

### Prompt template
```
Kreiraj novu stranicu docs/operating/cw_learning.md.

Napiši kompletan vodič za učenje Morseovog koda:
1. Zašto naučiti CW: prednosti (domet, jednostavnost, tradicija)
2. Koch metoda: kako funkcionira, zašto je najučinkovitija
3. Online resursi: LCWO, MorseCode.World, preporučeni tečajevi
4. Preporučeni redoslijed učenja znakova
5. Taster: paddle vs straight key vs bug — što za početnika
6. Razine napretka: 5 WPM (osnova), 12 WPM (CEPT), 20+ WPM (tekuće)
7. Skraćenice i prosignali (kompletna tablica)
8. Softveri za vježbu (usporedba tablicom)

Format: MkDocs, tablice, admonitions (tip, example)
Minimum 2000 riječi. Hrvatski jezik.
Ažurirati mkdocs.yml!
Spremi u docs/operating/cw_learning.md
```

---

## OPR-13: Tvoja prva veza (`operating/first_qso.md`)

### Sadržaj koji treba pokriti
1. Priprema — checklist (dozvola, pozivna, radio, antena, dnevnik)
2. Tjedan slušanja — što slušati, kako prepoznati QSO strukturu
3. Prva veza na repetitoru — najlakši put, step by step
4. Odgovaranje na CQ na HF-u
5. Pozivanje CQ
6. Kompletni transkripti — SSB primjer u code bloku
7. Česte greške i kako ih izbjeći
8. "Strah od mikrofona" — savjeti za prevladavanje

### Prompt template
```
Kreiraj novu stranicu docs/operating/first_qso.md.

Napiši vodič za potpunog početnika koji radi svoju prvu vezu:
1. Što trebate prije prvog QSO-a (checklist)
2. Slušanje tjedan dana: kako naučiti promatrajući
3. Prva veza na repetitoru: step-by-step (najlakši način za početi)
4. Prva HF veza: odgovaranje na CQ (uz primjer)
5. Pozivanje CQ: kako i kad
6. Kompletni transkripti (SSB primjer u code bloku, annotiran)
7. Česte greške početnika i kako ih izbjeći
8. Savjeti za prevladavanje "straha od mikrofona"

Ton: ohrabrujući, prijateljski, "svi smo bili početnici"
Format: MkDocs, admonitions, primjeri u code blokovima
Minimum 2000 riječi. Hrvatski jezik.
Ažurirati mkdocs.yml!
Spremi u docs/operating/first_qso.md
```

---

## OPR-08: Repetitori (`operating/repeaters.md`)

### Sadržaj koji treba pokriti
1. Što je repetitor — pojačivač dometa za VHF/UHF
2. Offset — ulazna i izlazna frekvencija, standardni offseti za 2m i 70cm
3. CTCSS i DCS — što su tonovi, zašto se koriste, tablica standardnih tonova
4. Digitalni repetitori — EchoLink, IRLP, Allstar, D-STAR, DMR
5. Repetitori u HR — kako ih pronaći (RepeaterBook, HRS lista)
6. Etiketa na repetitoru — ponašanje, identificiranje, pauze
7. Veza kroz repetitor — step by step za početnika

### Prompt template
```
Kreiraj novu stranicu docs/operating/repeaters.md.

Comprehensive vodič za repetitore (releje):
1. Što je repetitor: princip rada, zašto povećava domet
2. Offset: ulaz/izlaz, standardni offseti za 2m (-600 kHz) i 70cm (-7.6 MHz) — tablica
3. CTCSS i DCS: što su, tablica standardnih tonova, kako programirati u radio
4. Digitalni repetitori: EchoLink, IRLP, Allstar, D-STAR, DMR — kratki pregled svakog
5. Repetitori u HR: kako ih pronaći (linkovi)
6. Etiketa: ponašanje, identificiranje, pauze za hitne pozive
7. Veza kroz repetitor: step by step

Format: MkDocs, tablice, admonitions
Minimum 2000 riječi. Hrvatski jezik.
Ažurirati mkdocs.yml!
Spremi u docs/operating/repeaters.md
```

---

## REG-06: Razredi dozvola (`regulations/license_classes.md`)

### Sadržaj koji treba pokriti
1. Hrvatski razredi — A (CEPT), B, N — tko smije što
2. CEPT sustav — T/R 61-01, CEPT Novice Licence
3. Usporedba — HR vs USA (Technician/General/Extra) vs UK (Foundation/Intermediate/Full) [tabbed]
4. Tablica privilegija — Razred | HF | VHF/UHF | Snaga | Modovi
5. Napredovanje — kako prijeći iz nižeg u viši razred

### Prompt template
```
Kreiraj novu stranicu docs/regulations/license_classes.md.

Detaljno objasni razrede radioamaterskih dozvola:
1. Hrvatski sustav: razredi A, B, N — tko, što, kako
2. CEPT sustav: T/R 61-01, CEPT Novice Licence — što smiješ u inozemstvu
3. Usporedba s USA i UK (tabbed format)
4. Tablica privilegija: Razred | HF | VHF/UHF | Max snaga | Modovi
5. Kako napredovati iz jednog razreda u viši

Format: MkDocs, tablice, tabbed sadržaj, admonitions
Minimum 1500 riječi. Hrvatski jezik.
Ažurirati mkdocs.yml nav sekciju!
Spremi u docs/regulations/license_classes.md
```

---

## REG-10: Radioamaterska etika (`regulations/ethics.md`)

### Sadržaj koji treba pokriti
1. Amaterski kod — The Amateur's Code (Paul Segal, W9EEA, 1928.) preveden na HR
2. Zlatna pravila ponašanja na opsegu
3. Što NE raditi — zabranjeno ponašanje (komercijalno, glazba, psovke)
4. QRM i namjerno ometanje — kako reagirati, što prijaviti
5. Obveza pomaganja — hitne situacije (MAYDAY, SOS)
6. Elmering — tradicija mentorstva

### Prompt template
```
Kreiraj novu stranicu docs/regulations/ethics.md.

Napiši o radioamaterskoj etici i ponašanju:
1. The Amateur's Code (Paul Segal, 1928.) — prevedi na hrvatski
2. Ponašanje na opsegu: zlatna pravila etikete (minimum 10 pravila)
3. Zabranjeno ponašanje i zakonske posljedice
4. Kako reagirati na namjerno ometanje (QRM) — bez eskalacije
5. Prioritet hitnih veza — kako reagirati na MAYDAY/DISTRESS
6. Elmering — tradicija mentorstva u hobiju, kako postati Elmer

Format: MkDocs, admonitions (warning za zabranjeno, tip za savjete)
Minimum 1500 riječi. Hrvatski jezik.
Ažurirati mkdocs.yml!
Spremi u docs/regulations/ethics.md
```

---

## RES-05: Softver za radioamatere (`resources/software.md`)

### Sadržaj koji treba pokriti
Katalog po kategorijama — za svaki program: naziv, opis, platforma, cijena, link:
1. Logiranje — N1MM+, DXKeeper, Log4OM, CloudLog
2. Digitalni modovi — WSJT-X, fldigi, JS8Call
3. SDR — SDR#, HDSDR, SDRuno, Gqrx
4. Antene — MMANA-GAL, 4NEC2, EZNEC
5. Propagacija — VOACAP, HamClock, DXView
6. Sateliti — Gpredict, SatPC32
7. CW — LCWO, Just Learn Morse Code
8. Radio kontrol — Hamlib, OmniRig, flrig
9. Mobilne aplikacije — HamAlert, RepeaterBook, APRS.fi

### Prompt template
```
Kreiraj novu stranicu docs/resources/software.md.

Napravi katalog softvera za radioamatere po kategorijama:
Kategorije: Logiranje, Digitalni modovi, SDR, Antene, Propagacija,
            Sateliti, CW učenje, Radio kontrol, Mobilne aplikacije

Za svaki program:
- Naziv i link na službenu stranicu
- Kratak opis (1-2 rečenice na HR)
- Platforma (Windows/Mac/Linux/Web/Android/iOS)
- Cijena (Free/Paid/Donationware)

Koristi MkDocs tablice po kategorijama.
Minimum 1500 riječi. Hrvatski jezik.
Ažurirati mkdocs.yml!
Spremi u docs/resources/software.md
```

---

## RES-06: NATO fonetska abeceda (`resources/phonetic_alphabet.md`)

### Sadržaj koji treba pokriti
1. Kompletna tablica — slovo, NATO riječ, izgovor (fonetski HR), primjer
2. Brojevi — kako se izgovaraju u radio prometu (0-9)
3. Posebni signali — prosignali (AR, SK, BT, KN...)
4. Vježba — kako vježbati s pozivnim oznakama i brojevima
5. Česte greške — grješna izgovaranja

### Prompt template
```
Kreiraj novu stranicu docs/resources/phonetic_alphabet.md.

Napravi kompletnu referencu za NATO fonetsku abecedu:
1. Tablica: Slovo | NATO riječ | Izgovor (fonetski) | Primjer korištenja u HAM radio
2. Brojevi: 0-9 i kako se izgovaraju u radio prometu (niner, etc.)
3. Posebni prosignali: AR, SK, BT, KN, DN — kratka tablica s objašnjenjima
4. Vježba: kako vježbati (koristiti registracijske tablice, adrese, pozivne)
5. Česte greške i ispravni izgovori

Format: MkDocs, tablice, admonitions
Minimum 800 riječi. Hrvatski jezik.
Ažurirati mkdocs.yml!
Spremi u docs/resources/phonetic_alphabet.md
```

---

## RES-08: Priprema za ispit (`resources/exam_prep.md`)

### Sadržaj koji treba pokriti
1. Plan učenja — tjedni raspored za 2-3 mjeseca
2. Sažetak gradiva po temama s linkovima na stranice priručnika
3. Primjeri ispitnih pitanja (15-20) s odgovorima i objašnjenjima
4. Savjeti za dan ispita
5. Online resursi za vježbu (kvizovi, aplikacije)

### Prompt template
```
Kreiraj novu stranicu docs/resources/exam_prep.md.

Napravi vodič za pripremu radioamaterskog ispita u HR:
1. Plan učenja: tjedni raspored za 2-3 mjeseca pripreme (tablica)
2. Sažetak gradiva po temama s linkovima na sve relevantne stranice priručnika
3. Primjeri ispitnih pitanja (15-20) s točnim odgovorima i objašnjenjima ZAŠTO
4. Savjeti za dan ispita (što ponijeti, kako se opustiti)
5. Online resursi za vježbu — web kvizovi i mobilne aplikacije

Format: MkDocs, admonitions, tablice, linkovi unutar priručnika
Minimum 2000 riječi. Hrvatski jezik.
Ažurirati mkdocs.yml!
Spremi u docs/resources/exam_prep.md
```

---

# VAL 3: P2 i P3 moduli (bonus sadržaj)

> Raditi kad ima slobodnih tokena. Agent odabire jedan modul, radi ga kompletno pa prelazi na sljedeći.

## P2 Moduli — kratki opis

| ID | Naslov | Kratki opis sadržaja |
|----|--------|---------------------|
| TEC-07 | Hamnet | Arhitektura, oprema (Ubiquiti/Mikrotik), konfiguracija, HR čvorovi |
| TEC-09 | Napajanja | Linearni vs switching, 13.8V, dimenzioniranje, baterije, solar |
| TEC-10 | Filtri | Low-pass, band-pass, high-pass, notch — primjena u ham radiju |
| TEC-11 | Prijenosni vodovi | Koaksijalni detaljno, ladder line, gubici, waveguide |
| TEC-12 | Antenski tuneri | Manual vs auto, L-network, T-network, kako koristiti |
| TEC-13 | Pojačala (PA) | Klase pojačanja, tube vs solid-state, linearnost, IMD |
| TEC-17 | SDR detaljno | RTL-SDR, SDRPlay, HackRF, Airspy — arhitektura, softver, projekti |
| TEC-18 | Mjerni instrumenti | SWR metar, NanoVNA, osciloskop, spektralni analizator |
| TEC-19 | EMC i smetnje | TVI/BCI, filtriranje, feritne jezgre, dijagnostika |
| TEC-21 | Katalog antena | Detaljni profil za 15+ vrsta antena |
| TEC-23 | RF sigurnost/PEM | ICNIRP, proračuni, praktične sigurne udaljenosti |
| REG-07 | Namjena spektra | Nacionalna tablica, primarna/sekundarna namjena |
| REG-08 | ITU regije | Mapa regija, zone, kako utječu na frekvencije |
| REG-09 | Recipročne dozvole | CEPT T/R 61-01, rad iz inozemstva |
| OPR-09 | APRS | Digipeaters, I-gates, tracker, weather station, mobilni |
| OPR-10 | DMR/D-STAR/C4FM | Talkgroups, reflektori, code plugs, usporedba |
| OPR-14 | Diplome | DXCC, WAS, WAZ, IOTA, SOTA, 9A diplome |
| OPR-15 | Logging softver | Detaljne usporedbe, setup vodič (N1MM, Log4OM, CloudLog) |
| ACT-05 | Sateliti (proširen) | Keplerian elementi, tracking, oprema, ISS ARISS program |
| ACT-07 | QRP | Filozofija, oprema, antene, QCX+, uBITX, TR-USDX |
| ACT-08 | Samoizgradnja | Alati, lemljenje, PCB izrada, kit vs scratch |
| ACT-10 | Field Day | Pravila, organizacija, setup, ARRL FD vs HRS |
| ACT-11 | Posebne postaje HR | 9A kontesti, memorijalne, jubilarne pozivne |
| EMC-04 | Winlink (proširen) | Detaljni setup VARA, ICS forms, WINMOR |
| EMC-05 | Go-Kit | Kompletna lista opreme, nivoi (basic/intermediate/advanced) |
| EMC-06 | ICS obrasci | ICS 213, 214, 205 — kako ih koristiti u EmComm-u |
| EMC-07 | Mesh mreže | AREDN, Meshtastic, LoRa — setup vodič |
| CB-06 | Od CB do hama | Put nadogradnje, usporedba, motivacija |
| COM-05 | Online zajednice | Reddit, Discord, forumi, Facebook grupe |
| COM-06 | Ham sajmovi | Friedrichshafen, Dayton, HR susreti |
| RES-03 | Formule | Quick reference sheet svih formula s MathJax |
| RES-04 | Linkovi | Kategorizirani linkovi na sve važne resurse |
| RES-07 | Band chart | Vizualni prikaz opsega i dozvola za HR razrede |
| RES-09 | Knjige | Preporučena literatura (HR i EN) |
| HIS-03 | HR ham povijest | Od prvih amatera do danas, značajne ličnosti |

## P3 Moduli — kratki opis

| ID | Naslov | Kratki opis sadržaja |
|----|--------|---------------------|
| TEC-14 | Oscilatori/PLL | VFO, crystal, PLL, DDS — teorija i primjena |
| TEC-16 | Digitalna elektronika | Logička vrata, mikrokontroleri, Arduino za ham |
| TEC-22 | Modeliranje antena | MMANA-GAL tutorial korak po korak, 4NEC2 |
| OPR-16 | SSTV | Slow Scan TV, Robot modes, softver |
| OPR-17 | Packet Radio | AX.25, TNC, BBS, digipeaters |
| OPR-18 | EME | Moonbounce, oprema, WSJT JT65B |
| ACT-09 | Fox hunting | T-hunt, oprema za snifanje, strategija |
| PRJ-02 | Dipol — DIY | Korak po korak gradnja dipola s materijalima |
| PRJ-03 | Dummy load — DIY | Jednostavno izgradi RF opterećenje |
| PRJ-06 | End-Fed — DIY | 9:1 Unun + žica, izračuni i gradnja |
| HIS-02 | Povijest radija | Tesla, Marconi, Hertz — kronologija |
| HIS-05 | Poznati radioamateri | Astronauti, predsjednici, nobelovci koji su bili OM-i |
| PRO-01 do PRO-07 | Propagacija (sekcija) | Ako se odluči odvojiti od TEC-08 u zasebnu sekciju |

---

> **NAPOMENA O OPSEGU**
>
> Ukupan projekt ima potencijal od 113 modula i ~150.000+ riječi sadržaja.
> Ne pokušavajte napraviti sve odjednom!
>
> Preporučeni pristup po sprintovima:
> - **Sprint 1**: 3-5 P1 modula iz Vala 1 (proširenje postojećih)
> - **Sprint 2**: 3-5 novih P1 modula iz Vala 2
> - **Sprint 3+**: Miješati Val 1, 2 i 3 po potrebi i dostupnosti tokena
