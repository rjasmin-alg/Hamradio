# Antennas & Feedlines

An antenna dictates the true nature of propagation. Placing an awful stick upon a thousand dollar transceiver easily underperforms deploying a masterfully designed aerial loop fixed upon a cheap radio station. 

## Structural Aerial Varieties

### Dipole (Center-Fed)
Simplest wire iteration utilizing sheer symmetrical radiation efficiency.
*   Normally spanning lengths of EXACTLY $\lambda/2$ (half-wavelength rules) of the required operational frequency scope.
*   Cutting at exactly the mid-point splits elements symmetrically injecting feeds via Baluns.

### Yagi-Uda (Beam Director)
A highly directed aluminum arrow focusing all radio-electric emissions straightforward acting similarly to flashlight lenses ignoring backside strays.
*   Embraces a dipole element flanked actively utilizing a backing reflector pushing the element outwards via forward Directors.

### Ground Plane Verticals
Operating flawlessly upon omnidirectional requirements (sweeping fully around 360 orientations).
*   Typically necessitates heavy implementation of grounding counter-poises "Radials".

## Emission Polarization

Matching operational lines correctly maintains stability averting heavy $20+$ dB power drops.
Shooting a **horizontal** line while a receiver expects a **vertical** intercept yields dead connections. Therefore mobile operators fixant solely upon verticals whereas massive HF DX deployments align mostly horizontal bounds ignoring ambient noise pickups!

### Gain Expectations

Always note: Antennas **DO NOT produce internal free powers nor amplify signals**. Gain strictly specifies that power diverted via shape lenses towards exclusive points inherently starves rear paths!
*   **dBi**: Theoretical sphere (falsely inflating marketing scopes).
*   **dBd**: Real gain measured physically opposed to a raw classic dipole shape. ($0 \text{ dBd} = 2.15 \text{ dBi}$)

### Standing Wave Ratios (SWR) Mismatches
Pushing 50 Ohm ($50 \Omega$) limits represents absolute stability. Generating incorrectly adjusted un-resonant antennas drastically forces output paths crashing out, repelling heavily sending dangerous thermal blasts straight inwardly backwards down to transceiver bounds marking a bad Standing Wave Ratio exceeding `2:1` margins!

## Specialized Space Constraints & Stealth Loops

If lacking acres of territory these specific types allow urban apartments deployments:
1. **End-Fed Half Waves (EFHW):** Driving wires attaching solely using one extreme baseline without demanding center feed breaks natively pushing insane impedances exceeding 2000$\Omega$, relying entirely upon heavy impedance 49:1 massive Unun structures.
2. **QUAD serial Loops:** Circular/rectangled wire elements highly resistive targeting hostile noisy atmospheric rains!
3. **Small Magnetic Transmitting Loops:** Heavy copper circle employing a capacitor allowing incredibly short but ultra-filtered low-noise results natively!
4. **J-Poles (Slim Jims):** Bent tubular J structures ideal replacing missing ground-radial planes yielding fantastic gain values upon small balconies hitting UHF and VHF requirements transparently! 

## Balanced versus Unbalanced Feedpoints (Baluns)
Hooking an unbalanced tube line (a Coaxial output shielding mechanism) straight pushing into an exact symmetrical half dipole structure breaks its symmetry creating stray currents flowing backwards upon outer shields!
Using **Bal**anced-to-**un**balanced transformational ring cores (Balun systems) or asymmetrical Ununs dictates the safe flow resolving mismatch impedances.

| Reliable Cable Types | Attenuation Drop (Measured 100m lines) running at 50 MHz | VHF Drops on 144 MHz | Extreme 432 MHz Losses | 
|----------------------|---------------------------------------|---------------------|----------------------------|
| Standard raw RG-58 | Colossal 10 dB deficit losses! | Yields a tragic ~18.5 dB power wipe!| Horrific 35 decibels; practically blocking transmission!|  
| Stronger Thicker RG-213 | Sustainable 4.5 dB drops. | Manageable 8.8 dB transmission falloff | Signals dwindle noticeably past 16dB losses. |
| Specialized LMR-400 | Minuscule ~ 2.8 dB losses.. | Pristine 4.8 dB retention allowing top power!| Notable but totally workable drops. Excellent build grade!|

!!! tip "Connectors"
    For anything upon HF and VHF simply stick heavily attaching raw PL259 UHF caps. Extremely tough and cheap avoiding water leaks efficiently compared natively utilizing precise tiny BNC structures.
