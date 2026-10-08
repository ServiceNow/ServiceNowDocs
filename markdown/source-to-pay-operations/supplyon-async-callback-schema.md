---
title: SupplyOn async callback request schema and branches
description: The request schema of the async status callback, the correlation contract, the processing branches, and sample payloads.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/supplyon-async-callback-schema.html
release: zurich
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 1
breadcrumb: [Reference, Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# SupplyOn async callback request schema and branches

The request schema of the async status callback, the correlation contract, the processing branches, and sample payloads.

The async callback endpoint is `POST /api/sn_supplyon_po/supplyon_outbound_po_async_callback`. The request body follows the SupplyOn status notification schema, a pure status acknowledgment:

-   **uuid** \(required\): The correlation key. Equals the synchronous 201 transaction ID.
-   **status** \(required\): Strictly OK or ERROR.
-   **Errors** \(optional\): A list of items, each with a Code and Text.

No line-level positions ride the callback. Supplier confirmations come only from the confirmation pull.

Correlation contract. The send subflow stamps `SON-TXN:<TransactionID>` into the outbound header message at status 20. The callback uuid is that transaction ID, so the subflow looks up the row by message and then overwrites the message with the outcome text. The subflow does not use **erp\_number** for correlation. On the success branch only, the subflow stamps **erp\_number** with the order number so the framework **Handle Status Change** business rule fires on status 30.

|Branch|Condition|Behavior|
|------|---------|--------|
|Invalid body|No uuid, or unparseable|Logs an error. Nothing is updated.|
|No matching row|Valid uuid, no header message matching the token|Logs a warning. Safe no-op. The flow returns HTTP 200 \(no retry storm\).|
|Success|status = OK|Header and lines move to 30 \(Processed\). Header erp\_number set to the order number. Message set to a success note.|
|Failure|status = ERROR|Header and lines move to 40 \(Failed\). Message set to the error category and verbatim error text. No erp\_number write.|

Header and lines move in lockstep in both branches. A duplicate or re-delivered callback re-applies the same status \(idempotent\). An unexpected error in the subflow is caught by the native Error Handler.

## Sample callback payloads

```
// Success
{ "uuid": "2491C8AF4F962D2CCB87CC102AFCXXXX", "status": "OK", "Errors": [] }

// Failure
{
  "uuid": "2491C8AF4F962D2CCB87CC102AFCXXXX",
  "status": "ERROR",
  "Errors": [{ "Code": "BOOK_017", "Text": "Order rejected: unknown supplier for routing triple." }]
}
```

