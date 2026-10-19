# Encircle Crash Course for Field Techs (iPad)

Button-by-button recipes for the Encircle app. Each task is a
heading, one tap path, and at most two notes.

> **Read this first**
>
> - Unofficial training aid, built from Encircle's own help
>   articles (sources at the end), checked October 18, 2026.
> - **Bold** = a button or label shown in Encircle's docs.
>   **>** = tap next.
> - **[verify in app]** = not confirmed in the docs. Check it
>   on your iPad.
> - Your company's rules come first.
>
> **One-page sheets:** [Tech sheet (daily work)](encircle_cheat_sheet_tech.md)
> ([PDF](encircle_cheat_sheet_tech.pdf)) and
> [PM / Lead sheet (setup and oversight)](encircle_cheat_sheet_lead.md)
> ([PDF](encircle_cheat_sheet_lead.pdf)).

---

## Contents

1. [Moisture (Hydro)](#1-moisture-hydro)
2. [Before you go](#2-before-you-go)
3. [Login and the claim list](#3-login-and-the-claim-list)
4. [Jobs](#4-jobs)
5. [Floor Plan](#5-floor-plan)
6. [Rooms](#6-rooms)
7. [Photos and videos](#7-photos-and-videos)
8. [Notes and job events](#8-notes-and-job-events)
9. [Forms and signatures](#9-forms-and-signatures)
10. [Contents](#10-contents)
11. [Reports](#11-reports)
12. [Offline and sync](#12-offline-and-sync)
13. [Xactimate (estimator)](#13-xactimate-estimator)
14. [First water job, in order](#14-first-water-job-in-order)
15. [Common mistakes](#15-common-mistakes)
16. [Questions to ask your company](#16-questions-to-ask-your-company)
17. [Older Hydro screens (pre-2023)](#17-older-hydro-screens-pre-2023)
18. [Sources](#18-sources)

---

## 1. Moisture (Hydro)

These recipes follow Encircle's current Hydro screens (the
August 2023 redesign) and the current help center.

**Where you are**
- **Claim** home > **Hydro** opens the Hydro dashboard. Its
  tiles are **Tasks**, **Alerts**, **Psychrometrics**,
  **Materials**, **Equipment** and **Summary**.
- The **Tasks** tile opens the task list. Day 1 is
  **Job Setup**, then **Visit 1**, **Visit 2** and so on.
  Tasks can be done in any order. A lock means another task
  comes first.

### Open the task list

**Claim** > **Hydro** > **Tasks** tile (**Start Here** on day 1)

- A new job's button reads "Start water job." After setup it
  reads "Hydro: Visit #."

### Set the source of loss

**Tasks** > **Source of Loss and Category of Water** > enter the source > pick the **Category of Water** > tick **Hazardous Materials** if any > **Complete**

### Set up the drying chamber (do this before chamber readings)

**Tasks** > **Drying Chamber** > tick each room, mark **Affected** or **Unaffected** > **Done** > **Drying Chamber Name** > **Complete Task** (or **Add Another Chamber**)

- **Chamber first.** Completing this task unlocks a
  "Drying Chamber – [name]" group for each chamber, with
  **Affected Area Reading**, moisture points, dehu readings
  and the other chamber tasks. Until then, the
  **Psychrometrics** tile reads "No chambers."
- Room missing? Tap **+ Add** in "Select rooms in chamber."
  Include the unaffected rooms in the chamber too.

### Add a material and its dry standard

**Tasks** > **Dry Standard** > pick the material (or **+ Add** if it's not listed) > next to Meter, **Change** > Meter and Probe Type > **Change Meter** > **Add Meter Photo** > shutter > **Done** > check Moisture Content > **Drying Variance** (10% default) > **Save**

- Next material: the red **+** on the Dry Standard list. Do
  one for every wet material on the job. Hydro remembers the
  meter for that material.
- Read the same material in a dry, undamaged area. Hydro
  shows Dry Standard, Variance and **Dry Goal** for each one.

### Add a moisture point (one per material, per room, no map)

**Tasks** > **Moisture Points** > **Place moisture points** (next to the room) > tick the material > **Done**; next material in that room: tap the room > red **+** > **Moisture Point** > tick the material > **Done**

- One point for each affected material in each room. The
  task list may show the task as **Moisture Point**.
- Optional, when a carrier or job asks for a map: **Room
  Moisture Map** > **Place** > **Place Existing** >
  **Moisture Point** tab > **Place All**.

### Take a moisture reading (first or daily)

**Tasks** > **Moisture Content Readings** (day 1: **Moisture Points**) > pick the room > **Tap to take reading** on the material > **Add Meter Photo** > shutter > **Done** > check Moisture Content > **Save** > next material > **Complete** (end of visit)

- Read the wettest spot of that material in the area today;
  it can move. Take the meter photo.
- The meter photo fills in the number (OCR), so check it.
  Tramex MEX5/CME5: **Take Bluetooth Reading**. The room
  layout on a visit's **Moisture Content Readings** screen
  isn't shown in the docs. [verify in app]

### Every visit: air and dehu readings (all four)

**Tasks** (**Visit #**) >
1. Outside: **Exterior Reading** > **Add Meter Photo** > Temperature + Relative Humidity > **Save** (or **Use** next to Current Weather)
2. Unaffected: **Unaffected Area Reading** > pick the room > **Add Meter Photo** > Temperature + Relative Humidity > **Save**
3. Affected, each chamber: **Affected Area Reading** (under "Drying Chamber – [name]") > pick an affected room > **Add Meter Photo** > Temperature + Relative Humidity > **Save**
4. Each dehu: **Dehumidifier Readings** > pick the room > **Tap to take reading** on the dehu > **Add Meter Photo** (meter at the exhaust) > **Add Timer Photo** (hour meter) > Temperature, Relative Humidity, Hours Running > **Save**

- **Exterior and Unaffected are reference readings and work
  without a chamber. Affected and dehu readings sit under
  each chamber, so set up the drying chamber first.**
- Use the same affected room every visit. For the next
  room's dehus, use the room selector at the top. HVAC
  readings show up only if you chose to monitor HVAC.

### Finish the visit

**Tasks** > **Complete** (bottom of the task list)

### Fix or add a past visit's readings

**Hydro** > **Tasks** tile > **⋯** (top right) > **Change Visit** > pick the visit > task (**⋯** to edit a completed one) > **X** to go back

### Place equipment (Quick Add)

**Tasks** > **Equipment Placement** > red **+** > pick the room > **+** next to each equipment type > room selector for the next room > **Place**

- If you see a list of models and asset IDs instead, your
  company uses Inventory equipment. The step-by-step for that
  is in Encircle's video. [verify in app]
- Adding equipment on a later visit isn't shown in the docs.
  [verify in app]

### Get the recommended equipment count

**Tasks** > **Room & Affected Area Dimensions** > each room (shape, sizes, % wet) > **Complete** > **Complete Task**; then **Equipment Calculation** > answer the drying factors > **Calculate** > **Complete Task**

### Remove equipment

**Hydro** > **Equipment** > **Days On Site** tab > **⋯** next to the unit > **Remove From Job** > **Yes**

- All of it (job dry): **Equipment** > **⋯** (top right) >
  **Remove All Equipment** > **Yes**.
- Pull it in the app the day you pull it on site. That's what
  sets the days on site.

### Chamber status, category, class

**Tasks** > **Drying Chamber Settings** > Status (**Stabilization**, **Drying**, **Dry Confirmed**), Category, Class > **Save**; later: **Hydro** > open the chamber > **⋯** > **Manage Drying Chamber**

- Change rooms here with **Edit Rooms**. Leave the tolerances
  at the company defaults unless a lead says otherwise.

### Moisture (Hydro) report

**Claim** > **Documents** > **Generate Report** > **PDF Report** > **Hydro Full Report**, **Hydro Summary Report**, **Hydro Equipment Report** or **Hydro Carrier Report** > fill in the details > **Generate Report**

- These steps are written for the web app. Encircle says
  mobile is similar. [verify in app]

---

## 2. Before you go

### Download the job for offline

**Claim** > **☰** (top right) > **Download Data**

- Do it while you still have signal.

---

## 3. Login and the claim list

### First login

Invite email > **Accept Invitation** > **Create Account** > install **Encircle** > **Log In** > **I'm here for business** > sign in

### Find a job

Claim inbox > **My Claims** (jobs shared with you) or **All Claims** > search by name, claim #, job # or address

### Claim shortcuts

**My Claims** > press and hold the claim > contact, view, edit, share, leave, delete, close

- Leave claims when your part is done. It keeps the list fast.

---

## 4. Jobs

### Create a job

**Add Claim** > **Only One Structure** or **Multiple Structures** > template (or **Default**) > loss info > at least one claim identifier > **Save**

- Usually the office or an integration creates the job.
  Check **My Claims** first.

### Edit claim details

**Claim** > **pencil icon** (top)

---

## 5. Floor Plan

### Start a scan

**Claim** (or the **structure**) > **Add Floor Plans** > **Let's Scan** > red **record**

- Limited users can't scan. Standard and Admin users can.

### Open the finished plan

**Claim** home > **Floor Plan** > tap the plan

- You get an email when it's ready (within 6 hours, about
  90 minutes on average).

### Make a room sketch from it

Open the plan > **Create Sketch** > name it > **Save** > crop the room > **Save** > pick the room > **Save**

### Report wrong dimensions

Open the plan > **wrench** (bottom right) > describe it > **Send**

---

## 6. Rooms

### Add a room

**Claim** home > **Add Room** > name > **Done**

- Use real names (Kitchen, Bedroom 1, Closet 1). Never
  "Before" or "Day 2."

### Rename, move or delete a room

**Claim** home > press and hold the room > **Edit**, **Move** or **Delete**

---

## 7. Photos and videos

### Overview photos

**Room** > **+** > **Add Photos & Videos** > shoot (the volume button works) > **Done**

- Start at the door and go left to right, iPad upright.
  **Video** switches to video.

### Move photos to the right room

**Room** > **Select** (top right) > pick photos > **Move** > structure > room

- Photos in the wrong *claim*: ask the office.
  [verify in app]

### Mark up a photo

Open the photo > **Markup**

- **Blur** hides faces, addresses and documents.

### Add photos from the iPad (FLIR, other apps)

**Room** or note > **Gallery** > **Pick from Device Gallery**

---

## 8. Notes and job events

### Room note (close-ups with a label)

**Room** > **+** > **Add Room Note** > title / description > add photos > **Save**

- Use one for the source of loss, pre-existing damage,
  hazards and mitigation complete.

### Use a note template

Inside a note > template icon (sticky note with a paper clip) > pick > **Use**

### General note (whole job)

**Claim** home > **General Notes** > red **+**

### Log a job event

**Job Events** icon (bottom) > **+** > pick the event > date and time > **Save**

---

## 9. Forms and signatures

### Fill in a form on site

**Claim** > **Documents** > **Generate Report** > **PDF Report** > pick your company's form > fill it in > save

- The customer signs on the iPad. It works offline.

### Send a form to sign remotely

**Claim** > **Share** tab > **Add Link** > email, SMS or both > rooms / documents > **Preview & Sign** (if you sign too) > **Share**

---

## 10. Contents

### Add a contents item

**Room** > **+** > **Add Contents** > photo > **Details** > **Set Disposition** > box (scan the QR or type it)

- The box and disposition carry over to the next item. Change
  them when you switch.
- Serial plate: **Details** > **Add Data Tag Photo**.

---

## 11. Reports

### Full job report from the iPad

**Claim** > **Documents** > **Generate Report** > **PDF Report** > **Encircle PDF Report** > **Everything** > **Report Title** > **Show Psychrometrics & Drying Information**: **Yes** > **Save**

- For big reports, set **Email Friendly** to **Yes**. The
  office usually builds and sends reports.

### Open or send a report

**Claim** > **Documents** > tap the report > **View PDF**, **Email to Policyholder** or **Send via...**

---

## 12. Offline and sync

### Go offline

**Network** icon (bottom right) > **Network Usage** > **Offline Mode**

### Sync when you're back

**Network** icon > **Wi-Fi + Mobile Data** (or **Wi-Fi Only**) > keep the app open and the screen on > wait for the number on the icon to clear

### Unstick a sync

**Network** icon > **Offline Mode** > wait 10 seconds > **Wi-Fi + Mobile Data**

> **Never delete or reinstall the app with unsynced data.**
> It's lost for good. Encircle support: 1-888-937-1077 x1,
> support@encircleapp.com.

### iPad settings (once)

**Settings** > **Encircle** > **Location** > **While Using the App**; **Settings** > **Display & Brightness** > **Auto-Lock** (longer)

---

## 13. Xactimate (estimator)

### Import the floor plan as a sketch

Xactimate (file closed) > **Data Request** > **Interior Walls** > Floor Plan ID as **Claim Number** > rep email > **Submit** > Sketch > **Data Import** > **Import**

- This needs the integration turned on. $10 per import.
  The ceiling always comes in at 8 ft.

---

## 14. First water job, in order

1. Van: **Claim** > **☰** > **Download Data**
2. Exterior cover photo, then **work authorization** signed
   (Documents > Generate Report > PDF Report)
3. **Add Floor Plans** > **Let's Scan**
4. **Add Room** for every affected and chamber room
5. **Add Photos & Videos** overviews, then **Add Room Note**
   for the source of loss and pre-existing damage
6. **Hydro** > **Tasks** > **Start Here**:
   **Source of Loss and Category of Water** > **Drying Chamber**
   (before any chamber readings) > **Exterior Reading** >
   **Unaffected Area Reading** > **Dry Standard** (every wet
   material) > **Affected Area Reading** (each chamber) >
   **Moisture Points** (**Place moisture points**, one per
   material per room) > first readings > **Equipment
   Placement** > **Dehumidifier Readings** > **Complete**
7. Sync before you leave: no number on the **Network** icon

**Every return visit:** **Hydro** > **Tasks** (**Visit #**) >
**Exterior Reading** > **Unaffected Area Reading** >
**Affected Area Reading** (each chamber) >
**Moisture Content Readings** (wettest spot, meter photo) >
**Dehumidifier Readings** (each dehu) > **Complete**

**Last visit:** final readings > chamber status
**Dry Confirmed** > **Hydro** > **Equipment** > **⋯** >
**Remove All Equipment** > **Yes** > a "Mitigation complete"
room note > sync

---

## 15. Common mistakes

- Equipment left on in the app after it's pulled. The days on
  site keep counting.
- Affected readings taken in a different room each visit.
- No drying chamber set up, so there's nowhere to log the
  affected-area air readings. Chamber first, then
  psychrometrics.
- A visit with only some of the four air readings (outside,
  unaffected, affected, each dehu).
- A daily reading saved without a meter photo.
- A dry standard with a different meter or probe than the
  daily readings.
- Unaffected chamber rooms left out of the chamber.
- Leaving before sync finished. Reinstalling the app to "fix"
  sync, which loses data.
- OCR numbers saved without a glance.

---

## 16. Questions to ask your company

- What's my permission level? Can I create jobs and floor
  plans?
- Who creates jobs? What's the claim naming rule?
- Which Hydro tasks do we skip (moisture map, dimensions,
  calculator)?
- Which meters and probes do we use? Are they set up in the
  app?
- Which photos and note templates are required?
- Which forms must be signed before work starts?
- Who sends reports? Which moisture report do carriers get?
- Who fixes equipment stuck on the wrong job?

---

## 17. Older Hydro screens (pre-2023)

Only for an app that still shows the original screens:
**☰** > **Hydro** inside the claim, with **Job Setup Tasks** /
**Visit # Tasks** lists. Source: Encircle's 2021 Hydro help
articles (now removed), reproduced in
[this contractor manual (PDF)](https://ec.ecrpro.com/job-manual.pdf).
Page numbers below are from it.

- **Open:** **Claim** > **☰** > **Hydro** > **Job Setup Tasks** / **Visit # Tasks** (p. 5, 35)
- **Chamber:** **Drying Chamber** > rooms, **Affected**/**Unaffected** > **Done** > name > **Complete Task** (p. 8)
- **Dry standard:** **Dry Standard** > material > **Meter** > **Probe Type** > Moisture Content > **Drying Variance %** > **Add Another** / **Complete Task** (p. 12–13)
- **Moisture point:** **Moisture Points** > **Without Moisture Map** > **Add** (by room) > material > **Done** > material > reading > **Save** (p. 20–21)
- **Daily reading:** **Visit # Tasks** > **Moisture Content Readings** > tap the point > Moisture Content, **Reading Photo** > **Save** > **Complete Visit #** (p. 21, 36)
- **Air:** **Exterior Reading**, **Unaffected Area Reading** (references); **Affected Area Reading** (locked until a chamber exists) (p. 6, 9–15)
- **Dehu:** **Dehumidifier Readings** > dehu > Temperature, Relative Humidity, Hours Running > **Save** (p. 32)
- **Equipment:** **Equipment Placement** > **Add** > type > **Without Moisture Map** > unit; remove: Hydro **☰** > **All Equipment** > **⋯** > **Remove All Equipment** (p. 27, 37–38)
- **Report:** **Documents** > **Generate Report** > **PDF Report** > **Moisture Full/Summary/Equipment Report** (p. 39–40)

---

## 18. Sources

Encircle's current help center (help.encircleapp.com),
checked October 18, 2026. Section 17 cites its own source.

### Moisture (Hydro), section 1

| Recipe | Help article |
|---|---|
| Where you are, open the task list | [Introduction to Hydro](https://help.encircleapp.com/hc/en-us/articles/18377208883853-Introduction-to-Hydro) |
| Source of loss | [Source of Loss & Category of Water](https://help.encircleapp.com/hc/en-us/articles/18377351266189-Source-of-Loss-Category-of-Water) |
| Drying chamber (and what it unlocks) | [Drying Chamber Setup](https://help.encircleapp.com/hc/en-us/articles/18377668096269-Drying-Chamber-Setup) |
| Material and dry standard | [Dry Standards & Drying Goals](https://help.encircleapp.com/hc/en-us/articles/18378175356685-Dry-Standards-Drying-Goals) |
| Moisture point, moisture reading, optional map | [Moisture Maps & Moisture Points](https://help.encircleapp.com/hc/en-us/articles/18384800011021-Moisture-Maps-Moisture-Points), [Instant Reading Capture](https://help.encircleapp.com/hc/en-us/articles/46355132990733-Instant-Reading-Capture), [Bluetooth (Tramex)](https://help.encircleapp.com/hc/en-us/articles/34387580752653-Taking-Bluetooth-Readings-with-Tramex) |
| Exterior and unaffected readings | [Psychrometric Reference Readings](https://help.encircleapp.com/hc/en-us/articles/18377914971405-Psychrometric-Reference-Readings) |
| Affected readings | [Drying Chamber Psychrometrics](https://help.encircleapp.com/hc/en-us/articles/18384725633165-Drying-Chamber-Psychrometrics) |
| Dehu readings, finish day 1 | [Dehumidifier Readings](https://help.encircleapp.com/hc/en-us/articles/18385065518861-Dehumidifier-Readings) |
| Visit task list, finish a visit | [Subsequent Visits](https://help.encircleapp.com/hc/en-us/articles/18385126323085-Subsequent-Visits) |
| Past visits | [Managing Hydro Visits](https://help.encircleapp.com/hc/en-us/articles/11437886053645-Managing-Hydro-Visits) |
| Place equipment | [Equipment Placement (Quick Add)](https://help.encircleapp.com/hc/en-us/articles/18385052243341-Equipment-Placement-Quick-Add), [Equipment Placement (Inventory)](https://help.encircleapp.com/hc/en-us/articles/32289040620429-Equipment-Placement-Inventory) |
| Equipment count | [Room & Affected Area Dimensions](https://help.encircleapp.com/hc/en-us/articles/20441182432397-Room-Affected-Area-Dimensions), [Equipment Calculations](https://help.encircleapp.com/hc/en-us/articles/18384977214093-Equipment-Calculations) |
| Remove equipment | [Removing Equipment](https://help.encircleapp.com/hc/en-us/articles/18385229916557-Removing-Equipment) |
| Chamber status, category, class | [Drying Chamber Settings](https://help.encircleapp.com/hc/en-us/articles/18384869232141-Drying-Chamber-Settings) |
| Moisture report | [Creating Moisture Reports](https://help.encircleapp.com/hc/en-us/articles/19195881775757-Creating-Moisture-Reports) |
| Task list on/off (admin) | [Customizing the Default Hydro Task List](https://help.encircleapp.com/hc/en-us/articles/9143131047437-Customizing-the-Default-Hydro-Task-List) |

### Sections 2–16

- [Claim inbox (mobile)](https://help.encircleapp.com/hc/en-us/articles/360051465411-The-Claim-Inbox-Mobile-App)
- [Adding a new claim (mobile)](https://help.encircleapp.com/hc/en-us/articles/360051377532-Adding-a-New-Claim-Mobile-App)
- [Accepting an invitation](https://help.encircleapp.com/hc/en-us/articles/360051439751-Accepting-an-Invitation-to-Join-Encircle)
- [User permissions](https://help.encircleapp.com/hc/en-us/articles/360050962451-User-Permissions)
- [Adding and editing rooms](https://help.encircleapp.com/hc/en-us/articles/360051377612-Adding-Editing-Rooms)
- [Labeling rooms](https://encircleapp.zendesk.com/hc/en-us/articles/44384777259405-Best-Practices-for-Labeling-Rooms)
- [Room overview photos and videos](https://encircleapp.zendesk.com/hc/en-us/articles/360051378052-Adding-Room-Overview-Photos-Videos)
- [Moving photos between rooms](https://help.encircleapp.com/hc/en-us/articles/22234018638989-Moving-Photos-Videos-from-One-Room-to-Another-Mobile-App)
- [Photo markup](https://encircleapp.zendesk.com/hc/en-us/articles/25614818587277-Using-Photo-Markup-to-Annotate-Photos-Mobile-App)
- [Uploading FLIR images](https://help.encircleapp.com/hc/en-us/articles/360051964331-Uploading-FLIR-Images-into-Encircle)
- [Room notes](https://encircleapp.zendesk.com/hc/en-us/articles/4405952537229-Adding-Room-Notes)
- [General notes (mobile)](https://help.encircleapp.com/hc/en-us/articles/360055523231-Using-General-Notes-Mobile-App)
- [Events and milestones](https://encircleapp.zendesk.com/hc/en-us/articles/41332642778893-Events-Milestones)
- [GPS location on media](https://help.encircleapp.com/hc/en-us/articles/21287957318029-Capturing-GPS-Location-Data-on-Media)
- [Adding a floor plan](https://help.encircleapp.com/hc/en-us/articles/11397605722253-Adding-a-Floor-Plan)
- [Floor Plan FAQ](https://encircleapp.zendesk.com/hc/en-us/articles/12200869740557-Encircle-Floor-Plan-FAQ)
- [Creating a sketch from your floor plan](https://help.encircleapp.com/hc/en-us/articles/12199419131405-Creating-a-Sketch-from-Your-Floor-Plan)
- [Submitting a fix request](https://help.encircleapp.com/hc/en-us/articles/15252212102413-Submitting-a-Fix-Request-for-Your-Floor-Plan)
- [Where are my custom forms](https://help.encircleapp.com/hc/en-us/articles/360051234012-Where-are-My-Custom-Forms)
- [Requesting photos and signatures (mobile)](https://help.encircleapp.com/hc/en-us/articles/360051856211-Requesting-Photos-Document-Signatures-Mobile-App)
- [Inventorying contents](https://help.encircleapp.com/hc/en-us/articles/360051487632-Inventorying-Contents)
- [Creating a report (mobile)](https://help.encircleapp.com/hc/en-us/articles/21521160943501-Creating-a-Report-Mobile-App)
- [Using Encircle in offline mode (Download Data)](https://help.encircleapp.com/hc/en-us/articles/29297671310477-Using-Encircle-in-Offline-Mode)
- [Syncing data from the field](https://help.encircleapp.com/hc/en-us/articles/12160264408717-Syncing-Data-from-the-Field)
- [Sync troubleshooting](https://help.encircleapp.com/hc/en-us/articles/360050510252-My-data-isn-t-syncing)
- [Importing a floor plan into Xactimate](https://help.encircleapp.com/hc/en-us/articles/18955629046797-Importing-an-Encircle-Floor-Plan-into-Xactimate)
- [Hydro training (Learning Hub)](https://www.getencircle.com/learning/hydro-water-mitigation/)
