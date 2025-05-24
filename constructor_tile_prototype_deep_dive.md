
# Constructor Tile Prototype Guide (Deep Dive)

This document is a step-by-step guide to building the **Constructor Tile**—a tiny chip that turns heat into usable energy for low-power electronics. The guide adds deeper context for decisions and trade-offs involved in the prototype process.

---

## 🔍 What is the Constructor Tile?

A tiny thermoelectric-powered chip that:
- Converts small temperature differences (like hand heat or pipe heat) into electrical energy
- Stores and manages that energy to power microelectronics
- Enables swarms of small, power-independent robots and sensors—without batteries

Think of it as a **microscopic steam engine**—but for ambient heat.

---

## ⚠️ Why It’s Hard (And Why It’s Possible Now)

Historically difficult due to:
- Sub-milliwatt energy capture efficiency
- Thermal leakage and dissipation
- Voltage too small for common electronics
- Energy harvesting circuit complexity

**Recent breakthroughs**:
- Cold-start PMICs from ePeas, Atmosic, and TI
- MEMS-scale thermoelectric materials
- AI microcontrollers under 1mW
- Ultra-low leakage supercapacitors

---

## 🛠️ Build Steps (with In-Depth Reasoning)

### Step 1: Define Your Power Target
**Target**: ~5µW average, enough to ping BLE every 10–30 seconds.

Why:
- Sets your thermal and electrical design constraints
- Helps choose thermoelectric chip and boost converter
- Ensures demo usefulness

---

### Step 2: Buy Your First Thermoelectric Generator (TEG)

**Vendors**: Micropelt, Ferrotec, Nextreme
- Look for: 15×15mm, Seebeck coefficient ~200 µV/K
- Typical ΔT needed: ≥5°C for useful output

Why:
- Start with known specs before jumping to custom MEMS builds

---

### Step 3: Build the Heat Gradient Stack

**Warm Side**:
- Thin copper plate bonded to heat source (e.g. laptop exhaust, human skin)

**Cold Side**:
- 3D-printed or aluminum fin to dissipate heat to air

**Interface**:
- Thermal pads or graphite sheets to minimize resistance

Why:
- Even 5°C delta at 200 µV/K gives ~1 mV per junction—requires stacking or conversion

---

### Step 4: Design the Harvesting Board

**Core Components**:
- PMIC: ePeas AEM10941 or Atmosic ATM3202 (cold start from 15 mV)
- Storage: 0.1–1F supercapacitor
- Regulator: 3V boost output
- MCU: Bluetooth SoC (e.g. Nordic nRF52)

Why:
- Converts drips of power into useful bursts
- Supercap prevents brownout between events

---

### Step 5: Build, Test, and Log Output

- Assemble TEG between copper & cold sink
- Connect PMIC, cap, MCU
- Place on warm object (pipe, laptop, cup)
- Use oscilloscope or multimeter to measure energy trickle
- Confirm BLE beacon or LED pulse

Why:
- Confirms feasibility, validates real-world use

---

### Step 6: Form Factor + Real-World Fit

**Enclosure**:
- Use SLA or CNC to create attachable form
- Add flexible mount for pipe or skin contact
- Shield circuitry from water/dust

**Field Test**:
- Pipe in winter
- Human wrist
- Outdoor utility box

Why:
- Demonstrates practicality, shows investor-ready use case

---

### Step 7: Advanced Version

**Goal**: Custom MEMS thermoelectric chip, energy-aware swarm integration

**How**:
- Use University of Michigan cleanroom (LNF)
- Fabricate BiTe or nanowire P-N junction array
- Integrate with Drooid swarm hive for collective sensing

**Bonus**: Add AI-based **heat-seeking behavior** so bots autonomously recharge

---

## 🔁 Summary

- You **can** build this today with off-the-shelf parts
- Detroit's ecosystem (Newlab, LNF, state grants) supports the build
- This tile is a foundational step to **battery-free swarms**

---

Want CAD files, circuit schematics, or a pitch deck next?
