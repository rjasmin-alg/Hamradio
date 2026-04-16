# TEC-20 — Uzemljenje i zaštita od groma

| Polje | Vrijednost |
|-------|-----------|
| **Datoteka** | `docs/technical/grounding.md` |
| **Status** | 🔴 Ne postoji — kreirati od nule |
| **Prioritet** | P1 — Val 2 |
| **Složenost** | 🔧 Srednja |
| **Ovisnosti** | TEC-06 |
| **Završeno** | ☐ |

---

## Checklist

### Priprema
- [ ] Pročitati `01_VIZIJA_I_STANDARDI.md`
- [ ] Pročitati `docs/technical/safety.md` (ovisnost)
- [ ] Web search: "ham radio station grounding RF ground vs safety ground"
- [ ] Web search: "single point ground ham radio station setup"
- [ ] Web search: "lightning arrestor amateur radio antenna coax"
- [ ] Web search: "ham radio ground radials vertical antenna"
- [ ] Web search: "ground loop noise ham radio eliminate"

### Sadržaj koji treba napisati
- [ ] **Uvodni paragraf** — zašto uzemljenje i zašto je kompleksno (RF ≠ sigurnosno ≠ grom)
- [ ] **3 vrste uzemljenja:**
  - [ ] RF uzemljenje — smanjenje smetnji, referentni potencijal za antene
  - [ ] Sigurnosno uzemljenje — zaštita od strujnog udara (PE vodič)
  - [ ] Gromobransko uzemljenje — odvod energije gromom
  - [ ] Zašto moraju biti SPOJENE u jednoj točki (Single Point Ground)
- [ ] **RF uzemljenje:**
  - [ ] Zašto vertikalke trebaju uzemljenje/radijale
  - [ ] Radijali — koliko, koliko dugi, ukopani vs nadzemni
  - [ ] Counterpoise — alternativa za portable rad
  - [ ] Ground rod — kako zabiti, dubina, vlažnost tla
  - [ ] Bakelit vs ferit vs RF choke za audio uzemljenje
- [ ] **Single Point Ground (SPG):**
  - [ ] Koncept — sve ide u jednu točku (bakarna šina)
  - [ ] Dijagram SPG sustava za kućnu stanicu
  - [ ] Zašto izbjegavati petlje (ground loop → brum, smetnje)
- [ ] **Zaštita od groma:**
  - [ ] Arrestori (odvodnici prenapona) — vrste, gdje montirati (blizu ulaza, ne u sobi!)
  - [ ] Gas discharge tube vs MOV vs TVS dioda arrestori
  - [ ] Uzemljenje arrestora — debeli vodič, kratak put do šine
  - [ ] Odvajanje antene — zašto je jedina 100% zaštita
  - [ ] Izo-switch — daljinsko odvajanje
- [ ] **Česte greške:**
  - [ ] Ground loop između računala i radio — rješenje: galvanska izolacija
  - [ ] Slaba veza (visoka impedancija) u uzemljenjem sustavu
  - [ ] Arester spojen na cigaste uzemljenje (ne radi!)
- [ ] **Praktični vodič: minimalni SPG sustav**
  - [ ] Što kupiti, gdje montirati, korak po korak
- [ ] **Admonitions** — DANGER za grom, WARNING za greške, TIP za praktične savjete
- [ ] **Interni linkovi** — safety.md, antennas.md, emc.md

### Kontrola kvalitete
- [ ] Minimalno 2000 riječi
- [ ] Dijagram SPG sustava (tekstualno opisan, ne slika)
- [ ] DANGER admonition za grom
- [ ] **mkdocs.yml** — dodati pod Tehnika
- [ ] `.en.md` stub

---

## Prompt (kopiraj i pokreni agenta)

```
Zadatak: Kreiraj novu stranicu docs/technical/grounding.md u MkDocs priručniku.

KORAK 1 — Pročitaj:
- .plan/01_VIZIJA_I_STANDARDI.md
- docs/technical/safety.md

KORAK 2 — Istraži web:
- "ham radio station grounding RF ground safety ground difference"
- "single point ground ham radio setup guide"
- "lightning arrestor amateur radio coax installation"
- "vertical antenna radials ground plane how many"
- "ground loop elimination ham radio audio hum"

KORAK 3 — Napiši stranicu s minimalno 2000 riječi:

# Uzemljenje i zaštita od groma

## Uvod
- Tri različita uzemljenja — i zašto ih moraš razumjeti

## Tri vrste uzemljenja
### RF uzemljenje
- Referentni potencijal za antene, smanjuje smetnje i RFI
### Sigurnosno uzemljenje (PE)
- Zaštita od strujnog udara, EU norma, plavo-žuta boja pE vodiča
### Gromobransko uzemljenje
- Odvod energije gromom, separatno ali spojeno na SPG

## Single Point Ground (SPG)
- Princip: SVE uzemljene točke spojene u JEDNU bakarne šine
- Opisati dijagram: radio → šina ← računalo, šina → ground rod
- Ground rod: min 1.5m dubok, u vlažnom tlu, bakrena šina od 6-10mm2
- Zašto petlje (loops) stvaraju probleme: slika toka buke kroz petlju

## RF uzemljenje za vertikalne antene
- Radijali: minimalno 4, idealno 16-32, duljina λ/4 svaki
- Ukopani radijali vs nadzemni — prednosti i mane
- Counterpoise: portable rješenje za vertikalke bez tla
- Efekt: svaki dodani radijal smanjuje gubitke

## Zaštita od groma
- !!! danger: "Gromobransko uzemljenje" od struje NE štiti antenmki sustav!
- Arrestori: gdje ih montirati (IZVAN zgrade, na ulazu kabela)
  - Gas discharge tube: brz, za direktne udare
  - MOV (Metal Oxide Varistor): sporiji, za naponske uskoke
  - Preporučeno: kombinacija obaju
- Kakav vodič od arrestora do šine: minimalno 10mm2, CO kratak put
- Odvajanje antene: fizički isključi koaksijalku pri grmljavini

## Ground loop — problem i rješenje
- Simptom: brum 50/60 Hz u audio kad spojiš radio na PC
- Uzrok: potencijalna razlika između uzemljenja radija i PC
- Rješenje: galvanska izolacija (audio isolator), zajednička SPG točka

## Česte greške
- Arester spojen tankim žicom (ne radi!)
- Više različitih uzemljenja bez SPG (ground loop pojačava smetnje)
- Ground rod suh (suho tlo = visoka otpornost = loša zaštita)

## Minimalni preporučeni SPG sustav (korak po korak)
1. Bakarna šina 40x5mm pričvrsti na zid pokraj ulaza kabela
2. Sve koaksijalne kabele proveduji kroz Polyphaser arrestore
3. Areste poveži kratkim debelim vodičem (10mm2) na šinu
4. Šinu povoli na zajednički ground rod (16mm Cu, 2m duboko)
5. Sve metalne dijelove opreme u sobi spoji na šinu (kratkim vodicima)

KORAK 4 — Tehničke smjernice:
- !!! danger za grom i opasnu grešku s tanjim vodičima
- !!! warning za ground loop
- !!! tip za praktične savjete (radijali, SPG korak po korak)
- Interni linkovi: safety.md, antennas.md

KORAK 5 — Spremi u docs/technical/grounding.md (nova datoteka)
KORAK 6 — Dodaj u mkdocs.yml nav → Tehnika:
  - Uzemljenje i zaštita od groma: technical/grounding.md
KORAK 7 — Kreiraj stub docs/technical/grounding.en.md
```

---

## Bilješke o napretku

- 
