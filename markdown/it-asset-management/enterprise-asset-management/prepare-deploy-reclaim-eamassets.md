---
title: Prepare, deploy, and reclaim loaner assets in Enterprise Asset Workspace
description: Select and prepare the loaner asset or consumable for deployment and reclamation by using loaner asset tasks. Deploy the loaner asset or consumable for a specific period of time, and reclaim it on the return date.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Request a loaner asset in Enterprise Asset Workspace, Create and manage enterprise asset inventory, Manage enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Prepare, deploy, and reclaim loaner assets in Enterprise Asset Workspace

Select and prepare the loaner asset or consumable for deployment and reclamation by using loaner asset tasks. Deploy the loaner asset or consumable for a specific period of time, and reclaim it on the return date.

## Before you begin

To use an asset as a loaner asset or consumable, go to the asset record and set the **Asset function** field to **Loaner**. These assets are reserved for use as loaner assets. You cannot use an asset that has the Asset function field set to anything other than **Loaner**.

The Loaner asset orders tab in the **Inventory** view shows all the loaner orders the asset has served in the past and at present. In case of consumables, if the consumable is not in a stockroom, it shows only the current loaner asset order that it's serving at present.

Role required: inventory\_user

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Inventory** &gt; **Loaner Asset Orders**.

2.  Open an enterprise loaner asset order.

3.  Select the **Loaner Asset tasks** tab.

4.  Select the **Prepare** task and fill in the details.

    |Fields|Descriptions|
    |------|------------|
    |Asset|Asset that is used to fulfill the loaner asset request.|
    |State|State of the task.|
    |Assigned to|Person who is assigned the task of fulfilling the Deploy task.|

5.  After entering the necessary details, select **Close Task** to close the Prepare task.

    After the Prepare task is completed, a Deploy task is created under the Loaner Asset Tasks related list. On the Asset record \[alm\_asset\] table, the following changes occur:

    -   The state of the loaner asset changes to In stock.
    -   The **Reserved for** field is automatically set to the name of the user who the loaner asset was requested for.
    -   The substate changes to Pending install.
6.  Open the Deploy task and fill in the details in the form.

    |Fields|Descriptions|
    |------|------------|
    |State|State of the task.|
    |Assigned to|Person who is assigned the task of fulfilling the Deploy task.|

7.  Select **Close Task** to close the Deploy task.

    On the Asset record \[alm\_asset\] table, the following changes occur:

    -   The state of the loaner asset changes to In use.
    -   The **Stock room** field changes to Null.
    -   The **Assigned to** field is automatically set to the name of the user who the asset was requested for.
    -   If you requested the loaner asset for a third-party vendor, then the **Managed by** field is automatically set to the name of the user who the asset was requested for.
    In case of consumable, state changes to Consumed.

    Two days before the return date, the users who opened or requested the asset will receive an email notification about the reclaim. One day before the return date, a Reclaim task is created under the Loaner Asset Tasks tab.

8.  Open the Reclaim task.

9.  On the form, fill in the details.

    |Field|Description|
    |-----|-----------|
    |Stockroom|Stockroom where the returned asset will be stored. If you entered a stockroom different from where you received the loaner asset, then a warning message appears which says that the existing loaner orders from the initial stockroom might be affected.|
    |Returned on|Actual date when the asset was returned.|
    |State|State of the task.|
    |Assigned to|Person who is assigned the task of fulfilling the Reclaim task.|
    |Asset returned|Option to mark the asset as returned. The Reclaim task cannot be closed if the asset is not returned.|
    |Asset functional|Functional status of the loaner asset after it's reclaimed.|

    If the asset is not functional, the state of the asset changes to In stock and substate changes to Pending repair.

10. To close the Reclaim task, select **Close Task**.

11. If a user returns the asset before the return date, do the following:

    1.  Select **Reclaim**.

    2.  On the Reclaim Asset form, update the fields.

    3.  Close the Reclaim task.

    On the Asset record \[alm\_asset\] table, the following changes occur:

    -   The state of the loaner asset changes to In stock.
    -   The substate changes to Available.
    -   The **Stockroom** field is automatically set to the value that was selected on the Reclaim task form.
    -   If the asset is assigned to a future loaner order, the substate changes to Reserved and reflects the details of the loaner order.

**Parent Topic:**[Request a loaner asset in Enterprise Asset Workspace](request-eam-assetloaner-request.md)

