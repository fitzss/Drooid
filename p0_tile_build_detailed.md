
# Detailed Instructions and Bill of Materials for P0 Constructor Tile Build

## Objective
Build a functional proof-of-concept (P0) prototype of the Constructor Tile at Newlab Detroit to demonstrate the ability to convert a small temperature difference into usable electrical power.

---

## 🔧 Phase 1 — Thermal Harvesting Stack (Weeks 1–3)

### ✅ Goal
Demonstrate that heat → electricity → usable energy storage works at the microwatt scale with off-the-shelf parts.

---

## 🧩 Step-by-Step Instructions

### 1. **Purchase µ-TEG (Micro Thermoelectric Generator)**

- **Vendors**: Micropelt, Ferrotec, Nextreme
- **Model example**: Micropelt MPG-D651
- **Size**: ~15mm × 15mm
- **Expected Power Output**: 20–50 µW for ΔT ~5–10 K
- **Cost**: ~$30–40

### 2. **Build the Thermal Path**

#### Materials:
- **Copper shim plate (1–2mm thick)** — conducts heat from warm surface
- **3D printed fin (Nylon-12 or ABS)** — dissipates heat into ambient air
- **Thermal interface pad (Graphite pad 50µm)** — increases heat transfer efficiency

#### Instructions:
- CNC or 3D print the copper and fin at Newlab’s fabrication lab
- Sandwich the TEG module between the copper and the nylon fin
- Use thermal pad on both hot/cold sides for contact efficiency
- Use epoxy or small clamps to secure the stack

### 3. **Assemble the Power Conditioning Board**

#### Components:
- **Boost Converter IC**: e.g. ePeas AEM10941 (cold-start at 350mV)
- **Supercapacitor**: 1F, 4.5V (Panasonic EEC-EN0F105)
- **Buck Converter IC**: e.g. TI TPS62740 (ultra-low Iq)
- **BLE header**: JST connector for Nordic nRF52 SoC or test LED

#### Instructions:
- Order PCB or solder components to a prototype board
- Use hot plate or reflow oven at Newlab to solder ICs
- Wire output of TEG to boost converter input
- Boost → Supercap → Buck → BLE/LED

---

## 🧪 4. Test Rig Setup

### Tools:
- Hot plate or laptop exhaust for heat source (~40°C)
- Fan or natural air for cold sink (~25°C)
- Multimeter or oscilloscope

### Procedure:
1. Place copper side on warm surface
2. Let nylon fin cool passively or use fan
3. Connect multimeter to output of boost converter
4. Record voltage rise and current flow

✅ **Success Metric**: ≥ 100 µW of stable average power at 3.3V

---

## 📦 Bill of Materials (BoM)

| Item                       | Description                              | Unit Cost | Qty | Total |
|---------------------------|------------------------------------------|-----------|-----|-------|
| µ-TEG Module              | Micropelt MPG-D651 or Ferrotec           | $35       | 1   | $35   |
| Copper Plate              | CNC copper shim (1–2mm)                  | $5        | 1   | $5    |
| Nylon-12 Fin              | SLS 3D printed heat sink                 | $5        | 1   | $5    |
| Graphite Thermal Pad      | 50µm thickness, 15×15mm                  | $2        | 1   | $2    |
| ePeas AEM10941            | Energy harvesting boost converter        | $6        | 1   | $6    |
| Supercapacitor            | 1F, 4.5V                                 | $2        | 1   | $2    |
| Buck Converter            | TI TPS62740                              | $1        | 1   | $1    |
| Custom PCB or Breadboard  | Small test board                         | $10–80    | 1   | $50   |
| Misc connectors/wire      | JST header, test pins, LED               | $5        | 1   | $5    |
| **Estimated Total**       |                                          |           |     | **$111–$140** |

---

## 🔁 Output

- Powers a BLE beacon or LED every 10–30 seconds using harvested heat
- Demonstrates “power from ambient waste heat”
- Launches Droid’s roadmap for battery-free autonomy

---

### 🔍 Next Steps After P0

- Package into 3D-printed module housing
- Begin stress testing in real environments (pipes, laptops, skin)
- Plan MEMS-scale design and wafer packaging phase (Q2–Q3 build)
