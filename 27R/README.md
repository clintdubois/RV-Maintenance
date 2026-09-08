# 27R — Winnebago View, 2027 model year, 24R floorplan

**Naming note:** The coach's actual floorplan code is **24R** (per Winnebago's own model designations, e.g. "524R2"). Since every document in this folder is about the 2027 model year, the "24" year-adjacent digit is redundant here — we refer to this vehicle simply as **"27R"** throughout (folder name, file prefixes, and body text) rather than writing out "2027 24R" every time. If you ever cross-reference Winnebago's official model/parts docs, look for **24R** or **524R2**, not "27R" — that string is local shorthand only and won't appear in manufacturer documentation.

## Contents

Markdown source files live in [MD/](MD/); `.docx` (and the one `.pdf`) stay here at the top level.

- [MD/27R_2000W_Inverter_Operation.md](MD/27R_2000W_Inverter_Operation.md) / `27R_2000W_Inverter_Operation.docx` — 2000W inverter/charger operation guide
- [MD/27R_12V_Fuse_and_Breaker_Panel_Location.md](MD/27R_12V_Fuse_and_Breaker_Panel_Location.md) / `27R_12V_Fuse_and_Breaker_Panel_Location.docx` — 12V fuse/breaker panel location and CZone digital switching system
- [MD/27R_60W_Draw_Isolation_Checklist.md](MD/27R_60W_Draw_Isolation_Checklist.md) / `27R_60W_Draw_Isolation_Checklist.docx` / `.pdf` — step-by-step checklist to isolate a continuous parasitic 12V draw. Generated from [MD/27R_60W_Draw_Isolation_Checklist.yaml](MD/27R_60W_Draw_Isolation_Checklist.yaml) — the first troubleshooting guide built with the reusable `scripts/troubleshooting_doc.py` template (see below); edit the YAML, not the `.md`, for future changes.
- [MD/Winnebago_27R_Negotiation_Playbook.md](MD/Winnebago_27R_Negotiation_Playbook.md) / `Winnebago_27R_Negotiation_Playbook.docx`
- [MD/Winnebago_27R_New_Owner_Orientation.md](MD/Winnebago_27R_New_Owner_Orientation.md) / `Winnebago_27R_New_Owner_Orientation.docx`
- [MD/Winnebago_27R_Operations_Guide.md](MD/Winnebago_27R_Operations_Guide.md) / `Winnebago_27R_Operations_Guide.docx`
- [MD/Winnebago_27R_PDI_Walkthrough_Checklist.md](MD/Winnebago_27R_PDI_Walkthrough_Checklist.md) / `Winnebago_27R_PDI_Walkthrough_Checklist.docx`
- [Winnebago_View_2027_Operator_Manual.pdf](Winnebago_View_2027_Operator_Manual.pdf) — official Winnebago operator's manual
- [Wiring_Diagrams/](Wiring_Diagrams/README.md) — official Winnebago wiring diagrams (524R2)

## Making a new troubleshooting guide

Every troubleshooting guide (like the 60W draw checklist above) should be built with the reusable
generator at `GIT/scripts/troubleshooting_doc.py` rather than a one-off script, so they all share the
same structure and PDF styling:

1. Copy `GIT/scripts/troubleshooting_template.yaml` to `MD/<Slug>.yaml` and fill it in (see inline
   comments in that file for the field reference).
2. Run: `python GIT/scripts/troubleshooting_doc.py MD/<Slug>.yaml MD`
3. Move the generated `<Slug>.docx` and `<Slug>.pdf` up from `MD/` to this top-level folder (the `.md`
   and `.yaml` stay in `MD/`).
4. Add an entry to the Contents list above and commit all four files (`.yaml`, `.md`, `.docx`, `.pdf` —
   note the repo's `.gitignore` excludes `*.pdf`, so the PDF stays local-only like the other PDFs here).
