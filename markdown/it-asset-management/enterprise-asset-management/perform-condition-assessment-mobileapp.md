---
title: Perform condition evaluation from the Mobile Agent application
description: Perform condition evaluation to calculate the score and result of the condition attributes from the Mobile Agent application.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Perform condition evaluation from the Mobile Agent application

Perform condition evaluation to calculate the score and result of the condition attributes from the Mobile Agent application.

## Before you begin

An asset condition work order task for an asset must be created and assigned to the technician.

Role required: sn\_eam.asset\_technician

## About this task

**Note:** Starting with Enterprise Asset Management version 10.0, work order task can be associated with multiple assets, either through an asset group or by assets added to the Affected assets list. When a work order task has multiple assets, the technician must assess the condition of each asset within the same work order task. After completing all condition evaluations, the condition results are recorded for each asset and are available for the enterprise asset manager to review.

These steps detail the process of performing the condition evaluation from a mobile application. Condition evaluations can also be performed from the Enterprise Asset Workspace. For details, see [Perform condition evaluation from the Enterprise Asset Workspace](perform-condition-assessment-webui.md).

## Procedure

1.  From your mobile device, launch the Mobile Agent application.

2.  On the navigation bar at the bottom of the screen, tap the **My Tasks** tab.

    The home screen opens with the list of tasks assigned to you.

3.  Tap the work order task for which you want to take action.

4.  On the **Details** tab, tap **Start Work**.

5.  Tap the **View asset conditions** tab to see all the condition lines associated with the asset.

    In Enterprise Asset Management version 10.0 and later, the **Assessment lines** screen opens and shows condition lines for all assets in the Affected assets list. A condition evaluation is created for each asset, and you must complete all condition lines to complete and close the task. The asset associated with the condition line is shown.

    -   The **Open** tab displays all condition lines associated with the assets that are not yet completed.
    -   The **Completed** tab displays all completed asset condition lines.
    Initially all the condition lines are in an open state and each condition line is associated with a template.

6.  Tap a condition line record.

    The mobile UI of the condition evaluation that is associated with the corresponding condition line opens.

7.  Tap **Next** and answer the questions.

8.  Tap **Submit** once you have answered all the questions.

    The score gets calculated and populated on the condition line record that moves to the completed state, and a pass or fail determination is made based on the scores. If the pass and fail criteria wasn’t defined on a condition line, then the score displays as NA.

9.  In Enterprise Asset Management version 10.0 and later, repeat steps 6 through 8 for each condition line for all assets in the work order task.

    After all condition lines are completed, the **Close** button appears on the work order task.

10. Tap **Close** to close the work order task.


