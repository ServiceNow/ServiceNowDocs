---
title: Update enterprise assets that have unknown enterprise models
description: If an enterprise asset is associated with an unknown enterprise model, update it with a known enterprise model so that you can accurately categorize and track it.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create and manage enterprise assets, Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Update enterprise assets that have unknown enterprise models

If an enterprise asset is associated with an unknown enterprise model, update it with a known enterprise model so that you can accurately categorize and track it.

## Before you begin

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## About this task

**Note:** You can update the enterprise model only for serialized and multi-component enterprise assets.

## Procedure

1.  From the Enterprise Asset Workspace, open the Enterprise asset estate view.

2.  Select either the **All enterprise** tab or the tab for a specific enterprise asset type, such as **Medical**.

3.  From the list of available enterprise assets, select an enterprise asset for which the **Model** field is set to **Unknown Model**.

    The asset record opens. All asset record fields are read-only.

4.  On the asset record, select **Update**.

    The To what type of enterprise asset would you like to change? dialog box opens.

5.  In the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Type|Enterprise asset type that you want to categorize the enterprise asset under.|
    |Model category|Enterprise model category that you want the enterprise asset to belong to. The enterprise asset can be linked to a corresponding configuration item \(CI\) based on the enterprise model category that you select.|
    |Model|Enterprise model that you want to associate the enterprise asset with.|

6.  Select **Update**.

    The dialog box closes and you automatically return to the asset record. If the update is successful, the asset record fields become editable.

    **Note:** If the selected enterprise asset type, enterprise model category, and enterprise model update the enterprise asset to a user-assembled multi-component asset, the **State** field on the asset record automatically changes to **Build**. The **Assemble** and **Auto assemble** buttons also appear on the asset record. You can use these buttons to initiate the assembly process for the enterprise asset. For more information on user-assembled multi-component assets, see [Select assets for user-assembled asset](assemble-assets-eam.md).


**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)

