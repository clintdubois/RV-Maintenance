# 2020 Winnebago View — Chassis Battery Replacement Plan

Vehicle: 2019 Mercedes-Benz Sprinter 3500 chassis (under the 2020 Winnebago View coach) — the "907" generation Sprinter, first model year 2019. This is the **chassis/starter battery** (engine start, dash electronics), separate from the coach/house battery system.

## Status / To-do

- [x] New H8 battery installed
- [x] Register the new battery — confirmed working via Ancel BZ700, see Section 6
- [ ] **Install genuine OEM hold-down clamp (906-541-04-00) once it arrives** — expected Tuesday
- [ ] **Install House2Start trickle charger** on the Mastervolt Chargemate, under the passenger seat — see [House2Start_Trickle_Charger_Install.md](House2Start_Trickle_Charger_Install.md)

## Battery spec

**OEM:** Mercedes-Benz genuine part **001-982-82-08-26** (covers 2018–2025 Sprinter) — 12V, ~92–95Ah, AGM, BCI Group 49/H8.

| Option | Spec | Dimensions | Weight | Terminal | Price (approx) | Review check |
|---|---|---|---|---|---|---|
| **Odyssey Performance Series ODP-AGM49H8L5 (49-950)** — premium pick | 12V, 950 CCA, 1,700 PCA, 180 min reserve, Group 49/H8 AGM | 13.9" × 6.9" × 7.5" | 62.8 lb | SAE | ~$399 | **Strong** — 4.8/5 on AutoZone, no meaningful complaint pattern found |
| **WEIZE Platinum AGM, Group 49/H8** — budget pick, purpose-marketed for Sprinter vans | 12V, 95Ah, 900 CCA, 160 min reserve | 13.9" × 6.89" × 7.48" | 56.4 lb | Type A | ~$170–240 | **Caution** — real reports of case swelling and early failure, plus weak after-sales/warranty support experiences. Still usable at this price if you're comfortable with that risk, but don't expect fast warranty service if it fails |
| **Interstate MTX-49/H8** (Costco / Interstate All Battery Center) | 12V, 95Ah, 900 CCA | Standard Group 49/H8 | ~56 lb | Varies | ~$170–178 | **Mixed, leans OK** — one long-time Interstate customer reported multiple shorted-cell failures across several batteries, but nothing at the scale of a controlled lab test; backed by a 36-month free replacement warranty, which mitigates the risk |

Both Odyssey and WEIZE match the OEM tray dimensions. Confirm terminal orientation against the old battery before ordering — SAE vs. Type A terminal style should match what's currently installed, or you'll need adapters.

**Removed from consideration: Duralast Platinum H8-AGM (AutoZone's house brand)** — Consumer Reports' own controlled life test found Duralast Platinum AGM batteries (Group 48, same product line) failing in **3, 5, 6, and 7 weeks**, and performing worse than cheap conventional lead-acid batteries in that same test. Couldn't confirm the H8/49 size was tested specifically (paywalled), but it's the same manufacturing line — not worth the risk given how much better the Odyssey option tested. If you're at AutoZone anyway, **ask for the Odyssey ODP-AGM49H8L5 instead** — they carry it too.

**Must be AGM** — the 907 Sprinter's Start-Stop system and intelligent battery sensor (IBS) require it; a standard flooded lead-acid battery is not a safe substitute here.

### H8 vs. H6 — can they interchange?

Worth understanding since H6/Group 48 batteries are more common and often cheaper/easier to find than H8/Group 49 — you may see H6 options while shopping and wonder if they'd work.

| | H6 (Group 48) | H8 (Group 49) — what this Sprinter needs |
|---|---|---|
| Dimensions | 11" × 6.9" × 7.5" (278 × 175 × 190mm) | 13.9" × 6.9" × 7.5" (354 × 175 × 190mm) |
| Capacity | ~60–72 Ah | ~80–95 Ah |
| CCA | ~720–800 | ~850–950+ |
| Reserve capacity | ~120–140 min | ~150–180 min |

**Same width and height, different length.** H6, H7, and H8 all share identical width and height in the DIN "Group H" battery family — length is the only dimension that changes as you go up the range, and H8 is about **2.9" (76mm) longer** than H6. Terminal layout (positive on the right) is the same general pattern, but the length difference shifts exact terminal position, so cables sized for one won't necessarily reach comfortably on the other without slack.

**Can you put an H6 in this Sprinter's H8 tray?** Physically, yes — the tray has room since H6 is smaller in every dimension except it's shorter. But it's not a drop-in swap:

- **You'll need a mounting bracket/spacer** to take up the ~3" of extra tray length and keep the smaller case from shifting — this is a real, sold product (e.g. an aftermarket H8-to-H6 adapter bracket, CNC-machined aluminum, ~$65) rather than something you're improvising. Confirm Sprinter-specific fitment before buying one, since most of these are marketed toward GM/other applications, not Sprinter vans specifically.
- **The factory hold-down clamp likely won't cinch down properly** on a shorter case without that bracket — don't skip this and rely on the clamp alone.
- **Terminal cables may need to be different length or gain a short extension**, since the terminals sit closer to the tray's front edge on a shorter battery.

**Can you put an H8 in an H6-sized tray?** Generally no — H8 is physically longer, so it won't fit in the smaller footprint without tray modification. Not a realistic path.

**Should you actually downsize to H6 here?** No — Mercedes specced H8/Group 49 for this Sprinter's electrical demands (Start-Stop cycling, accessory load, cold cranking) for a reason. An H6 has meaningfully less CCA and reserve capacity than what the vehicle was designed around, even though it would physically fit with the right bracket. Stick with H8 for the actual replacement; the interchange info above is useful to know but isn't a reason to downsize.

**Real-world note**: this specific vehicle was found with an H6 installed instead of the correct H8, held in with an aftermarket 3" spacer bracket. That confirms the OEM tray itself is genuinely H8-sized — the spacer was compensating for the undersized battery, not the other way around. Once the correct H8 is installed, that aftermarket spacer is no longer needed; use the genuine OEM hold-down clamp below instead.

### OEM battery hold-down bracket — genuine part, no need to 3D print

Genuine Mercedes-Benz part confirmed to fit this exact vehicle — buy this rather than fabricating anything, given how cheap it is relative to a structural clamp holding down a ~55–65 lb battery under constant vehicle vibration.

- **Part number**: 906-541-04-00 (also written A9065410400) — described as "Hold Down" in Mercedes' own catalog
- **Confirmed fitment**: 2019–2025 Sprinter 3500 (2.0L/2.1L and 3.0L diesel), also covers Sprinter 2500 and 1500 across 2014–2025
- **Price**: ~$11.59–$16
- **Where to buy**: [mbpartsgiant.com](https://www.mbpartsgiant.com/genuine/mercedes-benz~bracket~9065410400) ($11.59, genuine, 12-month/12,000-mile warranty, ships 1–2 business days) or the standard (non-classic) `mbparts.mbusa.com` Mercedes-Benz USA parts site ($16.00). **Not available on Amazon** as of this research — don't waste time searching there. **Avoid `classicparts.mbusa.com`** even though the part number shows up there too — that storefront is scoped to 1954–2006 vintage vehicles and isn't the right channel for a 2019, even if their catalog happens to surface the same part number.

Before ordering: check whether the original factory bracket is still present at the H8-sized tray position (separate from the aftermarket H6 spacer) — it may just need reuse rather than replacement.

### Where to buy locally (Seattle area)

| Source | Location | Notes |
|---|---|---|
| **Costco — Issaquah** | 1801 10th Ave NW, Issaquah, WA 98027 (Tire & Battery Center, appointments via costcotireappointments.com) | Interstate H8 AGM (Group 49), ~$169.99–$177.99 + ~$15 core charge, 3-yr warranty, made in Germany. A Sprinter owner on sprinter-source.com confirmed buying this exact battery and it worked. **Availability is inconsistent** — call ahead to confirm current stock before driving over. Closest/most convenient option to home. Review check: mixed-but-OK, see battery spec table above. |
| **Batteries Plus — Bellevue** | 14917 NE 20th St, Bellevue, WA 98007 — (425) 562-5000 | Battery specialist, likely to have Group 49/H8 AGM in stock rather than special-order |
| **Batteries Plus — Seattle/Northgate** | 536 NE Northgate Way, Seattle, WA 98125 — (206) 364-0446 | Fallback if Bellevue is out of stock |
| **Interstate All Battery Center — Kent** | 19033 68th Ave S, Suite D-104, Kent, WA 98032 | Interstate's own MTX-49/H8 AGM (900 CCA/95Ah), same review profile as the Costco option above |
| **Mercedes-Benz of Seattle Sprinter** | 2025 Airport Way South, Seattle, WA 98134 — (206) 489-1935 | OEM part (001-982-82-08-26), guaranteed fit, likely priciest option |
| **Mercedes-Benz of Tacoma (Larson Mercedes)** | 1701 Alexander Ave E, Fife, WA 98424 — (253) 778-7325 | OEM fallback if Seattle doesn't have stock |
| **AutoZone** | Multiple Seattle-area locations | Carries **both** Duralast Platinum H8-AGM and Odyssey ODP-AGM49H8L5 — **ask for the Odyssey specifically**; skip the Duralast (see review flag above) |
| O'Reilly / NAPA | Multiple Seattle-area locations | Typically carry or can order Group 49/H8 AGM — call ahead, this size is often special-order rather than on-shelf; confirm brand/model before committing |

**Recommended order to try**: Costco Issaquah first (closest, competitive price) → Batteries Plus Bellevue → Interstate All Battery Center Kent → Mercedes dealer as the guaranteed-fit fallback.

**Costco does not install batteries, under any circumstances** — purchase is warehouse-only, self-install or bring it to a mechanic. This isn't just a convenience note: even in documented cases elsewhere where an AGM battery ended up installed without registration, no BMS/ECU registration or adaptive-charging reset was performed. One real-world case: an unregistered AGM installation led to the vehicle not holding idle, throwing a "Battery Monitoring System Invalid" code, and draining overnight — the fix cost **$147 in diagnostic labor**. Buy the battery anywhere on this list, but the install (Sections 2–5 below) and registration (Section 6) are on you either way.

## 1. Before you start

- Confirm the battery spec above matches your van's actual data (door-jamb sticker or the label on the current battery) before ordering.
- Tools: T25 Torx driver, 10mm and 13mm socket wrench, work gloves, safety glasses. Optional: a memory saver (9V-battery OBD-port plug-in) to preserve radio presets/seat memory.
- Park on level ground, engine off, key out of the ignition, and **wait ~10 minutes** after shutdown before starting — Sprinter electronics need time to fully power down.

## 2. Access the battery

The main battery sits **under the driver's floor**, standard for this Sprinter generation across cargo/passenger/chassis-cab variants. Since this is a coach-built RV, visually confirm Winnebago didn't relocate it before assuming this location.

1. Slide the driver's seat all the way back.
2. Pull back the floor mat/liner at the door threshold.
3. Remove the 3 T25 Torx screws holding the rectangular access panel.
4. Lift the cover carefully — note how any wiring is routed around the edges so you can replace it the same way.
5. Remove any secondary plastic covers or hold-down brackets over the battery itself.

## 3. Disconnect the old battery

1. **Disconnect the main ground cable** near the accelerator pedal first — push down the red tab and pull back on the connector. This is Mercedes' main power cutoff, separate from the battery terminal itself.
2. At the battery: **remove the negative terminal first**, then the positive. Keep them separated and covered with a rag so they can't accidentally touch each other or anything metal.
3. Disconnect the **vent tube** from the side of the battery (routes hydrogen gas outside the cabin — note its routing for reinstall).
4. Remove the hold-down clamp/bracket.
5. Lift the old battery straight up and out. It's heavy (~55–65 lb) — lift with your legs, get a second person if needed.

## 4. Install the new battery

1. Confirm the new battery is AGM, correct group size (49/H8), and correct terminal polarity/orientation before setting it in the tray.
2. Set it in place matching the old battery's orientation exactly.
3. Reinstall the hold-down clamp — snug, not overtightened (AGM cases can crack).
4. **Reconnect the vent tube first**, before the terminals, and confirm it's routed to vent outside the cabin.
5. **Reconnect the positive terminal first, then the negative** (reverse of removal order). Tighten securely; avoid letting a metal tool bridge both terminals while you work.
6. Reconnect the main ground cable near the accelerator pedal until it clicks/locks.

## 5. Reassemble

Reinstall any secondary covers/brackets, then the main access panel (T25 screws), then the floor mat, then return the seat to its normal position.

## 6. Register the new battery — don't skip this

Sprinters from 2008+ with IBS/Start-Stop (including this 2019 chassis) track the battery's charge/discharge history to set the alternator's charging strategy. Skipping registration means the vehicle keeps using the **old, degraded battery's profile** — typically overcharging the new battery and shortening its life, and can cause Start-Stop to disable itself. Takes about 2 minutes once you have the right tool. Mercedes has stated that an unregistered replacement can also **invalidate powertrain warranty coverage on related control modules** — worth knowing if this chassis still has warranty remaining.

### Scan tool

See [Sprinter_OBD_Scanner_Review.md](Sprinter_OBD_Scanner_Review.md) for the full tier-by-tier buyer's guide, and [Ancel_BZ700_Deep_Dive.md](Ancel_BZ700_Deep_Dive.md) for the specific tool used here. **Update: battery registration is now owner-confirmed working on this exact 2019 VS30/907 chassis via the Ancel BZ700** — the doc's earlier caution (no budget tool had confirmed registration, as opposed to just testing) is resolved for this tool/chassis combination.

**Confirmed procedure on the BZ700:**

1. Plug into the 16-pin OBD2 port under the dash, power on.
2. Let it run Auto-VIN — selecting "Benz" manually first isn't necessary, it finds the Sprinter/VIN on its own.
3. Note: the **"Battery" option on the main menu is a battery health check/monitor**, not registration — it wants the engine running and just monitors charge/voltage. Skip it for this purpose (though it's useful diagnostic info on its own).
4. From the menu, go back and select **BMS Reset** instead.
5. It re-confirms the vehicle (Sprinter, VIN found).
6. It asks you to confirm the battery has already been replaced — confirm.
7. Hit OK — this runs the actual reset/registration.

Real-world run took about the same ~2 minutes quoted above. If your tool doesn't show a clear success screen, start the vehicle afterward and confirm Start-Stop behaves normally as a functional check (see Section 7).

## 7. After the swap

- Start the vehicle and confirm no battery/charging warning lights.
- Check that Start-Stop functions normally (if equipped) — a common symptom of skipped registration is Start-Stop refusing to engage.
- Reset the clock/radio presets if you didn't use a memory saver.
- **Recycle the old battery** — most auto parts stores take AGM/lead-acid cores; many states require it by law, and there's usually a core deposit refund.
