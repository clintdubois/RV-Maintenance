# House2Start Trickle Charger — Install Plan (2020 Winnebago View)

Purpose: keep the chassis/starter battery topped off from the house battery bank while parked/stored, so what just happened (chassis battery found dead at 3.5V, see [Winnebago_View_2020_Chassis_Battery_Replacement.md](Winnebago_View_2020_Chassis_Battery_Replacement.md)) doesn't recur from unmonitored drain.

## What it is

**House2Start** — a modern replacement for the discontinued Trik-L-Start. A small, permanently-installed **12V DC-DC trickle charger** that runs a true 4-stage charge profile (not a dumb float) to maintain the chassis/starter battery off the house bank. Compatible with Lead-Acid, AGM, or Lithium chemistries — relevant since you're going from an H6 to a proper H8 AGM on the chassis side.

- **Price**: $99
- **Amperage**: 2A charger — enough for maintenance/trickle duty, not a bulk charger
- **Size**: small form factor, fits tight spaces
- **Wiring**: pre-attached 18" yellow/blue/black wires simplify connection to the target device

## Where it installs on this vehicle: the Mastervolt Chargemate

House2Start explicitly calls this out as the **easiest installation point** for this exact vehicle type — *"installed in most 2020+ Winnebago Navion/View/Era (Mercedes chassis) motorhomes"* — which is this 2020 View.

- **Location**: Mastervolt Chargemate, **under the passenger seat**
- The Chargemate is a current-limiting battery combiner — House2Start connects directly onto its power lugs that lead to the house and starter batteries, rather than needing a separate wiring run to each battery.

## Generation-specific requirement — check before wiring

- **Gen2b**: requires installing the **included diode on the blue wire** when connecting to a Mastervolt Chargemate.
- **Gen2c or later** (anything shipped after Dec 22, 2025): diode requirement was **eliminated** for Chargemate installs.
- **Check the sticker on the unit itself** to confirm which generation you actually received before assuming either way — don't guess from order date alone.

## Install steps

1. **Locate the Mastervolt Chargemate** under the passenger seat.
2. **Identify the power lugs** on the Chargemate connected to the house battery bank and to the starter/chassis battery.
3. **Verify with a multimeter** before connecting anything — House2Start's own installation guide recommends measuring voltage at the actual battery terminals first, then cross-checking against the Chargemate's connection points, rather than trusting lug labeling alone.
4. **Check the House2Start unit's generation sticker** (2b vs. 2c+) to determine whether the diode step applies.
5. If Gen2b: **install the included diode on the blue wire** per the unit's documentation before making the final connection.
6. **Connect the pre-attached yellow/blue/black wires** to the corresponding Chargemate lugs (house+, starter+, ground) per the House2Start manual.
7. **Mount the unit securely** in the available space near the Chargemate — small form factor, but still secure it so it can't vibrate loose or contact anything it shouldn't.

## After install

- Confirm the chassis battery's state of charge trends upward/holds steady over a period of parked/unplugged time (a few days) rather than drifting back down — this is the actual proof the unit is doing its job.
- Since this runs off the house bank, keep an eye on house battery state of charge too if boondocking for extended periods — a 2A draw is small but not zero.

## Sources / open questions

Compiled from house2start.com (product page, installation guide, FAQ) and a Sportsmobile/Winnebago Revel Forum reference confirming the Mastervolt Chargemate as standard equipment on 2020+ View/Navion/Era. **Not confirmed**: the underlying electrical reason the diode is needed on Gen2b units specifically — House2Start's public documentation states the requirement without explaining the rationale. Worth asking House2Start support directly if you want that detail before wiring it in, rather than guessing.
