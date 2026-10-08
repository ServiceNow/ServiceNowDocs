---
title: SupplyOn integration limitations
description: The SupplyOn integration has known limitations that affect purchase orders, supplier confirmations, and blanket orders.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/supplyon-limitations.html
release: australia
topic_type: concept
last_updated: "2026-10-08"
reading_time_minutes: 1
breadcrumb: [Reference, Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# SupplyOn integration limitations

The SupplyOn integration has known limitations that affect purchase orders, supplier confirmations, and blanket orders.

## Current limitations

-   Purchase order cancellation is detected but not sent: The SupplyOn per-position cancel field does not exist in the POST schema. A detected cancellation posts as a normal `FunctionCode 9` order without attachments. Skipping a previously sent line does not cancel it, and there is no whole-PO cancel.
-   Supplier confirmations are available only through the confirmation pull: The async callback is a status acknowledgment \(whether SupplyOn accepted the order\), not line data.
-   Blanket main \(type 20\) orders are mapped to payload only: Release orders \(children of a blanket\) are excluded at the eligibility gate. SupplyOn receives only the main order.
-   Service and handling-fee lines aren't sent: Lines with product type 20 \(service\) or 30 \(handling fee\) are excluded from the payload. Lines with an empty product type are kept.
-   Attachments are sent at header level only: SupplyOn has no per-line attachment field, so line-level attachments aren't sent.

