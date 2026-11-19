---
title: Asset bundles
description: Asset bundles help you bundle a group of assets, already in your inventory, as a single entity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/asset-bundles-concept.html
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Hardware Asset Management, IT Asset Management]
---

# Asset bundles

Asset bundles help you bundle a group of assets, already in your inventory, as a single entity.

An asset bundle comprises consumable and hardware assets.

|Component|Model category|
|---------|--------------|
|Apple MacBook W9576XA|hardware asset|
|Samsung monitor B2156C|hardware asset|
|Logitech mouse PB567VT|consumable|
|Apple keyboard MT65021R|consumable|

Asset bundles are based on bundled models. A bundled model is a grouping of models. For more information on bundled models, see [Bundled models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/product-catalog/c_CreatingBundledModels.md).

Existing assets from stockrooms are used to create an asset bundle. Only assets that are in the **In stock** status and **Available** substatus are added to an asset bundle. If you want to exclude any assets, you must remove the asset from the bundle. For more information about asset exclusion, see [Hardware Asset Management license exclusion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/ham-license-exclusion.md). Assets that are part of an asset bundle aren’t available as individual assets. No CIs are associated with an asset bundle.

An asset bundle goes through the entire asset life cycle. From building an asset bundle, allocating the bundle to a user, moving it to a state of maintenance if assets need repair, and finally retiring the bundle when its purpose is fulfilled.

Asset bundles can be transferred between stockrooms. However, individual assets within a bundle can't be transferred between stockrooms. Assets within a bundle can't be disposed. After an asset bundle is retired, the assets are disassociated from the bundle and can be individually disposed. Deleting an asset bundle moves all assets belonging to the bundle to a stockroom.

You can swap assets belonging to an asset bundle. Assets can be swapped when the state of the bundle is **In maintenance** or **In stock** and substate **Pending repair**.

You can retire an asset bundle and release all the assets belonging to the bundle. The assets that are released are returned to a stockroom and you can delete the bundle.

Assets belonging to a bundle are excluded from sourcing, transfer orders, and disposal orders flows.

**Important:** Asset reclamation supports hardware and consumable assets. Asset bundles and pallets aren't supported by default and require customization of the reclamation flow and request to handle these asset classes.

For more information on creating asset bundles, see [Manage asset bundles from your inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/create-bundled-assets.md).

**Parent Topic:**[IT Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/it-asset-management.md)

