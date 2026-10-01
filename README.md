# RestoKit

![RestoKit banner](img/banner.jpg)

**A voice-ready field kit for water, mold, and crawlspace restoration techs.**

## What it is

RestoKit is a structured JSON kit that loads into a voice assistant and works alongside a tech on the job. It's grounded in IICRC S500 (water) and S520 (mold) principles and written in a peer voice, the way a senior tech talks a job through from the truck.

It has two layers:

- **Phases:** a linear job flow with gates in a set order, so safety-critical steps don't get skipped under time pressure.
- **Modules and base science:** a reference pool the steps point into for the why. It covers category, remove-vs-dry, containment, equipment sizing, drying science, mold cleaning, and crawlspaces.

It's senior-tech knowledge in a form you can use in the field. It doesn't replace years on the job. Its main job is memory: it holds the rare edge-case lessons that don't come up often enough to stay top of mind.

## What it covers on a job

- **Phase 0, Hold Status:** Minimum stabilization while a job waits on approval, abatement, or a plumber. That means protecting contents, flagging hazards, putting up minimal containment, and documenting the hold and the wet-time clock.
- **Phase 1, Initial Response & Stabilization:** A signed work authorization comes before any physical work. Then: a job-type check, the safety walk and category check, source control, bulk extraction, and baseline readings in affected and unaffected areas. It also covers crawlspace inspection and asbestos sampling in pre-1980 homes before destructive work.
- **Phase 2, Selective Demolition & Post-Demo Cleaning:** Remove vs. dry-in-place by material, category, and dwell time. Controls are upgraded before demo, and demo runs top-down. Hidden water gets chased into cavities, under LVP, and along base plates. Then post-demo cleaning and an equipment re-set.
- **Phase 3, Active Drying & Monitoring:** Daily temperature, RH, and GPP readings, plus dehumidifier grain depression. Moisture readings go at the same points every visit, and containment gets re-checked. If progress stalls after 48–72 hours of proper conditions, the kit calls for a root-cause check.
- **Phase 4, Verification & Closeout:** Controls stay up and teardown waits until final moisture verification passes. Then the cavity and crawlspace inspection, customer walkthrough, and documentation package.

## Checks the kit calls out

- **Category:** When unsure, go with the higher category. Water from under a toilet is Category 3 until proven otherwise. A strong musty or sewage odor overrides appearance.
- **Electrical:** Standing water plus live circuits means stop. Kill it at the breaker, verify it's dead, and use GFCI on temp power.
- **Crawlspaces:** Every crawl gets a 4-gas check (O₂, CO, H₂S/sewer gas). Never work one alone, and never push crawl air up into the house.
- **Containment:** Minimal containment on every job, even Category 1. Full containment before demo or when contamination risk rises. Never bag a live HVAC return.
- **Negative air:** Target about −5 Pa continuous, sized for 4+ air changes per hour. If a gas appliance is in or next to the chamber, check flue draft and plan makeup air.
- **Dry standard:** Match the unaffected material in the same building. For wood, that's within about 2–4 points. The ≤16 / 16.1–19.9 / ≥20% traffic light is a risk band, not a second dry standard.
- **Mold:** The condition labels Normal, Settled, and Colonized are ranked by severity, not a timeline. Kill is not remove, because dead spores stay a reservoir.

## The science behind the calls

- Read RH and temp, log GPP. RH for the quick check, GPP to compare days, rooms, and dehu inlet vs. outlet, since RH shifts with temperature.
- Vapor pressure and vapor drive
- Wicking, capillary action, and free vs. bound moisture
- Material behavior, including LVP and other modern flooring that traps water underneath
- Equipment sizing by water class and cubic footage, and the displacement principle behind tenting and ducting

## Voice behavior

Each step carries a short line meant to be spoken. A tech asks in one short phrase and gets only that part, not the whole module. Deeper detail stays in the reference layer until the tech asks for it.

**Example of what a tech might hear:**

> "Full containment before demo. Neg air target: about minus five pascals continuous, or more negative. Quick check: bounce a quarter on the six-mil. If it's flat or flapping, you lost pressure."

## How it grows

RestoKit grows from daily voice job logs. A lesson goes into the kit only after it proves itself on real jobs, as a short voice note in the module that owns it.

The current version is **0.8.9**.

## Where it's headed

Next up is connecting the field scope to Xactimate so the scope and the estimate line up.

## For shops

A demo of the kit is available on request. From there, Jason can build a company version around a shop's own procedures.

## About

RestoKit is built by **Jason Burns**, a restoration tech and builder in Portland, OR, and a U.S. Army Engineer veteran.

- GitHub: [github.com/neuresthetics](https://github.com/neuresthetics)
- Email: [neuresthetics@gmail.com](mailto:neuresthetics@gmail.com)

## Kit structure

Top-level layout of the kit, contents omitted:

```json
{
  "framework": "Kit identifier",
  "meta": "Author, version, date, and kit description",
  "framework_scale": "Rules for when modules grow into shallow trees",
  "main_content": {
    "phases": {
      "phase0": "Hold Status: minimal stabilization while a job waits",
      "phase1": "Initial Response & Stabilization",
      "phase2": "Selective Demolition & Post-Demo Cleaning",
      "phase3": "Active Drying & Monitoring",
      "phase4": "Verification & Closeout"
    },
    "modules": {
      "demolition": "Remove-vs-dry decisions, demo sequence, controls, post-demo clean",
      "crawlspaces": "Crawl safety, inspection, insulation, airflow, vapor barrier",
      "special_situations": "High-complexity homes needing elevated PPE and sequencing",
      "leadership_and_labor": "Crew leadership and labor distribution",
      "practical_judgment": "Sound technical calls under real-world constraints",
      "emergency_calls": "Triage for after-hours and urgent calls",
      "service_contract": "Work authorization before scope or demo",
      "initial_assessment": "First on-site evaluation",
      "source_control": "Stopping and verifying the water source",
      "extraction": "Removing standing water",
      "ambient_humidity_assessment": "Quick RH and temp screen before equipment",
      "contents_handling": "Protecting, moving, cleaning, and returning contents",
      "engineering_controls": "Negative pressure, air filtration, and related controls",
      "containment": "Containment types, build sequence, and blowouts",
      "extension_cord_safety": "",
      "electrical_safety": "",
      "drying_and_monitoring": "Drying setup, tenting, dry standards, dehu ducting",
      "general_cleaning": "",
      "ulv_vs_hand_pump_sprayer": "Choosing an application method for antimicrobials",
      "trash_management_and_logistics": "Debris handling and hauling",
      "final_verification": "Final moisture checks before teardown",
      "job_closeout": "Teardown, walkthrough, and closing the job",
      "documentation": "Documentation habits across the job",
      "category_decision": "Verifying or upgrading water category on site",
      "hazard_sampling": "Asbestos and hazardous material sampling",
      "limited_targeted_access": "Low-risk access before full demo",
      "equipment_setup": "Equipment placement and sizing",
      "van_organization": "Work vehicle setup",
      "mcgyver": "Practical field improvisations",
      "insurance_dynamics": "Working within carrier rules",
      "monitoring": "Daily monitoring methods and trend logging",
      "mold_cleaning": "Mold cleaning approach, sequence, and condition labels",
      "ale": "Additional living expense notes",
      "electricity_bills": "Equipment power cost notes",
      "_structure_note": "Internal note on module layout",
      "job_type_gate": "Confirm the job type before loading water modules"
    },
    "base_science": {
      "water_category": "",
      "psychrometry": "",
      "moisture_physics": "",
      "water_movement_pathways": "",
      "evaporation_principles": "",
      "dry_standards": "",
      "contamination_science": "",
      "mold_science": "",
      "material_behavior": "",
      "vapor_drive_and_pressure": "",
      "wood_emc": "Wood equilibrium moisture content"
    },
    "board_stage_aliases": "Maps workflow stages to project-board column names"
  },
  "update_notes": "Version-by-version changelog"
}
```

## A note on this repo

This is a public window into the project. The full kit is kept private. A demo is available on request.
