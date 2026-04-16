# RMZO — Croatian Amateur Radio Emergency Network

**RMZO** (Radioamaterska mreža za opasnost — Amateur Radio Emergency Network) is an organised system within the Croatian Amateur Radio Association that is activated in the event of natural disasters, technical accidents or any situation where standard telecommunications networks are not functioning.

RMZO is not just a list of frequencies — it is an **organisational structure** that defines who coordinates whom, which frequencies are used, what message priorities apply, and how reports are submitted to the competent authorities.

---

## Legal Framework

RMZO operates in cooperation with:
- **HAKOM** — Croatian Regulatory Authority for Network Industries (assigns special EmComm frequencies)
- **DUZS/MUP Civil Protection Directorate** — government civil protection authority
- **HRS** — coordinates and leads RMZO at the national level
- **112** — integration with the national emergency call centre

The Electronic Communications Act gives priority to communications involving danger to life and property over all other traffic.

---

## Organisational Structure

```
HRS (national coordination)
        │
        ▼
Regional coordinators (by county)
        │
        ▼
Local radio clubs and RMZO operators
        │
        ▼
Field stations (mobile and portable)
```

**Roles in RMZO:**

| Role | Description |
|---|---|
| **Net Control Station (NCS)** | Manages the net, grants permission to transmit, logs all traffic |
| **Relay station** | Forwards traffic between stations that cannot hear each other directly |
| **Field station** | Reports from the disaster location or coordination centre |
| **Base station** | Fixed RMZO station, often a club shack with backup power |

---

## RMZO Frequencies

!!! warning "Frequencies may change"
    Always verify current RMZO frequencies at [hamradio.hr](https://www.hamradio.hr) as they may be updated by HRS and HAKOM decisions. Keep a current list in your portable station.

### HF frequencies (long range, no infrastructure)

| Frequency | Band | Purpose |
|---|---|---|
| **3.675 MHz** | 80 m | Primary national EmComm frequency for Croatia |
| 7.060 MHz | 40 m | Alternative for daytime work (better daytime propagation) |
| 14.300 MHz | 20 m | IARU Region 1 EmComm frequency (international) |

### VHF/UHF frequencies (local range, clarity)

| Frequency | Band | Purpose |
|---|---|---|
| **145.500 MHz** | 2 m | Primary local simplex EmComm frequency |
| 144.800 MHz | 2 m | APRS (automatic packet reporting) |
| 433.500 MHz | 70 cm | UHF simplex working |
| Local repeaters | 2 m / 70 cm | Coordination if backup power is available |

---

## Activation of RMZO

### How is the network activated?

RMZO can be activated in two ways:

1. **Official request** — DUZS/MUP/112 contacts the HRS coordinator and requests activation
2. **Self-initiated** — if it is obvious that communications infrastructure has failed (earthquake, flood, widespread power outage), amateur radio operators can self-organise without waiting for a request

In practice, major disasters trigger both mechanisms simultaneously.

### Activation Phases

**Phase 1 — Monitoring:** Operators listen on EmComm frequencies and monitor the situation without transmitting unless they have urgent information.

**Phase 2 — Net activation:** NCS calls the net and takes over coordination. All stations report their location and availability.

**Phase 3 — Operational work:** Field stations send reports. NCS filters information and forwards it to the competent authorities.

**Phase 4 — Deactivation:** NCS announces the end of the operation. All traffic is archived.

---

## Example Net Opening

```text
NCS: "All stations, all stations — this is 9A1XX, Net Control for the RMZO EmComm net.
      Opening EmComm net on frequency 3.675 MHz at [UTC]. Mode: SSB.
      Stations with urgent traffic — respond immediately.
      All other stations — respond in callsign order when called.
      9A1XX, standing by."

Field station: "9A1XX, this is 9A7YY from Petrinja, I have a Priority report."

NCS: "9A7YY, you have clearance — go ahead with your report."
```

---

## EmComm Go-Bag Contents

A go-bag is a bag or rucksack with equipment ready for rapid field deployment:

| Item | Notes |
|---|---|
| Dual-band handheld (VHF/UHF) | Charged battery + spare |
| HF QRP transceiver | If available (IC-705, KX2, FT-818) |
| LiFePO4 battery 10+ Ah | Independent power source |
| Solar panel 20–30 W | For extended operation |
| Wire antenna (EFHW or dipole) | 10–15 m of wire, connector, short mast |
| Laptop/tablet with Winlink Express | Digital messaging |
| VARA modem or SignaLink | Audio interface for digital modes |
| Log notebook and pens | Paper log always as backup |
| EmComm frequency list | Laminated, in the bag |
| Power adapters | 12 V and 230 V versions |

!!! tip "Test your go-bag regularly"
    Once per quarter: unpack the equipment, verify batteries are charged, make a short QSO as a test. Equipment that hasn't been tested is not reliable equipment.

---

## Field Day — Annual Exercise

**Field Day** is an annual EmComm exercise — amateur radio operators set up portable stations without mains power and make as many QSOs as possible in 24 or 48 hours. The goal is to test:
- Portable equipment
- Backup power
- Operating procedures
- Team coordination

In the USA this is organised by ARRL every June. In Europe and Croatia, clubs organise their own Field Day activities — follow the HRS calendar and club websites.

---

## Related Topics

- [Emergency Procedures](procedures.md) — radio discipline and message protocols
- [Winlink](winlink.md) — digital messages without internet
- [Portable Operations](../activities/portable.md) — portable station
- [Safety](../technical/safety.md) — safe setup in crisis conditions
- [Associations and Organisations](../community/associations.md) — HRS contact and coordination
