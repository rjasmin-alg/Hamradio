# 🚀 Strategija značajnog proširenja priručnika

Ovaj dokument služi kao master-plan za podizanje kvalitete i opsega svih modula u radioamaterskom priručniku. Cilj je da svaka stranica postane autoritativan izvor informacija, nadmašujući osnovne definicije.

## 🏁 Opći standardi proširenja (za sve module)

Svaki modul koji se smatra "značajno proširenim" mora zadovoljiti:
1.  **Dubina (1500+ riječi)**: Ne samo "što", nego "kako" i "zašto".
2.  **Praktičnost**: Barem jedan "Step-by-step" vodič ili realni scenario.
3.  **Vizualizacija**: Detaljni tekstualni opisi shema koji omogućuju agentima da generiraju slike ili linkaju na simulatore.
4.  **Interaktivnost**: Linkovi na Falstad, web-SDR, ili online kalkulatore.
5.  **Cross-linking**: Povezanost s barem 3-5 drugih modula.

---

## 🛠️ Segment: Tehnika (Technical)

### TEC-02: Osnove elektronike
- **Proširenje**: Detaljna analiza reaktivnih komponenti ($X_L, X_C$) u RF okruženju.
- **Dodatak**: Tablica boja otpornika s primjerima, simulatori za dijelilo napona.
- **Zadatak**: Objasniti impedanciju ($Z$) kao vektor u kompleksnoj ravnini (jednostavno).

### TEC-03: Antene i vodovi
- **Proširenje**: Teorija zračenja (Hertzov dipol), dijagrami zračenja (E i H ravnina).
- **Dodatak**: Usporedba koaksijalnih kabela (RG-58 vs LMR-400) s tablicom gubitaka na 144/430 MHz.
- **Zadatak**: Praktični izračun za 1/4 valni vertikal s radijalima.

### TEC-08: Propagacija radio valova
- **Proširenje**: Detaljan opis slojeva ionosfere (D, E, F1, F2) i njihova promjena kroz ciklus dana/noći.
- **Dodatak**: Kako čitati Solar-Terrestrial Data (SFI, K, A indeksi).
- **Zadatak**: Objasniti "Gray Line" propagaciju i kako je iskoristiti za DX veze.

---

## ⚖️ Segment: Propisi (Regulations)

### REG-02: Kako postati radioamater
- **Proširenje**: Detaljan workflow od prve prijave u klub do HAKOM dozvole.
- **Dodatak**: Popis ispitnih pitanja (primjeri) i savjeti za prevladavanje treme.
- **Zadatak**: Usporediti HR sustav s CEPT standardima (T/R 61-01).

### REG-03: Hrvatski propisi
- **Proširenje**: Detaljna analiza Pravilnika o amaterskim radijskim komunikacijama.
- **Dodatak**: Tablica svih frekvencijskih opsega s dopuštenim snagama po razredima (A, B, N).
- **Zadatak**: Jasno definirati što je "sekundarna namjena" opsega.

---

## 🎙️ Segment: Operacije (Operating)

### OPR-04: Procedura veze
- **Proširenje**: Razlika u proceduri između lokalnog repetitora, HF DX veze i pile-upa.
- **Dodatak**: Transkripti (SSB, CW) s objašnjenjem svakog dijela veze.
- **Zadatak**: Detaljan vodič kroz fonetsku abecedu s fonetskim izgovorom na HR.

### OPR-06: FT8 praktični vodič
- **Proširenje**: Konfiguracija WSJT-X (CAT control, audio nivoi, time sync).
- **Dodatak**: Etiketa rada u digitalnim modovima (split rad, snaga).
- **Zadatak**: Troubleshooting čestih problema (npr. audio feedback).

---

## 🏆 Segment: Aktivnosti (Activities)

### ACT-02: Natjecanja (Contesting)
- **Proširenje**: Strategija "Rate vs Multiplier" i rad u različitim kategorijama (SOAB, SOSB).
- **Dodatak**: Usporedba N1MM+ i DXLog softvera.
- **Zadatak**: Objasniti Cabrillo format i proces slanja loga.

### ACT-04: Rad u pokretu (SOTA/POTA)
- **Proširenje**: Kako odabrati lokaciju, oprema za QRP rad (baterije, lagane antene).
- **Dodatak**: Lista 9A vrhova i parkova s linkovima na mape.
- **Zadatak**: Checklist za "Go-Bag" prije polaska na vrh.

---

## 🏗️ Novi moduli (P2/P3 - Razrada)

1.  **TEC-18: Mjerni instrumenti**: NanoVNA od A do Ž (kalibracija, mjerenje SWR-a, Smithov dijagram).
2.  **TEC-20: Uzemljenje i zaštita**: Razlika između RF, sigurnosnog i gromobranskog uzemljenja.
3.  **OPR-09: APRS**: Kako postaviti digipeater, praćenje na karti, slanje poruka.
4.  **ACT-08: Samoizgradnja**: Alati za lemljenje, čitanje shema, prvi projekt (npr. Pixie QRP ili balun).

---

## 📈 Tablica prioriteta za P1 (Val 1)

| Modul | Status | Fokus proširenja |
|-------|--------|------------------|
| **TEC-02** | 🟡 | Formule, MathJax, Sheme |
| **TEC-03** | 🟡 | Tipovi antena, gubici u kabelima |
| **REG-03** | 🔴 | Točni zakonski okviri, tablice snaga |
| **OPR-04** | 🟢 | Transkripti, fonetika |
| **ACT-04** | 🔴 | SOTA/POTA specifičnosti za HR |

> **NAPOMENA:** Svaka promjena mora biti popraćena ažuriranjem `.en.md` verzije (makar kao sažetak).
