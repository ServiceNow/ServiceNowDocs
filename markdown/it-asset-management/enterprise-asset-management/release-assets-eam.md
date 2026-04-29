---
title: Release assets from the parent asset
description: Release a child asset that is no longer required to be associated with its parent asset.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create and manage enterprise assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Release assets from the parent asset

Release a child asset that is no longer required to be associated with its parent asset.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## About this task

You can release only one child asset at a time from a user-assembled, pre-assembled, or a single asset.

You can release an asset that isn't required or an add-on asset that's in one of the following states:

-   In use
-   In maintenance
-   In stock \(Substate as Pending disposal\)
-   In stock \(Substate as Pending repair\)

## Procedure

1.  Navigate to **All** &gt; **Enterprise Asset Workspace** &gt; **Enterprise asset estate**.

2.  Select the parent asset record from which you want to release assets.

3.  Select **Release assets**.

4.  In the **Release asset** dialog box, fill in the details.

    1.  In the **Asset to release** field, select the child asset that you want to release.

        The **Asset Tag** and the **Serial Number** fields are displayed. These fields are automatically populated only if the details are available in the Asset \[alm\_asset\] table. Otherwise, you must manually enter the details in these fields to proceed with the Release action.

        **Note:** The **Asset Tag** and the **Serial Number** fields aren't displayed for consumables.

    2.  In the **Select stockroom for released assets** field, select the stockroom to which the child asset should be released.

    3.  In the **Quantity** field, enter the quantity of assets that you want to swap.

        This field is automatically populated with the quantity of the asset that you want to swap. However, you can change the value in this field only if the asset is a consumable. For all the other assets, this field is a read-only field. You can't swap more than the actual quantity of the consumable. For example, if you have five consumables, you can either swap less than 5 or swap all the five consumables.


## Result

-   The asset that you released isn't listed in the **Child assets** tab.
-   The state of the released asset changes to In stock and the substate changes to Pending disposal.

**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)

