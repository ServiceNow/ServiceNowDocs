---
title: Create an Industrial Guided Task from Recommended Actions
description: Create an Industrial Guided Task \(IGT\) based on the Recommended Actions for a deviation.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Industrial Guided Tasks, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Create an Industrial Guided Task from Recommended Actions

Create an Industrial Guided Task \(IGT\) based on the Recommended Actions for a deviation.

## Before you begin

Make sure that you:

-   Published a standard that should appear in Recommendations
-   Enabled Allow ad-hoc request
-   Set a deviation to active

Role required: both sn\_icw.deviation\_user and sn\_icw\_igt.user

## Procedure

1.  Navigate to **Lists** &gt; **Deviations**.

2.  Open the deviation that you need.

    The standard appears in the **Suggestions** tab of the **Recommendations** sidebar if any of the following conditions are met:

    -   The functional location of the standard contains the functional location of the deviation.
    -   The equipment model of the standard contains the equipment model ID of the deviation.
    -   The equipment in the standard matches the equipment in the deviation.
    -   The failure mode of the standard contains the failure from the deviation.
    -   The material model of the standard contains active material from the deviation.
3.  On the card for the recommended standard, create a task from a recommended standard by selecting **Create task**.

4.  Remove a recommendation from the sidebar by selecting **Dismiss**.

    The card disappears but the action is saved in actions history.


## Result

A new standard task is created and displayed in the list of tasks. It contains all the information from both the standard and the deviation.

**Parent Topic:**[Using Industrial Guided Tasks](../concept/using-industrial-guided-tasks.md)

