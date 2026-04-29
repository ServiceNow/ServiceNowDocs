---
title: Organize the migration process
description: There are several ways to convert the old SLAs to the new Task SLAs.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Level Agreement \(Legacy\) engines, Service Level Management reference, Service Level Management, IT Service Management]
---

# Organize the migration process

There are several ways to convert the old SLAs to the new Task SLAs.

## Before you begin

Role required: admin

## About this task

Perform the following steps to organize the conversion process:

## Procedure

1.  Convert the old SLAs to new SLA Definitions, but leave the Active flag unchecked on each one.

2.  Back up the old SLAs by exporting the table to XML.

3.  Deactivate the old SLAs, setting the **Run the old SLA engine \(System Policy -&gt; SLA Management\)** system property \(**com.snc.sla.run\_old\_sla\_engine**\) to **false**.

    This setting deactivates the legacy SLA engine preventing both engines from running and conflicting. This property is set to true by default, but will be set to false by the new SLA plugins, effectively deactivating the old SLAs.

4.  Activate the new SLA Definitions by checking the Active flags on each one.

5.  Navigate to **Incident** &gt; **Open** and use the List Editor to "touch" each record.

    As each record is updated, the new Task SLA will attach to each incident. If there are too many open incidents to effectively touch using the List Editor, run a business rule that will update every open incident.


**Parent Topic:**[Service Level Agreement \(Legacy\) engines](../concept/c_GetStartedWithSLAs.md)

