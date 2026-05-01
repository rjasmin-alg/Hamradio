# RMZO — Radioamaterska mreža za opasnost

**RMZO** (Radioamaterska mreža za opasnost) je organizirani sustav unutar Hrvatskog radioamaterskog saveza koji se aktivira u slučaju prirodnih katastrofa, tehničkih nesreća ili bilo koje situacije u kojoj standardne telekomunikacijske mreže ne funkcioniraju.

RMZO nije samo lista frekvencija — to je **organizacijska struktura** koja definira tko koga koordinira, koje frekvencije se koriste, koji su prioriteti poruka i kako se izvještava nadležnim tijelima.

---

## Pravni okvir

RMZO djeluje u suradnji s:
- **HAKOM** — Hrvatska regulatorna agencija za mrežne djelatnosti (dodjeljuje posebne emcomm frekvencije)
- **HRS** — koordinira i vodi RMZO na nacionalnoj razini
- **112** — integracija s nacionalnim pozivnim centrom za hitne slučajeve

Zakon o elektroničkim komunikacijama daje prednost komunikacijama u slučaju opasnosti po život i imovinu pred svim ostalim prometom.

---

## Organizacijska struktura

```
HRS (nacionalna koordinacija)
        │
        ▼
Regionalni koordinatori (po županijama)
        │
        ▼
Lokalni radioklubovi i RMZO operatori
        │
        ▼
Terenske postaje (mobilne i portabl)
```

**Uloge u RMZO-u:**

| Uloga | Opis |
|---|---|
| **Net Control Station (NCS)** | Vodi mrežu, daje dozvolu za odašiljanje, bilježi sav promet |
| **Relay stanica** | Prosljeđuje promet između postaja koje se ne čuju direktno |
| **Terenska postaja** | Šalje izvještaje s lokacije katastrofe ili koordinacijskog centra |
| **Base stanica** | Fiksna postaja u RMZO, često klupska s backup napajanjem |

---

## Frekvencije RMZO

!!! warning "Frekvencije se mogu mijenjati"
    Uvijek provjerite aktualne RMZO frekvencije na [hamradio.hr](https://www.hamradio.hr) jer se mogu ažurirati odlukama HRS-a i HAKOM-a. Čuvajte aktualni popis u portabl stanici.

### HF frekvencije (dug doseg, bez infrastrukture)

| Frekvencija | Opseg | Namjena |
|---|---|---|
| **3.675 MHz** | 80 m | Primarna nacionalna EmComm frekvencija HR |
| 7.060 MHz | 40 m | Alternativna za dnevni rad (bolja dnevna propagacija) |
| 14.300 MHz | 20 m | IARU Regija 1 EmComm frekvencija (međunarodna) |

### VHF/UHF frekvencije (lokalni doseg, jasnoća)

| Frekvencija | Opseg | Namjena |
|---|---|---|
| **145.500 MHz** | 2 m | Primarna lokalna simplex EmComm frekvencija |
| 144.800 MHz | 2 m | APRS (automatsko praćenje i izvještavanje paketa) |
| 433.500 MHz | 70 cm | UHF simplex radno |
| Lokalni repetitori | 2 m / 70 cm | Koordinacija ako imaju backup napajanje |

---

## Aktivacija RMZO

### Kako se aktivira mreža?

RMZO se može aktivirati na dva načina:

1. **Službeni poziv** — DUZS/MUP/112 kontaktira HRS koordinatora i traži aktivaciju
2. **Samoinicijativno** — ako je očigledno da komunikacijska infrastruktura ne funkcionira (potres, poplava, nestanak struje na većem području), radioamateri se mogu organizirati bez čekanja poziva

U praksi, za veće katastrofe uvijek postoji i jedan i drugi mehanizam istovremeno.

### Faze aktivacije

**Faza 1 — Motrenje:** Operatori slušaju EmComm frekvencije i prate situaciju bez odašiljanja osim ako imaju hitnu informaciju.

**Faza 2 — Net aktivacija:** NCS poziva mrežu i preuzima koordinaciju. Sve postaje se javljaju s lokacijom i raspoloživošću.

**Faza 3 — Operativni rad:** Terenske postaje šalju izvještaje. NCS filtrira informacije i prosljeđuje nadležnima.

**Faza 4 — Deaktivacija:** NCS objavljuje kraj operacije. Sav promet se arhivira.

---

## Primjer net otvaranja

```text
NCS: "Svim postajama, svim postajama — ovo je 9A1XX, Net Control za RMZO mrežu.
      Otvaram EmComm net na frekvenciji 3.675 MHz u [UTC]. Mode: SSB.
      Postaje s hitnim prometom — javiti se odmah.
      Ostale postaje — javiti se prema abecedi kada dobijete poziv.
      9A1XX."

Terenska postaja: "9A1XX, ovde 9A7YY s lokacije Petrinja, imam izvještaj za prioritet."

NCS: "9A7YY, imate dozvolu — izvještajte."
```

---

## Što nositi u EmComm "go-bag"?

Go-bag je torba/ruksak s opremom sprema za brzo premještanje na terenu:

| Stavka | Napomena |
|---|---|
| Dualbandna ručna stanica (VHF/UHF) | Napunjena baterija + rezervna |
| HF QRP transceiver | Ako imate (IC-705, KX2, FT-818) |
| LiFePO4 baterija 10+ Ah | Neovisno napajanje |
| Solarni panel 20–30 W | Za produženi rad |
| Wire antena (EFHW ili dipol) | 10–15 m žice, konektor, kratki jarbol |
| Laptop/tablet s Winlink Expressom | Digitalne poruke |
| VARA modem ili SignaLink | Zvučna kartica za digitalne modove |
| Log bilježnica i olovke | Papirnat zapis uvijek kao backup |
| Popis EmComm frekvencija | Laminiran, u torbi |
| Punjač i multi-adapter | 12V i 230V verzije |

!!! tip "Testirajte go-bag redovito"
    Jednom kvartalno: izvadite opremu, provjerite jesu li baterije napunjene, i napravite kratki QSO kao test. Oprema koja nije testirana nije pouzdana oprema.

---

## Field Day — godišnja vježba

**Field Day** je godišnja EmComm vježba — radioamateri postavljaju portabl stanice bez kućnog napajanja i rade što više QSO-a u 24 ili 48 sati. Cilj je testirati:
- Portalb opremu
- Backup napajanje
- Operativne procedure
- Koordinaciju timova

U USA to organizira ARRL svaki lipanj. U Europi i HR organiziraju se klupske Field Day aktivnosti — pratite HRS kalendaré i klupske stranice.

---

## Kako se prijaviti u RMZO?

1. Kontaktirajte **HRS tajništvo** ili regionalnog EmComm koordinatora
2. Prijavite se prema uputama na [hamradio.hr](https://www.hamradio.hr)
3. Prođite **obuku** (klupski tečajevi, online materijali IARU)
4. Sudjelujte na redovitim **mrežnim testovima** (net check-in) kako vas sustav "zna"

---

## Povezane teme

- [Postupci u hitnim situacijama](procedures.md) — radio disciplina i protokoli poruka
- [Winlink](winlink.md) — digitalne poruke bez interneta
- [Rad u pokretu](../activities/portable.md) — portabl stanica za EmComm
- [Sigurnost](../technical/safety.md) — sigurna postava u kriznim uvjetima
- [Savezi i organizacije](../community/associations.md) — HRS kontakt i koordinacija
