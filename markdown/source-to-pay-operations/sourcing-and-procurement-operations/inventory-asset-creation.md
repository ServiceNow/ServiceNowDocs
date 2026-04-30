---
title: Inventory asset creation
description: Inventory assets are not created upfront when fixed assets are created.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Inventory asset creation

Inventory assets are not created upfront when fixed assets are created.

They are created only when the following conditions are satisfied:

-   Asset tracking strategy on the product model is set to create assets.
-   Product category referenced on the product model has an asset class defined.
-   Product has been partially or fully delivered. In case of partial delivery, only the corresponding partial quantity of inventory assets are created.

Inventory assets are not created if goods receipt required is specified as no for a good, or if the acknowledgment type is a two-way match for a service.

If you have defined an asset class, the corresponding asset records are created and associated to the relevant contract model on the purchase order, which are then displayed on the assets covered related list. The applicable contract models that should have the assets covered related list are insurance, lease, maintenance, purchase order, software license, subscription, and warranty.

To view the asset related list, navigate to **Asset** &gt; **Portfolios** &gt; **All Assets**. A **Purchasing** tab has been added to the asset form view to capture procurement specific fields that are populated from the purchase order line of the corresponding asset.

|Field|Description|
|-----|-----------|
|Purchase order|Purchase order associated with this asset.|
|ERP number|Unique number generated within the ERP system for the purchase order.|
|Purchase order line|Purchase order line associated with the asset.|
|Supplier|Supplier associated with the asset.|
|Unit|Unit used to purchase this asset.|
|Unit price|Unit price of this asset.|
|Recipient|Recipient of the asset.|
|Received|Date when the asset was received.|

For more information on asset creation, see [Create assets](https://www.servicenow.com/docs/access?context=c_ManagingAssets&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

A fixed asset related list has also been added. It displays the fixed asset that is associated with this inventory asset if a capitalization policy was satisfied.

**Parent Topic:**[Sourcing and Purchasing Automation](../reference/purchase-experience-workflow.md)

