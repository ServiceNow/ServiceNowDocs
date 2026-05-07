---
title: Create a standard schedule plan
description: Create a plan for the scheduled creation of standard tasks.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Scheduling, Industrial Standards, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Create a standard schedule plan

Create a plan for the scheduled creation of standard tasks.

## Before you begin

To create a template schedule, you must define a schedule first. For more information about defining schedules, see [Define a schedule](https://www.servicenow.com/docs/access?context=t_DefineASchedule&version=australia&pubname=australia-platform-administration&ft:locale=en-US). To create a custom template that is based on shifts, refer to [Define a shift](define-shifts.md) to configure shifts.

Role required: sn\_icw\_std.standard\_author

## Procedure

1.  Open the standard for which you want to create a plan.

2.  Navigate to the tab **Scheduled Plans**.

3.  Select **New schedule**.

4.  On the Scheduled plan form, fill in the fields.

    For a description of field values, see [Schedule plan form](../reference/scheduled-plan-form.md).

5.  Select **Save**.

6.  For custom schedules, select **Custom schedule** to configure the scheduled plan.

7.  To create a shift-based schedule, enable the **Shift** option before filling in the Custom schedule form fields.

    **Note:** If you enable shift-based scheduling, the form hides the **Start date/time** and **End date/time** fields and displays a **Start date** field instead. The system automatically calculates the start and end time frames from the shift configuration. For more information, see [Create a shift-based schedule plan](create-shift-based-schedule.md).

8.  On the Custom schedule form, fill in the fields.

    For a description of field values, see [Custom schedule plan form](../reference/custom-schedule-plan-form.md).

9.  Select **Save**.


## Result

The new schedule plan is displayed in the list of schedule plans for the standard.

-   **[Create a shift-based schedule plan](create-shift-based-schedule.md)**  
Create a scheduled plan for standard tasks based on shift configuration of a functional location.

**Parent Topic:**[Scheduling standards](../concept/scheduling-standards.md)

