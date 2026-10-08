---
title: SupplyOn error handling and retry
description: Error handling in the SupplyOn integration uses a layered model that includes transport-level HTTP retry, status and message updates, integration error tasks, and retrigger paths.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/supplyon-error-handling.html
release: australia
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 1
breadcrumb: [Reference, Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# SupplyOn error handling and retry

Error handling in the SupplyOn integration uses a layered model that includes transport-level HTTP retry, status and message updates, integration error tasks, and retrigger paths.

Error handling is layered: a transport-level HTTP retry at the connection, then the S2P integration framework paradigm, rather than a custom retry loop.

-   **Transport-level HTTP retry** Both aliases reference the out-of-box Default HTTP Retry Policy, which every Flow Designer REST step using the alias honors automatically. A qualifying failed call is retried up to three times at a fixed 10-second interval before the failure reaches flow logic. The retry conditions are idempotency-aware.
-   **Set status and message** On failure, the flow sets the staging record integration status to 40 \(Failed\) and populates the message field. The status write is a direct field write, which still fires the framework business rule.
-   **Error task creation** The framework async business rule Handle status change fires on status 40 and creates an integration error task \(`sn_shop_erp_error_task`, subtype purchase\_order\) assigned to the buyer. On a successful update that carries a non-empty erp\_number, the same rule closes active error tasks. Inbound \(confirmation pull\) errors create an unassigned, group-routed error task instead.
-   **Retrigger paths** Re-clicking Create PO resubmits the order \(closes error tasks, re-runs dispatch, and changes Draft to New, which re-fires the outbound trigger\). Run job re-runs the confirmation pull.
-   **Late callback recovery** The send subflow waits up to 24 hours for the callback. On timeout, the row is marked 40. The SON-TXN correlation token is preserved in the message, so a late callback can still reconcile the row from 40 to 30.
-   **Confirmation pull retry**. Because the pull re-runs on schedule with an overlapping look-back window and a high-water mark, a transient failure recovers on the next scheduled run.

|HTTP method|Retry conditions|
|-----------|----------------|
|GET \(confirmation pull\)|HTTP 408 \(request timeout\), 429 \(too many requests\), or a connect-timeout exception.|
|POST, PUT, DELETE \(outbound POST\)|Connect-timeout exception only. Not retried on 408, 429, or 5xx, to avoid double-submitting an order.|

**Note:** A SupplyOn-returned 4xx or 5xx on the POST is not retried at the transport layer. It passes directly to the Failed handling \(status 40\). A transient connectivity blip is handled transparently.

