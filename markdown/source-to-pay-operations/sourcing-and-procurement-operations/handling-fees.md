---
title: Handling fees
description: Configure the conditions of a purchase request that, met, add a handling fee to that purchase request. Any field on the Purchase Request table can be used as part of the conditions to determine if a handling fee is to be applied for a purchase.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/handling-fees.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Purchase requisition, Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Handling fees

Configure the conditions of a purchase request that, met, add a handling fee to that purchase request. Any field on the Purchase Request table can be used as part of the conditions to determine if a handling fee is to be applied for a purchase.

If multiple handling fees are generated based on the configurable conditions, the handling fee with the lowest rank is applied. A Procurement Administrator can use the Pricing table to apply handling fee pricing. In the Pricing table, handling fees can be set as a fixed price or as a percentage-based price. When percentage-based pricing is used, the handling fee is calculated as a percentage of the total amount of all lines on the purchase request.

If there is a handling fee rule associated with a purchase requisition, a new purchase line is created with product type as handling fee. The handling fee purchase line is view-only and visible from the **My purchases** tab.

**Note:** Handling fees support fixed amounts and percentage-based pricing only. Tiered or break-based pricing is not available for handling fees.

**Parent Topic:**[Purchase requisition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-requisition.md)

