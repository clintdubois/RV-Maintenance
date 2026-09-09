# Isolating a Continuous 60W Parasitic Draw

*Generated from `27R_60W_Draw_Isolation_Checklist.yaml` via `troubleshooting_doc.py` — edit that file, not this one.*

Start with every switch believed OFF. This checklist confirms that's actually true, then reads the true baseline and isolates further if the draw remains.

**What you need:** WinConnect touchscreen (Energy Management screen), passenger-side compartment access, water heater exterior access panel, entry/galley walk-through.

*Several items below have a physical switch **and** a separate software toggle that can disagree with each other — that mismatch is the most common cause of an unexplained draw.*

---

## Part 1 — Confirm Everything Is Actually Off

Work through in order — each item lists both the physical check and the software confirmation.

### ☐ 1. Shore power and generator disconnected

- Shoreline power cord fully unplugged and coiled back into its compartment (driver's side).
- Generator confirmed OFF (WinConnect generator screen, plus listen/check for exhaust).

*Why this matters:* If shore power or the generator is live, you're not reading a true battery drain.

### ☐ 2. Inverter/charger disconnect switch — **TOP SUSPECT**

- Physical switch (passenger-side compartment, near the inverter/charger unit) is OFF.
- WinConnect → Energy Management screen also shows the inverter OFF (not just “on but inactive”).

*Why this matters:* This switch is separate from the software toggle. Left on while the app shows “off,” the inverter's standby electronics can keep drawing power — plausibly the full 60W by itself.

### ☐ 3. Water heater

- Physical switch behind the exterior access panel is OFF (green indicator light off).
- WinConnect → Water Systems screen confirms OFF — not just Economy mode (which still cycles the recirculation pump).

### ☐ 4. Tank heating pads

- WinConnect → Water Systems screen — pad toggle(s) confirmed off.

*Why this matters:* Thermostatically controlled — can silently re-engage in cold weather.

### ☐ 5. Refrigerator

- Control panel/thermostat fully OFF (not just turned down to “1” — that's still running).
- WinConnect Home screen (if it shows fridge status) agrees.

*Why this matters:* This is a 12V DC compressor refrigerator — draws directly off the house battery.

### ☐ 6. Winegard router / WiFi booster

- Dedicated power switch (separate from interior light switches) confirmed off.

*Why this matters:* Exact location isn't specified in the manual — check near the Winegard antenna control panel.

### ☐ 7. Interior lights and 12V accessories

- Walked the length of the coach — no interior/reading/accent lights lit.
- Any actively-charging USB devices unplugged from 12V USB outlets.

### Expected residual load — don't chase these

**Propane gas leak detector & CO detector** — always powered by design; should be well under 1–2W combined.

**CZone/RV-C control modules** (main switching module, coach management, Truma interface, lighting controller, solar charge controller) — stay powered whenever the master battery switch is on. Normal combined standby should be low single-digit watts.

---

## Part 2 — Read the True Baseline

With every Part 1 item confirmed off (master House/Coach Battery Disconnect switch still ON — you need this to read anything):

**1.** Open WinConnect → Energy Management screen.

**2.** Read the **Usage** value — this is your true “everything off” baseline.

| Reading | What it means |
|---|---|
| Near 0W | Found it — whichever item in Part 1 was actually still live (most likely the inverter disconnect switch mismatch) was the cause. |
| Still ~60W | The draw is coming from something not covered by a normal user-facing switch — continue to Part 3. |

---

## Part 3 — If the Draw Persists: Further Isolation

**1.** Re-confirm each Part 1 item once more — double-check the inverter disconnect switch especially.

**2.** Inspect the Coach 12V Panel (passenger-side compartment) for any breaker/fuse that looks tripped, warm, or abnormal. Do **not** pull the Coach Batt Fuse or Chassis Batt Fuse to “test” — that kills power to the monitor you're trying to read.

**3.** If nothing explains it: likely a stuck relay in a CZone/RV-C module, or a wiring short/chafe point.

**4.** Use the Wire Identification Chart and wiring diagrams to trace circuits with a multimeter/clamp meter, or contact a dealer/mobile RV electrician — a draw surviving every user-accessible off switch usually means a component-level fault.

---

*Companion documents: 27R_12V_Fuse_and_Breaker_Panel_Location.md/.docx (Coach 12V Panel contents and the CZone digital switching system) | 27R_2000W_Inverter_Operation.md/.docx (inverter operation and disconnect switch location)*