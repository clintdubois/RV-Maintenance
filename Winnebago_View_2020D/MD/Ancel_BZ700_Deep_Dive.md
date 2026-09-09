# Ancel BZ700 — Deep Dive

Companion to [Sprinter_OBD_Scanner_Review.md](Sprinter_OBD_Scanner_Review.md), where the BZ700 was the standout budget pick for this van's VS30/907 chassis (2019+). This digs into exactly what it does and doesn't cover.

## What it is

A dedicated Mercedes-Benz/Sprinter/Smart diagnostic scanner (not a generic multi-brand OBD2 reader) — Ancel builds it on Mercedes-specific firmware rather than a generic OBD2 protocol stack, which is why it can reach functions a universal scanner can't. It's a standalone handheld unit (2.8" TFT LCD screen), not a Bluetooth dongle requiring a phone — it plugs directly into the OBD2 port and runs on its own.

**Price**: $109.99–$129.99 depending on retailer/sale (Ancel's own site lists $129.99 regular / $109.99 sale).

## Vehicle coverage — the part that matters most for you, and where sources disagree

This is the one area where I want to be direct about conflicting information rather than smooth it over:

| Source | Coverage claim |
|---|---|
| Ancel's own product page | Mercedes-Benz (including Maybach) **1991–2021**; "ALL Sprinter models with 16PIN interface" |
| Ancel's own user manual | Same 1991–2021 range, with the explicit carve-out that **Sprinter models using a 38-pin diagnostic interface are NOT supported** |
| A third-party retail listing | Mercedes-Benz/Sprinter/Smart **2000–2020** specifically, stating "2020+ Mercedes are not supported" |
| Sprinter-Source.com owner forum thread (VS30-specific) | Confirmed working on the **907 model (2019+)** — no upper year limit stated by the poster |
| Real-world test report | Worked "perfectly" on a **2017 3.0L Sprinter RV engine** — that's the older NCV3 chassis, not your VS30/907 generation |

**What this means for your 2019 specifically**: every source that gives a cutoff either includes 2019 outright or doesn't exclude it — even the most conservative claim (2000–2020) covers your model year. The genuine uncertainty is about the *edges*: whether coverage extends past 2020/2021, and whether "supported" means full advanced-function access or just basic code reading on the newest model years. Your 2019 sits comfortably inside every range quoted, which is more assurance than most tools on the broader review list can offer.

### The connector caveat, explained

One real-world forum comment on Sprinter diagnostics generally is worth understanding: on some Sprinter model years, "a real scan can only be done via the 38-pin [connector] under the hood... newer cars can do everything via the [16-pin] OBD port." The BZ700 explicitly does **not** support the 38-pin interface. Practically:

- If your 2019 View relies solely on the standard 16-pin OBD2 port (under the dash) for the functions you need — which is standard for US-market Sprinters — the BZ700 should reach everything it claims to.
- If a specific advanced function on your exact chassis requires the 38-pin route instead, the BZ700 won't reach it, full stop, regardless of what year-range it claims.
- There's no way to resolve this from documentation alone — see the recommendation below.

**Ancel's own suggested fix for this uncertainty**: if you're not sure whether the BZ700 covers advanced features for your specific model, **send Ancel your VIN and ask them to confirm** before buying. This is literally what their own marketing material recommends for edge cases — take them up on it rather than guessing from spec sheets.

## Full function list

**Diagnostics** (reads across engine, airbag, transmission, ABS, SAS, SRS, EPB, DPF, DISA, DSC, SZL, TPMS, body, chassis, powertrain, and all control modules):
- Read/erase fault codes
- Freeze frame data
- Live data stream / real-time parameter monitoring
- Health report scan across all modules
- I/M readiness status
- EVAP system testing
- Vehicle info / Auto-VIN detection
- Battery voltage monitoring

**Reset/service functions** (16 total per the manual):
- **Battery registration** / BMS reset
- Oil service light reset
- ABS bleeding
- SAS (steering angle sensor) reset
- EPB (electronic parking brake) — brake pad replacement procedure
- TPMS reset/relearn
- ETC reset
- Transmission adaptation
- CKP (crankshaft position) reset
- Active test / actuation

**Diesel-specific** (relevant since your Sprinter is a diesel):
- DPF regeneration and adaptation
- AdBlue/DEF reset
- Injector coding/adjustment
- Fuel pump activation

## Hardware & practical details

- 2.8" TFT LCD screen, powered directly from the OBD2 port (no separate battery/charging to manage)
- 10 languages supported
- "Lifetime free updates" per Ancel
- Auto-VIN technology — identifies your exact model/year automatically rather than requiring manual menu selection (this was a specific complaint about the plain iCarsoft MB II in forum reports — having to manually pick sub-models is a common source of user error)

## Real-world performance notes

- One tester reported consistent connection, vehicle ID, and fault display within 3–4 seconds — described as faster than competing budget units in that same comparison.
- Reviewers describe the unit as well-built and reliable in day-to-day use.
- The 907/VS30-specific forum confirmation (Sprinter-Source.com) specifically named: code scanning, SRS clearing, the DPF regen button, and battery testing as working — this is the most directly relevant data point since it's from an actual owner on your exact chassis generation, not marketing copy.

## Bottom line for your 2019 View

- Your model year is inside every coverage range quoted by every source, including the most conservative one.
- The battery registration function you actually need is explicitly listed by Ancel (not just inferred), which is stronger footing than most of the alternatives in the broader review.
- The one real unknown is whether every advertised function reaches full depth via the 16-pin port on your specific chassis, or whether some deeper functions would need the 38-pin route this tool doesn't support.
- **Recommended before buying**: email Ancel support with your VIN and ask them to explicitly confirm battery registration support on your 2019 Sprinter 3500 (907/VS30 chassis). That converts this from "probably fine based on ranges" to an actual written confirmation for your exact vehicle.
