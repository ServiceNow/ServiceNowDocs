---
title: Create an asset resale flow
description: Create an asset resale flow for an asset to be resold in order to reduce waste and save cost.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Service Catalog for Enterprise Asset Management requests and flows, Enterprise Asset Management, IT Asset Management]
---

# Create an asset resale flow

Create an asset resale flow for an asset to be resold in order to reduce waste and save cost.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## About this task

The asset vendor must confirm which assets can be resold and how much they are worth.

Only assets that are in a non-terminal state, which is any state in which the asset can transition into a different state, can be resold through a enterprise resale order. Each asset must also be associated with either an enterprise model or pallet model. You can add simple assets; multi-component assets, which include pre-assembled and user-assembled assets; and pallet assets with children to an enterprise resale order.

**Note:** If you are adding a pallet asset with children to a resale order, any changes that you make to the pallet asset are automatically applied to all child assets.

## Procedure

1.  Navigate to the **Service Catalog** &gt; **Enterprise Asset Lifecycle**.

2.  Select Enterprise Resale Order.

3.  On the form, fill in the fields.

4.  Add assets and submit the order.

    Once the asset resale request is submitted, you can fulfill the request by navigating to the Enterprise Asset Workspace.

5.  Navigate to **Inventory** &gt; **Resale orders**.

6.  Next go through each task.

7.  Select Verify Asset to select assets and verify them.

    Before completing the Verify Asset task, you can add or remove assets from the disposal order. You can also edit the quantity of consumables.

8.  Select Close task.

    The next task in the workflow, Schedule pickup, is automatically created and appears in the **Enterprise Asset Resale Tasks** tab

9.  Select Schedule Pickup to specify when the asset can be picked up from the stockroom as well as the vendor details

10. Select Close task.

    The stage changes to in transit and the Asset departure task is created.

11. Select the Asset departure task and select each asset departing for resale as well as pickup contact details,

12. Select Close task.

    The stage changes to confirmation and the Vendor confirmation task is created.

13. Select the Vendor confirmation task once the vendor confirms that the assets were received.

14. Select Close task.

    The stage changes to documentation and a Resale Documentation task is created.


