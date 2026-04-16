# CB Regulations and Channels

CB radio in Europe and Croatia uses **40 channels** in the 26.965–27.405 MHz frequency band. Each channel has a fixed frequency — unlike amateur radio where operators can tune freely across a band, CB users follow a prescribed channel plan.

---

## Permitted Technical Parameters (Croatia / EU)

| Parameter | Value |
|---|---|
| Frequency range | 26.960 – 27.410 MHz |
| Number of channels | 40 (standard European plan) |
| Channel spacing | 10 kHz |
| AM modulation | Permitted, max. 4 W carrier (ERP) |
| FM modulation | Permitted, max. 4 W (ERP) |
| SSB modulation | Permitted, max. 12 W PEP |
| Antenna gain | Not separately restricted; device must be type-approved |
| Standard | EN 300 433 (EU) |
| Regulatory body (HR) | HAKOM |
| Licence | Not required (general authorisation) |

!!! note "AM vs FM vs SSB — which modulation?"
    - **AM** (Amplitude Modulation) is the original CB modulation — cuts through well, compatible with all radios, but less efficient (55% of power goes into the carrier which carries no information)
    - **FM** (Frequency Modulation) is cleaner, less susceptible to noise and interference — preferred for local work
    - **SSB** (Single Sideband) is the most efficient — all power goes into the speech signal, giving 2–3× the range. Essential for DX work. LSB (Lower Sideband) is the CB SSB convention.

---

## Complete 40-Channel Table

| Channel | Frequency (MHz) | Notes |
|:---:|:---:|:---|
| 1 | 26.965 | |
| 2 | 26.975 | |
| 3 | 26.985 | |
| 4 | 27.005 | |
| 5 | 27.015 | |
| 6 | 27.025 | |
| 7 | 27.035 | |
| 8 | 27.055 | Alpha channel (27.045) |
| **9** | **27.065** | **🚨 Emergency channel only — do not use for normal QSOs!** |
| 10 | 27.075 | |
| 11 | 27.085 | |
| 12 | 27.105 | Alpha channel (27.095) |
| 13 | 27.115 | |
| 14 | 27.125 | |
| 15 | 27.135 | |
| 16 | 27.155 | Alpha channel (27.145) |
| 17 | 27.165 | |
| 18 | 27.175 | |
| **19** | **27.185** | **🚛 Road / Truckers (EU standard)** |
| 20 | 27.205 | Alpha channel (27.195) |
| 21 | 27.215 | |
| 22 | 27.225 | |
| 23 | 27.255 | Alpha channels (27.235 and 27.245) |
| 24 | 27.235 | |
| 25 | 27.245 | |
| 26 | 27.265 | |
| 27 | 27.275 | |
| 28 | 27.285 | |
| 29 | 27.295 | |
| 30 | 27.305 | |
| 31 | 27.315 | |
| 32 | 27.325 | |
| 33 | 27.335 | |
| 34 | 27.345 | |
| 35 | 27.355 | |
| 36 | 27.365 | |
| 37 | 27.375 | |
| 38 | 27.385 | SSB channel (LSB/USB) — DX |
| 39 | 27.395 | SSB channel — DX |
| 40 | 27.405 | SSB channel — DX |

---

## Reserved and Conventional Channels

### Channel 9 — Emergency Channel 🚨

Channel 9 (27.065 MHz) is the internationally recognised **emergency channel**. Reserved exclusively for:
- Calling for help in emergencies (accidents, missing persons, vehicle breakdowns)
- Communication with CB-equipped emergency services
- Coordination during disasters

!!! danger "Channel 9 is not for conversation"
    Using Channel 9 for normal chat or "testing equipment" is prohibited and irresponsible — someone in need of help may be unable to reach the frequency.

### Channel 19 — Road 🚛

Channel 19 (27.185 MHz) is the European standard for driver communication on motorways and main roads. Drivers exchange:
- Traffic conditions and accident reports
- Speed camera warnings
- Calling and switching to working channel

Standard practice: **call on Ch19, switch to a free channel for the conversation.**

### Channels 38–40 — SSB DX

Channels 38, 39 and 40 are the conventional SSB DX channels. LSB is the standard for CB SSB communication. On these channels you can hear contacts with operators from across Europe.

### Alpha Channels

"Alpha" (or "A") channels are intermediate frequencies included in Australian and American CB channel plans (e.g. 27.045 MHz between channels 7 and 8). The European standard plan does not include these as standard channels, but some CB radios may have the capability to access them.

---

## Legal Framework in Croatia

CB radio use in Croatia is governed by:

- **Electronic Communications Act** (ZEK) — NN 73/08 and amendments
- **Ordinance on conditions and manner of using the radio spectrum** — HAKOM
- European Decision **2006/771/EC** and amendment **2013/752/EU** — harmonises CB across the EU

**Key rules:**
1. Devices must carry a **CE mark** and be type-approved to EN 300 433
2. Modifying or amplifying the device beyond permitted power is prohibited
3. Interfering with emergency communications (Channel 9) is prohibited
4. Broadcasting music, advertisements, or content that interferes with communications is prohibited

!!! warning "Amplifiers (linear amplifiers) are illegal"
    Amplifiers that raise CB power above 4 W (AM/FM) or 12 W (SSB) are **illegal** in the EU and Croatia. HAKOM can:
    - Issue fines
    - Confiscate equipment
    - Initiate criminal proceedings for intentional interference

---

## International Differences

The CB channel plan is not entirely unified — regional differences exist:

| Region | Standard | Notes |
|---|---|---|
| Europe (EU) | CEPT, 40 channels | Identical frequency plan, FM dominant |
| USA | FCC, 40 channels | Same plan, AM more dominant, same power |
| Australia | ACMA, 40 channels | Slightly different plan + alpha channels |
| Japan | MIC, 40 channels | Completely different plan and power |

For international DX CB communication, SSB on channels 38–40 is the de facto standard among European operators.

---

## Related Topics

- [CB Equipment](equipment.md) — choosing a radio and antenna
- [Introduction to CB](intro.md) — history and broader context
- [Radio Wave Propagation](../technical/propagation.md) — why CB DX works only occasionally
- [Band Plans](../operating/bandplans.md) — comparison with amateur band plans
