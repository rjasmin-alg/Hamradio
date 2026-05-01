# Electronics Fundamentals

Understanding electronics is the foundation for every radio amateur. Without knowing the basic components and laws, it's hard to understand why an antenna needs to be a certain length, what 50 Ω impedance means, or how a radio transmits a signal.

## Basic Components

### Resistor
Limits the flow of electric current. Think of it as a narrowing in a water pipe.

*   **Unit**: Ohm ($\Omega$), Symbol: $R$
*   **Uses**: Voltage division, LED current limiting, pull-up/pull-down

### Capacitor
Stores electrical energy in an electric field between two plates.

*   **Unit**: Farad ($F$), typically $\mu F$, $nF$, $pF$. Symbol: $C$
*   **Uses**: Filtering, DC blocking, tuned circuits

### Inductor
Stores energy in a magnetic field. Opposes changes in current.

*   **Unit**: Henry ($H$), typically $\mu H$, $mH$. Symbol: $L$
*   **Uses**: RF chokes, filters, transformers, baluns

### Semiconductors

**Diode** — One-way valve for current. Conducts only from anode to cathode.

**Zener Diode** — Conducts in reverse above a specific "Zener voltage". Used for voltage regulation.

**BJT Transistor** — Current-controlled amplifier/switch with Base, Collector, Emitter leads. Gain factor: $\beta$ (hFE).

**MOSFET** — Voltage-controlled switch/amplifier with Gate, Drain, Source leads. Nearly all modern RF power amplifiers use RF MOSFETs.

---

## Ohm's Law

$$ I = \frac{U}{R} $$

**Power:**
$$ P = U \cdot I = I^2 \cdot R = \frac{U^2}{R} $$

---

## Series and Parallel Circuits

**Resistors in series:** $R_{total} = R_1 + R_2 + \ldots$

**Resistors in parallel:** $\frac{1}{R_{total}} = \frac{1}{R_1} + \frac{1}{R_2} + \ldots$

**Capacitors** work in reverse: they add in parallel, divide in series.

---

## AC vs DC

**DC** = electrons flow in one direction (batteries, power supplies).  
**AC** = electrons alternate direction sinusoidally (mains power, RF signals).

| Parameter | Description | Formula |
|-----------|-------------|---------|
| Frequency ($f$) | Cycles per second (Hz) | $f = 1/T$ |
| Period ($T$) | Duration of one cycle | $T = 1/f$ |
| RMS Voltage | Effective value equivalent to DC heating | $U_{RMS} = U_{peak}/\sqrt{2}$ |

---

## Reactance and Impedance

**Capacitive reactance** (opposes low frequencies, passes high):
$$ X_C = \frac{1}{2\pi f C} $$

**Inductive reactance** (opposes high frequencies, passes low):
$$ X_L = 2\pi f L $$

**Impedance** (total AC opposition):
$$ Z = R + jX \quad \Rightarrow \quad |Z| = \sqrt{R^2 + X^2} $$

The 50 Ω standard in amateur radio is a compromise that minimises cable losses while maximising power transfer.

---

## LC Resonant Circuit

When $X_L = X_C$, the circuit resonates. Thomson's formula:

$$ f_r = \frac{1}{2\pi\sqrt{LC}} $$

**Q factor** — sharpness of resonance:
$$ Q = \frac{f_r}{\Delta f} = \frac{X_L}{R} $$

Higher Q = narrower bandwidth = more selective filter.

---

## Transformers

$$ \frac{U_1}{U_2} = \frac{N_1}{N_2} \qquad U_1 I_1 = U_2 I_2 $$

RF transformers (balun/unun) convert between balanced and unbalanced lines. Essential for antennas — see [Antennas](antennas.md).

---

## Resistor Colour Code

| Colour | Digit | Multiplier | Tolerance |
|--------|-------|-----------|-----------|
| Black | 0 | ×1 | — |
| Brown | 1 | ×10 | ±1% |
| Red | 2 | ×100 | ±2% |
| Orange | 3 | ×1k | — |
| Yellow | 4 | ×10k | — |
| Green | 5 | ×100k | ±0.5% |
| Blue | 6 | ×1M | ±0.25% |
| Violet | 7 | ×10M | ±0.1% |
| Grey | 8 | ×100M | ±0.05% |
| White | 9 | — | — |
| Gold | — | ×0.1 | ±5% |
| Silver | — | ×0.01 | ±10% |

---

## Related Topics

*   [Antennas and Feedlines](antennas.en.md)
*   [Modulation and Demodulation](modulation.en.md)
*   [Safety](safety.en.md)
*   [Grounding](grounding.en.md)
