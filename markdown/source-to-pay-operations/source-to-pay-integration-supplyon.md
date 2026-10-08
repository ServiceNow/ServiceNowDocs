---
title: Purchase Order Management integration with SupplyOn
description: The Purchase Order Management integration with SupplyOn sends purchase orders from your ServiceNow instance to the SupplyOn Supply Chain Collaboration portal. It returns processing status updates and retrieves supplier confirmations into ServiceNow, enabling buyers and suppliers to collaborate on the same order information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/source-to-pay-integration-supplyon.html
release: australia
topic_type: concept
last_updated: "2026-10-08"
reading_time_minutes: 3
breadcrumb: [Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Purchase Order Management integration with SupplyOn

The Purchase Order Management integration with SupplyOn sends purchase orders from your ServiceNow instance to the SupplyOn Supply Chain Collaboration portal. It returns processing status updates and retrieves supplier confirmations into ServiceNow, enabling buyers and suppliers to collaborate on the same order information.

The integration sends purchase orders from your ServiceNow instance to SupplyOn and receives the asynchronous processing outcome for each order. It also pulls supplier line-level confirmations back into the ServiceNow platform.

The integration is delivered as a single scoped application and plugin \(scope `sn_supplyon_po`, Purchase Order Management Integration with SupplyOn\). It builds on two ServiceNow® frameworks that must already be present on the instance: the Source-to-Pay \(S2P\) integration framework and the ERP integration framework.

\[Omitted image "pom-with-supplyon-integration.png"\] Alt text: Diagram of the Purchase Order Management with SupplyOn, described in the following sections.

## Key features

-   Send standard purchase orders to SupplyOn automatically when an order is created, revised, or canceled, including header attachments and line-level cancellation.
-   Correlate the status responses that SupplyOn returns asynchronously to the original purchase order by transaction identifier, including late callbacks.
-   Retrieve line-level supplier confirmations on a schedule, using incremental windowing so that no supplier responses are missed.
-   Track the purchase order status end to end on the staging records, and raise an error task when a failure occurs, without creating duplicate tasks.
-   Tailor the outbound purchase order payload through an extension point, without modifying the shipped code.

## What the integration doesn't send

The integration applies the following send restrictions:

-   Blanket orders — SupplyOn receives only the primary order. For more information, see [SupplyOn integration limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplyon-limitations.md).
-   Service lines \(product type 20\) and handling-fee lines \(30\). For more information, see [SupplyOn outbound purchase order request mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplyon-outbound-request-mapping.md).
-   Line-level attachments — Attachments are sent at header level only. For more information, see [SupplyOn outbound purchase order request mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplyon-outbound-request-mapping.md).

## Integration streams

The integration consists of three streams that together form one closed collaboration loop.

1.  Outbound send \(push, outbound\): When the existing Purchase Order Management flow writes an outbound purchase order staging record routed to SupplyOn, the integration pushes the order to the SupplyOn `POST /purchaseorder` API. The integration then records the returned transaction ID for correlation.
2.  Async status callback \(push, inbound\): The synchronous response from SupplyOn confirms transport receipt only. SupplyOn sends the actual processing outcome later as an asynchronous status notification to a receiver endpoint that the integration hosts. The integration correlates the notification to the outbound staging row by transaction ID and advances the row status.
3.  Confirmation pull \(pull, inbound\): On a schedule, the integration pulls the supplier line-level confirmations through `GET /demandresponse-summaries` and `GET /demandresponse`, then lands them in the inbound confirmation staging tables.

|Stream|Direction|Mechanism|Trigger|SupplyOn API|Lands in|
|------|---------|---------|-------|------------|--------|
|Outbound send|Outbound \(push\)|Flow to subflow to REST step|Outbound staging row reaches New \(10\)|POST /purchaseorder|Transaction ID correlation token on the staging header|
|Async status callback|Inbound \(push\)|REST API asynchronous flow trigger to subflow|SupplyOn posts to the receiver endpoint|SupplyOn calls the integration|Outbound staging header and lines, status 30 or 40|
|Confirmation pull|Inbound \(pull\)|Scheduled ERP-framework subflow to REST steps|SupplyOn schedules the pull \(default approximately 24 hours\), or a job runs manually|GET /demandresponse-summaries then GET /demandresponse|sn\_fcms\_intg\_imp\_po\_confirmation and \_line staging|

## How it works

Flows and subflows provide a plug-and-play experience for the integration scenarios. Integration Hub actions provide the building blocks for the Purchase Order Management subflows and connect to SupplyOn through REST APIs.

The SupplyOn source is modeled as an ERP source and uses the standard purchase order, legal entity, ERP source, integration source, and connection pattern.

When a purchase order is routed to SupplyOn, a flow sends the order to the SupplyOn purchase order API. SupplyOn returns the processing status asynchronously to an endpoint that the integration hosts, and the integration updates the order status. On a schedule, a subflow retrieves the supplier confirmations from SupplyOn.

