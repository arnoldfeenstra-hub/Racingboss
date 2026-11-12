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
| 1 | Stooklijn (Seizoensgeb. auto temp, op *Invoer*) | −10 °C → 45 °C / +20 °C → ≈19 °C | **−10 °C → 25 °C / +10 °C → 21 °C** |
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

**Stel deze vaste watertemperatuur in, afhankelijk van het weer** (gemiddelde buitentemperatuur van de
komende dag(en), bijv. van de weerapp voor Eelde):

| Buitentemperatuur | Woonkamer **20 °C** | Woonkamer **21 °C** |
|---|---|---|
| boven 2 °C | **22 °C** | **23 °C** |
| −1 tot 2 °C | 23 °C | 24 °C |
| −4 tot −1 °C | 24 °C | 25 °C |
| −7 tot −4 °C | 24–25 °C | 26 °C |
| kouder dan −7 °C | 25 °C | 27 °C |
| **Woonkamer-DT4** (bovengrens) | **20,5 °C** | **21,5 °C** |

Verder: slaapkamer-DT4 op wat je daar wilt (nu 18,5 °C), geen nachtverlaging, stille modus uit, warm
water via Roosters → DHW (11:00 → 48 °C, 16:00 → 40 °C), groepspompen op HD1 en eventueel de berging
teruggeregeld (§6). De DT4-parameters (2:CR, 3:OT) hoeven dan niet te veranderen: omdat de DT4 een
halve graad boven het doel staat, schakelt hij vrijwel nooit. Staat hij er precies op (bijv. 21,0 °C bij
een doel van 21), dan gaat hij weer schakelen en pendelt de warmtepomp: bij 3 °C ≈ 24 starts per dag
in plaats van 0–1.

**Weer in Eelderwolde** (Open-Meteo, uurwaarden): 11-11 gemiddeld **3,0 °C** (0,4–5,0) met **94 %**
luchtvochtigheid; 12-11 gemiddeld **5,2 °C** (−0,3–9,0) met **82 %**. Verwachting 13–19 november:
gemiddeld 4,5–8 °C, 80–92 %. Voor 21 °C is de komende week dus **23 °C** water de juiste stand; ga naar
24 °C als het een dag rond het vriespunt blijft.

**25 °C, zoals nu ingesteld, is te hoog.** Bij 2–3 °C buiten gebruikt het huis maar ≈ 22 °C retour. Bij
25 °C haalt de warmtepomp zijn doel nooit en blijft de DT4 hem uitzetten: volgens de simulator nog
steeds ≈ 60 starts per dag. Bij 22 °C draait hij vrijwel continu.

| Simulator (bijgewerkt 12-11: echt weer, DT4's op fabrieksinstelling) | Stroom LG per jaar | SCOP | Starts per jaar | Woonkamer in de winter |
|---|---|---|---|---|
| Oud (AI, stooklijn 45/19), DT4 20 °C | ≈ 3.080 kWh | 2,6 | ≈ 10.700 | 20,0 °C |
| Oud, DT4 21 °C | ≈ 3.290 kWh | 2,6 | ≈ 10.500 | 21,0 °C |
| **Vast volgens de tabel, 20 °C** | **≈ 2.650 kWh** | **2,95** | **≈ 800** | **20,1 °C** |
| **Vast volgens de tabel, 21 °C** | **≈ 2.840 kWh** | **2,9** | **≈ 900** | **21,1 °C** |
| Installateur (−10/10 → 25/21), 20 °C | ≈ 2.710 kWh | 3,0 | ≈ 1.000 | 20,9 °C |
| Installateur, 21 °C (AI +1, DT4 22) | ≈ 2.870 kWh | 2,95 | ≈ 1.200 | 21,7 °C |

21 °C kost met de tabel ≈ 190 kWh per jaar (≈ 7 %) meer dan 20 °C, maar ≈ 450 kWh minder dan 21 °C met de
oude instellingen. Bij het weer van deze week (5,5 °C, 86 %): oud bij 21 °C 16,1 kWh per dag, COP 2,8,
46 starts; met de tabel 13,9 kWh per dag, COP 3,2, 4 starts. De stooklijn van de installateur levert
ongeveer hetzelfde op; het verschil is dat die zich vanzelf aan het weer aanpast. Het nadeel van zelf doen: bij omslaand weer
moet je de waarde zelf bijstellen. Doe je dat niet, dan wordt het bij vorst kouder in huis (bij 22 °C en
−5 °C buiten ≈ 18,5 °C) en bij zacht weer begrenst de DT4. De stooklijn van de installateur doet dat
automatisch en blijft daarom de beste eindoplossing.

### Meting 12-11: eerste dag met vaste watertemperatuur

Ingesteld: vast **23 °C**, woonkamer-DT4 **20,5 °C**, groepspompen op **HD1**, warm water vanaf 11:00.

| 00:00–19:50 | 11-11 (oud) | 12-11 (nieuw) | Verschil |
|---|---|---|---|
| Stroom | 15,8 kWh | 12,5 kWh | **−21 %** |
| Warmte | 42,6 kWh | 39,4 kWh | −8 % |
| **COP** | **2,70** | **3,15** | **+17 %** |
| Starts | ≈ 2,3 per uur | ≈ 0,5 per uur (10:30–19:44: 5 starts) | |
| Draaitijden | 13–18 min | 34, 3, 109 en 10 min | |

Van de 3,3 kWh minder stroom komt ≈ 2,1 kWh door de hogere COP en ≈ 1,2 kWh door iets minder
warmte. De simulator voorspelde voor deze instellingen bij 3 °C een COP van 3,0 en 15 kWh per dag,
dus dat klopt goed. Het warmwatervenster werkt: om 10:30 was de boiler 43 °C en werd hij pas na 11:00
bijgewarmd. Om 18:35 warmde hij opnieuw bij van 41 naar 48 °C, omdat het doel na 16:00 nog op 48 °C
stond (de regel 16:00 → 40 °C ontbreekt nog).

**Weer meegerekend:** 12-11 was warmer en droger (5,2 °C en 82 % tegen 3,0 °C en 94 %). Volgens de
simulator gaf het weer alleen al de oude instellingen een COP van ≈ 2,8 in plaats van 2,7. De rest van de
stijging, naar 3,15, komt van de nieuwe instellingen. Met de nieuwe instellingen op het weer van 11-11
zou de COP ≈ 3,0 zijn geweest.

**Wat het logboek nog laat zien:** de stops om 11:04 en 15:24 gebeurden met *Uit* 28 °C en *In* 22–23 °C,
door de woonkamer-DT4. De watertemperatuur van 23 °C is dus nog iets hoog: het huis wordt 20,5 °C en
dan zet de DT4 de warmtepomp én de pomp beneden uit. Met **22 °C** (zolang het boven 2 °C is) draait hij
langer en lager (simulator: COP 3,05 → 3,1, ≈ 1 kWh per dag minder, woonkamer ≈ 19,8–20 °C).

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
| Seizoensgeb. auto temp → **Buitentemp.** | −10 / 20 | **−10 / 10** | Boven 10 °C blijft het doel 21 °C; meer is niet nodig. |
| Seizoensgeb. auto temp → **Target temp.** | 45 / ≈19 | **25 / 21** | Zie tabel hieronder. Afgeleid van de meting van 12-11 (23 °C vast bij ≈ 3 °C was net te warm) en de simulator; daarna fijnregelen (§9). |
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
| −5 °C | 24,0 °C | 26–27 °C | 41 °C |
| 0 °C | 23,0 °C | 25–26 °C | 36 °C |
| 3 °C | 22,4 °C | 24–25 °C | ≈ 34 °C |
| 5 °C | 22,0 °C | 24 °C | ≈ 32 °C |
| 10 °C en warmer | 21,0 °C | 23 °C | ≈ 28 °C |

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

> **Bevestigd op 12-11:** beide DT4's schakelen hun groepspomp (woonkamer → pomp beneden, slaapkamer →
> pomp boven). Het logboek ("Oper. Off" als de DT4 uitschakelt) laat zien dat ze via het relais ook de
> warmtepomp aan- en uitzetten. Zet de woonkamer-DT4 daarom als bovengrens (20,5–21 °C) en laat de
> watertemperatuur het werk doen; elke keer dat de DT4 uitschakelt, stopt ook de vloer beneden.

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
    halve graad hoger af (bijv. AI +0,5). In de simulator: kies
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

| Woonkamer 20 °C | Oude instellingen | Vast met het weer mee (zelf) | Advies installateur (−10/10 → 25/21) |
|---|---|---|---|
| Stroom LG per jaar | ≈ 3.080 kWh | ≈ 2.650 kWh (**≈ −430**) | ≈ 2.710 kWh |
| SCOP | ≈ 2,6 | ≈ 2,95 | ≈ 3,0 |
| Starts per jaar | ≈ 10.700 | ≈ 800 | ≈ 1.000 |

Voor 21 °C: zie de tabel in §1b. Het model is geijkt op twee dagen met het echte weer van
Eelderwolde: 11-11 (3,0 °C, RV 94 %; COP 2,7, ≈ 54 starts, pauzes van 11 minuten; model 48 starts en
14 min) en 12-11 (5,0 °C, RV 84 %; gemeten COP 3,15, model 3,14). Daarvoor moest de warmtevraag
omhoog: de dagwaarden liepen tot ≈ 19:50, over een hele dag is het ≈ 51 kWh (11-11) en ≈ 46 kWh (12-11).
Van 1 januari tot en met 11 november rekent het model nu 2.287 kWh stroom en 5.755 kWh warmte, tegen
2.404 en 5.382 kWh gemeten. Het gemeten
warmwaterverbruik (524,7 kWh) past bij ≈ 60 L warm water van 40 °C per dag.

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
| Alleen te warm bij zacht weer | Alleen het +10 °C-punt −0,5 à 1 °C (niet lager dan ≈ 20,5 °C: met hysterese Aan −1 moet de herstartdrempel rond kamertemperatuur blijven) |

Is de AI-correctie na een paar weken structureel ±2 of meer, verwerk die dan in de stooklijnpunten en
zet de correctie terug op 0. Met de stooklijn −10/10 → 25/21 verwacht de simulator dat AI 0 tot −1
nodig is voor 20 °C in de woonkamer. De knop "Afstemmen op 20 °C" in de simulator laat zien waar je
ongeveer uitkomt. Controleer de lijn opnieuw bij de eerste echte vorst.

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

- [ ] Mode **Warmte** → *Buitentemp.* → punt 1 **−10**, punt 2 **10**
- [ ] *Target Temp.* → punt 1 **25**, punt 2 **21**
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
