# Powering Down the 12V System

*Generated from `27R_12V_Power_Down_Procedure.yaml` via `troubleshooting_doc.py` — edit that file, not this one.*

To store the coach or fully de-energize the house 12V system, follow the operator's manual's own documented procedure for this coach's specific battery option — not a generic AGM/lead-acid sequence, which is a different set of steps for a different option package.

**What you need:** access to inside the driver's door, access to the compartment behind the main entry door, access to the driver's side compartment behind the driver's door.

*The operator's manual documents two different 3-step procedures depending on which battery option the coach was built with. This coach has the lithium battery + BMS ("NeverDie" battery, Option 33W) — confirmed by the BMS power button documented on the battery itself elsewhere in this manual — so the 33W procedure below is the one that applies here, not the AGM/lead-acid version.*

---

## Part 1 — Which Procedure Applies to This Coach

Section 7 of the operator's manual has a dedicated "12 Volt Power On Procedure" and "12 Volt Power Off Procedure," each documented **twice** — once for Models 78G, 52D, and 52U (a conventional battery + breaker setup), and once for Model 33W (the lithium battery with BMS).

This coach has the lithium/BMS setup, so **Option 33W is the correct procedure** — Parts 2 and 4 below use the manual's exact 33W steps, not the 78G/52D/52U version.

**Do not mix the two.** The step order, component names ("BMS" vs. "battery," "disconnect" vs. "breaker"), and locations differ between the two documented procedures.

---

## Part 2 — Official 12V Power Off Procedure (Option 33W)

Verbatim from the operator's manual, Section 7, page 7-5 — follow in this exact order.

### ☐ 1. Turn off the coach disconnect

- Located inside the driver's door.

*Why this matters:* Step 1 of 3 in the manual's documented order for this coach's battery option.

### ☐ 2. Turn off the disconnect behind the main door

- Located in the compartment behind the main (entry) door.
- This is the same Battery Disconnect switch documented in the 12V Fuse and Breaker Panel Location guide, in the passenger-side compartment.

*Why this matters:* Step 2 of 3.

### ☐ 3. Turn off the BMS

- Located in the driver's side compartment behind the driver's door — this is the power button on the lithium battery itself. Press and hold until the LED indicator goes out.

*Why this matters:* Step 3 of 3 — this is what actually isolates the lithium cells and stops any remaining draw from the house battery.

---

## Part 3 — Before You Power Down: General Storage Prep

If this is for long-term storage rather than a quick shutdown, the manual's Vehicle Storage Preparation checklist (Section 12) calls out these steps first, before disconnecting anything:

**1.** Turn off the propane gas tank.

**2.** Turn the furnace thermostat OFF from the WinConnect Climate Control screen.

**3.** Remove food and odor-causing items from cabinets and the refrigerator; clean and defrost it, prop the door open slightly, and place an open box of baking soda inside.

**4.** Turn off the inverter — see the 2000W Inverter Operation guide for its physical disconnect switch and why leaving it on during storage will drain the house battery even with no AC load.

**5.** Fully charge the batteries before disconnecting — the manual specifies **at least 80% charge** to survive freezing temperatures and long periods of non-use. Connecting a charger or shore power once a month during long-term storage is recommended (but don't leave shoreline plugged in continuously).

Only after the batteries are charged should you run the Part 2 power-off procedure.

---

## Part 4 — If Long-Term Storage (2+ Weeks): Also Disconnect the Chassis Battery

This is separate from the house 12V system above — it's its own connector, on the chassis side.

### ☐ 1. Confirm ignition off and wait 10 minutes

- Ignition key in the Off position and removed.
- Wait at least 10 minutes before disconnecting, per the manual's own note — this lets chassis electronic modules go to sleep first.

*Why this matters:* Disconnecting too soon after key-off can be harder on chassis electronics than waiting the documented 10 minutes.

### ☐ 2. Unplug the Chassis Battery Connector

- Located to the right of the accelerator pedal, in the driver-side foot well, inside the access panel.

*Why this matters:* Winnebago recommends this specifically when the coach will be unoccupied for two weeks or more, to avoid chassis battery discharge — it's a separate recommendation from the house-battery power-off procedure in Part 2.

---

## Part 5 — Powering Back Up (Option 33W)

The manual's "12 Volt Power On Procedure" for Option 33W is the same three components in reverse order:

**1.** Turn on the BMS, located in the driver's side compartment behind the driver's door.

**2.** Turn on the disconnect, located in the compartment behind the main door.

**3.** Turn on the coach disconnect, located inside the driver's door.

If the chassis battery was also disconnected for long-term storage (Part 4), reconnect that connector first, before running the sequence above.

**To verify:** interior lights and the WinConnect touchscreen should power up normally once all three steps are complete. When powering the system down instead, the same displays going dark (and the lithium battery's status LED going out) confirms the shutdown actually took.

---

*Companion documents: 27R_12V_Fuse_and_Breaker_Panel_Location.md/.docx (Coach 12V Panel and the CZone digital switching system) | 27R_2000W_Inverter_Operation.md/.docx (inverter disconnect switch location and why it matters before storage)*