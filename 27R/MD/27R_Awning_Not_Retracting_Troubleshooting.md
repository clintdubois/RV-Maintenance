# Awning Not Retracting: Troubleshooting

*Generated from `27R_Awning_Not_Retracting_Troubleshooting.yaml` via `troubleshooting_doc.py` — edit that file, not this one.*

The powered patio awning won't retract. Before assuming a motor or mechanical failure, work through the control paths and the coach-specific interlock first — they're the most common source of a "won't respond" complaint.

**What you need:** WinConnect touchscreen, phone with the awning's Bluetooth app (if paired), flashlight, a second person to watch the mechanism while you operate the switch.

*Pinch hazard — keep hands, pets, and objects clear of the arms and fabric any time you operate the awning, including during testing.*

---

## Part 1 — How This Awning Is Actually Controlled

Per our own Operations Guide and PDI checklist for this coach: this is a **powered patio awning with integrated LED lighting and Bluetooth**, operable from **three independent paths** — the WinConnect touchscreen, a physical wall switch, and a phone app over Bluetooth. That gives you a fast way to isolate the fault: if one control path fails but another works, the problem is in that specific control path, not the motor or mechanism.

On WinConnect: the Awning screen is reached from the menu icon. Each time you open it, you must read and accept the Awning safety page ("I understand") before the retract/extend/LED controls appear.

The base operator's manual does not name the awning's manufacturer and has no dedicated troubleshooting section for it — it defers to "the Awning manufacturer's user guide provided in your InfoCase" for complete operating instructions, features, and maintenance care. Check there for anything beyond what's covered here, including any manual crank/override procedure in case of a motor failure.

**Ignition Lockout System** (documented in Section 13 of the operator's manual): the ignition lockout system disables the awning's extend function and retracts the awning when triggered. In other words, this coach is designed to force the awning closed around the vehicle's ignition state as a driving-safety measure — it isn't something that should ever *prevent* a retract. If the awning won't retract even with the ignition confirmed off, this system is not your cause; move on to Part 2.

---

## Part 2 — What's Actually Inside the Awning Circuit

Per the body wiring installation drawing, the awning runs through a dedicated **Electronics Kit-Awning** control module, connected into the coach's RV-C/CZone network via a 4-pin jumper — the same digital switching backbone documented in the [12V Fuse and Breaker Panel Location guide](27R_12V_Fuse_and_Breaker_Panel_Location.md).

The awning's own connector carries **6 conductors in 3 pairs** — this is the key fact most owners don't expect:

| Pair | Function |
|---|---|
| Motor +/− | Drives the awning arms in and out |
| Motion/wind sensor PWR/GND | Feeds an automatic wind-safety sensor — separate circuit from the motor |
| LED PWR/GND | Powers the awning's integrated lighting, independently switchable |

---

##  — 

That middle pair matters: this awning has a **motion/wind sensor** wired in parallel with the motor circuit, separate from it. Many powered awnings with this kind of sensor will refuse normal operation, or behave unpredictably, if that sensor circuit itself has a fault — even though the sensor's actual job is to auto-retract the awning in high wind, not to block a manual retract. If you've ruled out the motor and control paths and the awning still won't budge, this sensor circuit is worth inspecting next, not just the motor wiring.

---

## Part 3 — Diagnostic Steps

Work through in order — each step narrows down whether this is a control problem, a power problem, or a mechanical one.

### ☐ 1. Confirm ignition is truly off

- Key out, parked, engine off.

*Why this matters:* The coach's ignition lockout logic ties directly into this circuit (Part 1) — you want that variable eliminated before testing anything else.

### ☐ 2. Try all three control paths — **KEY STEP**

- Attempt retract from the WinConnect Awning screen, the physical wall switch, and the Bluetooth phone app, one at a time.
- Note exactly what happens (or doesn't) with each — silence, a hum with no movement, partial movement, an error/notification, etc.

*Why this matters:* If even one control path gets any response from the motor, the fault is upstream in the other two controls, not the motor or mechanism itself — this single test does more to narrow the problem than anything else here.

### ☐ 3. Listen closely when you press retract

- No sound at all from the awning motor area → suspect power, ground, a blown fuse/tripped breaker, or the Electronics Kit-Awning module itself.
- A motor hum or strain sound with no arm movement → suspect a mechanical bind, not electrical.

*Why this matters:* This is the fastest way to split "electrical/control problem" from "mechanical problem" without opening anything up.

### ☐ 4. If it's silent: check WinConnect notifications and the Coach 12V Panel

- Open the WinConnect notification bell for any fault related to the awning, its sensor, or the RV-C/CZone network generally.
- Check the Coach 12V Panel (passenger-side compartment, under/near the passenger seat) for anything visibly tripped or abnormal — see the 12V Fuse and Breaker Panel Location guide for what's normally in there.

*Why this matters:* A silent motor with no response on any control path points at the power/control side, and these are the two places most likely to show it.

### ☐ 5. If it hums but doesn't move: inspect for a mechanical bind before forcing anything

- Check both arms and the roller tube for visible obstruction, debris, a bent arm, or fabric caught on something.
- Do not force the mechanism or keep holding the switch against a bind — that risks burning out the motor or bending an arm.

*Why this matters:* A strained-but-non-moving motor almost always means something physical is stopping it, not an electrical fault — forcing it turns a simple fix into an expensive one.

### ☐ 6. If a notification points at the motion/wind sensor specifically

- Inspect the sensor's own 2-wire connection for damage, corrosion, or a loose pin, separately from the motor wiring — it's a distinct circuit, not part of the motor pair.

*Why this matters:* Per Part 2, this sensor circuit is wired independently of the motor — a fault there is easy to overlook if you're only checking the motor wiring.

---

## Part 4 — Manual Retraction — Confirmed Gap in This Coach's Documentation

Checked specifically: the operator's manual documents a manual/crank override for other powered components — the Power Roof Ventilator has a documented "Dome Crank knob" for use during a power failure, for example — but it has **no manual-retract or crank procedure for the awning anywhere in the manual or the wiring diagrams**. It only defers to "the Awning manufacturer's user guide provided in your InfoCase."

**Why there's no generic set of steps to give here:** manual-override mechanisms differ significantly by awning brand and model, and guessing wrong risks real damage or injury:

• Bluetooth-controlled awnings (Girard-style) often have **no crank at all** — releasing them manually means removing the motor housing and turning the drive shaft directly with a hex key/socket.

• Others (Solera, Carefree, Dometic) commonly have a small crank port or a manual-release lever built into the motor end.

• Some newer powered-only designs have **no field-serviceable manual override** and require a technician.

**Two ways to get the actual procedure for this awning:**

**1.** Check the InfoCase for the awning's own manufacturer's manual — it should be filed there separately from the coach operator's manual.

**2.** Look for a brand/model sticker on the motor housing (the tube-shaped part at the roof line where the arms pivot) and look up that model's manual override procedure directly, or provide the brand/model for a model-specific lookup.

**If it's currently stuck extended:** don't force the mechanism, and don't drive with it out. If wind or weather is a factor before you can resolve it, treat it as urgent — Winnebago roadside assistance or the nearest dealer is the safer path than improvising a release.

---

## Part 5 — When to Stop and Call for Help

A confirmed mechanical bind, a bent arm, or a motor that hums but won't move under load is a job for a dealer or RV service center — continuing to operate a jammed awning risks turning a repair into a full replacement.

If none of the three control paths get any response and the Coach 12V Panel looks normal, the Electronics Kit-Awning module or its RV-C/CZone connection is the next suspect — that's also dealer/technician territory rather than a DIY fix, since it sits on the same digital network as several other coach systems.

---

*Companion documents: 27R_12V_Fuse_and_Breaker_Panel_Location.md/.docx (Coach 12V Panel and the CZone digital switching system) | Wiring_Diagrams/README.md (full diagram index, including the awning's connector detail in Wiring_Diagram_12Volt.pdf and Body_12V_Wiring_Installation.pdf)*