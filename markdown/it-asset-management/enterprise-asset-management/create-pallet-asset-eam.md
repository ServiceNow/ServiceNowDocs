---
title: Create pallet assets in the Enterprise Asset Workspace
description: Create pallet assets to track and manage the pallets that can transport and store your enterprise, hardware, base, bundle, and consumable assets.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create and manage enterprise assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create pallet assets in the Enterprise Asset Workspace

Create pallet assets to track and manage the pallets that can transport and store your enterprise, hardware, base, bundle, and consumable assets.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager or sn\_eam.enterprise\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Enterprise asset estate view.

2.  On the **All assets** tab, select **New pallet asset**.

3.  On the form, fill in the fields.

<table id="table_zqn_vj5_2xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Pallet Details

</td></tr><tr><td>

Vendor

</td><td>

Vendor that the pallet was purchased from. If the pallet was automatically created from a procurement purchase order, the **Vendor** field is automatically set to the same vendor that was specified on the purchase order.

</td></tr><tr><td>

Model

</td><td>

Pallet model that the pallet is associated with.

</td></tr><tr><td>

Asset tag

</td><td>

Alphanumeric value that your organization assigns to the pallet for tracking purposes.

</td></tr><tr><td>

State

</td><td>

Current state of the pallet.

 This field is automatically set to **In stock**. However, you can also set this field to one of the following options:

-   **In transit**
-   **Retired**
-   **Missing**


</td></tr><tr><td>

Stockroom

</td><td>

Stockroom that the pallet is located in.

</td></tr><tr><td>

Aisle and space

</td><td>

Stockroom aisle and space that the pallet is located in.

</td></tr><tr><td>

Parent

</td><td>

Parent asset of the pallet.

</td></tr><tr><td>

Comments

</td><td>

Message that you want to apply to the pallet.

</td></tr><tr><td>

Pallet type

</td><td>

Type of pallet. Select one of the following options:-   **Pallet**
-   **Bin**
-   **Box**
-   **Container**
-   **Other**


</td></tr><tr><td>

Substate

</td><td>

Current substate of the pallet, such as **Available** or **Reserved**. The options that are available in the **Substate** field change based the option that you select in the **State** field.

</td></tr><tr><td>

Reserved for

</td><td>

User who the pallet is reserved for.

</td></tr><tr><td>

Location

</td><td>

Physical location of the pallet.**Note:**

If you set the location to a specific place and then set the **sn\_itam\_common.sn\_enable\_indoormap\_for\_assets** system parameter to **true** on your ServiceNow instance, the pallet asset record, which is generated after you fill in all fields and save this form, includes an interactive map that shows the real-time location of the asset.

This map is still included in the pallet asset record when you open the record from an associated work order task or stockroom record.

The map does not display by default. To display the map, select the Location map icon \(![Location map icon.](../image/asset-indoor-location-icon.png)\) on the sidebar of the pallet asset record.

</td></tr><tr><td colspan="2">

Disposal

</td></tr><tr><td>

Disposal vendor

</td><td>

Vendor that is assigned to carry out the disposal order for the pallet.

</td></tr><tr><td>

Vendor disposal order ID

</td><td>

ID number that is assigned to the disposal order by the disposal vendor.

</td></tr><tr><td>

Disposal date

</td><td>

Date on which the disposal order is completed.

</td></tr><tr><td>

Resold value

</td><td>

Estimated price that the pallet can be resold for.

</td></tr><tr><td>

Scheduled retirement

</td><td>

Date on which you want to retire the pallet.

</td></tr><tr><td>

Retired date

</td><td>

Actual date on which you retired the pallet.

</td></tr><tr><td>

Beneficiary

</td><td>

Organization that receives the pallet after it is retired.

</td></tr><tr><td>

Resale price

</td><td>

Value of the pallet when it is retired.

</td></tr><tr><td colspan="2">

Activities

</td></tr><tr><td>

Work notes

</td><td>

Work notes related to the pallet.

</td></tr></tbody>
</table>4.  Select **Save**.


-   **[Add assets to a pallet in the Enterprise Asset Workspace](add-assets-pallet.md)**  
Add enterprise, hardware, base, bundle, or consumable assets to a pallet so that you can track and manage them as a group.
-   **[Remove assets from a pallet in the Enterprise Asset Workspace](remove-assets-pallet.md)**  
Remove any enterprise, hardware, base, bundle, or consumable assets that you no longer want to track and manage as part of a pallet.
-   **[Using pallet assets to manage your asset inventory in the Enterprise Asset Workspace](../concept/using-pallets-manage-inventory-eam.md)**  
You can manage your asset inventory by using pallets and the assets contained within those pallets in your transfer orders, disposal orders, resale orders, and various consumption workflows.

**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)

