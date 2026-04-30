---
title: Create enterprise assets
description: Create assets for specific model categories in the Enterprise Asset Management application.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create and manage enterprise assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create enterprise assets

Create assets for specific model categories in the Enterprise Asset Management application.

## Before you begin

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## About this task

Enterprise asset classes have a one to one mapping to product model classes and model categories​. Enterprise asset classes are mapped to existing CI classes where applicable.

There are two kinds of assets: consumable assets and serialized assets. Consumable assets don’t have an asset tag or a serial number.

**Note:** This topic provides details on how to create enterprise, construction, facility, industrial, medical, retail, tactical equipment, transportation, and wearable assets. For details on how to create pallet assets, see [Create pallet assets in the Enterprise Asset Workspace](create-pallet-asset-eam.md).

## Procedure

1.  Navigate to **All** &gt; **Enterprise Asset Workspace** &gt; **Enterprise asset estate**.

2.  Select the **All enterprise** tab to select from all the Enterprise Asset Management models or select a specific asset tab such as **Facility**, **Industrial**, **Medical**, **Retail**, **Transportation**, and **Consumable**.

3.  Select **New**.

4.  In the dialog box, fill in the fields.

<table id="table_etr_rqq_wsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

The type of asset you want to create. Choose from the following options:-   Enterprise Asset
-   Construction Asset
-   Facilities Asset

**Note:** The Enterprise Asset Management application supports only facilities assets that fall under the Facility asset \[sn\_ent\_facility\_asset\] child class of the Enterprise asset \[sn\_ent\_asset\] class. The application does not support facilities assets that are listed in the Facility \[alm\_facility\] table.

-   Industrial Asset
-   Medical Asset
-   Retail Asset
-   Transportation Asset
-   Tactical Equipment Asset
-   Wearable Asset
 **Note:** This field only appears if you selected **New** from the **All enterprise** tab.

</td></tr><tr><td>

Model category

</td><td>

The model category that the asset belongs to. Based on the model category selected, the asset can be linked to a configuration item.

</td></tr></tbody>
</table>5.  Select **Create**.

    The Create new asset page appears. By default, the asset is in **Build** state. You can change the status only after you’ve saved the asset record.

6.  In the Create New asset page, fill in the details.

    For a detailed description of the fields, see [Asset fields for enterprise assets](../reference/asset-fields-eam.md).

7.  Select **Save**.

    The asset is created along with a Configuration Item \(CI\) for this asset. Child assets are automatically created for the newly created asset. You can perform additional configuration on the asset by entering details in the other tabs such as **Child Assets**, **Contracts**, **Expense Lines**, and **All Related Tasks**.

    **Note:** The All Related Tasks tab shows a list of the related tasks such as Disposal task, Resale task, Recall task, Work order task, and Move task associated with the asset. The Recall task and the Work order task associated with the child assets are also shown in the All Related Tasks tab.

    For the pre-assembled industrial assets, the MAC address field is also shown in the **Child Assets** tab.

8.  After you’re done performing the additional configuration on the asset, you can change the status of the asset to **In Use**.

    The asset can be deleted only by the sn\_eam.enterprise\_admin role.


**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)

