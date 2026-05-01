# Hrvatski propisi za radioamatere

Radioamaterizam u Republici Hrvatskoj reguliran je jasnim zakonskim okvirom koji osigurava da hobi ne ometa komercijalnu, vojnu i hitnu komunikaciju. Razumijevanje propisa nije samo zakonska obveza — štiti vas i jamči mirno uživanje u hobiju.

## Zakonski okvir

### 1. Zakon o elektroničkim komunikacijama (ZEK)

Krovni zakon koji regulira korištenje RF spektra u RH. Za radioamatere relevantne odredbe:

*   Definira RF spektar kao javno dobro kojim upravlja HAKOM
*   Propisuje uvjete za dodjelu dozvola
*   Određuje sankcije za nelegalno odašiljanje
*   Implementira EU direktive o elektromagnetskoj kompatibilnosti (EMC)

[Zakon o elektroničkim komunikacijama (NN 76/2022)](https://narodne-novine.nn.hr/clanci/sluzbeni/2022_07_76_1143.html)

### 2. Pravilnik o amaterskim radijskim komunikacijama

Specifični pravilnik za radioamatere — "biblija propisa" svakog operatora. Sadrži:

*   Razrede dozvola i privilegije
*   Dopuštene opsege i maksimalne snage
*   Pravila za pozivne oznake
*   Obveze operatora (identifikacija, logbook)
*   Tehničke zahtjeve za opremu i antene

[Pravilnik — pretraži na Narodnim novinama](https://narodne-novine.nn.hr/)

!!! warning "Provjerite aktualnu verziju"
    Pravilnici se periodično ažuriraju. Uvijek provjerite najnoviju verziju na [nn.hr](https://narodne-novine.nn.hr/) ili [hakom.hr](https://www.hakom.hr/). Ovaj priručnik odražava stanje 2024/2025.

---

## Razredi dozvola i privilegije

### Tablica opsega i snaga

| Razred | Opseg | Frekvencije | Max snaga (ERP) | Modovi |
|--------|-------|------------|----------------|--------|
| **N** | 160 m | 1.810–1.850 MHz | 10 W | CW, SSB |
| **N** | 80 m | 3.500–3.600 MHz | 10 W | CW, SSB |
| **N** | 40 m | 7.000–7.100 MHz | 10 W | CW, SSB |
| **N** | 2 m | 144.000–146.000 MHz | 10 W | CW, SSB, FM, Digital |
| **N** | 70 cm | 430.000–440.000 MHz | 10 W | CW, SSB, FM, Digital |
| **B** | 160 m | 1.810–2.000 MHz | 100 W | CW, SSB, Digital |
| **B** | 80 m | 3.500–3.800 MHz | 100 W | Svi modovi |
| **B** | 40 m | 7.000–7.200 MHz | 100 W | Svi modovi |
| **B** | 20 m | 14.000–14.350 MHz | 100 W | Svi modovi |
| **B** | 15 m | 21.000–21.450 MHz | 100 W | Svi modovi |
| **B** | 10 m | 28.000–29.700 MHz | 100 W | Svi modovi |
| **B** | 2 m | 144.000–146.000 MHz | 100 W | Svi modovi |
| **B** | 70 cm | 430.000–440.000 MHz | 100 W | Svi modovi |
| **A** | **Svi opsezi** | **1.8 MHz – 250 GHz** | **1000–1500 W** | **Svi modovi** |

!!! note "ERP vs. PEP"
    **ERP** (Effective Radiated Power) = snaga predajnika × dobitak antene. **PEP** (Peak Envelope Power) = vršna snaga SSB signala. Pravilnik navodi ERP kao mjeru, a ne izlaznu snagu transciivera!

### Primarna vs. sekundarna namjena opsega

Ovo je kritičan pojam koji mnogi ignoriziraju:

*   **Primarna namjena**: Radioamateri imaju puna prava na opsegu; drugi servisi ne smiju ih ometati
*   **Sekundarna namjena**: Radioamateri "gostuju" u opsegu koji pripada drugom servisu; **ne smiju ometati primarnog korisnika** i moraju prestati raditi na zahtjev

Primjeri sekundarne namjene za radioamatere:
*   **160 m** (1.8–2.0 MHz): Sekundarna u dijelu spektra; vojska i pomorstvo su primarni
*   **40 m** (7.0–7.2 MHz): U nekim regijama sekundarna (posebno izvan IARU Regija 1)
*   **23 cm** (1240–1300 MHz): Sekundarna uz radar, navigacijske sustave

!!! warning "Primarna vs. sekundarna — pravni status"
    Ako koristite opseg u sekundarnoj namjeni i primate komentar od primarnog korisnika da prekinete — **morate odmah prestati**. Kršenje ovog pravila je zakonski prekršaj.

---

## Pozivne oznake (Callsigns)

### Struktura

Sve hrvatske pozivne oznake imaju prefiks **`9A`** (dodijeljen ITU-om za Republiku Hrvatsku):

```
9A + [regionalni broj] + [1–3 slova]
Primjer: 9A1ABC, 9A3T, 9A2AA
```

**Regionalni brojevi:**
*   **1**: Zagreb i okolica
*   **2**: Splitsko-dalmatinska, Dubrovačko-neretvanska
*   **3**: Osječko-baranjska, Vukovarsko-srijemska
*   **4**: Primorsko-goranska, Istarska, Ličko-senjska
*   **5**: Varaždinska, Koprivničko-križevačka, Krapinsko-zagorska
*   **6**: Bjelovarsko-bilogorska, Virovitičko-podravska, Požeško-slavonska
*   **7**: Šibensko-kninska, Zadarska
*   **0**: Specijalne, memorijalne i ekspedicijske postaje

### Sufiksi za privremene lokacije

Kada radite s lokacije koja nije vaša domicilna stanica, koristite sufiks:

| Sufiks | Situacija | Primjer |
|--------|-----------|---------|
| **/P** | Portable (privremena postaja, npr. SOTA) | `9A1ABC/P` |
| **/M** | Mobile (u pokretu, u automobilu) | `9A1ABC/M` |
| **/MM** | Maritime Mobile (na brodu) | `9A1ABC/MM` |
| **/AM** | Aeronautical Mobile (u zrakoplovu) | `9A1ABC/AM` |
| **/QRP** | Neslužbeno, za označavanje rada na malim snagama | `9A1ABC/QRP` |

!!! tip "Inozemni rad s HR dozvole"
    S HAREC certifikatom (razred A), možete raditi u svim CEPT zemljama s privremenom dozvolom. Pravilnik za tu zemiju provjerite na [T/R 61-01](https://cept.org). Uglavnom dodajete `/P` ili prefiks zemlje domaćina.

---

## Obveze operatora

### Identifikacija

*   Svaka postaja mora se identificirati pozivnom oznakom **minimalno svaka 10 minuta** i na kraju svake veze
*   Nije dopušteno odašiljanje bez identifikacije (anonimno odašiljanje)
*   Iznimka: Signal distresa (MAYDAY/SOS) — uvijek odgovorite, bez obzira na dozvolu

### Dnevnik rada (Logbook)

Pravilnik ne zahtijeva obavezno vođenje dnevnika za sve razrede, ali:

*   HAKOM inspekcija može tražiti evidenciju veza
*   Dnevnik je osnova za potvrđivanje DX veza (QSL karte, diplome)
*   Preporučen za sve operatere

Više o vođenju dnevnika: [Logbook](../operating/logbook.md)

### Ograničenja sadržaja

Radioamaterske komunikacije smiju biti isključivo:

*   **Osobne prirode**: Između radioamatera, bez komercijalnog karaktera
*   **Tehničke**: Eksperimentiranje s opremom i propagacijom
*   **Nužne**: Koordinacija aktivnosti i informacije od zajedničkog interesa

**Zabranjeno je:**
*   Komercijalna komunikacija (reklamiranje usluga ili proizvoda)
*   Emitiranje glazbe ili zabavnih sadržaja
*   Obsceni ili uvredljivi sadržaj
*   Emitiranje šifrirane komunikacije namjerno skrivenoj od inspekcije
*   Ometanje legitimnih radio servisa

### Tehničke obveze

*   Oprema mora imati odgovarajuće filtriranje (ne smije emitirati harmonike koji ometaju TV ili 4G)
*   Antene moraju biti sigurno postavljene i ne smiju ugroziti susjednu infrastrukturu
*   EMF (elektromagnetsko polje) mora biti unutar ICNIRP granica — više na [Sigurnost](../technical/safety.md)

---

## Regulatorna tijela

### HAKOM — Hrvatska regulatorna agencija za mrežne djelatnosti

*   Jedino tijelo koje izdaje dozvole za radioamaterske postaje u RH
*   Provodi inspekcije RF spektra (terenski automobili s mjernom opremom)
*   Može zaplijeniti opremu pri kršenju propisa
*   Dodjeljuje pozivne oznake
*   Web: [www.hakom.hr](https://www.hakom.hr/)

### HRS — Hrvatski radioamaterski savez

*   Nacionalni savez radioamatera (član IARU — International Amateur Radio Union)
*   Organizira ispite u suradnji s HAKOM-om
*   QSL bureau — besplatno posredovanje u razmjeni QSL karata
*   Organizira nacionalna natjecanja i zastupa interes amatera
*   Web: [www.hamradio.hr](https://www.hamradio.hr/)

### IARU — International Amateur Radio Union

*   Koordinira radioamaterske interese na međunarodnoj razini (ITU, CEPT)
*   Donosi frekvencijske planove (bandplanove) kojima se radioamateri moraju pridržavati
*   Web: [www.iaru.org](https://www.iaru.org/)

---

## Kronologija zakonodavnih promjena

| Godina | Promjena |
|--------|---------|
| **1992.** | RH dobiva prefiks `9A` — radioamateri prelaze s YU prefiksa |
| **1995.** | Osnivanje HAKOM-a kao neovisnog regulatora |
| **2003.** | Morseov kod uklonjen iz obaveznih ispitnih zahtjeva (WRC-03) |
| **2012.** | Ratifikacija novih CEPT sporazuma; proširenje privilegija |
| **2022.** | Novi Zakon o elektroničkim komunikacijama (NN 76/2022) |

---

## Kaznene odredbe

Zakon o elektroničkim komunikacijama predviđa sankcije:

*   **Nelegalno odašiljanje** (bez dozvole): Novčana kazna + zaplijena opreme
*   **Ometanje hitnih servisa**: Kaznena prijava
*   **Kršenje tehničkih uvjeta** (harmonici, prekoračenje snage): Upozorenje → zaplijena opreme

!!! danger "HAKOM inspekcija"
    HAKOM operira vozilima opremljenim za triangulaciju izvora odašiljanja (RDF — Radio Direction Finding). Nelegalni operatori se lociraju i kažnjavaju. Nije to teorija — to se događa.

---

## Povezane teme

*   [Razredi dozvola](license_classes.md) — Detaljni opis privilegija
*   [Kako postati radioamater](exams.md) — Ispitni postupak
*   [Radioamaterska etika](ethics.md) — Ponašanje na opsegu
*   [Frekvencijski planovi](../operating/bandplans.md) — Što radi gdje na opsegu
