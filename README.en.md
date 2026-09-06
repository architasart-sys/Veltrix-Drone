<div align="center">

<img src="assets/veltrix_drone_logo.png" alt="Veltrix Drone" width="190">

# Veltrix Drone

### Local engineering system for UAV fleet management, operation, maintenance and technical analysis

![Version](https://img.shields.io/badge/version-v1.0-2f81f7)
![Release](https://img.shields.io/badge/release-Stable-238636)
![Windows](https://img.shields.io/badge/platform-Windows-0078D4)
![Offline](https://img.shields.io/badge/mode-Offline--first-8250df)
![Database](https://img.shields.io/badge/database-SQLite-0f80cc)
![License](https://img.shields.io/badge/license-Non--Sale-d73a49)

**Drones · Flights · LiPo · Maintenance · Repairs · Inventory · Reliability · Engineering Analysis · Reports · Windows ↔ Android**

**English** · [Русский](README.ru.md)

</div>

---

> [!IMPORTANT]
> **Veltrix Drone v1.0** is a standalone local Windows application.  
> Core functionality works **without Internet access**, and operational data is stored locally in SQLite.

> [!WARNING]
> The working file `dronebase.db` contains user data.  
> **Do not publish it on GitHub and do not replace it when updating the application.**

---

# 📌 Table of Contents

- [What is Veltrix Drone](#-what-is-veltrix-drone)
- [What the application can do](#-what-the-application-can-do)
- [Quick start in 5 minutes](#-quick-start-in-5-minutes)
- [Installation](#-installation)
- [First launch](#-first-launch)
- [Main menu](#-main-menu)
- [How to start from an empty database](#-how-to-start-from-an-empty-database)
- [Drones](#-drones)
- [Drone Card](#-drone-card)
- [LiPo Batteries](#-lipo-batteries)
- [Flights](#-flights)
- [Planning and Dispatch](#-planning-and-dispatch)
- [Preflight and Postflight](#-preflight-and-postflight)
- [Repairs](#-repairs)
- [Maintenance](#-maintenance)
- [Components and Configuration](#-components-and-configuration)
- [Inventory and Procurement](#-inventory-and-procurement)
- [Reliability and Engineering](#-reliability-and-engineering)
- [Diagnostics and Knowledge Base](#-diagnostics-and-knowledge-base)
- [QR Codes](#-qr-codes)
- [Attachments and Documents](#-attachments-and-documents)
- [Excel](#-excel)
- [Backups](#-backups)
- [Windows ↔ Android](#-windows--android)
- [Users and Roles](#-users-and-roles)
- [Typical Workflows](#-typical-workflows)
- [Updating the Application](#-updating-the-application)
- [Where Data is Stored](#-where-data-is-stored)
- [What Must Not Be Uploaded to GitHub](#-what-must-not-be-uploaded-to-github)
- [Troubleshooting](#-troubleshooting)
- [FAQ](#-faq)
- [License](#-license)

---

# 🚁 What is Veltrix Drone

**Veltrix Drone** is a unified engineering environment for working with a fleet of unmanned aerial vehicles.

The application covers the full technical lifecycle of a UAV:

```text
Registration
      ↓
Operation
      ↓
Mission planning
      ↓
Preflight check
      ↓
Flight
      ↓
Postflight check
      ↓
Diagnostics / event / failure
      ↓
Repair or maintenance
      ↓
Bench verification
      ↓
Return to Service
      ↓
Validation flight
      ↓
Reliability analysis
      ↓
Complete technical history
```

### Core principles

| Principle | Meaning |
|---|---|
| **Offline-first** | Internet access is not required for normal work |
| **Local database** | Working data is stored in `dronebase.db` |
| **Engineering traceability** | Flights, repairs, maintenance, components and events are linked |
| **No fabricated technical states** | The application should not invent technical conclusions without factual data |
| **Action history** | User actions and technical events are recorded |
| **Windows ↔ Android** | Mobile synchronization uses a local API |

---

# ✨ What the application can do

<details>
<summary><b>🛩️ Fleet Management</b></summary>

- UAV registry;
- models and serial numbers;
- operational state and flight hours;
- location;
- assigned user;
- photos and documents;
- electronic UAV passport;
- operational history.

</details>

<details>
<summary><b>✈️ Flights and Planning</b></summary>

- Mission Planner;
- Dispatch Center;
- Operations Calendar;
- Preflight control;
- flight log;
- Postflight control;
- telemetry;
- flight debrief;
- flight comparison;
- technical trends.

</details>

<details>
<summary><b>🔧 Service and Maintenance</b></summary>

- repairs;
- maintenance;
- regulations;
- checklists;
- diagnostics;
- bench tests;
- Return to Service;
- validation flights;
- Work Packages;
- Technical Cycles.

</details>

<details>
<summary><b>🧩 Components and Configuration</b></summary>

- physical component tracking;
- exact component-to-node binding;
- component resource;
- replacement history;
- Configuration Control;
- FC Config Audit;
- revision control.

</details>

<details>
<summary><b>📊 Reliability and Engineering Analysis</b></summary>

- Reliability Dashboard;
- Node Degradation;
- Reliability Cases;
- Common Factors;
- Corrective Actions;
- Effectiveness Tracking;
- Fleet Reliability Reports;
- Engineering Command Center.

</details>

<details>
<summary><b>📦 Supply and Economics</b></summary>

- inventory;
- receipt / issue / return / write-off;
- kits;
- procurement;
- parts forecasting;
- fleet economics;
- budget;
- total cost of ownership.

</details>

<details>
<summary><b>📁 Data and Documents</b></summary>

- attachments;
- photos;
- PDF / DOCX / XLSX;
- technical reports;
- QR codes;
- Excel import / export;
- backups;
- action log.

</details>

---

# ⚡ Quick start in 5 minutes

If you have just downloaded Veltrix Drone:

### 1. Extract the release archive

For example:

```text
C:\Veltrix_Drone\
```

### 2. Start the application

Run:

```text
START_VELTRIX.bat
```

### 3. Create the administrator account

During first setup specify:

- organization name;
- administrator name;
- login;
- password.

### 4. Add your first drone

```text
Operations → Drones → Add
```

### 5. Add a LiPo battery

```text
Operations → Batteries → Add
```

### 6. Add inventory items

```text
Supply → Inventory
```

### 7. Create your first backup

```text
System → Backups
```

> [!TIP]
> Before entering a large amount of real data, create one test drone, one battery, one repair and one flight to learn the workflow.

---

# 💻 Installation

## Requirements

Recommended:

```text
Windows 10
Windows 11
```

The source distribution requires:

```text
Python 3
```

and dependencies from:

```text
requirements.txt
```

Main libraries:

| Library | Purpose |
|---|---|
| CustomTkinter | user interface |
| Pillow | image handling |
| qrcode | QR generation |
| openpyxl | Excel |
| python-docx | DOCX |
| tkinterdnd2 | Drag & Drop |

---

## Launch using the launcher

Run:

```text
START_VELTRIX.bat
```

The launcher searches for Python in this order:

```text
1. .venv\Scripts\python.exe
2. venv\Scripts\python.exe
3. py -3
4. python
```

---

## If the application does not start

Run:

```text
CHECK_PYTHON.bat
```

It checks:

- Python version;
- Python executable path;
- availability of core dependencies.

---

# 👤 First launch

On first launch, Veltrix Drone opens the initial setup wizard.

Fill in:

| Field | Example |
|---|---|
| Organization | Drone Service |
| Administrator | Administrator |
| Login | admin |
| Password | your password |

After setup, the login screen will open.

> [!IMPORTANT]
> Do not use a weak password for a real working installation.

---

# 🧭 Main menu

The navigation is divided into logical sections.

## Operations

- Dashboard
- Command Center
- Planning
- Dispatch Center
- Operations Calendar
- Flight Debrief
- Drones
- Flights
- Batteries

## Service

- Service Center
- Repairs
- Maintenance
- Components
- Checklists
- Diagnostics
- Corrective Actions
- Configuration Control
- Bench Tests
- Return to Service
- Validation Flights
- Reference Flights
- Node Degradation
- Technical Health
- Predictive Maintenance
- Technical Review
- Work Packages
- Technical Cycle
- Engineering Command Center
- Reliability
- Node Trends
- Reliability Cases
- Effectiveness Tracking
- Reliability Reports
- Regulations

## Supply

- Inventory
- Procurement
- Kits
- QR Codes

## Economics and Data

- Analytics
- Economics
- Budget and TCO
- Assistant
- Knowledge Base
- Technical Reports
- Attachments
- Excel

## System

For administrators:

- Users
- Action Log
- Recycle Bin
- Backups
- Mobile Connection
- System Diagnostics

---

# 🏁 How to start from an empty database

Recommended order:

```text
1. Users
2. Drones
3. Batteries
4. Inventory
5. Components
6. Drone configuration
7. Maintenance regulations
8. Flights
9. Repairs and maintenance
10. Attachments
11. Backup
```

This helps build correct links between entities from the beginning.

---

# 🚁 Drones

Open:

```text
Operations → Drones
```

## Adding a drone

Create a new record and fill in the main fields:

- code;
- model;
- serial number;
- status;
- flight hours;
- location;
- assigned user;
- firmware;
- purchase date;
- photo;
- notes.

### Recommended coding convention

Use stable internal codes:

```text
DRN-001
DRN-002
DRN-003
```

Avoid changing a drone code without a strong reason because it is used by related technical records.

---

# 🪪 Drone Card

Open a drone from the registry.

The Drone Card acts as the **electronic technical passport** of the aircraft.

## Overview

Shows:

- general information;
- current technical state;
- flight hours;
- configuration;
- technical summary.

## Operation

Contains:

- mission plans;
- flights;
- LiPo;
- resource information.

## Service

Contains:

- diagnostics;
- troubleshooting;
- failures;
- repairs;
- maintenance.

## Configuration

Contains:

- components;
- electronics;
- technical nodes.

## History

Contains:

- files;
- events;
- technical changes.

---

# 🔋 LiPo Batteries

Open:

```text
Operations → Batteries
```

For every battery you can track:

- internal code;
- series;
- capacity;
- cycle count;
- condition;
- cost;
- usage;
- drone assignment;
- QR.

### Example coding

```text
BAT-001
BAT-002
BAT-003
```

> [!TIP]
> Assign a unique code to every physical battery.

---

# ✈️ Flights

Open:

```text
Operations → Flights
```

A flight record may include:

- flight number;
- drone;
- pilot;
- battery;
- date;
- duration;
- mission;
- result;
- remarks;
- operational data.

After saving, the flight becomes part of the UAV history.

---

# 🗓️ Planning and Dispatch

## Creating a mission plan

```text
Operations → Planning
```

Select:

- drone;
- pilot;
- battery;
- date;
- time;
- duration;
- mission;
- location.

---

## Checking readiness

Before a sortie:

```text
Operations → Dispatch Center
```

Dispatch Center evaluates recorded restrictions such as:

- active repair;
- maintenance requirement;
- technical block;
- LiPo state;
- schedule conflict.

> [!NOTE]
> Readiness depends on the data that is actually recorded. Missing information cannot be evaluated.

---

# ✅ Preflight and Postflight

## Before flight

Complete the Preflight checklist.

Record remarks immediately instead of postponing them until later.

## After flight

Record:

- detected defects;
- changes in behavior;
- physical damage;
- repair requirement;
- technical events.

If a technical problem is found, create a repair or diagnostic record.

---

# 🔧 Repairs

Open:

```text
Service → Repairs
```

## Creating a repair

Specify:

- drone;
- issue;
- status;
- affected nodes;
- description;
- parts used;
- cost;
- labor.

### Good practice

Avoid vague notes such as:

```text
broken
```

Prefer:

```text
Crack found on the front-right arm after landing.
Increased vibration detected during FR motor check.
```

Better records produce better reliability history.

---

# 🛠️ Maintenance

Open:

```text
Service → Service Center
```

or:

```text
Service → Maintenance
```

## Scheduled maintenance

You can define:

- due date;
- flight-hour threshold;
- priority;
- responsible technician;
- current work state.

## Regulations

```text
Service → Regulations
```

A regulation can be based on:

- calendar interval;
- flight hours;
- node;
- UAV category.

---

# 🧩 Components and Configuration

## Components

```text
Service → Components
```

Each physical component can be linked to a specific UAV and node.

The logical link is:

```text
component
   ↓
drone_code
   ↓
node_key
```

Example:

```text
MOTOR-014
→ DRN-002
→ motor_fr
```

This allows the system to know which exact physical part is installed at a specific location.

---

## Configuration Control

```text
Service → Configuration Control
```

Used for:

- current configuration;
- approved baseline;
- configuration revisions;
- change comparison;
- Return to Service verification.

---

# 📦 Inventory and Procurement

## Inventory

```text
Supply → Inventory
```

For every item you can store:

- SKU;
- name;
- quantity;
- unit;
- minimum quantity;
- unit cost.

### Example SKU

```text
STK-0001
STK-0002
```

---

## Stock movements

Supported operations:

```text
Receipt
Issue
Return
Write-off
```

If a component is issued to a specific UAV, select the drone.

---

## Procurement

```text
Supply → Procurement
```

A procurement request can move through:

```text
Draft
→ Approved
→ Ordered
→ Partially received
→ Received
```

---

# 📈 Reliability and Engineering

These sections become more useful as real operational history accumulates.

> [!IMPORTANT]
> If the database contains only a few flights, failures and repairs, reliability analysis will naturally be limited.

## Reliability

```text
Service → Reliability
```

Uses:

- confirmed failures;
- flight hours;
- downtime;
- recurrence;
- technical events.

---

## Reliability Cases

```text
Service → Reliability Cases
```

A Reliability Case is useful when the same technical issue repeats.

Example:

```text
3 UAVs of the same model
→ same node_key
→ several confirmed failures
→ one engineering case
```

---

## Corrective Actions

```text
Service → Corrective Actions
```

Track:

- action;
- responsible person;
- due date;
- status;
- verification result.

---

## Effectiveness Tracking

```text
Service → Effectiveness Tracking
```

The application compares data **before and after** a corrective measure.

Example:

| Metric | Before | After |
|---|---:|---:|
| Failures | 5 | 1 |
| Flight hours | 80 h | 95 h |
| Downtime | 12 h | 3 h |
| Cost | 45,000 | 10,000 |

The final engineering conclusion remains a human decision.

---

# 🧠 Diagnostics and Knowledge Base

## Knowledge Base

```text
Economics and Data → Knowledge Base
```

Create technical articles about:

- common faults;
- symptoms;
- verification methods;
- technical solutions.

## Diagnostics

```text
Service → Diagnostics
```

Veltrix Drone compares entered symptoms against the local knowledge base.

> [!WARNING]
> Diagnostics is an engineering aid, not an automatic final diagnosis.

---

# 🔳 QR Codes

Open:

```text
Supply → QR Codes
```

1. Select an entity type.
2. Select an object code.
3. Click **Generate QR Code**.
4. Use **Save PNG** if necessary.

QR can be used for:

- drone;
- battery;
- component;
- kit;
- inventory item.

---

# 📎 Attachments and Documents

Open:

```text
Economics and Data → Attachments
```

Supported attachments include:

- photos;
- PDF;
- DOCX;
- XLSX;
- TXT;
- other files.

Files are linked to a specific entity.

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

### Export

```text
Export entire database to XLSX
```

### Template

```text
Create import template
```

### Import

```text
Import XLSX
```

> [!WARNING]
> Always create a backup before a large import.

---

# 💾 Backups

Open:

```text
System → Backups
```

Recommended:

### Before major changes

Create a backup.

### Before updating Veltrix Drone

Create a backup.

### Before bulk Excel import

Create a backup.

### Before restoring another database

Create a backup of the current database first.

---

## Main data file

```text
dronebase.db
```

If this file is preserved, the core application records are preserved.

---

# 📱 Windows ↔ Android

Open:

```text
System → Mobile Connection
```

The Windows application starts a local API.

Architecture:

```text
Windows Veltrix
      ↕
 Local API / Wi-Fi
      ↕
Android Veltrix
```

The page displays:

- server state;
- local IP;
- port;
- access token;
- previously connected devices.

### Connection procedure

1. Connect PC and phone to the same Wi-Fi/LAN.
2. Start Mobile Connection on Windows.
3. Enter the Windows server address on Android.
4. Enter the token.
5. Start synchronization.

> [!WARNING]
> Do not publish the token and do not expose the local API port directly to the Internet.

---

# 👥 Users and Roles

Open:

```text
System → Users
```

It is recommended to create a separate account for every person.

| Role | Main purpose |
|---|---|
| Operator | daily operation |
| Technician | service and engineering |
| Storekeeper | inventory |
| Administrator | system management |

Avoid using one administrator account for everyone.

---

# 🔁 Typical Workflows

## Workflow 1 — New UAV

```text
Drones
→ Add UAV
→ Add photo
→ Define configuration
→ Assign components
→ Add LiPo
→ Configure maintenance regulations
→ Generate QR
```

---

## Workflow 2 — Normal Flight

```text
Planning
→ Dispatch
→ Preflight
→ Flight
→ Postflight
→ Flight Debrief
```

---

## Workflow 3 — Technical Fault Found

```text
Postflight remark
→ Diagnostics
→ Repair
→ Work Package
→ Bench Test
→ Return to Service
→ Validation Flight
→ Closure
```

---

## Workflow 4 — Component Replacement

```text
Inventory
→ Issue part
→ Drone
→ Components
→ Remove old component
→ Install new component
→ Bind node_key
→ Update configuration
```

---

## Workflow 5 — Repeating Problem

```text
Several failures
→ Reliability Case
→ Common Factors
→ Corrective Action
→ Implement measure
→ Effectiveness Tracking
→ Engineering conclusion
```

---

# 🔄 Updating the Application

## Recommended procedure

1. Close Veltrix Drone.
2. Create a backup.
3. Copy `dronebase.db` to a safe location.
4. Extract the new release.
5. Copy new application files over the current installation.
6. **Do not replace your working `dronebase.db`.**
7. Run `START_VELTRIX.bat`.

Current release:

```text
Veltrix Drone v1.0
DB Schema 64
```

> [!NOTE]
> Application version `v1.0` and database schema `64` are different versioning systems. This is normal.

---

# 📂 Where Data is Stored

Example structure:

```text
Veltrix_Drone/
│
├── app.py
├── version.json
├── requirements.txt
├── START_VELTRIX.bat
├── CHECK_PYTHON.bat
│
├── assets/
│
├── backups/
├── documents/
├── logs/
├── media/
├── qr_codes/
├── reports/
│
├── mobile_sync_server.py
├── veltrix_*.py
│
└── dronebase.db
```

| Path | Content |
|---|---|
| `dronebase.db` | main working database |
| `backups/` | backup files |
| `documents/` | documents |
| `media/` | photos and media |
| `reports/` | generated reports |
| `qr_codes/` | QR PNG files |
| `logs/` | technical logs |

---

# 🚫 What Must Not Be Uploaded to GitHub

Never publish:

```text
dronebase.db
dronebase.db-wal
dronebase.db-shm
```

Also avoid publishing:

```text
backups/
logs/
media/
documents/
reports/
qr_codes/
```

when they contain real operational data.

---

## Recommended `.gitignore`

```gitignore
__pycache__/
*.py[cod]
*.pyd

.venv/
venv/

dronebase.db
dronebase.db-wal
dronebase.db-shm
*.db-journal

backups/
logs/
media/
documents/
reports/
qr_codes/

.idea/
.vscode/

Thumbs.db
Desktop.ini
.DS_Store

*.tmp
*.bak
*.log
```

---

# 🧯 Troubleshooting

## Application does not start

Run:

```text
CHECK_PYTHON.bat
```

Check Python and dependencies.

---

## `ModuleNotFoundError`

A required dependency is missing.

See:

```text
requirements.txt
```

---

## Data disappeared after an update

Check that Veltrix Drone is using your original:

```text
dronebase.db
```

Do not overwrite a working database with a new empty one.

---

## Interface does not fit the screen

Check Windows display scaling.

Recommended test values:

```text
100%
125%
150%
```

---

## Drag & Drop does not work

Check whether:

```text
tkinterdnd2
```

is installed.

Attachments should still work through the normal file-selection button.

---

## Android cannot connect to Windows

Check:

1. both devices are on the same Wi-Fi;
2. the local server is running;
3. IP address is correct;
4. port is correct;
5. token is correct;
6. Windows Firewall allows access on private networks.

---

# ❓ FAQ

### Is Internet required?

No. Core functionality is local.

### Where is the database?

```text
dronebase.db
```

### Can I delete `dronebase.db`?

Not if it contains your working data.

### Why is the application version 1.0 but database schema 64?

Because `1.0` is the public product version and `64` is an internal database structure version.

### Is Android only a remote control for Windows?

No. The Android concept is a standalone local application with optional synchronization to Windows.

### Does Veltrix automatically decide that a component is broken?

No. Engineering modules help interpret recorded facts but do not replace a qualified technical conclusion.

---

# 🐞 Reporting an Issue

Create a **GitHub Issue** and include:

```text
Veltrix Drone:
v1.0

Windows:
Windows 10 / 11

Python:
version

Section:
for example "Repairs"

What you did:
...

Expected:
...

Actual:
...

Error / traceback:
...
```

Screenshots are welcome.

> [!WARNING]
> Do not attach your working `dronebase.db`, personal data or confidential documents.

---

# 📜 License

Veltrix Drone is distributed under the custom:

## Veltrix Drone Non-Sale License

Use is permitted according to the license terms.

Without written permission from the copyright holder, the following are prohibited:

- selling;
- reselling;
- paid redistribution;
- commercial repackaging;
- selling modified builds;
- paid SaaS based on the software;
- providing paid access to Veltrix Drone.

Full license text:

```text
LICENSE
```

> [!IMPORTANT]
> This is not a standard OSI Open Source License.

---

# 📦 GitHub Release

For the stable release use:

### Tag

```text
v1.0
```

### Release name

```text
Veltrix Drone v1.0 Stable
```

### Release asset

```text
Veltrix_Drone_v1.0_RELEASE.zip
```

---

<div align="center">

## Veltrix Drone v1.0

**Local engineering environment for the full UAV lifecycle**

```text
Drone → Flight → Event → Diagnostics → Repair → Verification → Operation → Reliability
```

**Stable · Windows · Offline-first · SQLite**

</div>
