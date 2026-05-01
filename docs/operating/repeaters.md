# Repetitori i linklovi

Repetitor (repeater) je automatska radio postaja koja prima vaš signal i odmah ga retransmitira na drugoj frekvenciji s većom snagom i s višeg mjesta. Čak i ručna stanica od 5 W može pokriti čitavu gradsku regiju putem dobrog repetitora.

## Princip rada repetitora

```
Vaš TX (145.200 MHz, ulazna/input) → [Repetitor na brdu] → TX (145.800 MHz, izlazna/output)
Vaš RX sluša: 145.800 MHz (izlaz repetitora)
```

Radio je podešen da odašilje na **ulaznoj** frekvenciji (input) i sluša na **izlaznoj** (output). Razlika između ulaza i izlaza naziva se **offset** ili **shift**.

## Standardni offseti

| Opseg | Input | Output | Offset |
|-------|-------|--------|--------|
| **2 m (144 MHz)** | Output − 600 kHz | 145.000–145.775 MHz | −600 kHz |
| **70 cm (432 MHz)** | Output − 7.6 MHz | 433.xxx–434.xxx MHz | −7.6 MHz |
| **10 m (29 MHz)** | 29.515–29.585 MHz | 29.615–29.685 MHz | +100 kHz |
| **6 m (51 MHz)** | Input − 500 kHz | 51.000–51.475 MHz | −500 kHz (EU) |

!!! tip "Programiranje offseta"
    Na modernim stanicama: unesite output frekvenciju, a transciiver automatski dodaje offset. Za starije radio: ručno programirajte ulaz i izlaz kao dva memorijska kanala.

---

## CTCSS / DCS — Subtonovi i digitalni kodovi

Repetitori često zahtijevaju **subton (CTCSS)** ili **digitalni DCS kod** za aktivaciju. Bez ispravnog tona, repetitor neće reemitirati vaš signal.

### CTCSS (Continuous Tone-Coded Squelch System)

CTCSS je analogni subton (ispod čujnog spektra, 67–254.1 Hz) koji se dodaje vašem signalu. Repetitor ga sluša i otvara squelch samo za stanice s ispravnim tonom.

**Standardni CTCSS tonovi:**

| Ton (Hz) | | Ton (Hz) | | Ton (Hz) |
|----------|---|----------|---|----------|
| 67.0 | | 103.5 | | 162.2 |
| 71.9 | | 107.2 | | 167.9 |
| 74.4 | | 110.9 | | 173.8 |
| 77.0 | | 114.8 | | 179.9 |
| 79.7 | | 118.8 | | 186.2 |
| 82.5 | | 123.0 | | 192.8 |
| 85.4 | | 127.3 | | 203.5 |
| 88.5 | | 131.8 | | 210.7 |
| 91.5 | | 136.5 | | 218.1 |
| 94.8 | | 141.3 | | 225.7 |
| 97.4 | | 146.2 | | 233.6 |
| 100.0 | | 151.4 | | 241.8 |
| | | 156.7 | | 250.3 |

### DCS (Digital Coded Squelch)

DCS koristi digitalnu poruku umjesto analognog tona — 3 oktalna cifre (npr. `023`, `071`, `114`). Robustniji od CTCSS u uvjetima zamiranja signala.

### Postavljanje CTCSS u transciiveru

*   Yamaha/Icom/Kenwood: CTCSS se obično postavlja u menu pod "Tone", "CTCSS TX", "Encode"
*   Baofeng/TYT: Directno unosite u memor kanal uz frekvenciju

!!! note "Gdje pronaći CTCSS za vaš repetitor"
    Svaki repetitor ima dokumentirani CTCSS ton. Pronađite ga na:
    - [RepeaterBook.com](https://www.repeaterbook.com) (globalna baza)
    - Web stranici vašeg radiokluba
    - HRS popis repetitora na [hamradio.hr](https://www.hamradio.hr/)

---

## Tipovi repetitora

### Analogni FM repetitor

Najčešći — standardni FM rad. Svaka ručna stanica može ga koristiti bez posebne opreme.

### DMR (Digital Mobile Radio)

Digitalni repetitor koji koristi TDMA (Time Division Multiple Access):
*   2 vremenska slota (timeslot) na istoj frekvenciji → 2 simultana QSO-a
*   **Colour Code** (CC): Ekvivalent CTCSS-a za DMR (CC 1–15)
*   **Talk Groups** (TG): Grupni kanali — TG 91 (WorldWide), TG 222 (Italija), TG 219 (Hrvatska)
*   Mreže: **Brandmeister**, **DMR-MARC**, **FreeDMR**
*   Oprema: Radio s DMR podrškom (Anytone 868/878, Motorola DP3400, TYT MD-380)

### D-STAR (Icom)

Digitalni protokol Icom korporacije:
*   **DV (Digital Voice)**: Digitalni glas
*   **DD (Digital Data)**: Podaci (do 128 kbps)
*   **Reflektori**: DCS001C (Europa), REF030C (svjetski)
*   Koristi **AMBE+2** codec
*   Registracija callsign-a na [D-STAR registar](https://www.dstarusers.org)

### System Fusion (Yaesu WIRES-X)

Yaesuov digitalni sustav:
*   C4FM modulacija
*   **Hybrid repeater**: Automatski prelazi između analognog i digitalnog
*   **WIRES-X**: Internet linking sustav
*   Kompatibilan s analognim FM (Yaesu radio može raditi i analogno)

### Hotspot

Osobni mali repetitor koji se spaja na internet i simulira repetitor za DMR/D-STAR/Fusion:
*   **SharkRF OpenSpot**: Popularan komercijalni hotspot
*   **MMDVM**: Open source sustav, DIY hotspot (Raspberry Pi + RF modul)
*   Radi na 430 MHz (70 cm) simpleks frekvencijama
*   Koristite s Brandmeister ili TGIF mreža

---

## EchoLink — Internet linking

EchoLink spaja radioamaterske repetitore i simplex frekvencije putem interneta:

*   Svaka stanica s EchoLink softverom može raditi s globalnom mrežom
*   Može se koristiti čak i bez radija (direktno računalom ili mobitelom)
*   Licenciranim amaterima — zahtijeva verifikaciju callsign-a

**Registracija:** [echolink.org](https://www.echolink.org)

**Pristup EchoLink repetitoru putem radija:**
1.  Pozovite repetitor (CTCSS ton)
2.  Unesite EchoLink broj čvora DTMF tipkama (npr. `123456#`)
3.  Repetitor se spaja na taj EchoLink čvor
4.  Govorite normalno

**DTMF kontrole:**
*   `#` → Odspoji (disconnect)
*   `*` + broj → Spoji na čvor
*   `0` → Status (tko je spojen)

---

## APRS putem repetitora

Neki repetitori podržavaju **APRS Digipeater** (Automatic Packet Reporting System):

*   **Frekvencija**: 144.800 MHz (EU), 144.390 MHz (SAD)
*   **Mod**: 1200 baud AFSK na FM
*   APRS šalje GPS poziciju, vremensku prognozu, poruke
*   Pratite live na [aprs.fi](https://aprs.fi)

Oprema za APRS:
*   Kenwood TM-D710, VX-8DR, FTM-400 — ugrađeni APRS
*   Bilo koji FM radio + TNC (Terminal Node Controller) ili Bluetooth TNC
*   iOS/Android: APRSDroid app + Bluetooth TNC

---

## Kako pronaći lokalne repetitore

### Hrvatska

*   **HRS popis**: [hamradio.hr](https://www.hamradio.hr/) → Repetitori
*   Tipično: 145.XXX MHz + CTCSS ton

### Europa

*   [**RepeaterBook.com**](https://www.repeaterbook.com) — Globalna baza svih repetitora
*   [**UKRepeater.net**](https://www.ukrepeater.net) — UK baza
*   [**Brandmeister Network**](https://brandmeister.network/?page=repeaters) — DMR mapa

### Aplikacije

*   **RepeaterBook** (iOS/Android) — GPS baza lokalno dostupnih repetitora
*   **DMR Contact Manager** — Kontakti i talk groups za DMR

---

## Repetitorska etiketa

1.  **Pauza između prijenosa**: Uvijek napravite kratku stanku (1–2 s) između predaje — daje prostor za hitne pozive i ID tona repetitora
2.  **Identificirajte se**: Koristite svoju pozivnu oznaku svaka 10 minuta i na početku/kraju
3.  **Kratke provjere**: `"9A1ABC, checking in"` — ne morate pisati esej za check-in
4.  **Simplex za duge QSO**: Ako vodite dug razgovor, dogovorite se s partnerom i prijeđite na simplex frekvenciju — oslobodite repetitor

!!! warning "Šumovi i supruge repetitora"
    Repetitor koji nema CTCSS ton može se aktivirati šumom. Nemojte namjerno aktivirati repetitore bez razloga — smetate ili trošite bateriju solar/baterijski repetitor.

---

## Programiranje memorije radija

### Baofeng UV-5R primjer (Linux/Mac: CHIRP, Windows: programski kabel)

1.  Instalirajte CHIRP: [chirpmyradio.com](https://chirpmyradio.com)
2.  Spojite radio USB kabelom, učitajte memoriju ("Download from radio")
3.  Dodajte memorijski kanal:
    *   Frekvencija: Output repetitora (npr. 145.800 MHz)
    *   Duplex: `-` (minus)
    *   Offset: 0.600 MHz
    *   CTCSS: Unesite ton (npr. 88.5 Hz)
    *   Name: Ime repetitora (npr. "9A0BB ZG")
4.  Upload na radio

### Yaesu FT-70D / FTM-400 programiranje

Koristite RT Systems software ili manualno kroz menu:
*   VFO mode → podesite frekvenciju output-a
*   RPT → definirajte offset tip (−) i vrijednost
*   TONE → CTCSS → unesite ton
*   MWRT → spremi u memoriju

---

## Povezane teme

*   [Modovi rada](modes.md) — Digitalni modovi (DMR, D-STAR, Fusion)
*   [APRS](aprs.md) — Automatski reporting sustav
*   [Frekvencijski planovi](bandplans.md) — VHF/UHF repetitorski segmenti
*   [Prva veza](first_qso.md) — Repetitorski QSO kao prvi korak
