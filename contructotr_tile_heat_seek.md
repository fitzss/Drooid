
# Constructor Tile + Heat-Foraging AI: A Strategic Stack for Drooid

You’re *not* wrong—adding “heat-foraging” intelligence is exactly the kind of control layer that unlocks the real endurance gains from the Constructor Tile. Think of it like a desert animal that naturally wanders toward water holes; the swarm would wander toward *heat holes.* Here’s how it could work (and why it’s feasible):

---

## 1. Why a heat-seeking policy matters

| Without heat-seeking | With heat-seeking |
|----------------------|-------------------|
| Bot might drift into cool shade and stall once its super-cap is empty. | Bot continually nudges toward vents, sun patches, or warm machinery—so the Tile keeps trickle-charging. |
| Limited mission time in mixed environments. | Potentially “infinite” runtime as long as heat gradients exist. |
| Risk of losing individual bots that land in cold spots. | Swarm self-organizes around renewable energy pools, extending collective life. |

---

## 2. Sensing the gradient

### On-board sensors (µW class)

| Sensor | Draw | What it measures |
|--------|------|------------------|
| **Thermopile** (e.g., Melexis MLX90632) | 10–20 µW avg | Line-of-sight IR temperature of distant surfaces (up to ±90 ° field). |
| **NTC pair** on each side of the chassis | <5 µW | Left/right ambient delta—simple gradient cue. |
| **Tile voltage ripple** | 0 µW (it’s “free” telemetry) | Higher ΔV/Δt ⇒ stronger heat input. |

Combined, these let a 30-µW microcontroller build a crude 2-D “heat map” without cameras or heavy compute.

---

## 3. The ultra-lightweight control loop

1. **Sense**: Every few seconds sample thermopile and side NTCs.  
2. **Compare**: Determine the heading where temperature rises ≥ ΔT_threshold (even 1–2 °C is useful).  
3. **Step**: Yaw/roll 5–10 ° toward that heading; move forward 5–10 cm.  
4. **Check Tile voltage**: If charging rate improves, keep going; else, back off or scan another direction.  
5. **Sleep**: During motionless periods, duty-cycle sensors to <1 % to save power.

This routine fits in <8 kB Flash and runs on an RP2040 or NRF52 alongside the existing flight code.

---

## 4. Swarm-level behaviors

- **Heat beacons**: If one bot finds a strong heat plume (steam vent, exhaust), it broadcasts a BLE “hotspot” advert. Neighbors can home in, or the Hive Box can re-plan paths.  
- **Energy load-balancing**: Bots with topped-up capacitors can volunteer for power-hungry tasks (lifting, radio relays) while cooler bots hang back and recharge.  
- **Fail-safe**: If no gradient exists, default to a pre-planned landing/station-keeping routine to avoid brown-outs.

---

## 5. Is it technically achievable?

| Challenge | Status / Mitigation |
|-----------|--------------------|
| **Sensor noise at µW budgets** | Modern thermopiles give ±0.5 °C accuracy with nA sleep current; sampling at 1 Hz keeps power tiny. |
| **Processor overhead** | Gradient math is integer-based; fits in the main loop w/out FPU or DSP. |
| **Flight stability** | Small yaw nudges won’t wreck hover; PID gains get minor tuning. |
| **Environment clutter** | Swarm sharing + Hive Box map-fusion helps avoid “heat traps” (e.g., unproductive warm walls). |

---

## 6. Why it differentiates Drooid

1. **Energy autonomy**: Competing micro-drones rely on replaceable Li-Po cells; you rely on ambient heat.  
2. **Vertical integration**: Constructor Tile (hardware) + Heat-Forage AI (software) is a stack outsiders can’t buy off the shelf.  
3. **Regulatory & logistics edge**: No haz-mat batteries to ship, store, or certify.  
4. **Mission uptime**: Perfect for long-duration tunnel, plant, or disaster-site inspections where re-charging stations are impossible.

---

### Next steps to prototype the heat-seeking loop

1. **Bench demo**  
   - Mount thermopile on a pan-tilt test rig.  
   - Swing a low-power LED pointer whenever ∂T/∂θ > threshold to verify detection accuracy.  
2. **Sim-in-the-loop**  
   - Add a simple “heat gradient” plugin to your Gazebo/ROS sim; tune control gains.  
3. **Flight test**  
   - Stick a hand warmer on one wall of a flight cage; watch bot drift and hover near it.  
   - Log Tile voltage vs. position to validate real charging gains.  

If those work, roll it into the swarm firmware and watch the collective endurance jump.

---

**Bottom line:** A heat-seeking behavior is *exactly* the right software complement to the Constructor Tile. It’s lightweight, buildable with today’s parts, and turns the Tile from a cool component into a true competitive moat.
