# Contesting

Ham radio contesting is the "competitive sport" of the hobby — organised events where the goal is not a lengthy conversation, but rather making as many contacts as possible within a set time frame. Contests are an excellent way to stress-test your station and operating skills, meet operators from around the world, and earn awards and placements.

If you've ever worked QSO after QSO on 20 m during a great opening, you're already close to contesting — all that's missing is a logger and a bit of strategy.

---

## What Is a Contest QSO?

Unlike a regular ragchew where you exchange names, locations, and equipment details, a contest exchange take665      ghhhhhhhhhhhfggggggggggggggggggggggggggggggggs **only a few seconds**. Every contest has a prescribed exchange format: typically a signal report (59 or 599) plus one additional element that scores points — CQ zone, ITU zone, serial number, grid locator, and so on.

Speed and accuracy matter more than the quality of conversation.

### Example SSB Exchange (CQ WW DX)

```text
9A1ZG: "CQ Contest, CQ Contest, Niner Alpha One Zulu Golf, 9A1ZG"
DJ3AB: "DJ3AB"
9A1ZG: "DJ3AB, 59, 15"          ← signal report 59, CQ zone 15 for Croatia
DJ3AB: "59, 14"                  ← signal report 59, CQ zone 14 for Germany
9A1ZG: "73, QRZ? 9A1ZG"
```

The entire exchange takes 10–20 seconds. Experienced contesters aim for under 10.

### Example CW Exchange

```text
9A1ZG: CQ TEST 9A1ZG 9A1ZG
DJ3AB: DJ3AB
9A1ZG: DJ3AB 599 001     ← RST 599, our serial number: 001
DJ3AB: 599 088           ← RST 599, his serial number: 088
9A1ZG: TU 9A1ZG
```

!!! tip "Why always 59 or 599?"
    In contests, nearly everyone sends a report of 59 or 599 regardless of actual signal quality. This is a convention — the goal is to exchange the required data as quickly as possible, not to evaluate the signal. Exceptions exist in contests that score based on real reports (e.g., the Worked All Germany contest).

---

## Operator Categories

To keep contests fair, participants submit their log in one of several defined categories, based on the number of operators, transmitter power, and use of the DX cluster (a spotting network that alerts you to active stations):

| Category | Description | Max TX | DX Cluster? | Typical use |
|---|---|---|---|---|
| **Single Op (SO)** | One operator doing everything — frequency management, logging, calling CQ | 1 | No | Beginners and solo experts alike |
| **Single Op Assisted (SOA)** | One operator, but with access to the DX cluster for spots | 1 | Yes | Great for hunting rare entities |
| **Multi Single (M/S)** | Multiple operators, but only one transmitter active at any given time | 1 | Yes | Club teams sharing operating duties |
| **Multi Two (M/2)** | Multiple operators, two transmitters running simultaneously on different bands | 2 | Yes | Organised club stations |
| **Multi Multi (M/M)** | Multiple operators, one transmitter per band running simultaneously | Unlimited | Yes | Large DX expeditions and mega stations |
| **QRP** | Maximum output power of 5 W | 1 | Varies | Enthusiasts of minimalist stations |

In addition to these main categories, many contests offer **overlay categories** — supplemental divisions you compete in simultaneously:

- **Rookie** — licensed for fewer than 3 years
- **Classic** — no assistance and no remote operation
- **Youth** — operators under 25 years of age

!!! note "Choose your category carefully"
    When you submit your log, you declare a category. Entering Low Power when you ran 100 W is grounds for disqualification. Operators in the same category compete against each other — getting the category right puts you on a level playing field.

---

## Scoring — Why Multipliers Matter

In almost every contest, your final score is not just a sum of contacts but the **product of QSO points and multipliers**:

$$\text{Score} = \sum \text{QSO Points} \times \sum \text{Multipliers}$$

**What are multipliers?** Special targets you can claim once per band (or once per contest) — for example, each CQ zone, each country (DXCC entity), each US state, each grid square... A single new multiplier can be worth more than a dozen "ordinary" QSOs.

### Scoring in CQ WW DX (the world's largest contest)

| Element | Scoring rule |
|---|---|
| QSO with your own country (9A ↔ 9A) | 0 points |
| QSO within the same continent (EU ↔ EU) | 1 point |
| QSO across continents (HR ↔ USA, JA, VK...) | 3 points |
| Multipliers — CQ zones | Each new zone, once per band |
| Multipliers — DXCC entities | Each new country, once per band |

!!! example "Score calculation example"
    An operator makes **800 QSOs** in 24 hours — 300 within Europe (1 point each) and 500 across continents to North America, Asia, and Oceania (3 points each).

    - QSO points: 300 × 1 + 500 × 3 = **1,800 points**
    - Multipliers: 38 CQ zones + 120 DXCC countries = **158 multipliers**
    - **Total score: 1,800 × 158 = 284,400 points**

    This is why working a rare station from zone 26 or a tiny island DXCC entity is far more valuable than ten contacts with common European stations.

---

## Major Contest Calendar

Contests run throughout the year. Here are the most significant events you'll encounter:

| Contest | Mode | Typical Date | Exchange | Rules |
|---|---|---|---|---|
| **CQ WW DX SSB** | SSB | Last weekend of October | RS + CQ zone | [cqww.com](https://cqww.com) |
| **CQ WW DX CW** | CW | Last weekend of November | RST + CQ zone | [cqww.com](https://cqww.com) |
| **CQ WPX SSB** | SSB | Last weekend of March | RS + serial number | [cqwpx.com](https://cqwpx.com) |
| **CQ WPX CW** | CW | Last weekend of May | RST + serial number | [cqwpx.com](https://cqwpx.com) |
| **ARRL DX SSB** | SSB | 3rd weekend of February | RS + US state or power | [arrl.org](https://www.arrl.org/) |
| **ARRL DX CW** | CW | 3rd weekend of March | RST + US state or power | [arrl.org](https://www.arrl.org/) |
| **WAE DX CW** | CW | 2nd weekend of August | RST + QTC blocks | [darc.de](https://www.darc.de/) |
| **WAE DX SSB** | SSB | 2nd weekend of September | RS + QTC blocks | [darc.de](https://www.darc.de/) |
| **IOTA Contest** | SSB/CW | Last full weekend of July | RS(T) + serial or IOTA ref. | [rsgbcc.org](https://www.rsgbcc.org/) |
| **9A DX Contest** | SSB/CW | 3rd weekend of December | RS(T) + county (9A) / ITU zone (DX) | [hamradio.hr](https://www.hamradio.hr) |

!!! warning "WARC bands — no contesting allowed"
    The **30 m (10 MHz)**, **17 m (18 MHz)**, and **12 m (24 MHz)** bands are WARC bands. By international agreement (IARU), organising or participating in contests on these bands is prohibited. They serve as "quiet zones" for normal QSOs and propagation research. See [Band Plans](../operating/bandplans.md) for details.

---

## Contest Logging Software

In a contest you don't log manually — you use specialised software that integrates with your radio (CAT control), checks duplicates automatically, displays multipliers in real time, and generates a Cabrillo log for submission.

=== "N1MM+ Logger"
    The most popular free contest logger for Windows. Used by everyone from first-time contesters to world champions.

    - **Strengths:** Supports 1,000+ different contests, excellent CAT integration with virtually any radio, voice keyer for automated SSB calls, a large active community with detailed documentation.
    - The built-in **rate meter** shows your contacts per hour in real time.
    - **Download:** [n1mmwp.hamdocs.com](https://n1mmwp.hamdocs.com/)
    - **Price:** Free

=== "DXLog.net"
    A modern, fast, and highly capable logger, especially favoured by Multi-Op stations. Developed partly by Croatian contesters.

    - **Strengths:** Excellent networked logging for M/S and M/M categories, real-time LAN synchronisation within the station, cloud backup of logs.
    - Supports all major contests with a clean modern UI.
    - **Download:** [dxlog.net](http://dxlog.net/)
    - **Price:** Free for amateur use

=== "Win-Test"
    A classic that serious contesters and large stations rely on. Based on the keyboard shortcuts of the legendary CT logger from the 1980s.

    - **Strengths:** Extremely stable, decades of proven use, supported at all serious Multi-Multi stations worldwide.
    - **Download:** [win-test.com](http://www.win-test.com/)
    - **Price:** Paid shareware (~€50)

!!! tip "Start with N1MM+"
    Install N1MM+, run through the setup wizard (callsign, CAT port), and try it **a week before** the contest — not on contest day. Every major contest has a preconfigured template in N1MM+ and you can be logging within minutes.

---

## Strategy

Contesting is not just about antenna gain — strategy plays a huge role.

### Running vs. Search & Pounce (S&P)

**Running** means holding your own clear frequency and calling `CQ TEST` continuously. Stations find you and respond. This is productive when you have a strong signal and a free spot on the band, but it requires a solid antenna and favourable propagation.

**Search & Pounce (S&P)** means tuning across the band, finding stations calling CQ, and answering them. This is ideal for beginners because you don't need to "hold" a frequency, and you still accumulate QSOs and multipliers efficiently.

**Practical approach:** Start S&P to collect multipliers from rare entities, then — if you find a quiet gap on the band — try a short CQ run and see who responds.

### Rate vs. Multipliers

Operators sustaining 200 QSOs/hour almost always prefer to keep running rather than interrupt the flow for a single multiplier. But the maths shifts when rate is lower: one unique multiplier can be worth more than 10–20 ordinary QSOs.

**Simple rule of thumb:** When your rate drops below 50 QSOs/hour, it's worth pausing to hunt for new multipliers across the band.

### Band Hopping and Propagation

Propagation changes throughout the day and night. 20 m is open to North America in the UTC afternoon; 40 m and 80 m perform best for DX at night; 15 m and 10 m only shine when solar flux (SFI) is elevated above ~120. For a deeper dive, see [Radio Wave Propagation](../technical/propagation.md).

!!! info "The grey line — a contester's golden hour"
    The twilight zone (grey line) moving across the Earth at sunrise and sunset creates brief but exceptional propagation windows. Experienced contesters plan their most intensive activity around these intervals to capture multipliers from the most distant parts of the world.

---

## 9A Contests (Croatia)

The Croatian Amateur Radio Association (HRS) organises and supports several traditional contests:

The **9A DX Contest** is the main Croatian contest, open to all stations worldwide. It runs on the third weekend of December, from Saturday 14:00 UTC to Sunday 13:59 UTC, across the 160–10 m bands in mixed mode (SSB and CW).

- Exchange for **9A stations**: RS(T) + two-letter county abbreviation (ZG = Zagreb, ST = Split, RI = Rijeka, OS = Osijek, etc.)
- Exchange for **DX stations** (outside Croatia): RS(T) + ITU zone
- **Scoring:** Contacts with 9A stations carry additional multiplier value
- Submit your Cabrillo log to [hamradio.hr](https://www.hamradio.hr/9a-dx-contest/) within 7 days of the contest closing.

**9A Activity Contests** are regular VHF/UHF events encouraging on-air activity on 144 MHz, 432 MHz, and 1,296 MHz. They use IARU grid locators for exchanges and are great for testing antennas and getting a feel for the contest format at lower stakes.

For the current calendar of Croatian and HRS-organised contests, visit [www.hamradio.hr](https://www.hamradio.hr).

---

## Submitting Your Log — Cabrillo Format

After the contest, you submit your log to the organiser in the standardised **Cabrillo format** — a plain-text file with a header and a list of every QSO. All contest loggers generate Cabrillo with a single click.

In N1MM+: `File → Generate Cabrillo Log`

!!! info "Example Cabrillo file"
    ```text
    START-OF-LOG: 3.0
    CALLSIGN: 9A1ZG
    CONTEST: CQ-WW-SSB
    CATEGORY-OPERATOR: SINGLE-OP
    CATEGORY-ASSISTED: NON-ASSISTED
    CATEGORY-BAND: ALL
    CATEGORY-POWER: LOW
    CLAIMED-SCORE: 284400
    OPERATORS: 9A1ZG
    NAME: Jasmin Surname
    ADDRESS: Zagreb, Croatia
    CREATED-BY: N1MM+ 1.0.10234.0
    ...
    QSO: 14195 PH 2024-10-26 1201 9A1ZG         59 15   DJ3AB         59 14
    QSO: 14195 PH 2024-10-26 1203 9A1ZG         59 15   W1ABC         59 05
    END-OF-LOG:
    ```

Log submission deadlines are typically 5–7 days after the contest ends. Even if you only have 20 QSOs — submit your log! You receive a certificate of participation and your result appears in the official statistics, which is valuable data for the organisers too.

---

## Getting Started — A Guide for First-Time Contesters

Contesting can look intimidating from the outside, but the entry point is simple:

1. **Install N1MM+** — it's free. Launch it, enter your callsign, and configure your CAT connection to the radio. Do this a few days before the contest, not on the day.
2. **Choose a lower-pressure contest to start** — the 9A Activity Contest (VHF) or the IOTA Contest are good first choices. CQ WW is excellent but the sheer volume of stations can be overwhelming for a first outing.
3. **Enter Single Op Low Power** — no pressure, and you'll be comparing yourself only with operators in the same class.
4. **Work S&P only at first** — tune the VFO, find stations calling CQ TEST, and answer them. You don't need to hold a frequency or worry about running.
5. **Participate for 2–4 hours, not 48** — get a feel for the rhythm, the logging, and the S&P flow. A full weekend contest is a challenge for next time.
6. **Always submit your log** — even with 15 QSOs. N1MM+ generates Cabrillo in seconds, and every submitted log counts.

!!! tip "You don't need a big station"
    Excellent contesters regularly achieve strong results with a dipole and 100 W. Strategy, propagation knowledge, and operating skill outweigh raw power. Start with what you have.

---

## Related Topics

- [Operating Procedures](../operating/procedures.md) — QSO procedure and Q-codes
- [Band Plans](../operating/bandplans.md) — which bands for which modes
- [Radio Wave Propagation](../technical/propagation.md) — when to work which bands
- [Antennas and Feed Lines](../technical/antennas.md) — the investment that pays off most in contesting
- [Portable Operations — SOTA/POTA](portable.md) — portable activations as an alternative
