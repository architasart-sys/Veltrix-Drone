<div align="center">

<img src="assets/veltrix_drone_logo.png" alt="Veltrix Drone" width="190">

# Veltrix Drone

### Engineering system for UAV fleet management, operation and technical support

![Version](https://img.shields.io/badge/version-v1.0-2f81f7)
![Release](https://img.shields.io/badge/release-Stable-238636)
![Windows](https://img.shields.io/badge/platform-Windows-0078D4)
![Offline](https://img.shields.io/badge/work-offline--first-8250df)
![License](https://img.shields.io/badge/license-Non--Sale-d73a49)

**Drones · Flights · LiPo · Maintenance · Repairs · Inventory · Reliability · Engineering Analysis · Reports · Windows ↔ Android**

**English** · [Русский](README.ru.md)

</div>

---

> [!IMPORTANT]
> **Veltrix Drone v1.0** is a complete Windows application for UAV fleet operation and technical management.  
> Core functionality works locally and does not require a permanent Internet connection.

> [!WARNING]
> Always create a backup before updating the application or performing a large data import.

---

# 📌 Contents

- [About Veltrix Drone](#-about-veltrix-drone)
- [Who is it for](#-who-is-it-for)
- [Main Features](#-main-features)
- [Quick Start](#-quick-start)
- [Installation](#-installation)
- [First Launch](#-first-launch)
- [Recommended Setup Order](#-recommended-setup-order)
- [Dashboard](#-dashboard)
- [Drones](#-drones)
- [Drone Card](#-drone-card)
- [Planning](#-planning)
- [Dispatch Center](#-dispatch-center)
- [Flights](#-flights)
- [Preflight](#-preflight)
- [Postflight](#-postflight)
- [Flight Debrief](#-flight-debrief)
- [LiPo Batteries](#-lipo-batteries)
- [Repairs](#-repairs)
- [Maintenance](#-maintenance)
- [Components and Nodes](#-components-and-nodes)
- [Configuration Control](#-configuration-control)
- [Bench Tests and Return to Service](#-bench-tests-and-return-to-service)
- [Work Packages and Technical Cycles](#-work-packages-and-technical-cycles)
- [Reliability](#-reliability)
- [Reliability Cases](#-reliability-cases)
- [Corrective Actions](#-corrective-actions)
- [Effectiveness Tracking](#-effectiveness-tracking)
- [Engineering Command Center](#-engineering-command-center)
- [Inventory](#-inventory)
- [Procurement](#-procurement)
- [Economics and Budget](#-economics-and-budget)
- [Diagnostics and Knowledge Base](#-diagnostics-and-knowledge-base)
- [QR Codes](#-qr-codes)
- [Attachments](#-attachments)
- [Excel](#-excel)
- [Technical Reports](#-technical-reports)
- [Backups](#-backups)
- [Users and Roles](#-users-and-roles)
- [Windows ↔ Android](#-windows--android)
- [Typical Workflows](#-typical-workflows)
- [Updating](#-updating)
- [Troubleshooting](#-troubleshooting)
- [FAQ](#-faq)
- [License](#-license)

---

# 🚁 About Veltrix Drone

**Veltrix Drone** is a unified engineering environment for managing the complete technical lifecycle of unmanned aerial vehicles.

Instead of maintaining separate disconnected logs, the application links operational and engineering records into one workflow:

```text
Drone
  ↓
Planning
  ↓
Preflight
  ↓
Flight
  ↓
Postflight
  ↓
Event / failure
  ↓
Diagnostics
  ↓
Repair / maintenance
  ↓
Verification
  ↓
Return to Service
  ↓
Validation flight
  ↓
Reliability analysis
  ↓
Complete aircraft history
```

Veltrix Drone combines operations, service, inventory, engineering analysis, documents, economics and fleet history.

---

# 👥 Who is it for

Veltrix Drone can be useful for:

- UAV fleet owners;
- technicians;
- repair workshops;
- operators;
- engineers;
- inventory personnel;
- organizations that need a unified technical record system.

---

# ✨ Main Features

| Area | Capabilities |
|---|---|
| 🛩️ **Fleet** | UAV registry, cards, photos, status, history |
| ✈️ **Flights** | planning, Dispatch, Preflight, Flight, Postflight |
| 🔋 **LiPo** | batteries, cycles, condition, history |
| 🔧 **Service** | repairs, maintenance, diagnostics, checklists |
| 🧩 **Configuration** | components, nodes, revisions, change control |
| 📈 **Reliability** | failures, cases, corrective measures |
| 📦 **Inventory** | stock, issue, return, write-off, kits |
| 🛒 **Procurement** | requests, orders, partial receipt, receipt |
| 💰 **Economics** | expenses, budget, ownership cost |
| 📁 **Documents** | attachments, QR, Excel, DOCX reports |
| 👤 **Users** | roles, permissions, action history |
| 📱 **Android** | local Windows ↔ Android synchronization |

---

# ⚡ Quick Start

After installing Veltrix Drone:

### 1. Start the application

Open:

```text
Veltrix Drone
```

### 2. Create the administrator

The first launch opens the initial setup wizard.

### 3. Add the first drone

```text
Operations → Drones → Add
```

### 4. Add a battery

```text
Operations → Batteries → Add
```

### 5. Create a backup

```text
System → Backups
```

> [!TIP]
> Before entering real operational data, create one test UAV and walk through a complete flight, repair and maintenance workflow.

---

# 💻 Installation

## Supported platform

```text
Windows 10
Windows 11
```

## Install from GitHub Releases

1. Open the repository **Releases** page.
2. Select the latest stable release.
3. Download the Veltrix Drone Windows installer.
4. Run the `.exe`.
5. Follow the installation wizard.
6. Start Veltrix Drone from the Start Menu or desktop shortcut.

> [!NOTE]
> If Windows SmartScreen displays a warning for a new unsigned build, verify that the installer was downloaded from the official project repository.

---

# 👤 First Launch

On first launch the setup wizard asks for:

| Field | Example |
|---|---|
| Organization | Drone Service |
| Administrator | Administrator |
| Login | admin |
| Password | your password |

After setup, the login screen opens.

> [!IMPORTANT]
> Use a unique administrator password for a real working installation.

---

# 🏁 Recommended Setup Order

For a new database, use this order:

```text
1. Users
2. Drones
3. Batteries
4. Inventory
5. Components
6. Drone configuration
7. Maintenance regulations
8. Flights
9. Repairs / maintenance
10. Attachments
11. Backup
```

This helps build consistent relationships between entities from the beginning.

---

# 🏠 Dashboard

The Dashboard provides a fleet overview.

It can show:

- technical readiness;
- aircraft requiring attention;
- active repairs;
- overdue maintenance;
- inventory warnings;
- notifications;
- quick actions.

The Dashboard is primarily designed for situational awareness.

---

# 🚁 Drones

Open:

```text
Operations → Drones
```

Create a drone and specify:

- code;
- model;
- serial number;
- status;
- flight hours;
- location;
- responsible user;
- purchase date;
- photo;
- notes.

### Recommended coding

```text
DRN-001
DRN-002
DRN-003
```

> [!TIP]
> Avoid changing a drone code without a strong reason because it is used to link flights, repairs, parts and other records.

---

# 🪪 Drone Card

The Drone Card is the main electronic technical passport of an aircraft.

## Overview

- general information;
- state;
- flight hours;
- photo;
- current configuration.

## Operation

- plans;
- flights;
- LiPo;
- resource.

## Service

- diagnostics;
- faults;
- failures;
- repairs;
- maintenance.

## Configuration

- components;
- electronics;
- nodes.

## History

- events;
- files;
- changes.

---

# 🗓️ Planning

Open:

```text
Operations → Planning
```

A mission plan can include:

- drone;
- pilot;
- LiPo;
- date;
- time;
- duration;
- mission;
- location;
- notes.

---

# 🚦 Dispatch Center

Open:

```text
Operations → Dispatch Center
```

Dispatch helps determine whether the aircraft can be used for the planned sortie.

It considers recorded conditions such as:

- active repairs;
- technical blocks;
- incomplete checks;
- LiPo state;
- scheduling conflicts;
- maintenance requirements.

> [!NOTE]
> Veltrix Drone can only evaluate information that has actually been recorded.

---

# ✈️ Flights

Open:

```text
Operations → Flights
```

A flight record can contain:

- flight number;
- drone;
- pilot;
- LiPo;
- date;
- duration;
- mission;
- result;
- remarks.

The saved record becomes part of the aircraft history.

---

# ✅ Preflight

Complete the preflight checklist before operation.

Recommended sequence:

```text
Plan
→ Dispatch
→ Preflight
→ Flight
```

If a problem is detected, record it before the flight.

---

# 🛬 Postflight

After a flight, record:

- physical damage;
- unusual behavior;
- vibration;
- communication problems;
- LiPo condition;
- diagnostic requirements;
- repair requirements.

Good Postflight records significantly improve long-term engineering history.

---

# 🔎 Flight Debrief

Flight Debrief combines:

- plan;
- Dispatch;
- Preflight;
- flight;
- analysis;
- Postflight;
- failures;
- remarks;
- conclusions.

---

# 🔋 LiPo Batteries

Open:

```text
Operations → Batteries
```

Track each physical battery separately.

You can store:

- code;
- series;
- capacity;
- cycle count;
- condition;
- cost;
- history;
- UAV assignment;
- QR code.

Example:

```text
BAT-001
BAT-002
BAT-003
```

---

# 🔧 Repairs

Open:

```text
Service → Repairs
```

A repair record can contain:

- drone;
- issue;
- affected node;
- description;
- status;
- performed work;
- parts;
- cost;
- labor;
- documents.

### Poor description

```text
Does not work
```

### Better description

```text
Crack found on the front-right arm after landing.
Increased vibration detected during FR motor inspection.
```

High-quality records make reliability analysis more useful.

---

# 🛠️ Maintenance

Use:

```text
Service → Service Center
```

and:

```text
Service → Maintenance
```

Schedule maintenance by:

- date;
- due interval;
- resource;
- priority;
- responsible technician;
- work state.

## Regulations

```text
Service → Regulations
```

Regulations can be linked to:

- calendar interval;
- flight hours;
- node;
- work type.

---

# 🧩 Components and Nodes

Open:

```text
Service → Components
```

Each physical component can be linked to a specific UAV and specific node.

Example:

```text
MOTOR-014
→ DRN-002
→ front-right motor
```

This makes it possible to track:

- what is installed;
- when it was installed;
- how long it was used;
- when it was removed;
- which technical events affected it.

---

# 🧬 Configuration Control

Open:

```text
Service → Configuration Control
```

Use this section for:

- current configuration;
- approved baseline;
- change comparison;
- revision history;
- release control.

---

# 🧪 Bench Tests and Return to Service

After repair, additional verification may be required.

Recommended flow:

```text
Repair
→ Bench Test
→ Return to Service
→ Validation Flight
```

Closing a repair does not always mean that the aircraft is ready for operation.

---

# 🧾 Work Packages and Technical Cycles

## Work Package

Formalizes technical work:

- operations;
- technician;
- materials;
- time;
- cost;
- result.

## Technical Cycle

Combines the complete path:

```text
Issue
→ Work
→ Work Package
→ Verification
→ RTS
→ Validation Flight
→ Closure
```

---

# 📈 Reliability

Open:

```text
Service → Reliability
```

Uses accumulated factual history:

- confirmed failures;
- flight hours;
- downtime;
- recurrence;
- technical work.

> [!IMPORTANT]
> A new database naturally has limited reliability information. The module becomes more useful as operational history grows.

---

# 🧷 Reliability Cases

Open:

```text
Service → Reliability Cases
```

A Reliability Case is useful when the same problem repeats.

Example:

```text
Several UAVs
→ same node type
→ repeated confirmed failures
→ one engineering case
```

---

# 🛠️ Corrective Actions

Open:

```text
Service → Corrective Actions
```

Track:

- action;
- owner;
- due date;
- status;
- result;
- verification.

---

# 📉 Effectiveness Tracking

Open:

```text
Service → Effectiveness Tracking
```

Compare the factual situation before and after corrective measures.

| Metric | Before | After |
|---|---:|---:|
| Failures | 5 | 1 |
| Flight hours | 80 h | 95 h |
| Downtime | 12 h | 3 h |
| Cost | 45,000 | 10,000 |

The final conclusion remains a human engineering decision.

---

# 🧭 Engineering Command Center

Combines:

- fleet technical state;
- engineering queue;
- Reliability Cases;
- Corrective Actions;
- Technical Cycles;
- configuration;
- restrictions;
- operational release status.

---

# 📦 Inventory

Open:

```text
Supply → Inventory
```

For each item you can store:

- SKU;
- name;
- quantity;
- unit;
- minimum quantity;
- unit cost.

Supported movements:

```text
Receipt
Issue
Return
Write-off
```

If a part is issued for a specific aircraft, link it to the drone.

---

# 🛒 Procurement

Open:

```text
Supply → Procurement
```

Typical process:

```text
Draft
→ Approved
→ Ordered
→ Partially received
→ Received
```

---

# 💰 Economics and Budget

The application can consolidate:

- repairs;
- maintenance;
- inventory;
- procurement;
- operating expenses;
- cost by UAV;
- budget;
- total cost of ownership.

---

# 🧠 Diagnostics and Knowledge Base

## Knowledge Base

Create technical articles for:

- faults;
- symptoms;
- verification methods;
- technical solutions.

## Diagnostics

Veltrix Drone can compare recorded symptoms against the local knowledge base.

> [!WARNING]
> Diagnostics is an engineering aid, not an automatic final technical conclusion.

---

# 🔳 QR Codes

Open:

```text
Supply → QR Codes
```

### Generate a QR code

1. Select entity type.
2. Select object code.
3. Click **Generate QR Code**.
4. Save PNG if needed.

Useful for labeling:

- drones;
- LiPo batteries;
- components;
- kits;
- inventory items.

---

# 📎 Attachments

Open:

```text
Economics and Data → Attachments
```

Attach:

- photos;
- PDF files;
- documents;
- spreadsheets;
- other files.

Example:

```text
Damage photo
→ Repair
→ DRN-002
```

---

# 📊 Excel

Open:

```text
Economics and Data → Excel
```

Available actions:

- data export;
- import template creation;
- data import.

> [!WARNING]
> Create a backup before any large import.

---

# 📄 Technical Reports

The application can generate technical documents such as:

- aircraft passport;
- repair report;
- diagnostics;
- maintenance history;
- reliability reports.

---

# 💾 Backups

Open:

```text
System → Backups
```

Create backups:

- before an update;
- before bulk import;
- before restore;
- after major changes;
- regularly during operation.

> [!IMPORTANT]
> Backups are the primary way to protect your working history.

---

# 👥 Users and Roles

Open:

```text
System → Users
```

| Role | Purpose |
|---|---|
| **Operator** | daily operation |
| **Technician** | diagnostics, repair, maintenance |
| **Storekeeper** | inventory and supply |
| **Administrator** | system management |

Use separate accounts for different users whenever possible.

---

# 📱 Windows ↔ Android

Open:

```text
System → Mobile Connection
```

Windows and Android can synchronize over the same local network.

```text
Veltrix Drone Windows
        ↕
    local network
        ↕
Veltrix Drone Android
```

Windows displays:

- address;
- port;
- token;
- server status;
- connected devices.

## Connection

1. Connect PC and phone to the same network.
2. Start Mobile Connection on Windows.
3. Open Veltrix Drone Android.
4. Enter the address and token.
5. Start synchronization.

> [!WARNING]
> Do not publish the connection token or expose the local server directly to the Internet.

---

# 🔁 Typical Workflows

## New UAV

```text
Drones
→ Add
→ Photo
→ Configuration
→ Components
→ LiPo
→ Regulations
→ QR
```

## Normal Sortie

```text
Planning
→ Dispatch
→ Preflight
→ Flight
→ Postflight
→ Debrief
```

## Technical Fault

```text
Remark
→ Diagnostics
→ Repair
→ Work Package
→ Bench Test
→ RTS
→ Validation Flight
→ Closure
```

## Component Replacement

```text
Inventory
→ Issue part
→ Drone
→ Remove old component
→ Install new component
→ Update configuration
```

## Repeating Failure

```text
Failures
→ Reliability Case
→ Common Factors
→ Corrective Action
→ Implementation
→ Effectiveness Tracking
→ Engineering conclusion
```

---

# 🔄 Updating

1. Close Veltrix Drone.
2. Create a backup.
3. Download the new release from GitHub Releases.
4. Run the new installer.
5. Complete the update.
6. Start Veltrix Drone and verify that your data is available.

> [!IMPORTANT]
> Always create a backup before updating.

---

# 🧯 Troubleshooting

## Veltrix Drone does not start

1. Restart Windows.
2. Try launching Veltrix Drone normally.
3. Check whether security software quarantined any application files.
4. If the problem continues, create a GitHub Issue.

## Data is not visible after an update

Do not create a new working database or delete existing data. Restore the latest backup using the built-in backup tools if required.

## Android cannot connect

Check:

1. both devices are on the same local network;
2. Mobile Connection is running;
3. IP address is correct;
4. port is correct;
5. token is correct;
6. Windows Firewall allows the connection.

---

# ❓ FAQ

### Is Internet required?

No, not for normal local operation.

### Can Veltrix Drone work only on one PC?

Veltrix Drone runs as a Windows application with local data. Android can synchronize with Windows over the local network.

### Is Android only a remote control?

No. The Android edition is designed as a standalone application with local data and Windows synchronization.

### Does Veltrix Drone automatically diagnose broken components?

No. Engineering modules support analysis of recorded facts, but the final technical decision belongs to a qualified specialist.

### Should I create backups?

Yes, especially before updates, imports and restores.

### Can Veltrix Drone be sold?

Not without separate written permission from the copyright holder.

---

# 🐞 Reporting an Issue

Create a **GitHub Issue** and include:

```text
Veltrix Drone: v1.0
Windows: Windows 10 / 11

Section:
What you did:
Expected:
Actual:
Error message:
```

Screenshots are welcome.

> [!WARNING]
> Do not publish real operational data, backups or confidential documents.

---

# 📜 License

Veltrix Drone is distributed under the custom:

## Veltrix Drone Non-Sale License

Without written permission from the copyright holder, the following are prohibited:

- selling;
- reselling;
- paid redistribution;
- commercial repackaging;
- selling modified builds;
- paid access;
- commercial SaaS based on Veltrix Drone.

Full text:

```text
LICENSE
```

> [!IMPORTANT]
> Veltrix Drone Non-Sale License is not a standard OSI Open Source License.

---

# 📦 GitHub Releases

Recommended stable release:

### Tag

```text
v1.0
```

### Name

```text
Veltrix Drone v1.0 Stable
```

For end users, Releases should contain the ready-to-install **Windows `.exe` / installer**.

---

<div align="center">

## Veltrix Drone v1.0

**Unified engineering environment for the complete UAV lifecycle**

```text
Drone → Flight → Event → Diagnostics → Repair → Verification → Operation → Reliability
```

**Stable · Windows · Offline-first**

</div>
