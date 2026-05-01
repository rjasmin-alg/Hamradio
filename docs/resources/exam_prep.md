# Priprema za radioamaterski ispit

## Uvod
Kako bi se radioamater snalazio s opremom a samim time bio neovisan operater radijske stanice on nužno mora ispunjavati tehničke preduslove propisane regulativama države te provesti testiranje znanja, čime po uspjehu pridobiva svoju licencu. Sama priprema mora stoga zahtjevati dosljedan pristup i **istinsko razumijevanje, a nikako učenje napamet metoda!**. 

Ovaj članak Vam predstavlja konzistentnu, višetsretnu rutinu učenja i prolaska za dobivanje "P" od HAKOM inspektora - prolaskom!

## Plan učenja (Preporuka 2 do 3 mjeseca radna rasporeda)

!!! tip "Dnevni prioritet — Pravilo konzistentnosti"
    Učenje radioamaterskih opsega i gradiva ne mora biti pretrpano i dugo. Upisivanje 30-45 minuta kvalitetnog aktivnog vremena **SVAKI DAN** bitno osnažuje put k rezultatu dok vikend "štrebanje i opijanje od 4 sata memorija" vodi do teških padova i rupa u gradivu pred testnim zadatcima.

Ovo je vremenski raspored organizacije kojim se provjereno osigurava najbolji uspjeh na državnim pragovima položenosti za oba razreda A/B.

| Tjedan obrade | Područje i tema | Reference gradiva u Priručniku | Cilj Provjere |
|---------------|-----------------|---------------------------------|---------------|
| Tjedan 1 i 2 | Propisi, uvjeti, dozvole | [regulativa](../regulations/index.md) i struktura | Imati sažetak opsega i ključnih HAKOM ograničenja moći i znanja prekršaja |
| Tjedan 3 i 4 | Osnove elektronike | [electronics.md](../technical/electronics.md) | Potrebno proći tečne izračune Ohmovog zakona, LC titrajne filtre|
| Tjedan 5 i 6 | Antene te dometi vodovi | [antennas.md](../technical/antennas.md) & [propagation.md](../technical/propagation.md) | Znam definirati razliku dometa po visini frekvencije dipol i SWR logiku te refleksiju |
| Tjedan 7 i 8 | Operatibilnost, Modovi, procedura | [modes.md](../operating/modes.md), i ostale [operating stranice](../operating/index.md) | Znam koje se frekvencije rade na donjem side-bandu LSB i USB princip. Q-kodove obavezno |
| Tjedan 9 i 10| Ljudsko zdravlje, izloženosti, Sigurnost, Sustavno | [safety.md](../technical/safety.md) te [grounding.md](../technical/grounding.md) | Razumijevanje principijelnih životnih situacija i kako u kratkom procjeniti rad |
| Tjedan 11 i 12| Ponavljanje za ispit, provjere ispita (repeticija) | Kompletno gradivo | Polagati probne ispite preko 80% prolaza redom svaku varijacu|

---

## Sažetak gradiva s linkovima

### Propisi i dozvole

Najbitnija stvar za razlikovati za Vaše legalno sudjelovanje. Istražite više u stranicama pod [Razrede dozvola](../regulations/license_classes.md), kao i unutrašnjim organizacima krovnih [Hrvatskih propisa](../regulations/croatian_regs.md).
KLJUČNI SAVJET ZA PAMĆENJE: Zlatno pravilo "A razreda." Da biste uistinu smjeli raditi apsolutno kroz *sve CEPT zemlje s prijenosnom opremom bez prijave*, uvijek morate biti imalac "A RAZREDA" kako piše u [Međunarodnim propisima](../regulations/international_regs.md). B opsezi ograničeni su i snagom i na manji prozor rada te su nacionalno definirane oštrije.

### Osnove elektronike

Nemilosrdno ali obavezno, čista fizika radio veze. Sadržaj ponovite kroz prozor lekcije [Osnova elektronike i sklopova](../technical/electronics.md).
KLJUČNI SAVJET ZA PAMĆENJE OVDJE: Tri formule za spas testnog zadatka: Ohmov zakon (U=R·I), Izračun snage za termalne efekte (P=U·I), te jednadžba rezonantne LC frekvencije (f=1/2π√LC). Tu pada do 30% korisnika brzopletosti!

### Antene, rad i procedure

Prilikom prelaska radnje pročitajte procedure uspostavljenih radio modova. Razliku pročitajte pod [Frekvencijski planovi (Bandplan)](../operating/bandplans.md) i [Procedura Veze](../operating/procedures.md). Za općenit pregled tehničkijeg dijela prijamnika proučite [Primopredajnike](../technical/transceivers.md).

---

## Primjeri ispitnih pitanja (s objašnjenjima pravog odgovora)

Pitanja variraju s godinama no suštinska narativna logika ostaje standardizirana iz europske CEPT regulative te same administracije. Važno je *shvatiti ZAŠTO ste prešli odgovor*.

### Pitanja: Propisi

**Pitanje 1: Koji razred dozvole u HR omogućuje rad na apsolutnoj radnoj listi svim amaterskih opsezima i najvišim snagama?**  
**Točan Odgovor:** Razred A (CEPT razred dozvole).
> **Zašto?**: Razred N  (nacionalni) i Razred B imaju visoka restriktivna ograničenja na snage emitiranja uređajima pa i propisane suženja na pojedinim valne duljine te nisu primjenjive nigdje izvan granica Lijepe Naše. Samo Razred A omogućuje međunarodnu slobodu kroz T/R 61-01 preporuke.

**Pitanje 2: Što je direktna CEPT dozvola te kakva to prava na putu nosiocu ona dodijeljuje?**  
**Točan Odgovor:** Ugovor, sporazum država po kojem dozvola stvara automatsko priznavanje valjanosti prava amatera država u preko 50 CEPT entiteta i uprava.
> **Zašto?**: Time štedite i papire o radu te s time dok putujete, ne treba Vam nikakva dozvola za primjerice posluživati ručnu stanicu na ljetovanju na mediteranu sa Vašom matičnom HRS/HAKOM dozvolom! Samo nadodate prefiks države gdje ste trenutačno prije oznake (npr IO / 9A1ZG).

---

### Pitanja: Elektronika i fizika

**Pitanje 3: Otpornici R1 od 100Ω i teži R2 od 150Ω spojeni su klasično, linearno i serijski. Koliki je njihov ukupan prepoznati otpor kruga?**  
**Odgovor:** 250 Ω (R = R1 + R2 = 100 + 150).
> **Zašto to funkcionira tako?**: U serijskom slijedu provodenja ne mijenjate protok ili grane. Isti protok juri od točke jedan na dva te naprosto nailazi kroz dvije prepreke zaredom, stoga im se ukupne sume zbrajaju na padove voltaže strujnih mjesta.

**Pitanje 4: Koji presudni element u Vašem pasivnom pretražnom LC zavojničkom sklopnome mjestu filtriranja u suštini određuje i definira "rezonantnu" frekvenciju tog dijela radiouređaja?**  
**Odgovor:** OBA (Zavojnica Induktoreta i Kapacitetni filter kondenzatora). 
> **Zašto?**: Matematička definicija (f = 1 / (2π√(LC))) je očito vezana preko dva korijena umnožanka na dnu razlomaka. Oboje L & C su jedina ovisnost bez obzira kakvi drugi naponi prolazili. Kada bi umjetno u testu Vas probavali, recimo kako se smanji, Povećanjem elemenata rezonanca pada. A smanjivanjem obodnih vrijednosti komponentnih - Vi frekvenciju zapravo podižete k višim bandovima.

**Pitanje 5: Kakav pojam opisuje riječ Impedancija radiostanice do izlazih oboda?**  
**Odgovor:** Impedancija prikazuje mjerljivi ukupan i združen otpor čitavoj propustljivoj visokofrekventnoj izlaznoj energiji iz zida ili signala (Z = R + jX).
> **Zašto?**: U pravom amaterskom okruženju, sva industrija se složila odraditi i regulirati uređaje, kablove od bakrenog oklopa i preklopnike obvezno oko praga 50 Ohma. Kada to prestane zbog različite greške – ta ista izmjenična AC snaga vraća radijaciju unazad - naziva se mjerilost SWR i time u opasnost stavljate elektronički sklop za emitiranje uništivši primopredajnik radije negdje pri pradavanjima bez izručivanja ka vanjskome ambijentu.

---

### Pitanja: Antene i domet radiovalne propagacije 

**Pitanje 6: Koji točni Ionosferski najviši oblak reflektirajućeg atmosferskog omotača donosi primat nad svakom kvalitetom dugorečnog DX prijenosa preko granica dometa u dnevnom pjevu Kratkih Valova (HF)?**  
**Odgovor:** Glavni odgovorni element za DX na ovim valovima u svako doba pa time i noćima radi postojanja zrači dugorazmjerni refleks gornjeg  **"F2"** sloja ionosfere na samoj sredini do 400 KILOMETARA!
> **Zašto?**: Ostali D (izuzetni upijač kratkih valova niži od 100km te obavezan prigušivač, te povremeni "E - sloj, tekući reflektor, nestanu sa zalaskom zvjezde jer gube svijež naboj energije ioniziranjem sunčevim bakljavim fotonima. Samo F2 drži dovoljno atoma noću te Vas dovodi oko globusa i u podne i u 4 ujutro.

**Pitanje 7: Mjerenjem u svom "šubitu" opazite na digitalnoj vagi uređaja da radna SWR razina mjerila na 3:1 s upaljenim pojačalom! Kakve su nam implikacije?**  
**Odgovor:** Pretilost i teška asimetrija rezonancije same neslaganjem antene i uvijetirane 50 ohmske impedancije na vodu prenosti snove u vatru - Gubitak od do golemih 50% ukupnog prenesenog Wattnog sustava i energije koje odlaze povratno natrag iz prigušnog radijatora antene k hladnjacima Vašeg izlaznog RF sklopa.
> **Zašto to primijetiti?**:  Jedini dobar (1.0 : 1) odnos SWR koeficijenta i manji od 1.5 vas sprječavaju uništavanju komponentata pojačala. Ovdje ćete pregrijavati uređaj na opštim nivoima te se traži podešnjavane ili obustavljanje emitiranih frekvenci,

---

### Pitanja: Komunikacijsko ophodište (Modovi i regulacije)

**Pitanje 8: Koja se točna i stroga vrst tonsko usmjerne radijske govorne emitirane pojave preferira obavezno ukoliko ste locirani ispod praga 10 MHz za sve kratkovalne (HF-DX) pojasne krupnorezerivane i ostale radije komunikacijske aspekte?**  
**Odgovor:** Donji sporedni band na skali (LSB - Lower Side Band)
> **Zašto se razlikuju?**: Ovaj standard prihvatio cjelokupan svijet bez obzirom tko diktira granice regija! USB-om će svi slušatelji u Europi za opsege 20, te ostale koji preskaču obvezni standard i prag prve crte iznad broja 10 (odnosno kratki valovi višeg ranga na gore i sve u UKV polozajima komunikacije) smatrati greškom koja krsi pravilan ton. 

**Pitanje 9: Začujete li s druge strane od sugovornika kao odgovor "Molim ponovi to ponovno, a moj je sud i mišljenje da ste mi upravo QSL", on Time misli na Vaš stav i potvrdjuje...?**  
**Odgovor:** Prevod "QSL" se tu ponaša kao pozitivni dokaz "Potvrdno sam zaprimio što si rekao u teškom trenutku s puno šuma te to razumio".
> **Zašto baš tako?**: Značenje telex procedurnih simbola unutar radijskih valova poput famoznih "Q Kodova" jest uvijek dvojnost značeju ukoliko nemate "?" upitnika. Kod telegrafije "QSL ?" pita *Jeste me potvrdili?* a QSL samo za sebe navješćuje potvrdan i završen dokaz sukladnosti shvaćanja prijenosa kretki.

---

### Pitanja: Život i okružje (Zdravstvene i primjena opće stanice - Sigurnost)

**Pitanje 10: Skrbite za pokvarenim teškim strujnim naponskim linijskim stabilizatorima (napon 230 i preko do stanice od pola i dva ampera amaterskog ispravljača te uređaja ali vi ste napajanje iz stisnuli isključkom te je "Mrtvo"). Otkuda dolaze upozorenji pogotova unutra od tehničara za visoku izuzetan stupanj nesretnih smrtnih ishoda?**  
**Odgovor:** Elektrolitički mrežni predimenzionirani "Kapacitetni" filtarski *Kondenzatori.* Oni čuvaju unutra i tiskaju visok radni smrtonosan strujni pogon i razarajući "naboje" - prenaponski rizik nažalost preostaju danima a u trenutnom ruku 20tak i preko desetina redovnih minuta prešućuju se unutra u kanti dok ga vaša opasnost ne odrješava direktno tijelom doticanjem bakra!
> **Zašto ostaje mrtva zona živa?**: Razina koju prve faza mrežnog stabilizacijskog procesora i transformatora daju preko tri-sto radnih V-a i doživoti strujni tok na takve tegle pohranjuje sve kroz gretčeve blokove kako ih izvodite pri emitiranih valova s velikim vrhovim, a kako oni nemaju prirodna curenja, oni prazne ulogu bez utjecaja i "potrošnje", zbog čega ih praznite direktno opasnošću preko ruke ukoliko dirate prebrzano matičnu i rastaljenu sklopnu građu opreme pa Vas je stresla životno pogubna frekvencija srca!

!!! danger "MPE Pravila Osvarenosti (Maximum Permissible Exposure)"
    Maksimalno RF polje koje radio operator sa svoje snage zračenja stavi kroz prozore stana zgušnjava i može otežavati propustljivo i ljudskom zdravlju neprimjetnoj mikrovalnoj okvirom ICNIRA razredu obustavljajući ljudske procesa na do 10 vata po poljima metarskog kvadrata. Propisanom normativnom mjerilima to podrazumijeva - ZAKON vas provodi pod zakletvama osiguravanju udaljenja svake instalirane krovne žarišta dalje i potpuno dalje ljudskih okoliša ili pristupanja djece gdje opterećavaju granicu poljima!

---

## Savjeti za veliki dan – Kako napisati i okončati test?

- **Pobrini se i Ponesi ranije spremno:** Nemojte u glavu misliti. Obavezan dolazak i predočenja teške papirologije uz Osobnu Ispravnicu izdanu MUPu, i raniji pozivnica-uputak za lokaciju prijavništva uz doprinos pisanja drvene grafitne "Penkalo-olovkice" kako su testri rabe papirnati u nekim centrima i okolišini su!
- **Dostupnost dopušštene pomoćne aparature Kalkulatora:** HAKOMov ispit je najčešće dozvoljena obrada kalkulator, ALI strogo neprograbilan standardni! Pametne aplikacije za iPhone s funkcijom na stolu su neprihvatljive!
- **Osnovna psihološka tehnika pri rješavanja pitanja:** Obujmi sate koje gori. Čitaj testnu preostalu okoliš **DO zadnje kvrge / zareza** i rečenicu, mnogo lakih krugova eliminacija promaše zbog jedne ubačeno riječi "ne". Probajte poćeti izuzetke od odgovora koji sigurna i asolutno smisla padaju vodom te smanje preostale varijacije.
- **Nesigurnost blokade pri panici:** → Ostavite ih praznim odmah! Označi zvjezdicom rub olovkom, stisni rješavanje dalje te prekinute krug provalivanjem naprijed kako bi adrenalin tijela nebi popustio pod koncentracijskom neimaštinom okidanja greški, onda pred pregled se opet ponovno vratite tim preostalim praznicama pred završetke radne liste.

## Online resursi i virtualna testiravnja
Niste prepuštena na vjetru. Postoje rješanjsja:
* **Hrvatska HRS arhiva materijala:** Pronađi zadnje dostupne popise dokumentacija pri samom mjestu prijave za priručnike klubova uz zadane ispisom PDF-ova zadnjih HAKOMovih ispita!
* **Međunarodne opcije:** Međunarodni CEPT model je jako blizu onima u EU pod bazom RadioAmateur.Eu s Europskim usmjerenjem kao odlični logični virtualno brzi interaktivni sustava za nabijanje i predočavanje ispita na stranom engleskom, pa tako i jako vizualnim testnim *Ham Test Online* (hamstudy.org) kao preporuka - bez obzira šta US FCC fokusiran pristup po istinitim formulama. Zato su pravila međunarodno obuhvatljiva - zakoni u svemiru ne vide regulaciju države pri valnim odbacivima!

---

## Ključne formule s MathJaxom

Ove formule **morate znati** za tehnički dio ispita:

### Ohmov zakon

$$U = I \cdot R \qquad I = \frac{U}{R} \qquad R = \frac{U}{I}$$

Gdje: U = napon [V], I = struja [A], R = otpor [Ω]

### Električna snaga

$$P = U \cdot I = \frac{U^2}{R} = I^2 \cdot R$$

### Serijsko spajanje otpornika

$$R_{uk} = R_1 + R_2 + R_3 + \ldots$$

### Paralelno spajanje otpornika (2 otpornika)

$$R_{uk} = \frac{R_1 \cdot R_2}{R_1 + R_2}$$

### Rezonantna frekvencija LC kruga

$$f_r = \frac{1}{2\pi\sqrt{LC}}$$

### Duljina dipola

$$L_{dipol} = \frac{143}{f(\text{MHz})} \text{ m} \qquad L_{krak} = \frac{71.5}{f(\text{MHz})} \text{ m}$$

### Frekvencija i valna duljina

$$\lambda \approx \frac{300}{f(\text{MHz})} \text{ m}$$

### dB omjer snage

$$\text{dB} = 10 \cdot \log_{10}\left(\frac{P_1}{P_2}\right)$$

Brze referentne vrijednosti: **+3 dB** = 2× snage; **+10 dB** = 10× snage

---

## Brze ispitne kontrolne kartice

### Propisi — morate znati

| Stavka | Vrijednost |
|--------|-----------|
| N razred max snaga | 10 W |
| B razred max snaga | 100 W |
| A razred max snaga | 1000–1500 W |
| CEPT Novice | B razred |
| CEPT HAREC | A razred |
| Hrvatska 9A prefiks | Dodijelio ITU |
| HAKOM | Regulatorna agencija |
| HRS | Nacionalni savez |
| WARC opsezi (bez contesta) | 30 m, 17 m, 12 m |
| Identifikacija svaki | 10 minuta |

### Modovi — gdje koji

| Opseg | LSB ili USB? |
|-------|------------|
| 160 m, 80 m, 40 m | **LSB** |
| 20 m, 17 m, 15 m, 12 m, 10 m | **USB** |
| VHF/UHF SSB | **USB** |
| VHF/UHF FM | FM, niti LSB ni USB |

### Q-kodovi — obavezni

| Kod | Značenje |
|-----|---------|
| QRL | Frekvencija zauzeta |
| QRM | Smetnje od stanica |
| QRN | Atmosferski šum |
| QRP | Mala snaga |
| QRT | Prekidam rad |
| QRZ | Tko me zove? |
| QSL | Potvrđujem |
| QSO | Veza |
| QSY | Mijenjam frekvenciju |
| QTH | Moja lokacija |

---

## Savjeti za visoku prolaznost

1.  **Propisi su kritični** — Greške iz regulatorne kategorije imaju viši prag za prolaznost. Naučite ih temeljito.

2.  **Razumijte formule, ne memorizujte** — Ohmov zakon ima logiku (više napona → više struje uz isti otpor). Logika ostaje u sjećanju, memorija ne.

3.  **Eliminacijska metoda** — Ako niste sigurni, eliminiranjem jasno pogrešnih odgovora preostaju samo 1–2 opcije.

4.  **Prijevarni Q-kodovi** — Pitanja s "?" i bez "?" imaju različita značenja. Pažljivo čitajte.

5.  **Vježbajte vremenski** — 30–45 pitanja u 45 minuta = 1 min/pitanju. Trenirajte brzinu.

6.  **NATO abeceda napamet** — Na ispitu može biti pitanje o fonetici ili se traži spelanje.

---

## Što slijedi nakon ispita?

1.  Prijavite uspjeh HAKOM-u — zahtjev za dozvolu i pozivnu oznaku `9Axxx`
2.  Pronađite klub — **[HRS popis radioklubova](https://www.hamradio.hr/)**
3.  Pročitajte [Tvoja prva veza](../operating/first_qso.md)
4.  Pratite propagaciju: [SolarHam](https://www.solarham.net) i [PSKReporter](https://pskreporter.info)
5.  Eksperimentirajte — antene, FT8, CW

---

## Poveznice po segmentima

*   [Razredi dozvola](../regulations/license_classes.md)
*   [Kako postati radioamater](../regulations/exams.md)
*   [Hrvatski propisi](../regulations/croatian_regs.md)
*   [Fonetska abeceda](phonetic_alphabet.md)
*   [Procedure veze](../operating/procedures.md)
* **Međunarodne opcije:** Međunarodni CEPT model je jako blizu onima u EU pod bazom RadioAmateur.Eu s Europskim usmjerenjem kao odlični logični virtualno brzi interaktivni sustava za nabijanje i predočavanje ispita na stranom engleskom, pa tako i jako vizualnim testnim *Ham Test Online* (hamstudy.org) kao preporuka - bez obzira šta US FCC fokusiran pristup po istinitim formulama. Zato su pravila međunarodno obuhvatljiva - zakoni u svemiru ne vide regulaciju države pri valnim odbacivima!
