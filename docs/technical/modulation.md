# Modulacija i demodulacija

Svaki radio signal koji čujete ili šaljete — govor, CW tipkanje, FT8 digitalni paket — nosi informaciju zahvaljujući procesu zvanom **modulacija**. Razumijevanje modulacije nije samo teorija; govori vam zašto CW prolazi tamo gdje SSB ne može, zašto FT8 radi pri signalima ispod razine šuma, i zašto koristite USB na 20 m a LSB na 40 m.

## Zašto moduliramo?

Zamislite da pokušavate prenijeti zvuk vašeg glasa (20 Hz – 3 kHz) direktno putem antene. Problem: antena dimenzionirana za takve niske frekvencije bila bi kilometrima duga! Umjesto toga, koristimo **nosioc (carrier)** — visokofrekventni RF signal koji putuje kroz antenski sustav bez problema. Nosioc nosi informaciju "utisnuti" u njega jednom od metoda modulacije.

**Analogija**: Nosioc je kamion, a informacija (zvuk, tekst, podatak) je teret. Kamion zna voziti autocestu (RF spektar), a teret sam ne može.

## Amplitudna modulacija (AM)

### Princip

Amplituda (visina) nosioca se mijenja proporcionalno s audio signalom:

$$ s(t) = [1 + m \cdot x(t)] \cdot A_c \cos(2\pi f_c t) $$

Gdje je:
*   $f_c$ — frekvencija nosioca (carrier)
*   $m$ — indeks modulacije (0–1; m=1 je 100% modulacija)
*   $x(t)$ — modulirajući signal (audio)

### Spektar AM signala

AM signal u frekvencijskom spektru pokazuje **tri komponente**:

*   **Nosioc** ($f_c$): Uvijek prisutan, ne nosi informaciju — čista "potrošnja snage"
*   **Gornji bočni pojas (USB — Upper Sideband)**: $f_c + f_{audio}$
*   **Donji bočni pojas (LSB — Lower Sideband)**: $f_c - f_{audio}$

!!! note "Rasipanje snage u AM"
    U AM signalu, nosioc troši **2/3 ukupne snage** predajnika, ali ne prenosi nikakvu korisnu informaciju. Oba bočna pojasa sadrže iste informacije (zrcalne su kopije). Ovo je razlog zašto je SSB efikasniji.

**Širina pojasa AM**: 6–8 kHz za govorne komunikacije

**Primjena**: AM broadcast (komercijalnie postaje), zrakoplovna komunikacija (118–137 MHz), WAM (Wide AM)

---

## Frekvencijska modulacija (FM)

### Princip

Amplituda nosioca ostaje konstantna, ali **frekvencija** se mijenja proporcionalno s audio signalom:

$$ s(t) = A_c \cos\left[2\pi f_c t + 2\pi k_f \int_0^t x(\tau)\,d\tau\right] $$

**Deviacija ($\Delta f$)**: Maksimalna promjena frekvencije od nosioca:
*   Narrow FM (amaterski VHF/UHF): $\pm 2.5$ kHz
*   Wide FM (broadcast radio): $\pm 75$ kHz

### Carson's rule — širina pojasa FM

$$ BW \approx 2(\Delta f + f_{max}) $$

Za narrow FM s $\Delta f = \pm 5$ kHz i audio do 3 kHz: $BW = 2(5 + 3) = 16$ kHz

### Capture effect

Jedna od prednosti FM: kada dva signala dolaze na istoj frekvenciji, prijemnik "hvata" jači i gotovo potpuno ignorira slabiji (za razliku od AM gdje se miješaju). Rezultat: čist zvuk bez interferencije od slabijih signala.

!!! tip "Kada koristiti FM?"
    FM je idealan za lokalne VHF/UHF veze gdje su signali jaki i kvaliteta zvuka je prioritet. Za DX rad na HF, FM je neučinkovit zbog širine pojasa — koristite SSB.

---

## Single Sideband (SSB)

### Zašto SSB?

SSB nastaje uklanjanjem nosioca i jednog bočnog pojasa iz AM signala. Rezultat:

1.  **Uža širina pojasa**: ~2.7 kHz umjesto 6–8 kHz za AM
2.  **Više snage u korisni signal**: Sva snaga (100 W) ide u informaciju, a ne u nosioc
3.  **Bolji odnos signal/šum**: Na prijemu, ekvivalentno pojačanje od ~9 dB nad AM

!!! example "Usporedba snage"
    100 W AM predajnik:
    - Nosioc: ~67 W (ne prenosi informaciju)
    - Svaki bočni pojas: ~17 W
    
    100 W SSB predajnik:
    - **Sav 100 W (PEP) u jedan bočni pojas** = informacija
    
    SSB je ekvivalentan AM predajniku od 400+ W za isti kvalitativni domet!

### Metode generiranja SSB

*   **Filter metoda**: Audio se modulira na međufrekvenciju (IF), zatim kvarcni filtar reže jedan bočni pojas. Najčešća u tradicionalnim transciverima.
*   **Phasing metoda (SDR)**: Matematički (DSP) poništavanje jednog bočnog pojasa. Koristi se u modernim SDR transciverima.

### USB vs LSB — konvencija

| Opsezi | Mod | Razlog |
|--------|-----|--------|
| 160 m, 80 m, 40 m (< 10 MHz) | **LSB** | Povijesna konvencija |
| 20 m, 17 m, 15 m, 12 m, 10 m (> 10 MHz) | **USB** | Povijesna konvencija |
| VHF, UHF (AM, FM, SSB) | **USB** | Standard |
| Digitalni modovi (FT8, PSK31) | **USB** (uvijek) | Software standard |

**Snaga SSB**: Mjeri se u PEP (Peak Envelope Power) — vršna snaga za trajanja samoglasnika.

---

## CW — Morseov kod (Continuous Wave)

### OOK — On/Off Keying

CW je najjednostavniji modulacijski mod: **nosioc se uključuje i isključuje** prema Morseovom kodu.

$$ s(t) = A_c \cos(2\pi f_c t) \cdot k(t) $$

Gdje je $k(t) = 1$ (uključeno) ili $k(t) = 0$ (isključeno).

### Zašto CW prolazi tamo gdje SSB ne može?

| Karakteristika | CW | SSB | FM |
|---------------|----|----|-----|
| Širina pojasa | 100–500 Hz | 2700 Hz | 12–16 kHz |
| Minimalni SNR za dekodiranje | −30 dB (soft.) / −10 dB (uho) | 0 dB | +5 dB |
| Snaga pri 100 W ERP | 100 W kontinuirano | 100 W (PEP) | 100 W |

**Ključna prednost**: Uzak pojas znači da se unutar jednog SSB kanala od 2.7 kHz može "stati" 5–27 CW stanica istovremeno. Prijemnik koji sluša 100 Hz propusni pojas prima i šum proporcionalno tom uskom pojasu — SNR je dramatično bolji.

!!! note "CW + DSP = rekord"
    Programski CW dekoderi (poput onih u WSJT-X / FT8, ali i CW Skimmer-a) mogu dekodirati CW signale ispod razine šuma koji je nečujno za ljudsko uho. Kombinacija CW modulacije i softverskog dekodiranja postiže SNR prednost od +15 dB nad SSB.

---

## Digitalne modulacije

### FSK — Frequency Shift Keying

Dvije (ili više) diskretne frekvencije predstavljaju digitalne podatke:
*   "Mark" = $f_c + \Delta f$
*   "Space" = $f_c - \Delta f$

Primjena: RTTY (radioteletype) — klasična digitalna komunikacija koja radi na 170 Hz razdvajanju.

### AFSK — Audio Frequency Shift Keying

Zvučna kartica generira audio tonove koji moduliraju SSB predajnik. Radio ne "zna" da prenosi digitalni signal — vidi samo audio.

*   **FT8, JS8Call, PSK31**: Svi koriste AFSK pristup
*   Prednost: Ne treba poseban radio hardware, radi s bilo kojim SSB transcieverom
*   Mana: Linearna karakteristika pojačala je kritična (ALC mora biti isključen ili minimalan)

### PSK — Phase Shift Keying

Faza signala (a ne amplituda ili frekvencija) kodira informaciju. PSK31 koristi BPSK (Binary PSK) s 180° promjenom faze:

$$ s(t) = A_c \cos(2\pi f_c t + \phi(t)) $$

Gdje $\phi(t) \in \{0°, 180°\}$.

*   **PSK31**: 31.25 baud, ~31 Hz širina pojasa — izuzetno uzak!
*   **PSK63**: Dvaput brži, dvaput širi
*   Prednost: Odlična čitljivost pri slabim signalima

### FT8 — 8-FSK digitalna modulacija

FT8 (Franke-Taylor 8-FSK) koristi 8 diskretnih frekvencija u 50 Hz raspon:

*   Svaki simbol kodira 3 bita
*   15-sekundni TX/RX ciklus
*   LDPC forward error correction
*   SNR limit: **−24 dB** (čuje što human uho ne može)

Više detalja na stranici [FT8 praktični vodič](../operating/ft8_guide.md).

---

## Usporedna tablica modulacijskih modova

| Mod | Tip modulacije | Širina pojasa | Min. SNR | Domet (relativno) | Softver |
|-----|---------------|--------------|----------|-------------------|---------|
| **CW** | OOK | 100–500 Hz | −10 dB (uho) | ⭐⭐⭐⭐⭐ | CW Skimmer |
| **SSB** | AM (1 bočni pojas) | 2.7 kHz | 0 dB | ⭐⭐⭐⭐ | — |
| **AM** | Amplitudna | 6–8 kHz | +3 dB | ⭐⭐⭐ | — |
| **FM** | Frekvencijska | 12–16 kHz | +5 dB | ⭐⭐⭐ (lokalno) | — |
| **PSK31** | Fazna BPSK | ~31 Hz | −5 dB | ⭐⭐⭐⭐ | fldigi |
| **FT8** | 8-FSK LDPC | ~50 Hz | −24 dB | ⭐⭐⭐⭐⭐ | WSJT-X |
| **FT4** | 4-FSK LDPC | ~83 Hz | −17 dB | ⭐⭐⭐⭐ | WSJT-X |
| **JS8Call** | 8-FSK | ~50 Hz | −24 dB | ⭐⭐⭐⭐⭐ | JS8Call |
| **WSPR** | 4-FSK | ~6 Hz | −28 dB | ⭐⭐⭐⭐⭐ | WSJT-X (beacon) |
| **RTTY** | AFSK/FSK | 250–500 Hz | 0 dB | ⭐⭐⭐ | fldigi, MMTTY |

---

## Waterfall — vizualizacija signala

Waterfall (vodopad) je frekvencijsko-vremenski prikaz RF spektra. Svaki red (pixel po visini) = trenutak u vremenu; horizontalna osa = frekvencija; boja = jačina signala.

Kako prepoznati modove na waterfallu:

| Mod | Izgled na waterfallu |
|-----|---------------------|
| **CW** | Uska vertikalna crtica, ritmički se uključuje/isključuje |
| **SSB** | Široka "oblak" traka, 2–3 kHz; mijenja oblik s govorom |
| **FM** | Ravnomjerno ispunjen pravokutnik, ~12–16 kHz |
| **PSK31** | Uska okomita crtica, ~31 Hz, kontinuirano |
| **FT8** | Grupirane okomite "crte" u 8 frekvencija, paljenje svakih 15 s |
| **WSPR** | Gotovo nevidljiv, 4 tanka traka, svake 2 minute |
| **RTTY** | Dvije paralelne vertikalne crte, 170 Hz razmak |

!!! tip "Naučite čitati waterfall"
    Waterfall je "rentgen" radijskog spektra. [WebSDR](https://websdr.org) vam omogućava da slušate i gledate waterfall bez ikakvog vlastitog hardvarea. Idealno za učenje prepoznavanja modova!

---

## Demodulacija

Demodulacija je obrnuti proces — iz primljenog RF signala izvlačimo originalnu informaciju.

*   **AM demodulacija**: Envelope detector (dioda + RC filtar) — jednostavno, jeftino
*   **FM demodulacija**: Phase-locked loop (PLL) ili discriminator krug
*   **SSB demodulacija**: Zahtijeva BFO (Beat Frequency Oscillator) — reinjekcija nosioca; zato SSB ne radi na AM radio postajama
*   **Digitalne demodulacija**: DSP algoritmi u zvučnoj kartici — FFT, korelacija, Viterbi dekodiranje

---

## Povezane teme

*   [Modovi rada](../operating/modes.md) — Koji mod za koju situaciju
*   [FT8 praktični vodič](../operating/ft8_guide.md) — Konfiguracija i rad u FT8
*   [Osnove elektronike](electronics.md) — LC krugovi, filtri koji selektiraju modove
*   [Antene i vodovi](antennas.md) — Širina pojasa antene vs. mod
