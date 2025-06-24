# Drooid: A Prompt‑Native Robotics Platform for the Underserved Experimenter

The past decade has delivered dazzling strides in cloud AI and in high‑end industrial robotics, yet one layer of the market remains chronically overlooked: small R&D groups, field engineers, university labs and solo founders who need *occasional, on‑site* robotic capability but cannot justify six‑figure capital purchases or permanent cloud contracts. Their work is typically location‑constrained (ranches, mines, green‑houses, disaster zones), bandwidth‑starved and highly iterative; they need to try something, measure, tweak and try again—often within hours, not quarters.

Drooid proposes a **field‑lab stack** that collapses swarm coordination, edge AI, burst‑power actuation and rapid‑fabrication into a rugged carry‑on box plus printable robots, all driven from plain‑language prompts.

---

## 1. Job‑to‑Be‑Done

**Rapid, low‑overhead physical experimentation**  
1. Draft a task in English (“scan these vines for mildew, spot‑spray any infected leaves”).  
2. Push that prompt to whatever robots are on hand—COTS quad‑copters, a 3‑D‑printed rover, or a borrowed Spot Mini—*without* rewriting ROS nodes or standing up an edge cluster.  
3. Iterate in the field, possibly off‑grid, and archive results for later analysis.

Incumbent offerings break down on three fronts:

| Pain | Why incumbents fail |
|------|--------------------|
| Up‑front cost | DJI, Skydio and Boston Dynamics embed hardware margin + proprietary spares; \$5 k–\$75 k per unit is beyond maker‑lab budgets. |
| Compute coupling | Jetson/Orin assume 15–25 W, active cooling and a CUDA‑savvy developer. |
| Cloud tether | AWS RoboMaker et al. require reliable back‑haul; fees penalise bursty, project‑based usage. |

---

## 2. Drooid Architecture (Layer View)

| Layer | Component | Key Idea |
|-------|-----------|----------|
| Actuation | **µTER‑Mini** 120 mg HV ASIC | 5 V→150 V boost + GaN H‑bridge + 0.5 mJ burst bank in WLCSP; snaps onto sub‑10 g drones. |
| Compute | **BP‑SPAR boardlets** | RK3588 SBC with unified 5 V rail; Orin Nano or cloud off‑load as plug‑in. |
| Hub | **Hive Box** | 1.3 kg, fan‑less, battery‑swap, tri‑radio mesh; boots Rust OS in 6 s; stores LLM + plans. |
| Software | **Prompt‑to‑Plan (P2P)** | LLM → constraint graph → ROS 2 micro‑graph; enforces power/airtime/legal envelopes. |
| Fab loop | **GPT‑CAD ↔ 3‑DP** | Text‑to‑parametric CAD → sliced → farm‑printed; firmware stubs auto‑insert µTER footprints. |
| KB | **Book of Nature** | Crowd‑source repo of successful task+robot recipes, searchable by environment + sensor load‑out. |

---

## 3. Subscription Model

**Field‑Lab‑as‑a‑Service**  
* \$495 / yr: Hive Box + 2 BP‑SPARs + OTA + Book access  
* Robot credits: 500 g PA12 print/month, shipped flat‑pack in 72 h  
* µTER‑Mini metering: extra reels at cost‑plus when duty cycle spikes

---

## 4. Competitive Moat

1. **Power‑first silicon** – µTER‑Mini beats discrete boost + driver chains on cost/size.  
2. **Prompt abstraction** – no URDFs; end‑users get human‑readable plans.  
3. **Edge autonomy** – runs offline; Starlink optional.  
4. **Circular hardware sub** – print‑farm turns CAPEX into OPEX; frames evolve with tasks.

---

## 5. Roadmap

| Q | Milestone |
|---|-----------|
| 3Q25 | µTER‑Mini EVT + 10 alpha labs |
| 1Q26 | Public beta, external GPT‑CAD plugins |
| 4Q26 | Orin mezzanine; 10 k Book recipes |
| 27+ | Metal cold‑spray printing, solar perch charger |

---

## 6. Risks & Mitigations

* ASIC yield – keep discrete fallback.  
* Regulation – bake geofence + audit trail.  
* Copycats – community lock‑in + silicon supply agreements.

---

## 7. Conclusion

Drooid is **not** “Jetson in a box.” It is a vertically sliced field‑lab platform melding power, compute, comms and fabrication into one coherent stack, optimised for the 80 % of real‑world experiments that industrial giants ignore. By lowering cognitive load (prompt not firmware) and capital burden (subscription not CapEx), Drooid activates a long‑tail market—tens of thousands of scientists, civic engineers and indie founders eager to move fast in the physical world.
