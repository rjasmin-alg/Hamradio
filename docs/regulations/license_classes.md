# Razredi radioamaterskih dozvola

Sustav razreda dozvola osigurava da operatori stječu znanje i odgovornost postupno. Početnik ne dobiva pristup maksimalnoj snazi odmah — nego tek kad dokaže da razumije propise, tehniku i sigurnost. Ovaj model štiti RF spektar i sve koji ga dijele.

## Hrvatski sustav razreda

Hrvatska slijedi CEPT (Conférence Européenne des Postes et Télécommunications) model s tri razreda:

### N razred — Nacionalni početnik

*   **Ciljna skupina**: Djeca i odrasli koji žele brzo početi, bez dubokog teorijskog znanja
*   **Opsezi**: Ograničeni segmenti VHF/UHF + pojedini HF opsezi
*   **Maksimalna snaga**: 10 W ERP
*   **Modovi**: CW, SSB, FM, digitalni (na odobrenim opsezima)
*   **Posebnosti**: Dozvola vrijedi samo u Republici Hrvatskoj (nema CEPT reciprociteta)
*   **Ispit**: Jednostavniji, osnove propisa i sigurnosti

### B razred — CEPT Novice

*   **Ciljna skupina**: Hobisti koji žele raditi na HF i ostvarivati europski DX
*   **Opsezi**: Ograničeni HF segmenti + svi VHF/UHF opsezi
*   **Maksimalna snaga**: 100 W ERP
*   **Modovi**: Svi modovi
*   **Posebnosti**: CEPT Novice Licence — priznat u svim CEPT državama (44+ zemalja)
*   **Ispit**: Osnove elektronike, propagacija, propisi, operativni rad

### A razred — CEPT HAREC

*   **Ciljna skupina**: Ozbiljni hobisti, DX-eri, experimenteri, gradioci
*   **Opsezi**: **Svi** amaterski opsezi (1.8 MHz – 250 GHz i više)
*   **Maksimalna snaga**: 1000–1500 W ERP (ovisno o opsegu)
*   **Modovi**: Apsolutno svi modovi
*   **Posebnosti**: HAREC certifikat — priznat u svim CEPT i mnogim ne-CEPT zemljama; smije graditi vlastita pojačala (PA)
*   **Ispit**: Detaljna elektronika, RF tehnika, antenski proračuni

---

## Tablica privilegija

| Privilegija | N razred | B razred | A razred |
|-------------|----------|----------|----------|
| **160 m** | ograničeno | ✅ | ✅ |
| **80 m** | ograničeno | ✅ | ✅ |
| **40 m** | ograničeno | ✅ | ✅ |
| **30 m** (WARC) | ❌ | ✅ | ✅ |
| **20 m** | ❌ | ✅ | ✅ |
| **17 m** (WARC) | ❌ | ✅ | ✅ |
| **15 m** | ❌ | ✅ | ✅ |
| **12 m** (WARC) | ❌ | ✅ | ✅ |
| **10 m** | ograničeno | ✅ | ✅ |
| **6 m** | ❌ | ✅ | ✅ |
| **2 m** | ✅ | ✅ | ✅ |
| **70 cm** | ✅ | ✅ | ✅ |
| **23 cm i više** | ❌ | ✅ | ✅ |
| **Max snaga** | 10 W | 100 W | 1500 W |
| **CEPT priznat** | ❌ | ✅ (Novice) | ✅ (HAREC) |
| **Gradnja PA** | ❌ | ❌ | ✅ |

---

## CEPT sustav — putovnica za Europu

CEPT je europska organizacija koja harmonizira telekomunikacijske propise. Dva ključna dokumenta za radioamatere:

### T/R 61-01 — CEPT HAREC

*   **Nositelji**: A razred (HAREC) iz svih CEPT zemalja
*   **Privilegije**: Rad u gotovo svim CEPT zemljama bez posebnih formalnosti
*   **Kako**: Koristite pozivnu oznaku domicilne zemlje + /P ili prefiks zemlje domaćina
*   **Primjer**: Hrvat `9A1ABC` radi u Njemačkoj kao `DL/9A1ABC`

### T/R 61-02 — CEPT Novice

*   **Nositelji**: B razred
*   **Ograničenja**: Specifičan za svaku zemlju (neke ne priznavaju Novice reciprocitet za sve opsege)
*   **Važno**: Uvijek provjerite propise konkretne CEPT zemlje prije rada

!!! tip "Puna lista CEPT zemalja"
    [CEPT T/R 61-01 lista](https://cept.org/ecc/groups/ecc/wg-fm/fm-25/client/files/ecc-recommendation-6101) — 44+ zemalja uključujući svu EU, Norvešku, Švicarsku i druge. S HAREC certifikatom možete raditi u svim!

---

## Napredovanje između razreda

### Iz N u B razred

1.  Položite B razred ispit (složeniji od N)
2.  HAKOM ažurira dozvolu i dodjeljuje prava B razreda
3.  Isti callsign — samo drugačija razina privilegija

### Iz B u A razred

1.  Položite A razred ispit (detaljnija elektronika i RF tehnika)
2.  HAKOM izdaje novu dozvolu s puni A privilegijama i HAREC certifikatom
3.  Opcija: Zatražite kraći callsign (dvoslokovni: `9A1A`, `9A2B` i sl.) — prestižne su i teže dostupne

!!! note "Preskakanje razreda"
    Nema obveze prolaska kroz sve razrede. Slobodno možete direktno pristupiti A razredu ispitu bez prethodnog B razreda. Preporučujemo ovo tehničkim profilima (IT, inženjeri).

### Kada nadograditi?

*   Pohađate li natjecanja — A razred nudi ekskluzivne segmente (donje CW pojaseve)
*   Želite li koristiti pojačalo (PA) snage > 100 W
*   Planujete li putovati i raditi u inozemstvu (HAREC = sloboda)
*   Gradnja vlastite opreme (A razred dozvoljava modificiranje i gradnju)

---

## Usporedba s međunarodnim sustavima

=== "SAD (FCC)"
    | FCC razred | CEPT ekvivalent | Opsezi | Max snaga |
    |-----------|----------------|--------|----------|
    | **Technician** | — (sub-Novice) | VHF/UHF + ograničeni HF | 1500 W (VHF), 200 W (HF) |
    | **General** | CEPT Novice (B) | Većina HF | 1500 W |
    | **Amateur Extra** | CEPT HAREC (A) | Svi opsezi + ekskluzivni segmenti | 1500 W |

=== "Velika Britanija (RSGB/Ofcom)"
    | UK razred | CEPT ekvivalent | Max snaga |
    |-----------|----------------|----------|
    | **Foundation** | — (sub-Novice) | 10 W |
    | **Intermediate** | — | 50 W |
    | **Full Licence** | CEPT HAREC (A) | 400 W |

=== "Njemačka (Bundesnetzagentur)"
    | DE razred | CEPT ekvivalent | Max snaga |
    |-----------|----------------|----------|
    | **Klasse E** | CEPT Novice (B) | 100 W |
    | **Klasse A** | CEPT HAREC (A) | 750 W |

=== "Japan (JARL/MIC)"
    | JP razred | Opis | Max snaga |
    |-----------|------|----------|
    | **4级** (4th class) | VHF/UHF lokalni | 10 W |
    | **3级** (3rd class) | Prošireni HF | 50 W |
    | **2级** (2nd class) | Puni HF | 200 W |
    | **1级** (1st class) | Sve + AM broadcast | Bez limita |

---

## Posebne pozivne oznake

### Kratke pozivne oznake (Short callsigns)

Nositelji A razreda mogu zatražiti kraće pozivne oznake:

*   **Dvoslovna**: `9A1A`, `9A2B` — posebno prestižna, rijetka
*   **Troslovna**: `9A1AB`, `9A3CD` — standardna, lako dostupna
*   **Četveroslov**: `9A1ABC` — najčešća

### Posebne i memorijalne postaje

*   `9A0` prefiks — memorijalne i jubilarne ekspedicije
*   Klubovi na natjecanjima — specijalni callsign za contest period
*   SOTA ekspedicije — koriste `/P` sufiks

---

## Primjeri pozivnih oznaka iz prakse

| Situacija | Callsign |
|-----------|---------|
| Normalan rad s kućne stanice | `9A1ABC` |
| SOTA aktivacija | `9A1ABC/P` |
| Mobilni rad iz auta | `9A1ABC/M` |
| Rad na brodu | `9A1ABC/MM` |
| Rad u Italiji (Novice) | `I/9A1ABC` ili `9A1ABC/I` |
| Rad u Italiji (HAREC A) | `I/9A1ABC` ili uz T/R 61-01 prava |

---

## Povezane teme

*   [Kako postati radioamater](exams.md) — Ispitni postupak i tečajevi
*   [Hrvatski propisi](croatian_regs.md) — Pravilnik i snage po razredima
*   [Radioamaterska etika](ethics.md) — Ponašanje na opsegu
*   [Pozivne oznake](callsigns.md) — Format i dodjela
