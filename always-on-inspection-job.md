# 1 | The “always-on inspection” job-to-be-done

## Layer
| Classic outage-based inspection (incumbents) | Emerging underserved job |
|---------------------------------------------|---------------------------|
| “When the plant is cold and idle, prove nothing is cracked or fouled before we restart.” | “While the plant is running, tell me now if a tube is thinning, slag is forming or a flame is wandering so I can act before throughput or safety are hit.” |

### Situations when it matters most
- 2-to-6-week planned turn-arounds; unplanned shutdowns.
- Week-to-week steady operation; brief alarms; seasonal peak loads when shutdowns are impossible.

### Success metric
- Finish inspection inside outage window; certify restart.
- Zero forced outages; zero de-rates; early warning > 24 h; no human entry.

### Constraints
- Furnace is cool
- Unlimited human access
- Power, tethers, scaffolding OK

vs

- 200-500 °C gas flow
- 3–10 cm view-ports only
- No power plug; no human inside
- Must coexist with production

# 2 | Why incumbents don’t chase the “always-on” job

## Incumbent model
| Why it fits outage work | Why it doesn’t fit live-fire work |
|-------------------------|----------------------------------|
| **Revenue** – Day-rate crews, scaffold, UT carts | More hours, more gear → more revenue | $ value of a single 5-minute mini-inspection is tiny vs their overhead |
| **Hardware** – Tethered crawlers, water-cooled cameras | Weight & water lines fine in cold vessel | Impossible to cool or tether in 400 °C flow |
| **Process** – 2-week mobilise, permit, entry team | Aligns with scheduled outage timeline | Can’t react to “need a peek in 10 min” alarms |
| **Cost structure** – High labour, per-shift billing | High margin on big jobs | Microrobotic CAPEX + negligible OPEX breaks their model |

> Incumbents therefore rationally ignore the live-fire slice even though it sits inside the same $8–10 B industrial inspection market.

# 3 | Where DROID’s stack plugs the gap

## Stack element | Specific hurdle solved

- **DockTile P0 (“perch pad” harvesting ΔT)**  
  3–10 µW trickle removes battery swaps → drone can wait inside a 5–10 K gradient for hours, ready to launch in seconds.

- **Micro-drone (P1)**  
  20 g flyer with burst radio + hot-gas-rated skin performs 90-second reconnaissance, then re-perches.

- **Edge-sync on pad**  
  While perched, off-loads imagery, does local CV inference, pushes only findings upstream → no continuous high-power radio.

- **Fleet scheduler (“Hive”)**  
  Orchestrates dozens of pads/drones; auto-rotates sorties; issues early-warning tickets to CMMS.

## Economic impact (single furnace example)
Avoid one unplanned trip (≈ $500k fuel+capacity) per year; DockTile+drone network CAPEX ≈ $70k; payback < 60 days.

---

# 4 | People to interview & questions to validate need

| Persona | Org | 3 laser-focused questions |
|---------|-----|---------------------------|
| Combustion engineer | Refinery fired-heater group | 1. How often do you “fly blind” after a flame-out or opacity alarm? 2. What does a 24-h de-rate cost you? 3. What’s the fastest safe way you can currently look inside a hot duct? |
| Reliability superintendent | Coal or biomass power plant | 1. How many leak-before-break tube failures last year? 2. What did the forced-outage hours cost? 3. If a 3-inch port camera could warn you 24 h earlier, what would that save? |
| Plant turn-around planner | Petrochem maintenance | 1. What % of outage scope is “find what broke while running”? 2. Would a live-fire scout shaving 1 outage day justify ~$100k? |
| Inspection vendor PM (e.g. Applus, TEAM) | | Success signal: prospect puts a dollar figure on one avoided forced outage or one day of outage reduction that eclipses the estimated DockTile + drone network cost. |

# Business-model fit

## Why “robot + SaaS” (not pure service) matches this job

1. **Continuous value** – The Pad+drone stays on-site 365 days; client pays subscription for analytics & replacement birds.  
2. **Low variable cost** – Once installed, site visits drop to quarterly; margin scales with fleet not labour hours.  
3. **Capital budgets exist** – Plants already buy fixed sensors (thermocouples, IR gas) as CAPEX; DockTiles slot in there, while the data layer is OPEX.

---

# 6 | Simple note to co-founder

> “Hot-duct watch isn’t a new market; it’s a blind spot inside a huge one. Outage-oriented players won’t chase a job worth just a few thousand dollars per incident, but to the plant those few hours avert half-million-dollar hits. DockTile + nano-drone can own that blind-spot because we solve power, access and autonomy in one package.”

That’s the thesis in a nutshell.
