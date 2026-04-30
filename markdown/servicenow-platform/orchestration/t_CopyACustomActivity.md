---
title: Copy a custom activity
description: You can copy activities for reuse from the Custom tab in the global scope.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Orchestration activity designer, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Copy a custom activity

You can copy activities for reuse from the **Custom** tab in the global scope.

## Before you begin

Role required: admin, activity\_admin, activity\_creator

## About this task

**Note:** You cannot copy an activity in a private scope.

## Procedure

1.  To reuse an activity in the global scope, expand the parent category to display the activities.

2.  Right-click the activity you want to copy and select one of these options:

    -   Copy into global scope as new activity: Copies the activity with the new name you provide, uses the same version number as the original activity, and moves it to the global scope in the **Custom** tab.

        ![Naming an activity copy](../image/CopyCustomActivity.png "Naming an activity copy")

    -   Copy into global scope as new version: Copies the activity using the same name, increments the version number, and moves it to the global scope in the **Custom** tab. The system automatically adds the parent category to the **Custom** tab if it does not already exist. This action will overwrite another activity with the same name and version number.

        ![Creating a new activity version](../image/NewVersionCustomActivity.png "Creating a new activity version")

    **Note:** If the activity is in any other scope but global, the system displays this message: `Cannot copy privately scoped activity`.


**Parent Topic:**[Orchestration activity designer](../concept/c_WorkflowActivityDesigner.md)

