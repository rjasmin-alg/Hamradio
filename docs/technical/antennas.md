# Antene i vodovi

Antena je najvažniji dio svake radiostanice. Loša antena na skupom uređaju radi lošije nego dobra antena na jeftinom uređaju. Antena pretvara električni signal iz predajnika u elektromagnetski val koji putuje prostorom — i obrnuto pri prijemu. Razumijevanje kako to funkcionira daje vam prednost nad operaterima koji samo "priključe i nadaju se".

## Teorija antenskog zračenja

### Kako antena emitira

Kada izmjenična struja (RF signal) teče kroz vodič, oko njega se stvara promjenjivo elektromagnetsko polje. Ako je vodič odgovarajuće duljine, to polje se "odljepljuje" od vodiča i širi kao slobodni elektromagnetski val brzinom svjetlosti:

$$ c = 3 \times 10^8 \, \text{m/s} \approx 300{,}000 \, \text{km/s} $$

Veza između frekvencije i valne duljine:

$$ \lambda = \frac{c}{f} $$

!!! example "Primjer: duljina vala na 14 MHz (20-metarski opseg)"
    $\lambda = \frac{300{,}000 \, \text{km/s}}{14{,}000{,}000 \, \text{Hz}} = 21.4 \, \text{m}$
    
    Polvalni dipol za 20m imat će ukupnu duljinu ≈ 10.7 m (svaki krak ≈ 5.35 m).

### Polarizacija

Polarizacija opisuje orijentaciju električnog polja u prostoru:

*   **Vertikalna polarizacija**: Antena je okomita na tlo. Tipična za mobilne i VHF/UHF antene. Elektromagnetski val "vibrira" gore-dolje.
*   **Horizontalna polarizacija**: Antena je paralelna s tlom. Tipična za HF dipole i Yagi antene.
*   **Kružna polarizacija (RHCP/LHCP)**: Koristi se za satelitske veze i EME jer se ne gubi signal pri rotaciji.

!!! warning "Gubitak zbog neskladne polarizacije"
    Ako predajnik koristi vertikalnu antenu a prijemnik horizontalnu, gubite oko **20 dB** snage! To je faktor 100 — ekvivalent smanjenja snage sa 100 W na 1 W. Uvijek uskladite polarizaciju!

### Dijagram zračenja (Radiation Pattern)

Antena ne emitira jednako u svim smjerovima. Dijagram zračenja grafički prikazuje relativnu jačinu signala u svakom smjeru.

*   **Omnidirektivan (kružni)**: Vertikalne antene — jednako u svim smjerovima, ali ograničen kut prema horizontu.
*   **Usmjeren (beam)**: Yagi, Quad — koncentracija energije u jednom smjeru.
*   **F/B omjer (Front-to-Back)**: Koliko je jači signal naprijed u odnosu na straga. Veći F/B = manje smetnji izvana.

---

## Antenski dobitak (Gain)

Antena **ne stvara energiju** — samo je preusmjerava. Kao leća za svjetlo: ne pojačava izvor, ali fokusira zrake u jedan smjer.

### dBi vs dBd

| Mjerna jedinica | Referenca | Opis |
|----------------|-----------|------|
| **dBi** | Izotropni izvor (teorijska savršena sfera) | Svi proizvođači koriste ovo — veće brojke |
| **dBd** | Standardni $\lambda/2$ dipol | Realniji za usporedbu antena |

Konverzija: $0 \, \text{dBd} = 2.15 \, \text{dBi}$

!!! note "Praktična interpretacija"
    Yagi antena s dobitkom 10 dBd znači da je 10× jača od dipola u smjeru fokusa. U praksi to je razlika između "čujemo vas dobro" i "jedva čujemo" na DX vezama.

---

## Vrste antena

### Dipol ($\lambda/2$)

![Dipol Antena](https://upload.wikimedia.org/wikipedia/commons/2/2f/Dipole_antenna.png)

Najjednostavnija efikasna antena. Dva jednaka kraka, napajana u centru koaksijalnim kabelom (kroz balun).

**Duljina dipola:**

$$ L_{total} = \frac{142.5}{f_{MHz}} \, \text{m} $$

(faktor 142.5 umjesto 150 zbog "end effect" skraćenja)

| Opseg | Frekvencija | Ukupna duljina | Svaki krak |
|-------|-------------|----------------|------------|
| 80 m | 3.65 MHz | 39.0 m | 19.5 m |
| 40 m | 7.1 MHz | 20.1 m | 10.0 m |
| 20 m | 14.2 MHz | 10.0 m | 5.0 m |
| 15 m | 21.2 MHz | 6.7 m | 3.35 m |
| 10 m | 28.5 MHz | 5.0 m | 2.5 m |
| 2 m | 144 MHz | 1.0 m | 0.5 m |

**Impedancija**: 73 Ω u slobodnom prostoru, u praksi 50–70 Ω ovisno o visini.

*   [**Video: Kako radi dipol antena**](https://www.youtube.com/results?search_query=how+dipole+antenna+works+radiation+pattern)

### Yagi-Uda (Beam)

![Yagi Antena](https://upload.wikimedia.org/wikipedia/commons/0/05/Yagi-uda_antenna.svg)

Usmjerena antena s visokim dobitkom. Sastoji se od:
*   **Reflektor**: Malo dulji od $\lambda/2$, iza dipola — "odbija" signal naprijed
*   **Dipol (driven element)**: Jedini koji je električki spojen na kabel
*   **Direktori**: Malo kraći od $\lambda/2$, ispred dipola — "usmjeravaju" signal

Više direktora = veći dobitak, ali uži F/B kut.

*   Tipični dobitak 3-elementne Yagi: ~7 dBd
*   Tipični dobitak 5-elementne Yagi: ~10 dBd
*   [**Video: Kako radi Yagi antena**](https://www.youtube.com/results?search_query=how+yagi+antenna+works)

### Vertikalna antena (Ground Plane)

![Ground Plane Antena](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c1/Ground_plane_antenna_diagram.svg/320px-Ground_plane_antenna_diagram.svg.png)

Omnidirektivan vertikalni dipol. Gornji krak (radiator) je $\lambda/4$ visok, a donji "tlo" čine radijali (minimalno 4).

**Duljina vertikalnog radijatora ($\lambda/4$):**

$$ L = \frac{71.5}{f_{MHz}} \, \text{m} $$

*   Impedancija bez radijala: ~36 Ω → s radijalima na tlu: ~50 Ω (idealno za koaks)
*   Prednosti: omnidirekcionalnost, nema potrebe za rotatorom
*   Nedostaci: treba puno radijala za dobar odziv, hvata i šum jednako kao signal

### End-Fed Half Wave (EFHW)

Genijalno rješenje za male prostore — kabel se priključuje na kraj žice, a ne u centar. Problem: impedancija na kraju polvala je **2000–4000 Ω** pa treba transformator.

*   Koristi se **49:1 unun** transformator za prilagodbu na 50 Ω
*   Prednosti: lako postavljanje, nema baluna (antena nije simetrična)
*   Nedostaci: moguće RF struje na plaštu kabela bez kvalitetnog ferrita

### Magnetic Loop (Mali magnetski krug)

Kompaktan urezan krug od debele bakrene cijevi ili trake s kondenzatorom za ugađanje.

*   Promi 0.3–1 m, radi na HF opsezima
*   Izuzetno visok Q faktor — uski propusni pojas, niska razina smetnji
*   Može raditi unutar prostorije (slabiji signal, ali koristan kad nema vrta)

!!! danger "OPASNOST: Visoki napon na kondenzatoru!"
    Na vrhu kondenzatora magnetic loop antene **mogu se javiti naponi od nekoliko tisuća volti** pri većim snagama. Nikada ne dodirujte antenu dok predajnik radi!

### Logaritmijsko-periodska antena (Log-Periodic)

Slična televizijskoj anteni — skup dipola različitih duljina koji osiguravaju **širokopojasnu** pokrivenost.

*   Radi na više opsega bez ugađanja
*   Manji dobitak od Yagi (6–8 dBi) ali mnogo širi radni pojas
*   Česta u komercijalnim instalacijama gdje nije važno mijenjati opsege

### J-Pole (Slim Jim)

Jednostavna VHF/UHF antena od bakrene cijevi ili 450 Ω feeder žice.

*   Nema zemnih ploča (radijala) — napajanje je u J-dijelu koji služi kao prilagodnik
*   Popularna za 2 m i 70 cm opsege
*   Može se napraviti u sat vremena od bakrenih vodovodnih cijevi

### Quad antena

Žična verzija Yagi antene — elementi su kvadratni ili dijamantni zatvoreni petlji umjesto ravnih šipki.

*   Sličan dobitak kao Yagi s jednim elementom manje
*   Otpornija na vjetar zbog manje površine
*   Popularna kod DX operatera

---

## Balun i Unun transformatori

### Zašto su potrebni?

Koaksijalni kabel je **asimetričan** (nesimetričan, "unbalanced") — signal teče po unutarnjem vodiču, a povrat po plaštu. Dipol antena je **simetričan** ("balanced") — oba kraka su jednaka.

Bez baluna, RF struje teku i po **vanjskoj strani plašta kabela** — kabel postaje dio antene, uzrokuje:
*   TVI (Television Interference) i RFI u kući
*   Neočekivane dijagrame zračenja
*   RF "paljenje" u vašim rukama

**Balun** (BALanced-UNbalanced) rješava ovaj problem.

### Vrste

| Tip | Omjer | Primjena |
|-----|-------|---------|
| **Balun 1:1** | Impedancija 1:1 | Dipol, Yagi (50 Ω antena) |
| **Balun 4:1** | Impedancija 4:1 | Folded dipol (200 Ω), windom antene |
| **Unun 1:1** | Asimetričan→Asimetričan | Potiskivanje struja na plaštu vertikalki |
| **Unun 49:1** | Asimetričan prilagodnik | EFHW antene (2450 Ω → 50 Ω) |

!!! tip "Napravi vlastiti 1:1 balun"
    Najjednostavniji balun za HF je "choke balun" od ferritnog torusa (FT-240-43): namotajte 8–10 okretaja koaksijalnog kabela kroz torusni ferritor. Zatvori RF struje na plaštu bez promjene impedancije.

---

## Antenski vodovi (Feedlines)

### Koaksijalni kabel

Najčešće korišten vod u radioamaterizmu. Standard impedancije: **50 Ω**.

**Gubici koaksijalnog kabela** (dB/100 m):

| Kabel | HF 28 MHz | 50 MHz | VHF 144 MHz | UHF 432 MHz | 1296 MHz |
|-------|-----------|--------|-------------|-------------|---------|
| **RG-58** | 3.0 dB | 4.5 dB | 7.5 dB | 13.5 dB | 25+ dB |
| **RG-213** | 1.8 dB | 2.8 dB | 4.5 dB | 8.0 dB | 15 dB |
| **LMR-400** | 0.9 dB | 1.4 dB | 2.4 dB | 4.3 dB | 7.5 dB |
| **7/8" Heliax** | 0.35 dB | 0.55 dB | 1.0 dB | 1.8 dB | 3.5 dB |

!!! warning "Gubici su razorni na UHF!"
    30 m kabela RG-58 na 432 MHz gubi 4 dB — to je gotovo **60% snage** bačeno u toplinu. Na 1296 MHz je kabel od 10 m gotovo beskoristan. Za UHF/SHF koristite LMR-400 ili Heliax, i premjestite predajnik što bliže anteni!

**Konektori:**
*   **PL-259 (UHF)**: Standard na HF, do ~150 MHz. Lako lemiti.
*   **N-tip**: Za VHF, UHF, SHF — vodootporan, nizak gubitak, kompliciranije lemljenje.
*   **BNC**: Za laboratorijsku upotrebu, do ~4 GHz, brzo spajanje.
*   **SMA**: Sitni konektor za SDR prijemnike i handhelds.

### Dvožilni vod (Ladder Line / Twin-Lead)

450 Ω dvožilni vod (ladder line) ima **puno manje gubitke** od koaksijalnog kabela, osobito pri visokim SWR vrijednostima.

*   Može raditi s SWR 10:1 bez katastrofalnih gubitaka
*   Idealan za **ZS6BKW / G5RV** i slične multiband antene
*   Treba antenska tuner na ulazu (ne direktno na transciever)
*   Ne smije prolaziti uz metalne površine (debalanciranje)

---

## SWR — Omjer stojnih valova

SWR (Standing Wave Ratio) mjeri koliko dobro je antena prilagođena vodu.

$$ SWR = \frac{1 + |\Gamma|}{1 - |\Gamma|} $$

Gdje je $\Gamma$ koeficijent refleksije. Za savršenu prilagodbu: $\Gamma = 0$, SWR = 1:1.

| SWR | Udio reflektirane snage | Ocjena |
|-----|------------------------|--------|
| 1:1 | 0% | Savršeno |
| 1.5:1 | 4% | Odlično |
| 2:1 | 11% | Prihvatljivo |
| 3:1 | 25% | Treba ugađanje |
| 5:1 | 44% | Loše, moguće oštećenje PA |
| ∞:1 | 100% | Otvoreni ili kratki spoj |

!!! warning "SWR i transciever"
    Moderni transciiver pri SWR > 2:1 automatski smanjuje izlaznu snagu (fold-back) radi zaštite PA. To nije potvrda da je SWR dobar — samo da je uređaj preživio. Uvijek provjerte SWR prije rada!

---

## Praktični vodič: Postavljanje prvog dipola

### Što vam treba
*   2× žica (bakrena, 1.5–2.5 mm², ≥20 m za 40 m opseg)
*   1:1 balun (ferritor ili komercijalnan)
*   Koaksijalni kabel do stanice (RG-213 ili LMR-400)
*   2 izolacijska vijka (end insulators)
*   Uže za podizanje

### Korak po korak

1.  **Izračunajte duljinu**: $L_{total} = \frac{142.5}{f_{MHz}}$ metara. Za 40 m (7.1 MHz): ≈ 20 m ukupno.
2.  **Prerežite žicu** na dva kraka od po 10 m.
3.  **Montajte balun** u centar — žice pričvrstite na bočne priključke baluna.
4.  **Podignite antenu** što više možete — idealno $\lambda/2$ od tla (>10 m za 40 m opseg).
5.  **Koaksijalni kabel** od baluna do stanice — spojite što je kraće moguće.
6.  **Izmjerite SWR** — počnite s antenskim analizatorom (NanoVNA) ili SWR metrom.
7.  **Finom ugodite** skraćivanjem žice po 10–20 cm ako je SWR visok na nižim frekvencijama.

!!! tip "Savjet iz prakse"
    Antena u obliku "obrnutog V" (inverted V — oba kraka spuštena pod kutom od 120°) zahtijeva manje prostora od horizontalnog dipola i ima gotovo jednak SWR. Centralni oslonac može biti drvo, jarbol ili čak ribički štap.

---

## Simulatori antena

Softver za modeliranje antena omogućuje vam da "izgradite" antenu virtualno i vidite dijagram zračenja, SWR i impedanciju:

*   [**MMANA-GAL**](http://gal-ana.de/basicmm/en/) — Besplatan, moćan, standard u hobiju. NEC2 baziran.
*   [**4NEC2**](https://www.qsl.net/4nec2/) — Napredniji NEC-2 simulator za Windows.
*   [**EZNEC**](https://www.eznec.com/) — Komercijalni, najjednostavniji za početnike (demo verzija dostupna).
*   [**Online kalkulator dipola**](https://www.allaboutcircuits.com/tools/dipole-antenna-length-calculator/) — Brzi izračun bez instalacije softvera.

---

## Povezane teme

*   [Osnove elektronike](electronics.md) — Impedancija, reaktancija, LC krugovi
*   [Uzemljenje i zaštita](grounding.md) — RF uzemljenje, radijali, zaštita od groma
*   [Sigurnost](safety.md) — Sigurnost pri postavljanju antena, blizina dalekovoda
*   [Frekvencijski planovi](../operating/bandplans.md) — Koji opsezi su dostupni i za što
