# Propagacija radio valova

Propagacija je jedna od fascinantnih tema radioamaterizma — ona određuje sve. S istom opremom, na 20-metarskom opsegu možete u jednom trenutku čuti samo lokalne stanice, a već sat kasnije raditi DX veze s Japanom ili Australijom. Razumijevanje propagacije pretvara sreću u vještinu.

## Tri temeljna mehanizma propagacije

### 1. Zemni val (Ground Wave)

Elektromagnetski val koji se "prilijepljuje" za površinu Zemlje i prati njenu zakrivljenost.

*   **Frekvencijsko područje**: Najefektivniji ispod 3 MHz (160 m, 80 m)
*   **Domet**: Do ~500 km za AM postaje; do ~1000 km za LF/VLF
*   **Karakteristike**: Stabilan, neovisan o dobu dana; opada s porastom frekvencije
*   **Primjena**: Lokalne veze na 160 m i 80 m, AM broadcast, brodske komunikacije

### 2. Ionosferski val / Nebeski val (Sky Wave)

RF signal koji se odašilje pod kutom prema nebu, reflektira od ionosfere i vraća na Zemlju stotinama ili tisućama kilometara dalje.

$$ d_{skip} = 2h \cdot \tan(\theta) $$

Gdje je $h$ visina ionosfere i $\theta$ kut odašiljanja iznad horizonta. Manji kut = veći domet.

*   **Frekvencijsko područje**: 3–30 MHz (HF opsezi)
*   **Domet**: 1000–20,000+ km (višestruki skokovi)
*   **Karakteristike**: Ovisi o dobu dana, godišnjem dobu i sunčevom ciklusu
*   **Primjena**: DX komunikacije na HF — osnova interplanetarne komunikacije

!!! note "Skip zona (mrtva zona)"
    Između dosega zemnog vala i prvog skoka ionosferskog vala postoji zone gdje vas nitko ne čuje — "skip zona" ili "dead zone". Stanica 100 km od vas može biti "nevidljiva" dok vas jasno čuje postaja u Australiji!

### 3. Linija vidljivosti (Line-of-Sight — LOS)

VHF i UHF signali putuju u ravnoj liniji, poput svjetlosti.

$$ d_{km} \approx 4.12 \left(\sqrt{h_{T,m}} + \sqrt{h_{R,m}}\right) $$

Gdje su $h_T$ i $h_R$ visine antena predajnika i prijemnika u metrima.

*   **Frekvencijsko područje**: VHF (30 MHz+), UHF, SHF
*   **Domet**: Tipično 50–150 km (za visoke pozicije)
*   **Karakteristike**: Stabilan, predvidljiv; uvećan za ~10% zbog atmosferske refrakcije
*   **Primjena**: FM repeteri, digitalne veze, satelitske komunikacije

---

## Ionosfera — slojevi i mehanizmi

Ionosfera je sloj atmosfere (60–1000 km visine) koji ionizira sunčeva UV i X-ray radijacija. Ioni i slobodni elektroni reflektiraju RF signale.

### D sloj (60–90 km)

*   **Prisutan**: Samo danju (solar UV ionizacija)
*   **Efekt**: Apsorbira niže frekvencije (3–10 MHz) umjesto da ih reflektira
*   **Praktično**: Danju utrne 80 m i 160 m opsege za DX. Noću se D sloj raspada — tada ti opsezi "otvaraju" za dalekovide veze!

### E sloj (90–140 km)

*   **Prisutan**: Danju, slabije noću
*   **Efekt**: Reflektira signale do ~20 MHz; noću omogućuje lokalne veze na 40 m
*   **Sporadični E (Es)**: Nepredvidljive oblake ionizacije koje se javljaju ljeti → spektakularne DX veze na 50 MHz (6 m), 70 MHz, pa čak i 144 MHz!

### F sloj (140–400+ km)

Najvažniji sloj za HF DX komunikacije.

*   **F1 sloj** (140–200 km): Postoji samo danju, slabiji reflektor
*   **F2 sloj** (200–400+ km): Postoji cijeli dan, noću se F1 i F2 spajaju u jedan F sloj; **primarni reflektor za DX**

Visina F2 sloja varira: noću niže (~200 km), danju više (~350 km). Viši F2 → dulji domet skoka.

### MUF — Maksimalna upotrebljiva frekvencija

MUF je **najviša frekvencija** koja se pri određenom kutu odašiljanja može reflektirati od ionosfere i vratiti na Zemlju:

$$ MUF = f_{oF2} \cdot \sec(\theta) = \frac{f_{oF2}}{\cos(\theta)} $$

Gdje je $f_{oF2}$ kritična frekvencija F2 sloja (mjerena vertikalnim sounderom) i $\theta$ kut odašiljanja od zenita.

*   **Iznad MUF**: Signal prolazi kroz ionosferu u svemir — nema refleksije
*   **Ispod MUF**: Signal se reflektira — dobra propagacija
*   **Pravilo**: Radite na frekvenciji **10–15% ispod MUF** za najpouzdaniju propagaciju

### LUF — Najniža upotrebljiva frekvencija

LUF je **najniža frekvencija** koja prolazi kroz apsorpcijski D sloj s dovoljno snage za korisnu vezu. Ovisi o snazi predajnika, opsegu i uvjetima.

---

## HF propagacija po opsezima

| Opseg | Frekvencija | Danju | Noću | DX potencijal | Karakteristike |
|-------|-------------|-------|------|---------------|---------------|
| **160 m** | 1.8–2.0 MHz | Lokalni (zemni val) | EU/globalni (ionosf.) | Zimske noći | "Top Band", tih i zahtjevan |
| **80 m** | 3.5–4.0 MHz | EU regionalni | EU i transkontinentalni | Zima, noć | Popularan za europski DX |
| **40 m** | 7.0–7.2 MHz | EU regionalni | Transkontinentalni | Cijela godina, noć | Najpouzdaniji all-round opseg |
| **30 m** | 10.1–10.15 MHz | EU i transkontinentalni | Globalni | Cijela godina | WARC, samo CW/digital |
| **20 m** | 14.0–14.35 MHz | **Globalni DX!** | Ovisi o ciklusu | ⭐ Cijela godina | "Kralj HF", uvijek aktivan |
| **17 m** | 18.068–18.168 MHz | Globalni (uz sunce) | Slabije | Visok solar flux | WARC opseg, odličan za DX |
| **15 m** | 21.0–21.45 MHz | Globalni (uz sunce) | Rijetko | Visokog solar flux | Otvara uz jači SFI |
| **12 m** | 24.89–24.99 MHz | Nepredvidljiv | Zatvoren | "Otvori i luđe" | WARC, odličan uz visok SFI |
| **10 m** | 28.0–29.7 MHz | Impresivni DX! | Zatvoren | Maksimum ciklusa | Ludnica kad se otvori |
| **6 m** | 50–52 MHz | LOS + sporadični E | LOS | Sporadični E ljeti | "Magični opseg" |

!!! tip "40 m je svakodnevni prijatelj"
    40 m (7 MHz) je najpouzdaniji opseg — noću transkontinentalan, danju europski. Ako ne znate što raditi, uključite 40 m i slušajte.

---

## Sunčev ciklus i solarni indeksi

Sunčeva aktivnost mijenja se u ciklusima od ~11 godina, direktno utječući na ionizaciju F2 sloja.

### Solar Flux Index (SFI)

Mjera jakosti sunčevog RF zračenja na 10.7 cm. Proporcionalan ionizaciji ionosfere.

| SFI | Stanje ionosfere | HF propagacija |
|-----|-----------------|----------------|
| < 70 | Minimum ciklusa | 10 m i 12 m zatvoreni, ostalo slabije |
| 70–100 | Prosječno | 20 m uvijek radi, 15 m ponekad |
| 100–150 | Dobro | 10 m i 15 m otvoreni, DX odlično |
| > 150 | Maksimum | Svi opsezi otvoreni, DX rekordi |

**Trenutno stanje**: Solani ciklus 25 (SC25) je u svom maksimumu (2024–2025) — SFI redovito prelazi 200! Odlično za DX na 10 m i 15 m.

### K-indeks (geomagnetic activity)

Mjera geomagnetskih poremećaja. Skala 0–9.

| K-indeks | Stanje | Efekt na HF |
|----------|--------|------------|
| 0–2 | Mirno | Odlično za DX |
| 3 | Blago nestabilno | Uglavnom dobro |
| 4 | Aktivno | Degradacija viših opsega |
| 5–6 | Mali geomagnetski oluja | Značajni poremećaji |
| 7–9 | Velika oluja | HF blackout, aurora |

!!! warning "Geomagnetske oluje"
    Kada je K ≥ 5, HF veze postaju nesigurne ili nemoguće. Istovremeno, aurora se pojavljuje i moguće su aurora-scatter veze na VHF! Pratite [NOAA Space Weather](https://spaceweather.gov).

### A-indeks

Dnevni prosjek geomagnetske aktivnosti. A < 15 = dobri uvjeti; A > 30 = poremećeno.

---

## VHF/UHF propagacija — posebni načini

### Troposferska propagacija (Tropo)

Nastaje kada postoji **temperaturna inverzija** u troposferi — sloj toplog zraka iznad hladnog. RF signal se "zarobi" u ovom "tunelu" i prolazi stotine kilometara.

*   **Frekvencije**: 144 MHz–10 GHz
*   **Domet**: 200–2000+ km (u izuzetnim uvjetima)
*   **Prognoza**: [DXinfocentre.nl tropo prognoza](https://www.dxinfocentre.com/tropo_eur.html)
*   **Sezona**: Topliji dio godine (proljeće, ljeto, jesen), posebno rano jutro i kasna večer

!!! example "Tropo primjer iz HR"
    Iz Dalmacije prema Italiji (Jadran) tropo je redovita pojava. Na 144 MHz SSB mogu se ostvarivati veze s talijanskim stanicama na 300–500 km bez ikakvog skoka.

### Sporadični E (Sporadic-E, Es)

Oblaci guste ionizacije u E sloju koji se formiraju nepredvidljivo, uglavnom ljeti.

*   **Frekvencije**: 50 MHz (6 m) — najčešće; 70 MHz; rjeđe 144 MHz
*   **Domet**: 800–2500 km (jedan skok)
*   **Sezona**: Travanj–kolovoz (sjevernim ljeto); sekundarni minimum prosinac–siječanj
*   **Trajanje**: Minute do nekoliko sati
*   **Praćenje**: [DXmaps](https://www.dxmaps.com) — real-time mapa Es veza

!!! note "6 m = 'Magični opseg'"
    50 MHz opseg se zove "Magic Band" jer se nikad ne zna što će se dogoditi. Može biti mrtav tjednima, zatim se odjednom otvori i radite Ameriku ili Afriku sa 100 W. Uvijek isplatite pretvornik na 6 m!

### Meteor scatter (MS)

Meteori koji upadaju u atmosferu ioniziraju kratke trase (milisekunde) koje reflektiraju VHF signale.

*   **Frekvencije**: 50 MHz i 144 MHz pretežno
*   **Trajanje**: Milisekunde (za meteorske prskove) do minute (bolidi)
*   **Digitalni modovi**: MSK144 (WSJT-X) — jedini praktični način danas
*   **Meteorski rojevi**: Perseidi (kolovoz), Leonidi (studeni) su najpouzdaniji

### Aurora scatter

Aurora Borealis je efektivni reflektor VHF signala prema jugu. Nastaje za geomagnetskih oluja.

*   **Frekvencije**: 50 MHz i 144 MHz pretežno
*   **Karakteristike**: CW ima specifičan "reski" zvuk; SSB je nerazumljiv
*   **Smjer**: Antena okrenuta prema sjeveru (aurora)
*   **Sezona**: Jesen i zima, uz K-indeks ≥ 5

### EME (Earth-Moon-Earth)

Signal se odašilje prema Mjesecu, reflektira i vraća na Zemlju. 770,000 km ukupni put!

*   **Gubici**: ~250 dB ukupne propagacijske gubitke
*   **Zahtjevi**: Velika antena (Yagi array), najmanji 100 W (bolje kW), digitalni mod (JT65, QRA64)
*   **Frekvencije**: 144 MHz, 432 MHz, 1296 MHz — i više
*   **"Window"**: Mogućno samo kada je Mjesec dovoljno visoko s obje strane

---

## Gray Line — zlatni sat DX-ing-a

Gray line (siva linija) je granica između osvijetljene i tamne strane Zemlje.

**Zašto je posebna?** Na ovoj granici:
*   D sloj još nije formiran (nema apsorpcije) ILI se upravo raspada
*   F2 sloj je još ioniziran s prethodnog dana ILI se počinje ionizirati

To stvara kratki prozor (15–30 minuta) povlaštene propagacije, posebno za niže opsege (40 m, 80 m).

**Praktično**: Pratite gray line na [DXWatch](https://www.dxwatch.com) ili HamClock aplikaciji. Namjestite alarm za izlazak i zalazak sunca na vašoj i ciljnoj lokaciji. Pokrenite radio točno tada!

---

## Alati za praćenje propagacije

| Alat | URL | Opis |
|------|-----|------|
| **VOACAP** | [voacap.com](https://www.voacap.com) | Point-to-point HF prognoza propagacije |
| **PSKReporter** | [pskreporter.info](https://pskreporter.info) | Real-time prikaz FT8/FT4 veza diljem svijeta |
| **DXMaps** | [dxmaps.com](https://www.dxmaps.com) | Interaktivna mapa DX veza i Es/tropo |
| **SolarHam** | [solarham.net](https://www.solarham.net) | SFI, K, A indeksi i sunčeva aktivnost |
| **NOAA SWPC** | [swpc.noaa.gov](https://www.swpc.noaa.gov) | Službena američka prognoza svemirskog vremena |
| **Ionospheric Data** | [digisonde.iau.cas.cz](http://digisonde.iau.cas.cz) | Europski ionosondni podaci (realna foF2) |
| **HamClock** | [github.com/k1jt/hamclock](https://github.com/k1jt/hamclock) | Programabilni sat s gray line, SFI i DX spotovima |

---

## Praktični savjeti za optimalno korištenje uvjeta

1.  **Slušajte prije odašiljanja**: Provjerite PSKReporter ili DXMaps je li željeni opseg otvoren prema vašoj ciljanoj regiji.
2.  **Koristite beacon stanice**: 10 m (28 MHz) beacon mreža (NCDXF) daje izvrsnu sliku otvorenosti opsega.
3.  **40 m noću**: Uvijek pouzdan za europski i transatlantski DX od zalaska do izlaska sunca.
4.  **Pratite SFI**: Ako je SFI > 130, odmah testirajte 10 m i 12 m.
5.  **K > 4? Idite na 40 m**: Viši opsezi su poremećeni, 40 m je otporniji na geomagnetske oluje.
6.  **Gray line alarm**: Postavite svakodnevni alarm za izlazak/zalazak sunca — to je zlatni sat.

---

## Povezane teme

*   [Antene i vodovi](antennas.md) — Kut odašiljanja antene utječe na domet skoka
*   [Frekvencijski planovi](../operating/bandplans.md) — Što se radi na kojim opsezima
*   [Modovi rada](../operating/modes.md) — FT8, SSB, CW za različite uvjete propagacije
*   [DX rad](../activities/dxing.md) — Kako iskoristiti otvorenu propagaciju za DX
