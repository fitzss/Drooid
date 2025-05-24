# Constructor Tile – Prototype Build Plan (v2.0)

A sharpened, more realistic roadmap for getting your first heat‑powered “Constructor Tile” from whiteboard to demo unit.

---

## 0. Decide the *job to be done*

1. **Pick ONE launch application**  
   *Example*: a Bluetooth Low‑Energy (BLE) asset‑tracking tag that broadcasts every 15 s from a warm industrial pipe.

2. **Translate the job into three numeric specs**  
   | Metric | Target | Why it matters |
   |-------|--------|----------------|
   | Average electrical power | **≥ 10 µW** | Covers BLE advertising + PMIC losses |
   | Minimum ΔT (temperature difference) | **≥ 5 °C** | Lets you work with “lukewarm” sources like human skin |
   | Lifetime in field | **2 years, no battery swap** | Shows clear advantage over coin‑cells |

---

## 1. Model before you buy

| Task | Tool | Outcome |
|------|------|---------|
| Quick thermodynamic simulation | **COMSOL** or free Energy2D | Estimates open‑circuit voltage at various ΔT & chip sizes |
| Power‑budget spreadsheet | Google Sheets | Confirms capacitor size, duty‑cycle, radio burst energy |

**Why:** Ten lines of math here can save ten weeks of re‑spins later.

---

## 2. Choose a *starter* TEG die

* **Options (July 2025, stock parts):**  
  | Vendor | Size | R<sub>int</sub> | V/ΔT | Comment |
  |-------|-----|-----------|--------|---------|
  | *Ferrotec NES15* | 15 × 15 mm | 5 Ω | 20 mV K⁻¹ | Hobby‑friendly |
  | *Micropelt MP1060* | 6 × 6 mm | 18 Ω | 32 mV K⁻¹ | Tiny but higher V |

* Order **5–10 pcs** for destructive tests.

---

## 3. Build the thermal stack

```text
[Heat Source]─Cu shim─TIM 1──TEG──TIM 2─3‑D printed fin/graphite sheet─[Ambient]
```

* **TIM 1/TIM 2**: 0.2 mm silicone pads (6 W m⁻¹ K⁻¹); easier than grease.  
* **Cold‑side fin**: Print in black PA12, coat in graphite spray to radiate better.

> No heat gradient, no watts. 80 % of first‑time failures are bad clamping pressure—use spring screws and a torque spec (e.g., 0.3 Nm).

---

## 4. Energy‑harvesting electronics

| Block | Part # (example) | Notes |
|-------|-----------------|-------|
| Nanopower boost / MPPT | **ePeas AEM10941** | Starts at 50 mV, > 90 % eff. |
| Storage element | 22 mF 3.6 V supercap | Gives 20 J @ 3 V |
| System MCU/RF | **Nordic nRF54L** in DC‑DC mode | 1.1 µA sleep |

Add **NTC thermistors** on both TEG faces—these later feed the “heat‑seeker” algorithm.

---

## 5. Firmware v0.1 (“heat‑seeker”)

1. Poll ΔT every 5 s.  
2. If ΔT < 3 °C **→** drop TX rate to 1 pkt/min.  
3. If ΔT > 8 °C **→** full TX rate; also blink an “energy OK” LED.

> This adaptive duty‑cycle is the *software* half of your Constructor Theory story: the tile behaves as a three‑state work variable (cold / nominal / hot).

---

## 6. Benchtop validation

* **Hot plate + fan tunnel** → sweep 25 → 60 °C, log V<sub>out</sub>, TX current.  
* **Environmental chamber** → 0 → 45 °C cycles, 200 hrs.  
* **Drop & vibration** → ensure solder joints survive real robots.

---

## 7. Looks‑like / works‑like unit

* **Enclosure**: SLA print, snap‑fits around fin & PCB.  
* **Interface**: USB‑C test header + Magnetic pogo pads (for swarm docking).  
* Weight target < 4 g.

---

## 8. Pilot deployment

| Vertical | User | Mount | Success metric |
|----------|------|-------|----------------|
| Utilities | Water‑pipe inspector | Hose‑clamp | ≥ 90 % packet delivery for 30 days |
| Wearables | Bio‑patch startup | Medical adhesive | Skin temp > air temp 60 % of day |

---

## 9. Version 2.0 moon‑shot

* Move from bulk BiTe TEG to **MEMS solid‑state Stirling** (see Sandia 2024 paper).  
* Integrate on‑die **EdgeTPU uNP** (400 µW) for local anomaly detection.  
* Co‑design with Drooid’s swarm motherboard so each drone carries a Tile + thin‑film LiPo as hybrid.

---

## 10. Resources & vendors

* **Thermal pads**: Laird Tflex HR400.  
* **Micro‑machining**: University of Michigan LNF Foundry (startup waiver program).  
* **PCB assembly**: Tempo Automation Detroit line (24 h turn).

---

### Key changes vs. the earlier plan

| Old step | Improvement |
|----------|-------------|
| “Buy any TEG” | Pick from a vetted shortlist + order extras for failure analysis |
| No simulation | Up‑front COMSOL + budget sheet prevents underspec |
| Generic firmware | Added ΔT‑adaptive “heat‑seeker” logic |
| Vague testing | Concrete test rigs + reliability hours |
| Jump to custom MEMS | Stage‑gate: prove market first, then custom silicon |

---

### Bottom line

You still start simple, but now every step *de‑risks* power, thermal, electronics **and** market fit before you sink cash into MEMS tooling. This is builder‑level actionable—and investor‑ready.

