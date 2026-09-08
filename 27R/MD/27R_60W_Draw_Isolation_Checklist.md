# 27R — Isolating a Continuous 60W Parasitic Draw (Step-by-Step)

**Starting assumption:** every power switch you know of is already in the OFF position. This checklist first *confirms* that's actually true (several of these have a physical switch **and** a separate software toggle that can disagree with each other — that mismatch is the most likely cause of the draw), then walks through reading the true baseline and isolating further if the draw remains.

**What you need:** access to the WinConnect touchscreen (Energy Management screen), and physical access to the passenger-side compartment, water heater exterior access panel, and entry/galley area.

---

## Part 1 — Confirm Everything Is Actually Off

Go through these in order. For each, the check has two parts where applicable: the **physical switch position** and the **WinConnect confirmation** — don't skip the second part, since a switch can be flipped off while the device behind it is still electrically live if there's a second, separate control.

### ☐ 1. Shore power and generator disconnected
- Unplug the shoreline power cord completely from the outside receptacle; coil it back into its compartment (driver's side).
- Confirm the generator is not running (WinConnect → generator screen should show it off; also listen/check for exhaust).
- **Why first:** if shore power or the generator is live, you're not reading a true battery drain — you're reading something else. This has to be off before anything else is meaningful.

### ☐ 2. Inverter/charger disconnect switch — **the top suspect**
- Physical switch location: **passenger-side compartment**, near the inverter/charger unit itself (behind the mid or front passenger-side compartment door, depending on option package).
- Confirm the physical switch is in the OFF position.
- Separately, open WinConnect → **Energy Management** screen and confirm the inverter is shown OFF there too (not just "on but inactive").
- **Why this matters:** the inverter has its own on/off control in the touchscreen software *and* a separate physical disconnect switch. Turning it off in the app does not guarantee the physical switch is off, and vice versa. If the physical switch is on while the app shows "off," the inverter's internal standby electronics can still draw continuous power — a very plausible single source of ~60W by itself.

### ☐ 3. Water heater
- Physical switch: **behind the water heater access panel on the exterior** of the motorhome. Confirm it's pressed to OFF (both "on" positions on this switch do the same thing — either up or down can mean on, depending on the unit — check for the green indicator light, which should be OFF).
- Also confirm via WinConnect → Water Systems screen that the water heater shows off, not just set to Economy mode (Economy still runs the recirculation pump periodically; that's a real continuous-ish draw and not what we want for a clean baseline).

### ☐ 4. Tank heating pads
- WinConnect → **Water Systems screen** — confirm the tank heating pad toggle(s) are off. These are thermostatically controlled and can silently re-engage in cold weather even if you don't remember turning them on, so check them explicitly rather than assuming.

### ☐ 5. Refrigerator
- Confirm the refrigerator control panel/thermostat is switched off (not just turned down to setting "1"). This is a **12V DC compressor refrigerator** — it draws directly off the house battery, and "1" is still a running setting, not off.
- If WinConnect's Home screen shows a refrigerator status, confirm it agrees.

### ☐ 6. Winegard router / WiFi booster
- This has its own dedicated power switch per the coach wiring (separate from general interior light switches — easy to forget as part of "everything"). Confirm it's off.
- *Note:* the operator's manual doesn't give an exact physical location for this switch — check near the Winegard antenna control panel (commonly near the entry door or overhead near the dash). If you can't find it, flag that and we can dig into the wiring diagrams further.

### ☐ 7. Interior lights and 12V accessories
- Walk the length of the coach and confirm no interior lights, reading lamps, or accent lighting are lit.
- Unplug any USB devices actively charging from 12V USB outlets (phone chargers, etc.) — small individually, but worth ruling out.

### ☐ 8. Things that legitimately cannot be turned off (expect these, don't chase them)
- **Propane gas leak detector** and **CO detector** — always powered from the house battery by design. Manual explicitly notes these draw "a small amount of current" continuously. This should be well under 1–2W combined, not a meaningful contributor to 60W.
- **CZone/RV-C control modules** (main switching module, coach management module, Truma interface, lighting controller, solar charge controller) — these stay powered whenever the master coach battery switch is on, so they can listen for commands from the touchscreen and physical switches. Normal combined standby draw for these should be low single-digit watts.

---

## Part 2 — Read the True Baseline

With every item in Part 1 confirmed off (master House/Coach Battery Disconnect switch still ON — you need this on to read anything):

1. Open WinConnect → **Energy Management** screen.
2. Read the **Usage** value. This is your true "everything off" baseline.

**Interpreting the result:**
- **Near 0W:** you found it — whichever item in Part 1 you discovered was actually still on (most likely the inverter disconnect switch mismatch) was the cause. Leave it off going forward, or note it as something to check each time before storage.
- **Still showing ~60W:** the draw is coming from something not covered by a normal user-facing switch — proceed to Part 3.

---

## Part 3 — If the Draw Persists: Further Isolation

1. Re-confirm each item in Part 1 one more time — it's easy to miss one, and the inverter disconnect switch in particular is worth double-checking since it's the most likely culprit.
2. Check the **Coach 12V Panel** (passenger-side compartment, under/near the passenger seat) for any breaker or fuse that looks tripped, warm, or otherwise abnormal. Note: most of this panel is main supply protection (Coach Batt Fuse, Chassis Batt Fuse, slideout breaker, etc.) rather than individual branch circuits — do **not** pull the Coach Batt Fuse or Chassis Batt Fuse to "test," as that removes power to everything, including the monitor you're trying to read.
3. If nothing so far explains it, this points toward either:
   - A fault in one of the CZone/RV-C modules (e.g., a relay stuck closed, keeping something energized that should be off), or
   - A wiring short or chafe point somewhere in the coach harness.
4. At this point, use the [Wire Identification Chart](../Wiring_Diagrams/Wire_Identification_Chart.pdf) and [wiring diagrams](../Wiring_Diagrams/README.md) to trace individual circuit codes with a multimeter/clamp meter, or contact a dealer/mobile RV electrician — a persistent draw that survives every user-accessible off switch usually means a component-level fault rather than something you can toggle away.

---

*Companion documents: [27R_12V_Fuse_and_Breaker_Panel_Location.md](27R_12V_Fuse_and_Breaker_Panel_Location.md) (Coach 12V Panel contents and the CZone digital switching system), [27R_2000W_Inverter_Operation.md](27R_2000W_Inverter_Operation.md) (inverter operation and disconnect switch location).*
