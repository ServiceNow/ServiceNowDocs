---
title: Create consumable assets
description: Create a consumable to track an asset as a group of the same model.
locale: en-US
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Consumables life cycle, Using Asset Management, Asset Management, IT Asset Management]
---

# Create consumable assets

Create a consumable to track an asset as a group of the same model.

## Before you begin

Role required: asset

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Portfolios** &gt; **Consumables** and create a new record \(see table for field descriptions\).

<table id="table_ulx_gy5_ngb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the asset.

</td></tr><tr><td>

Model category

</td><td>

Model category that controls if an asset is linked to a CI.

</td></tr><tr><td>

Model

</td><td>

Product model of the asset.

</td></tr><tr><td>

Quantity

</td><td>

Amount of items the asset represents.

</td></tr><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

State

</td><td>

State of the asset.

</td></tr><tr><td>

Parent

</td><td>

Parent asset. When a parent asset is defined, the **Assignment** and **State** fields of the child asset are automatically populated based on the **Assignment** and **State** fields of the parent asset and are read-only.

</td></tr><tr><td>

Class

</td><td>

Type of asset. The system automatically sets the **Class** to **Consumable**.

</td></tr><tr><td>

Expenditure type

</td><td>

The type of expenditure. Choose from the following options:-   **Capex**: Capital expenditure is a one-time expenditure, where the value is realized over the years. For example, a photocopier.
-   **Opex**: Operational expenditure is an on-going expenditure. For example, toners for the photocopier.


</td></tr><tr><td>

Substate

</td><td>

Substate of the asset.

</td></tr><tr><td>

Location

</td><td>

Location of the asset.

</td></tr><tr><td>

Cost

</td><td>

Price that the asset was purchased for.

</td></tr><tr><td>

Cost Center

</td><td>

Cost center financially responsible for the asset.

</td></tr><tr><td class="sub-head" colspan="2">

Disposal

</td></tr><tr><td>

Disposal order number

</td><td>

A unique number assigned to the asset disposal order.

 **Note:** This field appears only if you have installed Hardware Asset Management from the ServiceNow Store.

</td></tr><tr><td>

Disposal vendor

</td><td>

The vendor assigned to carry out the asset disposal order.

 **Note:** This field appears only if you have installed Hardware Asset Management from the ServiceNow Store.

</td></tr><tr><td>

Vendor disposal order ID

</td><td>

Order number assigned by the vendor assigned to carry out the asset disposal order.

 **Note:** This field appears only if you have installed Hardware Asset Management from the ServiceNow Store.

</td></tr><tr><td>

Disposal date

</td><td>

The date when the asset disposal order process is completed.

 **Note:** This field appears only if you have installed Hardware Asset Management from the ServiceNow Store.

</td></tr><tr><td>

Disposal reason

</td><td>

Text explaining why the asset is being retired.

</td></tr><tr><td>

Beneficiary

</td><td>

Organization that receives the asset when it is retired.

</td></tr><tr><td>

Resale price

</td><td>

Value of the asset when it is retired. For example, if the asset is donated, the value used when reporting taxes.

</td></tr><tr><td>

Scheduled retirement

</td><td>

Scheduled date on which the asset is retired.

</td></tr><tr><td>

Retired date

</td><td>

Actual date on which the asset was retired.

</td></tr><tr><td class="sub-head" colspan="2">

Activities

</td></tr><tr><td>

Work Notes

</td><td>

Work notes related to the asset.

</td></tr></tbody>
</table>2.  Click **Submit**.


**Parent Topic:**[Consumables life cycle](../concept/c_FollowLifeCycleConsumbl.md)

