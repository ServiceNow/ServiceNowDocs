---
title: Create pre-allocated assets
description: Create a pre-allocated asset that physically exists, but isn’t yet a financial liability.Assets can be allocated from pre-allocated asset records, which creates new asset records and reduces the Quantity in the original pre-allocated asset record.You can split a pre-allocated asset to create a group that can be moved to a different stockroom.
locale: en-US
release: xanadu
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Asset Management, IT Service Management]
---

# Create pre-allocated assets

Create a pre-allocated asset that physically exists, but isn’t yet a financial liability.

## Before you begin

Role required: asset

## About this task

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Portfolios** &gt; **All Assets** and create a record \(see table for field descriptions\).

    **Note:** Category must have the **Allow pre-allocated** option selected.

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

Model category that controls whether an asset is linked to a CI.

</td></tr><tr><td>

Model

</td><td>

Product model of the asset.

</td></tr><tr><td>

Quantity

</td><td>

Number of items the asset represents.

</td></tr><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

State

</td><td>

State of the asset.

</td></tr><tr><td>

Stockroom

</td><td>

Stockroom of the asset. This field is only available if the State field is set to **In stock**.

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

The type of expenditure. Choose from the following:-   **Capex**: Capital expenditure is a one-time expenditure, where the value is realized over the years. For example, a photocopier.
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

Activities

</td></tr><tr><td>

Work Notes

</td><td>

Work notes related to the asset.

</td></tr></tbody>
</table>2.  Select **Submit**.


**Parent Topic:**[Asset Management](../concept/c_AssetManagement.md)

## Allocate a pre-allocated asset

Assets can be allocated from pre-allocated asset records, which creates new asset records and reduces the **Quantity** in the original pre-allocated asset record.

### Before you begin

Role required: asset

### About this task

Allocating an asset makes it a financial liability. After all pre-allocated assets have been allocated, the pre-allocated asset record is removed from the asset list.

### Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Portfolios** &gt; **All Assets**.

2.  Filter the **Substate** column to show only **Pre-allocated** assets.

3.  Select the reference icon in the row containing the asset to allocate.

4.  Select **Allocate** at the bottom of the form.

    **Note:** If the **glide.asset.create\_ci\_with\_ire** property is set to `true`, a form appears when you click **Allocate**. On the form, fill in the **Asset tag**, **Serial number**, and **Reserved for** fields, then click **OK**.


### Result

The system creates and navigates to a new asset record, which has the same model and parent information as the pre-allocated asset. The new asset has a **Quantity** of one, while the pre-allocated asset's **Quantity** is reduced by one.

## Split a pre-allocated asset

You can split a pre-allocated asset to create a group that can be moved to a different stockroom.

### Before you begin

Role required: asset

### About this task

For example, a group of 100 pre-allocated computers is in Stockroom A. Split the group into two groups of 50 and move one group to Stockroom B. Allocate the computers from the two different stockrooms.

### Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Portfolios** &gt; **All Assets**.

2.  Filter the **Substate** column to show only **Pre-allocated** assets.

3.  Select the reference icon in the row containing the asset to split.

4.  Select **Split**.

5.  Enter a **Quantity to Split** and select **OK**.

    The pre-allocated asset is split into two groups and the **Quantity** field on each record indicates the number in each group.


