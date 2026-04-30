---
title: Add assets to a pallet in the Enterprise Asset Workspace
description: Add enterprise, hardware, base, bundle, or consumable assets to a pallet so that you can track and manage them as a group.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create pallet assets in the Enterprise Asset Workspace, Create and manage enterprise assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Add assets to a pallet in the Enterprise Asset Workspace

Add enterprise, hardware, base, bundle, or consumable assets to a pallet so that you can track and manage them as a group.

## Before you begin

To add hardware, base, or bundle assets to a pallet, install and activate the Hardware Asset Management application on your ServiceNow® instance. To install and activate the application, request it from the [ServiceNow Store](https://store.servicenow.com).

Role required: sn\_eam.enterprise\_asset\_manager or sn\_eam.enterprise\_asset\_technician

## About this task

You can add an asset to a pallet only under the following conditions:

-   The **State** field on the pallet asset record is set to **In stock**.
-   The **State** field on the asset record is set to one of the following options:
    -   **On order**
    -   **In stock**
    -   **In transit**
-   The **Stockroom** field on the asset record is either empty or set to the same stockroom as the pallet.
-   The asset isn’t associated with another parent asset.

## Procedure

1.  From the Enterprise Asset Workspace, open the Enterprise asset estate view.

2.  On the **All assets** tab, select the pallet that you want to add assets to.

    The pallet asset record opens.

3.  Select the **Assets** tab.

4.  Add assets to the pallet.

    -   To add enterprise, hardware, base, or bundle assets to the pallet, use the following steps:
        1.  Select **Add assets**.

            The Add assets dialog box opens.

        2.  In the dialog box, select the check box for every asset that you want to add to the pallet.
        3.  Select **Add**.
    -   To add consumable assets to the pallet, use the following steps:
        1.  Select **Add consumables**.

            The Add consumable to pallet dialog box opens.

        2.  In the **Consumable** field, search for and select the consumable asset that you want to add to the pallet.
        3.  In the **Quantity** field, specify the quantity of the consumable asset that you want to add to the pallet.
        4.  Select **Add**.

## Result

The assets are added to the **Assets** tab of the pallet asset record.

**Parent Topic:**[Create pallet assets in the Enterprise Asset Workspace](create-pallet-asset-eam.md)

