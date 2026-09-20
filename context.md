# RV-Maintenance — Current Context

Living status file for this repo. **Overwrite this** (don't append) after
any meaningful chunk of work, so a new session can pick up state without
re-reading history or old chat transcripts.

Last updated: 2026-09-20.

## What this repo is

Maintenance, repair, and system documentation for RV vehicles and camper
vans, split by vehicle: `Winnebago_View_2020D/` (24D floorplan),
`Winnebago_View_2027R/` (24R floorplan, referred to locally as "27R" — see
that folder's own README for the naming note), `Luna_Campervan/`, plus
cross-vehicle `Systems/` docs (battery, charging, etc.) and `Projects/`.
Camping/`24R` docs were moved into `Winnebago_View_2027R` (see Camping's
context.md).

## Current state

Active thread: **rear suspension upgrade** — a reference doc was just
started for the 2027R (most recent commit). Just before that: rebuilt the
fridge voltage-drop doc as a `troubleshooting_doc.py`-generated guide,
fixed the Fridge folder to match the `MD/` subfolder convention, renamed
vehicle folders to include the floorplan letter, and added
low-voltage-under-load as a possible (unconfirmed) cause in a
troubleshooting doc.

## Standing conventions specific to this repo

- Troubleshooting guides are built with the reusable
  `scripts/troubleshooting_doc.py` template — reuse it rather than writing
  a one-off doc structure.
- Vehicle folders are named with their floorplan letter included (e.g.
  `Winnebago_View_2027R`, not just `Winnebago_View_2027`).
