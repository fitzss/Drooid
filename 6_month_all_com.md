# Drooid – 6-Month Prototype Budget & Milestones  
*Single-purpose ask: fund the very first working swarm.*

---

## 1. Complete Bill of Materials  
*(all lines shown exactly as specced; unit range = low ↔ high)*  

### Block 1 · **SWARM INTEL** (10 Micro ISR Drones / UGVs)

| Component | Spec | Unit $ | Qty | Sub-total |
|-----------|------|-------:|----:|----------:|
| Flight Controller | Pixhawk Mini / Matek H743 | 60–90 | 10 | 600 – 900 |
| Edge AI Processor | Pi 5 / Orin Nano / OAK-D Lite | 80–130 | 10 | 800 – 1 300 |
| IMU / GPS (opt.) | Ublox M9N + ICM-20948 | 20–40 | 10 | 200 – 400 |
| Comms Module | XBee SX 900 / nRF24L01+ HP | 30–70 | 10 | 300 – 700 |
| Frame / Chassis | CF-Nylon or ABS print | 5–20 | 10 | 50 – 200 |
| Battery Pack | 2 S Li-Po 1000 mAh / 18650 Li-ion | 10–15 | 10 | 100 – 150 |
| Sensors | OV5640 / OAK-D Lite / AMG8833 IR | 30–150 | 10 | 300 – 1 500 |
| Motors + ESCs | 1104/1106 + 4-in-1 ESC | 40–70 | 10 | 400 – 700 |
| Propellers | 3-4 in tri-blade | 2–4 | 10 | 20 – 40 |

### Block 2 · **CRAWLERS** (10 Adaptive-Terrain Units)

| Component | Spec | Unit $ | Qty | Sub-total |
|-----------|------|-------:|----:|----------:|
| Compute Core | Pi 5 / Jetson Nano / CM4 | 60–130 | 10 | 600 – 1 300 |
| Mobility Platform | Micro tracked chassis | 30–80 | 10 | 300 – 800 |
| Motors + Driver | Gear motor + L298N / dual H-bridge | 10–30 | 10 | 100 – 300 |
| Proximity Sensors | VL53L0X / ToF / Ultrasonic | 10–20 | 10 | 100 – 200 |
| Environmental Sensor | BME680 | 10–15 | 10 | 100 – 150 |
| Comms Module | LoRa / XBee / Wi-Fi mesh | 20–60 | 10 | 200 – 600 |
| Battery | 18650 pack / 3 S Li-ion | 10–15 | 10 | 100 – 150 |
| Camera / IR | OV2640 / USB cam | 10–25 | 10 | 100 – 250 |

### Block 3 · **JAMNET** (1 EW Micro Drone)

| Component | Spec | Unit $ | Qty | Sub-total |
|-----------|------|-------:|----:|----------:|
| Compute Core | Jetson Nano / LimeSDR Mini / HackRF One | 120–300 | 1 | 120 – 300 |
| RF Front-End | Tunable dir./omni antenna | 30–70 | 1 | 30 – 70 |
| Comms Module | Encrypted mesh (XBee / LoRa) | 20–60 | 1 | 20 – 60 |
| Frame | Lightweight drone frame | 10–20 | 1 | 10 – 20 |
| Power Supply | 3 S Li-Po 850–1300 mAh | 10–20 | 1 | 10 – 20 |
| Jamming SW | GNU Radio + scripts | Free | — | — |

### Block 4 · **HIVE MIND OPS** (1 Swarm AI Hub)

| Component | Spec | Unit $ | Qty | Sub-total |
|-----------|------|-------:|----:|----------:|
| AI Server | Jetson Xavier / x86 Mini PC | 300–1 000 | 1 | 300 – 1 000 |
| Local Comm Hub | Pi 5 + RF | 100–150 | 1 | 100 – 150 |
| LLM Framework | LLaMA.cpp / GGUF | Free | 1 | — |
| Battery | Portable power station | 300 | 1 | 300 |
| Software | ROS 2 + custom models | Free | — | — |

### Block 5 · **FLYER** (10 VTOL Recon Drones)

| Component | Spec | Unit $ | Qty | Sub-total |
|-----------|------|-------:|----:|----------:|
| Flight Controller | Kakute F7 / Pixhawk Mini | 60–90 | 10 | 600 – 900 |
| VTOL Mechanism | Tilt-rotor frame kit | 30–60 | 10 | 300 – 600 |
| Compute Core | Pi 5 / CM4 + cam | 80–100 | 10 | 800 – 1 000 |
| Camera + IR | Arducam + AMG8833 / Lepton | 30–80 | 10 | 300 – 800 |
| Obstacle Sensors | LiDAR-Lite v3 / ToF | 50–80 | 10 | 500 – 800 |
| Indoor Nav | Visual Odo / UWB | 50–150 | 10 | 500 – 1 500 |
| Qi Charging Rx/Tx | 20–40 | 10 | 200 – 400 |
| Battery | 3 S Li-Po 850–1300 mAh | 10–15 | 10 | 100 – 150 |

---

### Block-Level Low / High Totals  

| Block | Pattern | Low $ | High $ |
|------:|---------|------:|-------:|
| 1 – Swarm Intel | 9 lines × 10 u | 2 770 | 5 890 |
| 2 – Crawlers | 8 lines × 10 u | 1 600 | 3 750 |
| 3 – JamNet | 6 single-unit lines | 190 | 470 |
| 4 – Hive-Mind Ops | 5 single-unit lines | 700 | 1 450 |
| 5 – Flyer | 8 lines × 10 u | 3 300 | 6 150 |
| **Grand Hardware Range** |  | **\$8 560** | **\$17 710** |

We budget **\$13 k midpoint + 15 % buffer ≈ \$15 k** for hardware.

---

## 2. Non-Parts Spend (6 months)

| Item | \$ | Why it matters |
|------|---:|----------------|
| Newlab desks + resin & powder | 8 000 |
| AAIR corridor test slots (3) | 4 000 |
| Liability & drone insurance | 3 000 |
| Founders living allowance *(housing + food + misc, \$2.5 k × 2 × 6)* | 30 000 |
| Consumables / shipping | 3 000 |
| Contingency buffer | 5 000 |
| **Non-parts total** | **\$53 000** |

---

## 3. All-in 6-Month Spend  
Hardware \$15 000 + Ops/Living \$53 000 → **≈ \$68 k**

*(Rounded to \$70 k to stay safe.)*

---

## 4. Six-Month Milestones

| Month | Deliverable |
|------:|-------------|
| **1** | Funds clear • parts ordered • insurance bound |
| **2** | Frames printed • bench-test electronics |
| **3** | Indoor hover demo (Newlab cage) |
| **4** | GPS-denied nav test – AAIR slot #1 |
| **5** | Sensor-integration flight – AAIR slot #2 |
| **6** | 10-bot swarm demo video + telemetry packet |

Outcome: **working multi-domain swarm in < 180 days** for **≈ \$70 k**.

---

## 5. Upside & Reporting
- **DIU prize:** \$50–500 k possible inside 6 mo  
- **SPARK match:** reimburses up to \$100 k prototype spend  
- Quarterly e-mail: cash left • spend vs plan • next milestone  
- SAFE remains YC standard; this sheet is informational only.
