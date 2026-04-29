---
title: Convert an SLA to an SLA Definition
description: You must replicate the default SLA record as a new SLA definition.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Level Agreement \(Legacy\) engines, Service Level Management reference, Service Level Management, IT Service Management]
---

# Convert an SLA to an SLA Definition

You must replicate the default SLA record as a new SLA definition.

## Before you begin

Role required: admin

## About this task

To convert old SLAs to SLA Definitions:

## Procedure

1.  Transfer the **Name** and **Table** fields.

2.  If desired, check the **Retroactively Start** checkbox.

    If checked, this will cause the SLA to calculate from the moment the record is created \(or from the date and time on the selected task\), rather than the moment the SLA is attached. This is especially helpful for Task SLAs that will attach to active incidents that have old SLAs currently running.

3.  Transfer the **Conditions** field to the **Start Conditions** field.

    Make sure to add **Active is True** as well, so that the new Task SLAs don't attach to closed incidents when they are updated.

4.  Define a new set of **Pause Conditions** and **Close Conditions**.

5.  Set the **Duration Type** and **Duration** fields.

    The old SLAs did not support relative duration, so to define the Task SLA to behave similarly to the old SLA, select **User Defined Duration** as the **Duration Type** and put the total length of time of all of the escalations here.

    For instance, an old SLA that has escalations of 4 hours to Moderate, 2 hours to High, and 2 hours to Overdue, the new Task SLA should have **Duration** set to **Days 0 Hours 08:00:00**.

6.  Calendars have been replaced by Schedules, so if schedules haven't been defined yet, they will need to be.

7.  Instead of escalations, attach an SLA Workflow.

    There is a default SLA workflow, however, you must create a new workflow to replicate the escalation levels on the old SLA. Escalation Levels are defined hour-by-hour, whereas the SLA Workflow uses a percentage timer.

    So for the above example of 4 hours to Moderate, 2 hours to High, and 2 hours to overdue, the workflow will need a 50% timer and then two 25% timers. The new task SLA records do not use the **Escalation** or **Made SLA** fields on the task record.


## Example

The following example is an old SLA for Priority 1 incidents to be resolved on a Monday-Friday \(8-5\) Calendar, with escalations to Moderate at 4 hours, to High at 2 hours, and to Overdue at 2 hours:

![Old SLA form.](../image/OldSLA.png "Old SLA example")

This is the new Task SLA created from the same information:

![New SLA form.](../image/NewSLA.png "New SLA example")

This is the workflow which powers the new Task SLA.

**Note:** This example workflow responds to each escalation by firing off an event. A business rule can be configured to respond to escalation events, or the workflow can be adjusted to match the organization's process.

![Diagram of the new SLA workfow.](../image/NewSLAWorkflow.png "New SLA workflow")

**Parent Topic:**[Service Level Agreement \(Legacy\) engines](../concept/c_GetStartedWithSLAs.md)

