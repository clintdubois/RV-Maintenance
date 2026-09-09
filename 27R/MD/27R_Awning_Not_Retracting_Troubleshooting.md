# Awning Not Retracting: Troubleshooting

*Generated from `27R_Awning_Not_Retracting_Troubleshooting.yaml` via `troubleshooting_doc.py` — edit that file, not this one.*

The powered patio awning won't retract. Before assuming a motor or mechanical failure, work through the control paths and the coach-specific interlock first — they're the most common source of a "won't respond" complaint.

**What you need:** WinConnect touchscreen, phone with the awning's Bluetooth app (if paired), flashlight, Phillips screwdriver and a 13mm wrench (for manual retraction), a second person to watch the mechanism while you operate the switch.

*Pinch hazard — keep hands, pets, and objects clear of the arms and fabric any time you operate the awning, including during testing.*

---

## Part 1 — How This Awning Is Actually Controlled

Per our own Operations Guide and PDI checklist for this coach: this is a **powered patio awning with integrated LED lighting and Bluetooth**, operable from **three independent paths** — the WinConnect touchscreen, a physical wall switch, and a phone app over Bluetooth. That gives you a fast way to isolate the fault: if one control path fails but another works, the problem is in that specific control path, not the motor or mechanism.

On WinConnect: the Awning screen is reached from the menu icon. Each time you open it, you must read and accept the Awning safety page ("I understand") before the retract/extend/LED controls appear.

The base operator's manual does not name the awning's manufacturer and has no dedicated troubleshooting section for it — it defers to "the Awning manufacturer's user guide provided in your InfoCase" for complete operating instructions. **Confirmed from the nameplate on the awning box:** this is a **Girard GG750** (Lippert brand), 16' x 8' patio awning, 12VDC, motion-sensor-equipped. That identification is what makes Parts 3 and 4 below model-specific rather than generic.

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
- It moves a short distance (roughly 10-12 inches) and then stops → this is a specific, documented symptom — go to the next step before assuming a mechanical or motor fault.

*Why this matters:* This is the fastest way to split "electrical/control problem" from "mechanical problem" without opening anything up.

### ☐ 4. If it moves partway then stops: check house battery voltage — possible, not yet confirmed — **CHECK THIS**

- Girard's own troubleshooting guide for the GG750 documents this exact symptom: "The motor will operate for 10-12" and then stop... The motor may not be receiving enough power to operate correctly... Check to ensure that you have a minimum of 12VDC at the motor connection, if not switch on your generator or connect to shore power."
- Check house battery voltage on WinConnect. This coach's lithium battery documentation lists a normal resting/float voltage of about 13.6V — if the reading is noticeably below that (e.g. ~13.2V), there may not be enough headroom left once the motor's current draw (up to 10A) pulls the voltage down further under load, especially over the wire run to a roof-mounted motor.
- **Start the generator (or plug into shore power) and let it run for about 5 minutes to actually begin charging**, then retry retracting from the panel. This is a real fix Girard documents for this symptom, not a workaround — try it before escalating to Part 5.

*Why this matters:* This isn't confirmed as the cause on this coach yet — but it's a specific, documented match for the exact symptom (partial movement then stall), it's non-invasive, and it takes 5 minutes to rule in or out before opening anything up mechanically.

### ☐ 5. If it's silent: check WinConnect notifications and the Coach 12V Panel

- Open the WinConnect notification bell for any fault related to the awning, its sensor, or the RV-C/CZone network generally.
- Check the Coach 12V Panel (passenger-side compartment, under/near the passenger seat) for anything visibly tripped or abnormal — see the 12V Fuse and Breaker Panel Location guide for what's normally in there.
- Per Girard's own official troubleshooting for this exact model: also check the panel fuse on the 12VDC circuit feeding the awning, and check for a dedicated "Awnings Power Main Switch" if this coach has one — both are named directly in the manufacturer's guide as the first things to check for a motor that won't operate at all.

*Why this matters:* A silent motor with no response on any control path points at the power/control side, and these are the two places most likely to show it.

### ☐ 6. If it hums but doesn't move: inspect for a mechanical bind before forcing anything

- Check both arms and the roller tube for visible obstruction, debris, a bent arm, or fabric caught on something.
- Do not force the mechanism or keep holding the switch against a bind — that risks burning out the motor or bending an arm.

*Why this matters:* A strained-but-non-moving motor almost always means something physical is stopping it, not an electrical fault — forcing it turns a simple fix into an expensive one.

### ☐ 7. If a notification points at the motion/wind sensor specifically

- Inspect the sensor's own 2-wire connection for damage, corrosion, or a loose pin, separately from the motor wiring — it's a distinct circuit, not part of the motor pair.

*Why this matters:* Per Part 2, this sensor circuit is wired independently of the motor — a fault there is easy to overlook if you're only checking the motor wiring.

---

## Part 4 — Manual Retraction — Verified Girard GG750 Procedure

The coach's own operator's manual has no crank/override procedure for the awning — this comes directly from Girard's official GG750 Installation, Service and Repair Manual.

### ☐ 1. Know the limitation before you start — **IMPORTANT**

- The GG750's manual override is **one-way: it can only close (retract) the awning, not extend it.**
- The procedure differs by which side the motor is on — the manual shows a right-hand motor version; if this coach has a left-hand version, the override is on the opposite endcap from what's pictured.

*Why this matters:* Knowing it's retract-only and side-dependent up front avoids wasted effort looking for an extend override that doesn't exist, or opening the wrong end cap.

### ☐ 2. Remove the end cap opposite the motor

- Remove the 3 Phillips-head screws holding on the end cap on the side **opposite** the motor.

*Why this matters:* The override shaft is accessed from the non-motor end, not the motor end itself.

### ☐ 3. Turn the manual override shaft closed with a 13mm wrench

- Using a 13mm wrench on the exposed override shaft, turn it to close the awning (per Girard's Figure 10 in the official manual).

*Why this matters:* This is the verified, manufacturer-documented method for this exact model — not a generic RV-awning workaround.

---

##  — 

**If the motor won't operate at all** (the original symptom), Girard's own troubleshooting guide for this model says to check these two things before anything else, and gives a direct support line if they don't resolve it:

**1.** Check that the panel fuse on the 12VDC circuit is good.

**2.** If the coach has an "Awnings Power Main Switch," confirm it's in the ON position.

**3.** If that doesn't solve it, call the Girard Systems service line directly: **(949) 259-4000** or toll-free **(800) 382-8442**.

**Duty cycle warning from the manual:** to prevent motor overheating, don't exceed 4 minutes of continuous operation per hour — if you're testing repeatedly while troubleshooting, give the motor a rest between attempts rather than running it back-to-back.

Full source: **Girard GG750 Awning Installation, Service and Repair Manual** (Rev. 01/22/2020), saved locally as [Girard_GG750_Awning_Manual.pdf](../Girard_GG750_Awning_Manual.pdf), confirmed against the nameplate photographed on this coach's awning box ([Girard_GG750_Awning_Nameplate.JPG](../Girard_GG750_Awning_Nameplate.JPG)).

---

## Part 5 — When to Stop and Call for Help

A confirmed mechanical bind, a bent arm, or a motor that hums but won't move under load is a job for a dealer or RV service center — continuing to operate a jammed awning risks turning a repair into a full replacement.

If none of the three control paths get any response and the Coach 12V Panel looks normal, the Electronics Kit-Awning module or its RV-C/CZone connection is the next suspect — that's also dealer/technician territory rather than a DIY fix, since it sits on the same digital network as several other coach systems.

---

*Companion documents: 27R_12V_Fuse_and_Breaker_Panel_Location.md/.docx (Coach 12V Panel and the CZone digital switching system) | Wiring_Diagrams/README.md (full diagram index, including the awning's connector detail in Wiring_Diagram_12Volt.pdf and Body_12V_Wiring_Installation.pdf) | Girard_GG750_Awning_Manual.pdf (official manufacturer manual, saved locally in this folder)*