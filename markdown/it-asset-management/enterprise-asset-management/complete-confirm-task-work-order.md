---
title: Complete and close the Confirm asset task for a serialized enterprise asset
description: If your work order is associated with a serialized enterprise asset, complete and close the Confirm asset task for that asset.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing work for your enterprise assets, Managing work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Complete and close the Confirm asset task for a serialized enterprise asset

If your work order is associated with a serialized enterprise asset, complete and close the Confirm asset task for that asset.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## About this task

Before an agent can perform work on an enterprise asset, it must be picked up from its designated stockroom. If you want an agent to perform work on a serialized enterprise asset, you must first confirm which asset needs to be picked up by using the Confirm asset task. For all other enterprise asset types, skip the Confirm asset task and proceed directly to the [Pickup task](complete-pickup-task-work-order.md).

## Procedure

1.  From the Enterprise Asset Workspace, open the Enterprise asset estate view.

2.  On the **Asset tasks** tab, select the **Confirm** task for the serialized enterprise asset that is associated with your work order.

    The Confirm task opens.

3.  On the **Details** tab of the Confirm task, modify the fields as needed.

    |Field|Description|
    |-----|-----------|
    |Asset|Serialized enterprise asset that is associated with your work order.|
    |Model|Model of the serialized enterprise asset.|
    |State|State of the Confirm task.|
    |Stockroom|Stockroom that the serialized enterprise asset is located in.|
    |Short description|Brief description of the Confirm task.|
    |Description|Detailed description of the Confirm task.|

4.  Select **Close Task**.


## Result

The state of the Confirm task changes from Open to Closed Complete. The Enterprise Asset Management application then generates a subsequent Pick Up task for the enterprise asset.

## What to do next

The agent who is assigned to the associated work order must complete and close the Pick Up task.

**Parent Topic:**[Managing work for your enterprise assets](../concept/managing-work-enterprise-assets.md)

