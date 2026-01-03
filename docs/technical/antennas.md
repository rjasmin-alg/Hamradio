# Antene i vodovi

Antena je najvažniji dio svake radio stanice. Loša antena na skupom uređaju radi lošije nego dobra antena na jeftinom uređaju.

## Vrste antena

### Dipol
Najjednostavnija i vrlo efikasna antena.
- Sastoji se od dvije žice ukupne duljine $\lambda/2$ (pola valne duljine).
- Primjer za 20m (14 MHz): Ukupna duljina oko 10m.

### Yagi-Uda (Beam)
Usmjerena antena koja pojačava signal u jednom smjeru.
- Sastoji se od dipola (zračeći element), reflektora i direktora.
- Koristi se za DX rad jer "fokusira" energiju.

### Vertikalka (Ground Plane)
Omnidirekcijska antena (zrači u svim smjerovima).
- Dobra za lokalne veze (VHF/UHF) i DX na nižim frekvencijama ako ima dobro uzemljenje.

## Antenski vodovi (Feedlines)

### Koaksijalni kabel
Najčešće korišten vod.
- **RG-58**: Tanak, za kraće relacije i manje snage.
- **RG-213**: Deblji, manji gubici, za veće snage.
- **Impedancija**: Standard je 50 $\Omega$.

### SWR (Standing Wave Ratio)
Omjer stojnih valova. Mjera prilagođenosti antene i voda.
- **1:1**: Savršeno.
- **do 1.5:1**: Odlično.
- **preko 2:1**: Potrebno ugađanje ili korištenje tunera.

## Simulatori Antena
Softver za modeliranje antena omogućuje vam da "izgradite" antenu na računalu i vidite kako će raditi prije nego što odrežete ijednu žicu.

*   [**MMANA-GAL**](http://gal-ana.de/basicmm/en/): Besplatan i moćan alat za modeliranje žičanih antena. Standard u hobiju.
*   [**4NEC2**](https://www.qsl.net/4nec2/): Napredniji NEC-2 bazirani softver za Windows.
*   [**Dipole Calculator**](https://www.allaboutcircuits.com/tools/dipole-antenna-length-calculator/): Jednostavan online kalkulator za duljine dipola.
