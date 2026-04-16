# CB Equipment

CB radio equipment is accessible, robust, and requires no special technical knowledge to set up. However, the difference between a poor and a good CB station — especially in terms of range and signal clarity — can be dramatic, and the antenna is almost always the decisive factor.

---

## CB Radios

### Mobile (vehicle) radios

Mobile CB radios are mounted in vehicles and powered from the 12 V electrical system. This is the most common CB application:

| Model | Modes | Power | Size | Price (approx.) | Notes |
|---|---|---|---|---|---|
| **President McKinley** | AM/FM/SSB | 4/12 W | Standard DIN | ~€150–200 | Popular European choice, SSB, NOAA |
| **President Lincoln II+** | AM/FM/SSB | 4/12 W | Wider than DIN | ~€200–250 | Advanced model, 10 m and CB, SSB |
| **Midland Alan 78 Plus** | AM/FM/SSB | 4/12 W | Standard DIN | ~€120–160 | Good value, compact |
| **Albrecht AE 6491** | AM/FM/SSB | 4/12 W | Compact | ~€130–180 | Discreet, control head on cable |
| **Midland Alan 48 Plus** | AM/FM | 4 W | Mini | ~€80–100 | No SSB, good for beginners |
| **President Bill** | AM/FM | 4 W | Mini | ~€70–90 | Ultra compact |

!!! tip "Recommendation for beginners"
    Midland Alan 48 Plus or President Bill — excellent value for local CB work. If you plan DX or motorway driving with hunters, choose a model with SSB (Alan 78 Plus or McKinley).

### Base stations

Base stations are installed at home and powered from mains (230 V) or an external 12–13.8 V supply:

- **President George** — classic AM/FM/SSB base unit, DIN format, excellent sensitivity
- **Albrecht AE 5890** — modern featuring dual watch, USB charger
- Older models such as **Uniden HR 2510** or **Galaxy DX 99V** — popular with the DX community for their improved filters

!!! note "Alternative: mobile radio + power supply"
    Many users run a mobile radio at home with an inexpensive regulated power supply (13.8 V / 5+ A). The result is identical to a "base station" in performance, at a lower cost.

### Handheld radios

For hiking, camping, and off-road use:

| Model | Modes | Power | Battery | Notes |
|---|---|---|---|---|
| **President Randy FCC** | AM/FM | 4 W | 1,500 mAh Li-Ion | IP67 waterproof, robust |
| **Midland Alan 42 DS** | AM/FM | 4 W | 1,200 mAh Li-Ion | Compact, dual band (EU/US) |
| **Albrecht AE 33H** | AM/FM | 4 W | AA batteries | Long runtime |

Handheld radios have a shorter range due to the short antenna — typically 2–5 km in open terrain, less in woodland. For convoys and camping this is perfectly adequate.

---

## CB Antennas — The Most Important Part of the System

On CB, more than any other single factor, **the antenna determines your range**. The difference between a poor and a good antenna can easily be a 10× improvement in range. Given the fixed 4 W power limit, investing in the antenna always pays off more than illegal power increases.

### CB Antenna Physics

The wavelength at 27 MHz is approximately **11 metres**. A full-wave antenna (dipole) would have arms 5.5 m long — practical for a base station, but not for a car. This is why CB mobile antennas use loading coils to electrically shorten the element.

$$\lambda = \frac{c}{f} = \frac{300\,000\,\text{km/s}}{27\,\text{MHz}} \approx 11.1\,\text{m}$$

The closer the antenna is physically to the full resonant length (or $\lambda/4 \approx 2.75$ m without a coil), the more efficient it is.

### Mobile (vehicle) antennas

| Antenna | Length | Gain | Mount | Price | Notes |
|---|---|---|---|---|---|
| **Sirio Performer 5000** | 171 cm | ~3 dBd | M6/PL stud | ~€60–80 | Popular high-performance antenna |
| **President Virginia** | 140 cm | ~2 dBd | Magnetic | ~€40–60 | Magnetic base, good pattern |
| **Midland 1822 Dual Firestik** | 155 cm | ~3 dBd | Bracket | ~€50–70 | Fibreglass, durable |
| **Albrecht 6130** | 120 cm | ~1.5 dBd | Magnetic | ~€25–40 | Budget option, ok for local |

**Rules for mobile antennas:**
1. **The higher the mount, the better the range** — rooftop beats bonnet every time
2. **Longer is generally better** (to a reasonable limit) — avoid very short antennas
3. **Magnetic bases are convenient but have worse RF ground** — a bolted mount is always better

### SWR — Standing Wave Ratio

SWR (Standing Wave Ratio) measures how well the antenna is matched to the transmitter at the operating frequency. Poor SWR means power is reflected back into the transmitter, which can damage it and reduces range.

$$\text{SWR} = \frac{V_{max}}{V_{min}} = \frac{1 + |\Gamma|}{1 - |\Gamma|}$$

| SWR value | Rating | Action |
|---|---|---|
| 1.0 – 1.5 | ✅ Excellent | None needed |
| 1.5 – 2.0 | ✅ Acceptable | Minor adjustment possible |
| 2.0 – 2.5 | ⚠️ Poor | Antenna adjustment required |
| > 2.5 | ❌ Dangerous | Stop immediately — transmitter damage likely |

**Adjusting a CB antenna:** Nearly all mobile CB antennas have an adjustable tip or sliding whip for fine-tuning length. Procedure:
1. Connect an SWR meter between the coax cable and antenna
2. Key up on channels 1, 20, and 40 and measure SWR on each
3. Shorten or lengthen the antenna element until SWR is below 1.5 on all channels
4. If SWR is higher at the band edges, the antenna is too long or too short

!!! warning "Never transmit without an antenna connected!"
    Transmitting with no antenna (or a disconnected antenna connector) can burn out the output transistor within seconds. Always verify the antenna is connected before keying up.

### Base station antennas

For home base stations on 27 MHz, full-size verticals without loading coils are available:

| Antenna | Height | Gain | Price | Notes |
|---|---|---|---|---|
| **Sirio 827** | 5.65 m | 3 dBd | ~€120–180 | Popular, EU/US channels |
| **Sirio Gain-Master** | 7.1 m | 4 dBd | ~€200–280 | High gain, premium |
| **Albrecht GP 27 CB** | 5.9 m | 3 dBd | ~€100–140 | Solid budget option |
| **President ML145** | 4.6 m | 2 dBd | ~€70–100 | Height/gain compromise |

Base antennas are mounted on a rooftop, mast, or balcony — the higher, the greater the range. Coaxial cable from the base antenna to the radio should be quality cable (RG-8X or RG-213 for longer runs, minimum RG-58 for short runs up to 5 m).

---

## Connections and Accessories

### Coaxial cables

| Type | Diameter | Max. useful length | Notes |
|---|---|---|---|
| **RG-58** | 5 mm | up to 5 m | Flexible, higher losses over distance |
| **RG-8X** | 7 mm | up to 20 m | Flexibility/loss compromise, base station standard |
| **RG-213** | 10 mm | up to 50 m | Low loss, stiff, professional installations |
| **Airspace/Ecoflex** | Various | 100+ m | Premium, minimal loss, expensive |

### Essential accessories

- **SWR meter** — mandatory for antenna tuning (€10–50)
- **PL-259 connectors** — standard CB connector; match them to your cable diameter
- **Mounting hardware** — required for base antenna installation (mast brackets, clamps)
- **Regulated 13.8 V / 5 A power supply** — for using a mobile radio as a base station (€30–80)

---

## How to Increase Range (Legally)

Without increasing power, range can be improved by:

1. **Better antenna** — higher gain, higher mounting position, better SWR
2. **Shorter and thicker coaxial cable** — reduces losses
3. **Mode selection** — SSB on channels 38–40 gives 2–3× the range of AM at the same power
4. **Exploit propagation** — use Sporadic-E and tropospheric conditions for DX
5. **Improve audio** — a good microphone with compression, clear diction, slower speech

!!! info "The rule: antenna always before power"
    Doubling the transmit power gives a 3 dB signal increase — barely noticeable in practice.
    Doubling the antenna gain achieves the same 3 dB, legally and without risk of burning out the transmitter.
    Investment in the antenna always returns more than illegal power amplification.

---

## Related Topics

- [Regulations and Channels](channels.md) — permitted power levels and modulations
- [Introduction to CB](intro.md) — context and community
- [Antennas and Feed Lines](../technical/antennas.md) — deeper antenna physics
- [Safety](../technical/safety.md) — safe antenna installation and RF exposure
