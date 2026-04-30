---
title: Schedule condition evaluations for enterprise models or assets
description: Schedule a condition evaluation by creating a work order for it.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-03-31"
reading_time_minutes: 1
breadcrumb: [Managing work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Schedule condition evaluations for enterprise models or assets

Schedule a condition evaluation by creating a work order for it.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## Procedure

1.  Navigate to **All** &gt; **Enterprise Asset Workspace** &gt; **Work management**.

2.  On the **Work orders** tab, select **New**.

3.  Select **Asset condition work order** in the **Template** field.

    For more details on creating a work order, see [Create a work order for an enterprise asset](create-eam-work-order.md).

4.  After you have entered the details in the work order, select **Save**.

    The work order is created in the draft state.

5.  Select **Ready to Work**.

    A work order task gets created for the work order in the **Work Order Tasks** tab.

    Additionally, a service event gets created along with condition lines. Depending on the number of templates linked to the asset, an equivalent number of assessment lines are generated. Only a single service event gets created per asset.

6.  Open the work order task and assign it to an enterprise technician.

    A service event gets created along with condition lines. Depending on the number of attributes created on the asset, an equivalent number of condition lines are generated. Only a single service event gets created per work order task. The technician must log in to begin work on the work order task.


