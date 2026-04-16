# Winlink — Email Without the Internet

**Winlink** is a global network that enables sending and receiving **email messages via radio**, without relying on internet infrastructure. In crisis situations — when telephone networks and the internet are unavailable — Winlink remains operational as long as there is a radio signal.

Winlink is used by emergency services, the Red Cross, Coast Guard, ARES teams, and thousands of amateur radio operators for regular digital communication and EmComm exercises.

---

## How Winlink Works

The Winlink system has three elements:

```
[Your computer + radio]
        │
        │ (RF signal — HF or VHF/UHF)
        ▼
[Gateway / RMS station]
(amateur radio station connected to the internet)
        │
        │ (internet)
        ▼
[CMS — Winlink Central Message Server]
(cloud system that stores and forwards messages)
        │
        ├── → Winlink users (retrieve via radio or web)
        └── → Regular internet email recipients
```

**Key advantage:** Your message travels **by radio** to a gateway station that has internet access. You have no internet — but the gateway does, and it forwards the message onwards. Via HF (shortwave) you can connect to a gateway in another country thousands of kilometres away — even if all local infrastructure is completely down.

---

## Winlink Operating Modes

Winlink supports several data transmission modes:

=== "VARA HF"
    The most modern HF mode, high throughput, robust in difficult conditions.
    - Frequency range: HF (3–30 MHz)
    - Software: VARA HF modem (free for 1,200 bps, paid for full speed)
    - Recommended speed: up to 8,400 bps in good conditions
    - **Recommended for EmComm HF work**

=== "VARA FM"
    FM version for VHF/UHF repeaters and simplex frequencies.
    - Frequency range: VHF/UHF (144 MHz, 432 MHz)
    - Fast and reliable for local connections
    - Excellent for coordination within a town or region
    - **Recommended for local EmComm VHF work**

=== "Pactor"
    Older but robust HF mode, popular in maritime and ARES communities.
    - Requires a hardware Pactor TNC modem (SCS, ~€400–600)
    - Excellent throughput for HF, especially on DX links
    - Used in maritime and expedition stations

=== "ARDOP"
    Free open-source HF protocol, somewhat slower than VARA but with no licensing cost.
    - Good option for beginners without the VARA licence cost
    - Built into Winlink Express

=== "Packet (AX.25)"
    Classic VHF packet radio, reliable for local networks.
    - In use since the 1980s, well proven
    - 1,200 bps (or 9,600 bps on UHF)
    - Foundation for the APRS infrastructure

---

## Software — Winlink Express

**Winlink Express** is the free client software for Windows that integrates all Winlink functionality:

- Download: [winlink.org/downloads](https://winlink.org/downloads)
- Free for amateur radio operators (register with your callsign)
- Supports all Winlink modes (VARA, ARDOP, Packet, Telnet)
- Built-in message editor similar to an email client
- **ICS forms** — standardised civil protection forms for EmComm

!!! tip "Winlink Express on Linux/Mac"
    Winlink via the Pat client (free, open-source) is available on macOS and Linux: [getpat.io](https://getpat.io). Alternatively, Winlink Express runs under Wine on Linux.

---

## Equipment for Winlink

### Minimum configuration (VHF/UHF)

| Component | Example | Price |
|---|---|---|
| Computer / laptop | Older Windows laptop is fine | — |
| VHF/UHF transceiver | Icom IC-2300H, Yaesu FT-8900R | €100–200 |
| SignaLink USB | Audio interface radio-PC | ~€90–110 |
| Radio cable | Specific to transceiver model | €10–30 |

### Advanced configuration (HF with VARA)

| Component | Example | Price |
|---|---|---|
| HF transceiver | Icom IC-7300, Yaesu FT-991A | €700–1,500 |
| VARA HF licence | For full speed (optional) | ~$69 |
| CAT cable | USB-Serial for CAT control | €10–30 |
| SignaLink USB | Audio interface | ~€90–110 |

!!! note "Icom IC-7300 and built-in sound card"
    The Icom IC-7300 has a built-in USB audio interface and CAT — you connect a single USB cable to the computer and Winlink Express recognises the radio without a SignaLink adapter. An ideal combination for Winlink.

---

## ICS Forms in Winlink

**ICS (Incident Command System)** forms are standardised forms used by emergency services worldwide to document and transmit critical information. Winlink Express embeds ICS forms in digital format:

| Form | Purpose |
|---|---|
| **ICS-213** | General Message |
| **ICS-214** | Activity Log |
| **ICS-309** | Communications Log |
| **Red Cross DDS** | American Red Cross disaster damage report |
| **HICS-215A** | Hospital communications form |

In an EmComm situation, a hospital, shelter, or coordination centre can receive an ICS-213 form sent wirelessly via Winlink and process it as a structured document — without re-entering the same information manually.

---

## Winlink Gateway Network in the Croatian Region

Regional HF and VHF Winlink gateways accessible from Croatia:

| Station | Country | Mode | Frequency |
|---|---|---|---|
| 9A5ST-10 | Croatia | Pactor/VARA | HF (verify at winlink.org) |
| OE stations | Austria | VARA HF | Multiple HF frequencies |
| I stations | Italy | VARA HF | Multiple HF frequencies |
| S5 stations | Slovenia | VARA FM / HF | VHF + HF |

For the current gateway list and frequencies, use the map at [winlink.org/map](https://winlink.org/map).

---

## Practical Test — Sending a Test Message

Before you need Winlink in a real EmComm situation, practise by sending test messages:

1. Install Winlink Express and register (your amateur callsign is the login)
2. Configure your SignaLink or CAT connection to the radio
3. Select a mode (for starters: Telnet if you have internet — to test without radio)
4. Send a message to `WLNK-1@winlink.org` — a bot that responds with a confirmation
5. Check your inbox for the reply

Once the test mode works, repeat the same process without internet (VARA FM or HF) — that is the real test.

!!! example "Monthly Winlink exercise"
    Every first Sunday of the month, a global Winlink exercise encourages operators to send a test EmComm message. Details at [winlink.org](https://winlink.org). By participating you practise the procedure and your station remains "visible" in the system.

---

## Related Topics

- [RMZO](rmzo.md) — Croatian EmComm organisation and frequencies
- [Emergency Procedures](procedures.md) — radio discipline and messages
- [Portable Operations](../activities/portable.md) — portable station for EmComm
- [Operating Modes](../operating/modes.md) — digital modes in general
