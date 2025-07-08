---
marp: true
theme: default
backgroundColor: '#f7f9fc'
paginate: true
---

# **Drooid • DualEdge Utility Swarm**  
*Palm-size drones that talk, map & stop*  
Daniel Kalu | Fitz Doud · July 2025

---

### **1 · Battlefield pain (2025)**

| Gap inside ships & tunnels | Consequence |
|----------------------------|-------------|
| Comms drop once GPS / radios fade | Teams go blind & mute |
| No gas/chem pre-check | First soldier gets hit |
| No palm-size non-lethal (3-5 m) | Must escalate to lethal force |
| Legacy micro-drones only film | Zero active effect |

> *“Compact, lightweight non-lethal payloads for small UAS are still missing.”*  
> — Navy SBIR N211-001 / JNLWP

---

### **2 · DoD must-have list (July 2025)**

1️⃣ **Blue-listed, NDAA-clean air-frames**  
2️⃣ **Modular payload rail** — sensor ⇆ effector in seconds  
3️⃣ **Indoor autonomy** — GPS- & RF-denied spaces  
4️⃣ **Non-lethal incapacitation @ 3–5 m** — *unsolved*

---

### **3 · Solution — DualEdge v0**

| Piece | Spec |
|-------|------|
| **Blue frame** | 115 g ducted quad · VOXL 2 Mini · OAK-D Lite · TPM-signed SBOM |
| **Rail v1** | 35 g hot-swap latch (print in < 1 h) |
| **MeshPod-Lite** | ESP32 900 MHz relay · 1 Mbps through two steel doors |
| **StrobePod-S1** | 5 k-lumen flash + 118 dB siren · 3 s burst |
| **ChemSense & StingPod** | Slotted for Phase II (same rail) |

*One frame • two pods • cost ≈ $550 in parts.*

---

### **4 · Why now**

- **DIU Project G.I.** — \$20 M for *“ready-now, less-exquisite”* UAS (eval Oct-Dec 2025)  
- **Replicator Tranche 1** needs thousands of micro-drones by FY-26  
- Blue sUAS refresh demands *effectors*, not just cameras  
- AI-to-Print loop → frame CAD ➜ SLS part ➜ flight **same day**

---

### **5 · AI → Print → Hover loop**

1. Prompt spec → generative CAD (3 min)  
2. Blue-fit script checks VOXL/OAK envelope + SBOM IDs  
3. Auto-slice → HP MJF print (5 h)  
4. Snap motors, VOXL, payload rail (30 min)  
5. Indoor hover with VIO (< 10 cm drift)  

*Physical iteration moves at software speed.*

---

### **6 · 6-month build & demo plan**

| Month | Deliverable | DoD value proved |
|-------|-------------|------------------|
| **0** | Design freeze · NDAA BOM | Compliance gate |
| **1** | Hover demo on Blue frame | ✔ air-frame |
| **2** | StrobePod burn-in (100 cycles) | ✔ non-lethal (3 m) |
| **3** | MeshPod relay test (steel) | ✔ modular comms |
| **4** | Depth-only auto-hover, UWB anchor | ✔ indoor autonomy |
| **5** | 90-sec video + TPM-hash SBOM | DIU Project G.I. packet |

Cost to demo: **≈ \$5 k** (6 air-frames, 2 pods, spare parts).

---

### **7 · Business pathway**

1. **SBIR Phase I** (AFWERX \$75 k + MI \$25 k match)  
2. **Project G.I. pilot** — live eval, OTA award  
3. **LRIP via Replicator / RCCTO** — FY-26  
4. **Civ spin-off** — campus & private-security deterrence kits (FY-27)

---

### **8 · Market snapshot**

| Segment | 3-yr SAM |
|---------|----------|
| DoD small-UAS & C-UAS | \$3 B |
| Non-lethal RDT&E | \$0.15 B |
| Private security patrol | \$10.8 B |

1 % DoD SAM = \$30 M revenue potential by 2028.

---

### **9 · Funding ask**

**\$500 k SAFE @ \$6 M post-money**

| Spend | \$ | Milestone |
|-------|----|-----------|
| Frame & rail production (6 kits) | 120 k | Hover + SBOM video |
| StrobePod & MeshPod parts | 100 k | Non-lethal + relay demo |
| StingPod & ChemSense R&D start | 160 k | Phase II roadmap |
| Ops, travel, buffer | 120 k | 9-month runway |

Non-dilutive in-flight: AFWERX SBIR + MI fund = \$100 k.

---

### **10 · Team**

| | |
|---|---|
| **Fitz Doud** | Ex-open-source autopilot maintainer · HW/firmware |
| **Daniel Kalu** | Minerva CS · ROS 2 / SLAM/AI |
| **Advisors** | ex-SOCOM CQB officer · Wayne State HV Lab · ModalAI Blue team |

---

### **Thank you**

fitzdoud@gmail.com | dankalu.work@gmail.com  

*One palm drone. Two mission pods. DoD gap closed in six months.*
