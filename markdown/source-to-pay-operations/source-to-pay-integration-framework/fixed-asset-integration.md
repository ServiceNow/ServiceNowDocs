---
title: Fixed asset integration
description: Fixed assets are created automatically in Source-to-Pay \(S2P\) on creation of a purchase order, when capitalization policy criteria are satisfied, and synchronized to the ERP system asynchronously.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Source-to-Pay integration framework, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Fixed asset integration

Fixed assets are created automatically in Source-to-Pay \(S2P\) on creation of a purchase order, when capitalization policy criteria are satisfied, and synchronized to the ERP system asynchronously.

The following fields are added in the Fixed Asset table to integrate with the ERP systems:

-   Depreciation lifecycle
-   Depreciation term
-   Salvage value

Whenever the **Depreciated amount**, **Remaining value**, and **Salvage value** fields are updated in the ERP system, depending on the depreciation term defined in the ERP, the values are synced back to S2P for the corresponding fixed asset. A configurable scheduled job Fetch Fixed Asset Details defined in S2P determines the frequency to retrieve this data from the ERP system.

For more information on automatic fixed asset creation, see [Fixed asset creation](../../sourcing-procurement-operations/concept/fixed-asset-creation.md).

