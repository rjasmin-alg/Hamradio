# CB Propisi i Kanali

CB radio u Europi i Hrvatskoj koristi **40 kanala** u frekvencijskom pojasu 26.965–27.405 MHz. Svaki kanal ima fiksnu frekvenciju — za razliku od radioamaterizma gdje je na raspolaganju cijeli opseg, CB korisnici ne biraju slobodno frekvencije već se drže propisanog rasporeda.

---

## Propisani tehnički parametri (Hrvatska / EU)

| Parametar | Vrijednost |
|---|---|
| Frekvencijski opseg | 26.960 – 27.410 MHz |
| Broj kanala | 40 (standardni europski raspored) |
| Razmak između kanala | 10 kHz |
| Modulacija AM | Dopuštena, max. 4 W nosača (ERP) |
| Modulacija FM | Dopuštena, max. 4 W (ERP) |
| Modulacija SSB | Dopuštena, max. 12 W PEP |
| Antenski dobitak | Nije posebno ograničen, ali uređaj mora biti homologiran |
| Standard | EN 300 433 (EU) |
| Regulatorno tijelo (HR) | HAKOM |
| Dozvola | Nije potrebna (opće odobrenje) |

!!! note "AM vs FM vs SSB — koja modulacija?"
    - **AM** (Amplitude Modulation) je originalna CB modulacija — dobro se probija, kompatibilna sa svim stanicama, ali manje učinkovita (55% snage odlazi u nosač koji ne nosi informaciju)
    - **FM** (Frequency Modulation) je čišća, manje osjetljiva na šum i smetnje — preferirana za lokalni rad
    - **SSB** (Single Sideband) je najučinkovitija — sva snaga ide u govorni signal, dosezi su 2–3× veći. Neophodna za DX rad. Dijeli se na LSB (Lower) i USB (Upper) — LSB je konvencija za CB SSB.

---

## Kompletna tablica 40 kanala

| Kanal | Frekvencija (MHz) | Napomena |
|:---:|:---:|:---|
| 1 | 26.965 | |
| 2 | 26.975 | |
| 3 | 26.985 | |
| 4 | 27.005 | |
| 5 | 27.015 | |
| 6 | 27.025 | |
| 7 | 27.035 | |
| 8 | 27.055 | Alpha kanal (27.045) |
| **9** | **27.065** | **🚨 Hitni kanal (Emergency) — samo za nuždu!** |
| 10 | 27.075 | |
| 11 | 27.085 | |
| 12 | 27.105 | Alpha kanal (27.095) |
| 13 | 27.115 | |
| 14 | 27.125 | |
| 15 | 27.135 | |
| 16 | 27.155 | Alpha kanal (27.145) |
| 17 | 27.165 | |
| 18 | 27.175 | |
| **19** | **27.185** | **🚛 Cesta / Kamiondžije (EU standard)** |
| 20 | 27.205 | Alpha kanal (27.195) |
| 21 | 27.215 | |
| 22 | 27.225 | |
| 23 | 27.255 | Alpha kanal (27.235 i 27.245) |
| 24 | 27.235 | |
| 25 | 27.245 | |
| 26 | 27.265 | |
| 27 | 27.275 | |
| 28 | 27.285 | |
| 29 | 27.295 | |
| 30 | 27.305 | |
| 31 | 27.315 | |
| 32 | 27.325 | |
| 33 | 27.335 | |
| 34 | 27.345 | |
| 35 | 27.355 | |
| 36 | 27.365 | |
| 37 | 27.375 | |
| 38 | 27.385 | SSB kanal (LSB/USB) — DX |
| 39 | 27.395 | SSB kanal — DX |
| 40 | 27.405 | SSB kanal — DX |

---

## Rezervirani i konvencionalni kanali

### Kanal 9 — Hitni kanal 🚨

Kanal 9 (27.065 MHz) je međunarodno prihvaćeni **hitni kanal**. Rezerviran je isključivo za:
- Pozivanje pomoći u nuždi (nesreće, nestajanje u prirodi, kvarovi vozila)
- Komunikaciju s hitnim službama opremljenim CB-om
- Koordinaciju u katastrofama

!!! danger "Kanal 9 nije za razgovore"
    Korištenje kanala 9 za normalne razgovore ili "testiranje opreme" zabranjeno je i nemoralno — netko kome je potrebna pomoć možda ne može doći do frekvencije.

### Kanal 19 — Cesta 🚛

Kanal 19 (27.185 MHz) je europski standard za komunikaciju vozača na autocestama i prometnicama. Na njemu se razmjenjuju:
- Informacije o prometnim uvjetima
- Upozorenja o kontrolama
- Pozivanje i prebjeg na radni kanal

Normalna praksa: **pozivanje na K19, prebacivanje na slobodan kanal za razgovor.**

### Kanali 38–40 — SSB DX

Kanali 38, 39 i 40 su konvencionalni SSB DX kanali. LSB je standard za CB SSB komunikaciju. Na ovim kanalima možete čuti razgovore s operatorima iz cijele Europe.

### Alpha kanali

"Alpha" (ili "A") kanali su međufrekvencije koje australski i američki raspored CB kanala uključuju (npr. 27.045 MHz između kanala 7 i 8). Europski raspored ih ne uključuje kao standardne, ali neke CB postaje mogu imati mogućnost rada na njima.

---

## Zakonski okvir u Hrvatskoj

Korištenje CB radija u Hrvatskoj regulirano je kroz:

- **Zakon o elektroničkim komunikacijama** (ZEK) — NN 73/08 i izmjene
- **Pravilnik o uvjetima i načinu korištenja radijskog spektra** — HAKOM
- Europska odluka **2006/771/EC** i izmjena **2013/752/EU** — harmonizira CB u cijeloj EU

**Ključni propisi:**
1. Uređaji moraju imati **CE oznaku** i biti tipa odobrenih prema EN 300 433
2. Zabranjeno je modificirati ili pojačavati uređaj izvan propisanih snaga
3. Zabranjeno je ometanje hitnih komunikacija (Kanal 9)
4. Zabranjeno je emitiranje glazbe, reklama ili sadržaja koji remete komunikaciju

!!! warning "Pojačala (linear amplifiers) su ilegalna"
    Pojačala koja podižu CB snagu iznad 4 W (AM/FM) ili 12 W (SSB) su **ilegalna** u EU i HR. HAKOM provodi inspekcije i može:
    - Izreći novčanu kaznu
    - Oduzeti opremu
    - Pokrenuti kazneni postupak za namjerno ometanje komunikacija

---

## Međunarodne razlike

CB raspored kanala nije potpuno unificiran — postoje razlike između regija:

| Regija | Standard | Napomena |
|---|---|---|
| Europa (EU) | CEPT, 40 kanala | Frekvencijski raspored identičan, FM dominira |
| USA | FCC, 40 kanala | Isti raspored, AM dominantniji, snaga ista |
| Australija | ACMA, 40 kanala | Malo drugačiji raspored + alpha kanali |
| Japan | MIC, 40 kanala | Potpuno drugačiji raspored i snaga |

Za internacionalnu DX komunikaciju na CB-u, SSB na kanalima 38–40 je de facto standard između europskih operatora.

---

## Povezane teme

- [CB oprema](equipment.md) — kako odabrati stanicu i antenu
- [Uvod u CB](intro.md) — povijest i propisi šire
- [Propagacija radio valova](../technical/propagation.md) — zašto CB DX funkcionira samo povremeno
- [Frekvencijski planovi](../operating/bandplans.md) — usporedba s amaterskim planovima
