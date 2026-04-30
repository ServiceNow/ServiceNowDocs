---
title: Managing an equipment model entity schedule
description: You can manage an equipment model entity schedule with the Industrial Process Manager application. By using a schedule, you can track several maintenance tasks for one equipment model entity.
locale: en-US
release: yokohama
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure, Industrial Process Manager, Operational Technology]
---

# Managing an equipment model entity schedule

You can manage an equipment model entity schedule with the Industrial Process Manager application. By using a schedule, you can track several maintenance tasks for one equipment model entity.

## Equipment model entity schedule overview

You can link schedules to any equipment model entity. If you have the Equipment Model Downtime Planner role \(sn\_isa\_schedule\_admin\), you can add, modify, or delete the schedule entries of an equipment model entity and do the following tasks:

-   Maintain the schedules for the various equipment model entities.
-   Associate these schedules with equipment model entities.
-   Pick a time slot from a schedule so that you can work on an Operational Technology \(OT\) incident or remediation task. For more information, see [Select a start time for an OT remediation task](../../mftg-manufacturing-ot-vulnerability-response/task/select-start-time-for-ot-remediation-task.md).

## Examples

Let's say that you want to set multiple schedule entries for one equipment model entity schedule. These entries complete different tasks and occur at different times. You can do so by creating schedule entries in the Schedule Entries related link of the existing equipment model entity schedule record.

If you no longer want a schedule associated with an equipment model entity, you can detach the schedule by using the Schedules related link in the equipment model entity record.

If you want to view existing schedules for an equipment model entity, you can do so in the Equipment Model Manager or in the Planned Downtime module on the Platform.

-   **[Create an equipment model entity schedule](../task/create-equipment-model-entity-schedule.md)**  
Create an equipment model entity schedule with the Industrial Process Manager application. With these schedules, you can easily maintain multiple equipment model entities.
-   **[Create a schedule entry](../task/create-new-schedule-entry.md)**  
Create a schedule entry for an existing equipment model entity schedule in the Industrial Process Manager application. You can create more than one entry for a schedule. Schedule entries allow multiple maintenance tasks to take place for one equipment model entity.
-   **[Associate a schedule with an equipment model entity](../task/associate-schedules-with-equipment-model-entity.md)**  
Create one or more maintenance schedules for an equipment model entity, edit an existing schedule, or delete schedules with the Industrial Process Manager application.
-   **[Add a child schedule](../task/create-child-schedules.md)**  
Add a child schedule to an existing equipment model entity schedule with the Industrial Process Manager application. When you make adjustments to the child schedule, it also applies to the parent schedule. For example, you might want to extend the scheduled time on a particular day or remove the holidays from a schedule.

**Parent Topic:**[Configuring the Industrial Process Manager](configuring-manufacturing-process-mgr.md)

