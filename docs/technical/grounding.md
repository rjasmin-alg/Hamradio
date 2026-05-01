# Uzemljenje i zaštita od groma

Uzemljenje je jedna od tema koje izazivaju najveću zabunu u radioamaterskim krugovima — zato što **postoje tri potpuno različite vrste uzemljenja** s različitim svrhama, i njihovo miješanje uzrokuje probleme od zujanja do požara.

!!! danger "Tri različita uzemljenja"
    RF uzemljenje, sigurnosno uzemljenje i gromobransko uzemljenje su **tri neovisna koncepta**. Svaki ima drugačiju svrhu i drugačiju izvedbu. Pogrešno miješanje može biti opasno.

---

## Tri vrste uzemljenja

### 1. RF uzemljenje

**Svrha**: Pruža referentni potencijal (masu) za RF signale — posebno važno za asimetrične antene (vertikale, end-fed).

**Princip**: Struja RF signala teče iz antene, kroz uređaj, i mora se "vratiti" negdje. Bez RF uzemljenja, struja se vraća plaštem koaksijalnog kabela — što uzrokuje emisiju RF iz kabela unutar kuće (TVI, RFI, šum).

**Izvedba**:
*   Horizontalne bakrene žice (radijali) na tlu ili unutar tla za vertikalne antene
*   Kratka, ravna veza na zajednički SPG (Single Point Ground) u stanici
*   Koaksijalni kabel s ferritnim torusom na ulazu u kuću

**Što RF uzemljenje NE radi**: Ne štiti od munje. Ne sprječava strujni udar od 230 V napajanja.

---

### 2. Sigurnosno (zaštitno) uzemljenje

**Svrha**: Zaštita od strujnog udara pri kvaru opreme. Zakonski obavezno.

**Princip**: Ako dođe do kratkog spoja unutar uređaja (npr. faza na kućištu), struja teče kroz zaštitni vodič (PE — Protective Earth) u masu, aktivira osigurač i prekida napajanje — umjesto da teče kroz operatora.

**Izvedba**:
*   Žuto-zeleni kabel u Schuko utičnicama
*   Svaki uređaj s metalnim kućištem mora biti priključen na PE
*   Zajednička PE šina u razvodniku sobe

**Standardi**: IEC 60364, EN 61140 — obvezni u svim EU zemljama.

!!! note "Kabel boje"
    - Žuto-zelena pruga = PE (Protective Earth / zaštitno uzemljenje)
    - Plava = N (neutralni vodič)
    - Smeđa/crna = L (fazni vodič, "faza")
    
    Nikada ne koristite zaštitni vodič za "normalni" povrat struje — to je zakonski prekršaj i opasnost.

---

### 3. Gromobransko uzemljenje

**Svrha**: Odvođenje energije munje bezopasno u tlo. Onemogućuje oštećenje opreme od induciranih prenapona.

**Princip**: Munja nosi stotine tisuća ampera u mikrosekundnom pulsu. Sustav mora pružiti minimalni otpor putu do tla — daleko od opreme.

**Izvedba**:
*   Čelična ili bakrena šipka promjera ≥16 mm, ukopana ≥2 m u vlažno tlo
*   Masivni bakreni vodič (≥16 mm²) koji spaja antenu/odvodnik s uzemljem
*   Prenaponski odvodnici (SPD) na ulazu kabela u kuću

**Što gromobransko uzemljenje NE garantira**: Potpunu zaštitu od direktnog udara munje. Direktan udar razvija nekoliko milijuna volti — nijedno uzemljenje ne može to "apsorbirati" bez oštećenja.

!!! danger "JEDINA prava zaštita od munje"
    Fizički isključite antenu iz uređaja i izvucite kabel iz prostorije **čim zabrundite grmljavinu**. Niti jedan odvodnik nije zamjena za ovo.

---

## Single Point Ground (SPG) — ključni koncept

SPG je temeljna tehnika za radioamatersku stanicu: **sve mase se spajaju na jednu jedinu točku** (bakrena šina), a ta točka ide ravnom, kratkom vezom na uzemljenje.

### Zašto SPG?

Zamislite munju koja udari u vašu antenu i induktivno unese 10.000 V u koaksijalni kabel. Bez SPG:
*   Kabel donese 10.000 V do transciivera
*   Drugi kabel (USB, audio) donese 0 V do računala
*   Razlika: 10.000 V — iskri između uređaja i uništava sve

S SPG:
*   Munja podiže potencijal SPG šine za 10.000 V
*   **Sva oprema spojena na tu šinu podiže se istovremeno za 10.000 V**
*   Razlika između uređaja: 0 V — nema iskre, nema oštećenja

!!! example "Vizualizacija SPG"
    Zamislite sve uređaje kao objekte na mreži. Bez SPG, mreža je šarena — svaki uređaj visoko na različitoj razini. S munjom, razlike uzrokuju iskre. 
    
    S SPG: sva mreža se pomiče gore i dolje zajedno, kao jedan brod na valu — razlika između brodskih elemenata ostaje nula.

### Zemne petlje (Ground Loops) — najveći neprijatelj

Zemna petlja nastaje kada postoji **dva ili više puta između mase jednog uređaja i mase drugog**. Svaka petlja djeluje kao antena koja prikuplja elektromagnetske smetnje.

Simptomi zemne petlje:
*   50 Hz ili 100 Hz zujanje u audio signalu ("brum")
*   RF QRM koji se mijenja ovisno o položaju kabela
*   "Šum" proporcionalan snazi gradske elektrane

**Rješenje**: Sve mase voditi prema centru (SPG) kao zvijezda — ne kao prsten ili petlja!

---

## Radijali — RF uzemljenje vertikalnih antena

Vertikalna antena je u osnovi pola dipola — gornji krak je žica koja ide prema nebu, a donji krak mora biti "zemlja". Problem: stvarna zemlja loš je vodič RF struje (gubici u tlu).

Radijali su horizontalne žice rasprostrijete na tlu ili zakopane plitko, koje tvore "elektricni odraz" koji anteni simulira drugu polovicu dipola.

### Koliko radijala?

| Broj radijala | Dobit antene | Smanjenje gubitaka |
|---------------|-------------|---------------------|
| 0 (bez radijala) | Loše (−10 dB ili više) | Osnova |
| 4 radijala | Prihvatljivo | +6 dB |
| 16 radijala | Dobro | +9 dB |
| 32 radijala | Izvrsno | +10 dB |
| 120 radijala | Maksimum | +11 dB |

**Preporuka**: Minimum **16 radijala** duljine $\lambda/4$ za operativni rad. Svaki dodatni radijal poboljšava, ali s opadajućim prinosom.

### Duljina radijala

Optimalna duljina jednog radijala: $L = \frac{71.5}{f_{MHz}}$ metara ($\lambda/4$)

Za 40 m opseg (7 MHz): $L = \frac{71.5}{7} \approx 10.2 \, \text{m}$

!!! tip "Zakopani vs. na površini"
    Istraživanja pokazuju da su zakopani radijali i radijali na površini gotovo jednako efikasni. Radijali na površini su lakši za postavljanje i provjeru, ali zahtijevaju zaštitu od lawnmowera. Zakopani (5–10 cm dubine) estetski su prihvatljiviji.

### Counterpoise

Za prijenosne postaje bez mogućnosti polaganja radijala (balkon, krov):

*   Duga žica (minimalno $\lambda/4$) obješena prema dolje ili horizontalno
*   Ne mora biti baš $\lambda/4$ — svaka duljina pomaže u odnosu na ništa
*   Može se koristiti i metalična oluka, ograda ili krovni lim kao counterpoise

---

## Zaštita od groma — sustav odvodnika

Odvodnici prenapona (SPD — Surge Protection Devices) su "sigurnosni ventili" koji se aktiviraju pri prenaponu i odvedu energiju u uzemljenje.

### Vrste odvodnika

| Vrsta | Naziv | Reakcijsko vrijeme | Max. energija | Primjena |
|-------|-------|-------------------|---------------|---------|
| **GDT** | Gas Discharge Tube | 100–500 ns | Visoka | Koaksijalni kabel, glavna zaštita |
| **MOV** | Metal Oxide Varistor | 1–50 ns | Srednja | Brza zaštita 230 V |
| **TVS** | Transient Voltage Suppressor | < 1 ns | Niska | Elektronički sklopovi |
| **Polyphaser** | Kombinirana rješenja | < 1 ns | Visoka | Profesionalna izvedba za antene |

### Pozicija montaže odvodnika

!!! warning "Montaža odvodnika — kritično"
    Odvodnik mora biti montiran **IZVAN kuće, na ulazu kabela kroz zid ili prozor**, a ne blizu uređaja. Kada se aktivira, oslobađa energiju u tlo. Ako je montiran u sobi — ispreči radni stol!

Preporučeni redoslijed za koaksijalni kabel:
```
Antena → [Koaks] → [Odvodnik na zidu, s kratkim izvodom na PE/SPG] → [Koaks] → Transciiver
```

### Statički elektricitet

Antene skupljaju statički elektricitet, posebno pri suhom vjetru. GDT odvodnik koji se aktivira pri nekoliko stotina volti štiti ulazni LNA tranzistor prijemnika.

Za SDR prijemnike i osjetljive prijemnike: GDT odvodnik na ulazu je obavezan ako je antena na krovu.

---

## Praktični vodič: Postavljanje SPG sustava

### Materijali
*   Bakrena šina (busbar) 40×5 mm, duljina ~50 cm
*   Bakreni vodič 16 mm² (za veze do uzemljenja)
*   Bakrena šipka za uzemljenje: ⌀16 mm, duljina 2 m
*   Odvodnik prenapona za koaksijalni kabel (tip N ili PL-259)
*   Kratki vodovi (< 30 cm) od uređaja do šine

### Korak po korak

**Korak 1**: Postavite bakrenu šinu na zid blizu prozora/ulaska kabela u sobu. Ovo je SPG točka.

**Korak 2**: Izvan kuće, montirajte odvodnik na ulazu koaksijalnog kabela. Povežite kućište odvodnika kratkim debeli vodičem (≥10 mm²) na SPG šinu ili direktno na gromobranske uzemljenje.

**Korak 3**: Uzemljenje — debeli vodič (≥16 mm²) od SPG šine, ravno (bez ostrih zavoja) do vanjskog uzemljenja. Zabijte šipku u vlažno tlo ≥2 m dubine.

**Korak 4**: Povežite sve uređaje kratkim (< 30 cm) žicama na SPG šinu:
*   Kućište transciivera
*   Kućište računala
*   Kućište SWR metra
*   Kućište antena switchera

**Korak 5**: Sve napajanje iz iste utičnice (iste faze) — smanjuje mogućnost ground loop-a.

!!! tip "Mjerenje kvalitete uzemljenja"
    NanoVNA ili multimetar može izmjeriti otpor prema tlu. Cilj je < 10 Ω od SPG šine do tla. Za gromobransko uzemljenje, standard je < 5 Ω (ili < 1 Ω za kritične instalacije).

---

## Česte greške i rješenja

| Greška | Simptomi | Rješenje |
|--------|---------|---------|
| Nema radijala na vertikali | Loše zračenje, visoki SWR | Dodajte minimalno 4×λ/4 radijala |
| Zemna petlja (ground loop) | 50 Hz zujanje u audio | Svi kablovi na isti SPG čvor |
| Dugi vodič do uzemljenja | Slaba zaštita pri grmljavini | Skratite; ravni kratki put je ključan |
| Odvodnik blizu uređaja | Šteta pri aktiviranju | Premjestite na ulaz u kuću |
| Nema ferrita na kabelu | RF struje na plaštu | Dodajte ferritor (FT-240-43, 8–10 okretaja) |
| Miješanje vrsta uzemljenja | Zujanje ili loša zaštita | Jasno odvojite RF, PE i gromobranski sustav |

---

## Resursi

*   [**Lightning Protection for the Amateur Station — ARRL**](https://www.arrl.org/lightning-protection) — Detaljan vodič za zaštitu
*   [**Polyphaser IS-B50LN-C2**](https://www.polyphaser.com) — Profesionalni odvodnik za koaksijalni kabel
*   [**ON4UN's Low Band DXing**](https://www.qsl.net/on4un/) — Poglavlje o RF uzemljenju i radijalima

---

## Povezane teme

*   [Sigurnost](safety.md) — Opasnosti visokih napona i električna sigurnost
*   [Antene i vodovi](antennas.md) — Balun, vertikalne antene i radijali
*   [Osnove elektronike](electronics.md) — Impedancija, kondenzatori i visokonaponska tehnika
