# Satelitske komunikacije

Radioamateri imaju vlastite satelite u orbiti — i možete ih koristiti s ručnom stanicom i improviziranom antenom. Satelitske komunikacije (skraćeno "sat") jedna su od tehničkih fascinantnih grana hobija koja kombinira razumijevanje astronomske mehanike, Dopplerove fizike i RF tehnike.

Na svijetu trenutno postoji više od 20 aktivnih amaterskih satelita različitih namjena — od jednostavnih FM repetitora do naprednih linearnih transponder-a za SSB i CW veze.

---

## Kako funkcioniraju amaterski sateliti?

Većina amaterskih satelita su **"leteći repetitori"** — primaju signal s Zemlje (uplink), pojačavaju ga i retransmitiraju natrag (downlink) na drugoj frekvenciji.

| Pojam | Objašnjenje |
|---|---|
| **Uplink** | Frekvencija na kojoj vi šaljete signal prema satelitu |
| **Downlink** | Frekvencija na kojoj slušate satelit (on odašilje prema Zemlji) |
| **Mode** | Kombinacija uplink/downlink banda (npr. Mode V/U = VHF gore, UHF dolje) |
| **Transponder** | Linearni "repeater" koji prenosi cijeli segment — ne samo FM, već i SSB i CW |
| **Footprint** | Geografska zona unutar koje je satelit dostupan (vidljiv) u danom trenutku |

### Tipovi satelita

**FM sateliti** (jednostavniji za korištenje):
- Rade poput standardnog FM repetitora, ali "vise" u orbiti
- Dovoljna je ručna stanica (handheld) od 5 W s improviziranom Yagi antenom
- Primjer: SO-50, AO-91, AO-92

**Linearne transponder satelite** (napredniji):
- Prenose cijeli frekvencijski segment — SSB, CW, digitalni modovi unutar "trake"
- Omogućavaju višestruke simultane veze (nije simplex kao FM)
- Zahtijevaju bolju opremu i antenu s praćenjem (azimut/elevacija rotori)
- Primjer: AO-7, FO-29, CAS-4A/B, XW-2 serija

---

## Dopplerska korekcija — ključni izazov

Amaterski sateliti lete brzinom od ~7.8 km/s (LEO orbita, niska orbita). Na toj brzini, Dopplerov efekt (isto što čujete kad vatrogasno vozilo prođe pored vas — sirena se mijenja) uzrokuje mjerljivu promjenu frekvencije:

- Na **145 MHz**: Dopplerski pomak može biti do ±3.5 kHz
- Na **435 MHz**: Pomak može biti do ±10 kHz

**Praktično:** Na početku prolaza, satelit se kreće prema vama — frekvencija je viša (trebate slušati "iznad" nominalnog downlinka). Na kraju prolaza, odmiče — frekvencija je niža. Ručno ili automatski korigirate frekvenciju na prijemniku tokom cijelog prolaza.

Softver poput **Gpredict** to radi automatski u kombinaciji s CAT kontrolom radija.

$$\Delta f = \frac{v}{c} \times f_0$$

gdje je $v$ radijalna brzina satelita, $c$ brzina svjetlosti, i $f_0$ nominalna frekvencija.

!!! tip "Za FM satelite — ručna korekcija je OK"
    Na FM satelitima, Dopplerski pomak nije fatalan — ako ste 2 kHz negdje drugdje od nominalnog, FM squelch će vas i dalje "otvoriti". Ručno korigiranje svakih 30-60 sekundi sasvim je dovoljno.

---

## Gdje i kada je satelit vidljiv?

Amaterski sateliti na niskoj orbiti (LEO) prolaze iznad vaše lokacije nekoliko puta dnevno, ali svaki prolaz traje samo **8–15 minuta**. Dakle, morate znati točno kad i gdje gledati (slušati).

### Alati za praćenje

| Alat | Platforma | Opis |
|---|---|---|
| **Gpredict** | Win/Linux/Mac | Desktopski tracker, CAT integracija za Doppler, besplatan |
| **ISS Detector** | Android/iOS | Jednostavan mobilni tracker focusiran na ISS |
| **Heavens-Above** | Web | Vizualni prikaz prolaza po vašoj lokaciji |
| **N2YO** | Web | Prikaz orbita u realnom vremenu s mapom |
| **SatPC32** | Windows | Klasičan sat tracker s CAT + rotator kontrolom |

Za točno praćenje, svi alati trebaju ažurirane **Keplerove elemente** (TLE — Two-Line Elements) koji opisuju orbitu satelita. Automatski se preuzimaju s NASA/AMSAT baze.

!!! note "Dva sata prije prolaza — ažuriraj TLE"
    Keplerovi elementi zastarijevaju. Za precizno praćenje ažurirajte ih barem jednom dnevno, posebno ako radite s satelitima koji imaju niže orbite (ISS ~400 km, SO-50 ~600 km).

---

## Oprema za početnike: FM sateliti

Za prvu satelitsku vezu na FM satelitu trebate iznenađujuće malo:

**Minimum:**
- Dualbandna ručna stanica (VHF + UHF) — npr. Baofeng UV-5R, Yaesu FT-70D, Kenwood TH-D75
- Improvizirana Yagi antena za 2 m + 70 cm (možete je napraviti za 20 kuna od aluminijskog štapa)
- Mobilni telefon s Gpredict ili ISS Detector aplikacijom (za praćenje prolaza)

**Tehnika rada:**
1. Saznajte kad satelit prolazi iznad vaše lokacije i koji je azimut (smjer) prolaza
2. Podesite uplink frekvenciju (s Doppler korekcijom +3 kHz na početku prolaza)
3. Slušajte downlink i čujte li satelit (karakteristični zvuk repetitora)
4. Zovite kratko: "9A1ZG, any station via SO-50?"
5. Pratite prolaz i ručno korigirajte Doppler kako satelit prolazi

!!! example "Popularne FM satelitske frekvencije"
    **SO-50:** Uplink 145.850 MHz (PL ton 67.0 Hz), Downlink 436.795 MHz
    
    **AO-91 (Fox-1B):** Uplink 435.250 MHz, Downlink 145.960 MHz
    
    **ISS:** Uplink/Downlink 145.825 MHz (APRS) ili 437.800 MHz (voice repeater, kad je aktivan)

---

## ISS — Međunarodna svemirska postaja

ISS (International Space Station) je najpoznatiji "amaterski satelit" — antene ARS (Amateur Radio Station) na ISS-u su pod pozivnom oznakama **NA1SS** (USA) i **RS0ISS** (Rusija).

Radioamaterske aktivnosti na ISS-u:

- **APRS gateway** (145.825 MHz) — ISS automatski digipeaterira APRS pakete s Zemlje. Možete "bounceati" APRS pakete kroz ISS!
- **Glasovni QSO** — kad je posada raspoložena i antena aktivna, javlja se na 145.800 MHz ili proglašenim frekvencijama
- **SSTV događaji** — ISS periodično šalje SSTV (Slow Scan TV) slike koje možete dekodirati i standardnim softverom (MMSSTV)
- **ARISS školski projekti** — ARISS (Amateur Radio on the International Space Station) program organizira veze između ISS posade i škola diljem svijeta

!!! info "ARISS i škole"
    ARISS (ariss.org) organizira direktne veze između astronauta na ISS-u i učenika u školama. Prijaviite svoju školu — Hrvatska je imala nekoliko takvih događaja. Astronauti koji su radioamateri: Thomas Pesquet (F4KLP), Sunita Williams (KC5ZTH), i mnogi drugi.

---

## Napredniji sateliti — linearne transpondere

Za SSB i CW veze putem satelita trebate:

- **Napredniji transceiver** s preciznim podešavanjem frekvencije (Fine Tune < 10 Hz)
- **Crossed-Yagi antenu** (circularly polarized) za azimut + elevacija praćenje
- **Rotorski sustav** — antena mora pratiti satelit kroz nebo (azimut i elevacija)
- **Gpredict + CAT** — automatsko Doppler korigiranje

Popularni linearni sateliti:
- **FO-29 (JAS-2)** — japanski satelit, V/U linearni transponder
- **AO-7** — lansiran 1974.! Još uvijek djelomično aktivan
- **CAS-4A i CAS-4B** — kineski sateliti, odlični transponderi, aktivni 2022–danas
- **XW-2 serija** — nekoliko kineskih linearnih satelita

---

## EME — Veza putem Mjeseca (Moonbounce)

EME (Earth-Moon-Earth) ili "moonbounce" je ekstremni oblik satelitske komunikacije — signal putuje do Mjeseca i natrag, ukupno ~760.000 km! Signal se gubi oko 250–270 dB na putu, što zahtijeva iznimno osjetljive prijemnike i jake antene.

- Popularno na 2 m (144 MHz) i 70 cm (432 MHz)
- Koristi se **JT65** i **Q65** digitalni protokol (iz WSJT-X paketa)
- Minimalna praktična oprema: 4-element Yagi array, 100+ W, niskošumni LNA predpojačalo
- Počelo se eksperimentirati 1950-ih, danas dostupno entuzijastima s odgovarajućom opremom

---

## Kako početi sa satelitskim radom

1. **Instalirajte Gpredict** ili koristite web tracker (N2YO.com) — odmah vidite kad SO-50 ili AO-91 prolaze iznad vas
2. **Nabavite dualbandnu ručnu stanicu** — praktično ma kakav VHF/UHF handheld
3. **Napravite ili kupite Arrow antenu** (El Yagi za sat) — idealna za ručno praćenje
4. **Pratite prolaz** — pokušajte uhvatiti signal satelita (samo slušajte prvi put)
5. **Probajte QSO** — javite se kad čujete aktivnost na FM satelitu

!!! tip "Najlakši start: SO-50 ili AO-91"
    SO-50 i AO-91 su najpouzdaniji FM sateliti za početak. Oba zahtijevaju PL ton na uplinku (SO-50: 67.0 Hz; AO-91: 67.0 Hz). Prolaze 4–8 puta dnevno, prolaz traje 8–12 minuta. Slušajte downlink i zadovoljite se što čujete signal — to je već uspjeh!

---

## Povezane teme

- [Frekvencijski planovi](../operating/bandplans.md) — VHF/UHF bandovi za satelite
- [Antene i vodovi](../technical/antennas.md) — Yagi i kružno polarizirane antene
- [Rad u pokretu](portable.md) — portabl satelitska stanica
- [Propagacija radio valova](../technical/propagation.md) — razlika zemaljske i satelitske propagacije
