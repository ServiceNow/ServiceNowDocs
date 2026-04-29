---
title: Configure SLA repair
description: Administrators can set SLA repair properties and view repair logs.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Repair Service Level Agreement \(SLA\), Using Service Level Management, Service Level Management, IT Service Management]
---

# Configure SLA repair

Administrators can set SLA repair properties and view repair logs.

## Enable or disable SLA repair

The Repair SLA function is enabled for all new installed instances running the 2011 engine, but is disabled by default for upgraded instances. If disabled, no SLA repair functions are available, including all SLA repair modules, SLA repair logs, and UI actions.

**Note:** Repair actions will not be available for instances that are not running the 2011 engine. To enable or disable SLA repair, use the **com.snc.sla.repair.enabled** repair property.

## View repair logs

An SLA repair log record is created each time a repair action takes place with details such as who initiated the repair and start and end date and time. The log record contains a number of child **SLA Repair Log Entry** records related to it. Each repair log entry has a type of either **Before repair** or **After repair** that will contain the appropriate values from each Task SLA record that is repaired. If there is only a **Before repair** entry record for a task SLA, this indicates that it has been deleted. If there is only an **After record**, the repair function has created a task SLA that did not previously exist.

Navigate to **Service Level Management** &gt; **Repair Logs** to view repair log information:

-   **Active Repairs**: view repairs that are still in progress.
-   **My Repairs**: view repairs you have run.
-   **All Repairs**: view all repairs.
-   **Repair Entries**: view SLA Repair Log entries for all repairs that have run.

**Parent Topic:**[Repair Service Level Agreement \(SLA\)](../concept/c_RepairSLAs.md)

