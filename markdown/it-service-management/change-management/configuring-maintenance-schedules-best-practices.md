---
title: Configuring maintenance schedules - Best practices
description: Maintenance schedules define the periods during which a Configuration Item or change can be implemented.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2024-07-31"
reading_time_minutes: 2
breadcrumb: [Reference section for Change Management, Change Management, IT Service Management]
---

# Configuring maintenance schedules - Best practices

Maintenance schedules define the periods during which a Configuration Item or change can be implemented.

These schedules are incorporated into the conflict detection process for change requests. If a change request doesn't adhere to the relevant maintenance schedule, a conflict record is generated for the change request.

There are two ways to define Maintenance schedules for Conflict Detection:

-   [Configure maintenance schedule](../task/t_CreateBlkoutMaintSched.md). This path is enabled through the change.conflict.currentwindow system property.
-   Create maintenance schedule using Schedules table \[cmn\_schedule\]. This method can be enabled using the change.conflict.ci\_maint\_sched system property.

    **Note:** These system properties can be configured on the Conflict properties.


## Maintenance schedule using schedule maintenance form

All Maintenance Schedules defined through this method are processed based on the condition field, which must be evaluated to determine its applicability to the change request, the primary CI, or the associated Affected CIs \(if they are executed in Advanced mode\).

It should be noted that the presence of multiple Maintenance Schedules extends the time required to determine their relevance, and this duration increases with each Affected CI.

If a generic schedule is applicable to numerous CIs or change requests, you must define a maintenance schedule using [Configure maintenance schedule](../task/t_CreateBlkoutMaintSched.md).

However, if your schedules are tailored to a limited number of CIs, you must consider creating maintenance schedule using schedules table.

![Maintenance schedule](../image/cmn_schedule_maintenance_form.png)

## Maintenance schedule using schedules table

This method is designed where individual CIs or small groups of CIs must follow a specific schedule.

In such cases, the maintenance schedule should be set in the Schedule table \(cmn\_schedule\) instead of the maintenance schedule table. This approach prevents the need for conflict detection to process the schedule twice using maintenance form and the schedule table.

Unlike the maintenance schedule record, the schedule record lacks a condition or an **Applies to** field, as it is intended to be directly associated with a CI. After defining the schedule record, the **Type** must be set as `maintenance` to link to a CI. To attach this schedule to a CI, it should be referenced in the **Maintenance schedule** field on the CI record; if this field is not visible, it must be added to the form.

![Schedules table](../image/cmn_schedule_form.png)

**Parent Topic:**[Reference section for Change Management](reference-change-management.md)

