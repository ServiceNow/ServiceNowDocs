---
title: Close transfer order line tasks in Enterprise Asset Workspace
description: Close transfer order line tasks to move transfer order lines from one stage to the other.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a transfer order in Enterprise Asset Workspace, Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Close transfer order line tasks in Enterprise Asset Workspace

Close transfer order line tasks to move transfer order lines from one stage to the other.

## Before you begin

Role required: admin

## About this task

When you create a transfer order line, based on the model category specified in the asset, a transfer order line task is automatically created. Default template tasks are available with the Enterprise Asset Management application. The template tasks are based on model categories. Default template tasks cannot be deleted or modified.

When you create a transfer order line and select an asset, that asset corresponds to a model category. If a template task exists for that model category then that template task is added to the transfer order line as a transfer order line task.

Closing a transfer order line task completes the task and creates the next task in the process. For example, once you close the **Requested** task, the state for this task appears as Closed Complete and a new task is opened for the next stage, **Shipment Preparation**. This process continues till you close all the tasks required for completing the transfer order line. As you close a task and as a task moves from one stage to the next, the asset gets automatically updated too. For example, when the transfer order line moves from **Requested** to **Shipment Preparation**, the asset's status also moves from available to reserved.

## Procedure

1.  Navigate to a transfer order line record in the Enterprise Asset Workspace.

2.  Select the **Transfer Order Line Tasks** tab.

    The following are the transfer order line tasks:

    -   Requested:
    -   Shipment Preparation
    -   In Transit
    -   Received
    -   Delivered
3.  Open the Requested task.

4.  Select **Close Task** to close this task.

    As you close the Requested task, the **Shipment Preparation** task which is the next task in the process is created.

5.  Continue to open the next task in the process, till you close the **Delivered** task.

    Once you close the Delivered task, the transfer order line is completed.


**Parent Topic:**[Create a transfer order in Enterprise Asset Workspace](create-eam-transferorder.md)

