---
title: Create a move project from existing move requests
description: As a move manager, create a move project to logically group move requests based on different criteria and fulfill them on priority.
locale: en-US
release: zurich
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-25"
reading_time_minutes: 3
breadcrumb: [Working with Move management, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Create a move projectfrom existing move requests

As a move manager, create a move project to logically group move requests based on different criteria and fulfill them on priority.

## Before you begin

Ensure that you have the following plugins installed:

-   Workplace Central
-   Workplace Move Management

Role required: sn\_wsd\_move.manager

## About this task

Create a move project to group multiple move requests into a single project to oversee and manage them. Specify conditions based on which the move requests must be filtered to group them under the project. You can set conditions to group workplace move requests based on their workplace location, building, space type, assignment group, department, and more. Provide a name and give a short description to the project.

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Workplace Central**.

    You can also open Workplace Central from the Employee Center directly. Navigate to **Workspaces** &gt; **Workplace Central**.

2.  Select the Move management \(![Move management icon.](../images/move-mgmt-icon-central.png)\) module.

3.  Select **Create project**.

    You can also create a move project from the following locations:

    -   Select **My active projects** tile and select **Create** in the list view.
    -   In the **All move projects** section, select **View all**. In the list view, select **Create**.
    -   You can also create a move project when you deploy a scenario. After you select the **Deploy** action, in the dialog box, select **Create move project**.

        **Important:** The option is displayed only if there are any workplace user or workplace location moves in the scenario.

4.  On the Create a move project form, specify a name and short description for the project.

5.  Select **Select from existing move requests**.

6.  In the **Editor** section, specify your conditions.

    By default, the project is created with Project and Active conditions that you can’t remove.

    1.  To add a condition, select **+New condition set**.

    2.  Set a condition based on which you want to filter move requests to this project.

7.  Create the project by selecting **Create**.


## Result

The move project is created and all the move requests that have matched the filter conditions that you specified are displayed in the move scheduler. The move requests are displayed to you in the schedule view by default. The planned start and end date of the project are set based on the minimum **Expected start** date and the maximum **Due date** from the move requests that are associated with the project.

A move project contains both the schedule view and a list view. For more information on Move projects, refer to [Move project views, actions, and states](../reference/move-project-schedule-view.md).

## What to do next

[Work on a move project](work-on-a-move-project.md).

**Parent Topic:**[Working with Move management](../concept/working-with-move-management.md)

**Related topics**  


[Create a move project by uploading an Excel file](create-move-project-excel.md)

[Work on a move project](work-on-a-move-project.md)

