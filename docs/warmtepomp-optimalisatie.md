# Optimalisatie LG Therma V HN0913T – woning Eelderwolde (label A++)

*Opgesteld 11-11-2026 op basis van foto's van installatie, display, installateursmenu en de
vloerverwarmings-/ventilatietekening. Buitentemperatuur tijdens de metingen: 3 °C.*

---

## 1. In het kort

De warmtepomp **pendelt**: vanavond ruim **2 starts per uur** (≈ 50 per etmaal bij 3 °C), met
draaitijden van gemiddeld 16 minuten en pauzes van 11 minuten. De oorzaak is vooral dat de
**stooklijn veel te hoog staat** voor dit huis. De LG mikt bij 3 °C buiten op ≈ 34 °C
retourwater, terwijl het huis al warm genoeg is bij ≈ 22 °C retour. De pomp haalt zijn eigen doel dus
nooit, jaagt de compressor elke cyclus omhoog en wordt dan van buitenaf (thermostaat of
roomsensor) stilgezet.

**Top-6 aanpassingen (in volgorde van effect):**

| # | Wat | Nu | Advies |
|---|-----|----|--------|
| 1 | Stooklijn (Seizoensgeb. auto temp, op *Invoer*) | −10 °C → 45 °C / +20 °C → ≈19 °C | **−10 °C → 25 °C / +18 °C → 22 °C** |
| 2 | Hysterese verwarmingswater | Aan −2,0 / Uit +2,0 | **Aan −1,0 / Uit +3,0** |
| 3 | Temperatuursensor selecteren | (niet gefotografeerd) | **Water** (de bediening hangt in de berging) |
| 4 | Honeywell DT4 woonkamer | 20 °C, standaard schakelfrequentie | **21,5–22 °C als begrenzer**, CR = 3, OT = 5 min |
| 5 | Legionella-ontsmetting | 67 °C, vrijdag 12:00 | **60 °C**, vrijdag 12:00, 10 min |
| 6 | Stille modus | continu aan | **Alleen 's nachts** (schema) of uit |

Interactieve simulator van deze installatie, geijkt op de meting: `docs/simulator.html`. Daarin zitten
ook je zonnepanelen, het dynamische tarief en het warmwatergebruik van het gezin.

Daarnaast: de **berging** (3 groepen, staat nu op 21 °C) en de **slaapkamergroepen** waterzijdig
terugregelen in plaats van via de thermostaat, en de **twee groepspompen** zo laag mogelijk zetten.

**Gemeten COP (Samenvatting Energie ÷ Warmteafgifte):** dit jaar **2,2**, november **3,1**,
vandaag **2,7**. Voor deze unit bij vloerverwarming met ≈ 25 °C aanvoer is **4–4,5 of hoger**
haalbaar. Er valt dus veel te winnen. Bij een jaar-COP van 3,5–4 had dezelfde warmte (5.382 kWh)
dit jaar ≈ **850–1.050 kWh minder stroom** gekost (zie §3.3 en §8).

> **Let op garantie:** LG schrijft voor dat installateursinstellingen door een erkende installateur
> worden gewijzigd. Bespreek de wijzigingen in het installateursmenu met je installateur of laat
> hem/haar ze doorvoeren. De thermostaatinstellingen, DHW-temperatuur, AI-correctie en stille modus
> zijn gebruikersinstellingen.

---

## 1b. Zelf te doen, zonder installateursmenu: vaste watertemperatuur

De AI-correctie gaat op de LG maar tot **−5**. Met de huidige stooklijn (doel ≈ 34 °C retour bij 3 °C)
is dat te weinig; effect komt pas rond −10 tot −12. Wat wel werkt zonder installateur: zet de LG op het
hoofdscherm van **AI (Auto)** naar **Verwarmen (zon)** met een **vaste watertemperatuur**. Omdat er op
*Invoer* wordt geregeld, is dat de **retourtemperatuur**. Toegestaan bereik: 15–45 °C.

**Stel deze vaste watertemperatuur in, afhankelijk van het weer:**

| Buitentemperatuur (verwachting komende dagen) | Vaste watertemperatuur |
|---|---|
| boven 2 °C | **22 °C** |
| −2 tot 2 °C | **23 °C** |
| −6 tot −2 °C | **24 °C** |
| kouder dan −6 °C | **25 °C** |

Met daarbij: woonkamer-DT4 op **20,5 °C** (als bovengrens), 2:CR = 3, 3:OT = 5, geen nachtverlaging,
stille modus uit, warm water 11–16 uur, groepspompen op HD1 en de berging teruggeregeld (§6).

**25 °C, zoals nu ingesteld, is te hoog.** Bij 2–3 °C buiten gebruikt het huis maar ≈ 22 °C retour. Bij
25 °C haalt de warmtepomp zijn doel nooit en blijft de DT4 hem uitzetten: volgens de simulator nog
steeds ≈ 60 starts per dag. Bij 22 °C draait hij vrijwel continu.

| Simulator | Stroom LG per jaar | SCOP | Starts per jaar | Woonkamer in de winter |
|---|---|---|---|---|
| Huidig (AI, stooklijn 45/19) | ≈ 2.700 kWh | 2,55 | ≈ 11.300 | 20,0 °C |
| Vast 25 °C (zoals nu) | ≈ 2.695 kWh | 2,55 | ≈ 11.200 | 19,9 °C |
| **Vast met het weer mee (tabel)** | **≈ 2.325 kWh** | **2,95** | **≈ 390** | **20,0 °C** |
| Advies met installateur (stooklijn 25/22, AI −3) | ≈ 2.150 kWh | 3,0 | ≈ 350 | 20,0 °C |

Zonder installateur haal je dus ≈ 375 kWh per jaar van de ≈ 560 kWh. Het nadeel: bij omslaand weer
moet je de waarde zelf bijstellen. Doe je dat niet, dan wordt het bij vorst kouder in huis (bij 22 °C en
−5 °C buiten ≈ 18,5 °C) en bij zacht weer begrenst de DT4. De stooklijn van de installateur doet dat
automatisch en blijft daarom de beste eindoplossing.

**Op het display:** tijdens **Ontdooiing** is *Uitvoer* lager dan *Invoer* (bijv. 22 / 20 °C). Dat is
normaal: de warmtepomp draait dan even omgekeerd en haalt warmte uit het water om het ijs op het
buitendeel te smelten. Rond 0–4 °C en hoge luchtvochtigheid gebeurt dat meerdere keren per nacht.

---

## 2. De installatie (zoals uit foto's en tekening af te leiden)

| Onderdeel | Gegevens |
|---|---|
| Binnenunit | LG Therma V R32 **HN0913T** (Split IWT, 9 kW, 3 kW elektrisch element), buitendeel "Single" |
| Draaiuren | binnenunit 19.960 h (≈ 2,3 jaar onder spanning), interne pomp 4.107 h |
| Warm water | 180 L geëmailleerde, geïsoleerde boiler, DHW-setpoint 48 °C, nu 44 °C |
| Buffervat | 50 L staal, geïsoleerd, **4 aansluitingen = parallel buffer / hydraulische scheiding** |
| Primair debiet | 28,9 L/min (regeling "Optimale debiet", pomp 100 %), waterdruk 1,6 bar (prima) |
| Secundair | 2 groepspompen op de wand, **niet** door de LG aangestuurd ("Externe pomp gebruiken: Niet gebruiken") |
| Vloerverwarming | BG-verdeler 13 groepen + groep 1 naar de badkamer boven; verdieping 7 groepen; zolder 6 groepen; **berging: aparte 3-groepsverdeler** (≈ 30 groepen totaal) |
| Thermostaten | 2× Honeywell Home DT4 (aan/uit): woonkamer 20 °C, slaapkamer 18,5 °C |
| Ventilatie | Itho Daalderop HRU 400 (WTW, 400 m³/h, rendement 95,5 %) op zolder |
| Regeling LG | Modus Auto/**AI** (= stooklijn), regeling op **Invoer** (retourtemperatuur), stille modus aan |

De bediening (met ingebouwde kamersensor) zit op de toren in de berging en meet daar 21,0 °C.
Dat is geen representatieve plek voor ruimteregeling.

---

## 3. Wat de data laten zien

### 3.1 Pendelen (Gegevensregistratie 11-11, 16:39–19:45)

| Start | Stop | Draaitijd | Pauze daarna | In/Uit bij stop |
|---|---|---|---|---|
| 16:39 | 16:57 | 18 min | 11 min | 22 / 25 °C |
| 17:08 | 17:23 | 15 min | 11 min | 22 / 24 °C |
| 17:34 | 17:47 | 13 min | 12 min | 22 / 22 °C |
| 17:59 | 18:12 | 13 min | 12 min | 22 / 21 °C |
| 18:24 | 18:40 | 16 min | 11 min | 22 / 22 °C |
| 18:51 | 19:09 | 18 min | 11 min | 21 / 19 °C (waarschijnlijk ontdooien) |
| 19:20 | 19:37 | 17 min | 8 min | 22 / 26 °C |

* Cyclus ≈ 27 min → **≈ 2,3 starts per uur**, looptijd ≈ 59 %.
* De pauzes zijn opvallend constant **11–12 minuten**. Dat is precies de huidige
  *Pompinstelling in verwarming*: 1 min overloop + 10 min pomp uit + 1 min meten. Bij de eerste meting
  start de unit direct weer, omdat het water ver onder het (te hoge) doel ligt.
* Bij elke stop is de retour pas **21–22 °C**, ver onder het stooklijndoel van ≈ 34 °C. De stop komt
  dus **niet** uit de eigen waterhysterese, maar van buitenaf: de DT4 of de ruimtesensor van de
  bediening in de berging.

### 3.2 Stooklijn versus werkelijke behoefte

Huidige lijn (op retour): −10 °C → 45 °C, +20 °C → ≈ 19 °C (laatste punt op de foto niet exact
leesbaar). Bij 3 °C buiten is het doel daarmee **≈ 34 °C retour**.

Werkelijk: het huis blijft op 20–21 °C met een retour van **21–22 °C** en een aanvoer van
**24–26 °C**, terwijl de pomp maar 59 % van de tijd draait. Continu draaiend is een retour van ≈ 22–23 °C
dus genoeg. Extrapolatie naar −10 °C geeft ≈ 24 °C retour. Voor een A++-woning met veel
vloerverwarmingsoppervlak is dat heel normaal.

Warmtevraag volgens de warmteafgifte van vandaag: ≈ 40 kWh voor verwarming tot de avond, dus
gemiddeld **≈ 2 kW bij 3 °C buiten**. Doorgetrokken is dat ≈ **3,5–4 kW bij −10 °C**. De 9 kW-unit is
voor dit huis **ruim 2× te groot**. Lang en laag moduleren is daarom extra belangrijk.

### 3.3 Verbruik

| | Warmte | DHW | Totaal |
|---|---|---|---|
| Vandaag (t/m 19:52) | 14,6 kWh | 1,1 kWh | 15,8 kWh |
| November (11 dagen) | 86,4 kWh | 8,9 kWh | 95,4 kWh |
| Dit jaar | 1.879,5 kWh | 524,7 kWh | 2.404,2 kWh |

**Warmteafgifte en COP** (tabblad Warmteafgifte geeft één totaal voor verwarming + warm water):

| | Warmteafgifte | Stroom totaal | **COP totaal** | COP alleen verwarming* |
|---|---|---|---|---|
| Vandaag | 42,6 kWh | 15,8 kWh | **2,7** | ≈ 2,75 |
| November (11 dagen) | 298,9 kWh | 95,4 kWh | **3,1** | ≈ 3,2 |
| Dit jaar | 5.381,8 kWh | 2.404,2 kWh | **2,2** | ≈ 2,2–2,3 |

\* Geschat door voor warm water een COP van 2,0–2,5 aan te nemen.

De dagwaarde is gevoelig voor het tijdstip waarop beide tabbladen zijn gefotografeerd. Het
maandcijfer is het betrouwbaarst.

**Beoordeling:** bij 3–8 °C buiten en een aanvoer van ≈ 25 °C hoort deze unit voor verwarming
een COP van **4–5** te halen. De gemeten 2,7–3,2 ligt daar 30–40 % onder. Het jaargemiddelde van 2,2 is
voor een A++-woning met vloerverwarming zwak. LG berekent de warmteafgifte uit debiet × ΔT en het
verbruik intern. Bij een kleine ΔT van 2–3 K zitten daar meetfouten in, maar een verschil van deze
omvang is daarmee niet te verklaren. De waarschijnlijke oorzaken, in volgorde:

1. **Pendelen.** Elke start kost opstartverlies, en bij 3 °C komt er geregeld een ontdooicyclus bij.
2. **De compressor jaagt elke cyclus een onhaalbaar doel na** (≈ 34 °C retour) en draait daardoor op
   een hoger, minder efficiënt toerental dan nodig.
3. **Vaste verbruikers wegen zwaar bij een kleine warmtevraag.** Denk aan de elektronica en de
   carterverwarming van het buitendeel, en aan de interne pomp. Bij ≈ 40 kWh warmte per dag is
   1–1,5 kWh stand-by al een merkbaar deel.
4. **Mogelijk inzet van het elektrisch element** (verwarming of ontsmetting op 67 °C). Controleer de
   *Verwarmer aan-temperatuur* (§4.2).

Richtwaarden na optimalisatie bij 0–5 °C buiten: verwarming **≥ 4–4,5**, warm water **2,5–3**,
jaargemiddelde **≥ 3,5**.

---

## 4. Aanbevolen instellingen LG (installateursmenu)

Bereiken komen uit de LG-installatiehandleiding van de HN0913T.

### 4.1 Regeling en stooklijn

| Menu | Nu | Advies | Waarom |
|---|---|---|---|
| Configuratie → **Temperatuursensor selecteren** | ? | **Water** | De bediening (en dus de "kamer"-sensor) hangt in de berging. Kamertemperatuur regel je met stooklijn + DT4, niet met deze sensor. |
| Kamerverwarming → **Verwarming temp. instelling** | Invoer | **Invoer laten** | Retourregeling past goed bij een parallel buffer: de retour verandert langzaam, wat helpt tegen pendelen. De stooklijnwaarden hieronder zijn daarom **retourtemperaturen**. |
| Seizoensgeb. auto temp → **Buitentemp.** | −10 / 20 | **−10 / 18** | LG-standaard tweede punt; boven 18 °C is geen warmte nodig. |
| Seizoensgeb. auto temp → **Target temp.** | 45 / ≈19 | **25 / 22** | Zie tabel hieronder; startwaarde, daarna fijnregelen (§7). |
| Hysteresis Verwarmingswater | Aan −2,0 / Uit +2,0 | **Aan −1,0 / Uit +3,0** | Bereik: Aan 0…−9, Uit 0…+4. Een grotere bovenmarge geeft langere runs en de vloer buffert de warmte. Aan klein houden zorgt dat de herstartdrempel boven kamertemperatuur blijft (anders start hij bij zacht weer niet meer). |
| Waterverwarming temp. inst. (bereik) | 15 / 45 | **15 / 35** | Veiligheidsplafond voor vloerverwarming; voorkomt dat een AI-correctie of fout de aanvoer onnodig hoog maakt. |
| AI-correctie (±, op het AI-icoon) | ? | **0** | Na het invoeren van de nieuwe lijn op 0 zetten. Fijnregelen in stappen van ±1 (bereik op de LG: −5 tot +5). Hoofdscherm daarna terug op **AI**, als je tijdelijk de vaste watertemperatuur (§1b) gebruikte. |
| Hysteresis Kamerlucht (verwarming) | −0,5 / +1,5 | laten | Niet meer in gebruik bij sensor = Water. |
| Pompinstelling in verwarming | Tijdsinstelling 1 / 10 | **laten** | De groepspompen houden de vloer in beweging; de LG-pomp hoeft tijdens thermo-uit niet continu door het buffervat te draaien. |
| Stille modus | continu | **schema: alleen 's nachts**, of uit | Beperkt compressor en ventilator; bij vorst kan het element dan bijspringen. |
| Waterdebiet controle | Optimale debiet (28,9 L/min) | **laten** | Pas aanpassen na het inregelen van de secundaire kant (§6). |
| Voorrangsregeling 20 / 10 | Gebruik | **laten** | Is LG's "Forced operation": de pomp draait 10 min na 20 uur stilstand (anti-vastlopen). |
| Pompvoorloop/-overloop | 1 / 1 | laten | |

**Nieuwe stooklijn (retour = Invoer), met de aanvoer die je ongeveer kunt verwachten:**

| Buiten | Doel retour | ≈ Aanvoer | Huidige lijn (retour) |
|---|---|---|---|
| −10 °C | 25,0 °C | 27–28 °C | 45 °C |
| −5 °C | 24,5 °C | 27 °C | 41 °C |
| 0 °C | 23,9 °C | 26 °C | 36 °C |
| 3 °C | 23,6 °C | 26 °C | ≈ 34 °C |
| 5 °C | 23,4 °C | 25–26 °C | ≈ 32 °C |
| 10 °C | 22,9 °C | 25 °C | ≈ 28 °C |
| 15 °C | 22,3 °C | 24 °C | ≈ 23 °C |

### 4.2 Back-up element en energiemeting

| Menu | Nu | Advies |
|---|---|---|
| Verwarmer aan-temperatuur (*Heater On Temperature*) | niet gefotografeerd | **Zo laag mogelijk (bijv. −10 °C of lager).** De 9 kW-unit dekt deze woning ruim; het element hoeft voor verwarming eigenlijk nooit. |
| Energiebewaking → Instelling elektrische verwarming | Extern, 3 kW | **Laten controleren:** de HN0913T heeft een intern 3 kW-element. Klopt deze instelling niet, dan kloppen de energiecijfers (en je COP-berekening) ook niet. |

### 4.3 Warm water (180 L)

| Menu | Nu | Advies | Waarom |
|---|---|---|---|
| DHW-temperatuur (gebruiker) | 48 °C | **48 °C laten** | Met een regendouche (≈ 10–12 L/min) en twee volwassenen is 180 L op 46 °C krap bij twee douchebeurten achter elkaar. De winst haal je met het tijdvenster hieronder. |
| Tank instelling 2 → Hysterese | 3 | **4** (maximum) | Minder korte naverwarmingsbeurten. "Verwarming voorrang" staat bij IWT altijd op DHW. |
| Tank instelling 1 | Min 5 / Comp.limiet 58 | laten | Warmtepomp mag tot 58 °C. |
| DHW tijdsinstelling | 45 / 30 | laten | |
| Gebruik de tankverwarmer | Gebruik, Cyclus, 60 min | laten | Element pas na 60 min warmtepompbedrijf. |
| Tank ontsmetting 1 | Gebruik, vrijdag, 12 uur | **laten** | Midden op de dag = warmste buitenlucht (en eventueel zonnestroom). |
| Tank ontsmetting 2 | 67 °C / 10 min / eind 1 | **60 °C / 10 min / 1** | De warmtepomp doet tot 58 °C; alleen 58 → 60 °C gaat elektrisch in plaats van 58 → 67 °C. Bespaart ≈ 60–90 kWh/jaar. 60 °C blijft de gangbare desinfectietemperatuur; niet uitzetten. |
| DHW-schema | – | **Roosters → DHW** (niet "DHW verwarming"): elke dag **11:00 → 48 °C** en **16:00 → 40 °C** | Opwarmen naar 48 °C gebeurt dan in de middag: eigen zonnestroom (18 panelen), de warmste buitenlucht en meestal de goedkope middaguren van je dynamische tarief. Na het einde van salderen (1-1-2027) scheelt dat direct geld. Buiten het venster staat het doel op 40 °C (de laagste waarde), zodat hij alleen bijwarmt als de boiler echt leeg raakt (onder ≈ 36 °C). Zet het schema 's avonds niet op "uit": dan warmt hij helemaal niet meer bij. |
| Hercirculatietijd | Niet gebruiken | laten | |

### 4.4 Koelen (zomer, optioneel)

De koelinstellingen staan nu op Uitvoer, water 17 °C (max 24) en "Water stop temp. tijdens koel." 18 °C.
Wil je in de zomer vloerkoeling gebruiken, zet het koeldoel dan op **19–20 °C**. Laat de stoptemperatuur
op 18 °C (condensatiebeveiliging) en isoleer de koude leidingen in de berging tegen condens.

---

## 5. Honeywell DT4-thermostaten

De DT4 is een aan/uit-thermostaat met TPI-regeling. Installateursparameters (zie de handleiding van de
bedrade T4/DT4): **2:CR** schakelfrequentie 3/6/9/12 per uur (standaard 6), **3:OT** minimale
aan-tijd 1–5 min.

| Instelling | Woonkamer | Slaapkamer |
|---|---|---|
| 2:CR (cycli per uur) | **3** | **3** |
| 3:OT (minimale aan-tijd) | **5 min** | **5 min** |
| Temperatuur | **21,5–22 °C** (≈ 1,5–2 °C boven de gewenste 20 °C) | zie hieronder |
| Programma / nachtverlaging | **uit** (of hooguit 0,5 °C) | **uit** |

**Waarom de woonkamer-DT4 hoger:** de stooklijn bepaalt voortaan de temperatuur (≈ 20 °C). De DT4 is
alleen nog een **begrenzer** bij zoninstraling of veel interne warmte. Staat hij precies op de gewenste
temperatuur, dan blijft de TPI-regeling rond het setpoint hakken. Dat is precies het pendelen dat we
willen voorkomen. Een nachtverlaging levert bij vloerverwarming in een A++-woning niets op en kost
's ochtends juist een piek met een slechtere COP.

**Slaapkamer-DT4 (18,5 °C): eerst controleren wat hij schakelt** (aansluitkastje bij de pompen):

* **Parallel op de warmtepomp** (beide thermostaten kunnen de LG aanzetten): laat hem op 18,5 °C of zet
  hem lager. Hij hoort vrijwel nooit te vragen; de slaapkamers volgen via de vloer mee.
* **Schakelt hij de groepspomp van boven:** zet hem op 19,5–20 °C als begrenzer en maak de slaapkamers
  koeler door hun groepen op de verdeler terug te regelen (§6). Zo blijft de pomp gewoon draaien.
  Een pomp die steeds stopt, verkleint het afgifte-oppervlak en is juist een pendeloorzaak.
* **Schakelt hij allebei** (de warmtepomp én de pomp van boven, via een relais in het aansluitkastje):
  dan regelt hij de hele bovenverdieping, **inclusief de zolder**, want die hangt aan dezelfde pomp.
  Volgens de simulator werkt dat zonder extra pendelen. Bij 18,5 °C staat de pomp boven ≈ 45–60 % van
  de tijd uit en kost het ≈ 0,5–1 kWh per dag minder dan alles open. De keerzijde: de zolder wordt dan
  ook ≈ 18,5 °C.
  - Zolder als werk- of speelruimte warm houden: zet de slaapkamer-DT4 op **20 °C** en regel alleen de
    slaapkamergroepen op de verdieping terug naar ≈ 50–60 %. De zoldergroepen blijven open.
  - Zolder mag koeler: laat de slaapkamer-DT4 op **18,5 °C** staan. Beneden krijgt in deze opstelling
    iets minder warmte via de trap en het plafond (simulator: ≈ 0,5 °C). Stel de stooklijn daarom een
    halve graad minder ver omlaag bij (bijv. AI −2,5 in plaats van −3). In de simulator: kies
    "Slaapkamer-DT4 schakelt: Allebei" en druk op "Stooklijn afstemmen".

---

## 6. Vloerverwarming en hydrauliek

1. **Berging (3 groepen, aparte verdeler):** de bediening meet daar 21,0 °C. Er staan ook al een boiler
   en buffer die warmte afgeven. Moet de berging niet als woonruimte warm zijn, regel deze 3 groepen
   dan terug of dicht tot ≈ 16–18 °C (minimaal vorstvrij voor de installatie). Besparing hangt af van hoe
   goed de berging geïsoleerd is: ≈ 50–150 kWh/jaar.
2. **Slaapkamers (verdeler verdieping):** wil je daar 18,5 °C, zet die groepen dan op ≈ 50–60 % van het
   debiet van de woonkamergroepen. Zo komen ze vanzelf op temperatuur, zonder thermostaat-geschakel.
3. **Badkamer (groep 1 van de BG-verdeler) en woonkamer/keuken (groepen 5–13):** volledig open.
4. **Zolder (6 groepen):** is in gebruik, dus volledig open laten.
5. **Geen thermische motoren:** op de BG-verdeler zie ik handdoppen; laat alle groepen open. Een
   warmtepomp wil een zo groot mogelijk, constant afgifte-oppervlak.
6. **Groepspompen (OEG CPA-E 25-7.5 PWM, max. 60 W):** de gefotografeerde pomp staat op **HD2**
   (lampjes II + Auto: constante druk, middelste curve). Zet hem op **HD1** (lampjes II + III: laagste
   constante druk) en controleer na een dag of de flowmeters en de kamers nog goed zijn. Zo niet, terug
   naar HD2. Controleer de tweede pomp op dezelfde manier. Hun stroom zit **niet** in de LG-teller. Twee
   pompen die 24/7 draaien op 10–25 W kosten samen ≈ 175–440 kWh per jaar. Zet ze buiten het stookseizoen uit. Optioneel: laat de installateur één pomp
   via de LG aansturen ("Externe pomp gebruiken"), zodat ze vanzelf stoppen als er geen vraag is.
7. **Debietverhouding primair/secundair:** tel de flowmeters van alle verdelers op en vergelijk die
   som met de 28,9 L/min van de LG. Bij een parallel buffer werkt het het best als het primaire debiet
   ongeveer gelijk aan of iets hoger is dan het secundaire. Is het secundair veel hoger, dan wordt de
   aanvoer naar de vloer bijgemengd en moet de LG warmer stoken dan nodig. Dit is een klus voor de
   installateur.

---

## 7. WTW Itho Daalderop HRU 400

Met 95,5 % warmteterugwinning zijn de ventilatieverliezen klein. Belangrijk is vooral dat het huis niet
onnodig veel ventileert en dat de bypass in de winter dicht blijft.

* **Ventilatiestand:** in de winter op de laagste/automatische stand (vocht- of CO₂-sturing), alleen
  hoger bij koken, douchen of veel bezoek.
* **Bypass:** controleer dat de bypass in het stookseizoen dicht blijft. Zet de comfort-/bypass-
  temperatuur op ≥ 23–24 °C, zodat hij op zonnige winterdagen geen warmte naar buiten stuurt.
  Dat stel je in via de Itho-app of door de installateur.
* **Filters:** iedere ≈ 3 maanden schoonmaken, jaarlijks vervangen (of bij filtermelding). Vuile filters
  geven meer ventilatorvermogen en disbalans.
* **Balans:** toevoer en afvoer moeten gelijk zijn (inregelen via de Itho Service-app). Disbalans geeft
  extra infiltratie en dus extra warmtevraag.
* **Vorstbeveiliging:** bij vorst beschermt de unit de warmtewisselaar. Dat is normaal, maar die
  beveiliging hoort boven 0 °C niet actief te zijn.

---

## 7b. Zonnepanelen (18) en dynamisch tarief

* **Warm water in de middag.** Laat de boiler alleen tussen 11:00 en 16:00 opwarmen (§4.3). Dan draait
  het zwaarste deel van de dag (≈ 1–1,5 kWh stroom) op eigen zonnestroom of goedkope middaguren, bij de
  warmste buitenlucht. De ontsmetting op vrijdag 12:00 valt daar al in.
* **Salderen stopt op 1 januari 2027.** Daarna levert elke kWh eigen zonnestroom die je zelf gebruikt
  het verschil op tussen de inkoopprijs en de terugleververgoeding. Het tijdvenster wordt dan meer waard.
* **Verwarming verschuiven heeft weinig zin.** Met de lage stooklijn draait de compressor bijna continu
  op minimumvermogen. De vloer is een grote warmtebuffer, maar extra laden op zonnige middagen verlaagt
  de COP en geeft in november–februari weinig zonnestroom om te benutten. In het voor- en najaar kun je
  op zonnige dagen eventueel AI +1 geven tussen 11 en 16 uur, als het LG-schema dat toestaat.
* **Optioneel, later:** de LG heeft een ingang voor *Energy State* (SG-ready). Met een energiemanager
  die zonne-overschot of lage prijzen meldt, kan de warmtepomp dan zelf het warmwaterdoel verhogen.
  Dat is pas zinvol na 2027 en met een geschikte energiemanager; bespreek het met de installateur.

---

## 8. Verwachte effecten (indicatief)

| Maatregel | Effect |
|---|---|
| Lagere stooklijn + hysterese + DT4 als begrenzer | Van ≈ 50 naar ≈ 10–20 starts per etmaal bij 3 °C; compressor draait laag en lang. Dit is de grootste post: de COP van verwarming moet van ≈ 3 naar ≥ 4. |
| Ontsmetting 67 → 60 °C | ≈ 60–90 kWh/jaar |
| Warm water in het zonvenster 11–16 u + hysterese 4 | Hogere warmwater-COP (simulator: 1,8 → 2,2) en ≈ 2–3 kWh per dag eigen zonnestroom in plaats van netstroom |
| Berging terugregelen | ≈ 50–150 kWh/jaar (afhankelijk van isolatie) |
| Groepspompen lager + 's zomers uit | ≈ 50–200 kWh/jaar (buiten de LG-teller) |
| Stille modus alleen 's nachts | Voorkomt elementgebruik bij vorst; klein maar positief |

**Op basis van de gemeten COP:** dit jaar is tot nu toe 5.382 kWh warmte geleverd voor 2.404 kWh stroom
(COP 2,2). Dezelfde warmte kost bij een jaar-COP van **3,5** ≈ 1.540 kWh en bij **4,0** ≈ 1.345 kWh.
Dat is ≈ **850–1.050 kWh minder** over de eerste 10½ maand. Over een heel jaar komt dat neer op
≈ 1.000 kWh of meer (≈ € 250+ bij € 0,25/kWh). De groepspompen komen daar nog bij, want die zitten niet
in de LG-teller.

**Simulator (geijkt op de meting, zie `docs/simulator.html`):**

| | Huidige instellingen | Advies, stooklijn afgestemd (AI −3) |
|---|---|---|
| Stroom LG per jaar | ≈ 2.700 kWh | ≈ 2.150 kWh (**≈ −560 kWh**) |
| SCOP | ≈ 2,55 | ≈ 3,0 |
| Starts per jaar | ≈ 11.300 | ≈ 350 |
| Bij 3 °C | 64 starts, 17,1 kWh/dag | 1–2 starts, 14,3 kWh/dag |
| Kosten bij 3 °C (voorbeeldtarief € 0,27, 5 kWh zon) | € 4,43 per dag | € 3,45 per dag |

Het model reproduceert de meting goed. Bij 3 °C komt het uit op 64 starts tegen ≈ 54 gemeten, en
pauzes van 11 minuten. Van 1 januari tot en met 11 november rekent het 2.006 kWh stroom en 4.978 kWh
warmte, tegen 2.404 en 5.382 kWh gemeten. Het gemeten warmwaterverbruik (524,7 kWh) past precies bij
≈ 60 L warm water van 40 °C per dag. De ≈ 560 kWh is de voorzichtige schatting, omdat de
onverklaarde verliezen (ijkfactor ≈ 0,8) in alle scenario's gelijk blijven.

De bovengrens van 850–1.050 kWh geldt alleen als de oorzaken uit §3.3 vooral in de regeling zitten. Blijkt een
deel uit stand-byverbruik of meetonnauwkeurigheid te komen, dan is de winst kleiner. De meting na
48 uur (§13) laat zien waar je uitkomt.

---

## 9. Stappenplan en controle

**Stap 1 (nu):** §4.1 (sensor, stooklijn, hysterese, stille modus) en §5 (DT4's).
Wacht daarna 2–3 dagen; vloerverwarming reageert traag.

**Stap 2 (na 1 week):** §4.3 (warm water en ontsmetting) en §4.2 (element, energiemeting).

**Stap 3 (met de installateur):** §6 (berging, slaapkamers, groepspompen, debietverhouding) en
§7 (WTW-balans en bypass).

**Fijnregelen van de stooklijn** (max. één stap per 2–3 dagen):

| Situatie (gemiddeld over een dag) | Actie |
|---|---|
| Woonkamer < 19,7 °C terwijl de DT4 blijft vragen | AI-correctie **+1** (of beide punten +1 °C) |
| Woonkamer > 20,7 °C, of de DT4 schakelt vaak af | AI-correctie **−1** |
| Alleen koud bij vorst, goed bij zacht weer | Alleen het −10 °C-punt +1 à 2 °C |
| Alleen te warm bij zacht weer | Alleen het +18 °C-punt −1 °C (niet lager dan ≈ 21,5 °C: met hysterese Aan −1 moet de herstartdrempel boven kamertemperatuur blijven) |

Is de AI-correctie na een paar weken structureel ±2 of meer, verwerk die dan in de stooklijnpunten en
zet de correctie terug op 0. De simulator verwacht dat bij 3 °C buiten ongeveer **AI −3** nodig is voor
20 °C in de woonkamer. Begin toch met 0 en ga in stappen omlaag; de knop "Stooklijn afstemmen op
20 °C" in de simulator laat zien waar je ongeveer uitkomt. Controleer de lijn opnieuw bij de eerste echte vorst.

**Bijhouden (dagelijks, zelfde tijdstip):**

* Samenvatting → Energie én Warmteafgifte (dag) → **COP per dag** = warmte ÷ energie.
* Gemiddelde buitentemperatuur van die dag. Het KNMI-station Eelde ligt op een paar kilometer, dus
  daarmee kun je kWh per graaddag vergelijken.
* Gegevensregistratie: tel het aantal "Auto"-starts per uur. Doel bij ≤ 5 °C buiten: **≤ 1 start per uur**
  en draaitijden van ruim een uur of langer.

**Jaarlijks onderhoud:** zeef/filter in de binnenunit en het magneetfilter reinigen (te laag debiet
geeft o.a. foutcode CH14). Buitendeel vrijhouden van blad en sneeuw. Bij een geëmailleerde boiler de
anode laten controleren.

---

## 10. Huidige waarden (om terug te kunnen zetten)

| Menu | Waarde vóór wijziging |
|---|---|
| Verwarming temp. instelling | Invoer |
| Seizoensgeb. auto temp – Buitentemp. | −10 / 20 °C |
| Seizoensgeb. auto temp – Target temp. | 45 / ≈19 °C |
| Waterverwarming temp. inst. | 15 / 45 °C |
| Luchtverwarming temp. inst. | 16 / 30 °C |
| Hysteresis Verwarmingswater | −2,0 / +2,0 |
| Hysteresis Kamerlucht (verwarming) | −0,5 / +1,5 |
| Pompinstelling in verwarming | Tijdsinstelling, aan 1 / uit 10 min |
| Waterdebiet controle | Optimale debiet; pompcapaciteit 100 %; vast debiet 26 L/min; vaste ΔT 5 K |
| Pompvoorloop / -overloop | 1 / 1 min |
| Voorrangsregeling (forced operation) | Gebruik, 20 h / 10 min |
| Externe pomp gebruiken / Mengcircuit | Niet gebruiken / Niet gebruiken |
| Gebruik de tankverwarmer | Gebruik, Cyclus, vertraging 60 min |
| DHW temp. inst. (bereik) | 40 / 55 °C; ingesteld 48 °C |
| Tank instelling 1 | Min. temp 5, comp. limiet 58 °C |
| Tank instelling 2 | Hysterese 3, voorrang DHW |
| DHW tijdsinstelling | Actief 45 min, stop 30 min |
| Tank ontsmetting 1 / 2 | Gebruik, vrijdag 12 uur / 67 °C, 10 min, eindtijd 1 |
| Hercirculatietijd | Niet gebruiken (10/20) |
| Energiebewaking | Gebruik; elektrische verwarming Extern 3 kW |
| Antivriesoptie 1 | Type1 |
| Vloerdroging | Uit |
| Koeling | Uitvoer; water 17 (max 24); lucht 16 (max 30); stop 18 °C; hysterese ±0,5; pomp doorlopend |

---

## 11. Nog te controleren / aan te leveren

* ~~Tabblad Warmteafgifte~~ ontvangen: COP verwerkt in §3.3.
* Waarde van **Temperatuursensor selecteren** en **Verwarmer aan-temperatuur**. Die laatste is nu
  belangrijker, gezien de lage jaar-COP.
* De **AI-correctie** die nu op het AI-icoon staat.
* **Bedrading van de DT4's:** wat schakelt welke thermostaat (LG-ingang en/of groepspomp)?
* **Type en stand van de twee groepspompen**, en de **flowmeterstanden** per verdeler.
* Is de **berging** binnen de geïsoleerde schil, en moet die warm zijn?

De optimale instellingen hangen **niet** af van deze punten. In de instelkaart (§12) staat bij elk punt
de waarde die in alle gevallen goed is. De gegevens zijn alleen nodig om het resultaat te controleren (§13).

---

## 12. Instelkaart: alles in één keer invoeren (± 20 minuten)

**Installateursmenu openen (LG):** op het hoofdscherm naar het menu-icoon (4 vakjes) → OK →
naar **Instellingen** (tandwiel). Rechtsonder staat de softwareversie: dat is de code. Houd **▲ 5 seconden**
ingedrukt en voer die code in. Wijzigen met ◀ ▶ / ▲ ▼ en bevestigen met **OK**.

Vink af wat je gedaan hebt:

**A. Kamerverwarming / Configuratie**

- [ ] Configuratie → *Temperatuursensor selecteren* → **Water** (welke waarde er nu ook staat)
- [ ] Kamerverwarming → *Verwarming temp. instelling* → **Invoer** laten staan
- [ ] Kamerverwarming → *Waterverwarming temp. inst.* → **15 / 35**
- [ ] Kamerverwarming → *Hysteresis Verwarmingswater* → **Aan −1,0 / Uit 3,0**
- [ ] Kamerverwarming → *Verwarmer aan-temperatuur* → **laagst mogelijke buitentemperatuur** (welke waarde er nu ook staat)
- [ ] Kamerverwarming → *Pompinstelling in verwarming* → Tijdsinstelling **1 / 10** laten staan

**B. Seizoensgebonden auto temp (stooklijn)**

- [ ] Mode **Warmte** → *Buitentemp.* → punt 1 **−10**, punt 2 **18**
- [ ] *Target Temp.* → punt 1 **25**, punt 2 **22**
- [ ] Menu verlaten. Op het hoofdscherm het **AI**-icoon selecteren → correctie op **0**

**C. Warm water**

- [ ] *Tank ontsmettingsinstelling 2* → **60** / 10 / 1
- [ ] *Tank instelling 2* → hysterese **4**
- [ ] Hoofdscherm, douche-icoon → **48 °C** laten staan
- [ ] Roosters en bewerken → **DHW** (niet "DHW verwarming"): elke dag **11:00 → 48 °C** en **16:00 → 40 °C**
- [ ] Roosters en bewerken → **DHW verwarming**: leeg laten (dit is het elektrische element)

**D. Gebruikersmenu**

- [ ] Stille modus **uit**, of alleen via schema van bijv. 23:00 tot 07:00

**E. Honeywell DT4 (beide)**

Geavanceerd menu: houd de twee knoppen uit de DT4-handleiding (hoofdstuk *Configure the System*)
± 3 seconden samen ingedrukt tot het display verandert. Blader naar de parameter, wijzig hem, sla op en
verlaat het menu.

- [ ] **2:CR → 3** (beide thermostaten)
- [ ] **3:OT → 5** (beide thermostaten)
- [ ] Tijdprogramma: alle perioden **dezelfde temperatuur** (geen nachtverlaging)
- [ ] Woonkamer: **21,5 °C**
- [ ] Slaapkamer: eerst de test hieronder doen, dan instellen

**Test: wat schakelt de slaapkamerthermostaat?** Zet de woonkamer-DT4 even op 5 °C en de
slaapkamer-DT4 op 25 °C en wacht 5 minuten.

* Gaat de warmtepomp aan (op de LG staat "Thermostaat" en de unit start)? Dan zit hij **parallel op
  de LG**. Zet de slaapkamer-DT4 op **18,5 °C**.
* Gaat alleen de bovenste groepspomp aan of uit, en de LG niet? Dan **schakelt hij de pomp van boven**.
  Zet de slaapkamer-DT4 op **20 °C** en regel de slaapkamergroepen terug (§6, punt 2).
* Start de warmtepomp **én** gaat de pomp van boven aan (en bij 15 °C weer uit)? Dan schakelt hij
  **allebei**. Kies dan tussen 20 °C (zolder warm) en 18,5 °C (zolder koeler), zie §5.

Zet daarna de woonkamer-DT4 terug op 21,5 °C.

**F. Met de installateur (hoeft niet op dag 1)**

- [ ] Berging: 3 groepen terugregelen naar ± 16–18 °C (als de ruimte niet warm hoeft)
- [ ] Slaapkamergroepen ± 50–60 % van het debiet van de woonkamergroepen
- [ ] Groepspompen (OEG): knop indrukken tot de lampjes **II + III** branden (= HD1); na een dag de kamers en flowmeters controleren. Buiten het stookseizoen uit
- [ ] Energiebewaking → elektrische verwarming afstemmen op het interne 3 kW-element
- [ ] WTW: bypassdrempel ≥ 23–24 °C, filters, luchtbalans

---

## 13. Controle: is het geoptimaliseerd?

Laat de nieuwe instellingen **48 uur** ongemoeid. Controleer daarna dit:

| Criterium | Waar aflezen | Doel | Zo niet |
|---|---|---|---|
| Starts per uur (bij ≤ 5 °C buiten) | Gegevensregistratie: tel de "Auto"-regels per uur (3 regels met dezelfde tijd = 1 start) | **≤ 1**, met draaitijden van ≥ 60 min | Hysterese Uit → **4,0**. Daarna controleren of de woonkamer-DT4 tussentijds afschakelt. |
| Woonkamertemperatuur | DT4 woonkamer | **20,0 ± 0,5 °C**, en de DT4 vraagt vrijwel continu | Te koud: AI **+1**. Te warm: AI **−1**. |
| Slaapkamers | thermometer/DT4 | **18,5–19 °C** | Groepen op de verdeler bijregelen |
| COP (dag) | Samenvatting: Warmteafgifte ÷ Energie (Totaal), beide tabbladen **direct na elkaar** fotograferen | **≥ 4** bij 0–5 °C buiten (nulmeting: 2,7 vandaag, 3,1 november) | Stuur de cijfers op; dan zoeken we verder (debiet, buffer, ontdooien, stand-by) |
| COP warm water (week) | idem, kolom DHW | **≥ 2,5** | Meestal ligt het dan aan de ontsmetting of het element |
| Element | Energie, kolom Warmte, op een dag boven 0 °C | geen sprongen van ≥ 3 kWh in een uur | *Verwarmer aan-temperatuur* controleren |

**Om de optimalisatie af te ronden:** maak na 48 uur een foto van de Samenvatting (**Energie** en
**Warmteafgifte**) en van twee schermen Gegevensregistratie. Noteer ook de gemiddelde buitentemperatuur.
Dan kan ik de COP berekenen en de stooklijn in één keer definitief maken.

---

### Bronnen

* LG Therma V HN0913T installatiehandleiding (installateursinstellingen p. 110–173):
  <https://www.manualslib.com/manual/3289782/Lg-Therma-V-Hn0913t.html>
* LG Therma V weersafhankelijke regeling / AI (communityhandleiding, o.a. hysterese ±4 tegen pendelen,
  stille modus, thermostaat als begrenzer):
  <https://community.openenergymonitor.org/uploads/short-url/tEjZHjhjWscXnJqqde5e0p5AVwc.pdf>
* Honeywell Home T4 (bedraad) installatiehandleiding, parameters CR/OT:
  <https://www.tlc-direct.co.uk/Technical/DataSheets/Honeywell_Lyric/Honewell%20T4%20wired%20Installation%20Guide.pdf>
* Itho Daalderop HRU 400 productinformatie:
  <https://ithodaalderop.compano.com/Data/Environments/000001/Attachment/Bijlage/19_0201%20HRU%20400%20introductie%20Leaflet_WEB.pdf>
