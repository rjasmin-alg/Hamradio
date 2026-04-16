# CB Oprema

Oprema za CB radio je pristupačna, robusna i ne zahtijeva posebno tehničko znanje za postavljanje. Ipak, razlika između loše i dobre CB stanice — posebno u dometu i jasnoći signala — može biti dramatična, a antena je gotovo uvijek ključna.

---

## CB Radiostanice

### Mobilne (auto) stanice

Mobilne CB stanice montiraju se u vozilo i napajaju s 12 V autozapisa. Ovo je najčešća primjena CB-a:

| Model | Modulacije | Snaga | Dimenzije | Cijena (approx.) | Napomene |
|---|---|---|---|---|---|
| **President McKinley** | AM/FM/SSB | 4/12 W | Standardna DIN | ~150–200 € | Popularni europski izbor, SSB, NOAA |
| **President Lincoln II+** | AM/FM/SSB | 4/12 W | Šira od DIN | ~200–250 € | Napredni model, 10 m i CB, SSB |
| **Midland Alan 78 Plus** | AM/FM/SSB | 4/12 W | Standardna DIN | ~120–160 € | Dobra vrijednost, kompaktna |
| **Albrecht AE 6491** | AM/FM/SSB | 4/12 W | Kompaktna | ~130–180 € | Diskretna, zaslončić na žici |
| **Midland Alan 48 Plus** | AM/FM | 4 W | Mini | ~80–100 € | Bez SSB, dobra za početnike |
| **President Bill** | AM/FM | 4 W | Mini | ~70–90 € | Ultra kompaktna |

!!! tip "Preporuka za početnike"
    Midland Alan 48 Plus ili President Bill — odlična vrijednost za novac za lokalni CB rad. Ako planirate DX ili rad na autocestama s lovcima, uzmite model sa SSB-om (Alan 78 Plus ili McKinley).

### Bazne stanice

Bazne stanice montiraju se doma i napajaju mrežom (230 V) ili vanjske napajanjem 12–13.8 V:

- **President George** — klasičan AM/FM/SSB bazni uređaj, DIN format, izvrsna osjetljivost
- **Albrecht AE 5890** — suvremena polno fazirana bazna stanica, dual watch, USB punjač
- Stariji modeli poput **Uniden HR 2510** ili **Galaxy DX 99V** — popularni u DX zajednici zbog poboljšanog filtera

!!! note "Alternativa: mobilna + ispravljač"
    Mnogi korisnici koriste mobilnu stanicu doma s jeftinim ispravljačem (napajanje 13.8 V / 5+ A). Rezultat je identičan baznoj stanici po performansama, a cijena je niža.

### Ručne (handheld) stanice

Za planinarenje, kampiranje i off-road:

| Model | Modulacije | Snaga | Baterija | Napomene |
|---|---|---|---|---|
| **President Randy FCC** | AM/FM | 4 W | 1500 mAh Li-Ion | IP67 vodootporan, robusna |
| **Midland Alan 42 DS** | AM/FM | 4 W | 1200 mAh Li-Ion | Kompaktna, dual band (EU/US) |
| **Albrecht AE 33H** | AM/FM | 4 W | AA baterije | Dugotrajno napajanje |

Ručne stanice imaju manji domet zbog kratke antene — tipično 2–5 km u otvorenom terenu, manje u šumi. Za kolone i kampiranje to je sasvim dovoljno.

---

## CB Antene — Najvažniji dio sustava

Na CB-u više od ijednog drugog faktora, **antena određuje domet**. Razlika između loše i dobre antene lako je 10× u dometu. U kontekstu 4 W snage, investicija u antenu uvijek se isplati više od ilegalne snage.

### Fizika CB antena

Valna duljina na 27 MHz je otprilike **11 metara**. Puna valna antena (dipol) imala bi ramena dugačka 5.5 m — praktično za baznu stanicu, ali ne za auto. Zato CB mobilne antene koriste zavojnice (coil) za električno skraćivanje.

$$\lambda = \frac{c}{f} = \frac{300\,000\,\text{km/s}}{27\,\text{MHz}} \approx 11.1\,\text{m}$$

Što je antena fizički bliža punoj valnoj duljini (ili $\lambda/4 \approx 2.75$ m bez zavojnice), učinkovitija je.

### Mobilne antene (auto)

| Antena | Duljina | Pojačanje | Montaža | Cijena | Napomene |
|---|---|---|---|---|---|
| **Sirio Performer 5000** | 171 cm | ~3 dBd | M6/PL vijak | ~60–80 € | Popularna high-performance antena |
| **President Virginia** | 140 cm | ~2 dBd | Magnet | ~40–60 € | Magnetska, dobra distribucija signala |
| **Midland 1822 Dual Firestik** | 155 cm | ~3 dBd | Nosač | ~50–70 € | Dugotrajnija, vlakno |
| **Albrecht 6130** | 120 cm | ~1.5 dBd | Magnet | ~25–40 € | Ekonomična, ok za lokalno |

**Pravila za mobilne antene:**
1. **Što viša montaža, to bolji domet** — krov automobila bolji je od haube
2. **Što dulja, to bolja** (do razumnog limita) — izbjegavajte kukavičluk od kratkih antena
3. **Magnetske su praktične ali lošije RF mase** — vijčana montaža uvijek bolja

### SWR — Omjer stojnih valova

SWR (Standing Wave Ratio — Omjer stojnih valova) mjera je prilagođenosti antene na frekvenciju. Loš SWR znači da se snaga odbija natrag u predajnik, što ga može oštetiti i smanjuje domet.

$$\text{SWR} = \frac{V_{max}}{V_{min}} = \frac{1 + |\Gamma|}{1 - |\Gamma|}$$

| SWR vrijednost | Ocjena | Što učiniti |
|---|---|---|
| 1.0 – 1.5 | ✅ Odlično | Ništa |
| 1.5 – 2.0 | ✅ Prihvatljivo | Moguće sitno podešavanje |
| 2.0 – 2.5 | ⚠️ Loše | Nužno podešavање antene |
| > 2.5 | ❌ Opasno | Odmah prekinuti — moguće oštećenje predajnika |

**Podešavanje CB antene:** Skoro sve mobilne CB antene imaju vijak ili sklonivu šipku na vrhu za fine podešavanje duljine. Proces:
1. Spojite SWR metar između koaksijalnog kabela i antene
2. Keyrujte na kanalu 1, 20 i 40 te izmjerite SWR
3. Skratite ili produžite antenski element dok SWR nije < 1.5 na svim kanalima
4. Ako raste k krajevima, antena je preduga / prekratka

!!! warning "Nikad ne odašiljajte bez antene!"
    Rad bez priključene antene (ili s isključenom antenskim konektorom) u sekundu može spaliti izlazni tranzistor predajnika. Uvijek provjerite je li antena spojena.

### Bazne antene

Za bazne postaje na 27 MHz, dostupne su prave direktne vertikalke bez zavojnica:

| Antena | Visina | Pojačanje | Cijena | Napomene |
|---|---|---|---|---|
| **Sirio 827** | 5.65 m | 3 dBd | ~120–180 € | Popularna, EU/US channels |
| **Sirio Gain-Master** | 7.1 m | 4 dBd | ~200–280 € | Visoko pojačanje, premium |
| **Albrecht GP 27 CB** | 5.9 m | 3 dBd | ~100–140 € | Solidna ekonomična opcija |
| **President ML145** | 4.6 m | 2 dBd | ~70–100 € | Kompromis visina/pojačanje |

Bazne antene montiraju se na krov, jarbolo ili balkon — što više, to dalekosežniji domet. Coaksijalni kabel od bazne antene do stanice treba biti kvalitetan (RG-8X ili RG-213 za dulje trasse, minimalno RG-58 za kratke do 5 m).

---

## Konekcija i pribor

### Koaksijalni kabeli

| Tip | Promjer | Max. duljina | Napomene |
|---|---|---|---|
| **RG-58** | 5 mm | do 5 m | Jednostavan, fleksibilan, veći gubici na duljim trasama |
| **RG-8X** | 7 mm | do 20 m | Kompromis fleksibilnost/gubici, standard za bazne |
| **RG-213** | 10 mm | do 50 m | Mali gubici, krut, za profesionalne instalacije |
| **Airspace/Ecoflex** | Varijabilno | 100+ m | Premium, minimalni gubici, skupo |

### Potreban pribor

- **SWR metar** — obavezan za podešavanje antene (10–50 €)
- **PL-259 konektori** — standardni CB priključak; provjerite da odgovaraju debljini kabela
- **Antitetički uređaji** — neophodne za instalaciju baznih antena (nosač jarbola, stezaljke)
- **Ispravljač 13.8 V / 5 A** — za korištenje mobilne stanice kao bazne (30–80 €)

---

## Kako povećati domet (legalno)

Bez povećanja snage, domet se može poboljšati:

1. **Bolja antena** — veće pojačanje, viša montaža, bolji SWR
2. **Kraći i deblji koaksijalni kabel** — smanjuje gubitke
3. **Izbor kanala** — SSB na kanalima 38–40 za veće dosege (SSB = 2–3× veći domet od AM iste snage)
4. **Koristiti propagaciju** — sporadic-E i troposferne uvjete za DX
5. **Poboljšati audio** — dobar mikrofon s kompresijom, jasna dikcija, spor govor

!!! info "Pravo pravilo: antena uvijek prije snage"
    Svako udvostručenje snage donosi povećanje signala od 3 dB (jedva primjetno u praksi).
    Svako udvostručenje antenskoga pojačanja = isti 3 dB dobitak, ali legalno i bez rizika od kvara predajnika.
    Investicija u antenu uvijek se isplati više od ilegalne snage.

---

## Povezane teme

- [Propisi i kanali](channels.md) — dozvoljene snage i modulacije
- [Uvod u CB](intro.md) — kontekst i zajednica
- [Antene i vodovi](../technical/antennas.md) — detaljnija fizika antena
- [Sigurnost](../technical/safety.md) — sigurna instalacija antena i izloženost RF-u
