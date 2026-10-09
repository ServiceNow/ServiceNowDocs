---
title: SupplyOn outbound special cases and edge conditions
description: These special cases and edge conditions apply to the outbound send, covering non-eligible rows, release orders, missing lines, attachment violations, cancellations, and failure conditions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/supplyon-special-cases.html
release: australia
topic_type: reference
last_updated: "2026-10-09"
reading_time_minutes: 1
breadcrumb: [Reference, Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# SupplyOn outbound special cases and edge conditions

These special cases and edge conditions apply to the outbound send, covering non-eligible rows, release orders, missing lines, attachment violations, cancellations, and failure conditions.

The following special cases and edge conditions apply to the outbound send.

|Case|Behavior|
|----|--------|
|Row not routed through the SupplyOn connection alias|The eligibility gate takes no action and logs a distinct line. The row is left for its own ERP dispatch.|
|Blanket release order \(core blanket\_order populated\)|The gate takes no action and logs a distinct line. SupplyOn receives only the primary order.|
|Non-standard purchase order type|The factory throws an error and the row is not sent. Primary blanket \(type 20\) mapping is an open item.|
|Order with no eligible lines|The header NetValue is omitted and the POST carries no positions.|
|Service or handling-fee lines|These lines are excluded from the positions.|
|Attachment limit or type violation|The system throws `SUPPLYON_ATTACHMENT_VIOLATION` and aborts before the REST call. The row is marked Failed.|
|Detected cancellation|The order is reserved as the cancel operation with attachments omitted. Per-line cancel emission is pending a SupplyOn API field. Until then the order posts as a normal FunctionCode `9` order.|
|Synchronous response not 201|Header and lines move to `40`, the message is set to the error detail, and the flow ends without waiting.|
|No callback within 24 hours|Header and lines move to `40`. The correlation token is preserved so that a late callback can reconcile the row to `30`.|

