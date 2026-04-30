---
title: Complete the shipment for a moving enterprise asset
description: Perform all tasks that are required to ship an enterprise asset. You must perform these tasks if you set the Move type field to Ship in an enterprise move line.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Completing an enterprise asset move order, Managing enterprise asset move orders, Managing enterprise assets and models, Enterprise Asset Management, IT Asset Management]
---

# Complete the shipment for a moving enterprise asset

Perform all tasks that are required to ship an enterprise asset. You must perform these tasks if you set the **Move type** field to **Ship** in an enterprise move line.

## Before you begin

Before you can proceed with the shipment, you must complete the Prepare task for the enterprise asset. See [Complete the Prepare task for a moving enterprise asset](complete-prepare-task-moving-enterprise-asset.md) for detailed instructions.

Role required: sn\_eam.enterprise\_asset\_manager, sn\_eam.enterprise\_admin, or enterprise\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, navigate to **Asset operations** &gt; **Moves** &gt; **Move orders**.

2.  From the list of available move orders, select the move order that you want to complete.

    The move order record opens.

3.  On the move order record, select the **Enterprise move lines** tab.

4.  From the list of available enterprise move lines, select the enterprise move line for the enterprise asset that you want to move.

    The enterprise move line record opens.

5.  Complete and close the Ship task for the enterprise move line.

    To successfully complete and close this task, the enterprise asset must be shipped to the target location.

    1.  On the **Enterprise move tasks** tab, select the task number for the **Ship** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the enterprise move line record header.

        The Ship task opens.

    2.  On the **Details** tab of the Ship task, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Enterprise move task|
        |Assignment group|Group that the task is assigned to. This field populates automatically based on the group that the entire move order is assigned to.|
        |Assigned to|User who the task is assigned to. This field populates automatically based on the user who the entire move order is assigned to.|
        |Scheduled date|Date and time at which the task is scheduled to be completed.|
        |Priority|Priority of the task.|
        |Shipment details|
        |Shipping carrier|Shipping carrier through which the enterprise asset was shipped.|
        |Ship date|Date on which the enterprise asset was shipped.|
        |Tracking number|Tracking number that enables you to track the status and location of the shipment.|
        |Notes|
        |Short description|Brief description of the task.|
        |Description|Detailed description of the task.|
        |Work notes|Notes about the task that are visible to all users within your organization.|

    3.  Select **Close Task**.

    The Ship task is automatically updated with a state of Closed Complete. The Enterprise Asset Management application then automatically generates a corresponding Receive task for the enterprise move line.

6.  Complete and close the Receive task for the enterprise move line.

    To successfully complete and close this task, the enterprise asset must be received at the target location.

    1.  On the **Enterprise move tasks** tab, select the task number for the **Receive** task.

        Alternatively, select the task number that is displayed in the **Current task** field of the enterprise move line record header.

        The Receive task opens.

    2.  On the **Details** tab of the Receive task, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Enterprise move task|
        |Assignment group|Group that the task is assigned to. This field populates automatically based on the group that the entire move order is assigned to.|
        |Assigned to|User who the task is assigned to. This field populates automatically based on the user who the entire move order is assigned to.|
        |Scheduled date|Date and time at which the task is scheduled to be completed.|
        |Priority|Priority of the task.|
        |Notes|
        |Short description|Brief description of the task.|
        |Description|Detailed description of the task.|
        |Work notes|Notes about the task that are visible to all users within your organization.|

    3.  Select **Close Task**.

    The Receive task is automatically updated with a state of Closed Complete.


## Result

The enterprise move line is automatically updated with a status of Completed.

## What to do next

Move all remaining enterprise assets that are included in the move order. After all corresponding enterprise move lines reach a status of Completed, the move order is complete.

**Parent Topic:**[Completing an enterprise asset move order](../concept/completing-enterprise-asset-move-order.md)

