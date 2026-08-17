---
title: Integrating Order Management with southbound external systems
description: Submit outbound service order requests to external systems by integrating Order Management with southbound systems. This integration enables automated order fulfillment across your service provider ecosystem.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/order-mgt-integrate-southbound.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Integrating Order Management with southbound external systems

Submit outbound service order requests to external systems by integrating Order Management with southbound systems. This integration enables automated order fulfillment across your service provider ecosystem.

After the decomposition of an order, the Order Management application requires support from external systems. These systems manage the fulfillment life cycle of the order. They include network activation, network configuration, and resource management.

Using this integration, a Communications Service Provider \(CSP\) can do the following tasks:

-   Trigger outbound requests for one or more domain service orders by using the TeleManagement Forum \(TMF\) 641 Open POST order API.
-   Share updates with the external systems about the inflight changes to the existing domain service orders that have outbound requests.
-   Manage the inbound response of the outbound requests for the domain service orders.
-   Manage the errors and exceptions for the outbound requests and inbound responses.

## How the integration works

The integration process for Order Management with the external technical order management systems is as follows:

1.  As the administrator, you activate the Service Order Open API to capture the service order from the customer orders. To learn more, see [TMF641 Service Order Open API- POST](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/service-order-open-api.md).
2.  The integration now begins:

    1.  The order fulfillment manager selects the Create fulfillment request UI action in the domain order table.
    2.  The Service Order Outbound Policy decision table checks the domain order attributes, and the order management system generates the payload for the domain service order.
    3.  The generated payload is sent to the endpoint of the external fulfillment system. For more information on configuring external system endpoints by creating an integration request, see [Workflow Studio flow integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/flow-designer-integrations.md).
    **Note:**

    -   If the domain order is configured as hierarchical, all child service domain orders are sent to the external system configured in the application spoke selector.
    -   If the domain order is configured as non-hierarchical, only individual domain orders are sent to the external system configured in the application spoke selector.
    To learn more about spokes, see [Building spokes using Spoke Generator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/spoke-builder.md).

3.  The service order manager selects the Create Outbound Fulfillment Request UI action on the service order form and the system shares the service order details with the external systems.

    **Note:** The UI action appears if any of the following conditions is met by the system:

    -   No successful outbound request exists for the service domain order yet.
    -   An outbound request exists but the current external fulfillment state of the service domain order is an error.
4.  If the fulfillment request is successful, a response is received from the external system and is captured in the Outbound Request table \(sn\_tmt\_core\_outbound\_request\). To learn more, see [Create outbound requests for service orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-outbound-request.md).

