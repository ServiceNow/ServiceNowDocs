---
title: Create a Health and Safety action schedule
description: Create an action schedule to schedule actions across the organization such as learning activities and recurring tasks.
locale: en-US
release: yokohama
product: Health and Safety Core
classification: health-and-safety-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Schedule actions, Use, Health and Safety Core, Health and Safety, Employee Service Management]
---

# Create a Health and Safety action schedule

Create an action schedule to schedule actions across the organization such as learning activities and recurring tasks.

## Before you begin

Role required: sn\_ohs\_im.agent

## About this task

The action scheduler uses the condition builder to create and assign actions to individuals based on specified conditions.

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the incident management icon \(![Incident Management icon.](../image/list-icon-hs.png)\).

3.  Select the **Action schedules** list and then **All**.

4.  Select **New**.

5.  On the form, fill in the fields.

    For information on field descriptions, see [Health and safety action schedule form](../reference/hs-health-safety-action-schedule-form.md).

6.  In the **Assign to** field, add conditions to auto-assign the generated actions.

    This criteria is based on the Health and Safety profile \[sn\_ohs\_im\_health\_and\_safety\_profile\] table. It automatically adds users with the Health and Safety profile to the action records generated for this schedule.

    1.  Select **Set conditions**.

    2.  In the condition builder, define conditions to choose people this action should be assigned to, and select **Set**.

        You can choose fields from the Health and Safety profile table and dot-walk fields when selecting a field in the condition builder. For example, the following image shows the conditions to select users in the Warehouse department in Dublin.

        ![Assign to conditions showing location and dot-walked condition for user's department name](../../hs-risk-management/image/hs-affected-people-conditions.png)

7.  Select **Save**.


## Result

-   The action schedule is saved in the Action schedule \[sn\_ohs\_im\_action\_schedule\] table.
-   The **Actions** tab appears for the action schedule.
-   In the **Actions** tab, the action scheduler creates and auto-assigns actions based on the condition builder. An action schedule might generate multiple actions for people over time.
-   The created actions appear in the assigned user's **My Tasks** list on both the Employee Center and the Now Mobile app. From either location, the user can respond to the action and update its status. For information on action form fields, see [Health and Safety action form](../reference/hs-action-form.md).

**Parent Topic:**[Scheduling Health and Safety actions](../concept/scheduling-health-safety-actions.md)

