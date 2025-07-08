---
marp: true
theme: default
backgroundColor: '#ffffff'
paginate: true
---

# **Drooid • DualEdge Swarm**  
*Palm-size drones that **talk, map & stop***  
Daniel Kalu | Fitz Doud · July 2025

---

### **1 · What DoD says it needs (verbatim)**

> **“Modular effectors in addition to sensors”**  
> – DIU **Blue sUAS Block 4 RFI**, Apr 2025  
>
> **“Ready-now, less-exquisite sUAS that squads can adapt in weeks”**  
> – **Project G.I.** launch note, 2 Jun 2025  
>
> **“Compact, lightweight non-lethal payloads… incapacitation at **3–5 m**”**  
> – Navy SBIR **N211-001 / JNLWP**, still open FY-26  
>
> **“Operate autonomously in GPS- / RF-denied interiors”**  
> – Army DEVCOM OTA workshop minutes, Dec 2024  

*(Bold added.)*

---

### **2 · Current pain in confined combat spaces**

| Gap (cited) | Consequence today |
|-------------|------------------|
| **Blue-listed frames only do ISR** | Troops breach blind / lethal |
| **GPS & radios die in steel** | Loss of C2, lost soldiers |
| **No palm non-lethal at 3 m+** | Must escalate to lethal force |
| **Refresh cycle is months** | Unit-level hacks impossible |

Black Hornet films, Skydio maps, but **neither can relay comms *or* stop a threat**.

---

### **3 · DualEdge: one frame, many missions**

| Spec | Detail |
|------|--------|
| **Blue-clean frame** | 115 g duct quad · VOXL 2 Mini (Blue) · OAK-D Lite · TPM-signed SBOM |
| **Hot-swap rail** | 35 g payload · 30 s change-out · power + USB-C header |
| **v0 Pods** | **MeshPod-900** – 1 Mbps through 2 steel doors  <br>**StrobePod-S1** – 5 k-lumen flash + 118 dB siren (3 m) |
| **v1 Pods (Phase 2)** | **ChemSense-C8** gas sniffer  <br>**StingPod-L1** 1–2 kV contact shock |

*One palm drone ⇒ comms, map, & non-lethal in the same backpack.*

---

### **4 · Direct line to DoD wording**

| DoD bullet (slide 1) | **DualEdge** status |
|----------------------|---------------------|
| Blue-listed NDAA air-frames | ✔ VOXL 2 autopilot, US Li-Po, SBOM |
| Modular effectors | ✔ Rail + pods (Mesh, Strobe) |
| GPS-/RF-denied autonomy | ✔ VIO + UWB anchor; hover in steel stairwell |
| Non-lethal @ 3–5 m | ✔ StrobePod now · StingPod dev FY-26 |
| Ready-now / less-exquisite | ✔ \$750 BOM • print-to-flight < 72 h |

---

### **5 · Why incumbents can’t pivot**

|          | **DualEdge** | Skydio X2D | FLIR Black Hornet 3 | BRINC LEMUR 2 |
|----------|--------------|------------|--------------------|--------------|
| Unit cost | **\< \$3 K LRIP** | \$17 K | \$80 K | \$9 K |
| Hot-swap rail | **✔** | ✖ | ✖ | partial |
| Non-lethal pod | **✔ flash (shock dev)** | ✖ | ✖ | 40 mm drop-gas (heavy) |
| Mesh relay | **✔ 900 MHz** | add-on ($) | ✖ | Wi-Fi only |
| AI-to-Print loop | **Same-day frame** | Molded shell | Carbon lay-up | Molded |
| Open ROS-2 API | **✔** | closed | closed | closed |

**Cost + open rail** create a moat incumbents would need a ground-up redesign to match.

---

### **6 · AI-to-Print: hardware at software speed**

Prompt → generative CAD → Blue envelope check → HP MJF (5 h) → flight test  
*Hardware iteration cycle: **1 day vs 4 weeks** for molded rivals.*

---

### **7 · 6-month “ready-now” build plan**

| Month | Milestone | DoD value proved | Cash burn |
|-------|-----------|------------------|-----------|
| 0 | Design freeze · NDAA BOM | compliance gate | — |
| 1 | Hover Blue frame | air-frame ✔ | \$300 |
| 2 | StrobePod burn-in | non-lethal ✔ | 150 |
| 3 | Mesh relay through steel | modular comm ✔ | 100 |
| 4 | UWB-VIO nav in ship mock-up | GPS-deny ✔ | — |
| 5 | 90-sec demo + SBOM → DIU | Project G.I. packet | — |
| **Total** | 6 printed kits + video | **all 4 bullets met** | **≈ \$5 k** |

---

### **8 · Market & GTM**

| Phase | Target | Vehicle |
|-------|--------|---------|
| **I ’25-26** | DIU / SOCOM pilot kits | SBIR + Project G.I. OTA |
| **II ’26-27** | Replicator LRIP (thousands) | RCCTO / PEO Soldier |
| **III ’27-** | Campus & private security kits | EAR99 export, SaaS cloud |

1 % DoD small-UAS spend ⇒ **\$30 M** annual revenue.

---

### **9 · Funding ask**

**\$500 k SAFE @ \$6 M post**  

| Spend | \$ | 9-mo outcome |
|-------|----|--------------|
| Rail & frame run (20 units) | 160 k | pilot kits |
| Mesh & Strobe inventories | 120 k | DIU demo |
| StingPod & Chem R&D | 140 k | Phase 2 extras |
| Ops buffer | 80 k | runway |

*Non-dilutive in queue:* AFWERX SBIR \$75 k + Michigan match \$25 k.

---

### **10 · Team**

| | |
|---|---|
| **Fitz Doud** | ex-open-source autopilot maintainer · HW/FW |
| **Daniel Kalu** | Minerva CS · ROS 2 / SLAM / AI |
| **Advisors** | SOCOM CQB officer · Wayne State HV lab · ModalAI Blue lead |

---

### **11 · Why us, why now**

* **Exact DoD language, one product** — Blue + rail + indoor autonomy + 3 m non-lethal.  
* **AI-to-Print** out-iterates molded incumbents 10×.  
* **Attritable cost** \$750 vs \$17-80 K competitors.  
* **First-mover rail spec** becomes the Picatinny of palm drones.

---

### **Contact**

fitzdoud@gmail.com | dankalu.work@gmail.com  

*Palm-size, mission-ready. Let’s close the gap.*
