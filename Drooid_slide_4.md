---
marp: true
theme: default
backgroundColor: '#ffffff'
paginate: true
---

# **Drooid · Hive Swarm**  
*Blue-listed palm drones that** mesh, map & deter***  
Daniel Kalu | Fitz Doud · July 2025

---

### **1 · What DoD says it can’t get (verbatim)**

> **“Modular effectors in addition to sensors.”**  
> — DIU **Blue sUAS Block 4 RFI**, Apr 2025  
>
> **“Ready-now, less-exquisite sUAS that squads can adapt in weeks.”**  
> — DIU **Project G.I.** launch note, 2 Jun 2025  
>
> **“Compact, lightweight non-lethal payloads ... incapacitation at **3–5 m**.”**  
> — Navy SBIR **N211-001 / JNLWP**, FY-26  
>
> **“Operate autonomously in GPS- / RF-denied interiors.”**  
> — Army DEVCOM OTA minutes, Dec 2024  

Four bullets. Zero current systems hit all four.

---

### **2 · Hive in one slide**

| DoD must-have | **Hive spec** |
|---------------|---------------|
| **Blue / NDAA frame** | 115 g duct quad · VOXL 2 Mini · TPM-signed SBOM |
| **Indoor autonomy** | OAK-D depth + UWB — <10 cm drift in steel corridor |
| **30 s hot-swap rail** | 35 g payload · 5 V/12 V + USB-C header |
| **Attritable price** | **\$750** BOM proto → < \$3 k LRIP |

> *One palm drone → many missions.*

---

### **3 · How Hive satisfies every DoD bullet**

| DoD ask | Hive proof point |
|---------|-----------------|
| Blue / NDAA | Off-the-shelf VOXL 2 Mini (already on Blue list) + U.S. Li-Po |
| Modular effectors | Rail spec + pods swap with single Torx in 30 s |
| GPS-/RF-denied | Depth+UWB SLAM hover video (ship hold mock-up) |
| Non-lethal 3–5 m | StrobePod: 5 k lm flash + 118 dB siren (today); StingPod shock (FY-26) |
| Ready-now / low cost | AI-to-Print loop → frame CAD → flight same day; \$5 k demo budget |

---

### **4 · Pods now vs. next**

| Pod | TRL | What it delivers |
|-----|-----|------------------|
| **MeshPod-900** | ✔ | 1 Mbps relay through 2 steel walls |
| **StrobePod-S1** | ✔ | 3 m sensory stun; meets JNLWP pain-compliance spec |
| **ChemSense-C8** | ⚙ | CL₂ / NH₃ / H₂S sniff before entry |
| **StingPod-L1** | ⚙ | 1-2 kV contact-shock; JNLWP incapacitation target |

Rail stays the same; noses evolve like apps.

---

### **5 · Why incumbents can’t pivot**

|            | **Hive** | Skydio X2D | FLIR Black Hornet 3 | BRINC Lemur 2 |
|------------|----------|------------|--------------------|---------------|
| Unit cost  | **\< \$3 k** | \$17 k | \$80 k | \$9 k |
| Hot-swap rail | **✔** | ✖ | ✖ | partial |
| Mesh relay | **✔ 900 MHz** | add-on \$ | ✖ | Wi-Fi only |
| Non-lethal pod | **✔ flash (shock dev)** | ✖ | ✖ | 40 mm drop gas |
| AI-to-Print loop | **1-day** | Molded | Carbon lay-up | Molded |
| Open ROS-2 API | **✔** | closed | closed | closed |

Low cost + open rail = moat incumbents would need a ground-up redesign to copy.

---

### **6 · AI-to-Print loop**  
1 ️⃣ Prompt spec → generative CAD (3 min)  
2 ️⃣ Blue-envelope script + SBOM hash (30 s)  
3 ️⃣ Auto-slice → HP MJF print (5 h)  
4 ️⃣ Snap motors & VOXL (30 min)  
5 ️⃣ Hover test (< 10 cm drift)

Hardware iterations = **1 day** vs 4 weeks molded rivals.

---

### **7 · 6-month “ready-now” demo plan**

| Month | Deliverable | DoD value | Spend |
|-------|-------------|-----------|-------|
| 0 | Design freeze · Blue BOM | Compliance gate | — |
| 1 | Hover Blue frame | Air-frame ✔ | \$300 |
| 2 | 100-cycle Strobe burn | Non-lethal ✔ | 150 |
| 3 | Mesh relay test | Modular comm ✔ | 100 |
| 4 | UWB-VIO nav in steel stair | GPS-deny ✔ | — |
| 5 | 90-s video + SBOM to DIU | Project G.I. packet | — |
| **Total** | 6 kits + demo | All 4 bullets met | **≈ \$5 k** |

---

### **8 · Market & GTM**

| Phase | Target | Vehicle |
|-------|--------|---------|
| **I ’25-26** | DIU / SOCOM pilot | SBIR + Project G.I. OTA |
| **II ’26-27** | Replicator LRIP | RCCTO / PEO Soldier |
| **III ’27-** | Campus & private security | EAR99 kits + SaaS cloud |

1 % DoD small-UAS spend ⇒ **\$30 M** annual revenue.

---

### **9 · Funding ask**

**\$500 k SAFE @ \$6 M post**

| Use | \$ | 9-mo outcome |
|-----|----|--------------|
| Frames + rails (20) | 160 k | pilot kits |
| Mesh + Strobe parts | 120 k | DIU demo |
| StingPod + Chem R&D | 140 k | Phase-2 |
| Ops & runway | 80 k | 9 mo burn |

Non-dilutive filed: AFWERX SBIR \$75 k + MI match \$25 k.

---

### **10 · Team**

| | |
|---|---|
| **Fitz Doud** | ex-open-source autopilot maintainer · HW/FW |
| **Daniel Kalu** | Minerva CS · ROS 2 / SLAM / AI |
| **Advisors** | SOCOM CQB officer · Wayne State HV Lab · ModalAI Blue lead |

---

### **11 · Why invest now**

* DoD’s exact gap → **Hive** checks every bullet today.  
* **AI-to-Print loop** iterates hardware 10× faster.  
* \$750 attritable cost beats \$17-80 k incumbents.  
* **Open rail** spawns ecosystem — Drooid owns the socket.

---

### **Contact**

fitzdoud@gmail.com | dankalu.work@gmail.com  

*Palm-size, mission-ready. Let’s close the gap.*
