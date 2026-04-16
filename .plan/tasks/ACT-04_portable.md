# ACT-04 — Rad u pokretu (SOTA/POTA/IOTA)

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/activities/portable.md` |
| **Status** | 🟢 Postoji, treba proširiti |
| **Prioritet** | P1 — Val 1 |
| **Složenost** | 🏗️ Velika |
| **Ovisnosti** | — |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati postojeći `docs/activities/portable.md` (~971 bajtova)
- [ ] Web search: "SOTA rules activation points chaser scoring 2024"
- [ ] Web search: "POTA parks on the air rules Croatia 9A parks"
- [ ] Web search: "IOTA Croatia islands list 9A Adriatic"
- [ ] Web search: "QRP portable radio comparison FT-818 KX2 IC-705 TR-USDX"
- [ ] Web search: "LiFePO4 battery portable ham radio capacity hours"
- [ ] Web search: "SOTA activation checklist portable antenna tips"

### Sadržaj koji treba dodati

#### SOTA proširiti
- [ ] **Pravila detaljno:**
  - [ ] Minimalna visina vrha (150m iznad sedla u zoni od 25km)
  - [ ] Minimalan broj QSO za aktivaciju (4 QSO)
  - [ ] Trajanje: mora se biti na vrhu (ne podnožju)
  - [ ] Bonusi: zimski bonus (25. 10. - 28. 2.), S2S bonus (summit to summit)
- [ ] **Bodovanje:**
  - [ ] Koeficijenti prema visini vrha (1-10 bodova)
  - [ ] Chaser bodovi (1 bod po aktivatoru na kojeg si stavio potvrdu)
  - [ ] Diploma struktura (Goat = 1000, Mountain Goat = 1000 ljetno...)
- [ ] **HR specifičnosti:**
  - [ ] 9A SOTA asocycacija
  - [ ] Primjeri popularnih vrhova: Sljeme, Medvednica, planine u Gorskom kotaru
  - [ ] Kako pronaći HR vrhove: sota.database.org filter 9A
- [ ] **Alerts i Spots:**
  - [ ] Prijavi aktivaciju unaprijed na sotawatch.org
  - [ ] Spottaj se sami putem telefona (app: SOTA Spotter)
  - [ ] Zašto je važno spotanje (lovci te čekaju!)

#### POTA proširiti
- [ ] **Pravila:**
  - [ ] Aktivacija iz registriranog parka (POTA database)
  - [ ] Minimalno 10 QSO za aktivaciju
  - [ ] Smatra se 1 QSO per day per park (kann se reaktivirati!)
- [ ] **HR specifičnosti:**
  - [ ] NP Plitvice, NP Krka, PP Medvednica — registrirani parkovi
  - [ ] Kako pronaći HR parkove: pota.app
  - [ ] Upload na adif2pota.com
- [ ] **Hunter vs Activator:** razlika u bodovanju, diplomatska struktura

#### IOTA proširiti
- [ ] **Pravila:**
  - [ ] IOTA grupe — svaki otok/skupina ima IOTA broj (EU-016 = Jadransko otočje)
  - [ ] Minimalno 100 QSO za aktivaciju (ili 1 potvrda uspostavlja pravo za lovca)
- [ ] **HR specifičnosti:**
  - [ ] EU-016 (Kvarnerski otoci), EU-110 (Dalmatinski otoci), EU-136...
  - [ ] Legendarni otoci: Palagruža (EU-090) — rijedak i tražen!
  - [ ] Online baza: iota-world.org
- [ ] **Ekspedicije:** kratko o organizaciji i opremi

#### Oprema — detaljno
- [ ] **Usporedna tablica QRP radio uređaja:**
  - Redovi: FT-818ND, KX2, IC-705, TR-USDX, µBITX v6, QCX+
  - Stupci: Snaga (W), Opsezi, HF/VHF, Mod, Baterija, Masa (g), Cijena (€)
- [ ] **Antene za portable:**
  - [ ] End-Fed Half Wave (EFHW) — najlakše, teleskopska vertikala ili throw-line
  - [ ] Linked dipol — promjena opsega skidanjem/dodavanjem segmenta
  - [ ] Vertikalka na štapu za pecanje — elegantno, za 40m-10m
  - [ ] Moxon — kompaktna, za 2-element Yagi karakteristiku
  - [ ] Za svaku: masa, postavljanje (minute), prikladan opseg
- [ ] **Napajanje:**
  - [ ] LiFePO4 prevlast — zašto (ciklusi, sigurnost, masa)
  - [ ] Tablica kapaciteta: 3Ah | 5Ah | 10Ah | Trajanje pri 5W (sati)
  - [ ] Solar panel — kada vrijedi (dugačke aktivacije)
  - [ ] QRP = dulje trajanje baterije nego VHF/UHF FM

#### Logistika
- [ ] **Checklist za aktivaciju:**
  - [ ] Prijava alert unaprijed (SOTA/POTA)
  - [ ] Radio, baterija, antena
  - [ ] Telefon s SIM (spot sa vrha)
  - [ ] Logbook i bilježnica
  - [ ] Minimalna odjeća/oprema za planinu
- [ ] **Safety outdoor:**
  - [ ] Grom na vrhu — descend čim se vide oblaci!
  - [ ] Odjeća po vremenu
  - [ ] Prijava dolaska/odlaska (nije uvijek potrebno, ali pametno)
- [ ] **Admonitions** — minimalno 4 (tip za spotanje, danger za grom, note za pravila, example za checklist)
- [ ] **Interni linkovi** — contesting.md, antennas.md, safety.md, logbook.md

### Kontrola kvalitete
- [ ] Minimalno 2500 riječi ukupno
- [ ] Tablica QRP radio uređaja kompletna
- [ ] Tablica napajanja kompletna
- [ ] SOTA/POTA/IOTA pravila sva prisutna
- [ ] Checklist za aktivaciju prisutan
- [ ] `.en.md` ažuriran ili stub
- [ ] `mkdocs.yml` ne treba mijenjati

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Proširi stranicu docs/activities/portable.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- docs/activities/portable.md  (ZADRŽI SAV POSTOJEĆI SADRŽAJ!)
- .plan/01_VIZIJA_I_STANDARDI.md

KORAK 2 — Istraži web:
- "SOTA rules 2024 activation points bonuses"
- "POTA parks on the air rules activation Croatia 9A"
- "IOTA Croatia islands EU-016 EU-110 Adriatic"
- "QRP portable radio comparison FT-818 KX2 IC-705 TR-USDX weight"
- "LiFePO4 battery portable ham radio hours runtime"

KORAK 3 — ZADRŽI sve postojeće, proširi svaki program i dodaj sekcije o opremi:

## SOTA (detaljno)
Pravila: min visina vrha (150m iznad sedla), 4 QSO minimum, biti NA vrhu
Bodovanje: 1-10 bodova po vrhu, winterbonus, Summit-to-Summit bonus
HR specifičnosti: 9A SOTA, popularne planine (Sljeme, Gorski kotar, Velebit)
Alerts: sotawatch.org, SOTA Spotter app, zašto je spotanje ključno
Diploma: Mountain Goat (1000 aktivacijskih bodova), Shack Sloth (chaser)

## POTA (detaljno)
Pravila: 10 QSO minimum, registrirani park (pota.app), svaki park = nova aktivacija
HR parkovi: NP Plitvice, NP Krka, PP Medvednica, Vransko jezero...
Upload: adif2pota.com ili direktno kroz flLog ili Log4OM
Hunter vs Activator razlika

## IOTA (detaljno)
Pravila: IOTA grupe (svaki otok/skup = broj), 100 QSO za official activacija
HR IOTA grupe: EU-016 Kvarner, EU-110 Dalmacija North, EU-136 Dalmacija South...
Traženi otoci: Palagruža (EU-090!) — rijetko aktiviran, svaki spot izazove pile-up
Organizacija ekspedicije: kratko

## Oprema — usporedna tablica QRP radio uređaja
Tablica: Radio | Snaga | Opsezi | Mod | Masa (g) | Cijena (≈€) | Napomena
FT-818ND | 6W | HF+VHF+UHF | All | 830g | 500€ | Pouzdan klasik
KX2 | 10W | HF | All | 340g | 850€ | Kompaktan, premium
IC-705 | 10W | HF+VHF+UHF | All | 990g | 1200€ | SDR, BlueTooth
TR-USDX | 10W | HF (5 banda) | CW/SSB | 170g | 80-150€ | DIY, budget
QCX+ | 5W | 1 band CW | CW | 130g | 60€ | Kit, samo CW

## Antene za portable
Tablica: Antena | Masa | Postavljanje (min) | Opsezi | Prednosti
End-Fed HW (EFHW): 200g, 5 min, jedan opseg, najuniverzalnija
Linked dipol: 300g, 10 min, višestruki, promjena opsega na terenu
Vertikalka/štap: 400g, 8 min, 20-10m (s tunerom više), ne treba podlogu
Moxon: 250g, 15 min, jedan opseg, 2-elementna Yagi karakteristika

## Napajanje
Tablica: Kapacitet | Masa | Trajanje (5W TX, 50% duty) | Model primjera
3 Ah LiFePO4 | 250g | ~3h | Bioenno 3Ah
5 Ah LiFePO4 | 380g | ~5h | Bioenno 5Ah  
10 Ah LiFePO4 | 840g | ~10h | Bioenno 10Ah
Solar 10W | 700g | ∞ (ako svjeće) | BougeRV 10W

## Checklist za aktivaciju
- [ ] Alert poslan (sotawatch.org / pota.app) ispitvori unaprijed
- [ ] Radio: baterija napunjena, programirani opsezi
- [ ] Antena: provjerena doma, sva oprema
- [ ] Telefon: SOTA Spotter / POTA app, mobilna mreža (provjeri pokrivenost!)
- [ ] Logbook (app ili papir)
- [ ] Planinska oprema (puna!): kabanica, extra sloj, voda, hrana, mapa

!!! danger "Grom na vrhu: čim vidiš oblake — silazak odmah! Nikada ne čekaj!"

KORAK 4 — Tehničke smjernice:
- Tablice za svu opremu (QRP radio, antene, baterije)
- Admonitions: minimalno 4 (danger za grom, tip za spotanje)
- Interni linkovi: contesting.md, antennas.md, safety.md
- Minimalno 2500 riječi ukupno

KORAK 5 — Spremi u docs/activities/portable.md
```

---

## Bilješke o napretku

- 
