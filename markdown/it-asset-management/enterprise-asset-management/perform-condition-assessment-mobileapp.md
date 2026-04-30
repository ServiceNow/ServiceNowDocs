---
title: Perform condition evaluation from a mobile application
description: Perform condition evaluation to calculate the score and result of the condition attributes from a mobile application.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-04-01"
reading_time_minutes: 1
breadcrumb: [Managing work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Perform condition evaluation from a mobile application

Perform condition evaluation to calculate the score and result of the condition attributes from a mobile application.

## Before you begin

Role required: sn\_eam.asset\_technician

## About this task

Before proceeding with this task, ensure that an asset condition work order task for an asset has been created and assigned to the technician.

These steps detail the process of performing the condition evaluation from a mobile application. Condition evaluations can also be performed from the Enterprise Asset Workspace. For details, see [Perform condition evaluation from the Enterprise Asset Workspace](perform-condition-assessment-webui.md).

## Procedure

1.  From your mobile device, launch the Mobile Agent application.

2.  On the navigation bar at the bottom of the screen, tap the **My Tasks** tab.

    The home screen opens with the list of tasks assigned to you.

3.  Tap the work order task for which you want to take action.

4.  Tap the **View asset conditions** tab to see all the condition lines associated with the asset.

    Initially all the condition lines are in an open state and each condition line is associated with a template.

5.  Tap a condition line record.

    The mobile UI of the condition evaluation that is associated with the corresponding condition line opens.

6.  Tap **Next** and answer the questions.

7.  Tap **Submit** once you have answered all the questions.

    The score gets calculated and populated on the condition line record that moves to the completed state, and a pass or fail determination is made based on the scores. If the pass and fail criteria wasn’t defined on a condition line, then the score displays as NA.

    After all the condition lines are completed, the **Close** button appears in the Asset condition work task screen.

8.  Tap **Close** to close the work order task.


**Parent Topic:**[Managing work orders for your enterprise assets](../concept/create-manage-wo-enterprise-assets.md)

