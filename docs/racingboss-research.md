# Racing Boss: how the game works

*Research compiled 13 October 2026, from www.racingboss.com (public pages and public statistics) and third-party listings.*

Every statement is tagged with where it comes from:

- **[Rules]**: the official rulebook (`rules.php`) or other official pages.
- **[Observed]**: public statistics pages, the Info Center news feed, or the site's HTML/JS, read while Season 84 was in progress.
- **[Inferred]**: my own reasoning from the above. Treat these as hypotheses to test, not facts.

Without an account I could not see the office, garage, practice or race-log pages, so the per-lap simulation formulas are not visible. Section 10 pulls together everything the public material reveals about them.

---

## 1. What the game is

Racing Boss is a free, browser-based **Formula 1-style team-management game**. You are the team principal, not the driver. You:

- sign suppliers (engine, gearbox, tyres, chassis),
- design and build the car,
- hire a driver, a designer, a commerce director, mechanics and design crew,
- negotiate sponsors,
- run practice to find the car setup and the driver's point distribution,
- submit qualifying and race orders (fuel, tyres, pit laps, boost laps, risk levels, engine and gearbox tuning).

The server then **simulates qualifying and the race automatically**, and you can watch it in a live viewer with chat. [Rules / home page]

Basic facts:

- **Schedule:** two races a week. [Rules]
- **Setting:** a persistent multiplayer world with a promotion/relegation pyramid, plus player-created private leagues. [Rules]
- **Price:** free to play. Optional "Supporter credits" pay for cosmetics, extra statistics and private leagues (section 12). [Observed]
- **Operator:** footer reads "© 2001 – 2026 RACINGBOSS.COM | wwSims". Contact: `info (at) racingboss (dot) com`. A legacy address, `f1time@f1time.com`, still appears on the supporter page. [Observed]
- **Languages:** 16 UI languages: English, Lithuanian, French, Dutch, Romanian, Portuguese (BR and PT), Italian, Estonian, Polish, German, Spanish, Greek, Finnish, Hungarian. [Observed]

## 2. History

| Date | Event | Source |
|---|---|---|
| Sep 2001 | Work starts on the game, then called **F1TIME** (f1time.com) | [Rules – About] |
| 1 Apr 2002 | First official race (v1) | [About] |
| Apr 2002 – Aug 2005 | 24 seasons played, then a full stop "with a promise of redesign" | [About] |
| 4 Mar 2007 | First race of **v2.0** | [About] |
| 2012 | Major rework, re-released as **v3** | [About] |
| 2014 | Renamed **Racing Boss** | [About] |
| Season 82 (Feb 2026) | "Winter delayed" season start. Planned updates postponed | [Observed – news] |
| 29 Sep 2026 | Race postponed 24 h after a server outage. A move to new server hardware is planned "later this year" | [Observed – news] |
| 13 Oct 2026 | Season 84, Race 17 (Miami) run. The home page shows "Game is undergoing maintenance" | [Observed] |

The team is small and led by one developer from Lithuania, now in Ottawa, Canada, who calls himself "Developer, Manager, all in one". He is supported by a GameMaster, two community managers, a visual designer, a game-concept designer, a content contributor (who writes the race-report "magazine" posts) and a moderator. [About]

Season numbering is continuous from 2002. The Hall of Fame lists champions for seasons 1–24 and 26–83; **season 25 has no entry**. [Observed] *[Inferred]* Season 25 was probably the interrupted or relaunch season around the 2005–2007 gap.

**Points history (Hall of Fame).** Up to season 40, winning totals were about 73–140 points, which fits the old 10-8-6-5-4-3-2-1 system. From season 41 they are 279–500, which fits the modern 25-18-15… system. *[Inferred]* Season 41 is most likely the v3 relaunch (2012). The best season on record is 500 points from 20 wins in 20 races (season 74), which confirms that **a modern season has 20 races**.

**Stars after manager names** (`Alex Lesga**`, `Joakim Sjöblom**********`) count **Class 1 championships**. This checks out exactly against the Hall of Fame: Sjöblom has 10 titles and 10 stars, van Rijn 8 and 8, Sudalenko 4 and 4 (the Season 82 news post also calls his latest title his "4th championship"). [Observed / Inferred]

## 3. World structure

### 3.1 Public leagues: the pyramid [Rules]

| Class | Groups | Managers per group |
|---|---|---|
| C1 | 1 | up to 30 |
| C2 | 2 | up to 30 |
| C3 | 4 | up to 30 |
| C4 | 8 | up to 30 |
| C5 | 16 | up to 30 |
| C6 | 32 | up to 30 |

- Each class has twice as many groups as the class above it.
- **Newcomers start in the lowest active class.** The rules currently name C4 and say "C3 right now" for the second-lowest class, so the active depth changes with the player population.
- **Promotion:** the top 4 of each group go up (except in C1).
- **Relegation:** 23rd and lower go down (the "bottom 8" of a full 30-manager group).
- **Filling empty spots:** if the second-lowest class has empty places, extra managers are promoted from the lowest class, so you can go up from 5th or lower.
- Vacancies left in the top 22 of C1–C4 by players who quit stay **empty**, so nobody is promoted unexpectedly.

**Live state, Season 84** [Observed – statistics.php]:

| League | Active managers |
|---|---|
| Class 1 | 23 |
| Class 2 – Group 1 | 5 |
| Class 2 – Group 2 | 4 |
| Class 3 – Group 2 | 5–7 (new accounts land here: default driver at 140 DRP, default sponsor) |
| C5 and C6 groups | listed, but empty this season |

The countries page lists about 114 managers from 37 countries: USA 16, Brazil 11, Italy 8, France 8, UK 7, Lithuania 6, Netherlands 6, and others.

*[Inferred]* The active community is about 40 managers in public leagues. Most competition is concentrated in C1, and the lower groups are thin.

### 3.2 Private leagues [Rules / Observed]

- Created by players, with custom settings.
- Cost "a few credits per race".
- Examples: "A Race A Day", "Lister Cup", "VW Beetle Fun Cup", "F1 1990", "Speed Group 1 (20 races)", "The Ultimate Group".
- Some private leagues use **fantasy or extra tracks** that public leagues do not, such as Vilnius (44 s lap), California Speedway (26 s), Old Nürburgring (6:19 lap) and Cancún.

### 3.3 Season rhythm [Rules / Observed]

- **20 races per season**, two per week, so a season lasts about 10 weeks of racing.
- In the current season, race times are shown as e.g. `2026-10-13 18:00:00`.
- Pages that run in parallel through the season: the **Cup** (a knockout), the **Team championship** and the **drivers'/managers' championship**.
- Between seasons the offices close for the **season reset** (section 11).

## 4. Points and the economy

### 4.1 Championship points [Rules]

| Position | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
|---|---|---|---|---|---|---|---|---|---|---|
| Points | 25 | 18 | 15 | 12 | 10 | 8 | 6 | 4 | 2 | 1 |

There are no points for pole position or fastest lap. Poles and fastest laps are still tracked in the statistics.

### 4.2 Income [Rules]

**Fixed race income** is paid for starting each race:

| Class | Per race |
|---|---|
| C1 | $3,000,000 |
| C2 | $2,750,000 |
| C3 | $2,500,000 |
| C4 | $2,250,000 |
| C5 | $2,000,000 |
| C6 | $1,750,000 |

**Race prize money** is the same table in every class:

- P1 gets $3.0M and P2 gets $2.8M.
- After that, each place gets $100k less: P3 $2.7M, P10 $2.0M, P20 $1.0M, P29 $0.1M, P30 $0.
- **Qualifying pays nothing**, which pushes managers to race through the field.

**Championship bonus** at season end:

- C1 champion gets $10M. Each class below pays the champion $1M less (C6 champion: $5M).
- Each place is worth $0.5M less than the one above.
- Places up to 15th are paid in C1. In the lower classes the payouts reach zero sooner.

**Cup bonus:** $500k per cup round won in C1, and $50k less per class below (C4: $350k). The rules say there are 6 rounds.

**Team bonus** is a prize pot per group:

| Class | Pot |
|---|---|
| C1 | $30M |
| C2 | $27M |
| C3 | $24M |
| C4 | $21M |
| C5 | $18M |
| C6 | $15M |

- The pot is split among two-manager teams in proportion to the points they scored.
- Each team member gets **half** of the team's share.
- [Observed] Check against the C1 data: team "Rusteze Entente Cordiale" has 430 of the 1,626 team points scored, and 430/1,626 × $30M = $7.93M, exactly as shown.

**Sponsors** pay a fixed amount per race, plus a bonus if the season goal is met (section 7.3).

### 4.3 Costs [Rules / Observed]

Ongoing costs:

- **Staff salaries.** Observed driver contracts are about $0.4M–$2.5M, shown next to contract length in races.
- **Supplier contracts**, charged after every race and fixed for the whole season.
- **Car parts** in the garage. Higher levels and specialised speed or handling parts cost more.
- **Testing sessions**, mechanic training and design crew.

**Season-end tax** (applied *before* the bonuses are paid):

- Holdings up to $30M are untaxed.
- Above that, the rate is **30%**.

### 4.4 Negative balance [Rules]

While your balance is below zero you:

- may only use the lowest part level allowed in your league,
- cannot train mechanics,
- cannot hire the two top grades of mechanics or designers, and the ones you have **leave at season end** if you are still negative then,
- cannot bid more than **$750,000** in staff markets,
- cannot book testing.

You **can** still extend your driver's contract and hire low-level engineering or mechanic staff.

**RB.I.A financial assistance:** if you end the season negative *after* the winnings are paid, the debt is cleared and you start at $0. It never has to be repaid, but **you lose 1 point of pit-stop skill for every $1M of assistance.**

### 4.5 What the money looks like in practice [Observed – C1 "Balance" stats, Season 84]

| Manager rank by balance | Car level | Sponsors | Title-sponsor goal | Balance |
|---|---|---|---|---|
| 1 | 3 | 12.45M | Win 10 races in a season | $258.9M |
| 2 | 7 | 11.71M | Top 5 in season | $211.6M |
| 6 (title contender) | 8 | 10.91M | Top 5 | $84.8M |
| 18 (championship leader) | 7 | 11.72M | Top 10 | $10.8M |

- In C1, sponsor income is about **$9.7M–12.5M** (*[Inferred]* per race, given the scale of the fixed race income).
- In C3 every newcomer's sponsor pays **$4.81M** (default deal **$3.85M**).
- The season leader holds only $10.8M while back-markers have hoarded over $200M.

*[Inferred]* Money is not the binding constraint at the top. Spending (car level, staff) matters more than saving, and the 30% tax above $30M punishes hoarding. Very rich managers with a low car level are probably "banking" rather than competing.

## 5. The car

### 5.1 Design ratings [Rules]

**Reliability** is the chance of a mechanical failure in the race.

**Weight:**

- Heavier means slower.
- The **minimum weight is 600 kg**. Lighter cars carry ballast up to 600 kg.
- Only the driver, car parts and supplier parts count toward the minimum. **Fuel does not.** *[Inferred]* So below 600 kg extra lightness is wasted, while fuel weight always slows the car.

**Speed** is the sum of speed points from technologies and from the parts you choose.

**Handling** is the same, for handling points.

**Efficiency** is speed plus handling.

### 5.2 R&D points and how to spend them [Rules]

- **Earning:** after every race you earn R&D points from your **designer's Innovation** skill and your **design crew**. Testing earns more (section 5.5).
- **Saving:** points can be saved across races but **are lost at season end**.
- **Technologies:** an instant speed or handling boost, valid **for the current season only**. The "rules change" each season, so technologies reset to zero. Higher designer skill lowers the R&D cost of some technologies.
- **Supplier-part development:** invest in the engine, gearbox, tyres or chassis (section 5.4).

### 5.3 The garage: building for each track [Rules]

- **Ten part levels.** Low classes cannot use the top levels, and C1 cannot use the bottom ones.
- Better parts give more speed and handling but cost more.
- **Specialised parts** (with an uneven speed-to-handling ratio) cost more again.
- Every track has a **speed rating and a handling rating**. The car performs best when its own speed/handling profile is close to the track's. Your driver's own Speed and Handling ratings also show how well they use their DRP at a given track's speed/handling ratio.

*[Inferred]* Each race is a small optimisation problem: buy a part mix whose speed/handling ratio matches the track, at the cheapest cost that still delivers.

### 5.4 Suppliers [Rules]

At the start of each season you sign one supplier for each of the 4 components, chosen from those offered in your league. The contract runs **for the whole season, cannot be broken, and is charged after every race**. Supplier upgrades **do not carry over** to the next season.

| Component | Attributes |
|---|---|
| Engine | Power (hp), Weight (kg), Fuel consumption (higher = thirstier), Reliability % |
| Gearbox | Shift delay (ms with no drive while changing gear; lower is better), Weight, Reliability % |
| Tyres | Optimal temperature (grip drops away from it), Wear % (relative: 80% wear lasts 20% longer than 100%), Performance % (100% fastest; 98% is 2% slower, i.e. 2 s on a 1:40 lap) |
| Chassis | Weight, Reliability % |

**Development model:**

- Each part has a **"Current" spec**, which is fitted to the car, and a **"Development" spec**, which improves as you invest R&D.
- To use the improvements you must **"Upgrade to 1.X revision"**.
- **R&D rating** sets how fast a part improves for each point invested.
- **Revisions** caps how many upgrades you can make in a season.

**Supplier brands** are parody names (the TOS says the trademarks are illustrative and the stats are not real). Brands seen in use in Season 84 [Observed]:

| Class | Engines | Gearboxes | Tyres | Chassis |
|---|---|---|---|---|
| C1 | Asiateks, Ferarossa, BNV, Homda | Lemoën, Soda GB, Yamahaha | Sumo Tires, Yokohono, Goodstone | Acuri, Shevrolex, Panda |
| C2 | Peugaux, Mersedes, Homda, Aodi | Stracks, Volol, Hewland | Pipirelli, Blackrocks | Izuki, Jeeper, Nossan |
| C3 | Volksmobile | Lamboroni, MiniMaxi | Kontirenal, Hamook, Doneloop | Mizubi, Mazduka |

What the Season 83 race reports say about the C1 trade-offs [Observed – news]:

- The **Ferarossa** engine is the most powerful but has only **76% reliability**.
- **Homda** has less power, better fuel economy and more stability over a race.
- **Yokohono** tyres are very fast but wear quickly.
- **Goodstone** tyres are slower but durable.

In Season 84, Asiateks is the most common C1 engine (14 of 23 cars).

### 5.5 Testing [Rules]

| Type | Max days | What else it gives |
|---|---|---|
| Track | 5 | Car R&D, plus training **1 driver skill** |
| Wind tunnel | 3 | Car R&D (scale model) |
| Simulator | 2 | Virtual R&D, plus training **3 driver skills** |

- Testing earns extra R&D points.
- It is blocked while your balance is negative.
- It is allowed at the end of the season, but the points are wasted because R&D, technologies and supplier development all reset.

### 5.6 Liveries [Rules]

A large catalogue of liveries (current, historic, fantasy and national) is purely cosmetic. Statistics track "Most popular liveries".

## 6. Staff

### 6.1 Driver [Rules]

A driver's skills add up to **DRP (Driver Racing Points)**. More DRP means a faster driver.

The rules list the primary skills as: Concentration, Speed, Racing, Stamina, Experience, Reporting, Confidence. The rules say "six stats" but list seven; Speed is listed among them but not described.

| Skill | Extra effect |
|---|---|
| Concentration | Fewer and less severe mistakes |
| Racing | Overtaking and blocking |
| Stamina | Helps blocking |
| Experience | Builds up over a career |
| Reporting | Better practice feedback (chance of setup arrows) |
| Confidence | Goes up or down with how the driver feels: a high in-race DRP % and finishing at or above the expected position |

**Secondary skills**, used only in specific situations:

- **Starting:** affects race starts.
- **Pole:** affects qualifying.
- **Talent:** overtaking and blocking.
- **Speed rating and Handling rating:** how well the driver uses their DRP at a track with a given speed/handling ratio.
- **Weight:** the driver's weight counts toward the car weight.
- **Age.**
- **Favourite track:** the driver is slightly faster at one circuit.
- **Potential:** sets training speed. A training gain is **0.2 + 0.1 × Potential** skill points, so Potential 5 gives 0.7 and Potential 0 gives 0.2. Potential **drops by 1 every season** and cannot go below 0.

**Ageing:** each season the driver, designer and commerce director all age one year. Young drivers lose little in the off-season and can even improve. Older drivers lose more.

**Contracts:**

- You can extend for one more season at **+15% salary** once fewer than 6 races remain, unless you have already signed a replacement.
- Extending deletes any open market bids you have.
- [Observed] Contract lengths run past one season (e.g. 43 or 57 races). A "reserve" driver type exists alongside the race driver.

**Observed DRP levels, Season 84:**

| Group | DRP |
|---|---|
| C1 drivers | 371 – 559 (leader's driver: 559 DRP, 30 years old, about $2.48M) |
| C2 | 140 – 531 |
| C3 | 140 – 319 |
| New-account default driver | 140 DRP, $400k, 3-race contract |

### 6.2 Designer [Rules]

- **Innovation** sets how many R&D points you earn per race.
- Higher designer skills lower the R&D cost of some technologies.

### 6.3 Commerce director [Rules]

| Skill | Effect |
|---|---|
| Negotiating | Sponsor offers rise more as you negotiate |
| Initial offer | Better opening offers |
| Relations | Sponsor mood falls more slowly while you negotiate hard |
| Marketing | Extra sponsor slots for next season (0–3) |
| Offers | How many sponsor offers you can hold at once (1–3) |

### 6.4 Mechanics and design crew [Rules]

- **Mechanics** improve the chance of setup feedback (their *setup* skill), **add practice laps** ("hiring more and right kind of mechanics") and **shorten pit stops**. They can be trained (not while your balance is negative).
- **Pit-stop skill** is also the "currency" lost through RB.I.A bailouts.
- **Design crew** add R&D points after each race.

### 6.5 The staff market [Rules]

There are markets for **drivers, designers and commerce directors**.

1. **Timing:** the market runs **every hour, on the hour**.
2. **Asking price:** a new candidate asks an initial salary that falls **1% per hour** until it reaches a shown **minimum asking salary**. *[Inferred]* After n hours the asking price is max(min, initial × 0.99ⁿ).
3. **Retirement:** a candidate unsigned for **720 hours (30 days)** retires.
4. **Signing:** a bid ≥ the *current* asking price signs at the next hourly run. Your current holder of that role is then cut to a **1-race** contract. The highest qualifying bid wins, and **ties are decided by a coin flip**.
5. **Bid caps per class:**

| Class | C1 | C2 | C3 | C4 | C5 | C6 |
|---|---|---|---|---|---|---|
| Max offer | 4.5M | 3.75M | 3.0M | 2.25M | 1.5M | 0.75M |

With a negative balance the cap is $750k in any class.

*[Inferred]* Strategy: watch good candidates as their price decays, and bid exactly the asking price at the hour you are willing to pay, just before a rival's bid would match it.

## 7. The race weekend

### 7.1 Practice [Rules]

There are **two practice sessions**, and the lap allowance **shrinks as you climb**:

| Class | Laps/session | Total |
|---|---|---|
| C1 | 3 | 6 |
| C2 | 4 | 8 |
| C3 | 5 | 10 |
| C4 | 6 | 12 |
| C5 | 8 | 16 |
| C6 | 10 | 20 |

More or better mechanics add laps. [Observed] A C1 practice result shows 7 laps run.

For each practice lap you set two things.

**A. The driver's DRP split across 5 areas:** Acceleration, Braking, Top speed, Kerb use, Racing line.

- The total cannot exceed the driver's DRP. [Observed – `main.js` `update_points_left()` computes `driver_points − Σ(areas)` and turns the counter red when it goes negative.]

**B. The car setup:**

| Setting | Range | Low value means |
|---|---|---|
| Front wing | 0–50 | low downforce: more straight-line speed, less grip |
| Rear wing | 0–50 | same as front |
| Suspension | 0–25 | soft, for bumpy tracks |
| Gears | 0–25 | short gears, for acceleration |
| Tyre pressure | 15–25 | low pressure, more grip |

**Feedback rules:**

- After a lap you **may** get an arrow: green ▲ means "increase", red ▼ means "decrease".
- **Only the value furthest from its optimum** gets an arrow. Sometimes there is no arrow, sometimes more than one.
- The chance of a DRP arrow rises with the driver's **Reporting** skill. The chance of a car-setup arrow rises with the mechanics' **setup** skill.
- A **quality rating of your DRP split** is given only twice, at the end of each session.
- The optimal settings **can change with the weather**.
- **All tyre types** are available in practice.
- After each lap the team reports **fuel used**, so you can measure consumption and lap time against fuel load.

*[Inferred]* For each track there is a hidden optimum vector: 5 DRP shares plus 5 car settings. Practice is a noisy search for it: the arrow tells you the direction of the coordinate with the largest error. With only 6 laps in C1, managers have to start from good prior settings (last season's values for the track, notes in the built-in **Notebook** page, or setups shared with friends). The rules say data sharing is legal; a JS `loadSetup()` helper exists to load saved setups.

[Observed] The legacy JS `loadSetup()` also has a **`revs_limiter`** field, an older setting since replaced by "Engine HP" (section 7.2). Its 4-plus-1 DRP inputs (`do1`…`do5`) suggest an older version had 4 areas.

### 7.2 Qualifying and race orders [Rules]

Both are submitted **together, before the deadline**. Qualifying runs right before the race.

**Qualifying format:**

- Three 10-minute parts. After Q1 and again after Q2, a third of the field drops out, so the fastest third fights for pole.
- You choose the **minute** at which your driver sets the flying lap. Later laps get **more grip** but run a higher **risk of traffic** spoiling them.

**Race orders:**

- **Starting fuel = qualifying fuel**, as in Formula 1's 2003–2009 parc fermé era.
- **Tyre lock:** if you qualify on a dry compound you must race that **same dry compound**, and only one dry compound per race. Intermediates and wets are always allowed. *(Race reports show sequences like Soft/Soft/Medium/Medium, so in practice the lock appears to apply per weather phase or has been relaxed. Treat it as unclear.)*
- **Pit laps:** the laps on which you stop for tyres and fuel.
- **Boost laps:** three pushes of 3 laps each. You enter the start laps, e.g. 1, 5, 10 gives pushes on laps 1–3, 5–7 and 10–12. Overlapping pushes give nothing extra.
- **Expected finishing position:** set it about right and the driver may find a little extra pace. Set it far too high or too low and the driver loses condition (and Confidence).
- **Overtaking risk:** more risk means more passes in unexpected places, and more crashes.
- **Blocking risk:** more risk means holding off faster cars for longer, and more crashes.
- **Engine HP:** more hp than standard costs reliability; less hp gains it.
- **Shift delay:** a shorter delay is faster but costs gearbox reliability; a longer one is slower but more reliable.

**Advanced options:**

- *Pit when tyres start to wear:* reschedules your next planned stop early. It does not count as an emergency stop.
- *Emergency stop as normal pit within N laps:* an emergency stop takes on the next planned stop's tyres and fuel, and that planned stop is skipped if it falls within N laps.
- *Let my teammate pass:* only applies when the teammate is behind you and attacking.

### 7.3 Sponsors [Rules]

Sponsors are negotiated **during the season for the next season**. Each offer has three parts:

- an **amount per race**, paid whatever the result,
- a **season goal**, from "compete in all races" to "win all races",
- a **bonus**, paid in full only if the goal is met. There is no partial bonus.

Negotiation is a push-your-luck loop:

- Every round raises the offer and **lowers the sponsor's mood**.
- The lower the mood, the more likely the sponsor walks away.
- The commerce director's skills shape this loop: Negotiating sets how fast offers rise, Relations how fast mood falls, Initial offer the starting point.
- **Offers** caps how many open offers you can hold. **Marketing** gives 0–3 extra sponsor slots.

[Observed] Title-sponsor goals seen in C1 include "Win 10 races in a season", "Top 5 in season", "Top 10" and "Top 22". The default newcomer goal is "Top 22 in season".

### 7.4 Weather and track data [Observed – race reports]

- **Weather** is modelled in phases with rain in mm. For example, Indianapolis S83R2 had 1 mm at the start, dry in the middle and 1 mm late.
- **Tracks** are described by:
  - laps (e.g. Las Vegas 50, Indianapolis 73),
  - **speed demand** (e.g. "very high"),
  - **handling demand** (e.g. "low"),
  - **overtaking difficulty** (easy / medium / …),
  - **tyre wear on a 1–10 scale** (Las Vegas 8/10, Indianapolis 9/10),
  - **pit-lane time loss** (e.g. "short 15-second pit loss").
- **Dry compounds:** Soft, Medium, Hard. Intermediate and Wet also exist.
- **Failures appear as race-log messages**, e.g. "Driver has lost a gear and is trying to compensate by adjusting their line" (a gearbox problem that slows the car) and "a box full of neutrals" (gearbox retirement). Heavy crashes also occur.
- Lap-by-lap logs can be downloaded (`download_race_log.php?race_id=…`, members only). The live viewer shows the race unfolding at the scheduled time.

### 7.5 Track pool [Observed – lap-record table]

Lap records exist for: A1-Ring, Adelaide, Algarve, Anderstorp, Austin, Barcelona, Brands Hatch, Buddh, Buenos Aires, California Speedway, Cancún, Estoril, Fuji, Hockenheim, Hungaroring, Imola, Indianapolis, Interlagos, Istanbul, Jeddah, Kuala Lumpur (Sepang), Kyalami, Las Vegas, Lusail, Magny-Cours, Melbourne, Mexico City, Miami, Monaco, Montreal, Monza, Nürburgring, Old Hockenheim, Old Nürburgring, Paul Ricard, Sakhir, Shanghai, Silverstone, Singapore, Spa-Francorchamps, Suzuka, Valencia, Vilnius, Yas Island, Yeongam and Zandvoort.

Public-league calendars mix current, classic and historic venues. Each group in a class races its own calendar order. For example, on 13 Oct 2026 the C1 "current track" was Montreal while C2 groups were at Barcelona and Singapore.

## 8. Season-long side competitions

### 8.1 Cup [Rules / Observed]

- A knockout competition inside each group, paid per round won (section 4.2).
- [Observed] The C1 bracket for Season 84 is seeded 1–32 in standard bracket order (1 v 32, 17 v 16, 9 v 24 …) and runs: 1st round, 2nd round, quarter-finals, semi-finals, final.
- Ties are scored as **3–0 or 2–1**, so each round appears to be a best-of-3 head-to-head over three races, won by finishing ahead of your opponent.
- *[Inferred]* Seeding probably follows last season's ranking. The rules mention 6 rounds, which would fit a 64-manager draw. With 23 C1 managers, top seeds get byes against empty slots.

### 8.2 Teams [Rules]

- Teams of two managers are formed each season.
- Joining or creating a team is free, and you can renew, switch or go solo.
- Teams do **not** promote or relegate together.
- Only full two-manager teams score in the team championship.
- Teams also show in the data, e.g. "Smoking Brains", "SuperNova", "Insomnia MotorSport", "Silver Arrows". The "Let my teammate pass" order lets teammates cooperate in races.

## 9. Information and statistics

The public **statistics** page has a very wide set of views. Some, marked *(S)*, are supporter-only.

**Per league and season:**

- Practice Results, Season Standings (showing each manager's livery and four suppliers), Results by Race, **Balance** (car level, sponsor income, title-sponsor goal, cash), **Drivers** (DRP, age, contract length and salary),
- Team Standings and Results, Cup bracket,
- *(S)* Qualification History, *(S)* Progress in the Race.

**All-time:** managers' and drivers' records (most races, wins, podiums, points, poles, fastest laps, biggest race progress, win from lowest grid slot, average position, each also for C1 only), current and record streaks (and "no-win" streaks), most active managers, "best buddies", most popular liveries, races on tracks, managers per race, countries, lap records, and all supporters.

*[Inferred]* Because rivals' balances, car levels, suppliers, driver DRP and contracts are all public, scouting is a real part of the game. You can see who is about to lose a driver (short contract), who can afford the best market candidates, and which supplier package suits the next track.

## 10. The simulation: what we know

The race engine itself is server-side PHP and not visible. Below is a model built **only** from documented and observed behaviour. All of it is *[Inferred]* unless tagged otherwise.

### 10.1 Lap-time model (qualitative)

Lap time is roughly:

`base track time` (×) **tyre performance %** [Rules: 98% means 2% slower]

plus penalties that grow with:

- **how far the car's speed/handling profile is from the track's** [Rules]
- **how far the DRP split and car setup are from the track optimum** (the hidden target practice searches for) [Rules]
- **weight above 600 kg, plus fuel weight** [Rules]
- **shift delay** (time without drive) [Rules]
- **tyre wear**, which depends on the compound, the track's 1–10 wear rating and the supplier's wear %, plus grip loss away from the tyre's optimal temperature [Rules / Observed]
- **mistakes** (fewer with Concentration) [Rules]
- **traffic**, in qualifying and in the race [Rules]

and bonuses for:

- **engine hp** (supplier power, tuned with Engine HP) [Rules]
- **driver DRP**, scaled by the driver's speed/handling rating against the track [Rules]
- **favourite track** [Rules]
- **boost laps** ("very fast lap times") [Rules]
- **realistic expected-position target** [Rules]
- **track grip rising** through qualifying [Rules]

Observed spreads give a sense of scale: in the C1 Miami race, P1–P4 finished within 51 s over 57 laps and P5 onward were lapped. Pace differences between top and bottom cars are therefore large, around 1–2 s per lap.

### 10.2 Reliability and incidents

Each race there is a per-component failure chance:

- **Engine:** supplier reliability %, worse with extra hp, better with reduced hp.
- **Gearbox:** reliability %, worse with a shorter shift delay.
- **Chassis:** reliability %.
- **Car reliability:** the design rating.

Failures are graded. Some are partial (a lost gear makes the car slower) and some end the race (no gears left).

Crash risk comes from the overtaking and blocking risk settings and the driver's Racing, Stamina and Talent. A badly chosen expected position also costs condition.

### 10.3 Overtaking

Whether a pass works appears to depend on:

- the pace difference,
- the track's overtaking rating,
- each driver's **Racing** and **Talent** (attacker and defender), plus the defender's **Stamina**,
- the overtaking and blocking risk settings.

Higher risk raises the chance that a pass succeeds, and the chance of a crash for both cars.

### 10.4 Strategy

The pit-stop time loss differs by track (e.g. 15 s at Indianapolis), and **mechanics** shorten the stop itself. On high-wear tracks there is a real trade-off between more stops on faster tyres and fewer stops on Hards.

The Season 83 reports show both approaches winning:

- R1: Medium×3 then Soft, 3 stops.
- R3: Hard×3, 2 stops, beat Medium×4 with 3 stops.

Fuel load is fixed by the qualifying fuel, so a light qualifying fuel load buys grid position at the cost of an earlier first stop.

### 10.5 Practice optimisation

There is a hidden 10-dimensional optimum (5 DRP shares plus 5 settings) per track and weather. Feedback is directional, noisy and only covers the worst coordinate. The best approach is coordinate-wise: move the flagged value by a decreasing step each lap and keep a notebook of final values per track. The weather-dependence means a wet race can invalidate the dry setup.

## 11. Season reset: what carries over and what is lost [Rules]

Order of operations at season end:

1. Offices close.
2. **Tax** (30% of holdings above $30M).
3. **Winnings:** championship, cup and team bonuses.
4. **RB.I.A bailout** if still negative.
5. **Promotion and relegation.**

Then everyone ages.

| Lost | Kept |
|---|---|
| All technologies | Money (after tax) |
| Saved R&D points | Staff and contracts, which age; drivers' skills drift with age |
| Supplier contracts and all supplier development | Statistics and history |
| | Team choice (renew, switch, or none) |

**Order parts before the last race** for race 1 of the next season, because sponsor negotiations and other office activity pause during the break.

**Relegation to, or failing to escape, the lowest class means a full reset:** you lose your staff, money, technologies, weight work and supplier development, and restart with **default staff and $30M**. Your statistics survive.

**Retirement** is offered at the start of each season. A retired account can be reactivated to start fresh in the lowest class. Making a new account instead is not allowed.

## 12. Community, rules of conduct and monetisation

**Membership rules** [Rules]:

- One account per person, with real name and country (changing your flag requires a GameMaster).
- Report bugs instead of exploiting them, on pain of deletion.
- GameMaster decisions are final.
- A rollback to a backup is possible in emergencies.

**Multi-accounts:** sharing a PC or network is allowed, but you must avoid looking like a multi. Sharing data with someone on the same PC risks both accounts.

**Account babysitting** is allowed only under these conditions:

- both players notify a GameMaster in advance (when, how long, who),
- a sitter covers only one account at a time,
- the maximum is 30 days per sitter.

**Server downtime compensation:**

- A single outage of 6 hours or more within 36 hours of a race deadline moves the deadline back 24 hours.
- So do outages totalling 18 hours or more in that window.
- If no staff member is online to postpone the race, it runs anyway, with no rollback.

**Tools:** the Info Center (news, polls, comments), forums (including a Bugs section), live race chat, a ticketed contact form (categories include "Cheating and multiple accounts investigations" and "Supporter activation and extension"), a personal **Notebook**, a guided first-time tour, a magazine ("Racing Boss Magazine") and social accounts (facebook.com/RacingBossGame, twitter.com/racing_boss).

**Supporter credits** [Observed – `supporter.php`]:

| Credits | 100 | 200 | 400 | 1000 |
|---|---|---|---|---|
| Price (PayPal) | €9.49 | €17.99 | €33.99 | €79.99 |

- The site states credits give "no advantage in the game".
- They buy: forum powers (thread ratings), posting telemetry graphs, renaming your driver, designer and commerce director, viewing rivals' sponsor tables and the best sponsors overall, a rating graph on your profile, supporter-only statistics, and **private-league entry fees**.
- Credits can be gifted to other players.
- *[Inferred]* The extra statistics are a small information edge.

## 13. Technology notes [Observed]

- **Server:** Apache 2.4.10 on Debian (≈2014-era packages) with PHP (`*.php`, `PHPSESSID`). Server-rendered pages with light AJAX (`ajax.php`).
- **Front end:** a mix of Bootstrap 3 and 5, jQuery and jQuery UI, reCAPTCHA on registration, the markItUp BBCode editor for the forums and Joyride for the tour.
- **Automation:** the staff market runs hourly and race starts are automated, while race postponements are manual. This matches the downtime rule.
- **Recent status:** server instability in Sep–Oct 2026 and a "maintenance" banner on 13 Oct 2026, with a migration planned.

## 14. Practical strategy summary

These follow from the rules above. Most are *[Inferred]*.

1. **Practice is everything in C1.** With 6 laps, bring a recorded baseline per track and per weather condition. Reporting skill (driver) and setup skill (mechanics) buy information. More mechanics buy laps.
2. **Match the car to the track.** Buy part mixes whose speed/handling ratio fits the circuit. Don't pay for weight saving below 600 kg.
3. **Spend R&D on a schedule.** Technologies are an instant, season-long gain, so invest early. Points and development are wiped at the reset, so spend everything before the season ends.
4. **Mind your supplier revisions.** Development only counts once you upgrade the "Current" spec, and the number of upgrades is limited.
5. **Pick suppliers for the season's calendar.** Ferarossa-style high-power, low-reliability engines need conservative HP settings. Durable tyres (Goodstone) shine on 8–10/10 wear tracks.
6. **Keep cash near $30M at season end**, since anything above is taxed at 30%. Convert it into staff, parts and testing during the season. Never end negative unless the pit-skill loss is acceptable.
7. **Use the market's price decay.** Asking salaries fall 1% an hour, so sniping at the right hour saves millions. Remember the class bid caps.
8. **Negotiate sponsors in steps** and stop before mood collapses. A strong commerce director (Relations, Negotiating, Offers, Marketing) multiplies income. Choose goals you can actually reach, since the bonus is all-or-nothing.
9. **Take the team bonus.** A two-manager team in C1 shares a $30M pot. Even a mid-field pair earns several million.
10. **Escape the lowest class quickly.** Staying there or dropping back means a full reset to default staff and $30M.

## 15. Open questions (need an account or the in-game Help)

- The exact lap-time, wear, fuel and failure formulas, and the weight per unit of fuel.
- The per-level price list for parts, the suppliers' per-race prices and their R&D ratings and revisions.
- The mechanic and design-crew grades, their salaries and how training works.
- How "Car level" (balance stats) maps to part levels 1–10.
- The exact tyre-compound lock rule in mixed weather.
- Cup seeding and how a best-of-3 tie is decided.
- The weekly race days and the time zone (race times are shown as 18:00 server time).

## Sources

- Racing Boss home page – https://www.racingboss.com/
- Rules – https://www.racingboss.com/rules.php
- About – https://www.racingboss.com/about_us.php
- Terms of Service – https://www.racingboss.com/terms_of_service.php
- Supporter – https://www.racingboss.com/supporter.php
- Hall of Fame – https://www.racingboss.com/hall_of_fame.php
- Statistics (standings, balance, drivers, cup, teams, races on tracks, lap records, countries) – https://www.racingboss.com/statistics.php
- Info Center news and Season 83 race reports – https://www.racingboss.com/info_center.php
- Contact – https://www.racingboss.com/contact_us.php
- Client script – https://www.racingboss.com/site/js/main.js
- OnlineSportManagers – Racing Boss profile: https://www.onlinesportmanagers.com/game-profile/motorsport-202-racing-boss/
- OnlineSportManagers – F1 Time (former name, archived): https://www.onlinesportmanagers.com/game-profile/motorsport-45-f1-time/
