# Winlink — E-mail bez interneta

**Winlink** je globalna mreža koja omogućuje slanje i primanje **e-mail poruka putem radija**, bez oslanjanja na internet infrastrukturu. U kriznim situacijama — kad su telefonska mreža i internet nedostupni — Winlink ostaje operativan sve dok postoji radio signal.

Winlink koriste hitne službe, Crveni križ, Coast Guard, ARES timovi i tisuće radioamatera za redovitu digitalnu komunikaciju i EmComm vježbe.

---

## Kako funkcionira Winlink?

Winlink sustav ima tri elementa:

```
[Vaše računalo + radio]
        │
        │ (RF signal — HF ili VHF/UHF)
        ▼
[Gateway / RMS stanica]
(radioamaterska postaja spojena na internet)
        │
        │ (internet)
        ▼
[CMS — Winlink Central Message Server]
(cloud sustav koji čuva i prosljeđuje poruke)
        │
        ├── → Winlink korisnici (preuzimaju putem radio ili web)
        └── → Obični internet e-mail primatelji
```

**Ključna prednost:** Vaša poruka putuje **radiovalovima** do gateway postaje koja ima internet. Vi nemate internet — ali gateway ima, i prosljeđuje poruku dalje. Ako ste na HF-u (kratkim valovima), možete se spojiti na gateway u drugoj zemlji tisuće kilometara daleko — čak i ako je cijela vaša lokalna infrastruktura ugašena.

---

## Modovi rada Winlink-a

Winlink podržava više načina prijenosa podataka:

=== "VARA HF"
    Najsuvremeniji HF mod, visoka propusnost, robusnost u teškim uvjetima.
    - Frekvencijski raspon: HF (3–30 MHz)
    - Software: VARA HF modem (besplatan za 1200 bps, plaćeni za punu brzinu)
    - Preporučena brzina: do 8400 bps uz dobre uvjete
    - **Preporučeno za EmComm HF rad**

=== "VARA FM"
    FM verzija za VHF/UHF repetitore i simplex frekvencije.
    - Frekvencijski raspon: VHF/UHF (144 MHz, 432 MHz)
    - Brz i pouzdan za lokalne veze
    - Odličan za koordinaciju unutar mjesta/regije
    - **Preporučeno za lokalni EmComm VHF rad**

=== "Pactor"
    Stariji, ali robusni HF mod, popularan u mornarici i ARES zajednici.
    - Zahtijeva hardverski Pactor TNC modem (SCS, skuplje ~400–600 €)
    - Odlična propusnost za HF, posebno na DX vezama
    - Koristi se u brodskim i ekspedicijskim postajama

=== "ARDOP"
    Besplatan otvoreni HF protokol, nešto sporiji od VARA-e ali bez licenciranja.
    - Dobra opcija za početnike bez troška za VARA licencu
    - Ugrađen u Winlink Express

=== "Packet (AX.25)"
    Klasični VHF packet radio, pouzdani za lokalnu mrežu.
    - Korišten već od 1980-ih, dobro testiran
    - 1200 bps (ili 9600 bps na UHF)
    - Temelj za APRS infrastrukturu

---

## Softver — Winlink Express

**Winlink Express** je besplatni klijentski software za Windows koji integrira sve Winlink funkcionalnosti:

- Download: [winlink.org/downloads](https://winlink.org/downloads)
- Besplatan za radioamatere (prijava s pozivnom oznakom)
- Podržava sve Winlink modove (VARA, ARDOP, Packet, Telnet)
- Ugrađeni editor poruka sličan e-mail klijentu
- **ICS obrasci** — standardizirani obrasci civilne zaštite za EmComm

!!! tip "Winlink Express na Linux/Mac"
    Winlink putem Pat klijenta (besplatan, open-source) dostupan je na macOS i Linux: [getpat.io](https://getpat.io). Alternativno, Winlink Express radi pod Wine na Linuxu.

---

## Oprema za Winlink

### Minimalna konfiguracija (VHF/UHF)

| Komponenta | Primjer | Cijena |
|---|---|---|
| Računalo / laptop | Stariji Windows laptop je sasvim ok | — |
| VHF/UHF transceiver | Icom IC-2300H, Yaesu FT-8900R | 100–200 € |
| SignaLink USB | Zvučna kartica sučelje radio-PC | ~90–110 € |
| Kabel za radio | Specifičan za model transceivera | 10–30 € |

### Napredna konfiguracija (HF s VARA)

| Komponenta | Primjer | Cijena |
|---|---|---|
| HF transceiver | Icom IC-7300, Yaesu FT-991A | 700–1500 € |
| VARA HF licenca | Za punu brzinu (opcionalno) | ~69 $ |
| CAT kabel | USB-Serial za CAT kontrolu radia | 10–30 € |
| SignaLink USB | Audio sučelje | ~90–110 € |

!!! note "Icom IC-7300 i interna zvučna kartica"
    Icom IC-7300 ima ugrađenu USB zvučnu karticu i CAT — povezujete samo jedan USB kabel na računalo i Winlink Express prepoznaje radio bez SignaLink adaptera. Idealna kombinacija za Winlink.

---

## ICS obrasci u Winlinku

**ICS (Incident Command System)** standardizirani su obrasci koje koriste hitne službe diljem svijeta za dokumentiranje i prenošenje kritičnih informacija. Winlink Express ugrađuje ICS obrasce u digitalni format:

| Obrazac | Namjena |
|---|---|
| **ICS-213** | Opća poruka (General Message) |
| **ICS-214** | Evidencija aktivnosti (Activity Log) |
| **ICS-309** | Komunikacijski log (Communications Log) |
| **Red Cross DDS** | Američki Crveni križ — izvještaj o pritisku katastrofe |
| **HICS-215A** | Bolnički komunikacijski obrazac |

U EmComm situaciji, bolnica, sklonište ili koordinacijski centar može primiti ICS-213 obrazac koji je netko poslao bežičnim Winlink-om i obraditi ga kao strukturirani dokument — bez tipkanja iste informacije opet.

---

## Winlink Gateway mreža u HR okolici

Regionalni HF i VHF Winlink gateway-i koji su dostupni iz Hrvatske:

| Postaja | Zemlja | Mod | Frekvencija |
|---|---|---|---|
| 9A5ST-10 | Hrvatska | Pactor/VARA | HF (provjeri na winlink.org) |
| OE postaje | Austrija | VARA HF | Višestruke HF frekvencije |
| I postaje | Italija | VARA HF | Višestruke HF frekvencije |
| S5 postaje | Slovenija | VARA FM / HF | VHF + HF |

Za aktualni popis gateway-a i njihove frekvencije koristite mapu na [winlink.org/map](https://winlink.org/map).

---

## Praktičan test — probna poruka

Prije nego se nađete u pravoj EmComm situaciji, vježbajte slanjem testnih poruka:

1. Instalirajte Winlink Express i registrirajte se (vaša amaterska pozivna oznaka je login)
2. Podesite SignaLink ili CAT vezu s radiom
3. Odaberite mod (za početak: Telnet ako imate internet — za test bez radija)
4. Pošaljite poruku na `WLNK-1@winlink.org` — bot koji odgovara s potvrdom
5. Provjerite inbox za odgovor

Kad testni mod radi, ponovite isto bez interneta (VARA FM ili HF) — to je pravi test.

!!! example "Winlink vježba"
    Svake prve nedjelje u mjesecu, globalna Winlink vježba potiče operatore da pošalju testnu EmComm poruku. Detalji na [winlink.org](https://winlink.org). Sudjelovanjem vježbate proceduru i vaša postaja ostaje "vidljiva" u sustavu.

---

## Povezane teme

- [RMZO](rmzo.md) — hrvatska EmComm organizacija i frekvencije
- [Postupci u hitnim situacijama](procedures.md) — radio disciplina i poruke
- [Rad u pokretu](../activities/portable.md) — portabl postava za EmComm
- [Modovi rada](../operating/modes.md) — digitalni modovi općenito
