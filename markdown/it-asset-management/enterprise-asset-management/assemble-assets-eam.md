---
title: Select assets for user-assembled asset
description: Create a user-assembled asset by selecting assets from the parent asset's stockroom.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create and manage enterprise assets, Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Select assets for user-assembled asset

Create a user-assembled asset by selecting assets from the parent asset's stockroom.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## Procedure

1.  Open the user assembled model and open an asset record from the **Assets** tab.

2.  Select **Assemble** to open the Select assets dialog box.

3.  Fill in the form details.

    |Field|Description|
    |-----|-----------|
    |Model component|The model components associated with the multi-component model.|
    |Quantity|Quantity of the model component.|
    |Asset|Assets from the parent stockroom. For consumable assets, the quantity of the asset in the stockroom is also mentioned.|
    |Action|Indicates if the corresponding model component is required or not. A enabled cross indicates that you can remove the model component. A disabled cross indicates that this is a required model component. If you remove a model component, the Select more model components drop-down box appears allowing you to restore the model components that you removed.|

4.  Select **Assemble**.

    The assets you selected are added to the parent asset. You can view these assets in the **Child Assets** tab. All consumable assets are displayed as a single record, instead of individual records.


**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)

