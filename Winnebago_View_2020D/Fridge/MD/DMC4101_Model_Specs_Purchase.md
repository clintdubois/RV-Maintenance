# Dometic DMC4101 Refrigerator-Freezer — Model, Specs & Purchase Record

Reference record for the installed fridge, transcribed from the manufacturer nameplate (photographed in place — see `FridgeModel.jpeg` in the parent folder) plus purchase details.

## Purchase

| Field | Value |
|---|---|
| Retailer | Amazon |
| Purchase date | 7/30/2023 |
| Price | $1,600.00 |

## Nameplate Specifications

| Field | Value |
|---|---|
| Manufacturer | Dometic |
| Model | DMC4101 |
| Type | Refrigerator-freezer, built-in installation only |
| Design pressure — high side | 300 PSI |
| Design pressure — low side | 120 PSI |
| Refrigerant | R134a |
| Refrigerant amount | 3.86 oz |
| Rated voltage | DC 12V |
| Rated current | 13A |
| Fuse rating (circuit) | 15A |
| Defrost power | 120W |
| Net weight | 127.9 lbs |
| Blowing gas | Cyclopentane |
| Certification | CSA/US, cert. no. C160987 |
| Made in | China |

Note: the nameplate's **rated current of 13A** corrects an earlier note in [DMC4101_Not_Cooling_Voltage_Drop.md](DMC4101_Not_Cooling_Voltage_Drop.md), which cited a forum-sourced figure of ~15A for compressor draw — 13A is the manufacturer-specified running-current value and should be used for wire-gauge/voltage-drop calculations going forward.

**Fuse vs. draw — these are two different numbers, don't conflate them:** the fridge draws 13A continuous, but the circuit fuse should be rated **15A**, not 13A. The fuse is sized above the steady running draw to tolerate compressor startup inrush without nuisance-tripping, while still protecting the wiring gauge actually installed on the circuit. Sizing the fuse to the wire's ampacity (not just the appliance's rated draw) is what determines the correct fuse value — confirm that against the gauge of wire actually run to the fridge.

## Nameplate Photo

See `FridgeModel.jpeg` in the parent folder — photo of the nameplate/circuit diagram label as installed.

## Related Documentation

- [DMC4101 Not Cooling Below ~13V — Voltage Drop Research](DMC4101_Not_Cooling_Voltage_Drop.md)
