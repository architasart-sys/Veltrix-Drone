<div align="center">

<img src="../assets/veltrix_drone_logo.png" alt="Veltrix Drone" width="180">

# Veltrix Drone Android
## Complete User Manual

**Android · Offline-first · Standalone Local Operation · Optional Windows ↔ Android Synchronization**

[Русское руководство](VELTRIX_DRONE_ANDROID_USER_MANUAL_RU.md)

</div>

---

> [!IMPORTANT]
> **Veltrix Drone Android is a standalone application.**
> Windows is not required to create drones, batteries, repairs, flights, attachments, engineering records, local backups, or restores.

> [!NOTE]
> Windows connectivity is optional and can be enabled at any time through:
>
> **More → Exchange & Sync**

> [!WARNING]
> Do not uninstall the application or use Android **Clear Data** if you need to preserve the local Android database. Create a local ZIP backup before updates or major changes.

---

# 📌 Contents

- [1. What is Veltrix Drone Android](#1-what-is-veltrix-drone-android)
- [2. Standalone Architecture](#2-standalone-architecture)
- [3. Installing the APK](#3-installing-the-apk)
- [4. First Launch](#4-first-launch)
- [5. Autonomous Mode](#5-autonomous-mode)
- [6. Navigation](#6-navigation)
- [7. Recommended Initial Setup](#7-recommended-initial-setup)
- [8. Drones](#8-drones)
- [9. Drone Card](#9-drone-card)
- [10. Batteries](#10-batteries)
- [11. Inventory](#11-inventory)
- [12. KITs](#12-kits)
- [13. Components and Node Binding](#13-components-and-node-binding)
- [14. Repairs](#14-repairs)
- [15. Inspections](#15-inspections)
- [16. Scheduled Maintenance](#16-scheduled-maintenance)
- [17. Mission Plans](#17-mission-plans)
- [18. Preflight Checks](#18-preflight-checks)
- [19. Flights](#19-flights)
- [20. Postflight Checks](#20-postflight-checks)
- [21. Attachments](#21-attachments)
- [22. Engineering Modules](#22-engineering-modules)
- [23. Trends and Degradation](#23-trends-and-degradation)
- [24. Configuration Control](#24-configuration-control)
- [25. Technical Cycle](#25-technical-cycle)
- [26. Reliability](#26-reliability)
- [27. Economic Data](#27-economic-data)
- [28. Backups](#28-backups)
- [29. Restore](#29-restore)
- [30. Connecting to Windows](#30-connecting-to-windows)
- [31. First Synchronization](#31-first-synchronization)
- [32. What Is Synchronized](#32-what-is-synchronized)
- [33. Merge Behavior](#33-merge-behavior)
- [34. Android-only Engineering Data](#34-android-only-engineering-data)
- [35. Disconnecting Windows](#35-disconnecting-windows)
- [36. Updating the APK](#36-updating-the-apk)
- [37. Language](#37-language)
- [38. Offline Operation](#38-offline-operation)
- [39. Typical Workflows](#39-typical-workflows)
- [40. Troubleshooting](#40-troubleshooting)
- [41. FAQ](#41-faq)
- [42. Security](#42-security)

---

# 1. What is Veltrix Drone Android

Veltrix Drone Android is a mobile engineering application for UAV fleet operation directly from a phone or tablet.

It stores its own local data and operates independently of the Windows application.

Architecture:

```text
Android
   ↓
local database
   ↓
standalone work
   ↓
optional
   ↓
exchange with Windows
```

It is not a remote control for the Windows application.

---

# 2. Standalone Architecture

Android can independently:

- create and edit drones;
- manage batteries;
- manage inventory;
- manage KITs;
- create repairs;
- create inspections;
- manage scheduled maintenance;
- create mission plans;
- record flights;
- manage Preflight/Postflight records;
- store attachments;
- run local engineering logic;
- create backups;
- restore local backups.

Windows is only required when the user explicitly wants to exchange supported shared data.

---

# 3. Installing the APK

## Step 1 — Download

Download the APK only from the official Veltrix Drone GitHub Release.

The file normally has an `.apk` extension.

## Step 2 — Open

Open the downloaded APK on the Android device.

If Android blocks installation, it may ask you to allow app installation from that specific source.

The wording differs by phone manufacturer.

## Step 3 — Install

Tap:

```text
Install
```

After installation:

```text
Open
```

> [!WARNING]
> Do not install unofficial builds from random file-sharing websites or channels.

---

# 4. First Launch

A new installation starts in standalone mode.

There is no requirement to choose a Windows mode before entering the app.

Correct first-launch flow:

```text
Install APK
→ Open Veltrix Drone
→ Start local work
```

Windows can be connected later.

---

# 5. Autonomous Mode

Autonomous mode is a normal production mode.

In this mode:

- no PC is required;
- no Windows server is required;
- no LAN is required;
- Internet is not required for core local work;
- local records remain on the Android device;
- backup/restore remains available.

Turning Windows connectivity off does not disable Android features.

---

# 6. Navigation

Veltrix Drone Android is adapted for phone-sized screens.

Core functions are available through the main application navigation.

Additional system functions are available through:

```text
More
```

Windows connectivity is located at:

```text
More
→ Exchange & Sync
```

Long pages use vertical scrolling.

---

# 7. Recommended Initial Setup

For a new standalone Android database:

```text
1. Add drones
2. Add batteries
3. Fill inventory
4. Create KITs if needed
5. Add components
6. Bind components to nodes
7. Create maintenance tasks
8. Create a mission plan
9. Complete Preflight
10. Record the flight
11. Complete Postflight
12. Create the first backup
```

Windows can be connected before or after this process.

---

# 8. Drones

Open the Drones section.

Use a stable unique code:

```text
DRN-001
DRN-002
DRN-003
```

Enter available information such as:

- model;
- serial number;
- state;
- flight hours;
- location;
- notes;
- economic fields;
- other available parameters.

To edit:

1. Open a drone.
2. Enter edit mode.
3. Change fields.
4. Save.

---

# 9. Drone Card

The Drone Card is the main mobile view for a specific aircraft.

Use it to access:

- general information;
- technical state;
- components;
- flights;
- maintenance;
- repairs;
- engineering data;
- attachments;
- history.

Large sections are designed for vertical mobile scrolling.

---

# 10. Batteries

Create one record per physical battery.

Recommended codes:

```text
BAT-001
BAT-002
BAT-003
```

Track:

- model;
- serial;
- cycles;
- condition;
- LiPo data;
- cost;
- notes;
- aircraft relationship.

Do not use one generic battery record for several physical packs.

---

# 11. Inventory

Inventory is fully local on Android.

Use unique SKUs:

```text
STK-0001
STK-0002
```

Typical operations:

- create item;
- receipt;
- issue;
- return;
- write-off;
- economic tracking.

When issuing a part for an aircraft, link the movement to the relevant drone when the screen supports it.

---

# 12. KITs

A KIT groups several inventory items.

Example:

```text
KIT-001
```

KITs can represent:

- spare-part sets;
- maintenance sets;
- field kits;
- mission-specific kits.

Local-only KITs are preserved even when they are not present on Windows.

---

# 13. Components and Node Binding

Android supports physical component tracking and positional node binding.

Logic:

```text
component
→ drone
→ node / position
```

Example:

```text
MOTOR-014
→ DRN-002
→ front-right motor
```

When installing a component, record the actual installation rather than changing only a note.

When removing it, record the actual removal to preserve lifecycle history.

---

# 14. Repairs

Create a repair for a real technical event.

Record:

- aircraft;
- issue;
- node;
- description;
- status;
- cost;
- work performed;
- notes.

Prefer precise descriptions over vague entries.

Repair history supports later engineering analysis.

---

# 15. Inspections

Use inspections to capture aircraft condition at a specific point in time.

Typical uses:

- before technical work;
- after repair;
- after storage;
- periodic inspection;
- suspected technical issue.

Supported shared inspection records can participate in Windows synchronization.

---

# 16. Scheduled Maintenance

Create and manage maintenance tasks locally.

Record:

- drone;
- task;
- due information;
- status;
- notes;
- other available parameters.

Do not mark work complete before it has actually been performed.

---

# 17. Mission Plans

Create the mission plan before the flight.

Link:

- drone;
- date;
- mission;
- battery;
- other available fields.

Mission plans are part of the currently supported Windows exchange set.

---

# 18. Preflight Checks

Complete Preflight before operation.

Recommended sequence:

```text
Mission Plan
→ Preflight
→ Flight
```

Record any finding before flight.

If the check fails, resolve and record the actual issue before continuing.

---

# 19. Flights

Record factual flight information:

- aircraft;
- date;
- duration;
- battery;
- result;
- remarks;
- technical events.

Flights are currently included in the shared Windows ↔ Android data set.

---

# 20. Postflight Checks

After flight, record:

- damage;
- vibration;
- unusual behavior;
- communication issues;
- power issues;
- diagnostic requirement;
- repair requirement.

Recommended flow:

```text
Flight
→ Postflight
→ Repair / inspection when required
```

---

# 21. Attachments

Android stores local attachments independently of Windows.

Use attachments for:

- photos;
- documents;
- other supported files.

Example:

```text
Damage photo
→ Repair
→ DRN-002
```

Remote attachment metadata and local files are handled separately during synchronization.

---

# 22. Engineering Modules

Android includes local engineering functionality.

These modules do not require Windows for their local calculations.

Depending on the current build, the application includes migrated areas such as:

- Technical Health;
- Predictive Maintenance;
- Engineering Command Center;
- Configuration;
- Degradation;
- Technical Cycles;
- Reliability;
- Reliability Cases.

Engineering states are intended to be explainable and based on recorded data.

---

# 23. Trends and Degradation

The current mobile architecture can use technical trends including:

- condition index;
- LiPo voltage sag;
- LQ;
- temperature;
- maximum current;
- mAh/min;
- node-grouped signals;
- component resource;
- registered failure trend.

Use trends across meaningful history rather than one isolated flight.

---

# 24. Configuration Control

Android supports a Configuration Drift workflow.

Typical state progression:

```text
Open
→ Checked
→ Confirmed
→ Accepted
or
→ Resolved
```

An accepted drift may remain a warning.

A drift should only be resolved when the actual configuration matches the baseline.

---

# 25. Technical Cycle

Android stores technical closure data and snapshots.

Use a Technical Cycle for:

```text
Issue
→ technical work
→ verification
→ readiness
→ closure
```

If blockers are shown, resolve the actual causes before re-checking.

---

# 26. Reliability

Reliability features require accumulated factual history.

Useful inputs include:

- flights;
- flight hours;
- registered failures;
- repairs;
- component history;
- recurring events.

A new empty database naturally has limited reliability insight.

---

# 27. Economic Data

Android stores local economic fields.

Shared synchronization should not unnecessarily overwrite Android-only economic values.

Record actual:

- component cost;
- repair cost;
- other available expenses.

---

# 28. Backups

Local ZIP backups work independently of Windows.

Create backups:

- after initial setup;
- before APK updates;
- before major changes;
- before restore;
- regularly during normal operation.

Keep at least one recent backup outside the phone.

---

# 29. Restore

Restore does not require Windows.

Before restoring:

1. Create a backup of the current state.
2. Verify the selected ZIP.
3. Do not interrupt restore.
4. Verify drones, batteries and recent records afterward.

> [!WARNING]
> Do not use Android Clear Data as an update or restore procedure.

---

# 30. Connecting to Windows

Android connection is optional.

On Android:

```text
More
→ Exchange & Sync
```

On Windows:

```text
System
→ Mobile Connection
```

Both devices should be on the same private local network.

---

# 31. First Synchronization

## Windows

1. Open Mobile Connection.
2. Start the local server.
3. Note the address.
4. Note the port.
5. Copy the token.

## Android

1. Open **More → Exchange & Sync**.
2. Enable Windows connection.
3. Enter Windows address.
4. Enter port if shown separately.
5. Enter token.
6. Save the connection.
7. Start synchronization.

---

# 32. What Is Synchronized

The current Windows Mobile Bridge supports these shared entities:

| Entity | Exchange |
|---|:---:|
| Drones | ✅ |
| Batteries | ✅ |
| Repairs | ✅ |
| Inspections | ✅ |
| Inventory | ✅ |
| KITs | ✅ |
| Scheduled maintenance | ✅ |
| Attachments | ✅ |
| Mission plans | ✅ |
| Flights | ✅ |
| Preflight checks | ✅ |
| Postflight checks | ✅ |

---

# 33. Merge Behavior

Windows does not replace the Android database.

Synchronization uses merge/upsert behavior:

```text
record exists on both sides
→ update / merge

Android-only record
→ keep it

Windows-only supported record
→ add it to Android
```

Local master records are not supposed to disappear simply because Windows does not contain them.

---

# 34. Android-only Engineering Data

The current Mobile Bridge does not yet understand every newer Android engineering entity.

Those modules:

- continue working locally;
- remain stored on Android;
- do not depend on Windows;
- may not yet appear on the PC.

This is a synchronization scope limitation, not an Android application failure.

---

# 35. Disconnecting Windows

Open:

```text
More
→ Exchange & Sync
```

Disable Windows connection or clear only the Windows connection parameters.

After disconnecting:

- Android remains operational;
- local data remains;
- backups remain available;
- engineering modules continue to work.

Clearing Windows connection settings does not mean clearing the Android database.

---

# 36. Updating the APK

Recommended update process:

1. Create a local backup.
2. Download the new official APK.
3. Open it.
4. Install it over the existing application.
5. Do not uninstall the old app first.
6. Do not use Clear Data.
7. Start the app and verify several key records.

---

# 37. Language

The mobile application contains Russian and English UI strings.

Use the application's language setting available in the current build.

Available languages:

```text
Русский
English
```

User-entered records are not automatically translated.

---

# 38. Offline Operation

Internet is not required for normal local operation.

Offline you can:

- open the app;
- create records;
- edit records;
- use engineering modules;
- use local attachments;
- create backups;
- restore backups.

Windows synchronization requires a shared local network, not public Internet access.

---

# 39. Typical Workflows

## A. Phone only

```text
Install APK
→ open Veltrix Drone
→ create drone
→ create battery
→ record flights and repairs
→ create backups
```

---

## B. New UAV

```text
Drones
→ Add
→ Batteries
→ Components
→ Node binding
→ Maintenance
→ first mission plan
```

---

## C. Normal flight

```text
Mission Plan
→ Preflight
→ Flight
→ Postflight
```

---

## D. Postflight fault

```text
Postflight
→ record issue
→ repair / inspection
→ verification
→ continue operation
```

---

## E. Component replacement

```text
Inventory
→ component
→ remove old
→ install new
→ bind node
→ verify configuration
```

---

## F. Android + Windows

```text
Work on Android
→ start Windows Mobile Connection
→ More → Exchange & Sync
→ synchronize
→ continue work on either device
```

---

# 40. Troubleshooting

## APK will not install

Check:

- free storage space;
- permission to install from the selected source;
- whether the APK download completed;
- whether the file is damaged.

---

## App appears empty after an update

Do not clear app data.

If records are actually missing:

1. avoid creating large amounts of new data;
2. open local backups;
3. restore the latest verified ZIP backup.

---

## Windows will not connect

Check in order:

1. phone and PC are on the same network;
2. Windows Mobile Connection is running;
3. local IP is correct;
4. port is correct;
5. token is current;
6. Windows Firewall permits private-network access.

---

## A new engineering module does not appear on Windows

This can be expected.

Some newer Android engineering entities are currently local-only because the Mobile Bridge does not yet synchronize them.

---

# 41. FAQ

## Does Android work without Windows?

Yes. This is a core design principle.

## Is a phone-only mode selection required at first launch?

No. A new installation starts autonomously.

## Does disconnecting Windows delete Android data?

No.

## Does Windows replace the Android database?

No. Supported shared records use merge/upsert behavior.

## Is Internet required for sync?

No. Both devices need the same local network.

## Can I create a drone only on Android?

Yes.

## Can I create a repair only on Android?

Yes.

## Can I back up without Windows?

Yes.

## Can I restore without Windows?

Yes.

## Are all engineering entities synchronized?

No. Some newer engineering entities remain Android-local.

## Should I uninstall before updating?

No. Install the new APK over the existing app.

## Should I use Clear Data before updating?

No, not if you want to keep the local database.

---

# 42. Security

Recommended practices:

- download APK only from the official release;
- never publish the Windows connection token;
- do not expose Mobile Bridge directly to the public Internet;
- create regular backups;
- keep at least one backup outside the phone;
- do not use Clear Data without a deliberate reason;
- verify key records after an update;
- use a private local network for Windows synchronization.

---

<div align="center">

# Veltrix Drone Android

### Core principle

```text
The phone works independently.
Windows is an optional synchronization peer, not a mandatory server.
```

**Offline-first · Local data · Optional Windows Sync**

</div>
