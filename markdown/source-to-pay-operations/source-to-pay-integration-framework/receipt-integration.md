---
title: Receipt integration
description: Receipts are created in Source-to-Pay \(S2P\) and synchronized to the ERP system asynchronously.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Receipt integration

Receipts are created in Source-to-Pay \(S2P\) and synchronized to the ERP system asynchronously.

## Process flow

-   When a receipt record is created in S2P, integration with the ERP system is triggered. This creates a goods receipt \(GR\) in the ERP system.
-   If there is an integration error, an integration error purchasing task is created on the purchase order. This contains the error message from the ERP system to inform the procurement specialist what must be updated.
-   Similar to purchase order integration, a goods receipt is not created in the ERP system until the integration error is resolved in S2P. At this juncture, the status of the receipt in S2P is set to Pending Review.
-   On successful goods receipt creation in the ERP system, an ERP number is returned and synchronized back to the appropriate record in S2P.

**Note:** No additional configurations are required for receipt integration to function.

