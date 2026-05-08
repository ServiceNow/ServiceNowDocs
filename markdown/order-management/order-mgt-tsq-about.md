---
title: Service qualification requests
description: Use the Technical Service Qualification API to evaluate a service request for feasibility and availability before you submit an order for fulfillment in the Order Management application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-10-15"
reading_time_minutes: 3
breadcrumb: [Managing service orders, Order Management, Use, Sales Customer Relationship Management]
---

# Service qualification requests

Use the Technical Service Qualification API to evaluate a service request for feasibility and availability before you submit an order for fulfillment in the Order Management application.

## Service qualification request overview

If orders are submitted without feasibility checks, the order fulfillment process may be delayed and lead to cancellations and order fallouts. When you make feasibility checks a part of the pre-ordering process, the order fulfillment process is more efficient, and unnecessary delays can be avoided.

Let's understand this with an example. A communication service provider wants a broadband service at 3000 Main Street, Santa Clara, CA. As a part of the service delivery process, the service provider determines the technical feasibility of whether a given service can be delivered to their customers. This request then goes to the external inventory systems, which would do a further feasibility check based on the capacity, resources, and other parameters and send a response back to the order management system. The response regarding the qualified response can vary, or if the qualification isn't met, alternate proposals could be provided.

The key capabilities of the Technical Service Qualification process are as follows:

-   Confirm service availability before placing an order and meet customer expectation.
-   Confirm service availability by sending technical service qualification requests.
-   Process and coordinate technical service requests and responses with external inventory systems via APIs.
-   Aligned with the Service Qualification Management TMF 645 Open API.

## Use cases

The Technical Service Qualification process enables the service order managers to perform the following activities:

-   Support the creation of technical service qualification request via open TMF APIs so that they can enable external systems to submit qualification request to ServiceNow system for qualification process.
-   Decompose service qualification request in to underlying services as per the product catalog definition so that they can perform qualification for all underlying services to qualify the parent service.
-   Trigger service qualification requests for both parent and child services to external systems in TFM-aligned standard so that they can support interoperability with external systems to get the feasibility studies performed for service qualification request.

## Qualification process

Customer orders that have the fulfillment type as **Qualify** are captured from third-party customer order management systems through the Technical Service Qualification Open API. You can use this API, which is a ServiceNow implementation of the TMF645 API, to request the qualification of services for:

-   One or more service specifications with characteristics.

    For example, you can make a qualification request to check if Voice over IP \(VoIP\) and Access Service with a download speed of 1 GBPS could be delivered at a specified address.

-   Service specifications that use location information of an existing inventory.

    For example, you can make a qualification request to check if VoIP and 4000 TV services can be delivered at the same location of an existing and active Access Service.

-   Upgrading or downgrading an existing service.

    For example, you can make a qualification request to check if the download speed can be upgraded to 500 Mbps for an existing Access Service.


Order fulfillment managers can review customer orders that are captured through this API and confirm the availability of services before submitting requests for delivery. The requests are then sent to the external inventory system for approval and the customer order is updated with the result.

1.  A qualification requester system sends a qualification request for a customer facing service \(CFS\) into the ServiceNow Order Management system using the TM Forum Open API for Service Qualification \(TMF645\).

    An order is created in Order Management with order type as service and fulfillment type as Qualify.

    Order line items are automatically created based on the service specification relationship.

2.  The system decomposes the order line items into resource facing domain orders \(RFS\) based on catalog definition.
3.  The Order Management system coordinates and processes the technical service qualification request and returns the response to the external inventory system.

-   **[Review and approve service qualification requests](../task/order-mgt-tsq-approve.md)**  
Review and approve customer orders captured through the Technical Service Qualification API.
-   **[Process Qualification Request subflow](../reference/order-mgt-tsq-subflow.md)**  
The Process Qualification Request subflow generates a qualification request based on the customer order, sends the request to the third party inventory system, and executes the integration request.
-   **[Edit the Order Qualification Request](../task/edit-order-mgt-tsq-spoke.md)**  
Use the Order Qualification Request integration request type in the Order Management for Telecommunications application to process the customer order qualification requests and retrieve the results from the external inventory systems.
-   **[Alternate proposal for service orders](order-mgt-tsq-alternate.md)**  
Learn how you can provide alternate proposals if a service qualification isn't met.

**Parent Topic:**[Managing service orders](managing-service-orders.md)

