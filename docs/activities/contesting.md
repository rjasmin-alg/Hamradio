# Natjecanja (Contesting)

Radioamaterska natjecanja su "sportski" dio hobija — organizirani događaji u kojima cilj nije razgovor, već što više uspostavljenih veza u zadanom vremenskom okviru. Natjecanja su odličan način za testiranje vlastite stanice i operativnih vještina, upoznavanje novih OM-a širom svijeta, te osvajanje diploma i plasmana.

Ukoliko ste ikad zaredali QSO po QSO na 20 metrima dok su signali bili odlični, već ste na rubu contestiranja — jedino što nedostaje je logiranje i malo strategije.

---

## Što je contest QSO?

Za razliku od redovne veze gdje razmjenjujete ime, lokaciju i komentare o opremi, u natjecanjima razmjena traje **samo nekoliko sekundi**. Svako natjecanje ima propisanu formulu razmjene (exchange): najčešće je to raport (59 ili 599) plus neki element koji se boduje (CQ zona, ITU zona, serijski broj veze, lokator...).

Brzina i preciznost bitni su više od kvalitete "razgovora".

### Primjer SSB razmjene (CQ WW DX)

```text
9A1ZG: "CQ Contest, CQ Contest, Niner Alpha One Zulu Golf, 9A1ZG"
DJ3AB: "DJ3AB"
9A1ZG: "DJ3AB, 59, 15"          ← raport 59, CQ zona 15 za Hrvatsku
DJ3AB: "59, 14"                  ← raport 59, CQ zona 14 za Njemačku
9A1ZG: "73, QRZ? 9A1ZG"
```

Cijela razmjena traje 10–20 sekundi. Iskusni contesteri idu i ispod 10 sekundi.

### Primjer CW razmjene

```text
9A1ZG: CQ TEST 9A1ZG 9A1ZG
DJ3AB: DJ3AB
9A1ZG: DJ3AB 599 001     ← RST 599, naš serijski broj veze: 001
DJ3AB: 599 088           ← RST 599, njegov serijski broj: 088
9A1ZG: TU 9A1ZG
```

!!! tip "Zašto uvijek „59" ili „599"?"
    U natjecanjima gotovo svi šalju raport „59" ili „599", bez obzira na stvarnu kvalitetu signala. To je konvencija — cilj nije ocijeniti signal, nego što brže zamijeniti potrebne podatke. Iznimka su natjecanja koja boduju realni raport (npr. Worked All Germany — WAG Contest).

---

## Kategorije operatora

Kako bi natjecanja bila pravedna, sudionici se prijavljuju u jednu od definiranih kategorija prema broju operatora, snazi i upotrebi DX clustera (sustava koji obavještava o aktivnim stanicama):

| Kategorija | Opis | Maks. predajnika | DX klaster? | Tipična primjena |
|---|---|---|---|---|
| **Single Op (SO)** | Jedan operator, sve sam — i postavljanje frekvencije i logiranje i CQ | 1 | Ne | Počeci i iskusni solo operatori |
| **Single Op Assisted (SOA)** | Jedan operator, ali s pristupom DX klasteru za spot-ove | 1 | Da | Odlično za lovce na rijetke entitete |
| **Multi Single (M/S)** | Više operatora, ali samo jedan predajnik aktivan u danom trenutku | 1 | Da | Klubski timovi za varijante bende/mode |
| **Multi Two (M/2)** | Više operatora, dva predajnika simultano (na različitim bandovima) | 2 | Da | Organizirane skupne postaje |
| **Multi Multi (M/M)** | Više operatora, po jedan predajnik na svakom bandu simultano | Neograničeno | Da | Velike DX ekspedicije i mega postaje |
| **QRP** | Izlazna snaga maksimalno 5 W | 1 | Ovisno | Entuzijasti minimalnih stanica |

Uz ove osnovne kategorije postoje i **overlay kategorije** — dodatne podjele unutar kojih se natjeces paralelno s glavnom kategorijom:

- **Rookie** — operatori s dozvolom kraćom od 3 godine
- **Classic** — bez asistencije i bez daljinskog upravljanja
- **Youth** — operatori mlađi od 25 godina

!!! note "Operator vs. kategorija"
    Kada se prijavljujete za natjecanje, birate kategoriju koja odgovara vašoj postavi. Nema smisla stati u kategoriju High Power ako radite s 100 W — Low Power ste, i uspoređivat ćete se s jednakima. Pogrešna prijava znači diskvalifikaciju.

---

## Bodovanje — zašto su množitelji ključni

Ukupni rezultat u gotovo svakom natjecanju nije samo zbroj veza, nego **umnožak QSO bodova i množitelja (multipliers)**:

$$\text{Rezultat} = \sum \text{QSO bodovi} \times \sum \text{Množitelji}$$

**Što su množitelji?** To su posebni ciljevi koji se osvajaju jednom po bandu ili po natjecanju — npr. svaka CQ zona, svaka zemlja (DXCC entitet), svaki američki savez, svaki lokator... Svaki novi množitelj može biti vredniji od desetaka "normalnih" QSO-a.

### Bodovanje u CQ WW DX (najveće natjecanje na svijetu)

| Element | Pravilo bodovanja |
|---|---|
| QSO s vlasitom zemljom (HR ↔ 9A) | 0 bodova |
| QSO unutar iste CQ zone (EU ↔ EU) | 1 bod |
| QSO između kontinenata (HR ↔ USA, JA, VK...) | 3 boda |
| Množitelji — CQ zone | Svaka nova zona jednom po bandu |
| Množitelji — DXCC entiteti | Svaka nova zemlja jednom po bandu |

!!! example "Primjer izračuna"
    Operator je u 24 sata napravio **800 QSO-a** — 300 unutar Europe (1 bod svaki) i 500 prema Sjevernoj Americi, Aziji i Oceaniji (3 boda svaki).

    - QSO bodovi: 300 × 1 + 500 × 3 = **1.800 bodova**
    - Množitelji: 38 CQ zona + 120 DXCC zemalja = **158 množitelja**
    - **Ukupno: 1.800 × 158 = 284.400 bodova**

    Zato je pronalaženje neke rijetke stanice iz zone 26 ili malog otočnog DXCC entiteta daleko vrednije od deset QSO-a s uobičajenim europskim stanicama.

---

## Kalendar najvažnijih natjecanja

Natjecanja se odvijaju tokom cijele godine. Evo pregleda onih na kojima ćete najčešće čuti aktivnost:

| Natjecanje | Mod | Termin | Razmjena | Pravila |
|---|---|---|---|---|
| **CQ WW DX SSB** | SSB | Zadnji vikend listopada | RS + CQ zona | [cqww.com](https://cqww.com) |
| **CQ WW DX CW** | CW | Zadnji vikend studenog | RST + CQ zona | [cqww.com](https://cqww.com) |
| **CQ WPX SSB** | SSB | Zadnji vikend ožujka | RS + serijski broj | [cqwpx.com](https://cqwpx.com) |
| **CQ WPX CW** | CW | Zadnji vikend svibnja | RST + serijski broj | [cqwpx.com](https://cqwpx.com) |
| **ARRL DX SSB** | SSB | 3. vikend veljače | RS + država/snaga | [arrl.org](https://www.arrl.org/) |
| **ARRL DX CW** | CW | 3. vikend ožujka | RST + država/snaga | [arrl.org](https://www.arrl.org/) |
| **WAE DX CW** | CW | 2. vikend kolovoza | RST + QTC blokovi | [darc.de](https://www.darc.de/) |
| **WAE DX SSB** | SSB | 2. vikend rujna | RS + QTC blokovi | [darc.de](https://www.darc.de/) |
| **IOTA Contest** | SSB/CW | Posljednji puni vikend srpnja | RS(T) + serijski ili IOTA br. | [rsgbcc.org](https://www.rsgbcc.org/) |
| **9A DX Contest** | SSB/CW | 3. vikend prosinca | RS(T) + županija (9A) / ITU zona (DX) | [hamradio.hr](https://www.hamradio.hr) |

!!! warning "WARC opsezi — bez natjecanja!"
    Bandovi **30 m (10 MHz)**, **17 m (18 MHz)** i **12 m (24 MHz)** su WARC opsezi i na njima je po međunarodnom dogovoru (IARU) zabranjena organizacija i sudjelovanje u natjecanjima. To su "mirne zone" za normalne QSO-e i propagacijska istraživanja. Više o opsezima u [Frekvencijskim planovima](../operating/bandplans.md).

---

## Softver za logiranje

U natjecanjima se ne logira ručno — koriste se specijalizirani programi koji integriraju radio (CAT kontrola), automatski provjeravaju duplikate, prikazuju multipliere u realnom vremenu i generiraju Cabrillo log za slanje.

=== "N1MM+ Logger"
    Najpopularniji besplatni contest logger za Windows. Koristi ga većina operatora — od početnika do svjetskih prvaka.

    - **Prednosti:** Podržava 1000+ različitih natjecanja, izvrsna CAT integracija s gotovo svakim radiom, "voice keyer" za automatske SSB pozive, aktivna zajednica i detaljna dokumentacija.
    - **Rate metar** u realnom vremenu pokazuje koliko QSO-a postižete na sat.
    - **Download:** [n1mmwp.hamdocs.com](https://n1mmwp.hamdocs.com/)
    - **Cijena:** Besplatno

=== "DXLog.net"
    Moderan, brz i iznimno funkcionalan logger, posebno popularan za Multi-Op postaje. Projektiran je djelomično i u Hrvatskoj.

    - **Prednosti:** Odlično mrežno logiranje za M/S i M/M kategorije, sinkronizacija unutar LAN mreže postaje, cloud backup.
    - Podržava sva glavna natjecanja, moderan UI.
    - **Download:** [dxlog.net](http://dxlog.net/)
    - **Cijena:** Besplatno za natjecanja

=== "Win-Test"
    "Klasik" koji koriste iskusni contesteri i velike postaje. Baziran na prečacima programa CT (legendarnog contest loggera iz 80-ih).

    - **Prednosti:** Iznimno stabilan, u upotrebi desecima godina, podržan kod svih ozbiljnih Multi-Multi postaja.
    - **Download:** [win-test.com](http://www.win-test.com/)
    - **Cijena:** Plaćeno (shareware, ~50 €)

!!! tip "Za početak: N1MM+"
    Instalirajte N1MM+, prođite kroz kratki setup wizard (pozivna, CAT port za radio) i probajte ga **tjedan dana prije** natjecanja — ne na dan samog contesta. Svako natjecanje ima predefiniranu konfiguraciju u N1MM+ i možete početi s loggiranjem u par minuta.

---

## Strategija

Contesting nije samo o snazi antene — strategija igra veliku ulogu.

### Running vs. Search & Pounce (S&P)

**Running** znači da držite vlastitu čistu frekvenciju i neprestano zovete `CQ TEST`. Stanice vas same pronalaze i odgovaraju. Ovo je produktivno kad imate jaki signal i slobodnu frekvenciju, ali zahtijeva dobru antenu i malo sreće s propagacijom.

**Search & Pounce (S&P)** znači da vi tražite po bandu, pronalazite stanice koje zovu CQ i odgovarate njima. Ovo je idealno za početnike jer ne trebate "držati" frekvenciju, a ipak prikupljate QSO-e i multipliere.

**Praktični pristup:** Počnite S&P da prikupite multipliere s rijetkih entiteta, a onda — ako pronađete tišu rupu na bandu — probajte kratki CQ run.

### Rate vs. Množitelji

Operatori koji otkucavaju 200 QSO/sat gotovo uvijek radije nastavljaju run nego prekidaju ga radi jednog množitelja. No računica je drugačija kad је rate niži: jedan uniqni množitelj može biti vrijedniji od 10–20 "običnih" QSO-a.

**Jednostavno pravilo:** Ako vaš rate padne ispod 50 QSO/sat, vrijedi prekinuti i potražiti nove multipliere po bandu.

### Band hopping i propagacija

Propagacija se mijenja tokom dana i noći — 20 m je otvoren za Ameriku poslijepodne po UTC vremenu, 40 m i 80 m rade daljine noću, a 15 m i 10 m rade odlično samo pri višem solarnom fluksu (SFI > 120). Više o ovome u poglavlju [Propagacija radio valova](../technical/propagation.md).

!!! info "Grey line — zlatni sat contestera"
    Zona sumraka (grey line) koja se pomiče po Zemlji ujutro i navečer lokalno otvara iznimno povoljne propagacijske "prozore". Iskusni contesteri planiraju pojačanu aktivnost upravo u tim intervalima za uzimanje maksimalnih multipliera iz udaljenih dijelova svijeta.

---

## 9A natjecanja

Hrvatska radioamaterska zajednica (HRS) organizira ili sudjeluje u nekoliko tradicijskih natjecanja:

**9A DX Contest** je glavno hrvatsko natjecanje, otvoreno za sve stanice na svijetu. Odvija se trećeg vikenda u prosincu, traje od subote 14:00 UTC do nedjelje 13:59 UTC, na bandovima 160–10 m u miješanom modu (SSB i CW).

- Razmjena za **9A postaje**: RS(T) + dvoslovna kratica županije (ZG = Zagreb, ST = Split, RI = Rijeka, OS = Osijek, itd.)
- Razmjena za **DX postaje** (izvan HR): RS(T) + ITU zona
- **Bodovanje:** Kontakti s 9A stanicama vrijede više (posebni množitelji)
- Cabrillo logove šaljete na adresu na [hamradio.hr](https://www.hamradio.hr/9a-dx-contest/) najkasnije 7 dana után natjecanja.

**9A Activity Contest** su redoviti VHF/UHF natjecaji koji potiču aktivnost na 144 MHz, 432 MHz i 1296 MHz. Odlični su za testiranje antena i orijentaciju — radi se s lokatorima (IARU locator grid squares).

Za aktualni popis natjecanja, memorijalnih i prigodnih contesta u organizaciji HRS-a i hrvatskih klubova, pratite [www.hamradio.hr](https://www.hamradio.hr).

---

## Slanje loga — Cabrillo format

Nakon natjecanja, log se šalje organizatoru u standardiziranom **Cabrillo formatu** — tekstualna datoteka sa zaglavljem i popisom svih QSO-a. Svi contest loggeri (N1MM+, DXLog, Win-Test) generiraju Cabrillo jednim klikom.

U N1MM+: `File → Generate Cabrillo Log`

!!! info "Primjer Cabrillo datoteke"
    ```text
    START-OF-LOG: 3.0
    CALLSIGN: 9A1ZG
    CONTEST: CQ-WW-SSB
    CATEGORY-OPERATOR: SINGLE-OP
    CATEGORY-ASSISTED: NON-ASSISTED
    CATEGORY-BAND: ALL
    CATEGORY-POWER: LOW
    CLAIMED-SCORE: 284400
    OPERATORS: 9A1ZG
    NAME: Jasmin Prezime
    ADDRESS: Zagreb, Croatia
    CREATED-BY: N1MM+ 1.0.10234.0
    ...
    QSO: 14195 PH 2024-10-26 1201 9A1ZG         59 15   DJ3AB         59 14
    QSO: 14195 PH 2024-10-26 1203 9A1ZG         59 15   W1ABC         59 05
    END-OF-LOG:
    ```

Rokovi slanja su obično 5–7 dana po završetku natjecanja. Čak i ako imate samo 20 QSO-a — pošaljite log! Prijavom dobivate certifikat sudjelovanja i vaš rezultat ulazi u statistiku, što je korisno i organizatoru.

---

## Kako početi — vodič za prvog contestera

Contesting zna izgledati komplicirano izdaleka, ali ulaz je jednostavan:

1. **Instalirajte N1MM+** — besplatan je, pokrenite ga, unesite pozivnu oznaku i konfigurirajte CAT vezu s radiom. Probajte to nekoliko dana prije natjecanja.
2. **Odaberite manje zahtjevno natjecanje za start** — 9A Activity Contest (VHF) ili IOTA Contest su dobri izbori. CQ WW je sjajan, ali masa stanica može biti zastrašujuća za prvog puta.
3. **Prijavite se kao Single Op Low Power** — nema pritiska, natječete se samo unutar vlastite kategorije.
4. **Počnite s S&P modsom** — okrećite VFO, pronalazite stanice koje zovu CQ TEST i odgovarajte. Ne trebate "držati" frekvenciju.
5. **Sudjelujte 2–4 sata, ne 48** — iskusite ritam, logiranje, S&P. Puni vikend možete probati sljedeći put.
6. **Pošaljite log** — čak i s 15 QSO-a. N1MM+ generira Cabrillo u sekundi.

!!! tip "Ne čekajte savršenu stanicu"
    Odlični contesteri redovito postižu sjajne rezultate s dipol antenom i 100 W. Strategija i propagacijsko znanje su važniji od pojačala.

---

## Povezane teme

- [Procedura veze](../operating/procedures.md) — QSO procedura i Q-kodovi
- [Frekvencijski planovi](../operating/bandplans.md) — koji opsezi za koje modove
- [Propagacija radio valova](../technical/propagation.md) — kada raditi koje opsege
- [Antene i vodovi](../technical/antennas.md) — ulaganje koje se isplati za contesting
- [Rad u pokretu — SOTA/POTA](portable.md) — portabl aktivnosti kao alternativa
