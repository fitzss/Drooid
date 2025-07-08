---
marp: true
theme: default
backgroundColor: '#ffffff'
paginate: true
---

# **Drooid • DualEdge Swarm**  
Palm-size drones that **talk, map & stop**  
Daniel Kalu | Fitz Doud · July 2025

---

### **1 · The exact DoD gap (2025)**

| DIU / JNLWP wording | What operators face today |
|---------------------|---------------------------|
| “**Blue-listed, NDAA-clean** sUAS” | China-silicon bans sideline 60 % of COTS quads. |
| “**Modular effectors** in addition to sensors” — Project G.I. | Existing Blue quads = *flying GoPros* only. |
| “Autonomous in **GPS- and RF-denied interiors**” | Ship holds & bunkers kill GPS; Skydio loses VIO in low-light steel. |
| “**Non-lethal incapacitation at 3–5 m** remains unsolved” | Flash-bangs are hand-thrown; Taser Drone is >2 lb. |

**Result:** platoons breach blind or escalate to lethal force for lack of a palm tool.

---

### **2 · Solution in one line**

> **DualEdge** is the **first Blue-listed palm drone** with a **hot-swap rail** that flies through steel corridors, **relays comms**, **maps blind**, and **stuns a hostile** at hallway distance.

---

### **3 · What makes it novel vs. “Blue” competition**

| Feature | **DualEdge** | Skydio X2D | FLIR Black Hornet | Crazyflie |
|---------|--------------|------------|------------------|-----------|
| Weight | **115 g (Cat-1)** | 1320 g | 33 g | 61 g |
| NDAA parts | ✔ | ✔ | ✔ | ✖ (PRC Li-Po) |
| **Rail payload** | **30 g hot-swap** | fixed cam | none | header stack |
| Mesh relay pod | **✔ 900 MHz** | add-on backpack | ✖ | ✖ |
| Non-lethal pod | **✔ flash / siren (v0) · shock (v1)** | ✖ | ✖ | ✖ |
| Indoor GPS-deny | ✔ VIO + UWB | VIO only (fails in steel) | optical-flow | flow deck |
| Unit cost proto | **\$750** | \$17 k | \$90 k | \$200 |

*DualEdge is the **only** nano-drone that ticks every box DIU just published.*

---

### **4 · Minimum deliverable in 6 months**

| Item | Spec |
|------|------|
| **Blue frame** | 115 g duct, VOXL 2 Mini, OAK-D Lite, TPM SBOM |
| **Rail v1** | 35 g capacity · 30 s swap |
| **MeshPod-Lite** | 900 MHz relay 1 Mbps through 2 bulkheads |
| **StrobePod-S1** | 5 k-lumen flash + 118 dB siren (3 m pain-compliance) |
| **Autonomy** | Hover & navigate 10 m corridor with zero GPS |

---

### **5 · AI-to-Print build loop**  

1. **Prompt CAD** → generative duct + rail (3 min)  
2. **Blue check script** – NDAA parts envelope & SBOM auto-hash  
3. **Slice & MJF print** (5 h)  
4. **Bolt COTS motors + VOXL** (30 min)  
5. **Indoor hover test** (< 10 cm drift)  

*Hardware iterations move at software speed; competitors need carbon molds.*

---

### **6 · 6-month schedule & spend**

| Month | Milestone | Cost | DoD spec cleared |
|-------|-----------|------|------------------|
| 0 | Design freeze · NDAA BOM | — | Compliance gate |
| 1 | Print & hover Blue frame | \$300 | Air-frame ✔ |
| 2 | StrobePod burn-in (100 cycles) | 150 | Non-lethal ✔ |
| 3 | Mesh relay test (steel) | 100 | Modular comms ✔ |
| 4 | UWB-VIO indoor nav | — | GPS-deny ✔ |
| 5 | 90-s video + SBOM → DIU | — | Project G.I. packet |
| **Total cash** | | **≈ \$5 k** | |

---

### **7 · Business model**

* **Phase I (2025-26)** Non-dilutive SBIR + DIU prize → pilot kits  
* **Phase II (2026-27)** Replicator LRIP • OTA w/ SOCOM, Navy security  
* **Phase III (2027+)** Campus & private-security deterrence kits (Strobe / OC)

---

### **8 · Funding ask**

**\$500 k SAFE @ \$6 M post**

| Use | \$ | Outcome in 9 mo |
|-----|----|----------------|
| Rail & frame production (20) | 160 k | Pilot kits |
| Mesh + Strobe parts | 120 k | Demo & eval |
| StingPod R&D start | 140 k | 3-5 m shock v1 |
| Ops & runway | 80 k | 9 mo burn |

AFWERX SBIR + MI match (\$100 k) already filed.

---

### **9 · Team**

* **Fitz Doud** – Ex-open-source autopilot lead  
* **Daniel Kalu** – Minerva CS · ROS 2/SLAM  
* **Advisors** – ex-SOCOM CQB officer • Wayne State HV Lab • ModalAI Blue lead

---

### **10 · Why invest now**

* DIU’s **own language** defines the gap.  
* No other palm drone delivers **Blue + relay + indoor autonomy + non-lethal**.  
* AI-to-Print loop slashes hardware cycle time; \$5 k gets the demo, \$500 k gets LRIP pilots.

*Back us and own the first swarm that actually meets DoD’s 2025 shopping list.*

---

### **Contact**

fitzdoud@gmail.com | dankalu.work@gmail.com

*Palm-size, mission-ready. Let’s build it.*
