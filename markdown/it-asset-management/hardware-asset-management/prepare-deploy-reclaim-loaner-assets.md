---
title: Prepare, deploy, and reclaim loaner assets
description: Select and prepare the loaner asset or consumable for deployment and reclamation by using loaner asset tasks. Deploy the loaner asset or consumable for a specific period, and reclaim it on the return date.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Manage loaner assets, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Prepare, deploy, and reclaim loaner assets

Select and prepare the loaner asset or consumable for deployment and reclamation by using loaner asset tasks. Deploy the loaner asset or consumable for a specific period, and reclaim it on the return date.

## Before you begin

To use an asset as a loaner asset or consumable, go to the asset record and set the **Asset function** field to **Loaner**. These assets are reserved for use as loaner assets. You can’t use an asset that has the **Asset function** field set to anything other than **Loaner**. Only hardware, bundle, and consumables can be used as Loaner assets.

The Loaner Asset Orders related list in the Asset form shows all the loaner orders that the asset has served in the past and at present. When the consumable isn’t in a stockroom, it shows only the current loaner asset order that it's serving at present.

Role required: inventory\_user

## About this task

Use the Loaner Asset Orders module to view and complete the loaner asset orders that were requested by the users.

The Hardware Asset dashboard gives a consolidated view of all the loaner asset orders that are in the New, Deployed, or Return Overdue states. For details, see [Hardware Asset dashboard](../../../use/dashboards/application-content-packs/hardware-asset-content-pack.md#).

**Note:**

There are readily available decision tables that you can use to customize the Loaner Asset Request Flow. For more details, see [Hardware Asset Management flow customization](../concept/readily-available-dec-tables-ham.md).

## Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Loaner** &gt; **Loaner Asset Orders**.

2.  Open a loaner asset order record.

3.  Under the Loaner Asset Tasks related list, open the Prepare task.

4.  On the form, fill in the fields.

<table id="table_usp_kfv_gnb"><thead><tr><th>

Fields

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Asset

</td><td>

Asset that is used to fulfill the loaner asset request.When the Location field value of the Loaner Asset Request form is a service location of multiple stockrooms, the Asset field shows the list of loaner assets that are available in all those stockrooms in addition to the loaner assets available in the stockroom of that location. For more details on service locations, see [Associate a stockroom with service locations](associate-stockroom-with-service-locations.md).

**Note:** The stockroom that is available at the specified location is preferred for fulfilling the loaner asset request. The stockrooms that support the specified location are considered only when there isn't any stockroom in that location.

</td></tr><tr><td>

State

</td><td>

State of the task.

</td></tr><tr><td>

Assigned to

</td><td>

Person who is assigned the task of fulfilling the Deploy task.

</td></tr></tbody>
</table>5.  After you physically prepare the hardware asset for deployment, select **Close Task** to close the Prepare task.

    After the Prepare task is completed, a Deploy task is created under the Loaner Asset Tasks related list. On the Asset record \[alm\_asset\] table, the following changes happen:

    -   The state of the loaner asset changes to In stock.
    -   The **Reserved for** field is automatically set to the name of the user who the loaner asset was requested for.
    -   The substate changes to Pending install.
6.  Open the Deploy task.

7.  On the form, fill in the fields.

    |Fields|Descriptions|
    |------|------------|
    |State|State of the task.|
    |Assigned to|Person who is assigned the task of fulfilling the Deploy task.|

8.  Deploy the hardware asset.

9.  Set the **State** field to **Closed Complete**.

10. To close the Deploy task, select **Close Task**.

    On the Asset record \[alm\_asset\] table, the following changes happen:

    -   The state of the loaner asset changes to In use.
    -   The **Stock room** field changes to Null.
    -   The **Assigned to** field is automatically set to the name of the user who the asset was requested for.
    -   If you requested the loaner asset for a third-party vendor, then the **Managed by** field is automatically set to the name of the user who the asset was requested for.
    For a consumable, the state changes to Consumed.

    Two days before the return date, the users who requested the asset will receive an email notification about the reclaim. One day before the return date, a Reclaim task is created under the Loaner Asset Tasks related list.

11. Open the Reclaim task.

12. On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Stockroom|Stockroom where the returned asset is stored. If you entered a stockroom different from where you received the loaner asset, then a warning message appears which says that the existing loaner orders from the initial stockroom might be affected.|
    |Returned on|Actual date when the asset was returned.|
    |State|State of the task.|
    |Assigned to|Person who is assigned the task of fulfilling the Reclaim task.|
    |Asset returned|Option to mark the asset as returned. The Reclaim task can’t be closed if the asset isn’t returned.|
    |Asset functional|Functional status of the loaner asset after it's reclaimed.|

    If the asset isn’t functional, the state of the asset changes to In stock and the substate changes to Pending repair.

13. To close the Reclaim task, select **Close Task**.

14. If a user returns the asset before the return date, do the following:

    1.  Select **Reclaim**.

    2.  On the Reclaim Asset form, update the fields.

    3.  Close the Reclaim task.

    On the Asset record \[alm\_asset\] table, the following changes occur:

    -   The state of the loaner asset changes to In stock.
    -   The substate changes to Available.
    -   The **Stockroom** field is automatically set to the value that was selected on the Reclaim task form.
    -   If the asset is assigned to a future loaner order, the substate changes to Reserved and reflects the details of the loaner order.

**Parent Topic:**[Manage loaner assets](manage-loaner-asset.md)

