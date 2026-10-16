---
title: SupplyOn integration diagnostics
description: Techniques for diagnosing issues with the outbound send, the async callback, and the confirmation pull.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/supplyon-troubleshooting.html
release: zurich
topic_type: concept
last_updated: "2026-10-09"
reading_time_minutes: 1
breadcrumb: [Reference, Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# SupplyOn integration diagnostics

Techniques for diagnosing issues with the outbound send, the async callback, and the confirmation pull.

## Trace the outbound send

The outbound logic runs through flows and subflows, and each run is logged. Open the outbound order transactions, then open the subflow context to trace the run, including the Post SupplyOn Purchase Order action. SupplyOn returns only a transaction ID, so to see the request body on the platform, enable debug logging.

## Use the transaction ID

The transaction ID on the outbound order is a temporary correlation value, used for correlation. If the send fails, the SupplyOn error message appears in the processing message of the outbound order. A send fails when the 24-hour timeout elapses without SupplyOn receiving the order, or when SupplyOn rejects the order. Give the transaction ID to SupplyOn so SupplyOn can report the payload it received.

## Debug the async callback endpoint

The async callback is the most frequent integration failure point. SupplyOn must post the acceptance or rejection back to the instance through a webhook; this outcome can't be pulled. To confirm whether SupplyOn is reaching the endpoint, open the SupplyOn Outbound PO - Async Callback flow, turn on debugging, and review the operations. With debugging on, you can see the request body that SupplyOn posted, including the transaction ID.

## Enable debug logging

Set the logging verbosity system property to `debug`. The system logs then record the request payload sent to SupplyOn, so you can inspect it directly on the platform. The organization code and plant code override system properties are set in the System Properties table.

