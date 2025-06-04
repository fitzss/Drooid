# Silicon-Interposer Task-Energy Orchestrator Tile (TEO-µ)  
### A Thin-Film Thermoelectric / On-Chip-Capacitor Power Module for Sub-Gram Robots  
**Project description for Lurie Nanofabrication Facility (LNF)**  

**Lead investigators**  
- **Fitz _______** – Drooid Labs, Power Architect (primary user)  
- **Daniel _______** – Drooid Labs, Mechatronics Lead (secondary user)  
- **Faculty sponsor (UM-ECE, tentative)** – Prof. __________, Solid-State Devices Group  

---

## 1 &nbsp;Scientific motivation & broader impact
Palm- and insect-scale robots are now limited less by mechanics than by _how fast, how often, and how precisely energy can be delivered_ to µ-actuators. Conventional Li-ion cells are mass-dominated, exhibit millisecond-scale impedance recovery, and cannot supply the 100–500 mA, < 100 µs bursts required for agile flight or crawl-hop manoeuvres.  
This project prototypes a **chip-level “burst reservoir”** (TEO-µ) that harvests tens of microwatts from ambient heat or a low-power inductive link, buffers it in an ultra-low-ESR capacitor array, and releases deterministic 10–500 nJ packets under digital command.  

Success will (i) demonstrate a *fabrication pathway entirely achievable with existing LNF toolsets* and (ii) provide a reference energy subsystem for future LNF user projects in autonomous sensors, implantables, and soft micro-robots.

---

## 2 &nbsp;Project scope & milestones  

| Phase | Clean-room weeks | Key fabricated structures | Exit criterion |
|-------|-----------------|---------------------------|----------------|
| **0 – Process checkout** | 2 wks | Blanket Bi₂Te₃ film, ALD Al₂O₃ MIM capacitor stack (1 cm² test coupon) | Seebeck > 150 µV K⁻¹; Cap ESR < 50 mΩ |
| **1 – TEO-µ v1 tile** | 6 wks | • Four-leg thin-film TEG<br>• 13.56 MHz spiral coil (Cu 10 µm)<br>• 0.5 µF on-chip MIM capacitors<br>• Au I/O pads & diced 10 × 10 mm Si interposer | ≥ 200 mA, 50 µs burst into 10 Ω load |
| **2 – Integrated burst router** | 4 wks (packaging) | Flip-chip attach of 130 nm CMOS switch matrix; wire-bond breakout; Parylene passivation | Dragonfly wing-flap demo powered solely by tile bursts |
| **3 – Exploratory QD test mesa** (optional) | 4 wks | 20 nm InGaAs QD mesas patterned by e-beam & RIE | Room-temp PL signal > 5× background |

_Total anticipated LNF clean-room usage: **≈ 16 weeks** over 10 months._

---

## 3 &nbsp;Detailed phase-1 process flow  

| # | LNF tool / module | Material & thickness | Notes / contamination class |
|---|-------------------|----------------------|-----------------------------|
| 1 | — | 100 mm, 400 µm p-Si wafer |  |
| 2 | PECVD | SiO₂ 500 nm | Electrical isolation |
| 3 | Sputter (AJA) | Bi₂Te₃ 2.5 µm | Lift-off (SPR 955) |
| 4 | RTA | 250 °C N₂ | Crystallise TEG legs |
| 5 | E-beam evap | Ti/Cu seed 100 nm |  |
| 6 | Electroplate | Cu 10 µm | 13.56 MHz coil; SU-8 mask |
| 7 | ALD / PEALD | Al₂O₃ 50 nm + TiN 30 nm | MIM dielectric + bottom electrode |
| 8 | PVD | Al 300 nm (MIM top) |  |
| 9 | ICP-RIE | Cl₂/BCl₃ etch | Define TEG, coil, caps |
|10 | STS DRIE | Back-side cavity | Thin die to 200 µm |
|11 | Parylene C | 2 µm | Pad openings via O₂ plasma |
|12 | E-beam evap | Ti/Au 20/200 nm | I/O pads; lift-off |
|13 | Disco saw | — | Dice 10 × 10 mm |

Metrology after each critical layer: SEM, profilometer, 4-pt probe, AFM.

---

## 4 &nbsp;Materials & segregation statement
- **Semiconductors:** Si (all phases); InGaAs only on separate III-V wafers.  
- **Metals:** Cu, Ti, Au, Bi₂Te₃ (handled in dedicated chamber).  
- **Dielectrics:** SiO₂, Al₂O₃ (standard).  
No alkali metals, Hg/Cd, or unapproved polymers. All steps follow LNF material-restriction matrix.

---

## 5 &nbsp;Equipment & training requested  

| Category | Tool (ID) | Training |
|----------|-----------|----------|
| PVD | AJA Load-Lock #2 (BiTe) | New |
| Electroplating | Acid Cu C-2 | New |
| Lithography | SUSS MA6; JEOL e-beam | MA6 refresher; JEOL new |
| Etch | Oxford ICP-RIE; STS DRIE | Oxford refresher; DRIE new |
| ALD | Savannah (Al₂O₃); PEALD TiN | New |
| Metrology | Hitachi 4800 SEM; 4-pt probe | SEM refresher |
| Packaging | Finetech flip-chip | New |

Estimated phase-1 tool time ~120 h (schedule in Appendix A).

---

## 6 &nbsp;Safety & waste
- Bi/Sb-telluride waste collected in heavy-metal jar per SOP.  
- Parylene precursor handled in dedicated hood; vent to scrubber.  
- HF use < 2 min in wetch bench 12; all personnel HF-qualified.

---

## 7 &nbsp;Deliverables to LNF
1. **Process logs** shared on LNF wiki.  
2. **Electrical dataset** (Seebeck, ESR, burst current).  
3. **Poster & talk** at LNF Users’ Symposium.  
4. **Joint journal paper** (*IEEE J-MEMS*, process co-authorship offered).

---

## 8 &nbsp;Requested start window
Earliest access **Q3 2025**; phase-1 wafer run complete by **Nov 2025** to feed downstream robot demo.

---

## Contact  
Fitz _______ – <fitz@drooid.ai> – +1-313-xxx-xxxx  
Daniel _______ – <daniel@drooid.ai>  
_LNF project code (to be assigned): **TEO-µ-25-LNF**_

We look forward to collaborating with the LNF team to realise a first-of-its-kind silicon-compatible burst-energy module that can unlock agile, long-endurance micro-robots and other extreme-power-density devices.
