---
title: Publish a custom activity
description: When a user creates a custom activity and saves or submits it, that activity appears in the Custom and Packs tabs of the designer palette, but is visible only to the user who created it.Problems can arise if an activity version is checked out by a user and not checked back in. An activity in this state cannot be checked out for update.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Orchestration activity designer, Classic Orchestration, Workflow Data Fabric]
---

# Publish a custom activity

When a user creates a custom activity and saves or submits it, that activity appears in the **Custom** and **Packs** tabs of the designer palette, but is visible only to the user who created it.

## Before you begin

Roles required: admin, activity\_admin, activity\_creator

## Procedure

1.  When you finish configuring the activity, click **Publish**.

    This makes the activity accessible to other users on the instance with the workflow\_admin or activity\_creator role. Published activities are available for upload to the ServiceNow Store, can be added to workflows, and can be edited by any user with the proper roles.

2.  To edit a published activity, click **Checkout**.

    When an activity is checked out by a user, only that user can modify it. The fields of a checked out activity are read-only for all other users.

3.  When you are finished editing the checked out activity, publish it again.

    The system adds a new version of this activity to the **Custom** tab in the Workflow Editor palette.

    **Note:** Activities you create and publish are visible in the **Packs** tab only if they were created in the current application scope.


**Parent Topic:**[Orchestration activity designer](../concept/c_WorkflowActivityDesigner.md)

## Return a locked activity to a published state

Problems can arise if an activity version is checked out by a user and not checked back in. An activity in this state cannot be checked out for update.

### Before you begin

Role required: admin, activity\_admin, activity\_creator

### About this task

An administrator can return a locked activity to a published state.

### Procedure

1.  Open the Workflow Editor.

2.  From the **Custom** tab, open the activity that is locked.

3.  Click the menu icon in the title bar and select **Versions** from the context menu.

    A list of all the versions of that activity appears. The locked version displays the user who checked it out.

    ![The version history displays information about who checked out the activity](../image/CustomActivityVersions.png)

4.  Select the checked out version.

    The system opens the record in the activity designer.

5.  Click the menu icon again and select **Force Checkout** from the context menu.

    The activity fields become editable.

6.  Click **Publish**.

    The activity becomes available to users with the appropriate roles.


