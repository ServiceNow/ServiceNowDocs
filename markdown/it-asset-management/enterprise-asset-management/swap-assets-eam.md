---
title: Swap assets for parent multi-component asset
description: Swap child assets that are part of a multi-component asset. You can swap out only one child asset at a time.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create and manage enterprise assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Swap assets for parent multi-component asset

Swap child assets that are part of a multi-component asset. You can swap out only one child asset at a time.

## Before you begin

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterptrise\_asset\_manager

## About this task

You can swap assets that are in the following states:

-   In use, only if the child asset is hot swappable
-   In maintenance
-   In stock \(Substate Defective or Pending repair\)

The swap functionality is available only for the parent asset of a multicomponent asset.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Asset Workspace** &gt; **Enterprise model management**.

2.  Select a multi-component record.

3.  Select the **Assets** tab and select a parent asset.

4.  Select **Swap**.

5.  In the **Swap asset** dialog box, fill in the details.

    1.  In the **Asset to swap out** field, select the child asset that you want to swap.

        The **Asset Tag** and the **Serial Number** fields are displayed. These fields are automatically populated only if the details are available in the Asset \[alm\_asset\] table. Otherwise, you must manually enter the details in these fields to proceed with the Swap action.

        **Note:** The **Asset Tag** and the **Serial Number** fields aren't displayed for consumables.

    2.  In the **Choose stockroom for asset swap** field, select the stockroom from which you want to choose an asset to swap with your asset.

    3.  To display assets that are based on substitute models, select the **Include assets based on substitute models** check box.

        Assets of a substitute model are shown in the **Replacement asset** field only if they meet the following criteria:

        -   The asset function isn’t a loaner or the asset function is empty.
        -   The **State** or **Substate** is **In Stock** or **Available**.
        -   The potential replacement asset's **Parent** field is empty.
        -   Stockroom is the same as the value entered in the stockroom field.
        When the assets that meet the substitute model criteria aren't shown in the **Replacement asset** field, search for the model name because the search query refreshes with each keystroke.

    4.  In the **Replacement asset** field, select the asset that you want to swap with.

        You can only choose from the similar assets that are available in the stockroom that you selected.

    5.  In the **Quantity** field, enter the quantity of assets that you want to swap.

        This field is automatically populated with the quantity of the asset that you want to swap. However, you can change the value in this field only if the asset is a consumable. For all the other assets, this field is a read-only field. You can't swap more than the actual quantity of the consumable. For example, if you have five consumables, you can either swap less than 5 or swap all the five consumables.

    6.  Select **OK**.


## Result

-   The asset is successfully swapped and the new asset inherit the State and Status of the parent asset.
-   The state of the swapped-out asset changes to In stock and the substate changes to Pending repair. If the asset is a consumable, the state changes to In stock and the and substate changes to Pending disposal.
-   The stockroom of the swapped out asset changes to the stockroom that you selected in the **Choose stockroom for asset swap** field.

**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)

