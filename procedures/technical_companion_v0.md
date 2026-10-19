# Technical Companion to the Crew Procedures (v0, lead/PM version)

> [!CAUTION]
> **Not fully reviewed. Not policy yet.** This draft needs review by the RestoKit author before use. It has useful material, but AI-drafted RestoKit content tends to over-engineer and miss real-world limits (crew time, staffing, equipment on hand). The review is that reality check.

> Generic v0 draft. Adapt to your company's procedures, scope sheet and local rules.

**What this is:** This is the depth behind `crew_procedures_v0.md`, written for leads and PMs. The numbering matches the crew version, so any crew line maps to the detail here. The crew version builds habits. This version explains the why, the full how, the decision points, and what the crew version leaves out on purpose so the lead knows what to watch for.

**How to read it:** Each item has four parts:
- **Why:** the science or liability behind the crew line.
- **How (full):** the detailed method.
- **Decisions / edge cases:** the calls a lead makes.
- **Crew simplification, so watch for:** where the crew line is intentionally simplified, and what the lead covers.

Each item ends with **Kit:** pointers into RestoKit 0.9.2 (`resto_kit_0.9.2.json`). Paths are written the way the kit writes them. Modules sit under `main_content.modules`, and `phases` and `base_science` sit under `main_content`.

**Standards framing:** Our process is grounded in IICRC S500/S520 principles. The job file shows what we did and why. Do not call the company, a job, or this document "certified," "approved," or "compliant."

**Scope sheet = provisional billable list:** What counts as billable is answered, for now, by the mitigation scope sheet template ([scope sheet template](../templates/mitigation_scope_sheet_template.md) / `.json`), a transcription of a third-party industry sheet, pending your company's review. This document does not re-list billable items. It points to scope sheet line numbers ("SS 76") and sections instead. Line numbers follow the template and may shift after cleanup.

**Flags used:**
- **[verify]:** a common field practice or number that the kit does not state. Confirm it before treating it as a rule.
- **Company decision needed:** a company policy gap. This document does not invent the policy.

**Contents**
- [Read first: stops that override every section](#read-first-stops-that-override-every-section)
- [1. Field Documentation](#1-field-documentation): [1.1](#11-get-to-know-the-job-lead-first-crew-visit) · [1.2](#12-arrival-and-departure-sets) · [1.3](#13-proof-photos) · [1.4](#14-measurements) · [1.5](#15-daily-scope-sheet) · [1.6](#16-dehus) · [1.7](#17-equipment-numbers) · [1.8](#18-broken-equipment)
- [2. Cleaning](#2-cleaning): [2.1](#21-every-visit) · [2.2](#22-standard-post-demo-cleaning-base-end-of-demo-day) · [2.3](#23-adjust-to-the-job) · [2.4](#24-final-check-before-we-call-it-done) · [Containment tip](#containment-tip-crew-20-minutes-of-plastic-saves-an-hour-of-cleaning) · [Air-test (IEP) jobs](#air-test-iep-jobs)
- [3. Crew Training](#3-crew-training): [3.1](#31-dehu-setup) · [3.2](#32-scope-sheet-and-photos) · [3.3](#33-getting-to-know-the-water) · [3.4](#34-broken-equipment-tag) · [3.5](#35-cleaning) · [3.6](#36-arrival-and-departure-sets)
- [Flags collected](#flags-collected)

---

## Read first: stops that override every section

These are not crew-meeting topics. They are holds the lead enforces before any crew line applies.

- **Asbestos and lead before disturbance.**
 - Suspect material gets sampled or presumed before anyone cuts, pulls base, or scrapes. If results are pending, treat the material as positive.
 - Asbestos-containing material (more than 1 percent) or presumed material stops the disturbing work and goes to licensed abatement.
 - An owner survey does not clear demo. Building age is a prompt, not a clearance.
 - Pre-1981 fireproofing, 9-inch tile, and flooring and mastic installed by 1980 are named checks. Pre-1978 lead falls under the EPA renovation rule.
 - Oregon and Washington have their own survey rules, so check the jurisdiction on every job.
 - **Scope sheet:** year of construction (header) and SS 1 (testing, with who tested). The sheet's "lead before 1978, asbestos before 1980" rule is a minimum prompt from the source company. It does not clear a newer home, and the kit's named checks (pre-1981 fireproofing) and state survey rules can reach past it.
 - On Category 1 losses waiting on results, limited access is allowed: outlet covers and switch plates only. Baseboards wait in older or suspect homes.
 - **Kit:** `demolition.tree.controls_and_limits.asbestos_demo_limits`, `hazard_sampling.who_samples`, `hazard_sampling.decisions`, `limited_targeted_access`, `phases.phase1.sequence` (Confirm Sampling Results or Hold), `phases.hold_status.hold_reasons.abatement_scheduling`, `safety_and_health.stops`
- **Electrical.**
 - Standing water plus energized circuits means stop. De-energize at the breaker, then identify, isolate, and verify the circuit is dead.
 - Don't reset a breaker into a wet panel. A wet electrical system stays off until a qualified person clears it.
 - Use GFCI on all temporary power.
 - **Kit:** `electrical_safety.key_rules`, `extension_cord_safety.key_rules`
- **Crawl entry (4-gas / confined space).**
 - Size up the crawl at the hatch first: smell, water, sewage, gas appliances, wiring.
 - The kit *recommends* a 4-gas check before every crawl entry. The check is required, or nobody enters, when there is a gas or sewer smell, a gas appliance or line in the crawl, combustion equipment running, a known hazard, true confined-space conditions (no airflow, tight single egress), or when company policy requires it.
 - Most residential crawls are non-permit confined spaces. A crawl becomes permit-required (29 CFR 1910.146) only if it has or could have a hazardous atmosphere, engulfment, an entrapping shape, or another serious hazard. A permit-required space needs a posted permit, atmospheric monitoring, a trained entry team, and an attendant.
 - Put a buddy topside when the crawl is tight, hot, or contaminated. Use short, heavy-gauge GFCI cords. Treat heat as a hazard, with the buddy system in attics and crawls.
 - **Company decision needed:** the 4-gas policy. Options are every entry, triggers only, or meters on every crawl job. Also decide who owns and bump-tests the meters.
 - **Kit:** `crawlspaces.tree.safety_and_access.atmospheric_testing`, `crawlspaces.tree.safety_and_access.confined_space`, `safety_and_health.additional_stops`, `safety_and_health.crew_practices`
- **Negative air near gas appliances.**
 - A negative chamber that includes or sits next to a gas appliance can starve the flue and pull CO back down the vent. Identify the appliances first, check flue draft with the negative running, and plan makeup air from the clean side.
 - **Kit:** `engineering_controls.gas_appliance_backdraft`, `containment.gas_appliance_backdraft_check`
- **Respirators** need the written program: NIOSH-approved selection, medical evaluation, fit test, and training (29 CFR 1910.134). Use P-100 for spores.
 - **Company decision needed:** confirm the written respirator program and fit-test records exist for every tech who wears one.
 - **Scope sheet:** PPE SS 95–98 (suit changes, filters, half or full face).
 - **Kit:** `safety_and_health.additional_stops`, `safety_and_health.stops`
- **Category sets the controls.**
 - When the category is uncertain, call it higher. Water from under a toilet is Category 3 until proven otherwise.
 - Strong sewage or musty odor overrides clean looks.
 - Clean water past 48 hours warm gets Category 2 caution.
 - Category 2 and 3 are remediated before restorative drying.
 - **Kit:** `base_science.water_category.decision_rules`, `base_science.water_category.time_and_migration`, `category_decision`

---

## 1. Field Documentation

### 1.1 Get to know the job (lead, first crew visit)

**Why:**
- The survey map is a snapshot. Water keeps moving by bulk flow, wicking, air transport, and vapor diffusion, and the initial visual scope is almost always low.
- The edges of the wet decide the cut lines. Cut short, and you leave wet or contaminated material in a closed wall. That is a mold reservoir and a callback. Cut long, and you get unbillable or disputed removal.
- The kit defines the moisture map as the record of how far the water went, *including the adjacent dry areas*. The dry edge is part of the map.

**How (full):**
1. Review the job file before entry: the survey moisture map, category and its rationale, cause of loss, dwell time, building age and sampling status, and any pre-existing damage notes.
2. Confirm the hazard holds (see Read first). Pending asbestos results mean no disturbance.
3. Take baseline psychrometrics: temperature, RH, and GPP in an affected area, an unaffected area of the house, and outdoors. Rank GPP above RH, because RH moves with temperature.
4. Walk the water with the meter from wet to dry until you reach readings that match unaffected material of the same type. Check:
 - both sides of every affected wall, plus the room beyond (the baseplate highway);
 - under and behind cabinets, toe kicks, and vanities;
 - California corners and under shower pans and tubs;
 - the space below, whether that's a crawl or a lower floor;
 - sill plates (the scope sheet QA checklist asks for sill plate readings and a 3-inch screw test).
5. Read layered assemblies by layer. Tile, vinyl, LVP, and coatings are lids, and the dry is the substrate under them. A non-invasive meter reads only about ¾ inch deep, so lift an edge or probe when the surface reads dry over a suspect area. Confirm any thermal image with a meter.
6. Set the dry standard from unaffected material of the same type in the same building, under current conditions. Write it against a named material.
7. If the extent, category, or hazards differ from the map, mark the new readings, photograph them, and tell the PM before demo. Log the result even when nothing changed ("spot check matches survey").

**Reading-point placement (lead-level):**
- Use fixed points you can return to every day. In the screw method, two screws go into the wettest or most representative spot, and readings are taken off the screws. This lines up with the scope sheet QA item "3-inch screw test."
- For bad crawls, run wire from the screws out to the hatch so readings can be taken without full entry.
- Spacing is a common field practice the kit does not state: points about 24 inches out from the wall and grid spacing of roughly 8–10 feet across open floor. **[verify]** Whatever spacing you use, use the same spacing on every job, because uniformity matters more than the specific method.

**Decisions / edge cases:**
- **Concentrated vs widespread entry.** Water that drops into a crawl at one point may run down a joist rather than soak all the insulation. Check where it actually landed.
- **Slabs.** Assume the water spread farther than it looks, because the perimeter gap acts as a highway.
- **Category change on the walk.** Odor, sludge, a source from under the toilet, or long dwell moves the category up. Update the file before demo, since this changes controls, PPE, and removal.
- **Wood targets.** Wood within 2–4 points of unaffected wood of the same type is a field check, not the goal. The kit's wood risk bands are ≤16% lower risk, 16.1–19.9% elevated, and ≥20% high. They are for triage only, not a dry standard.
- **Hot-water line in a crawl.** Heat plus moisture plus organics means very fast growth. Treat it as urgent.

**Crew simplification, so watch for:**
- The crew line says "find the edges." It doesn't teach category, layered assemblies, or reading points.
- The lead owns:
 - the category call;
 - the dry standard and the reference material;
 - setting fixed points;
 - the PM call when the map is wrong.
- A crew member's meter walk is a training rep, not the record. The record is the lead's.

**Kit:** `base_science.water_movement_pathways`, `base_science.moisture_physics`, `base_science.psychrometry.core_concepts`, `base_science.dry_standards`, `base_science.material_behavior.reference_lines`, `base_science.material_behavior.field_implications.hidden_moisture_assessment`, `demolition.tree.decision_logic.chasing_the_water`, `monitoring.fixed_point_techniques`, `drying_and_monitoring.dry_standards.traffic_light`, `insurance_dynamics.key_realities`, `glossary` (moisture map), `phases.phase2.sequence` (Demo Planning & Scope Confirmation), `crawlspaces.tree.inspection`

### 1.2 Arrival and departure sets

**Why:**
- Fixed-point, same-angle photos make progress, or the lack of it, obvious. They also protect the file when scope, pre-existing damage, or equipment runtime is questioned.
- Each departure set doubles as the next day's "before" and as the equipment placement record, which the kit expects on Day 1 and on any day equipment changes.

**How (full):**
1. **Before touching anything.** Shoot every affected room from the corners, working inside out, with the same angles each time.
2. **Departure.** Clean up first, then reshoot the same angles. The set should show:
 - where every dehu, air mover, and AFD sits;
 - which way the airflow runs;
 - containment, zippers, and floor protection;
 - any tenting or ducting.
3. Name or date the photos consistently so the package can be navigated weeks later.
4. **Monitoring visits.** Photograph the dehu readout and record the fixed-point readings (with meter-in-frame photos per 1.3).
5. **Inspections.** Readings, tape, and mapping only.

**Decisions / edge cases:**
- **"Layout change" includes:**
 - equipment added, removed, or repositioned;
 - containment altered or repaired after a blowout;
 - a new opening cut;
 - contents moved;
 - a homeowner moving a fan.
 - Any of these triggers a full departure set that day.
- **Scope expansions and judgment calls** (category upgrade, remove vs dry, equipment change) get the triggering condition photographed the same day, even on a non-demo day.

**Scope sheet tie-in:** The QA checklist asks for before and after pictures, overviews, and all equipment shown. Arrival and departure sets are how we answer it.

**Crew simplification, so watch for:**
- The kit expects daily monitoring to repeat the same photo angles. The crew version limits full sets to demo and layout days so the habit is achievable.
- **The gap:** on a plain monitoring day, the file shows readings and the dehu screen but no room-wide image.
- **What the lead watches for:**
 - unrecorded equipment moves;
 - stalled rooms with no visual trend;
 - homeowner tampering.
- If a room isn't drying on schedule, shoot a full set that day.
- **Company decision needed:** whether monitoring visits on long dries, roughly 5+ days, get one wide shot per room per visit.

**Kit:** `documentation.key_habits`, `documentation.decision_criteria`, `documentation.practical_guidance`, `documentation.warnings`, `equipment_setup.practical_guidance` (placement photos and diagram), `phases.phase1.sequence` (Confirm or Complete Survey Documentation), `phases.phase3.sequence` (Daily Documentation & Trend Logging)

### 1.3 Proof photos

**Why:**
- Adjusters review the file after the evidence is gone, and some won't understand bound moisture or hidden pathways.
- A carrier may call a slow leak "neglect." Photos of staining, rot, and the cause of loss answer the duration and cause questions.
- Pre-existing damage photos protect the company from "you caused this."
- The documentation rule is to document before you touch and document as you reveal.

**How (full):**
1. **Required shots:**
 - the front of the house;
 - every affected room;
 - the cause of loss;
 - every scope sheet line used, before and after (scope sheet QA: before/after pictures, overviews);
 - plumbing detaches, which the sheet marks "Photo needed" (SS 101–103: supply line, P-trap, toilet).
2. **The moment a hidden condition is exposed, shoot it:**
 - wet insulation in the cavity;
 - wet pad and subfloor;
 - growth, rot, or checking in wood;
 - damage behind cabinets;
 - corroded or dissolved pipe (drain cleaners);
 - water under LVP or a tile liner.
3. **Wide first, then close,** so a reviewer can place the close-up.
4. **Meter shots:** the screen and the material in the same frame, at the fixed point, on the same meter each time.
5. **Action shots** of extraction, demo, cleaning, and containment build. These support labor lines, because equipment codes often carry no labor.
6. **Thermal images** are a scope line (SS 2) and a QA checklist item. Confirm every thermal image with a meter (1.1).

**Decisions / edge cases:**
- **Scope growth.** When you expand scope while chasing water, lead with visible evidence and the migration pattern, not meter numbers alone, and be ready to explain the reasoning.
- **Electronics and appliances exposed to moisture** (especially smoke plus water): document the exposure and recommend a specialist. Do not promise a working unit.
- **Pre-existing damage:** photograph it and note any homeowner statements about it.

**Integrity rule:** Record readings exactly as measured. Never smooth, invent, or backfill them. The kit notes that selective or smoothed readings are common in the industry, and that falsified readings are fraud exposure for the tech and the company. Staging gear for a file photo is not drying performance.

**Crew simplification, so watch for:**
- The crew list is short and general on purpose.
- The lead adds:
 - the category rationale shot (the source);
 - the reference-material reading for the dry standard;
 - photos of any judgment call.
- Watch for meter shots without the material in frame, and close-ups with no matching wide shot.

**Kit:** `documentation`, `insurance_dynamics.key_realities`, `insurance_dynamics.practical_guidance`, `insurance_dynamics.honesty_guard`, `crawlspaces.tree.airflow_and_drying.checkbox_vs_performance`, `legal_and_liability.records_and_retention`, `base_science.material_behavior.corrosion_and_degradation`, `estimating.field_practice`

### 1.4 Measurements

**Why:** The sketch covers routine footage. Tape-in-frame shots are for quantities a reviewer could dispute or that the sketch can't show.

**How (full):**
1. Sketch every wet room, including closets and halls. The scope sheet QA checklist sets the bar: accurate to within 1 inch, with equipment placement shown.
2. Take a tape-in-frame shot for:
 - **non-standard cut heights** (SS 31 records flood cut LF and height). The kit rule is to cut above the highest wet reading, not the visible water line. On Category 3 with dwell, go at least 12–18 inches above it, to the next 2-foot interval.
 - **odd-shaped removal areas;**
 - **foam removal height,** on closed-cell foam walls (probe for wicking height, then remove a margin above it);
 - **anything likely to be disputed.**
3. A line note names the condition, the reading, and the photo.

**Decisions / edge cases:**
- Category 3 gypsum board comes out regardless of height. The measurement documents how much came out, not whether it should.
- Spray-foam and plaster walls get the moisture map, the exact removal height, and the reasoning written down.

**Crew simplification, so watch for:**
- "As needed" relies on the crew recognizing non-standard work.
- The lead checks before the departure set that every cut deviating from the standard 2 ft has a tape shot.
- **Company decision needed:** whether the standard flood cut height and its exceptions get written into the scope or estimating notes.

**Kit:** `demolition.tree.decision_logic.material_decision_matrix.matrix.drywall` (cut height note), `demolition.tree.decision_logic.field_practice`, `demolition.tree.special_assemblies.closed_cell_foam_water_intrusion`, `estimating.field_practice`

### 1.5 Daily scope sheet

**Why:**
- Billables not captured on site get lost.
- Equipment days are billable rental days, so they belong on the scope sheet.
- The moisture log, not an assumed two or three days, justifies equipment runtime.
- The minimum file includes equipment and chemical logs with quantity and time.

**How (full):**
1. Filling out the scope sheet *is* the procedure. Use the mitigation scope sheet template ([scope sheet template](../templates/mitigation_scope_sheet_template.md) / `.json`): one per job per day, or one per room on big jobs. Its sections are the provisional billable list. Don't re-list them here or in the crew version.
2. Work the sheet top to bottom: header (category, class, year of construction, carrier and claim), rooms, then the line sections, the QA checklist, and the manpower table (techs, hours, after-hours).
3. Anything on the sheet gets a photo (1.3).
4. Record any antimicrobial application per 2.3 (product, method, time, quantity, dilution, location) alongside SS 76–78.
5. The lead signs the QA checklist. The customer signs the header to confirm dates and work times.

**Decisions / edge cases:**
- Separate lines, not folded into another: floor protection (SS 3–5), haul-off (SS 65), detach/reset (SS 10–11, 49–53, 57–60, 101–103), after-hours (manpower table).
- Removal without disposal, or carpet out without floor prep, is an incomplete pair.
- Keep mitigation and rebuild as separate subtotals.
- The template's equipment block (SS 80–94a) is quantity × days per room. Set and pull dates still live in the dehu log (1.6).

**Crew simplification, so watch for:**
- Crew rule: fill out the sheet, finish the bottom checklist, and photograph what's on it.
- The lead checks that equipment days (SS 80–94a) match the dehu log (1.6), that HEPA-vac (SS 71) and antimicrobial (SS 77–78) square footage match the cleaning actually done, and that fans and AFDs have quantity × days. They aren't tracked by unit, but they're still billed by count and days.
- The template is provisional, pending your company's review. Changes your company makes go into the template, not into this document.

**Kit:** `templates/mitigation_scope_sheet_template.json` (provisional billable list), `logs/scope_sheet_template.json` (kit scope schema), `estimating.field_practice`, `legal_and_liability.records_and_retention.minimum_file`, `job_closeout.critical_decision_points`, `job_closeout.warnings`

### 1.6 Dehus

**Why:**
- Dehus are both the drying engine and the main rental billable.
- Hour meter, unit number, and dates tie runtime to the invoice. On the scope sheet, dehus bill as quantity × days by size (SS 80 large, SS 81 XL).
- The daily readout photo plus inlet/outlet readings prove the unit was working. "It felt dry" is not defensible.

**How (full):**
1. **At placement:**
 - Reset job hours.
 - Log the unit number and placement date in the job app.
 - Photograph the readout and unit number.
2. **Placement:**
 - Central to the affected area, or pulling from the wettest or most contaminated zone.
 - 12–18 inches of clearance at intake and exhaust.
 - Exhaust aimed toward the wet areas or air-mover intakes.
 - A lipped tray under every unit.
 - Condensate line run straight with no dips, sloped to a safe drain, and taped.
3. **Small closed rooms** (baths, closets, laundry) get their own unit and a humidistat. They overheat and short-cycle.
4. **Daily:**
 - Record inlet and outlet temp/RH and convert to GPP. Grain depression is inlet GPP minus outlet GPP. A healthy unit on an active job typically pulls 15–25 grains.
 - Photograph the readout and unit number.
 - Check condensate removal.
5. **At pull:** photograph the readout, hours, and unit number, and log the pull date.

**Decisions / edge cases:**
- **Sizing starts.** Size from cubic feet and class (informative starts).
 - LGR: Class 1 100, Class 2 50, Class 3 40, Class 4 40 cu ft per pint per day.
 - Conventional: Class 1 100, Class 2 40, Class 3 30.
 - Desiccant: 1/2/3/3 air changes per hour.
 - Example: 12,000 cu ft, Class 2, LGR is 240 PPD to start.
 - Add capacity below 65°F. Containment reduces volume, so it lets fewer units do more.
 - Readings move the numbers.
- **Low depression:**
 - check filters, intake temperature, and placement first;
 - a very hot space cuts LGR capacity;
 - an LGR ducted into a tent with too much back pressure can freeze at the intake (peel the rear filter and look for ice).
- **Crawls:** duct output to the wettest material and use vents as relief (the displacement principle). Never push air from the crawl into the living space.
- **On hold:** watch the GPP delta for vapor management only. Don't chase a tighter depression.
- **Category 2/3:** start humidity control and AFD first. Air movers wait until contaminated porous material is out.

**Crew simplification, so watch for:**
- The readout photo is the crew habit. The readout may show only RH and temperature, depending on the model, which is not grain depression. **[verify per fleet model]**
- The lead takes or checks the inlet/outlet readings and the depression every visit.
- Watch for:
 - hours not reset;
 - unit numbers not matching the log;
 - a unit running in a room that is already dry (wasted rental, and an over-drying risk on wood or plaster).
- **Company decision needed:**
 - the fleet dehu models , and which count as "large" vs "XL" for SS 80–81;
 - whether dehu hours or job-app dates are the billing source of truth when they disagree.

**Kit:** `equipment_setup.equipment_field_basics.dehumidifier_placement`, `equipment_setup.equipment_field_basics.dehumidifier_types`, `equipment_setup.taping_and_routing`, `equipment_setup.sizing_and_calculations.class_sizing_factors`, `equipment_setup.sizing_and_calculations.dehumidifier_sizing`, `drying_and_monitoring.practical_guidance`, `drying_and_monitoring.dehumidifier_ducting`, `phases.phase3.sequence` (Daily Psychrometric & Equipment Baseline), `base_science.psychrometry`, `crawlspaces.tree.airflow_and_drying.air_movement_and_pressure`

**Air movers and AFDs (not tracked by unit, still managed):**
- **Air-mover starting count:** 1 per affected room, plus 1 per 50–70 sq ft of wet floor, plus 1 per 100–150 sq ft of wet wall above 2 ft, plus 1 per inset over 18 in. Aim 5–45 degrees along the wall. After demo you almost always need more, and under-equipping after demo is the most common reason a job dries slow.
- **AFDs:**
 - change pre-filters on dirty jobs;
 - change HEPA filters off the job;
 - seal the intake before shutdown;
 - never exhaust into clean areas.
- **Kit:** `equipment_setup.sizing_and_calculations.air_mover_sizing`, `equipment_setup.equipment_field_basics.afd_basics`, `containment.air_filtration_setup`

### 1.7 Equipment numbers

**Why:** If nobody has to flip a unit to read its number, the number actually gets read and logged. That keeps the dehu log (1.6) and the scope sheet (1.5) accurate.

**How:** Mark numbers large on the top and front, readable in a placement photo from across the room.

**Decisions / edge cases:** The kit has no equipment-inventory or chain-of-custody module. The kit's "chain of custody" means hazard-sample handling only.

**Crew simplification, so watch for:** The lead confirms that every unit in a departure set is identifiable, or at least countable for non-tracked equipment.

**Company decision needed:**
- whether the existing numbered barcode stickers tie into the job app or an inventory tool;
- whether to move them to the top and front;
- whether fans and AFDs ever get per-unit tracking.

**Kit:** none directly (kit gap). Related: `legal_and_liability.records_and_retention.minimum_file` (equipment logs), mitigation scope sheet template equipment block (SS 80–94a).

### 1.8 Broken equipment

**Why:**
- A failed unit on a job stalls the dry and can create a secondary damage claim, for example a pump failure that overflows.
- A unit that goes back to the shop untagged goes right back out broken.

**How (full):**
1. Tag it where it fails, in the field or the shop. Use tape with the problem, the date, and initials.
2. Pull it from service. Damaged or overheating cords come out of service immediately. A warm cord section means stop and correct the setup (wrong gauge, too long, coiled, or damaged).
3. If the unit came off a Category 2/3 or mold job, it is cleaned before it goes into the repair queue. **[verify: kit has no equipment decon procedure; common practice is HEPA-vac and wipe exterior, change or bag filters on-site]**
4. Note the swap in the job's daily log and dehu log, with the old unit number, the new unit number, and the time. Equipment decon is its own scope line on Category 3 jobs (SS 93).

**Crew simplification, so watch for:** Crew sees "tape it." The lead also makes sure the job log reflects the swap. Otherwise the runtime record shows one unit running for days it wasn't on site.

**Company decision needed:**
- where tagged units go in the shop;
- who triages them;
- the out-of-service or return-to-service sign-off;
- a cleaning standard for equipment coming off contaminated jobs.

**Kit:** `extension_cord_safety.key_rules`, `electrical_safety.key_rules`, `equipment_setup.practical_guidance` (trays, secondary damage), `van_organization.clean_dirty_flow`. The tagging system itself is a kit gap.

---

## 2. Cleaning

### 2.1 Every visit

**Why:**
- A clean site is safer: no trip hazards, nails, or loose cords.
- A clean site photographs as professional and keeps dust from re-entering cleaned or drying areas.
- Cleaning before the departure set makes that set a clean "before" for tomorrow.

**How (full):**
- Clean as you go when occupants are home. Batch-then-clean is acceptable on vacant production days, but the site is messier during the day.
- Keep walkways clear.
- Pull or hammer down fasteners after trim and drywall removal, especially at doorways, convex corners, and plates.
- Tape every cord and hose that crosses a walkway, using blue painter's tape only on finished floors.
- Stage bagged debris in an approved area and haul it at end of day.
- Contaminated debris is double-bagged, or bagged with the exterior wiped, inside the decon area before it leaves containment.

**Van flow:**
- Dirty items load from the back forward. The PPE bag and meters stay high and forward.
- Plastic off open-grate dividers on dirty jobs.

**Crew simplification, so watch for:** The lead checks:
- exposed tack strip (cover it, or remove it on unsanitary water);
- cord and condensate routing;
- that nothing contaminated was carried through clean rooms unbagged.

**Kit:** `trash_management_and_logistics`, `demolition.tree.physical_sequence.nail_removal`, `equipment_setup.taping_and_routing`, `van_organization.clean_dirty_flow`, `van_organization.cab_separation_and_contamination_control`, `safety_and_health.stops` (tack strip)

### 2.2 Standard post-demo cleaning (base, end of demo day)

**Why:**
- Demo dust carries spores, fragments, and soil. Leaving it raises odor and musty-callback risk and spreads contamination once air movers start.
- A clean structure dries better.
- In the kit, the post-demo clean is a repeatable checklist, not an optional step, and it is often rushed in the field.
- **The thinking behind the crew line:** read what's dirty and where, check the tools on hand, and take the path that gets the cleanest result in the time available. Top down, and move dirt toward the floor instead of chasing it with a rag.

**How (full):** the company minimum.
1. **HEPA vacuum the loose debris.** Remove heavy debris first, then pick up the loose load so the blow-down isn't pushing chunks around.
2. **Dry blow-down, with the AFD / air scrubber running for dust control.** Blow top to bottom: ledges, door and window frames, top plates, tops of cabinets, boxes, and other horizontals, down to the floor. The ULV fogger with the liquid off is the handiest tool here, with a nice focused air jet; a fan or leaf blower also works. The air scrubber captures what goes airborne. (See "Where the blow-down happens" below.)
3. **HEPA vacuum the floor while it's dry.** Pick up what the blow-down brought down before anything damp touches it. Fine drywall dust turns pasty when damp, smears, and loads the HEPA filter.
4. **Damp wipe** exposed framing, plumbing, wiring, electrical boxes (inside them too), and horizontals.
 - **Direct application:** mist with a pump sprayer and wipe, or use a wet rag, the tech's call based on tools on hand.
 - The moisture breaks surface tension and static so dust lets go. Keep it damp, not wet, near open electrical.
 - Because the blow-down and floor vac already moved the loose dust, the rag is only picking up residual dust, not dirt, so one rag goes roughly ten times further.
 - Fold rags for clean faces (the kit's microfiber tip: fold twice for 8 faces).
5. **HEPA vacuum the floor last,** with detail at corners, base plates, and gaps. Everything the earlier steps moved down ends up here.
6. Stain remover or sealer only when justified, after removal and cleaning, and with client approval. It is cosmetic.

**Why this order:** Each step makes the next one easier.
- The vac takes the bulk so the blower moves dust, not debris.
- The blow-down puts dust where the floor vac gets it, and vacuuming it dry keeps it from turning to paste.
- The damp wipe only picks up a film, and the final vac collects everything that came down.

It's less labor than HEPA, wipe, HEPA, and the result is better because the rag isn't smearing dirt. It also follows the kit's rule for cleaning stacks: never move dust onto a surface you already cleaned.

**Optional light ULV fog (escalation, not base):** For extra-dusty jobs or haze the air scrubber hasn't cleared, a light fog before the damp wipe knocks airborne dust down. Technique when used:

- Light means flash-off, not a bath. Mist the air and surfaces lightly, and it should be gone in a short time. If it's running down the walls or pooling, that's too much. This matches the kit's fog rule ("fog is flash-off, not a bath").
- Work from the far side of the space toward the exit, top down.
- Keep the AFD running. Keep the mist off open electrical (boxes, panels, energized equipment) and out of cavities or ducts you can't see and clean.
- Train a tech on the fogger before they use it for fog. Fogger output and droplet size vary by model, so the "how light" setting is per unit. **[verify per fogger model]**
- **What goes in the tank** for the optional light fog (plain water, or a cleaning solution at its label dilution) is not written yet. **Company decision needed.** If it's a product, its label governs whether it may be fogged, and its PPE and re-entry rules apply.

**Where the blow-down happens:** Inside the demo setup, which normally already has plastic up and an air scrubber running. Kit background: air washing belongs in a controlled area with HEPA capture, not as open air movement through the house.

**Readings after fog:** Don't surface-meter right after fogging. Wait for flash-off, or hammer-probe framing if you need a structural number.

**Occupants:** The kit bars fogging in occupied buildings and homes with infants, elderly, or chemically sensitive occupants. That rule is written for biocide fogs. Whether it also applies to a water-only knockdown fog is a company call (tied to the tank decision above). Until it's settled, occupants and pets stay out of the area while fogging.

**Scope sheet lines:** HEPA vac SS 71 (circle light or heavy, then SF or hours), cleaning solution SS 66 (if the sprayer, wipe or fog uses one), clean studs / walls / joists SS 67–69, cross-contaminated areas SS 72, clean other SS 74.

**Decisions / edge cases:**
- **Category 3 slab-on-grade with heavy soil:** the kit's alternative is pressure wash plus extractor running the whole time, then dehumidify. Never on a wood subfloor.
- **Heavier mold decon vs standard post-demo clean:** if growth is found, it becomes a mold scope under containment with minimum negative before disturbance (see 2.3).
- **Heavy soil or sludge:** physical cleaning first. Neither fog nor antimicrobial goes on over it.

**Crew simplification, so watch for:**
- The crew gets five steps. The lead watches for:
 - blowing with no air scrubber running, or through an open house;
 - over-fogging (wet walls, pooling, wet framing right before readings);
 - fog near open electrical;
 - wiping before the blow-down (smearing dirt instead of picking up dust);
 - skipping the final floor vac.

**Kit:** `demolition.tree.post_demo_clean.demo_final_cleaning`, `phases.phase2.sequence` (Post-Demo Foundational Cleaning), `general_cleaning`, `mold_cleaning.cleaning_stacks` (`rule`, `pre_dryout`, `fog_rule`, `wipe_gate`), `ulv_vs_hand_pump_sprayer`, `drying_and_monitoring.moisture_after_spray`, `demolition.tree.post_demo_clean.demo_final_cleaning.practical_guidance` (microfiber folding)

### 2.3 Adjust to the job

The crew line: "Use antimicrobial for mold, Category 2 or 3 water, or anything with legal or insurance stakes. Whatever you do goes on the scope sheet." This replaces the earlier "antimicrobial after demo is our default" position. The damp wipe in 2.2 is the everyday minimum. A light ULV fog and antimicrobial are escalations.

#### Escalate to antimicrobial

**When:**
- Mold: visible growth, or musty odor beyond the spot.
- Category 2 or 3 water, including clean water that degraded with dwell time (see Read first, "Category sets the controls").
- Legal or insurance stakes: disputes, claims likely to be scrutinized, sensitive occupants with a documented concern, or anything the PM flags.
- A clean Category 1 that stayed Category 1 generally does not get one. This matches the kit.

**Why it isn't the default:** Kill is not removal. Dead spores and fragments remain a reservoir, so physical cleaning (2.2) does the work and antimicrobial is a supplement where conditions call for it.

**Requirements whenever it's used:**
- **Consent, once, in the Day 1 paperwork** with the work authorization, so it's on file if the job escalates. Brief the customer, have the label (active ingredients) and SDS available, and get written consent. A "no" can change the scope.
- **One registered product, at the label rate.** Application rate and wet contact time come from the label. No under-label "light pass." A method not on the label is not used. Fog only if the label allows ULV or fogging for that use.
- **Trained applicator, label PPE,** occupants and pets out, re-entry time posted, HVAC serving the area off and isolated.
- **Pre-cleaned surfaces** (2.2 done first). Never spray over heavy soil or sludge.
- **Record:** product, method, time, quantity, dilution, and location, with SS 76 (Y/N) and square footage on SS 77 (floor) and SS 78 (walls and other).
- **No claims beyond the label,** to the customer, adjuster, or in the file. Don't say "sanitized" or "mold-free."
- **Sensitive occupants:** no biocide fogging in occupied homes or homes with infants, elderly, or chemically sensitive occupants. No fog into a cavity or system you can't see and clean afterward unless the label covers it. In finished, occupied spaces use a pump sprayer only if approved.
- **Applicator choice (after the decision, not a reason to apply):** prefer ULV for small complex spaces, open joists, two-story walls, and 1,000+ sq ft of surface.
- **A "legal or insurance stakes" treatment on a clean Category 1** is a company choice made for the customer, not something the standard requires. It's never billed or described to the adjuster as required.

**Company decision needed:**
- the consent language in the Day 1 paperwork;
- what counts as "legal or insurance stakes," and how a clean Category 1 treatment under that trigger is billed;
- which registered product (and whether its label allows ULV), and who counts as a trained applicator.

#### Containment jobs and teardown

The crew version no longer has a containment subsection. The crew carries the plastic tip only, and the lead runs and teaches the build and teardown below.

**Why:**
- Containment limits cross-contamination and reduces air volume, which makes every dehu and air mover more effective.
- Under negative pressure, any leak moves air into the work area instead of out of it.
- Teardown releases settled dust. Plastic taken down dirty, or out of order, undoes the clean.

**How (full):**
1. **Build.**
 - Minimal containment (doorway isolation, floor protection) is the baseline on every job, even clean Category 1.
 - Full containment with negative pressure and an airlock goes up before demo or when contamination risk exists.
 - Extract first on most losses. Containment before extraction is the exception: sewage spreading into clean occupied areas, a known mold disturbance, suspect asbestos or lead in the path, or occupants who can't leave.
 - Keep containment 18 inches to 2 feet beyond affected materials when possible.
 - Shut down HVAC and cover supplies and returns properly. Never bag a live return.
2. **Pressure.**
 - **Water-only jobs:** about −5 Pa or more negative is the kit target, with 4+ ACH when sizing. A quarter bounce on 6-mil plastic is a quick check, not verification.
 - **Mold scope:**
 - nothing is disturbed until containment is up and a minimum of −5 Pa (−0.02 in. WC) is established, verified by manometer, plastic direction, or indicator smoke.
 - Use 4 ACH drawn from the entry across the work area to the farthest point, exhausted outside when possible. Poly is 6-mil fire-retardant.
 - A breach or loss of pressure stops work until it's restored, and the breach is reported and recorded. The manometer reading is the record.
 - Place the negative air machine on the wall farthest from the door, with makeup air on the door wall as far from the machine as possible.
3. **Every monitoring visit:** re-verify containment integrity and pressure. Fix blowouts with extra poles, a second tape line, or staples with cardboard backers. Log them, and note repeat locations.
4. **Before teardown (the gate).** Teardown waits until final verification passes: moisture goals met in the materials, and the restorer evaluation done (see 2.4). On a mold scope with independent verification in the job, containment and air machines stay on until the independent party passes it.
5. **Clean inside before teardown:** HEPA vacuum, wipe, then HEPA vacuum again, top to bottom. This is the kit's post-dryout stack: HEPA vacuum, wipe, optional fog only if a biocide line is approved, wipe the settled residue, final check. Do not blow air and do not run a second dry at this stage. Repeat until it passes.
6. **Teardown:**
 - Keep the AFD or negative air running while plastic comes down. **[verify: kit keeps air machines on until the evaluation passes but does not spell out running them during plastic removal]**
 - Mist the plastic before folding to hold dust. **[verify]**
 - Fold the plastic dirty side in, and bag it inside containment.
 - Bags leave via the decon area, double-bagged or with the exterior wiped.
7. **After teardown:** vacuum the floor where the plastic stood, clean any teardown dust, then do the final walk.

**Decisions / edge cases:**
- **Limited containment** (capture at the tool, local barrier) is for investigative openings or very small spots with no red flags. Red flags are visible moisture beyond the spot, long dwell, a basement or crawl location, sensitive occupants, or musty odor beyond the spot. Any red flag means full containment. Doing a small mold removal with less is a written deviation.
- **Mold scopes over a few square feet:** consider a decon chamber. Field rule of thumb: at least 3×3 ft, ideally 4×4 ft.
- **When cleaning is done but drying continues,** the negative machine can switch to recirculation to keep warm, dry air in. On a mold scope, negative stays until the evaluation passes.

**Scope sheet lines:** negative pressure / decon chamber SS 13, containment SF SS 14, poles SS 15, zippers SS 16, 2x4s SS 17, air scrubber SS 84, lay-flat SS 90, equipment decon SS 93, PPE SS 95–98.

**Crew simplification, so watch for:**
- The crew line carries only the plastic tip. Teardown order is a lead job until it's trained.
- The lead owns:
 - the containment level decision;
 - the teardown sequence and dirty-side-in bagging;
 - the pressure target and its record;
 - the gas appliance check;
 - the verification gate before teardown.
- Teardown before the data says done is one of the fastest ways to create a callback.

**Kit:** `containment` (`philosophy`, `when_to_use`, `recommended_sequence`, `mold_pressure`, `mold_pressure_layout`, `air_filtration_setup`, `blowout`, `hvac_intake_ban`), `engineering_controls` (`negative_pressure_targets`, `practical_guidance`, `gas_appliance_backdraft`), `equipment_setup.containment_first_exceptions`, `demolition.tree.controls_and_limits.limited_containment_demo`, `mold_cleaning.cleaning_stacks.post_dryout`, `final_verification.mold_verification`, `phases.phase4.sequence` (Pre-Verification Controls & Safety Gate; Controlled Teardown & Site Restoration), `trash_management_and_logistics.contaminated_material`. Antimicrobial: `ulv_vs_hand_pump_sprayer` (`key_rules`, `when_not_to_use_ulv`, `consent_and_records`, `safety_requirements`), `legal_and_liability.informed_consent_antimicrobials`, `legal_and_liability.must_not_claim`, `mold_cleaning.kill_then_remove`, `base_science.mold_science.common_misunderstandings`, `safety_and_health.stops` (label rule), `demolition.tree.controls_and_limits.limited_containment_demo.framing_treatment`

### 2.4 Final check (before we call it done)

**Why:**
- The restorer's own check is what lets containment come down and the job close.
- On a mold job, the restorer's evaluation has defined parts:
 - visible growth and associated dirt, dust, and debris gone;
 - no malodor;
 - towel-wipe clean;
 - remaining materials dry.
- The towel wipe is the "rag swipe."

**Wording matters:**
- The kit separates the restorer's **post-remediation evaluation** from the independent party's **post-remediation verification**.
- Never call our own check "clearance" or "verification," and never tell anyone the house is "mold-free," "safe," "cleared," or "passed" without the independent verification that says so.
- The crew title is now "Final check (before we call it done)." This is our post-remediation evaluation. Calling for an outside inspection, when one is scoped, comes after it passes.

**How (full):**
1. **Water jobs:**
 - final moisture verification at all fixed points plus any borderline or suspect areas;
 - same meter, same locations;
 - each material at or above its dry standard, within 10 percent where that applies;
 - timestamped readings and photos.
 - Equipment stays until the goal is verified in the materials, not when the air feels dry.
2. **Mold or contaminated scopes:**
 - **visual:** no visible growth, dust, or debris;
 - **odor:** no musty smell;
 - **towel wipe:** a few representative spots;
 - **dry:** materials at goal.
 - Fail anywhere: HEPA vacuum and wipe again, then recheck. Repeat until it passes before scheduling an independent inspection.
3. Inspect opened cavities, subfloor, the crawl, and under cabinets for remaining moisture, staining, or growth.
4. Photograph, then write the evaluation in the file. If there is no independent verification, air scrubbers stay on until this check is done and written. On the scope sheet this is SS 75 (check cleaning) and SS 74b (final cleaning), and the "after" pictures for the QA checklist.
5. **Independent verification** is recommended when the clean is uncertain, occupant health is a concern, or the owner wants sampling. It is in the job only when scoped.

**Decisions / edge cases:**
- **Material that can't reach the goal** is an unrestorable call, documented.
- **Contents check:** visual, odor, towel wipe, and dry. Contents go back after the final clean.
- **A reported health issue** gets an independent assessor. Health questions go to a healthcare professional.

**Crew simplification, so watch for:**
- The crew check is a close look and a rag swipe. The flashlight test was cut because nobody will do it.
- The lead adds the two parts the crew line leaves out: an **odor** check and **moisture at goal**.
- The lead also decides whether independent verification is in the job.

**Kit:** `final_verification` (`restorer_evaluation`, `mold_verification`, `practical_guidance`), `mold_cleaning.cleaning_stacks.post_dryout`, `base_science.dry_standards`, `legal_and_liability.who_decides_what`, `legal_and_liability.must_not_claim`, `glossary` (post-remediation evaluation / verification), `phases.phase4.sequence` (Comprehensive Final Moisture Verification; Structural, Cavity & Contents Inspection), `safety_and_health.stops`

### Containment tip (crew: "20 minutes of plastic saves an hour of cleaning")

**Why it holds up:**
- In the kit's framing, plastic is billable and cheap for the customer.
- Reducing air volume is one of the highest-ROI moves on any job, because containment lets fewer machines dry the same space.
- Dust that never escapes never has to be cleaned.

**For the lead:**
- Mark the layout with double-sided tape first.
- Use 10-ft plastic hung vertically, ceiling first, then alternate sides down.
- Leave a foot or more of extra plastic at the walls.
- Double-tape seams on dirty Category 2 and all Category 3 jobs.
- Running negative pressure means more poles, especially in small rooms.
- Bill it on the scope sheet (1.5): floor protection SS 3–5, containment SS 13–17.

**Kit:** `containment.core_mindset`, `containment.philosophy.even_category_1`, `containment.recommended_sequence`, `equipment_setup.practical_guidance`, `equipment_setup.sizing_and_calculations.variance_factors`

### Air-test (IEP) jobs

**When this applies:** Any job where an independent environmental professional (IEP) will air-test or sample for post-remediation verification, or where the expected outcome is a near-zero spore count.

**Why the 2.2 minimum isn't enough:** The everyday minimum is built for the best result in the time available. An air test grades the result against outdoor or control samples, so leftover fine dust fails it. These jobs need a strict, sequenced procedure in which each step captures what the previous step disturbed, under verified containment and negative pressure, with nothing re-contaminating a surface already cleaned.

**Procedure:** *Placeholder.* A detailed protocol of this kind is to be added. Until then, use the containment, pressure, and teardown gates in 2.3, the post-dryout stack (HEPA vac, wipe, fog only if an antimicrobial is approved, wipe the settled residue, final check, with no blow and no second dry), and the 2.4 evaluation before the IEP is called.

**Kit:** `final_verification.mold_verification`, `mold_cleaning.cleaning_stacks.post_dryout`, `containment.mold_pressure`, `legal_and_liability.who_decides_what`

---

## 3. Crew Training

Each session is short and hands-on. Below are the learning objectives, what "done" looks like, and the lead's talking points.

**Company decision needed (all sessions):**
- who leads each session;
- whether sessions run at the crew meeting or on a slow shop day;
- whether completion is recorded, and where.

### 3.1 Dehu setup

- **Objectives:**
 - Reset job hours.
 - Set the humidistat, especially in small rooms and tents.
 - Find and log the unit number.
 - Read the screen for the photo.
 - Set placement: clearance, tray, and condensate routing.
- **Done looks like:** the tech places a unit, and the photo shows the readout and unit number. The condensate line has no dips, and the tray is in place.
- **Lead adds (not crew-level yet):** inlet/outlet readings to GPP, the 15–25 grain healthy range, back-pressure freeze in tents, small-room overheating.
- **Kit:** `equipment_setup.equipment_field_basics`, `equipment_setup.taping_and_routing`, `drying_and_monitoring.practical_guidance`, `drying_and_monitoring.dehumidifier_ducting`, `drying_and_monitoring.tenting`
- **Company decision needed:** the fleet model list and a one-page quick reference per model.

### 3.2 Scope sheet and photos

- **Objectives:**
 - One sheet per job per day, or per room on big jobs (mitigation scope sheet template).
 - The QA checklist at the bottom completed before leaving.
 - Every sheet item photographed.
 - Wide, then close.
 - Meter screen and material in the same frame.
 - Readings recorded exactly as read.
- **Done looks like:** a tech's day of photos can be matched line-for-line to the sheet by someone who wasn't there.
- **Lead adds:** the integrity rule (never smooth or backfill readings), and photographing judgment calls.
- **Kit:** `documentation`, `insurance_dynamics.honesty_guard`, `legal_and_liability.records_and_retention`, `templates/mitigation_scope_sheet_template.json`, `logs/scope_sheet_template.json`

### 3.3 Getting to know the water

- **Objectives:**
 - Walk a real job with a lead.
 - Follow the water from wet to dry.
 - Check both sides of walls, the room beyond, and under cabinets.
 - Understand why the edge sets the cut line.
- **Done looks like:** the tech finds the same edge as the lead within reason, and can explain where the water went and why.
- **Lead adds:**
 - layered assemblies and lids;
 - non-invasive meter depth (about ¾ inch);
 - the dry standard from unaffected material;
 - reading-point placement **[verify spacing]**;
 - crawl hatch size-up and the 4-gas rule before any crawl portion.
- **Kit:** `base_science.water_movement_pathways`, `base_science.material_behavior`, `demolition.tree.decision_logic.chasing_the_water`, `monitoring.fixed_point_techniques`, `crawlspaces.tree.safety_and_access`

### 3.4 Broken equipment tag

- **Objectives:**
 - Tape the problem, date, and initials.
 - Pull the unit from service.
 - Remove warm or damaged cords immediately.
- **Done looks like:** no untagged failed unit reaches the shop.
- **Lead adds:** logging the swap on the job, and cleaning units off contaminated jobs **[verify; Company decision needed]**.
- **Kit:** `extension_cord_safety`, `electrical_safety` (tag system is a kit gap)

### 3.5 Cleaning

- **Objectives:**
 - Read the job: what's dirty, where, what tools are on hand, how much time.
 - The after-demo minimum in order: HEPA, dry blow-down with the air scrubber running, HEPA, damp wipe (sprayer and rag, or wet rag), HEPA.
 - When to escalate to antimicrobial: mold, Category 2/3, legal or insurance stakes.
 - The final check: close look and rag swipe.
 - The plastic tip.
- **Done looks like:** the tech runs the five steps without prompting, never wipes before the blow-down, keeps the wipe damp rather than wet, and logs what was done on the scope sheet.
- **Lead adds:**
 - blow-down isolation and capture (2.2);
 - label, consent, and record requirements for any antimicrobial (2.3);
 - no biocide fog in occupied spaces;
 - no metering right after fog or spray;
 - containment build, the verification gate, and teardown order (2.3);
 - correct wording (evaluation vs clearance);
 - air-test (IEP) jobs follow the strict procedure, not the minimum.
- **Kit:** `demolition.tree.post_demo_clean`, `general_cleaning`, `mold_cleaning.cleaning_stacks`, `ulv_vs_hand_pump_sprayer`, `legal_and_liability.informed_consent_antimicrobials`, `containment`, `final_verification.restorer_evaluation`
- **Depends on:** the manager's consent sign-off (2.3).

### 3.6 Arrival and departure sets

- **Objectives:**
 - When to shoot: demo days and layout changes.
 - From the corners, inside out, same angles each time.
 - Clean up first.
- **Done looks like:** the departure set shows every piece of equipment and the airflow direction, and could serve as tomorrow's "before."
- **Lead adds:** what counts as a layout change (1.2 list), shooting extra sets on stalled rooms, and same-day photos of any scope change.
- **Kit:** `documentation.key_habits`, `documentation.decision_criteria`, `equipment_setup.practical_guidance`

---

## Flags collected

### [verify]

1. Reading-point placement: about 24 inches from the wall and 8–10 ft grid spacing. This is common practice, not in the kit (1.1, 3.3).
2. The dehu screen may show only RH and temperature depending on the model, so the readout photo may not equal grain depression (1.6).
3. Equipment cleaning off contaminated jobs before repair or reuse. The kit has no procedure (1.8, 3.4).
4. Running the AFD or negative air during plastic removal (2.3).
5. Misting plastic before folding at teardown (2.3).
6. Light-fog output setting per fogger model (2.2).

### Company decision needed

1. 4-gas policy for crawl entry, and meter ownership and bump testing (Read first).
2. Written respirator program and fit-test records (Read first).
3. Monitoring-visit photo policy on long dries (1.2).
4. Standard flood cut height and exceptions written into the scope or estimating notes (1.4).
5. Scope sheet template review: it stands in as the provisional billable list until then. Include estimating alignment and the lines in the template's transcription notes (1.5).
6. Fleet dehu models, large vs XL for SS 80–81, and the billing source of truth (hour meter vs job-app dates) (1.6, 3.1).
7. Barcode stickers, inventory tie-in, and per-unit tracking scope (1.7).
8. Shop handling for tagged units: triage, return-to-service, contaminated-equipment cleaning standard (1.8).
9. Antimicrobial: position decided (when conditions call for it: mold, Category 2/3, legal or insurance stakes; label rate; Day 1 consent). Your manager signs off on the consent language, defines "legal or insurance stakes," and decides Category 1 billing under that trigger. Product and applicator training are still open (2.3, 3.5).
10. Training owners, venue, and completion records (3.x).
11. Light ULV fog: what goes in the tank, and whether the kit's no-fog-in-occupied-homes rule applies to it (2.2).
12. (Resolved: blow-down happens inside the demo setup.)
14. Air-test (IEP) procedure: detailed protocol to be added (Air-test (IEP) jobs).
