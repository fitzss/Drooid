# Drooid – Unknown-Unknowns Map

Below is a structured list of **problems to expect**, **questions you must answer**, and **when they’ll bite you**. Treat it as a living risk register; tick items off as evidence replaces assumptions.

---

## 🔹 Weeks 0 - 6 — Bench & Indoor Cage

| Problem / Risk Area | Key Questions to Answer | Why It Matters / When It Bites |
|---------------------|-------------------------|--------------------------------|
| **Weight-vs-thrust margin** | • Can each flyer stay < 250 g *including* Remote-ID beacon?<br>• Is T/W ≥ 1.8 with the 0603 motors? | Staying < 250 g lets you skip FAA registration and Remote-ID hardware. If you creep over, you’ll need certified add-ons and registration. |
| **UWB indoor positioning noise** | • What anchor geometry keeps RMS error < 15 cm?<br>• How much multipath in metal-rich shop? | Swarm logic collapses if pose noise > half bot size. UWB errors surface the first time 3 bots converge. |
| **Li-Po fire & shipping compliance** | • Are packs <100 Wh (UN 3480 limit)?<br>• Do we have safe-bag SOP and DOT labels? | You won’t be allowed to charge at Newlab without documented Li-Po safety SOP. |
| **Print repeatability** | • What variation in arm hole diameter over 10 CF-Nylon prints?<br>• Does resin hull warp >0.3 mm after 72 h? | Determines whether assembly yield holds when producing multi-unit swarms. |

---

## 🔹 Months 2 - 6 — Outdoor Corridor & First Pilots

| Problem / Risk Area | Key Questions to Answer | Why It Matters / When It Bites |
|---------------------|-------------------------|--------------------------------|
| **Comms reliability in cluttered RF** | • What’s packet-loss vs. distance inside Michigan Central brownfield?<br>• Do BLE mesh and UWB interfere? | Telemetry loss ruins swarm control and video feeds—first seen during field tests. |
| **Regulatory paperwork** | • Do we need LAANC *further-coordination* for flights >100 ft?<br>• How does Detroit Class B airspace affect the corridor? | FAA paperwork can take 30+ days—delays outdoor test clearance. |
| **Edge-AI power budget** | • Can Jetson run Tiny-YOLO and DDS broker under 5 W?<br>• What’s the battery weight impact? | If AI cuts battery life in half, the drone becomes useless for SAR ops. |
| **Single-motor failure modes** | • Median time-to-failure for 0603 motors outdoors?<br>• Can crawler limp on 1 motor out? | Reliability data will be needed for grants and pilot program expansion. |

---

## 🔹 Months 6 - 12 — Pilot Customer Integration

| Problem / Risk Area | Key Questions to Answer | Why It Matters / When It Bites |
|---------------------|-------------------------|--------------------------------|
| **Manufacturability at 100-unit lots** | • What is PCB yield at 0402 scale?<br>• Can CF-Nylon print farm hit 90% first-pass? | Investors will demand real COGS, not MVP estimates. |
| **Remote-ID & export controls** | • Which modular Remote-ID fits if >250 g?<br>• Do UWB radios trigger EAR/ITAR screening? | C1/C2 classification and CE mark are required for EU or government work. |
| **Swarm safety / deconfliction** | • Max swarm density before mid-air collisions exceed 1%?<br>• Can we create a quantitative SMS (Safety Management System)? | Needed to pass municipal and emergency-service audits. |

---

## 🔹 Year 1+ — Commercial Rollout

| Problem / Risk Area | Key Questions to Answer | Why It Matters / When It Bites |
|---------------------|-------------------------|--------------------------------|
| **Battery logistics & hazmat at scale** | • How to ship 500 >100 Wh packs per month (UN 3480 IA)?<br>• What ESG-compliant recycling loop exists? | Batteries will become a supply chain choke point beyond pilot scale. |
| **Competitor moat** | • What IP protects the AI-to-Print loop?<br>• Can we open-source swarm logic without giving away the core? | If Skydio or DJI enters, defensibility matters. |
| **Constructor-Theory feasibility validation** | • How many missions until physics-based planner beats heuristics? | This defines whether the Book of Nature is scientific or just branding. |

---

## 🔁 Cross-Cutting Questions (Revisit Every Sprint)

1. **Regulation checkpoint:** Are we still under 250 g, under 100 ft, and compliant with all FAA regs?
2. **Unit economics:** Are we tracking toward the $8k swarm COGS, or drifting up?
3. **Reliability metric:** What’s the new MTBF after this week's firmware or print change?
4. **Customer value test:** Are we reducing SAR risk or cost in a quantifiable way?
5. **Automation leverage:** Did the AI-to-Print loop save at least one manual step this sprint?

---

Keep this .md file close. As each unknown becomes a known—with tests, logs, and costs—you reduce risk and increase story strength for investors, customers, and regulators.
