---
title: Consumables life cycle
description: Consumables are assets that are not tracked individually, but as a group of the same model.Consumables are tracked as a group of the same model, but you can view individual consumables in the consumable model record.Create a consumable to track an asset as a group of the same model.To consume consumable assets, they must have a state of In Stock and a substate of Available.
locale: en-US
release: xanadu
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Asset Management, IT Service Management]
---

# Consumables life cycle

Consumables are assets that are not tracked individually, but as a group of the same model.

The group of consumables has one or more of the following traits.

-   Same location
-   Same state
-   Consumed by the same asset, typically as accessories or parts

Some common consumable assets include mouse devices, computer keyboards, and pencils. The base ServiceNow system includes the **Consumable** model category. The first step in working with models is to create a model within the model category for an individual consumable asset. Items such as monitors, keyboards, and mouse devices are often tracked as consumables. Consumables cannot be pre-allocated.

Consumable assets are stored in the Consumable \[alm\_consumable\] table. Consumables follow a slightly different life cycle from other assets.

## Stages of consumables

The consumable lifecycle stages are as follows.

-   On order
-   In stock
-   In transit
-   Consumed
-   In maintenance
-   Retired
-   Missing

**Parent Topic:**[Asset Management](c_AssetManagement.md)

## View consumable assets

Consumables are tracked as a group of the same model, but you can view individual consumables in the consumable model record.

### Before you begin

Role required: model\_manager

### Procedure

1.  Navigate to **All** &gt; **Product Catalog** &gt; **Product Model** &gt; **Consumable Models**.

2.  Open a consumable model record.

3.  View individual consumables in the **Consumables** related list.


## Create consumable assets

Create a consumable to track an asset as a group of the same model.

### Before you begin

Role required: asset

### Procedure

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


## Consume consumable assets

To consume consumable assets, they must have a state of **In Stock** and a substate of **Available**.

### Before you begin

Role required: asset

### Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Portfolios** &gt; **Consumables**.

2.  Click the **Display Name** of a consumable asset with a state of **In Stock** and a substate of **Available**.

3.  Click **Consume**.

4.  Enter the **Quantity** to consume.

5.  In **Asset**, click the lookup icon and select the asset associated with the consumable.

    For example, a mouse tracked as a consumable asset can be associated with a non-consumable asset such as a computer.

6.  In **User**, click the lookup icon and select a user associated with the consumable.

7.  Click **OK**.

    On the **Consumable** form, the **Quantity** field shows the reduced number. The Consumables list contains two records for the consumable in the specific stockroom: one with a state and substate of **In Stock** and **Available** \(if you did not consume the entire quantity\), and one with a state of **Consumed**. If a consumable is not in the process of being transferred to a different stockroom and information in the data record is the same, similar records merge automatically. After a consumable is consumed, the record remains in the system for reporting purposes.


