# Osnove elektronike

Razumijevanje elektronike je temelj za svakog radioamatera. Bez poznavanja osnovnih komponenti i zakona, teško je shvatiti zašto antena treba biti određene duljine, što znači impedancija od 50 Ω, ili kako radio pretposilje signal u etar. Ova stranica objašnjava elektroniku na praktičan način — kao što bi iskusni OM objasnio kolegi uz kavu.

## Osnovne komponente

### Otpornik (Resistor)

![Otpornik](https://upload.wikimedia.org/wikipedia/commons/e/e5/Resistors-photo.jpg)

Ograničava tok električne struje. Zamislite ga kao suženje cijevi kroz koju teče voda — što je uže, to manje vode (struje) prolazi.

*   **Jedinica**: Ohm ($\Omega$)
*   **Oznaka**: $R$
*   **Primjena**: Prilagodba napona, ograničavanje struje LED dioda, dijelila napona
*   [**Video: Kako radi otpornik (Engineering Mindset)**](https://www.youtube.com/results?search_query=how+resistors+work+engineering+mindset)

---

### Kondenzator (Capacitor)

![Kondenzator](https://upload.wikimedia.org/wikipedia/commons/b/b9/Capacitors_%287189597135%29.jpg)

Pohranjuje električnu energiju u električnom polju između dvije ploče. Radi kao mala baterija koja se može jako brzo puniti i prazniti — u RF tehnici to je ključna osobina.

*   **Jedinica**: Farad ($F$) — u praksi se koriste $\mu F$, $nF$, $pF$.
*   **Oznaka**: $C$
*   **Primjena**: Filtriranje napona ("peglanje" šuma), titrajni krugovi, blokiranje istosmjerne struje na ulazu pojačala
*   [**Video: Kako radi kondenzator**](https://www.youtube.com/results?search_query=how+capacitors+work+engineering+mindset)

---

### Zavojnica (Inductor)

![Zavojnica](https://upload.wikimedia.org/wikipedia/commons/9/94/Inductor_coils.jpg)

Pohranjuje energiju u magnetskom polju. Opire se svakoj *promjeni* struje — što je promjena brža (viša frekvencija), to je veći otpor. Zato je ključna komponenta u RF filterima i antenskima balunima.

*   **Jedinica**: Henry ($H$) — najčešće $\mu H$, $mH$.
*   **Oznaka**: $L$
*   **Primjena**: Titrajni krugovi, prigušnice (blokiranje RF signala na napajanju), transformatori, baluni
*   [**Video: Kako radi zavojnica**](https://www.youtube.com/results?search_query=how+inductors+work+engineering+mindset)

---

### Poluvodiči

#### Dioda

![Dioda](https://upload.wikimedia.org/wikipedia/commons/c/cc/Diode-closeup.jpg)

Elektronički nepovratni ventil. Propušta struju samo u jednom smjeru (od anode prema katodi). Ključna je u ispravljačima napajanja i RF detektorima.

*   **Oznaka**: $D$
*   **Primjena**: Ispravljanje izmjenične struje (napajanja), detekcija AM signala, zaštita od obrnutog polariteta

#### Zener dioda

Posebna vrsta diode koja propušta struju u oba smjera, ali u obrnutom smjeru **tek od određenog napona** (Zener napon). Koristi se za stabilizaciju napona u napajanjima.

!!! example "Primjer: Zener stabilizator"
    Zener dioda s naponom $V_Z = 5.1\,V$ u obrnutom smjeru će uvijek "prikovati" napon na 5.1 V bez obzira na ulazni napon (koji mora biti viši). Idealna za referentne napone.

#### Tranzistor (BJT)

![Tranzistor](https://upload.wikimedia.org/wikipedia/commons/2/23/Transistors-white.jpg)

Bipolarni tranzistor (BJT — Bipolar Junction Transistor) je aktivna komponenta s tri nožice: **Baza (B)**, **Kolektor (C)** i **Emiter (E)**. Mali strujni signal na bazi kontrolira puno veću struju između kolektora i emitera.

*   **Analogija**: Slavina — mali okret ručke (baza) kontrolira veliki protok vode (C→E).
*   **Pojačanje**: Karakterizira ga faktor $\beta$ (beta ili $h_{FE}$) koji govori koliko puta se struja pojačava.
*   **Primjena**: Pojačala audio i RF signala, oscilatori, digitalni prekidači (u logičkim sklopovima).

#### MOSFET

MOSFET (Metal-Oxide-Semiconductor Field-Effect Transistor) kontrolira struju **naponom** (ne strujom kao BJT). Ima tri nožice: **Gate (G)**, **Drain (D)** i **Source (S)**.

*   **Prednosti**: Izuzetno mala ulazna struja (gotovo nula), brzo prebacivanje
*   **Primjena u RF**: Gotovo sva moderna pojačala snage (PA) u transcieverima koriste RF MOSFET-ove (npr. RD100HHF1)
*   **Primjena u napajanjima**: Switching regulatori (SMPS), kontrola baterija

---

## Ohmov zakon

Temeljni zakon elektrotehnike koji opisuje odnos između napona, struje i otpora. Vrijedi za istosmjerne (DC) krugove.

$$ I = \frac{U}{R} $$

Gdje je:
*   $I$ = Struja (Amper — $A$)
*   $U$ = Napon (Volt — $V$)
*   $R$ = Otpor (Ohm — $\Omega$)

!!! tip "Mnemonička formula"
    Zapamtite "URI" trokut: pokrijte veličinu koju tražite, a ostatak pokazuje računicu. Tražite I? Pokrijte I → ostaje U/R.

## Snaga

$$ P = U \cdot I = I^2 \cdot R = \frac{U^2}{R} $$

*   $P$ = Snaga (Watt — $W$)

!!! warning "Snaga u otporniku = toplina"
    Otpornik koji disipira previše snage se pregrije i izgori. Uvijek koristite otpornik s dvostruko većom snagnom od izračunate (safety margin). Otpornik od $\frac{1}{4}W$ koji disipira $0.5W$ će se dimiti!

---

## Serijski i paralelni spojevi

Da bismo dobili željenu vrijednost električnih karakteristika, komponente se mogu povezivati na dva osnovna načina: serijski i paralelno.

### Otpornici u serijskom spoju

U serijskom spoju ista struja teče kroz svaki otpornik. Ukupni otpor je zbroj svih:

$$ R_{uk} = R_1 + R_2 + \ldots + R_n $$

### Otpornici u paralelnom spoju

Ovdje se napon dijeli jednako, ali struja se dijeli po granama. Ukupni otpor je uvijek **manji** od najmanjeg otpornika:

$$ \frac{1}{R_{uk}} = \frac{1}{R_1} + \frac{1}{R_2} + \ldots $$

Za dva otpornika: $R_{uk} = \frac{R_1 \cdot R_2}{R_1 + R_2}$

### Kondenzatori — obrnuta logika

Kondenzatori se ponašaju suprotno od otpornika!

*   **Paralelno**: Kapaciteti se zbrajaju — $C_{uk} = C_1 + C_2 + \ldots$
*   **Serijski**: Kapaciteti se "dijele" — $\frac{1}{C_{uk}} = \frac{1}{C_1} + \frac{1}{C_2} + \ldots$

!!! example "Praktični račun"
    Imate dva otpornika $R_1 = 100\,\Omega$ i $R_2 = 100\,\Omega$:
    
    - **Serijski**: $R_{uk} = 100 + 100 = 200\,\Omega$
    - **Paralelno**: $R_{uk} = \frac{100 \cdot 100}{100 + 100} = \frac{10000}{200} = 50\,\Omega$
    
    Paralelni spoj uvijek daje otpor manji od najmanjeg otpornika!

---

## Izmjenična struja (AC) naspram Istosmjerne (DC)

Radioamateri rade isključivo s izmjeničnim (AC) signalima u RF spektru. Važno je razumjeti razliku.

*   **DC (Direct Current — Istosmjerna struja)**: Elektroni teku uvijek u jednom smjeru. Baterije, punjači. Primjer: 13.8 V napajanje vaše radiostanice.
*   **AC (Alternating Current — Izmjenična struja)**: Elektroni neprestano mijenjaju smjer. Gradska mreža (230 V / 50 Hz), ali i svaki RF signal.

### Ključni pojmovi AC signala

| Pojam | Opis | Formula |
|-------|------|---------|
| **Frekvencija ($f$)** | Broj punih ciklusa u sekundi; mjeri se u Hertzima (Hz) | $f = \frac{1}{T}$ |
| **Period ($T$)** | Trajanje jednog punog ciklusa | $T = \frac{1}{f}$ |
| **Amplituda** | Vršna vrijednost napona ili struje | — |
| **RMS vrijednost** | Efektivna vrijednost — ekvivalent DC napona iste snage grijanja | $U_{RMS} = \frac{U_{peak}}{\sqrt{2}}$ |

!!! note "Zašto RMS?"
    Kada kažemo da mreža ima 230 V, to je RMS vrijednost. Vršni napon je zapravo $230 \times \sqrt{2} \approx 325\,V$! RMS je koristan jer direktno daje snagu:  $P = U_{RMS} \cdot I_{RMS}$.

---

## Reaktancija i impedancija

### Reaktancija

Kada kroz zavojnicu ili kondenzator teče izmjenična struja, javljaju se "otpori" koji ovise o frekvenciji. Ti "frekvencijsko-ovisni otpori" zovu se **reaktancija**.

**Kapacitivna reaktancija ($X_C$)** — kondenzator se opire niskim frekvencijama, propušta visoke:

$$ X_C = \frac{1}{2\pi f C} $$

**Induktivna reaktancija ($X_L$)** — zavojnica se opire visokim frekvencijama, propušta niske:

$$ X_L = 2\pi f L $$

!!! tip "Korisna intuicija"
    - Kondenzator = "blokator DC, propušta RF" → koristi se za odvajanje stupnjeva pojačala
    - Zavojnica = "propušta DC, blokira RF" → koristi se u napajanjima za "peglanje"

### Impedancija — kompleksni otpor

Impedancija ($Z$) je ukupni "otpor" AC kruga koji uključuje i "pravi" otpor R i reaktanciju X:

$$ Z = R + jX $$

ili po apsolutnoj vrijednosti:

$$ |Z| = \sqrt{R^2 + X^2} $$

Gdje je $j$ imaginarna jedinica ($j = \sqrt{-1}$). Impedancija se prikazuje kao vektor u kompleksnoj ravnini:
*   Osa X (realna) = otpor R
*   Osa Y (imaginarna) = reaktancija X (pozitivna = induktivna, negativna = kapacitivna)

!!! note "Zašto je 50 Ω standard?"
    Sve radioamaterske antene, koaksijalni kabeli i transciever izlazi su 50 Ω. Ovaj kompromisni broj je odabran jer daje dobru ravnotežu između gubitaka u kabelu i maksimalne prenesene snage. Kada impedancija izvora i tereta nisu jednake, dolazi do refleksije signala — to je SWR! Više na stranici [Antene i vodovi](antennas.md).

---

## LC titrajni krug

Zavojnica (L) i kondenzator (C) zajedno čine **titrajni krug** — električki ekvivalent klatna. Kondenzator se "puni" a zatim "prazni" kroz zavojnicu koja taj impuls "vraća" natrag. Energija se neprestano izmjenjuje između električnog i magnetskog polja.

Na točno određenoj frekvenciji — **rezonantnoj frekvenciji** — $X_L = X_C$ pa se reaktancije poništavaju i krug nudi minimalan otpor. To je Thomsonova formula:

$$ f_r = \frac{1}{2\pi\sqrt{LC}} $$

### Faktor dobrote (Q)

Q faktor govori koliko "oštro" titrajni krug reagira na rezonantnu frekvenciju:

$$ Q = \frac{f_r}{\Delta f} = \frac{X_L}{R} $$

Gdje je $\Delta f$ širina pojasa. Viši Q znači uži, oštriji propusni pojas.

| Q faktor | Karakteristika | Primjena |
|----------|---------------|---------|
| Q < 10 | Širok pojasni propusnik | Pojačala s dobrim odzivom |
| Q = 10–100 | Selektivni filter | Bandpass filteri prijemnika |
| Q > 100 | Uski, oscilator | Kvarcni oscilatori (Q > 10 000!) |

!!! tip "Online laboratorij"
    Isprobajte LC titrajni krug bez kupnje komponenti: [**Falstad RLC Simulator**](https://www.falstad.com/circuit/e-rlc.html) — vidjet ćete sinusoidu i kako Q mijenja oblik rezonancije!

---

## Transformatori

Rade isključivo s izmjeničnom strujom (AC) na principu **magnetske indukcije**. Primarna zavojnica stvara magnetsko polje koje inducira napon u sekundarnoj — bez fizičkog kontakta vodiča.

**Omjer namotaja i napona:**

$$ \frac{U_1}{U_2} = \frac{N_1}{N_2} $$

Gdje su $N_1$ i $N_2$ broj navoja primarne i sekundarne zavojnice. Ako je $N_1 = 100$ i $N_2 = 10$, napon se smanjuje 10 puta (transformator pada napona).

**Snaga se čuva** (idealni transformator):

$$ U_1 \cdot I_1 = U_2 \cdot I_2 $$

Ako napon pada 10x, struja raste 10x.

### Transformatori u RF — Balun i Unun

U radioamaterizmu su posebno važni **balun** (BALanced-UNbalanced) transformatori koji pretvaraju neuravnoteženi koaksijalni kabel u uravnoteženu antenu (dipol). Bez baluna teku RF struje po plaštu kabela što uzrokuje TVI i šum. Više na stranici [Antene i vodovi](antennas.md).

!!! note "Galvanska izolacija"
    Transformator pruža galvansku izolaciju — napon se prenosi magnetski, ali metalne niti primarne i sekundarne zavojnice se ne dodiruju. Ovo štiti od strujnog udara pri kvaru. Detalji na stranici [Sigurnost](safety.md).

---

## Čitanje elektroničkih shema

Kada gradite QRP opremu ili popravite transciever, morat ćete čitati sheme. Simboli su standardizirani (IEC i ANSI):

| Simbol | Naziv | Funkcija |
|--------|-------|---------|
| Cik-cak linija (IEC: pravokutnik) | Otpornik | Ograničava struju |
| Dvije paralelne crte | Kondenzator | Pohrana naboja, blokiranje DC |
| Spiralna linija | Zavojnica | Pohrana mag. energije, blokiranje RF |
| Trokut s crticom | Dioda | Jednosmjerni propusnik struje |
| Krug s tri izvoda | Tranzistor BJT | Pojačalo, prekidač |
| Krug s G, D, S izvodima | MOSFET | RF pojačalo, prekidač |
| Tri opadajuće vodoravne crte | Masa (GND) | Referentna točka 0 V |
| Strelica s crtom | Naponski izvor (DC) | Napajanje |
| Kružnica s valnim znakom | Izvor AC signala | Generator signala |

!!! tip "Online alat za sheme"
    [**Falstad Circuit Simulator**](https://www.falstad.com/circuit/) — crtajte i simulirajte sheme direktno u pregledniku. Idealan za razumijevanje kako radi svaki spoj.

---

## Praktični primjeri s MathJax

### Izračun otpornika za LED

LED dioda zahtijeva ograničenje struje — bez otpornika bi izgorjela u sekundama.

**Zadatak**: Napajanje $V_S = 5\,V$, LED pada napona $V_F = 2\,V$, radna struja $I_F = 20\,mA$

**Rješenje:**

Pad napona na otporniku:
$$ V_R = V_S - V_F = 5\,V - 2\,V = 3\,V $$

Potrebni otpor:
$$ R = \frac{V_R}{I_F} = \frac{3\,V}{0.02\,A} = 150\,\Omega $$

Snaga u otporniku:
$$ P = V_R \cdot I_F = 3\,V \cdot 0.02\,A = 0.06\,W = 60\,mW $$

Koristite otpornik $150\,\Omega$, $\frac{1}{4}W$ — s dovoljno rezerve.

### Dijelilo napona (Voltage Divider)

Spoj dva otpornika kojima "uzimamo" dio napona sa čvora između njih:

$$ V_{out} = V_{in} \cdot \frac{R_2}{R_1 + R_2} $$

!!! example "Primjer S-metar u prijemniku"
    Potreban napon $V_{out} = 2\,V$ iz $V_{in} = 5\,V$. Biramo $R_2 = 200\,\Omega$:
    
    $2\,V = 5\,V \cdot \frac{200}{R_1 + 200}$ → $R_1 + 200 = 500$ → $R_1 = 300\,\Omega$
    
    Standardne vrijednosti: $R_1 = 300\,\Omega$, $R_2 = 200\,\Omega$. ✓

### Rezonantna frekvencija LC kruga

**Zadatak**: Izračunajte rezonantnu frekvenciju za $L = 10\,\mu H$ i $C = 100\,pF$.

$$ f_r = \frac{1}{2\pi\sqrt{LC}} = \frac{1}{2\pi\sqrt{10 \times 10^{-6} \cdot 100 \times 10^{-12}}} $$

$$ f_r = \frac{1}{2\pi\sqrt{10^{-15}}} = \frac{1}{2\pi \cdot 3.162 \times 10^{-8}} \approx 5.03\,MHz $$

Ovaj krug rezonira na 5 MHz — unutar 60-metarskog opsega!

---

## Boja kod otpornika

Mali otpornici nemaju dovoljno mjesta za ispisivanje vrijednosti, pa se koriste obojene pruge:

| Boja | Znamenka | Množitelj | Tolerancija |
|------|----------|-----------|-------------|
| Crna | 0 | × 1 | — |
| Smeđa | 1 | × 10 | ±1% |
| Crvena | 2 | × 100 | ±2% |
| Narančasta | 3 | × 1 k | — |
| Žuta | 4 | × 10 k | — |
| Zelena | 5 | × 100 k | ±0.5% |
| Plava | 6 | × 1 M | ±0.25% |
| Ljubičasta | 7 | × 10 M | ±0.1% |
| Siva | 8 | × 100 M | ±0.05% |
| Bijela | 9 | — | — |
| Zlatna | — | × 0.1 | ±5% |
| Srebrna | — | × 0.01 | ±10% |

**Čitanje 4-prstenastog otpornika**: Prve dvije pruge = znamenke, treća = množitelj, četvrta = tolerancija.

!!! example "Primjer čitanja"
    Pruge: Žuta — Ljubičasta — Crvena — Zlatna
    → 4, 7, × 100, ±5%
    → **4700 Ω = 4.7 kΩ ±5%**

!!! tip "Online kalkulator"
    Ne morate pamtiti tablicu napamet: [**Resistor Color Code Calculator**](https://www.digikey.com/en/resources/conversion-calculators/conversion-calculator-resistor-color-code) — unesite boje i dobijte vrijednost.

---

## Resursi za učenje

### Simulatori krugova
*   [**Falstad Circuit Simulator**](https://www.falstad.com/circuit/) — Animirani prikaz toka struje u realnom vremenu. Idealan za početnike.
*   [**Tinkercad Circuits**](https://www.tinkercad.com/circuits) — Virtualni breadboard s Arduino podrškom.
*   [**CircuitLab**](https://www.circuitlab.com/) — Profesionalni online simulator s SPICE analizom.

### Video lekcije (YouTube)
*   [**EEVblog (Dave Jones)**](https://www.youtube.com/user/EEVblog) — Dubinske analize, "teardown" videa, mjeriteljstvo.
*   [**W2AEW**](https://www.youtube.com/user/w2aew) — Odlična objašnjenja RF elektronike specifična za radioamatere.
*   [**The Signal Path**](https://www.youtube.com/user/TheSignalPathBlog) — Napredna RF mjerenja i popravci profesionalne opreme.

### Pisani resursi
*   [**All About Circuits**](https://www.allaboutcircuits.com/) — Besplatan online udžbenik elektrotehnike.
*   [**Electronics Tutorials**](https://www.electronics-tutorials.ws/) — Detaljni vodiči za svaku komponentu.
*   [**ARRL Handbook**](https://www.arrl.org/arrl-handbook-2024) — Biblija radioamatera, poglavlja o elektronici.

---

## Povezane teme

*   [Antene i vodovi](antennas.md) — Impedancija antene, baluni, prilagodba
*   [Modulacija i demodulacija](modulation.md) — Kako LC krugovi filtriraju signale
*   [Sigurnost](safety.md) — Opasnosti visokih napona, zaštita od strujnog udara
*   [Uzemljenje i zaštita](grounding.md) — RF uzemljenje i zaštita opreme
