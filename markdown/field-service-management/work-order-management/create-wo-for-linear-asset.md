---
title: Create work order for a linear asset using a map
description: Create a work order for tracking and managing work on a linear asset and its corresponding segments.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Assign work orders for linear assets in Field Service Management, Manage work orders, Prepare work orders, Use, Field Service Management]
---

# Create work order for a linear asset using a map

Create a work order for tracking and managing work on a linear asset and its corresponding segments.

## Before you begin

Role required: wm\_initiator and wm\_dispatcher

## About this task

Creation of work order for a linear asset enables you to leverage the linear asset's geometry on the service location map and choose the appropriate start and end locations or pinpoint the work location accurately.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **CSM/FSM Configurable Workspace.**.

2.  Select the List icon \(![List icon.](../image/ListIcon.png)\).

3.  Select **Work Orders** &gt; **Created by me** and then select **New**.

4.  On the form, fill in the **Company**, **Caller**, and **Affected CI** fields.

5.  Define the location for the affected linear assets.

    1.  Search for the affected linear assets segments on the map by selecting the Select an asset icon \(![Select an asset icon.](../image/EditWidgetButton.png)\) in the **Asset** field.

    2.  Display linear assets only of a specified type on the map by selecting an overlay.

        For example, to display only streets and roads, you could select Roadways.

        By default, the map loads your current service location, which you need to change to the work location for the linear asset.

    3.  Enter the work location in the **Search** address bar.

        When the map displays the desired area, you can use the zoom controls to zoom in.

        The linear asset segments are represented on the map with a solid green line.

    4.  Define the precise work location for a linear asset by selecting either multiple segments or a single point location.

        -   To specify the segment that requires work by selecting the start and end locations directly on the linear asset itself, select **Line** and drag the marker.

            When a segment is selected, the **Segments** field is automatically populated with either a single or multiple segment values depending on the number of segments selected. Additionally, the **Start location** and **End location** fields are populated with the appropriate physical location values for the chosen segment.

        -   To select a specific point location along the linear asset or choose a separate location that is relevant to the work being performed, select **Point**.

            When a specific location is pinpointed along the linear asset, the **Location** field is automatically populated with the selected physical location values for that particular point location.

    5.  Select **Submit**.

        The Linear Work option appears and enabled by default. The start and end locations are also populated automatically based on the length of the linear asset segment.

6.  Select **Save**.

    The form closes and you are automatically redirected to the newly created work order record.

7.  View the total number of affected segments selected by selecting **Affected Products**.


## What to do next

Create a work order task for the new work order. For more information, see [Qualify a work order](../../planning-and-policy/task/t_QualifyATask.md). You can create multiple work order tasks to track and manage an individual task for your linear asset work order.

