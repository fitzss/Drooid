
# How to Build the Prototype — Step-by-Step

## Step 1: Figure Out Your Power Target

Before building, you need to know:  
**How much power are you trying to make, and for what?**

Let’s say:  
- You want to power a tiny Bluetooth beacon that sends a signal every 10 seconds  
- It only needs about **5 microwatts (µW)** of average power

That’s like asking your tile to **sip a droplet of energy every few seconds** — and it should do that **forever**, just from heat.

**Why this matters:**  
If you don’t set this goal up front, you could waste weeks building something that doesn’t make enough power to do anything useful.

---

## Step 2: Buy Your First Energy Chip (Thermoelectric Generator)

This chip is like a **reverse fridge**: it turns a temperature difference (warm on one side, cold on the other) into electricity.

**Buy one online from:**  
- Micropelt  
- Ferrotec  
- Nextreme  

Look for a chip that’s about the size of your thumbnail (15 × 15 mm)

**Why this matters:**  
You’re not inventing a new material yet. You’re proving the concept works first with off-the-shelf parts.

---

## Step 3: Build a Heat Path

You need to keep one side of the chip warm, and the other side cool.

**How to do that:**  
- **Warm side:** Press a small copper piece against something warm (like your laptop vent or warm water)  
- **Cold side:** Use a plastic or printed fin to cool into the air  
- Use thermal pads (sticky heat sponges) between the metal and chip for clean heat transfer

**Why this matters:**  
No heat difference = no electricity. Even a few degrees (like your hand vs. air) can work — *but only if heat flows the right way*.

---

## Step 4: Make the Electronics Board

This board will:  
- Take the tiny voltage from your chip (way less than a battery)  
- Boost it to 3 volts (enough for Bluetooth or sensors)  
- Store it in a small **supercapacitor** (temporary battery)  
- Release energy every few seconds

**You’ll use:**  
- A **boost converter chip** (e.g., from ePeas or Atmosic)  
- A **supercapacitor**  
- A **connector** for Bluetooth chip or microcontroller

**Build and solder this at Newlab’s electronics station.**

**Why this matters:**  
Your heat chip gives tiny drips of power. This board turns those drips into **usable bursts** of energy.

---

## Step 5: Assemble and Test It

1. Attach your chip between the copper plate (hot) and plastic fin (cold)  
2. Wire it to the circuit board  
3. Place it on something warm (like a laptop or hot water)  
4. Use a **multimeter or LED** to check for power output

**Why this matters:**  
This is your **first real proof** that heat = power = action.

---

## Step 6: Make It Look Like a Real Product (Phase 2)

Once it works:  
- Use **Newlab’s 3D printers or CNC machines** to make a plastic shell  
- Mold it into a case you can hold, glue, or mount on a robot  
- Test it again in **real-world environments**

**Why this matters:**  
A working prototype is great—but a product people can *see and use* is what gets **partners, funding, and attention**.

---

## Step 7: Build an Advanced Version (Optional)

Once your first version works, level up:

- **Design your own tiny engine chip** (instead of buying one)  
- Use **University of Michigan’s cleanroom** (startups welcome)  
- You’ll make it smaller, stronger, and lower cost at scale

**Why this matters:**  
This version could power **robots, sensors, wearables** — and you could be **the first to sell** this kind of device.
