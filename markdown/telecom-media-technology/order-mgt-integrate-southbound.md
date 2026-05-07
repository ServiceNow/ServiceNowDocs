---
title: Integrating Order Management with southbound external systems
description: If you have a Telecommunications Service Management subscription, you can submit outbound service order requests to various external systems by integrating the Order Management application with the external southbound systems.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Integrating Order Management with southbound external systems

If you have a Telecommunications Service Management subscription, you can submit outbound service order requests to various external systems by integrating the Order Management application with the external southbound systems.

After the decomposition of an order, the Order Management application requires the support from external network activation, network configuration, and resource management systems to manage the fulfillment life cycle of the order.

Using this integration, a Communications Service Provider \(CSP\) can do the following tasks:

-   Trigger outbound requests for one or more domain service orders by using the TeleManagement Forum \(TMF\) 641 Open POST order API.
-   Share updates with the external systems about the inflight changes to the existing domain service orders that have outbound requests.
-   Manage the inbound response of the outbound requests for the domain service orders.
-   Manage the errors and exceptions for the outbound requests and inbound responses.

## How the integration works

The integration process for Order Management with the external technical order management systems is as follows:

1.  As the administrator, you activate the Service Order Open API to capture the service order from the customer orders. To learn more, see [TMF641 Service Order Open API- POST](https://www.servicenow.com/docs/access?context=service-order-open-api&version=australia&pubname=australia-api-reference&section=serviceorder-POST-order&ft:locale=en-US).
2.  The integration now begins:

    1.  The order fulfillment manager selects the Create fulfillment request UI action in the domain order table.
    2.  The Service Order Outbound Policy decision table checks the domain order attributes, and the order management system generates the payload for the domain service order.
    3.  The generated payload is sent to the endpoint of the external fulfillment system. For more information on configuring external system endpoints by creating an integration request, see [Workflow Studio flow integrations](https://www.servicenow.com/docs/access?context=flow-designer-integrations&version=australia&pubname=australia-build-workflows&ft:locale=en-US).
    **Note:**

    -   If the domain order is configured as hierarchical in the decision table, the system sends all the child service domain orders in the hierarchy to the external system that is configured in the application spoke selector.
    -   If the domain order is configured as non-hierarchical in the decision table, the systems send only the individual domain order to the external system that is configured in the application spoke selector.
    To learn more about spokes, see [Building spokes using Spoke Generator](https://www.servicenow.com/docs/access?context=spoke-builder&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

3.  The service order manager selects the Create Outbound Fulfillment Request UI action on the service order form and the system shares the service order details with the external systems.

    **Note:** The UI action appears if any of the following conditions is met by the system:

    -   No successful outbound request exists for the service domain order yet.
    -   An outbound request exists but the current external fulfillment state of the service domain order is an error.
4.  If the fulfillment request is successful, a response is received from the external system and is captured in the Outbound Request table \(sn\_tmt\_core\_outbound\_request\). To learn more, see [Create outbound requests for service orders](https://www.servicenow.com/docs/access?context=order-mgt-outbound-request&version=australia&pubname=australia-order-management&ft:locale=en-US).

