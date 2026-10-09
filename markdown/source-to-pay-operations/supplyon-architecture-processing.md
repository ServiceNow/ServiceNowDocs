---
title: SupplyOn integration architecture and processing
description: The outbound send, async status callback, and confirmation pull streams process purchase orders. The connection model defines how environments and credentials are structured.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/supplyon-architecture-processing.html
release: zurich
topic_type: concept
last_updated: "2026-10-09"
reading_time_minutes: 4
breadcrumb: [Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# SupplyOn integration architecture and processing

The outbound send, async status callback, and confirmation pull streams process purchase orders. The connection model defines how environments and credentials are structured.

Both outbound streams move the Purchase Order Management outbound staging records through the framework integration-status life cycle. The header \(`sn_spend_intg_outbound_purchase_order`\) and its lines \(`sn_spend_intg_outbound_purchase_order_line`\) move in lockstep. For the status values, see [SupplyOn integration status values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplyon-integration-status-values.md).

## Connection model and environments

-   One logical connection, two keys: Every call targets the same SupplyOn host. SupplyOn exposes the orders endpoint and the demand-response endpoint under two separate APIM products, each with its own subscription key. A single connection and credential alias uses one key at a time, so the integration defines two aliases \(`supplyOnOrders` and `supplyOnDemandResponse`\) that differ only in their key. Both use the same host and the same header name \(`Ocp-Apim-Subscription-Key`\).
-   Alias REST action binding: Each alias is wired directly into the specific Integration Hub REST steps that call its endpoint. There is no per-call connection resolution.
-   Connection selection: The `sn_fcms_intg_source` record carries a single connection reference, which is used only for the outbound orders side \(routing and the eligibility gate scope check\). The demand-response side is bound at the action level. Dynamic multi-connection selection is not supported by the single-connection framework model against a two-key API.
-   Environment \(QAS and PRD\): The connection URL and subscription keys are environment-specific runtime data configured on each instance after deployment. The application defines only the alias records and a setup wizard. To move between environments, re-point the two aliases rather than adding connections.
-   Tenant identity: The buyer identity in SupplyOn is the routing triple: organization code, plant code, and supplier number. See [Configure the routing triple and payload properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplyon-configure-routing-triple.md).

## Outbound send processing

A record trigger on the outbound header \(condition `status=10`, trigger strategy Once\) fires when a row reaches New. This trigger is distinct from the framework dispatch trigger and is deliberately status-only, so it fires for every ERP source. An in-flow eligibility gate then decides whether the row belongs to SupplyOn. The gate keys off the connection-alias scope prefix \(`connection.id STARTSWITH sn_supplyon_po`\) rather than the ERP source name, making routing portable across instances.

The gate applies two checks:

1.  SupplyOn-routed: The order routes to an `sn_fcms_intg_source` whose connection scope prefix is `sn_supplyon_po` and that is active.
2.  Not a release order: The order is resolved by number on `sn_shop_order`. If its `blanket_order` reference is populated, the row is a blanket release order \(a child of a primary\) and is skipped, because SupplyOn receives only the primary order.

For the detailed step sequence and status transitions, see [SupplyOn subflows and actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplyon-subflows-actions.md).

## Async status callback processing

The receiver front door is a Flow Designer flow that uses the Integration Hub REST API asynchronous trigger \(`rest_async`\). Activating the flow auto-creates the HTTP endpoint, owns platform authentication, and exposes the request body as data pills. The flow maps the raw request body into a subflow that correlates the callback to the outbound staging row and advances its status. This path uses no staging table or transform map, because the callback is a pure processing acknowledgment, not line data.

The callback is stateless per call and uses no job tracker: correlation is entirely off the transaction ID token carried on the staging row. A re-delivered callback re-applies the same status \(idempotent\), and the flow returns HTTP 200 on any well-formed handled call, including a no-match, to prevent SupplyOn retry storms.

## Confirmation pull processing

A subflow registered against the SupplyOn ERP source configuration pulls supplier confirmations on demand. The integration doesn't provide a default schedule, so you run the job from the source configuration whenever you want to retrieve confirmations. It calls `GET /demandresponse-summaries` for the look-back window, then `GET /demandresponse` per order, and lands each line-level confirmation in the inbound confirmation staging tables. This is the standard staging pattern: spoke action, staging table, then a customer or framework transform into the core target table.

Each run queries a configurable window \(default equals the schedule interval\) with a small overlap for safety. The integration persists a high-water mark \(`lastResponseDate`\) so that re-runs neither miss nor double-count confirmations. The integration handles empty windows as a clean no-op success.

## Callback and confirmation separation

The SupplyOn status notification schema is a pure status acknowledgment: `uuid`, `status`, and an optional list of errors. Real supplier confirmations \(confirmed quantity, date, price, changes requested, or rejections\) are available only through the confirmation pull. This keeps the boundary clean: the push tells you whether SupplyOn accepted the order, and the pull tells you what the supplier decided about the lines.

