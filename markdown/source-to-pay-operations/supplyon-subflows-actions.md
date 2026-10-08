---
title: SupplyOn subflows and actions
description: The flows, subflows, and actions that make up the integration, and the outbound send step sequence.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/supplyon-subflows-actions.html
release: zurich
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 2
breadcrumb: [SupplyOn integration architecture and processing, Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# SupplyOn subflows and actions

The flows, subflows, and actions that make up the integration, and the outbound send step sequence.

The integration is delivered as a set of flows, subflows, and Integration Hub actions.

|Type|Name|Purpose|
|----|----|-------|
|Flow|SupplyOn Outbound PO - Create/Update/Cancel|Fires when an outbound header reaches New \(10\). Runs the eligibility gate and invokes the send subflow.|
|Subflow|SupplyOn Outbound PO - Send|Builds and posts the order to SupplyOn, stamps the correlation token, and waits for the async outcome. Runs as system.|
|Action|Post SupplyOn Purchase Order|Posts POST /purchaseorder through the supplyOnOrders alias.|
|Flow|SupplyOn Outbound PO - Async Callback|REST API asynchronous trigger. Hosts the receiver endpoint and maps the request body into the callback subflow.|
|Subflow|SupplyOn Async Callback - Handle Status|Correlates the notification to the outbound row and advances its status. Runs as system.|
|Subflow|Get Order Confirmation from SupplyOn|Scheduled pull of line-level confirmations into inbound staging.|
|Action|Get demand-response summaries|Lists orders with confirmations in the look-back window \(GET /demandresponse-summaries\).|
|Action|Get demand-response detail|Retrieves per-line confirmation detail for one order \(GET /demandresponse\).|

## Outbound send: step sequence

The send subflow moves the row through the following steps and status transitions.

1.  Resolve the operation: The resolver returns create or cancel, never update, because SupplyOn owns insert-versus-update. Cancel is returned when the source purchase order header or any line is in a canceled or pending-cancellation state.
2.  Move the header and lines to 20 \(In process\): This happens before the POST, so a row can't sit at 20 without the send having started.
3.  Build the payload: The factory maps the staging header and lines into the SupplyOn JSON. It also maps the source purchase order for attachments, applies the routing triple, embeds header attachments, and runs the scripted extension point.
4.  Invoke Post SupplyOn Purchase Order: The REST step posts the order and reads back the status code and the synchronous response \(TransactionID, StatusCode, StatusText\).
5.  Handle the synchronous outcome: On a non-201, the header and lines move to 40 \(Failed\), the message is set to the error detail, and the flow ends without waiting. On a 201, the header message is stamped with the SON-TXN:&lt;TransactionID&gt; token and a note that the order was sent and is awaiting the async status. The status stays at 20.
6.  Wait up to 24 hours for the status to change from 20: On timeout, the header and lines move to 40 and the correlation token is preserved so that a late callback can reconcile the row to 30. If the callback has already arrived, the async path has set 30 or 40 and the send subflow does not rewrite the status.

**Note:** This subflow writes 20 and 40 \(synchronous failure or timeout\). It does not write 30. Setting status 30 is the async callback job.

Cost-allocation lockstep: At each transition, the integration mirrors the status onto any `sn_spend_intg_outbound_cost_allocation` rows for the order, so that buyer-side cost-allocation records don't remain open after the order closes. Because the cost-allocation table has no foreign key to the outbound header, correlation is by the order line numbers. These rows are not sent to SupplyOn.

Custom extension point: The outbound send provides a scripted extension point for payload adjustment. The confirmation pull does not currently define one.

