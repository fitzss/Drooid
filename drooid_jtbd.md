# Drooid Prototype #1: First Job to Be Done

**Job to build for first:**  
“Send a micro-swarm into tight, GPS-denied spaces (collapsed rooms, 4-inch pipes, drill holes) and return usable thermal video and location data within 5 minutes.”

---

## 1. Compute & Power Choices

| Requirement | Big-vendor default | Drooid choice | Why this matters for the job |
|-------------|--------------------|---------------|------------------------------|
| **On-board inference** | Jetson Nano/Orin (5 – 60 W, > $130) | RP2040 or STM32 MCU (80 mW) + 400 mW Edge-TPU or Himax tinyML | Keeps flyer under **250 g** with a **1 S Li-Po**, enabling 8–10 min flight in rubble or laterals. |
| **Heavy vision tasks** | Same module on every robot | **Hive Box** with 1 × Jetson Orin Nano (499 USD) | Centralizes SLAM and thermal mapping; each node only runs lightweight object/line following. |
| **Comms** | Wi-Fi 6E or proprietary mesh | Sub-GHz UWB + nRF BLE mesh | Penetrates concrete and metal better; packets hop bot-to-bot back to Hive. |
| **Cost per node** | $300 – $900 bill of materials | **$65 – $90** (motors, MCU, radio, sensors, frame) | A 5-robot kit lands under $600 parts, so loss of one unit is acceptable. |

---

## 2. Mechanical & Sensing Stack

| Module | Spec | Rationale for first job |
|--------|------|--------------------------|
| **Flyer arms** | CF-Nylon, 1-night print | Survive rubble impacts; printable spares in field. |
| **Crawler chassis** | Tough resin, 4 hrs print | Slides through 100 mm pipes; snap-fit tracks. |
| **Thermal + RGB sensor** | FLIR Lepton 3.5 + OV5640 | Thermal finds hotspots, RGB confirms survivor or crack. |
| **Gas / particulate** | SGP30 VOC + PM2.5 | Flags CO or dust levels before human entry. |
| **Navigation** | UWB anchors in Hive, IMU + optical-flow on bot | Gives 10–20 cm pose accuracy without GPS. |

---

## 3. Prototype Sprint Timeline (6 Weeks)

| Week | Deliverable | Key risk to tackle | “Definition of done” |
|------|-------------|--------------------|----------------------|
| 0–1 | Electronics bring-up | Edge-TPU + MCU SPI driver | 5 FPS person-box detection on bench at < 500 mW |
| 2 | Printable frame v1 | Weight creep | Flyer + battery ≤ 230 g, 6-min hover |
| 3 | Nested comms mesh | UWB LOS < 30 m, NLOS < 5 m | Packets hop through 2 walls with < 100 ms latency |
| 4 | Thermal + RGB fusion | Mis-align of sensors | 2 cm pixel-to-pixel alignment at 3 m |
| 5 | Swarm SLAM on Hive | Bandwidth overload | Three bots stream, Hive builds live map at 1 Hz |
| 6 | End-to-end demo | All above at once | 5-bot swarm finds heated mannequin in rubble cage, operator sees map + alert in < 5 min |

---

## 4. Why Incumbents Will Still Stand Aside

- **Cannibalisation** – A $600 five-robot kit ruins the business case for their $30k ground rover.  
- **Process mismatch** – They certify hardware for FCC/CE once a year; Drooid re-prints arms nightly.  
- **Value hurdle** – Public companies want $50M lines at 40% GM. Our first SAR niche is maybe $10M total with 15% GM—but it is *white space*.

---

## 5. Strategic Upside (for Nvidia too)

- **Drooid buys one Orin per swarm**—incremental demand Nvidia wouldn’t have captured.  
- **Edge-TPU, RP2040, open radios** build a stack Nvidia doesn’t bother with.  
- If Drooid swarms proliferate, **Nvidia sells more Hive boxes** and still owns the premium end; no conflict.

---

## Take-away for the Prototype Team

Build **what incumbents can’t**: ultra-light, throw-and-go robots optimized around a **sub-watt compute budget, printable parts, and a 5-minute lifesaving window**. Nail that single job; the gap stays wide open for Drooid to own.
