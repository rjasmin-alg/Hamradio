# Sigurnost u radu

Sigurnost je apsolutni prioritet u radioamaterizmu. Radioamateri rade s **visokim naponima** (do 3000 V i više u pojačalima snage), **RF elektromagnetskim poljem** i na **visinama** pri postavljanju antena. Svake godine nesreće na antenama i pri popravku opreme završe tragično — jer se nisu slijedila osnovna sigurnosna pravila.

!!! danger "NIKADA ne zanemarujte sigurnost"
    Ova stranica može vam spasiti život. Pročitajte ju u cijelosti, a ne samo dijelove koji vam se čine relevantni.

---

## Električna sigurnost

### Opasnosti visokih napona

Suvremeni transciiveri rade na 13.8 V — relativno sigurno. Ali mnoga pojačala snage (PA), stara cijevna (tube) pojačala i visoko-naponski napajači koriste napone koji su smrtonosno opasni:

*   **Linearna pojačala (tube PA)**: 2000–4000 V na anodi
*   **Elektrolizatorski kondenzatori u napajanjima**: 400–500 V (SMPS) do 3000+ V (tube)
*   **Antena na kraju dipola**: Tisuće volti RF napona pri 100 W snage

!!! danger "OPASNOST: Kondenzatori ostaju nabijeni!"
    Nakon isključivanja opreme, **velikih filtarskih kondenzatora mogu ostati nabijeni 30 minuta ili dulje** na smrtonosnoj razini. Nikada ne otvarajte kućište odmah nakon isključivanja. Uvijek prazite kondenzatore otpornikom (npr. 10 kΩ, 10 W) priključenim na prikladnom štapu — nikada rukom!

### Pravilo jedne ruke

Pri radu na otvorenoj, potencijalno nabijenoj opremi, uvijek koristite **jednu ruku** a drugu držite u džepu ili iza leđa.

**Zašto?** Električni udar ubija jer struja prolazi kroz srce. Ako struja ulazi u jednu ruku i izlazi drugom — prolazi kroz srce. Ako koristite samo jednu ruku, put struje je ruka → noge → tlo (manje vjerojatno da prođe kroz srce).

!!! warning "Rad na otvorenoj opremi"
    - Uvijek isključite napajanje i pričekajte 5 minuta minimum (30+ minuta za tube PA)
    - Provjerite napon mjernim uređajem PRIJE dodirivanja
    - Nikada ne radite sami — neka netko bude u blizini
    - Koristite certificirane dielektrične alate (s izoliranim ručkama)
    - Nikad ne premošćujte osigurače — oni štite vas i opremu

### Zaštita od prenapona i kratkih spojeva

*   **Osigurači**: Svaka oprema mora imati osigurač na napajanju odgovarajuće vrijednosti. Nikada ne postavljajte veći osigurač da bi "riješili" problem pregorijevanja.
*   **Zaštitna dioda**: Pri spajanju 12 V napajanja uvijek provjerite polaritet — obrnuti spoj može odmah uništiti tranzistorska pojačala.
*   **Feritni prsteni na napajanju**: Sprečavaju RF signale da uđu u napajanje i uzrokuju EMI probleme.

---

## RF Sigurnost — Elektromagnetsko polje (EMF/PEM)

### Što je RF izlaganje?

Radio valovi su neionizirajuće elektromagnetsko zračenje — ne oštećuju DNA kao rendgenske zrake ili gama zrake. Međutim, pri dovoljno velikim snagama **griju tkivo** (kao mikrovalna pećnica). Oči i testisi su posebno osjetljivi jer ne mogu lako odvesti toplinu.

### ICNIRP smjernice

Međunarodna komisija za zaštitu od neionizirajućih zračenja (ICNIRP) definira **MPE** (Maximum Permissible Exposure) limite:

| Frekvencija | Limit za općenitu populaciju | Limit za profesionalce |
|-------------|------------------------------|----------------------|
| 3–30 MHz (HF) | 28 V/m (električno polje) | 61 V/m |
| 30–300 MHz (VHF) | 28 V/m | 61 V/m |
| 300 MHz–3 GHz (UHF) | 1.375√f mW/cm² | 5 mW/cm² |

!!! note "Hrvatski propisi"
    U Republici Hrvatskoj primjenjuje se Pravilnik o zaštiti od elektromagnetskih polja (NN 204/03), koji se bazira na ICNIRP smjernicama. Radioamateri su obvezni provoditi proračun MPE za svoju stanicu ako koriste više od 100 W ERP.

### Procjena sigurne udaljenosti

Aproksimativna formula za slobodni prostor (najgori slučaj):

$$ d_{min} = \frac{\sqrt{P \cdot G}}{2\pi \cdot MPE_{E}} $$

Praktična tablica za tipične amaterske instalacije:

| Snaga | Antena | Frekvencija | Min. udaljenost (opća populacija) |
|-------|--------|-------------|----------------------------------|
| 10 W | Dipol (2.15 dBi) | 14 MHz | ~0.5 m |
| 100 W | Dipol (2.15 dBi) | 14 MHz | ~1.5 m |
| 100 W | Yagi (10 dBd) | 14 MHz | ~5 m |
| 400 W | Dipol | 144 MHz | ~3 m |
| 100 W | GP | 432 MHz | ~1 m |
| 1500 W | Yagi | 144 MHz | ~25 m |

!!! warning "Posebno osjetljiva mjesta"
    RF izlaganje je osobito zabrinjavajuće za:
    - **Oči**: Leća oka ne može odvesti toplinu i može razviti kataraktu
    - **Testise**: Slično, bez efikasnog hlađenja
    - **Trudnice i djeca**: ICNIRP preporuča 50% vrijednosti limita
    - **Nositelji srčanog stimulatora (pacemaker)**: Konzultirajte liječnika

### Smanjenje RF izlaganja

1.  **Visina antene**: Što je antena viša, to je veće polje dalje od stambenog prostora.
2.  **Smjer antene**: Usmjerite Yagi antenu dalje od kuće i susjednih zgrada.
3.  **Snaga**: Koristite minimalnu potrebnu snagu (QRP kad god je dovoljno).
4.  **Vrsta antene**: Vertikalne antene imaju nizak kut izlaza — dobar za DX, ali RF polje na tlu je jače.
5.  **Daljinski upravljač**: Koristite CAT sustav i ne budite blizu antene pri odašiljanju.

---

## Zaštita od groma

### Rizik munje

Munja može udariti u antenu ili u okolno tlo i induktivno prenijeti ogromne napone kroz vaš kabel do opreme i do vas. Direktni udar iznosi **milijune volta i tisuće ampera** — ni jedan odvodnik ne može zaštititi od direktnog udara. Cilj je smanjiti štetu od induciranih prenapona.

!!! danger "NAJVAŽNIJE PRAVILO"
    Pri grmljavini — **isključite antenu iz uređaja i fizički izvucite koaksijalni kabel** iz sobe. Niti jedan odvodnik prenapona nije zaštita od direktnog ili bliskog udara munje. Jedina sigurna mjera je odvajanje.

### Sustav zaštite od groma

Detaljan opis sustava uzemljenja i zaštite od groma dostupan je na stranici [Uzemljenje i zaštita](grounding.md). Ključne točke:

*   **Single Point Ground (SPG)**: Sve kabele i mase dovodi na jednu uzemljenu točku u stanici.
*   **Odvodnici prenapona (SPD)**: Instalirati na ulazu kabela u kuću — štite od induciranih prenapona (ne od direktnog udara).
*   **Diskonekcija**: Ugradite prekidače na kabelima koji omogućuju brzo odvajanje antene.
*   **Ferritni torusi**: Na kabelu blizu ulaska u kuću — sprječavaju RF struje na plaštu.

### Statički elektricitet

I bez grmljavine, antene skupljaju statički elektricitet (posebno za vjetrovitog i oblačnog vremena). Ovo može oštetiti ulazni tranzistor u prijemniku.

*   Koristite **gas discharge tubes (GDT)** ili **MOV odvodnici** između kabela i mase
*   Ferritna prigušnica na ulazu prijemnika pomaže smanjiti statički šum

---

## Sigurnost pri radu na visini

### Opasnosti

Postavljanje antena zahtijeva rad na krovovima, jarbolima i drveću. Pad s visine od samo 3 m može biti smrtan.

!!! danger "Zakonska obveza"
    U Republici Hrvatskoj, rad na visini zahtijeva primjenu osobnih zaštitnih sredstava (OZS) — sigurnosni pojas, karabineri, sidra. Ovo je zakonska obveza, ne preporuka.

### Obvezna zaštitna oprema

*   **Certificirani sigurnosni pojas** (harness) klase C (za rad na visini), ne samo pojas od sportskog penjanja
*   **Karabineri** s duplim zatvaranjem (EN 362)
*   **Vida linija** (lanyard) s amortizerom pada
*   **Zaštitna kaciga** — za zaštitu od pada predmeta odozgo
*   **Radne rukavice** — zaštita od oštrih rubova

### Sigurnosna pravila

1.  **Nikada sami**: Uvijek mora biti netko na tlu koji drži uže i može pozvati pomoć.
2.  **Provjera vremena**: Ne penjite se po kiši, snijegu, jakom vjetru ili grmljavini.
3.  **Pregled opreme**: Svaki put pregledajte konope, karabinere i sidrišta.
4.  **Dalekovodi**: Minimalna sigurna udaljenost od nadzemnih dalekovoda je **10 m** (pri normalnom radu) — obavezno provjerite s HEP-om za konkretnu instalaciju.
5.  **Upute za pad**: Naučite STOP tehniku — ne paničarite, sigurnosna oprema vas drži.

!!! warning "Blizina dalekovoda"
    Antenski elementi i vodovi ne smiju se nalaziti bliže od 10 m od nadzemnih vodova. U slučaju pada antene ili koaksijalnog kabela, on ne smije moći doseći dalekovod. Ako niste sigurni, kontaktirajte HEP distributera za procjenu.

---

## Zaštita opreme

### Zaštita od prekomjernog SWR

*   Uvijek provjerite SWR prije povećanja snage
*   Nikada ne odašiljajte u otvoreni kabel (bez antene)
*   Koristite odgovarajući SWR zaštitni sklop ili ugrađenu zaštitu u transciiveru

### Zaštita od prenapona na 230 V mreži

*   Koristite UPS (uninterruptible power supply) ili surge protector s odgovarajućom energetskom zaštitom (>1000 J)
*   Za audio/CAT kablove koristite galvanski izolirane verzije

### Zaštita izlaza predajnika

*   Nikada ne spajajte antenu i terminiranu dummy load istovremeno bez odgovarajućeg RF preklopnika
*   Pri ugađanju koristite dummy load, ne antenu u stanu

---

## Prva pomoć pri strujinim udarom

!!! danger "HITNO — Strujni udar"
    Pozovite hitnu pomoć (112) odmah. Strujni udar može uzrokovati zastoj srca koji nije odmah vidljiv.

### Korak po korak

1.  **NE DODIRUJTE žrtvu golim rukama** dok je još spojena s izvorom struje — vi ćete postati sljedeća žrtva
2.  **Prekinite izvor**: Isključite struju na glavnom prekidaču, osiguraču ili izvucite utikač — koristite drvo, suhu tkaninu ili rubber-izolirani alat
3.  **Tek tada**: Odmaknite žrtvu od izvora struje (suhim drvom, vrpcom)
4.  **Pozovite 112** i opišite što se dogodilo
5.  **Provjera stanja**: Provjerite dišanje i puls
6.  **KPR** (Kardiopulmonarna reanimacija): Ako nema disanja i pulsa, odmah počnite sa 30 kompresija prsnog koša, zatim 2 udaha — i nastavite do dolaska hitne pomoći
7.  **Stabilni bočni položaj**: Ako diše ali je nesvijestan

!!! tip "Naučite KPR"
    Svaki radioamater bi trebao pohađati tečaj prve pomoći. Hrvatski Crveni križ organizira tečajeve KPR u svim većim gradovima. Potrvda vrijedi 2 godine.

---

## Sigurnosna kontrolna lista (Checklist) za stanicu

Pregledajte svoju stanicu redovito prema ovoj listi:

- [ ] Sva oprema je uzemljena na zajedničku točku (SPG)
- [ ] Osigurači na napajanju su ispravni i odgovarajuće veličine
- [ ] Koaksijalni kabel je u dobrom stanju (bez preloma, erozije)
- [ ] Postoji odvodnik prenapona na ulazu kabela u kuću
- [ ] Postoji mehanizam za brzo odvajanje antene pri grmljavini
- [ ] Znate gdje je glavni prekidač struje u vašem domu
- [ ] Pohađali ste tečaj prve pomoći u zadnje 2 godine
- [ ] Vaša obitelj zna što napraviti u slučaju nesreće

---

## Resursi i vanjske reference

*   [**ICNIRP smjernice**](https://www.icnirp.org) — Međunarodne norme za elektromagnetska polja
*   [**ARRL RF Safety**](https://www.arrl.org/rf-exposure) — Kalkulator RF izlaganja
*   [**OZ7IGY RF Exposure Calculator**](https://www.oz7igy.dk/rfsafety/) — Online MPE kalkulator
*   [**HRS — Hrvatska radioamaterska savez**](https://www.hrs.hr) — Informacije o propisima

---

## Povezane teme

*   [Uzemljenje i zaštita od groma](grounding.md) — Detaljan sustav SPG, odvodnici, radijali
*   [Antene i vodovi](antennas.md) — SWR, RF naponi na anteni
*   [Osnove elektronike](electronics.md) — Kondenzatori, transformatori, visoki naponi
