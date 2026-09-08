# 2019 Sprinter Chassis — Charger Cycling & Wipers Activating: Troubleshooting Notes

Symptom observed: connecting a 6A battery charger causes the windshield wipers to activate on their own, and the charger goes to full load for ~30 seconds, then cuts off, then comes back on — repeating.

## Update: the installed battery is an H6, not the H8 this Sprinter needs

On inspection, the currently installed battery is a **Group 48/H6**, while this Sprinter is specced for **Group 49/H8** (see [Winnebago_View_2020_Chassis_Battery_Replacement.md → H8 vs. H6](Winnebago_View_2020_Chassis_Battery_Replacement.md#h8-vs-h6--can-they-interchange)). This is now the **leading suspect** for the symptoms above, ahead of the SAM/ground-strap theory below — a genuinely simpler and more likely explanation.

H8 is about 2.9" longer than H6 (same width/height). Fitting an H6 into an H8 tray needs a mounting bracket/spacer to take up that extra length and let the factory hold-down clamp actually grip the case.

**Confirmed: a ~3" bracket is present and holding the battery in place.** That rules out the simplest version of this theory (battery just loose in an oversized tray). Two things still worth a quick check before moving on:

- **Is the bracket actually snug**, or does the battery have any wiggle when you push on it? A bracket that's present but not fully tightened can still allow enough movement to cause an intermittent connection under load.
- **Do the terminal cables reach without strain**, or are they extended/spliced to bridge the gap? A marginal splice or a taut cable can be a connection point that only fails under the higher current a charger pushes, even with the case itself mechanically secure.

If both of those check out fine, the mounting angle is likely resolved, and the isolation test in Step 3 below becomes the key next move — it separates "the battery itself is genuinely bad" (possible after however long it's been running mismatched against this Sprinter's H8-spec charging system) from "it's a SAM/ground-strap issue" as covered further down.

## What the SAM module is

**SAM = Signal Acquisition Module** (sometimes called Signal Acquisition *and Actuation* Module). Mercedes has used them since the mid-90s, and most Mercedes vehicles have 4–5 of them. Think of it as a network router for the vehicle's electrical system: it receives input from switches, sensors, and controllers, and sends output to actuate components (lights, wipers, locks, etc.) — replacing what would otherwise be hundreds of discrete point-to-point wires with a shared data network. When you press a switch, the signal passes through a SAM before the component responds. A fault in a SAM (rather than in the component itself) is why symptoms often look scattered and unrelated — wipers, lights, locks, warning messages — because they all route through the same module.

**Location on the Sprinter**: the front SAM sits near the base of the **passenger-side A-pillar**, low in that footwell/kick-panel area — this is also the spot SprinterRVDesk specifically flags as a moisture-intrusion point (water entering via the A-pillar or windshield seal corrodes the SAM's connectors over time). Since this Sprinter is under an RV conversion, trim panels may cover direct access — treat this as the area to start with, not necessarily a panel you can pop off in two minutes; confirm exact access against the Sprinter service manual (WIS) or have a tech locate it if it's not obviously reachable.

## Most likely explanation

Applying a charger pushes more current through the system than normal resting draw. A SAM connector or ground strap that "mostly works" under light load can glitch or trip under that extra current — which would explain both the wipers activating (a SAM/CAN-bus glitch triggered by the current) and the charger cycling off every ~30 seconds (its protection circuit reacting to the fault it's seeing through that same bad connection).

**Ground strap corrosion** is the other half of this: every electrical circuit in the van returns current through the ground straps (engine-to-frame, battery negative-to-chassis, chassis-to-body). A corroded strap adds resistance to that shared return path, which can produce simultaneous, seemingly unrelated symptoms — hard starting, alternator warnings, random check-engine lights, instrument cluster malfunctions — alongside exactly the kind of wiper/charger behavior described here.

## Diagnostic sequence (free, ~90 minutes, before buying any parts)

1. Inspect all ground connections — engine-to-frame, battery negative-to-chassis, chassis-to-body. Clean to bare metal with a wire brush, apply dielectric grease. Replace the strap ($15–25) if corroded or frayed.
2. Check the SAM module's connectors for corrosion (the A-pillar moisture-entry point above) — clean with electrical contact cleaner and a brass brush, reapply dielectric grease.
3. Check the fuse box's rear connectors for corrosion — another known weak point.
4. Audit any aftermarket/RV-conversion wiring for taps or splices near these areas.
5. Inspect the sliding door harness boots.
6. Read fault codes with a Mercedes-compatible scan tool if the above doesn't resolve it — see [Sprinter_OBD_Scanner_Review.md](Sprinter_OBD_Scanner_Review.md).

## Check the charging connection point

VS30 Sprinter owners note the correct chassis-battery charging point is the **under-hood jump-start posts**, not the AGM battery terminals directly under the driver's seat. If the charger is currently clamped onto the battery itself rather than the under-hood posts, that's worth changing — and if there's corrosion specifically at the under-hood posts (which route back to the actual battery), that alone could be contributing to what's being seen.

## Don't rule out a genuinely bad battery

A charger cycling off repeatedly is also just standard protective behavior when it detects a bad or shorted cell — independent of any SAM/ground-strap issue. If the battery itself is the root cause, the electrical troubleshooting above would be a wasted detour, and the [replacement plan](Winnebago_View_2020_Chassis_Battery_Replacement.md) is the more direct path. The steps below triage the battery in place to figure out which one you're actually dealing with.

## Triage steps — battery in place

### 1. Visual inspection first (2 minutes, no tools beyond your eyes)

- **Case**: any bulging, swelling, or distortion? AGM batteries that have been overcharged or overheated swell — a swollen case is a bad battery, full stop, don't bother testing further.
- **Terminals**: corrosion (white/greenish crust), looseness, or visible damage at the post or clamp.
- **Leaking/weeping**: AGM is sealed and shouldn't leak; any moisture around the case seams is a bad sign.
- **Date code**: check the label for a manufacture date — helps you judge whether "just genuinely worn out" is plausible given the vehicle's age.

If the case is swollen or leaking, stop here — replace it, no further testing needed.

### 2. Resting voltage (multimeter, no charger or load connected for at least 1–2 hours first)

With the battery sitting untouched — charger and any vehicle load off it — read voltage across the terminals:

| Reading | Interpretation |
|---|---|
| ~12.6–12.8V | Fully charged, healthy |
| ~12.2–12.4V | Partially discharged — normal-ish, not a red flag alone |
| ~11.5–12.0V | Significantly discharged |
| ~10.5V or lower | Strong indicator of a shorted/dead cell — a 12V AGM has 6 cells at ~2.1V each, so losing one cell drops total voltage by roughly that much |

A reading in the ~10.5V range essentially confirms a bad cell on its own, independent of anything else below.

### 3. The decisive test — isolate the battery from the vehicle entirely

This is the single test that tells you which theory (bad battery vs. vehicle wiring/SAM fault) is correct, and it needs no special tools beyond what you already have.

1. **Fully disconnect the battery from the vehicle** — negative terminal first, then positive (standard safety order) — and move it a few inches clear of the vehicle's cables so there's no chance of accidental contact.
2. Connect your 6A charger **directly to the isolated battery only**, with nothing else attached.
3. Watch what the charger does:
   - **If it still cycles on/off every ~30 seconds with the battery completely isolated** → the fault is *inside the battery* (a bad/shorted cell). The vehicle wiring and SAM module are not involved. Skip the SAM/ground-strap diagnostics entirely and go straight to the [replacement plan](Winnebago_View_2020_Chassis_Battery_Replacement.md).
   - **If it charges normally/steadily once isolated** (no cycling) → the battery itself is fine, and the cycling + wiper activation only happens when connected to the vehicle. That confirms the SAM/ground-strap/wiring explanation above — proceed with the diagnostic sequence in that section instead, and hold off on replacing the battery.

(Note: wipers obviously can't activate while the battery is disconnected from the vehicle — that part of the symptom is expected to disappear during this test regardless. The charger's cycling behavior in isolation is the data point that matters here.)

### 4. If the isolation test points to a bad battery, confirm with a load test if you have the means

A battery can read an acceptable resting voltage but still collapse under real load if a cell has failing capacity rather than a hard short. If you have a load tester (or a charger with a test function), a healthy 12V battery should hold above ~9.6V for 15 seconds at its rated CCA per the standard SAE test. A battery that reads fine at rest but drops well below that under load confirms the cell is failing even without a dead-short symptom.

### 5. If the battery tests fine, clean before reconnecting

Before reconnecting a battery that passed isolation testing, clean the terminal posts and the vehicle-side cable clamps (wire brush + dielectric grease) — corrosion right at that connection point can itself cause exactly this symptom pattern and is worth ruling out before moving on to the SAM module deeper in the wiring.

## Sources

SprinterRVDesk ("Mercedes Sprinter Wiring Problems: Ground Straps, SAM Faults, and the Gremlins That Fool Everyone"), Class B Forums (VS30 coach battery maintenance thread — charging connection point), MercedesMedic and BenzWorld forum threads (SAM module function and location), general battery-charger troubleshooting sources (cycling behavior with a bad/shorted cell). A directly on-point sprinter-source.com thread ("Wipers will not turn off") was found but not accessible to fetch — worth checking directly for another data point from other 907/VS30 owners.
