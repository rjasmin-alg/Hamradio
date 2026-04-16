# Satellite Communications

Amateur radio operators have their own satellites in orbit — and you can use them with a handheld radio and a homemade antenna. Satellite communications ("sat") is one of the most technically fascinating branches of the hobby, combining orbital mechanics, Doppler physics, and RF engineering.

There are currently more than 20 active amateur satellites in various configurations — from simple FM repeaters accessible with a handheld, to advanced linear transponders for SSB and CW contacts.

---

## How Do Amateur Satellites Work?

Most amateur satellites are **"flying repeaters"** — they receive a signal from Earth (uplink), amplify it, and retransmit it back (downlink) on a different frequency.

| Term | Explanation |
|---|---|
| **Uplink** | The frequency on which you transmit your signal toward the satellite |
| **Downlink** | The frequency on which you receive the satellite (it transmits toward Earth) |
| **Mode** | The uplink/downlink band combination (e.g. Mode V/U = VHF up, UHF down) |
| **Transponder** | A linear "repeater" that passes an entire frequency segment — not just FM, but SSB and CW too |
| **Footprint** | The geographic area from which the satellite is accessible (visible) at any given moment |

### Satellite Types

**FM satellites** (easier to use):
- Work like a standard FM repeater, but orbiting in space
- A handheld transceiver (5 W) and a simple Yagi held in your hand are sufficient
- Examples: SO-50, AO-91, AO-92

**Linear transponder satellites** (more advanced):
- Pass an entire frequency band — SSB, CW, and digital modes simultaneously in a "window"
- Allow multiple simultaneous contacts (not simplex like FM)
- Require better equipment and tracking antennas (azimuth/elevation rotators)
- Examples: AO-7, FO-29, CAS-4A/B, XW-2 series

---

## Doppler Correction — The Key Challenge

Amateur satellites travel at ~7.8 km/s (LEO — low Earth orbit). At that speed, the Doppler effect (the same shift you hear when an emergency vehicle passes you — the siren changes pitch) causes a measurable frequency shift:

- At **145 MHz**: Doppler shift can be up to ±3.5 kHz
- At **435 MHz**: Shift can be up to ±10 kHz

**In practice:** At the start of a pass, the satellite is approaching — frequency appears higher (you need to listen slightly above the nominal downlink). At the end of the pass, it recedes — frequency drops. You correct the frequency on your receiver manually or automatically throughout the pass.

Software such as **Gpredict** does this automatically in combination with CAT control of the radio.

$$\Delta f = \frac{v}{c} \times f_0$$

where $v$ is the radial velocity of the satellite toward/away from you, $c$ is the speed of light, and $f_0$ is the nominal frequency.

!!! tip "For FM satellites — manual correction is fine"
    On FM satellites, the Doppler shift is not fatal — if you are 2 kHz off nominal, the FM squelch will still open. Manual correction every 30–60 seconds is perfectly sufficient.

---

## When and Where Is the Satellite Visible?

Amateur satellites in low Earth orbit (LEO) pass over your location several times a day, but each pass lasts only **8–15 minutes**. You need to know precisely when and in which direction.

### Tracking Tools

| Tool | Platform | Description |
|---|---|---|
| **Gpredict** | Win/Linux/Mac | Desktop tracker, CAT integration for Doppler, free |
| **ISS Detector** | Android/iOS | Simple mobile tracker focused on ISS |
| **Heavens-Above** | Web | Visual pass display for your location |
| **N2YO** | Web | Real-time orbital display with map |
| **SatPC32** | Windows | Classic tracker with CAT + rotator control |

All tools require up-to-date **Keplerian elements** (TLE — Two-Line Elements) describing the satellite's orbit. These are downloaded automatically from NASA/AMSAT databases.

!!! note "Update TLE two hours before the pass"
    Keplerian elements become outdated. Update them at least once a day, especially for lower-orbit satellites (ISS ~400 km, SO-50 ~600 km).

---

## Getting Started: FM Satellites

Your first satellite contact on an FM satellite requires surprisingly little:

**Minimum:**
- Dual-band handheld (VHF + UHF) — e.g. Baofeng UV-5R, Yaesu FT-70D, Kenwood TH-D75
- Improvised cross-band Yagi for 2 m + 70 cm (can be built from aluminium rod for a few euros)
- Mobile phone with Gpredict or ISS Detector (to track the pass)

**Operating technique:**
1. Find out when the satellite passes over your location and the azimuth of the pass
2. Set the uplink frequency (with Doppler correction +3 kHz at the start of the pass)
3. Listen on the downlink and check whether you hear the satellite (characteristic repeater noise)
4. Call briefly: "9A1ZG, any station via SO-50?"
5. Follow the pass and manually correct Doppler as the satellite moves

!!! example "Common FM satellite frequencies"
    **SO-50:** Uplink 145.850 MHz (PL tone 67.0 Hz), Downlink 436.795 MHz
    
    **AO-91 (Fox-1B):** Uplink 435.250 MHz, Downlink 145.960 MHz
    
    **ISS:** Uplink/Downlink 145.825 MHz (APRS) or 437.800 MHz (voice repeater, when active)

---

## ISS — International Space Station

ISS is the most famous "amateur satellite" — the onboard ARS (Amateur Radio Station) operates under callsigns **NA1SS** (USA) and **RS0ISS** (Russia).

Amateur radio activities on ISS:

- **APRS gateway** (145.825 MHz) — ISS automatically digipeats APRS packets from Earth. You can bounce APRS packets through ISS!
- **Voice QSO** — when crew are available and the antenna is active, they operate on 145.800 MHz or announced frequencies
- **SSTV events** — ISS periodically transmits SSTV (Slow Scan TV) images that you can decode with standard software (MMSSTV)
- **ARISS school projects** — the ARISS (Amateur Radio on the International Space Station) programme organises contacts between ISS crew and schools worldwide

!!! info "ARISS and schools"
    ARISS (ariss.org) facilitates direct contacts between astronauts aboard ISS and students in schools. Amateur radio astronauts include Thomas Pesquet (F4KLP), Sunita Williams (KC5ZTH), and many others.

---

## Advanced Satellites — Linear Transponders

For SSB and CW contacts via satellite you need:

- **A more capable transceiver** with fine frequency tuning (< 10 Hz steps)
- **Crossed-Yagi antenna** (circularly polarised) for azimuth + elevation tracking
- **Rotator system** — the antenna must follow the satellite across the sky
- **Gpredict + CAT** — automated Doppler correction

Popular linear satellites:
- **FO-29 (JAS-2)** — Japanese satellite, V/U linear transponder
- **AO-7** — launched in 1974 and still partially operational!
- **CAS-4A and CAS-4B** — Chinese satellites with excellent transponders, active from 2022 onwards
- **XW-2 series** — several Chinese linear transponder satellites

---

## EME — Earth-Moon-Earth (Moonbounce)

EME is the extreme form of satellite communication — the signal travels to the Moon and back, totalling ~760,000 km. The path loss is approximately 250–270 dB, requiring extremely sensitive receivers and high-gain antennas.

- Popular on 2 m (144 MHz) and 70 cm (432 MHz)
- Uses **JT65** and **Q65** digital protocols (from the WSJT-X package)
- Minimum practical equipment: 4-element Yagi array, 100+ W, low-noise LNA preamplifier
- Experimentation began in the 1950s; today accessible to dedicated enthusiasts

---

## Related Topics

- [Band Plans](../operating/bandplans.md) — VHF/UHF bands for satellites
- [Antennas and Feed Lines](../technical/antennas.md) — Yagi and circularly polarised antennas
- [Portable Operations](portable.md) — portable satellite station
- [Radio Wave Propagation](../technical/propagation.md) — difference between terrestrial and satellite propagation
