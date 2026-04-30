---
title: Fixed asset creation
description: As a procurement administrator, you can create fixed assets for products that are purchased for long-term use and are not likely to be converted quickly into cash.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Fixed asset creation

As a procurement administrator, you can create fixed assets for products that are purchased for long-term use and are not likely to be converted quickly into cash.

Fixed asset creation is automated when capitalization policy criteria are satisfied. To ensure that fixed assets are created automatically on creation of a purchase order, you must first define an applicable capitalization policy. For more information on how to define a capitalization policy, see [Define a capitalization policy](../task/define-capitalization-policy.md).

**Note:** Blanket purchase orders cannot result in the creation of a fixed asset.

You can navigate to **Sourcing and Purchasing Automation** &gt; **Primary Data** &gt; **Fixed Assets**, and review these fields.

|Field|Description|
|-----|-----------|
|Number|System-generated unique identifier for the fixed asset.|
|ERP asset number|Unique identifier generated within the ERP system for the fixed asset.|
|Display name|System-generated unique display name for the fixed asset. This is an auto-generated value derived from concatenating the ERP number and the product name into &lt;ERP number - Product name&gt;, where the values are taken from the **ERP asset number** and **Product name** fields respectively. If either of these fields are null or empty, then the corresponding value is left empty.|
|Supplier|Supplier from whom this fixed asset was purchased.|
|Product name|Name of the purchased product.|
|Purchase order line|The purchase associated with this fixed asset.|
|Status|Current status of the creation of the fixed asset. The options are Submitted, Success, and Pending Deletion. This field is used in the back end for SAP integration purposes.|
|Capitalize on|The date on which the requester assumes the liability of the fixed asset, depending on the supplier incoterm.|
|Original value|The amount originally paid for the fixed asset.|
|Depreciation lifecycle|The length of time in which the fixed asset is fully depreciated.|
|Depreciation term|The frequency of depreciation throughout the lifecycle of the fixed asset.|
|Depreciated amount|The amount that the fixed asset has depreciated by, over time.|
|Remaining value|The amount that the fixed asset is worth today, after factoring in depreciation.|
|Salvage value|The amount that the fixed asset is worth after it has come to the end of its useful life.|

**Parent Topic:**[Sourcing and Purchasing Automation](../reference/purchase-experience-workflow.md)

