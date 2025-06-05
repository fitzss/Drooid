# Project Title – µTER: A Monolithic Micro-Time/Energy Router for Sub-Millisecond Robotic Actuation

## 1-page project description for Lurie Nanofabrication Facility (LNF)

---

### What we want to build

µTER (“micro Time/Energy Router”) is a postage-stamp ASIC that sits on each gram-class robot in the DROID research program. It turns stored charge on-die into deterministic 10-to-1000 nJ packets that can be steered to any load (motor phase, sensor, radio PA) within < 500 ns of the commanded start time and with verified completion. In effect, the chip is a hard-real-time power switch-matrix that replaces the traditional “one Li-ion + single buck regulator” bus now limiting agility and modularity in micro-robotics.

---

### Why LNF?

To hit the required speed-and-mass envelope we must co-fabricate:

| Sub-block | Process need | Why LNF is a fit |
|-----------|--------------|------------------|
| 64-256 on-die MIM charge bins (0.5–2 µF ea.) | Dual-damascene Cu + ALD Al₂O₃ & 2 µm deep trenches on 200 mm Si | Proven in LNF’s BEOL capacitor runs; thickness control ≤ 2 % |
| GaN lateral e-mode switch cells (< 30 mΩ, 20 V) | Flip-chip attach of 40 µm × 40 µm GaN dielets to Si interposer | LNF can handle µ-bump re-flow & under-fill at wafer scale |
| Clock-deterministic arbiter logic | 180 nm BCD-Lite (Si CMOS + thick-gate LDMOS) | Standard mixed-sig PDK already qualified at LNF |
| Through-Cu vias + backside thin-grind | TSV etch / fill, final device thinned to 80 µm | Available in LNF’s packaging & mechanical finishing bays |

The facility’s ability to run heterogeneous integration—Si logic, GaN power, large MIM caps—on the same coupon is essential; no single foundry PDK offers that stack out-of-the-box.

---

### Fabrication flow (condensed)

- **CMOS front-end**: 180 nm logic & SRAM on 200 mm Si.
- **BEOL capacitor build-up**: three ALD-Al₂O₃ MIM layers, Cu redistribution, deep trench etch.
- **TSV & backside grind**: 10 µm TSVs, thin wafer to 80 µm for mass budget.
- **Flip-chip attach**: pick-and-place GaN dielets onto prepared islands, 30 µm µ-bumps.
- **Passivation & probe**: SiN over-coat, KGD testing at wafer level.
- **Singulation & wire-bond**: diced into 4.5 mm × 4.5 mm QFN-28 footprints; final RF shield lid.

---

### Deliverables for the 6-month LNF pilot

- **Tape-out-A mask set** (single-channel demonstrator, 50 µF aggregate on-die).
- **20 fully populated, packaged parts** with bench-top evaluation board.
- **Process data-pack**: capacitor density, GaN attach yield, timing-closure plots.
- **Joint publication** on “Sub-µs deterministic power routing via heterogeneous Si/GaN MIM-cap ASIC.”

---

### Impact & originality

Commercial PMICs and FPGA-based power modules regulate to average load; they cannot guarantee that a 250 nJ burst arrives at Port-A exactly 0.75 ms after the flip command while simultaneously withholding energy from Port-B. µTER adds that determinism layer, making energy a schedulable, digitally verifiable resource—crucial for sub-20 g flyers, centimetre-scale swimmers, and future modular swarm robots.

We seek LNF’s process integration expertise to prove the concept in silicon; if successful, µTER becomes the backbone of DROID’s constructor-theoretic “physical-AI” runtime and a unique showcase of LNF’s heterogeneous-integration capabilities.

---

### Primary contact:
**Fitz** — Graduate researcher, U-M Robotics  
fitz@umich.edu | +1 313-xxx-xxxx
