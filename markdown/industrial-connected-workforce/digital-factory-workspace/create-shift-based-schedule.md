---
title: Create a shift-based schedule plan
description: Create a scheduled plan for standard tasks based on shift configuration of a functional location.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a schedule plan, Scheduling, Industrial Standards, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Create a shift-based schedule plan

Create a scheduled plan for standard tasks based on shift configuration of a functional location.

## Before you begin

Role required: sn\_icw\_std.standard\_author

To use shift-based scheduling with automatic time zone and time frame calculation, make sure that the following additional prerequisites are met:

-   Industrial shift configurations are defined for the functional location associated with the manufacturing standard.
-   The site location record linked to the functional location has a time zone defined. If the time zone isn’t defined, the system uses the logged-in user's time zone, which may cause tasks to be generated at unexpected times.

## About this task

In the [Create a standard schedule plan](create-events-based-on-schedules.md) procedure, you can create a customized schedule. If you want to create a shift-based schedule, select the **Shift** option at the top of the form before configuring the recurrence pattern.

## Procedure

1.  Select one or more shifts.

    The available shifts are determined by the industrial shift configuration associated with the functional location. When you enable shift-based scheduling:

    -   The **Start date/time** and **End date/time** fields are hidden.
    -   A **Start date** field is displayed with date only. Select the date from which the schedule plan starts initiating tasks.
    -   The system automatically calculates the start and end time frames based on the selected shifts and the production day configuration of the functional location.
    For more information about shift-based scheduling, see [Shift-based scheduling for manufacturing standards](../concept/icw-shift-based-scheduling.md).

2.  Verify the time zone displayed on the custom schedule page.

    The system automatically applies the time zone from the factory location. If a warning is displayed indicating that the time zone isn’t defined, you can:

    -   Select a different time zone from the displayed **Timezone** field.
    -   Select the link in the warning to navigate to the location record and add the missing time zone.

## Result

For shift-based schedules, the system generates standard tasks sequentially, one shift at a time, aligned with the shift boundaries defined in the industrial shift configuration. The system automatically manages the task lifecycle:

-   Tasks are released at the start of each selected shift on the scheduled dates.
-   Tasks that aren’t completed within the designated shift window are automatically expired.
-   Duplicate events and tasks are detected and cleaned up during schedule updates.
-   If the schedule is deactivated or modified, the system invalidates pending occurrences and adjusts future task generation accordingly.

**Parent Topic:**[Create a standard schedule plan](create-events-based-on-schedules.md)

