# 📋 Mapa Modula — Radioamaterski Priručnik

> **VAŽNO:** Ovaj dokument definira **sve module** priručnika, njihov status i prioritet.
> Agenti biraju module iz ovog popisa i prate upute iz dokumenta `03_RAZRADA_MODULA.md`.

---

## Legenda

| Oznaka | Značenje |
|--------|----------|
| 🟢 | Postoji sadržaj, treba proširiti |
| 🟡 | Postoji stub/skeleton, treba napisati |
| 🔴 | Ne postoji, treba kreirati od nule |
| **P1** | Visoki prioritet (temelji priručnika) |
| **P2** | Srednji prioritet (korisno, ali ne urgentno) |
| **P3** | Niski prioritet (nice-to-have, duboke teme) |
| ⚡ | Brzo za napraviti (~30 min agentskog rada) |
| 🔧 | Srednja složenost (~1-2h agentskog rada) |
| 🏗️ | Velika složenost (~2-4h agentskog rada, više izvora) |

---

## Sekcija 1: Propisi i Dozvole (`regulations/`)

| ID | Modul | Status | Prioritet | Složenost | Ovisnosti |
|----|-------|--------|-----------|-----------|-----------|
| REG-01 | `index.md` — Uvod u propise | 🟢 | P1 | ⚡ | — |
| REG-02 | `exams.md` — Kako postati radioamater | 🟢 | P1 | 🔧 | — |
| REG-03 | `croatian_regs.md` — Hrvatski propisi | 🟢 | P1 | 🏗️ | — |
| REG-04 | `international_regs.md` — Međunarodni propisi | 🟢 | P1 | 🏗️ | — |
| REG-05 | `callsigns.md` — Pozivne oznake | 🟢 | P1 | 🔧 | REG-03 |
| REG-06 | `license_classes.md` — Razredi dozvola (HR + CEPT) | 🔴 | P1 | 🔧 | REG-03, REG-04 |
| REG-07 | `spectrum.md` — Radiofrekvencijski spektar (namjena) | 🔴 | P2 | 🏗️ | REG-03 |
| REG-08 | `itu_regions.md` — ITU regije i zone | 🔴 | P2 | 🔧 | REG-04 |
| REG-09 | `reciprocal.md` — Recipročne dozvole i CEPT T/R 61-01 | 🔴 | P2 | 🔧 | REG-04, REG-06 |
| REG-10 | `ethics.md` — Radioamaterska etika i ponašanje | 🔴 | P1 | 🔧 | — |

---

## Sekcija 2: Tehnika (`technical/`)

| ID | Modul | Status | Prioritet | Složenost | Ovisnosti |
|----|-------|--------|-----------|-----------|-----------|
| TEC-01 | `index.md` — Uvod u tehniku | 🟢 | P1 | ⚡ | — |
| TEC-02 | `electronics.md` — Osnove elektronike | 🟢 | P1 | 🏗️ | — |
| TEC-03 | `antennas.md` — Antene i vodovi | 🟢 | P1 | 🏗️ | TEC-02 |
| TEC-04 | `receivers.md` — Prijemnici i SDR | 🟢 | P1 | 🏗️ | TEC-02 |
| TEC-05 | `transceivers.md` — Primopredajnici | 🟢 | P2 | 🏗️ | TEC-04 |
| TEC-06 | `safety.md` — Sigurnost | 🟢 | P1 | 🔧 | — |
| TEC-07 | `hamnet.md` — Hamnet | 🟡 | P2 | 🏗️ | — |
| TEC-08 | `propagation.md` — Propagacija radio valova | 🔴 | P1 | 🏗️ | TEC-02 |
| TEC-09 | `power_supplies.md` — Napajanja | 🔴 | P2 | 🔧 | TEC-02 |
| TEC-10 | `filters.md` — Filtri (NF, BP, HP, notch) | 🔴 | P2 | 🔧 | TEC-02 |
| TEC-11 | `transmission_lines.md` — Prijenosni vodovi (detaljno) | 🔴 | P2 | 🔧 | TEC-02, TEC-03 |
| TEC-12 | `antenna_tuners.md` — Antenski tuneri (ATU) | 🔴 | P2 | 🔧 | TEC-03, TEC-11 |
| TEC-13 | `amplifiers.md` — Pojačala (PA) | 🔴 | P2 | 🔧 | TEC-02, TEC-05 |
| TEC-14 | `oscillators.md` — Oscilatori i PLL | 🔴 | P3 | 🔧 | TEC-02 |
| TEC-15 | `modulation.md` — Modulacija i demodulacija (teorija) | 🔴 | P1 | 🏗️ | TEC-02 |
| TEC-16 | `digital_electronics.md` — Digitalna elektronika osnove | 🔴 | P3 | 🔧 | TEC-02 |
| TEC-17 | `sdr_deep.md` — SDR detaljno (RTL-SDR, SDRPlay, etc.) | 🔴 | P2 | 🏗️ | TEC-04 |
| TEC-18 | `test_equipment.md` — Mjerni instrumenti | 🔴 | P2 | 🔧 | TEC-02 |
| TEC-19 | `emc.md` — EMC i smetnje (TVI/BCI) | 🔴 | P2 | 🔧 | TEC-02, TEC-06 |
| TEC-20 | `grounding.md` — Uzemljenje i zaštita od groma | 🔴 | P1 | 🔧 | TEC-06 |
| TEC-21 | `antenna_types.md` — Katalog vrsta antena (Loop, End-fed, Quad, itd.) | 🔴 | P2 | 🏗️ | TEC-03 |
| TEC-22 | `antenna_modeling.md` — Modeliranje antena (MMANA, 4NEC2) | 🔴 | P3 | 🔧 | TEC-03, TEC-21 |
| TEC-23 | `rf_safety.md` — RF sigurnost i PEM proračuni | 🔴 | P2 | 🔧 | TEC-06 |

---

## Sekcija 3: Rad na opsegu (`operating/`)

| ID | Modul | Status | Prioritet | Složenost | Ovisnosti |
|----|-------|--------|-----------|-----------|-----------|
| OPR-01 | `index.md` — Uvod u rad na opsegu | 🟢 | P1 | ⚡ | — |
| OPR-02 | `bandplans.md` — Frekvencijski planovi | 🟢 | P1 | 🔧 | — |
| OPR-03 | `modes.md` — Modovi rada | 🟢 | P1 | 🏗️ | TEC-15 |
| OPR-04 | `procedures.md` — Procedura veze | 🟢 | P1 | 🔧 | — |
| OPR-05 | `logbook.md` — Dnevnici i QSL | 🟢 | P1 | 🔧 | — |
| OPR-06 | `ft8_guide.md` — FT8 praktični vodič (WSJT-X) | 🔴 | P1 | 🏗️ | OPR-03, TEC-17 |
| OPR-07 | `cw_learning.md` — Učenje CW (Morseov kod) | 🔴 | P1 | 🔧 | OPR-03 |
| OPR-08 | `repeaters.md` — Repetitori (CTCSS, DTMF, EchoLink) | 🔴 | P1 | 🔧 | OPR-03 |
| OPR-09 | `aprs.md` — APRS sustav | 🔴 | P2 | 🔧 | OPR-03 |
| OPR-10 | `dmr.md` — DMR i digitalni glasovni modovi (D-STAR, C4FM) | 🔴 | P2 | 🏗️ | OPR-03 |
| OPR-11 | `qcodes.md` — Q-kodovi (detaljan popis) | 🔴 | P1 | ⚡ | OPR-04 |
| OPR-12 | `rst_system.md` — RST sustav i raport | 🔴 | P1 | ⚡ | OPR-04 |
| OPR-13 | `first_qso.md` — Tvoja prva veza (korak po korak) | 🔴 | P1 | 🔧 | OPR-04, TEC-05 |
| OPR-14 | `awards.md` — Diplome (DXCC, WAS, WAZ, 9A diplome) | 🔴 | P2 | 🔧 | OPR-05 |
| OPR-15 | `logging_software.md` — Softver za logiranje (detaljno) | 🔴 | P2 | 🔧 | OPR-05 |
| OPR-16 | `sstv.md` — SSTV (Slow Scan TV) | 🔴 | P3 | ⚡ | OPR-03 |
| OPR-17 | `packet_radio.md` — Packet Radio i AX.25 | 🔴 | P3 | 🔧 | OPR-03 |
| OPR-18 | `moonbounce.md` — EME (Earth-Moon-Earth) | 🔴 | P3 | 🔧 | TEC-03, TEC-08 |

---

## Sekcija 4: CB Radio (`cb/`)

| ID | Modul | Status | Prioritet | Složenost | Ovisnosti |
|----|-------|--------|-----------|-----------|-----------|
| CB-01 | `index.md` — Uvod u CB sekciju | 🟢 | P2 | ⚡ | — |
| CB-02 | `intro.md` — Uvod u CB radio | 🟢 | P2 | 🔧 | — |
| CB-03 | `channels.md` — Propisi i kanali | 🟢 | P2 | 🔧 | — |
| CB-04 | `equipment.md` — Oprema | 🟢 | P2 | 🔧 | — |
| CB-05 | `antennas_cb.md` — CB antene | 🔴 | P3 | ⚡ | TEC-03 |
| CB-06 | `cb_to_ham.md` — Od CB do radioamaterizma | 🔴 | P2 | ⚡ | REG-02 |
| CB-07 | `dx_cb.md` — DX na CB-u (propagacija na 11m) | 🔴 | P3 | ⚡ | TEC-08 |

---

## Sekcija 5: Aktivnosti (`activities/`)

| ID | Modul | Status | Prioritet | Složenost | Ovisnosti |
|----|-------|--------|-----------|-----------|-----------|
| ACT-01 | `index.md` — Uvod u aktivnosti | 🟢 | P1 | ⚡ | — |
| ACT-02 | `contesting.md` — Natjecanja | 🟢 | P1 | 🏗️ | OPR-04 |
| ACT-03 | `dxing.md` — DXing | 🟢 | P1 | 🔧 | TEC-08 |
| ACT-04 | `portable.md` — Rad u pokretu (SOTA/POTA/IOTA) | 🟢 | P1 | 🏗️ | — |
| ACT-05 | `satellites.md` — Sateliti | 🟢 | P2 | 🏗️ | TEC-03 |
| ACT-06 | `ardf.md` — ARG (Radio orijentacija) | 🟢 | P2 | 🔧 | — |
| ACT-07 | `qrp.md` — QRP (Rad malom snagom) | 🔴 | P2 | 🔧 | TEC-05 |
| ACT-08 | `homebrewing.md` — Samoizgradnja opreme | 🔴 | P2 | 🏗️ | TEC-02 |
| ACT-09 | `foxhunting.md` — Traženje lisice (transmitter hunting) | 🔴 | P3 | ⚡ | ACT-06 |
| ACT-10 | `field_day.md` — Field Day | 🔴 | P2 | ⚡ | ACT-02 |
| ACT-11 | `special_events.md` — Posebne postaje i natjecanja u HR | 🔴 | P2 | 🔧 | ACT-02 |

---

## Sekcija 6: Krizne situacije (`emcomm/`)

| ID | Modul | Status | Prioritet | Složenost | Ovisnosti |
|----|-------|--------|-----------|-----------|-----------|
| EMC-01 | `index.md` — Uvod u EmComm | 🟢 | P1 | ⚡ | — |
| EMC-02 | `rmzo.md` — RMZO u Hrvatskoj | 🟢 | P1 | 🏗️ | REG-03 |
| EMC-03 | `procedures.md` — Postupci u hitnim situacijama | 🟢 | P1 | 🔧 | OPR-04 |
| EMC-04 | `winlink.md` — Winlink | 🟢 | P2 | 🏗️ | — |
| EMC-05 | `go_kit.md` — Go-Kit (oprema za hitne situacije) | 🔴 | P1 | 🔧 | — |
| EMC-06 | `ics_forms.md` — ICS obrasci i vježbe | 🔴 | P2 | 🔧 | EMC-03 |
| EMC-07 | `mesh_networking.md` — Mesh mreže (AREDN/Meshtastic) | 🔴 | P2 | 🔧 | TEC-07 |
| EMC-08 | `skywarn.md` — Skywarn i meteorološko opažanje | 🔴 | P3 | ⚡ | — |

---

## Sekcija 7: Zajednica (`community/`)

| ID | Modul | Status | Prioritet | Složenost | Ovisnosti |
|----|-------|--------|-----------|-----------|-----------|
| COM-01 | `index.md` — Uvod u zajednicu | 🟢 | P1 | ⚡ | — |
| COM-02 | `associations.md` — Savezi (HRS, IARU) | 🟢 | P1 | 🔧 | — |
| COM-03 | `clubs.md` — Radioklubovi u HR | 🟢 | P1 | 🏗️ | — |
| COM-04 | `yota.md` — YOTA program | 🟢 | P2 | 🔧 | — |
| COM-05 | `online.md` — Online zajednice (forumi, Discord, Reddit) | 🔴 | P2 | ⚡ | — |
| COM-06 | `hamfests.md` — Ham sajmovi i susreti | 🔴 | P2 | ⚡ | — |
| COM-07 | `mentoring.md` — Mentorstvo i Elmering | 🔴 | P2 | ⚡ | — |

---

## Sekcija 8: Resursi (`resources/`)

| ID | Modul | Status | Prioritet | Složenost | Ovisnosti |
|----|-------|--------|-----------|-----------|-----------|
| RES-01 | `index.md` — Uvod u resurse | 🟢 | P1 | ⚡ | — |
| RES-02 | `glossary.md` — Rječnik kratica | 🟢 | P1 | 🔧 | — |
| RES-03 | `formulas.md` — Referentni list formula | 🔴 | P1 | 🔧 | TEC-02 |
| RES-04 | `links.md` — Korisni linkovi (kategorizirano) | 🔴 | P2 | ⚡ | — |
| RES-05 | `software.md` — Softver za radioamatere (katalog) | 🔴 | P1 | 🔧 | — |
| RES-06 | `phonetic_alphabet.md` — NATO fonetska abeceda | 🔴 | P1 | ⚡ | OPR-04 |
| RES-07 | `band_chart.md` — Vizualni band chart (HR dozvole) | 🔴 | P1 | 🔧 | OPR-02, REG-06 |
| RES-08 | `exam_prep.md` — Priprema za ispit (pitanja + odgovori) | 🔴 | P1 | 🏗️ | REG-02 |
| RES-09 | `books.md` — Preporučene knjige i materijali | 🔴 | P2 | ⚡ | — |

---

## NOVA Sekcija 9: Propagacija (`propagation/`) — PREDLOŽENA

| ID | Modul | Status | Prioritet | Složenost | Ovisnosti |
|----|-------|--------|-----------|-----------|-----------|
| PRO-01 | `index.md` — Uvod u propagaciju | 🔴 | P1 | ⚡ | — |
| PRO-02 | `ionosphere.md` — Ionosfera i slojevi (D, E, F1, F2) | 🔴 | P1 | 🏗️ | — |
| PRO-03 | `hf_propagation.md` — HF propagacija | 🔴 | P1 | 🏗️ | PRO-02 |
| PRO-04 | `vhf_propagation.md` — VHF/UHF propagacija (tropo, sporadic E) | 🔴 | P2 | 🔧 | PRO-02 |
| PRO-05 | `solar_cycle.md` — Sunčev ciklus i indeksi (SFI, K, A) | 🔴 | P1 | 🔧 | PRO-02 |
| PRO-06 | `tools_propagation.md` — Alati za predikciju (VOACAP, PSKReporter) | 🔴 | P2 | 🔧 | PRO-03 |
| PRO-07 | `gray_line.md` — Gray Line i posebni uvjeti | 🔴 | P3 | ⚡ | PRO-03 |

---

## NOVA Sekcija 10: DIY Projekti (`projects/`) — PREDLOŽENA

| ID | Modul | Status | Prioritet | Složenost | Ovisnosti |
|----|-------|--------|-----------|-----------|-----------|
| PRJ-01 | `index.md` — Uvod u DIY projekte | 🔴 | P2 | ⚡ | — |
| PRJ-02 | `dipole_build.md` — Izgradi dipol antenu | 🔴 | P1 | 🔧 | TEC-03 |
| PRJ-03 | `dummy_load.md` — Izgradi umjetno opterećenje | 🔴 | P2 | ⚡ | TEC-02 |
| PRJ-04 | `swr_meter.md` — Izgradi SWR metar | 🔴 | P3 | 🔧 | TEC-02, TEC-03 |
| PRJ-05 | `qrp_tx.md` — Izgradi jednostavan QRP odašiljač | 🔴 | P3 | 🏗️ | TEC-02 |
| PRJ-06 | `end_fed.md` — Izgradi End-Fed antenu | 🔴 | P2 | 🔧 | TEC-03 |
| PRJ-07 | `raspberry_pi.md` — Raspberry Pi projekti za ham radio | 🔴 | P3 | 🔧 | — |
| PRJ-08 | `fox_transmitter.md` — Izgradi ARG odašiljač | 🔴 | P3 | 🔧 | TEC-02, ACT-06 |

---

## NOVA Sekcija 11: Povijest (`history/`) — PREDLOŽENA

| ID | Modul | Status | Prioritet | Složenost | Ovisnosti |
|----|-------|--------|-----------|-----------|-----------|
| HIS-01 | `index.md` — Uvod u povijest | 🔴 | P3 | ⚡ | — |
| HIS-02 | `radio_history.md` — Povijest radija (Tesla, Marconi, Hertz) | 🔴 | P3 | 🔧 | — |
| HIS-03 | `ham_history_croatia.md` — Povijest radioamaterizma u HR | 🔴 | P2 | 🏗️ | — |
| HIS-04 | `ham_history_world.md` — Povijest radioamaterizma u svijetu | 🔴 | P3 | 🔧 | — |
| HIS-05 | `famous_hams.md` — Poznati radioamateri | 🔴 | P3 | ⚡ | — |

---

## Statistika

| Kategorija | Broj modula | 🟢 Postoji | 🟡 Stub | 🔴 Novo |
|-----------|-------------|-----------|---------|---------|
| Propisi | 10 | 5 | 0 | 5 |
| Tehnika | 23 | 7 | 0 | 16 |
| Rad na opsegu | 18 | 5 | 0 | 13 |
| CB Radio | 7 | 4 | 0 | 3 |
| Aktivnosti | 11 | 6 | 0 | 5 |
| Krizne situacije | 8 | 4 | 0 | 4 |
| Zajednica | 7 | 4 | 0 | 3 |
| Resursi | 9 | 2 | 0 | 7 |
| Propagacija (NOVO) | 7 | 0 | 0 | 7 |
| DIY Projekti (NOVO) | 8 | 0 | 0 | 8 |
| Povijest (NOVO) | 5 | 0 | 0 | 5 |
| **UKUPNO** | **113** | **37** | **0** | **76** |

> **Preporučeni redoslijed rada:**
> 1. Prvo obraditi sve **P1 module** koji već postoje (🟢) — proširiti na minimalnu dubinu
> 2. Zatim **P1 module** koji ne postoje (🔴) — stvoriti od nule
> 3. Na kraju P2 i P3 module kao bonus sadržaj
