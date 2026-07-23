---
title: Multi-domain service order orchestration
description: Sales CRM for Telecommunications decomposes a customer order into multiple parallel domain orders. Each order is routed to the appropriate fulfillment domain using catalog-defined subflows and TMF Open API standards. Dependency sequencing coordinates service design, resource provisioning, and field operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/mdso-service-order-orchestration-somt.html
release: australia
topic_type: concept
last_updated: "2025-07-14"
reading_time_minutes: 3
keywords: [multi-domain service order, MDSO, service order orchestration, domain orders, TMF641, TMF716, TMF697, subflow, CFSS, RFSS, CMDB, FSMT]
breadcrumb: [Explore, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Multi-domain service order orchestration

Sales CRM for Telecommunications decomposes a customer order into multiple parallel domain orders. Each order is routed to the appropriate fulfillment domain using catalog-defined subflows and TMF Open API standards. Dependency sequencing coordinates service design, resource provisioning, and field operations.

Multi-domain service order \(MDSO\) orchestration in Sales CRM for Telecommunications decomposes a single customer order into multiple domain orders, each routed to a different fulfillment domain using catalog-defined specification relationships. Each domain order runs an independent subflow a task sequence that triggers an outbound API request, consumes the response, and closes the domain order on completion.

Domain orders run in parallel by default. Where one domain order depends on the output of another, catalog-defined decomposition rules enforce the wait condition automatically. Each domain order routes to its target system using the appropriate TMF Open API standard. The platform manages outbound requests, inbound responses, and error handling within a single orchestration view.

## Benefits

-   A single customer order decomposes into multiple domain orders, each routed to the appropriate fulfillment domain using catalog-defined rules, without manual order construction.
-   Catalog-defined decomposition rules enforce dependency sequencing between domain orders automatically, removing the need for manual coordination between fulfillment teams.
-   Each domain order routes to its target system using the appropriate TMF Open API standard TMF641 removing the need for custom integration adapters per domain.
-   The platform maps characteristic values from external system responses back to the order and inventory records automatically, maintaining data consistency across the order, IBI, and CMDB.
-   The platform creates or updates CMDB configuration items during subflow execution, giving operations teams an accurate view of provisioned services without manual CI updates.
-   Parallel subflow execution across fulfillment domains reduces the total time from order approval to service activation.
-   Fallout management tracks domain orders and tasks that can't complete, enabling targeted resolution without blocking other subflows in the same MDSO.

## Features

|Feature|Description|
|-------|-----------|
|Multi-domain order decomposition|Decomposes a single customer order line item into multiple domain orders, each targeting a different fulfillment domain service design, network provisioning, supply chain, or field operations based on catalog-defined specification relationships.|
|Parallel subflow execution|Runs domain order subflows in parallel where no dependency exists, reducing total fulfillment time. Each subflow manages its own task sequence, outbound API call, and response consumption independently.|
|Catalog-defined dependency sequencing|Enforces wait conditions between domain orders using decomposition rules. Dependent subflows pause until the required domain order completes and returns the necessary output. For example, a Circuit ID or service activation confirmation.|
|Multi-standard TMF routing|Routes domain orders to external systems using TMF641 \(Service Order\) standards within a single orchestration. The outbound standard is determined by the domain order type and the Service Order Outbound Policy decision table.|
|Inbound response consumption|Consumes API responses from external systems including resource identifiers, characteristic values, and work order confirmations and maps them back to the domain order and inventory records automatically.|
|CMDB and IBI integration|Creates or updates CMDB configuration items and Install Base \(IBI\) inventory records during subflow execution. Characteristic values from service design responses are mapped to CI records, maintaining alignment between the order, inventory, and CMDB.|
|Outbound request and error management|Manages outbound request state, inbound response handling, and error conditions for each domain order. Failed or error outbound requests are tracked in the Outbound Request table \[sn\_tmt\_core\_outbound\_request\] for investigation and retry.|
|Fallout management|Creates fallout records for domain order tasks that can't complete. Fallout records are tracked separately from the main fulfillment flow, so other domain orders in the same MDSO continue processing while the fallout is investigated and resolved.|

