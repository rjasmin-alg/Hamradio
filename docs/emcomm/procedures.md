# Postupci u hitnim situacijama

U kriznim komunikacijama, **disciplina spašava živote**. Razlika između kaotičnih i koordiniranih radio komunikacija u katastrofičnoj situaciji može biti presudna za pravovremenu reakciju spasilačkih službi.

Ova stranica pokriva základne principe, standardne formate poruka i pravila ponašanja na EmComm mreži.

---

## Zlatna pravila EmComm komunikacije

### 1. Slušanje je primarno

Prije nego odašiljete bilo što — slušajte. Saznajte:
- Je li frekvencija već u upotrebi?
- Postoji li Net Control Station (NCS)?
- Kakav je promet — rutinski, hitni, prioritetan?

Pravilo: **90% vremena slušate, 10% odašiljate.**

### 2. Kratko, jasno, bez žargona

EmComm komunikacija nije nijansirani razgovor — to je prijenos informacija pod stresom. Koristite:
- **Standardne fraze** (ne improvizaciju)
- **Fonetsku abecedu** za spelanje ključnih podataka
- **Kratke rečenice** — jedna poruka, jedna misao
- **Brojeve** — "jedan-nula-dva" umjesto "sto i dva"

### 3. Zapišite sve

Svaki QSO u EmComm mora biti dokumentiran:
- UTC vrijeme
- Pozivna oznaka pošiljatelja
- Sadržaj poruke
- Radnja poduzeta / prosljeđeno kome

Papirnat log je backup kada laptop ne radi. Uvijek imajte bilježnicu i olovku.

### 4. Ne odašiljite bez dozvole NCS-a

Kad postoji Net Control Station, **sva komunikacija ide kroz NCS**. Ne zovite druge postaje direktno, ne prosljeđujete poruke bez najave, ne "posjećujete" net odmah po ulasku.

!!! danger "Frekventno gaženje = kaos"
    Istovremeno odašiljanje više postaja (carrier clash) rezultira nerazumljivim signalom i gubitkom poruke. U EmComm situaciji to znači izgubljena informacija o žrtvama ili lokaciji. Disciplinirajte se.

---

## Prioritet poruka

Poruke se razvrstavaju prema hitnosti:

| Prioritet | Naziv | Opis | Primjer |
|---|---|---|---|
| 🔴 1 | **DISTRESS / MAYDAY** | Neposredna opasnost po živote | "Mayday, mayday — brod tone, 12 osoba na brodu" |
| 🟠 2 | **URGENCY / PAN-PAN** | Hitna situacija, ali bez neposredne životne opasnosti | "Pan-Pan — putnik s napadajem srca, trebamo hitnu pomoć na lokaciji X" |
| 🟡 3 | **SAFETY / SÉCURITÉ** | Upozorenje o opasnosti za ostale | "Sécurité — potres registriran, moguće oštećenje ceste na ruti Y" |
| 🟢 4 | **WELFARE** | Informacije o statusu žrtava / povrijeđenih | Popis evakuiranih, stanje infrastrukture |
| ⚪ 5 | **ROUTINE** | Rutinska koordinacija i logistika | Promjena frekvencije, status postaje, zahtjev za relay |

---

## Standardni formati poruka

### MAYDAY poziv

Koristiti isključivo za neposrednu opasnost po živote:

```text
MAYDAY MAYDAY MAYDAY
Ovo je [pozivna oznaka]
Mayday — [opis situacije u 1-2 rečenice]
Naša pozicija je [koordinate ili opis lokacije]
Na lokaciji se nalazi [broj osoba]
Trebamo [hrana/voda/medicinska pomoć/evakuacija]
[pozivna oznaka], over
```

### PAN-PAN poziv

Za hitne situacije bez neposredne životne opasnosti:

```text
PAN-PAN PAN-PAN PAN-PAN
Sve postaje, ovo je [pozivna oznaka]
Pan-Pan — [opis situacije]
Lokacija: [opis]
[Zahtjev za pomoć]
[pozivna oznaka], over
```

### IARU Standard EmComm poruka

Za strukturirani prijenos informacija kroz mrežu (ne verbalno, nego pisano — Winlink ili relay):

```
1. PRIORITET: [Routine / Welfare / Priority / Emergency]
2. POŠILJATELJ: [pozivna oznaka]
3. PRIMATELJ: [pozivna oznaka ili institucija]
4. DATUM/VRIJEME (UTC): [DD/MMM/YYYY HH:MM]
5. PRESLUŠANO KROZ: [pozivne oznake relay postaja]
6. PORUKA:
   [Jasna, kratka poruka. Jedna misao po rečenici. 
    Ne koristiti kratice koje primatelj možda ne poznaje.]
7. KRAJ PORUKE
8. [pozivna oznaka pošiljatelja]
```

!!! example "Primjer IARU EmComm poruke"
    ```
    1. PRIORITET: Priority
    2. POŠILJATELJ: 9A7YY
    3. PRIMATELJ: 9A1XX (NCS)
    4. DATUM/VRIJEME: 29/DEC/2024 14:35 UTC
    5. PRESLUŠANO KROZ: Direktno
    6. PORUKA:
       Javljam s lokacije Petrinja, Moslavačka ulica.
       Zgrada na broju 22 djelomično srušena, vidim 3 preživjele osobe.
       Pristup otežan — ulica blokirana ruševinom.
       Koordinate: 45.4417 N, 16.2744 E.
       Potrebna je teška mehanizacija za pristup.
    7. KRAJ PORUKE
    8. 9A7YY
    ```

---

## Fonetska abeceda (ICAO/NATO)

U EmComm komunikaciji, svako slovo koje može biti krivo čuto mora se spelati fonetskom abecedom:

| Slovo | NATO | Slovo | NATO |
|---|---|---|---|
| A | Alpha | N | November |
| B | Bravo | O | Oscar |
| C | Charlie | P | Papa |
| D | Delta | Q | Quebec |
| E | Echo | R | Romeo |
| F | Foxtrot | S | Sierra |
| G | Golf | T | Tango |
| H | Hotel | U | Uniform |
| I | India | V | Victor |
| J | Juliet | W | Whiskey |
| K | Kilo | X | X-ray |
| L | Lima | Y | Yankee |
| M | Mike | Z | Zulu |

Brojeve se izgovara jasno: **"niner"** za 9 (da se ne zamijeni s "nein" na njemačkom), **"fife"** za 5 (jasno od "fire").

---

## Posebna pravila na EmComm frekvencijama

- **Nikad ne testirajte antenu** emitiranjem na EmComm frekvenciji — to se čuje kao gibanje i uznemirava mrezu
- **Nemojte koristiti** frekvenciju za rutinski rad osim na pozivu NCS-a
- **Ako čujete MAYDAY** — prestanite odašiljati, slušajte, i zapišite informacije
- **Relay odgovornost** — ako čujete distress i NCS ga nije potvrdio, vaša dužnost je prosljeđivanje

!!! note "Pravni aspekt"
    Pomoć u nevolji je moralna i u nekim jurisdikcijama zakonska obveza i za radioamatere. Ignoriranje MAYDAY-a koji ste primili bez poduzimanja akcije nije prihvatljivo.

---

## Vježba i priprema

EmComm vještine se gube ako se ne primjenjuju. Preporučeni minimum:

- **Tjedno**: Javljanje na lokalnu EmComm mrežu (net check-in) — samo potvrdite prisutnost
- **Mjesečno**: Klupska EmComm vježba s porukama
- **Godišnje**: Field Day (postavljanje portabl stanice u uvjetima bez kućnog napajanja)

---

## Povezane teme

- [RMZO](rmzo.md) — hrvatska EmComm organizacija i frekvencije
- [Winlink](winlink.md) — slanje strukturiranih poruka digitalnim putem
- [Rad u pokretu](../activities/portable.md) — portabl stanica
- [Fonetska abeceda](../resources/phonetic.md) — detalji o NATO abecedi
