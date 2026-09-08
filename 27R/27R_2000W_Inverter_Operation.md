# 2027 Winnebago View (27R) — 2000W Inverter/Charger Operation

**Source:** *2027 Winnebago View Operator's Manual*, Section 7 (Electrical) and Section 4 (Winnebago Connect), pages 7-6 through 7-8 and 4-6 through 4-7. Saved locally as [Winnebago_View_2027_Operator_Manual.pdf](Winnebago_View_2027_Operator_Manual.pdf) in this folder.

> The manual documents this as a factory option ("If Equipped") shared across View floorplans, including the 27R. It does not name the inverter/charger manufacturer or model number — that detail is only in the inverter manufacturer's own user guide, which should be in the coach's InfoCase (the binder of individual component manuals that ships with the vehicle). Check there before doing anything beyond basic on/off/monitor use (e.g. changing charger profiles, battery type settings).

## What It Is

- **2000-watt inverter/charger, pure sine wave.**
- Converts 12-volt DC from the house batteries into 120-volt AC for household outlets and appliances.
- Also functions as the shore-power **battery charger**: whenever the coach is connected to 120V shore power, it runs a 3-stage charge cycle on the house batteries (bulk → absorption → trickle/float).
- Has a built-in AC input circuit breaker and internal protections against overload/abnormal conditions.

## Where It Is

- The inverter/charger unit itself is behind a **passenger-side compartment door** (mid or front passenger side, depending on option package).
- A separate **inverter/charger disconnect switch** is also in the passenger-side compartment (near the unit).
- A **250-amp circuit breaker** sits next to the disconnect switch — it can fully isolate the coach battery from the rest of the coach electrical system.

## Operating It — Winnebago Connect ("WinConnect")

There is no physical on/off switch for daily use — the inverter is controlled through the coach's WinConnect touchscreen:

1. From the WinConnect home/menu screen, select **Energy Management** (battery icon).
2. The Energy Management screen shows, left to right: incoming power **Source** (shore/solar/generator), **Battery** status (charging/discharging, time to full/empty, % charge), and **Usage** (AC and DC draw).
3. **Inverter on/off control is at the bottom of this screen**, alongside a live readout of how much power is being drawn through it.

### Screen states to recognize

| Indicator | Meaning |
|---|---|
| Inverter off | No AC output from the inverter; only shore/generator power (if connected) reaches AC outlets |
| Inverter on, inactive | Enabled but no AC load currently pulling from it |
| Inverter on, normal use (**green** bar) | Actively supplying AC power to the coach |
| **AC pass-through** | Shore power is present; incoming AC is passed through to run appliances while the charger simultaneously charges the batteries |
| Load warning (**orange** bar) | Electrical load is approaching the inverter's power limit |
| Load shedding (**orange** bar) | Coach is automatically cutting non-essential loads to extend battery life during a power shortfall |
| Red alert | Demand exceeds supply, or battery reserves are critically low |

## When to Use It

- Intended for **short-term, limited use** when not on shore power or generator — e.g., running a microwave or coffee maker briefly while dry camping.
- **Not designed for sustained dry-camping use.** The house batteries will deplete quickly under continuous inverter load.
- Safe to run **while driving** — the engine's secondary alternator keeps the house batteries charged during that time.

## When to Turn It Off

- **Turn the inverter off when not actively using AC power from it.** If shore power is disconnected and the inverter/charger disconnect switch is left on, the inverter itself will slowly drain the house batteries even with no AC load — this is called out explicitly in the manual as a battery-drain risk during storage.
- Before extended storage: turn off the inverter/disconnect switch and **do not leave shore power connected during storage** — follow normal battery inspection/maintenance instead.

## Clearance & Heat

- The inverter generates heat while operating and needs unrestricted airflow. Don't stack or store items close around the unit in its compartment — the manual warns this can cause damage.

## Safety Warnings (from the manual)

- Do not use an extension cord with the shoreline power cord — improper/damaged cords or poor connections are a fire risk.
- Verify proper polarity and grounding before connecting shore power; ensure all prongs are fully seated.
- The 30A shoreline connection is rated for 110/125V AC, 60Hz, 30A — do not exceed circuit rating.

## Further Reading

- **WinConnect chapter** (Section 4) of the operator's manual — screen navigation and icon reference.
- **Inverter/charger manufacturer's user guide** in the coach's InfoCase — full explanation of the system, operating instructions, and charging setup/configuration (battery type, charge profiles, etc.) not covered in the Winnebago manual itself.
- **[Wiring Diagrams](Wiring_Diagrams/README.md)** — official Winnebago wiring diagrams for this coach (View 524R2). For tracing the inverter/battery circuit specifically, start with `Body_12V_Wiring_Installation.pdf`, `Wiring_Diagram_12Volt.pdf`, and the two `Battery_Installation` sheets.
