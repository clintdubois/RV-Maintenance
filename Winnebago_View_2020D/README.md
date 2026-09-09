# Winnebago View 2020D Maintenance

Documentation and maintenance records for the Winnebago View 2020 (24D floorplan) motorhome, including battery systems, electrical diagnostics, charging solutions, and appliance management. Folder named `Winnebago_View_2020D` to match the sibling `Winnebago_View_2027R` folder's vehicle+year+floorplan convention.

## Vehicle Overview

**Make/Model:** Winnebago View 2020, 24D floorplan
**Chassis:** Sprinter (Mercedes-Benz)
**Status:** Active

## Documentation

Markdown source files live in `MD/` subfolders (e.g. `MD/`, `Fridge/MD/`); `.docx` files stay alongside the other content at each folder's top level.

### Battery & Electrical Systems
- [Chassis Battery Replacement](MD/Winnebago_View_2020_Chassis_Battery_Replacement.md) - Procedures for replacing the main chassis battery
- [Electrical Troubleshooting](MD/Wiper_Charging_Electrical_Troubleshooting.md) - Diagnosing and resolving electrical gremlins, wiper issues, and charging problems

### Charging System Upgrades
- [Trickle Charger Installation](MD/House2Start_Trickle_Charger_Install.md) - Installing House2Start smart charging system for house battery management while parked

### Diagnostics & Tools
- [OBD Scanner Review](MD/Sprinter_OBD_Scanner_Review.md) - Review of Ancel BZ700 diagnostic scanner and how to use it for engine diagnostics

### Scanner & Diagnostics Tools
- [Ancel BZ700 Deep Dive](MD/Ancel_BZ700_Deep_Dive.md) - Detailed guide to the Ancel BZ700 OBD-II scanner features and usage

### Appliances
- [Fridge: DMC4101 Model, Specs & Purchase Record](Fridge/MD/DMC4101_Model_Specs_Purchase.md) - Nameplate specs (model, ratings, refrigerant) transcribed from the installed unit, plus Amazon purchase record (7/30/2023, $1,600)
- [Fridge: DMC4101 Not Cooling Below ~13V](Fridge/MD/DMC4101_Not_Cooling_Voltage_Drop.md) / `Fridge/DMC4101_Not_Cooling_Voltage_Drop.docx` / `.pdf` - Dometic DMC4101 warming below ~13V (wiring/voltage-drop vs. sag-under-load), plus other commonly reported cooling issues. Generated from [Fridge/MD/DMC4101_Not_Cooling_Voltage_Drop.yaml](Fridge/MD/DMC4101_Not_Cooling_Voltage_Drop.yaml) via `scripts/troubleshooting_doc.py` — edit the YAML, not the `.md`, for future changes. Published to WayfinderNorthwest.
- [Fridge: DMC4101 Manuals](Fridge/MD/DMC4101_Manuals.md) - Combined install/operation manual (local PDF copy saved) and notes on what documentation Dometic does/doesn't publish for this model

## Recent Maintenance

- Battery replacement and diagnostic work
- Electrical system troubleshooting (charging circuit, wiper systems)
- House battery trickle charger installation
- OBD scanner setup and diagnostics

## Quick Reference

### Key Systems
- **Chassis:** Mercedes-Benz Sprinter
- **Main Battery:** (See battery replacement guide)
- **House System:** 12V house battery with House2Start trickle charger
- **Diagnostic Tool:** Ancel BZ700 OBD-II scanner

### Common Issues Addressed
- Electrical gremlins and intermittent faults
- Wiper system malfunctions
- Charging system diagnostics
- House battery management

## Notes

All procedures documented with step-by-step guides. Electrical diagrams and specifications included in relevant documents.
