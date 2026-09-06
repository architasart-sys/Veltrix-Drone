<div align="center">

<img src="assets/veltrix_drone_logo.png" alt="Veltrix Drone" width="180">

# Veltrix Drone v1.0
## Complete User Manual

**Windows · Local Operation · UAV Fleet Operations · Service · Inventory · Reliability · Reporting**

[Русское руководство](VELTRIX_DRONE_USER_MANUAL_RU.md)

</div>

---

> [!IMPORTANT]
> This is the **end-user operating manual** for the current Veltrix Drone v1.0 Windows application. It explains workflows, screen purpose, major buttons and recommended operating practices.

> [!WARNING]
> Always create a backup through **`Система → Резервные копии` (System → Backups)** before an update, bulk import or restore operation.

# 1. What Veltrix Drone Does

Veltrix Drone connects the complete UAV lifecycle into one technical history:

```text
Drone
→ Planning
→ Dispatch
→ Preflight
→ Flight
→ Postflight
→ Diagnostics / Failure
→ Repair / Maintenance
→ Bench Test
→ Return to Service
→ Validation Flight
→ Reliability
→ History
```

The key operating principle is: **significant technical facts should be recorded and linked to the correct aircraft, node and work item**.

# 2. Installation and Updates

## New installation

1. Open GitHub **Releases**.
2. Download the latest stable Windows build.
3. Run the Windows `.exe` installer.
4. Complete the installation wizard.
5. Start Veltrix Drone from the shortcut or Start Menu.

## Update

1. In the existing application open `Система → Резервные копии`.
2. Create a database backup.
3. Preferably also create a full ZIP backup.
4. Close Veltrix Drone.
5. Install the newer build.
6. Start it and verify several drones, flights, batteries and repairs.

# 3. First Launch

The **`Первичная настройка` (Initial Setup)** screen asks for:

- organization/workshop name;
- administrator display name;
- administrator login — at least 3 characters;
- password — at least 6 characters;
- password confirmation.

Complete setup. Veltrix Drone then displays a **recovery code**.

Save this code separately from the password. A recovery code is required for self-service password recovery.

# 4. Login and Password Recovery

On **`Вход в систему` (Login)** enter the username and password.

If the password is forgotten, click **`Забыли пароль?`** and enter:

- username;
- saved recovery code;
- new password;
- repeated new password.

After a successful recovery, the previous recovery code becomes invalid and a new one is generated.

If the code is lost, another administrator can generate a new code under `Система → Пользователи`.

# 5. User Profile

The bottom of the sidebar contains:

- `Сменить пароль` — Change Password;
- `Код восстановления` — Recovery Code;
- `Выйти` — Log Out.

Generating a new recovery code invalidates the old one.

# 6. Roles

| Role | Main responsibility |
|---|---|
| **Оператор / Operator** | flight operations, planning and monitoring |
| **Техник / Technician** | repairs, maintenance, diagnostics, engineering workflows |
| **Кладовщик / Storekeeper** | inventory, procurement and kits |
| **Администратор / Administrator** | complete access, users, backups and system functions |

If a button is missing or disabled, verify both permissions and whether a record is selected.

# 7. Interface Basics

- Sidebar: section navigation.
- Page header: current module and main actions.
- `Поиск по разделу`: search within the current section.
- Filters: status/model/date and other screen-specific filters.
- Most record actions require selecting a table row first.
- `Открыть` means Open.
- The user profile is at the bottom-left.

# 8. Recommended New-System Setup Order

```text
1. Users
2. Drones
3. Batteries
4. Inventory
5. Components
6. Configuration
7. Maintenance Regulations
8. Planning and Flights
9. Repairs / Maintenance
10. Attachments
11. Backup
```

# 9. Data Quality Rules

1. Use stable unique codes such as `DRN-001`, `BAT-001` and clear SKUs.
2. Edit an existing object instead of creating duplicates.
3. Record faults when they are actually observed.
4. Do not record a hypothesis as a confirmed failure.
5. When replacing a component, update both inventory and actual aircraft configuration.
6. Complete the required verification/RTS workflow after technical work.
7. Create backups regularly.
8. Verify corrective-action effectiveness before closing it.

# 10. Core Daily Workflows

## Normal sortie

```text
Планирование
→ Диспетчер вылетов
→ Preflight
→ Полёт
→ Postflight
→ Разбор полётов
```

## Technical problem

```text
Remark
→ Диагностика
→ Repair / Maintenance
→ Work Package
→ Bench Test
→ Return to Service
→ Validation Flight
```

## Component replacement

```text
Склад
→ Issue
→ Детали
→ Remove old part
→ Install new part
→ Bind correct node
→ Configuration Control
```

## Repeated failure

```text
Confirmed Failures
→ Reliability Case
→ Common Factors
→ Corrective Action
→ Effectiveness Tracking
→ Report
```

# 11. Quick Setup of a New UAV

1. Open `Операции → Дроны → + Добавить`.
2. Create a unique drone code.
3. Open the Drone Card.
4. Add actual components through `Сервис → Детали`.
5. Bind components to their actual nodes.
6. Verify `Сервис → Контроль конфигурации`.
7. Add batteries through `Операции → Аккумуляторы`.
8. Configure relevant maintenance regulations.
9. Generate a QR code if useful.
10. Create a backup after initial setup.


# 12. Complete Screen Reference

The table and subsections below cover **every sidebar screen in the current Veltrix Drone v1.0 Windows application**. Because the current Windows UI uses Russian labels, the exact Russian menu/button text is shown in code formatting so you can locate it reliably.


## Operations (`Операции`)


### Dashboard — `Главная`

Fleet readiness, service, inventory and warnings overview.


**Main on-screen actions:** `Командный центр` · `Сервис`.


### Fleet Command Center — `Командный центр`

Fleet-wide aircraft availability and technical restriction overview.


**Main on-screen actions:** `Планировщик` · `Календарь` · `Диспетчер` · `Сервис` · `Возврат` · `Надёжность` · `Полёты` · `Открыть карточку` · `Тренды` · `Дроны` · `+ Назначение` · `+ Полёт`.


### Mission Planning — `Планирование`

Assign drones, pilots and batteries to future sorties.


**Main on-screen actions:** `Открыть` · `Карточка вылета` · `Командный центр` · `Календарь` · `Готовность` · `+ Назначение` · `Редактировать`.


### Dispatch Center — `Диспетчер вылетов`

Check readiness for a specific time window and inspect blocking reasons.


**Main on-screen actions:** `Календарь` · `История` · `Проверить` · `Причины` · `Открыть дрон` · `Сохранить снимок` · `Назначить вылет`.


### Operations Calendar — `Операционный календарь`

Unified timeline for sorties, maintenance, repairs, deliveries and blocks.


**Main on-screen actions:** `Конфликты` · `←` · `Сегодня` · `→` · `+ Блокировка`.


### Flight Debrief — `Разбор полётов`

Combine planning, Dispatch, Preflight, flight, analysis, Postflight and failures.


**Main on-screen actions:** `Полёты` · `Открыть разбор` · `Корректирующие меры`.


### Drones — `Дроны`

UAV registry and access to the electronic aircraft card.


**Main on-screen actions:** `Открыть карточку` · `+ Добавить` · `Редактировать`.


### Flights — `Полёты`

Flight history, telemetry, comparison, trends and reference/validation workflows.


**Main on-screen actions:** `Открыть` · `Разбор вылета` · `Сравнить полёты` · `История сравнений` · `Тренды дрона` · `+ Новый полёт` · `Контрольные полёты` · `Эталонные полёты` · `Сделать эталоном` · `Редактировать`.


### Batteries — `Аккумуляторы`

LiPo Center: battery identity, cycles, condition, measurements and events.


**Main on-screen actions:** `Открыть LiPo` · `+ Добавить LiPo` · `+ Измерение` · `+ Событие`.


## Service (`Сервис`)


### Service Center — `Центр ТО`

Fleet-wide service queue for maintenance, repairs and due work.


**Main on-screen actions:** `Календарь 30 дней` · `Открыть` · `+ Новое ТО` · `+ Ремонт` · `Прогноз запчастей` · `Прогноз ТО` · `Наряды` · `Техцикл` · `Начать ТО` · `Пауза ТО` · `Выполнить ТО` · `Планировать`.


### Repairs — `Ремонты`

Repair request, diagnosis, repair, verification and closure workflow.


**Main on-screen actions:** `Открыть` · `+ Новый ремонт` · `Редактировать`.


### Maintenance — `Обслуживание`

Scheduled maintenance by date/flight hours, service state and history.


**Main on-screen actions:** `Календарь сервиса` · `История ТО` · `+ Добавить ТО` · `Прогноз ТО` · `Начать` · `Пауза` · `Выполнить ТО` · `Редактировать`.


### Components — `Детали`

Physical components, resource tracking and exact node binding.


**Main on-screen actions:** `Открыть историю` · `Тренды узлов` · `+ Добавить деталь` · `Мастер 3D-привязки` · `Редактировать`.


### Checklists — `Чек-листы`

Saved technical inspections with result for every checklist item.


**Main on-screen actions:** `+ Новый осмотр` · `Открыть результат`.


### Diagnostics — `Диагностика`

Local symptom matching against the knowledge base; technician verification required.


**Main on-screen actions:** `Сохранить результат` · `Создать заявку на ремонт` · `Проанализировать` · `История диагностики`.


### Corrective Actions — `Корректирующие действия`

Manage corrective measures from issue to verification and closure.


**Main on-screen actions:** `Открыть` · `Возврат` · `+ Новое действие`.


### Configuration Control — `Контроль конфигурации`

Approved baseline, revisions, change comparison and release linkage.


**Main on-screen actions:** `Инженерный центр` · `История ревизий` · `Возврат в эксплуатацию` · `Открыть` · `История FC` · `Стенд` · `Аудит FC`.


### Bench Tests — `Стендовые проверки`

Functional bench verification after repairs/configuration changes.


**Main on-screen actions:** `История` · `Возврат в эксплуатацию` · `Открыть проверку`.


### Return to Service — `Возврат в эксплуатацию`

Final Return to Service gate after technical work.


**Main on-screen actions:** `История` · `Корректирующие меры` · `Проверить` · `Контрольные полёты` · `Стенд` · `Конфигурация`.


### Validation Flights — `Контрольные полёты`

Validation flights after repair, configuration or release work.


**Main on-screen actions:** `Полёты` · `Планировщик` · `Открыть` · `Эталонные полёты`.


### Reference Flights — `Эталонные полёты`

Accepted reference flights used as a comparison baseline.


**Main on-screen actions:** `Контрольные полёты` · `Полёты` · `Открыть` · `Тех. здоровье` · `Мониторинг деградации`.


### Degradation Monitoring — `Мониторинг деградации`

Repeated deviation monitoring against reference flight data.


**Main on-screen actions:** `Эталонные полёты` · `Корректирующие меры` · `Открыть` · `Тех. здоровье` · `Тренды узлов`.


### Technical Health — `Тех. здоровье`

Combined factual technical condition across fleet data sources.


**Main on-screen actions:** `Деградация узлов` · `Командный центр` · `Открыть` · `Техразбор` · `Прогноз ТО`.


### Predictive Maintenance — `Прогноз ТО`

Maintenance recommendations based on recorded resource, plans and technical evidence.


**Main on-screen actions:** `Центр ТО` · `Тех. здоровье` · `Открыть` · `Техразбор`.


### Technical Review — `Техразбор`

Structured engineering review combining evidence, localization and technician decision.


**Main on-screen actions:** `Прогноз ТО` · `Тех. здоровье` · `Открыть` · `Наряды` · `Создать / открыть наряд`.


### Work Packages — `Наряды`

Work Packages: operations, personnel, parts, time, cost and result.


**Main on-screen actions:** `Техразбор` · `Центр ТО` · `Открыть` · `Техцикл`.


### Technical Cycle — `Техцикл`

End-to-end technical closure from work package through validation.


**Main on-screen actions:** `Наряды` · `Открыть` · `Стенд`.


### Engineering Command Center — `Инженерный центр`

Unified engineering command view of reliability, actions, configuration and cycles.


**Main on-screen actions:** `Надёжность` · `Отчёты` · `Конфигурация` · `Сохранить снимок`.


### Reliability — `Надёжность`

Confirmed failures relative to recorded utilization, recurrence and downtime.


**Main on-screen actions:** `История снимков` · `Инженерный центр` · `Открыть отказ` · `Тренды узлов` · `Системные случаи` · `Эффективность` · `Отчёты` · `+ Зафиксировать отказ` · `Редактировать`.


### Node Trends — `Тренды узлов`

Long-term history and degradation evidence for exact technical nodes.


**Main on-screen actions:** `Надёжность` · `Открыть узел` · `Системные случаи` · `Дрейф / эталон`.


### Reliability Cases — `Системные случаи`

Reliability Cases for repeated confirmed failures by model/node.


**Main on-screen actions:** `Надёжность` · `Эффективность` · `Открыть` · `Тренды узлов` · `Отчёты` · `Создать / открыть случай`.


### Effectiveness Tracking — `Эффективность мер`

Before/after verification of corrective measures using factual metrics.


**Main on-screen actions:** `Системные случаи` · `Отчёты надёжности`.


### Reliability Reports — `Отчёты надёжности`

Generate fixed fleet/model/node/case reliability reports.


**Main on-screen actions:** `Тех. отчёты` · `Инженерный центр` · `Обновить` · `Системные случаи` · `Сформировать DOCX` · `Снимок JSON`.


### Regulations — `Регламенты`

Maintenance procedures and intervals.


**Main on-screen actions:** `+ Новый регламент` · `Создать план ТО по регламенту`.


## Supply (`Снабжение`)


### Inventory — `Склад`

Inventory balance, movements and minimum stock control.


**Main on-screen actions:** `Прогноз закупок` · `История` · `QR-код` · `+ Новая позиция` · `Закупки` · `Редактировать`.


### Procurement — `Закупки`

Procurement requests, ordering and partial/full receipt.


**Main on-screen actions:** `Прогноз запчастей` · `Открыть` · `+ Новая заявка`.


### Kits — `Комплекты`

Equipment/spare-part kits and completeness.


**Main on-screen actions:** `Открыть комплект` · `QR-код` · `+ Новый комплект` · `Редактировать` · `Удалить`.


### QR Codes — `QR-коды`

Generate local QR identifiers for Veltrix entities.


**Main on-screen actions:** `Сформировать QR-код` · `Сохранить PNG`.


## Economics & Data (`Экономика и данные`)


### Analytics — `Аналитика`

High-level cost, reliability, service and inventory analytics.


**Main on-screen actions:** `Надёжность парка`.


### Economics — `Экономика`

Actual fleet operating cost tracking.


**Main on-screen actions:** `Бюджет / стоимость` · `+ Расход` · `Сохранить снимок` · `Удалить`.


### Budget & TCO — `Бюджет и стоимость владения`

Budget, commitments, forecast and total cost of ownership.


**Main on-screen actions:** `Экономика` · `+ Бюджет` · `+ Плановый расход` · `Снимок` · `Архивировать` · `Провести в факт` · `Отменить`.


### Assistant — `Помощник`

Local fleet summary and explainable priorities/recommendations.


**Main on-screen actions:** `Обновить анализ` · `Спросить` · `Показать техническую сводку` · `Отметить выполненной`.


### Knowledge Base — `База знаний`

Offline technical knowledge articles used by diagnostics.


**Main on-screen actions:** `+ Новая статья`.


### Technical Reports — `Тех. отчёты`

Generate technical DOCX documents and access stored reports.


**Main on-screen actions:** `Отчёты по надёжности` · `Открыть папку отчётов` · `Сформировать DOCX`.


### Attachments — `Вложения`

Manage linked photos and files.


**Main on-screen actions:** `Открыть файл` · `Папка файла` · `Обновить` · `+ Добавить файлы` · `Изменить` · `Удалить`.


### Excel — `Excel`

Export, import template and controlled XLSX import.


**Main on-screen actions:** `Импортировать XLSX` · `Экспортировать всю базу в XLSX` · `Создать шаблон для импорта`.


## System (`Система`)


### Users — `Пользователи`

User accounts, roles, passwords, recovery codes and access state.


**Main on-screen actions:** `+ Добавить пользователя` · `Редактировать` · `Сбросить пароль` · `Новый код восстановления` · `Вкл/выкл доступ`.


### Action Log — `Журнал действий`

Audit history of who changed what and when.


This screen is primarily for review/search rather than record creation.


### Recycle Bin — `Корзина`

Restore deleted records or permanently delete them.


**Main on-screen actions:** `Восстановить` · `Удалить окончательно`.


### Backups — `Резервные копии`

Database backups, full ZIP backups and restore.


**Main on-screen actions:** `Создать копию БД` · `Полная ZIP-копия` · `Восстановить выбранную` · `Открыть папку backups`.


### Mobile Connection — `Мобильная связь`

Secure local Windows ↔ Android synchronization service.


**Main on-screen actions:** `Копировать` · `Новый токен` · `Остановить мобильную связь` · `Запустить мобильную связь`.


### System Diagnostics — `Диагностика системы`

Check storage, database, backups and basic application health.


**Main on-screen actions:** `Запустить проверку` · `Диагностическая ZIP-копия` · `Отчёт DOCX` · `Оптимизировать БД` · `Открыть logs`.


# 13. Practical Instructions for Major Workflows

## 13.1 Drones

Open `Операции → Дроны`.

Use `Открыть карточку` (Open Card), `+ Добавить` (Add) and `Редактировать` (Edit).

Use a permanent internal code. After creating the registry record, open the Drone Card and complete actual configuration, batteries, documents and history.

## 13.2 LiPo

Open `Операции → Аккумуляторы`.

The current battery card supports chemistry, cell count, capacity, C-rating, cycles, cycle limit, remaining resource, voltage, storage state, technical status, dates, cost, deep-discharge information, thresholds, photo and notes.

Create one record per physical battery.

## 13.3 Planning and Dispatch

Create an assignment under `Операции → Планирование`, then use `Операции → Диспетчер вылетов`.

In Dispatch:

1. select the time window;
2. select the aircraft;
3. click `Проверить` (Check);
4. use `Причины` (Reasons) if restricted;
5. resolve factual blockers;
6. repeat the readiness check.

## 13.4 Flight and Debrief

Use `+ Новый полёт` under Flights. Complete Postflight and open `Разбор вылета` for significant sorties.

If there is a technical remark, verify whether a diagnostics record, confirmed failure, repair, maintenance item or corrective action is required.

## 13.5 Repair

Open `Сервис → Ремонты → + Новый ремонт`.

Write specific factual descriptions. Avoid “does not work.” Prefer descriptions such as “crack found on front-right arm after landing; increased vibration observed on FR motor check.”

After work, use Work Package, Bench, RTS and Validation Flight when the technical impact requires them.

## 13.6 Maintenance

Open `Сервис → Обслуживание`.

Typical sequence:

```text
Add Maintenance
→ Start
→ perform work
→ Complete Maintenance
```

On completion record date, flight hours, technician, cost and actual work.

Use `Сервис → Регламенты` for repeated procedures.

## 13.7 Components and Configuration

Use `Сервис → Детали` to track physical parts and link them to the correct drone/node. After a significant replacement, update Configuration Control.

## 13.8 Bench and RTS

Bench result values include `Не проверено`, `ОК`, `Замечание`, `Не пройдено`, `Н/П`.

Return to Service checks related records, mechanics, propulsion, power, controls/failsafe, video/navigation, configuration and documentation. If a validation flight is required, the technical cycle is not finished before that gate is completed.

## 13.9 Work Packages and Technical Cycle

Work Package states:

```text
Черновик
Назначен
В работе
Приостановлен
Выполнен
Отменён
```

Technical Cycle:

```text
Наряд
→ Характер работ
→ Связанные факты
→ Стендовая проверка
→ Return to Service
→ Контрольный полёт
→ Завершён
```

## 13.10 Reliability

Use `+ Зафиксировать отказ` only for a confirmed failure.

Reliability Case states are:

```text
Открыт
Анализ
Действия
Проверка
Закрыт
Отменён
```

Human effectiveness outcomes are:

```text
Не проверено
Эффект подтверждён
Эффект не подтверждён
Недостаточно данных
```

For a repeated failure, open Reliability Cases, confirm evidence, create corrective actions, allow an adequate observation period, then verify effectiveness and record the human conclusion.

## 13.11 Inventory

When recording stock movement, enter quantity, related drone/object when applicable, recipient/returner, reason and document reference. Movement history is more valuable than silently editing balance.

## 13.12 Procurement

Typical lifecycle:

```text
Черновик
→ Согласовано
→ Заказано
→ Частично получено
→ Получено
```

Items are added while the request is Draft. Record actual receipt through Procurement so Inventory is updated correctly.

## 13.13 Attachments

Link a file to the entity it actually documents. A damage photo is best linked to the relevant repair, while aircraft technical documentation belongs to the drone.

## 13.14 Excel

For controlled import:

1. use `Создать шаблон для импорта`;
2. fill the template;
3. create a backup;
4. use `Импортировать XLSX`;
5. review the import result.

The current bulk import adds new drones, batteries and inventory items. It should not be treated as a blind overwrite mechanism.

# 14. Users and Access Security

Administrators manage users under `Система → Пользователи`.

Available functions include adding users, changing roles, password reset, new recovery code and enabling/disabling access.

Use individual accounts rather than sharing one administrator account; otherwise the Action Log loses accountability value.

# 15. Recycle Bin

`Восстановить` restores a deleted record. `Удалить окончательно` permanently removes it from the Recycle Bin.

A restore may fail when another record already uses the same unique code.

# 16. Backups and Restore

Open `Система → Резервные копии`.

Use `Создать копию БД` before updates, bulk import, major changes or restore.

Use `Полная ZIP-копия` when a portable backup including user files is required.

Restore procedure:

1. select a backup;
2. click `Восстановить выбранную`;
3. confirm;
4. Veltrix creates a safety copy of the current state;
5. wait for completion;
6. log in again.

Do not interrupt a restore.

# 17. Windows ↔ Android

Open `Система → Мобильная связь`.

1. Connect PC and phone to the same private Wi‑Fi/LAN.
2. Check the port.
3. start mobile connection;
4. copy the server address;
5. copy the token;
6. enter both on Android;
7. synchronize;
8. verify the device appears in the device list.

Do not expose the local port to the public Internet and never publish the token. In Windows Firewall, allow access only on private networks.

# 18. System Diagnostics

Open `Система → Диагностика системы`.

If a problem occurs:

1. run the system check;
2. review the result;
3. create a Diagnostic ZIP or DOCX report when needed;
4. include the error and reproduction steps in a GitHub Issue.

Database optimization is maintenance, not a substitute for correcting bad records.

# 19. Settings

Administrators open `Настройки` at the bottom of the sidebar.

Settings include organization/workshop name, daily automatic backup and backup retention. Save after changes.

# 20. Recommended Operating Routine

## Daily

- review Dashboard;
- review Fleet Command Center;
- review Service Center;
- review Operations Calendar;
- record every actual flight;
- complete Postflight;
- record significant faults.

## Weekly

- review low inventory;
- review procurement;
- review overdue maintenance;
- review open corrective actions;
- review Reliability;
- create a manual backup.

## Before major changes

Always back up before update, bulk import, restore or large data operations.

# 21. If a Button Is Unavailable

Check:

1. whether a row is selected;
2. whether the role has permission;
3. whether the record is in the required state;
4. whether required linked data exists.

Example: Procurement items can only be added while a request is `Черновик` (Draft).

# 22. If Data Appears Missing

Do not immediately create duplicates.

1. Clear section search.
2. Reset filters.
3. Refresh the screen if available.
4. Check Recycle Bin.
5. If the issue followed an update/restore, review backups.
6. If Android is involved, synchronize again.

# 23. If the Application Does Not Start or Shows an Error

1. Record the exact error.
2. Restart the application/Windows if appropriate.
3. Verify you are using the latest Stable release.
4. Run System Diagnostics if the application can be opened.
5. Create a GitHub Issue.

Include:

```text
Veltrix Drone: v1.0
Windows:
Screen:
Action:
Expected:
Actual:
Error:
```

Do not upload confidential operational data.

# 24. FAQ

### Is Internet required?
No for normal local work.

### Does Windows work without Android?
Yes. The Windows application is standalone.

### Is Android required?
No. It is an additional standalone mobile edition with synchronization capability.

### Why is Reliability nearly empty in a new installation?
It needs real utilization, failure and technical-work history.

### Does Veltrix automatically decide that a drone is safe?
No. It organizes factual evidence and workflow gates. The responsible technical decision remains with qualified personnel.

### Can permanently deleted records be restored?
Not through the application.

### How should data be protected?
Regular backups plus a full ZIP backup before major changes.

# 25. Glossary

| Term | Meaning |
|---|---|
| **Dispatch** | readiness for a specific sortie |
| **Preflight** | preflight check |
| **Postflight** | postflight check |
| **RTS** | Return to Service |
| **Work Package** | formal technical work package |
| **Technical Cycle** | end-to-end technical closure |
| **Reliability Case** | repeated-failure engineering case |
| **Corrective Action** | corrective measure |
| **Effectiveness Tracking** | verification of measure effectiveness |
| **Reference Flight** | accepted baseline flight |
| **Validation Flight** | post-work confirmation flight |
| **LiPo** | battery pack |
| **SKU** | inventory item code |

# 26. License

Veltrix Drone is distributed under the **Veltrix Drone Non-Sale License**.

Sale, resale, paid redistribution, commercial repackaging and paid access require separate written permission from the copyright holder.

See `LICENSE` for the full legal terms.

---

<div align="center">

## Core operating principle

```text
Fact → Record → Link → Verification → Decision → History
```

**The engineering picture is only as good as the records entered into the system.**

</div>
