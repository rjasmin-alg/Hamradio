# Softver za radioamatere

## Uvod
U modernom radioamaterizmu računalo je postalo neodvojivi dio amaterske radio postaje (shack-a). Od vođenja dnevnika veza koji nam omogućavaju lakšu analizu i razmjenu potvrda, preko digitalnih modova do softverski definiranih radija (SDR), softver je jednako važan kao i primopredajnik ili antena. Korištenje računala ne olakšava samo svakodnevni rad i administraciju, nego i proširuje horizonte eksperimentiranja.

## Kako koristiti ovaj popis
Ovaj iscrpan popis sadrži brojne alate, no mi preporučujemo usredotočiti se prvo na osnove, stoga evo onoga što čini "Starter Pack":
- **WSJT-X**: Apsolutni standard za FT8/FT4 digitalne modove.
- **Log4OM v2**: Vrlo dobar i besplatan alat za Windows s odličnom integracijom, najbolji generalni logging alat.
- **MMANA-GAL**: Jedan od najboljih početnih alata za dizajniranje i modeliranje kratkovalnih žičanih antena.
- **HamAlert**: Ključan mobilni alat za praćenje propagacije i spotova.
- **LCWO.net**: Najbolji web alat za ovladavanje telegrafijom (CW).

!!! tip "Preporučena lista za početnike"
    Preuzimanjem ovog "Starter packa" prekrit ćete većinu zahtjeva za početak rada na frekvencijama, vođenje dnevnika te testiranje prvih digitalnih modova. U kombinaciji s ovladavanjem telegrafijom kroz *LCWO*, imate odličan start!

!!! note "O licencama"
    Prilikom instalacije softvera, uvijek provjerite točno kakva prava pruža licenca. Mnogo sjajnog softvera pružen je pod opensource, free ili donationware licencama, no postoje komercijalna rješenja sa znatnijim naknadama koja mogu pružiti više tehničke podrške za složen(iji) setup.

---

## Logiranje
Dnevnik veza (logbook) središnji je softver svake postaje. S njim osiguravamo sigurno i pregledno spremanje kontakata.

| Naziv | Link | Opis (HR) | Platforma | Cijena | Preporučeno za |
|-------|------|-----------|-----------|--------|----------------|
| N1MM+ | [n1mm.hamdocs.com](https://n1mm.hamdocs.com) | Vodeći svjetski logger za takmičenja (contesting). | Windows | Besplatno | Contesteri, sportski radioamaterizam |
| Log4OM v2 | [log4om.com](https://www.log4om.com) | Kompletan i moderan generalni logger s integracijom klastera i rig-controle. | Windows | Slobodno/Donacija | Svi amateri |
| DXKeeper | [dxlabsuite.com](https://www.dxlabsuite.com) | Napredni logging alat kao dio moćnog DXLab paketa. | Windows | Besplatno | DX lovci |
| CloudLog | [github.com/magicbug/Cloudlog](https://github.com/magicbug/Cloudlog) | Izvrsni web-bazirani logger hostan na vlastitom poslužitelju. | Web | Besplatno | Modernisti i korisnici različitih OS-a |
| Ham Radio Deluxe | [hamradiodeluxe.com](https://www.hamradiodeluxe.com) | "Sve-u-jednom" sustav za kontrolu uređaja, digitalne modove i dnevnik. | Windows | Komercijalno | Korisnici koji žele potpuno integrirani sustav |
| MacLoggerDX | [dogparksoftware.com](https://dogparksoftware.com/MacLoggerDX.html) | Prvorazredni logger i CAT alat za Mac ekosistem. | macOS | Komercijalno | Mac korisnici |

---

## Digitalni modovi
Digitalni modovi promijenili su svijet HF komunikacija. Omogućavaju iznimno stabilne veze iako stanja propagacije možda nisu idealna. Vidi više u [FT8 Vodiču](../operating/ft8_guide.md).

| Naziv | Link | Opis (HR) | Platforma | Cijena | Preporučeno za |
|-------|------|-----------|-----------|--------|----------------|
| WSJT-X | [physics.princeton.edu/pulsar/k1jt](https://physics.princeton.edu/pulsar/k1jt) | Dominantan alat za FT8, FT4, WSPR, MSK144 na HF-u i satelitima. | Win/Mac/Linux | Besplatno | Sve moderne operatere |
| fldigi | [w1hkj.com](http://www.w1hkj.com) | Temeljni softver za legacy digitalne modove poput PSK31, RTTY, Olivia MFSK. | Win/Mac/Linux | Besplatno | Ljubitelje tastature u stvarnom vremenu |
| JS8Call | [js8call.com](http://js8call.com) | Omogućuje slobodni i nesmetani tekst koristeći robusnost FT8 usmjeravanja signala. | Win/Mac/Linux | Besplatno | Komunikaciju uz slab signal |
| Winlink Express| [winlink.org](https://winlink.org) | Standrad za prijenos e-mail poruka putem RF opsega bez interneta. | Windows | Besplatno | EmComm entuzijaste i hitne službe |
| MultiPSK | [f6cte.free.fr](http://f6cte.free.fr/) | Svejterovski program s preko 100 egzotičnih i standardnih modova dekodiranja. | Windows | Shareware | Eksperimentatore i dekodere rijetkih signala |

---

## SDR (Software Defined Radio)
Aplikacije zadužene za obradu izvanredno velikih pojaseva RF signala te njihovu vizualizaciju.

| Naziv | Link | Opis (HR) | Platforma | Cijena | Preporučeno za |
|-------|------|-----------|-----------|--------|----------------|
| SDR# | [airspy.com](https://airspy.com/download/) | Vrlo popularan i svestran preglednik za RTL-SDR bazirane uređaje. | Windows | Besplatno | Rad s jeftinim SDR donglovima |
| HDSDR | [hdsdr.de](http://www.hdsdr.de) | Izuzetno napredan dizajn za bolju manipulaciju filtrom te pregledno grafičko sučelje. | Windows | Besplatno | Razni prijamnici srednje klase |
| SDRuno | [sdrplay.com](https://www.sdrplay.com/sdruno/) | Glavni softver i referentna točka za SDRPlay prijamnike i vrhunski performansom. | Windows | Besplatno | Posjednike SDRPlay prijamnika |
| Gqrx | [gqrx.dk](https://gqrx.dk) | Aplikacija bazirana na GNU Radiju koja izvrsno radi na Linux OS platformama. | Mac/Linux | Besplatno | Linux zajednicu |
| CubicSDR | [cubicsdr.com](https://cubicsdr.com) | Moderan i prenosiv softver (cross-platform), pogodan za jednostavne prijemne stanice. | Win/Mac/Linux | Besplatno | Korisnike na više operacijskih sustava |
| OpenWebRX | [openwebrx.de](https://www.openwebrx.de) | Postavljanje vlastitog web SDR-a kako bi se omogućilo udaljenu uporabu primopredajnika. | Web (Linux) | Besplatno | Klubovima koji žele dijeliti svoje uređaje |

---

## Modeliranje antena
Značajan doprinos radioamaterizmu je sposobnost oblikovanja vlastitih antena te predviđanja njihovog ponašanja prije izrade.

| Naziv | Link | Opis (HR) | Platforma | Cijena | Preporučeno za |
|-------|------|-----------|-----------|--------|----------------|
| MMANA-GAL | [gal-ana.de/basicmm](http://gal-ana.de/basicmm/en/) | Zlatni besplatni standard za početnike - modeliranje žičanih antena za kratke valove. | Windows | Besplatno | Početnike i graditelje antena |
| 4NEC2 | [qsl.net/4nec2](https://www.qsl.net/4nec2/) | Napredni NEC2 baziran simulator za složenije antenske oblike, omogućuje precizniji model tla. | Windows | Besplatno | Iskusne entuzijaste |
| EZNEC (Demo)| [eznec.com](https://www.eznec.com) | Komercijalni standard za inženjersku evaluaciju, danas otvorenog formata zavisno o verziji. | Windows | Paid/Demo | Napredno modeliranje |

---

## Propagacija
Aplikacije za vizualizaciju i praćenje solarnih ciklusa te utjecaja na izosphere i radijske komunikacije na kratkom valu.

| Naziv | Link | Opis (HR) | Platforma | Cijena | Preporučeno za |
|-------|------|-----------|-----------|--------|----------------|
| VOACAP | [voacap.com](https://www.voacap.com) | Temeljito predviđanje mogućih i stabilnih radio komunikacija obzirom na snagu, vremensku zonu i stanje ciklusa. | Web | Besplatno | Svi HF korisnici |
| HamClock | [clearskyinstitute.com](http://www.clearskyinstitute.com/ham/HamClock) | All-in-one cjelokupni zaslon za praćenje iznimnog mnoštva korisnih podataka (sateliti, solar, spotovi). | Linux/Web/Pi | Besplatno | Radioklubovi i napredni shack displayi |
| DX Atlas | [dxatlas.com](http://www.dxatlas.com) | Vrhunska aplikacija mapa s vizualizacijom zonskih i dnevnih terminatora, odlična za planiranje DX-a. | Windows | Shareware | DX lovci i contesteri |
| SolarHam | [solarham.net](https://www.solarham.net) | Središnja stranica za procjenu solarnih baklji, indeksa, K-indeksa te ostalih ključnih podataka solarnih flukseva. | Web | Besplatno | Svaki operater na kratkom valu |

---

## Sateliti
Softver namijenjen obradi orbitalne putanje letjelica i satelita radi ostvarivanja uspješnijih radioamaterskih interakcija. Za više informacija posjetite poglavlje [Sateliti](../activities/satellites.md).

| Naziv | Link | Opis (HR) | Platforma | Cijena | Preporučeno za |
|-------|------|-----------|-----------|--------|----------------|
| Gpredict | [oz9aec.net](http://gpredict.oz9aec.net/) | Pregledan vizualizator i doppler kalibrator otvorenog standarda (omogućuje automatsku rotaciju antena za klubove). | Win/Linux/Mac | Besplatno | Prikaz pozicija i pracenje |
| SatPC32 | [amsat-uk.org](https://amsat.org/) | Industrijski radioamaterski alat za CAT kontrolu letjelica s mogućnostima automatske korekcije po VFO-u. | Windows | Besplatno | Operateri opremljeni azimut/elevacija rotorima |

---

## CW vježba (Učenje telegrafije)
Telegrafija nije zaboravljena vještina. Preduvjet je za dugotrajno bavljenje sportom i najpopularnijim [natjecanjima](../activities/contesting.md). Provjerite i poglavlje o [Učenju telegrafije](../operating/cw_learning.md).

| Naziv | Link | Opis (HR) | Platforma | Cijena | Preporučeno za |
|-------|------|-----------|-----------|--------|----------------|
| LCWO.net | [lcwo.net](https://lcwo.net) | Standard za online učenje koristeći efikasnu i modernu "Kochovu metodu". | Web | Besplatno | Svaki početnik telegrafije |
| Just Learn Morse | [justlearnmorsecode.com](http://www.justlearnmorsecode.com) | Desktop alat dizajniran kako bi olakšao i poboljšao progres kroz slušne zvučne predloške i testiranje. | Windows | Besplatno | Trening za Windows operacijski sustav |
| G4FON Koch Trainer| [g4fon.net](https://www.g4fon.net) | Tradicionalniji pristup i nevjerojatno realistična simulacija pravog radijskog prometa s QRM/QRN ometačima zvuka. | Windows | Besplatno | Simulacija natjecanja i grešaka u opsegu |
| Morse Trainer | (Naći na trgovinama) | Prilagodljiva metoda učenja Koch sustava s mobitelima za prenošenje vježbanja bilo kamo i na raspoložive minute svuda. | iOS/Android| Besplatna/Plaćena | Osobe s nedostatkom računalnog pristupa |

---

## Radio kontrola (CAT) i arhitektura
Mnogome se komunikacija operativnog softvera svodi na posredničke 'library' slojeve kako bi razgovarali direktno s hardverom koji čeka serijske komande i CAT upute.

| Naziv | Link | Opis (HR) | Platforma | Cijena | Preporučeno za |
|-------|------|-----------|-----------|--------|----------------|
| Hamlib | [hamlib.github.io](https://hamlib.github.io) | Temelj open-source posredni slojeva preko 200 modernih uređaja. Mnogo ostalog softvera se oslanja na ovu istu bazu. | Win/Mac/Linux | Besplatno | Developer alat |
| OmniRig | [dxatlas.com/omnirig](http://www.dxatlas.com/omnirig) | Iznimno popularna Windows COM sučeljnica prepoznavanja više VFO-a opreme gdje deseci loggera zbilja koriste ovo. | Windows | Besplatno | Windows softver integratore |
| flrig | [w1hkj.com](http://www.w1hkj.com) | Izvorni softver Fldigi paketa kako ne bi nužno ovisili o drugome ali s preglednom GUI strukturom za Hamlib i kontrolu | Win/Linux | Besplatno | U kombinaciji s grafičkim aplikacijama modova |

---

## Mobilne aplikacije
Zahvaljujući pametnim telefonima, mogućnosti šeka danas su nam na dlanu.

| Naziv | iOS | Android | Opis (HR) | Cijena |
|-------|-----|---------|-----------|--------|
| HamAlert | ✓ | ✓ | Izenadna puštavanja i obavijesti obzirom na vlastite filtre za spotanje teških i specifičnih DX-ova. | Besplatno |
| RepeaterBook | ✓ | ✓ | Terenski offline repozitorij frekvencija repetitora lokacija po cijelom svijetu neovisno o mrežnom doboku u autu i šumi | Besplatno |
| APRS.fi | ✓ | ✓ | Vizualizacija kretanja korisnika priključenih na digitalno-lokacijski APRS mobilni sustav nadziravši i poziciju prijateljev. | Besplatno |
| SOTA Goat/Spotter | ✓ | ✓ | Najpopularniji praćenje vrhova SOTA stanica i alarma o pronalascima terenskih planinskih radio operatera na licu mjesta. | Bespl./Pl. |
| QRZ | ✓ | ✓ | Najveći imenik imena korisnika sa pretragom pozivnih oznaka kako bi potražili preostale detalje dok vodite brzu govornu vezu. | Bespl./Pre. |
| POTA | ✓ | ✓ | Aplikacija Parks on the Air sustava pronalaska ulova stanaca smještenih iz opreme po svim zaštićenim rezervaritetima| Besplatno |

---

## Preporučeni starter stack

Za početnike koji žele odmah početi s kvalitetnom instalacijom:

**Minimalni stack (besplatno, ~30 min instalacije):**
1.  [**Log4OM**](https://www.log4om.com) — logbook i DX klaster
2.  [**WSJT-X**](https://physics.princeton.edu/pulsar/k1jt/wsjtx.html) — FT8 digitalni rad
3.  [**fldigi**](http://www.w1hkj.com) — PSK31, RTTY i ostali digitalni modovi
4.  [**SDR#**](https://airspy.com/download/) + RTL-SDR dongle (~15 EUR) — primanje bez slanja

**Napredni dodatci:**
5.  [**N1MM+**](https://n1mmwp.hamdocs.com) — contest logiranje
6.  [**MMANA-GAL**](http://gal-ana.de/basicmm/en/) — modeliranje antena
7.  [**LCWO.net**](https://lcwo.net) — učenje CW-a
8.  [**DX Atlas**](http://www.dxatlas.com) — vizualizacija DX veza i gray line

!!! tip "Sve besplatno"
    Svaki softver u minimalnom stacku je 100% besplatan i aktivan. Radioamaterska zajednica tradicionalno dijeli softver otvorenog koda.

---

## Povezane teme

*   [FT8 praktični vodič](../operating/ft8_guide.md) — Detaljno korištenje WSJT-X
*   [Učenje CW](../operating/cw_learning.md) — LCWO i Koch metoda
*   [Modovi rada](../operating/modes.md) — Koji softver za koji mod
*   [Antene i vodovi](../technical/antennas.md) — Antenski modeliranje u praksi
