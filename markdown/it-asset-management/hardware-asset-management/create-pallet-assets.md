---
title: Create pallet assets
description: Create a pallet asset from the Asset estate view in the Hardware Asset Workspace to track and manage assets in the inventory.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Manage your inventory through pallet assets, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Create pallet assets

Create a pallet asset from the Asset estate view in the Hardware Asset Workspace to track and manage assets in the inventory.

## Before you begin

You must create a model for a pallet asset. For more information, see [Models](https://www.servicenow.com/docs/access?context=c_Models&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

Role required: asset

## About this task

While creating a pallet asset, only the Details, Disposal, Activities, and Audit sections of the asset form appear. Although audit-related fields are shown on the asset form, you can't conduct the audit of pallet assets. You can specify the aisle and space details to give the exact location of the pallet in a stockroom.

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Asset estate**.

2.  Select **New Asset**.

3.  In the dialog box, select **Pallet** as the asset type and then select **Create**.

4.  On the form, fill in the fields.

<table id="table_xn3_1tz_gvb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the pallet asset based on the values in the **Asset Tag** and **Model** fields set when the pallet asset is created. For example, the display name for a pallet with an Asset tag of PAL0000001 whose Model is 3Com Wooden pallet would be PAL0000001 - 3Com Wooden pallet.

</td></tr><tr><td>

Model category

</td><td>

The model grouping of the pallet asset. This field is read-only and is automatically set to Pallet.

</td></tr><tr><td>

Number

</td><td>

Unique, auto-generated number for the pallet asset.

</td></tr><tr><td>

Model

</td><td>

Product model of the pallet asset.

</td></tr><tr><td>

Quantity

</td><td>

Number of items the pallet asset represents. This field is automatically set to 1.

</td></tr><tr><td>

Asset tag

</td><td>

Alphanumeric tracking information from the tag attached to the pallet asset.

</td></tr><tr><td>

Pallet type

</td><td>

Type of pallet. The available values are:-   Pallet
-   Bin
-   Box
-   Container
-   other


</td></tr><tr><td>

State

</td><td>

Current state of the pallet asset. The available values are:-   In stock
-   In transit
-   Retired
-   Missing


</td></tr><tr><td>

Substate

</td><td>

Current substate of the asset, such as Available or Reserved. The values in the Substate list change based on what you select from the State list.

</td></tr><tr><td>

Stockroom

</td><td>

Name of the stockroom.

</td></tr><tr><td>

Reserved for

</td><td>

Name of the person for whom the pallet is reserved.

</td></tr><tr><td>

Aisle

</td><td>

Aisle details of the pallet within the stockroom. This field appears only when In stock or Build is selected from the **State** field.

</td></tr><tr><td>

Location

</td><td>

Physical location of the stockroom.

</td></tr><tr><td>

Space

</td><td>

Space details of the pallet within the aisle. This field appears only when In stock or Build is selected from the **State** field.

</td></tr><tr><td>

Parent

</td><td>

Parent asset of the pallet asset.

</td></tr><tr><td>

Comments

</td><td>

Optional additional information.

</td></tr></tbody>
</table><table id="table_srk_nxd_hvb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Disposal order number

</td><td>

This field is automatically set to the unique number assigned to the asset disposal order.**Note:** This field appears only if you have installed Hardware Asset Management from the ServiceNow Store.

</td></tr><tr><td>

Scheduled retirement

</td><td>

Scheduled date on which the asset retires.

</td></tr><tr><td>

Disposal vendor

</td><td>

The vendor assigned to carry out the asset disposal order.**Note:** This field appears only if you have installed Hardware Asset Management from the ServiceNow Store.

</td></tr><tr><td>

Retire date

</td><td>

Actual date on which the asset retires.

</td></tr><tr><td>

Vendor disposal order ID

</td><td>

Order number from the vendor assigned to carry out the asset disposal order.**Note:** This field appears only if you have installed Hardware Asset Management from the ServiceNow Store.

</td></tr><tr><td>

Refresh request line

</td><td>

Refresh request line number if the asset has been identified as an aged asset by the Hardware Asset Refresh flow.

</td></tr><tr><td>

Disposal date

</td><td>

Date when the asset disposal process is completed.**Note:** This field appears only if you have installed Hardware Asset Management from the ServiceNow Store.

</td></tr><tr><td>

Beneficiary

</td><td>

Organization that will receive the asset when the asset is retired.

</td></tr><tr><td>

Resale price

</td><td>

Value of the asset when it's retired. For example, if the asset is donated, the value used when reporting taxes.

</td></tr></tbody>
</table><table id="table_qlw_pd2_hvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Work notes

</td><td>

Any additional information about the asset.

  Work notes are updated automatically in the following situations:

-   Updates to **State**, **Substate**,or **Reserved for** fields of the asset record. Any updates to these fields are automatically recorded in the **Work notes** field.
-   When the asset is received by a transfer order. These work notes help in tracking the life cycle of an asset.


</td></tr></tbody>
</table>5.  Select **Save**.


## Result

The pallet that you created is added to the list shown in the Pallets tab.

**Parent Topic:**[Manage your inventory through pallet assets](../concept/pallets-for-inventory-management.md)

**Related topics**  


[Add assets to a pallet](add-assets-to-pallet.md)

[Remove assets from a pallet](remove-assets-from-pallet.md)

[Delete pallet assets](delete-pallet-assets.md)

[Using pallet assets for managing inventory](../concept/using-pallet-assets-for-inventory-mgmt.md)

