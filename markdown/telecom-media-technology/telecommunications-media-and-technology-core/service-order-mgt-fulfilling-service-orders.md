---
title: Creating, reviewing, approving, and fulfilling service orders
description: Service Order Management \(SOM\) is a domain of order management that is responsible for the end-to-end life cycle of service requests. Learn how service orders are captured Order Management, and how your fulfillment managers and agents review, orchestrate, and fulfill them.OM revamp project - This topic has been removed from the SOM bundle on Oct 7, 2025. The viable content has been moved to newer topics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/telecommunications-media-and-technology-core/service-order-mgt-fulfilling-service-orders.html
release: australia
product: Telecommunications, Media and Technology Core
classification: telecommunications-media-and-technology-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Creating, reviewing, approving, and fulfilling service orders

Service Order Management \(SOM\) is a domain of order management that is responsible for the end-to-end life cycle of service requests. Learn how service orders are captured Order Management, and how your fulfillment managers and agents review, orchestrate, and fulfill them.

## Service order capture

Use service orders for the activation of new services or for the post-sales requests for the services that were activated for and delivered to customers at earlier dates. By using this process, you ensure that service orders are correct and handled efficiently throughout the entire fulfillment process.

Most of the service orders that you process are captured from third-party customer order management systems through the Service Order Open API. The Service Order Open API is a ServiceNow implementation of the TM Forum TMF641 Service Ordering Open API specification. To learn more, see Service Order Open API.

## Service order direct entry

You can also use Order Capture as needed to directly enter service orders into the ServiceNow AI Platform.

## Post-capture service order record generation

When you capture or directly enter a service order, a service order record is generated in the ServiceNow AI Platform to manage service order fulfillment. It has one or more associated service order line items that describe a service and the action \(Add, Change, or Disconnect\) that is required to perform for the service. The service order line item also consists of the following:

-   The details of the services that are being added, updated, or deleted.
-   For Add new service activations, the details of the service specification, including the required characteristics and characteristic values.
-   For Change and Disconnect service orders, the details of the service inventory that you're updating or disconnecting.
-   The location and related information such as the customer contact details.

The following diagram provides you with an understanding of how Service Order Management relates to external capture systems.

\[Omitted image "service-order-customer-order-relationship.png"\] Alt text: Infographic showing how customer order management and service order management relate. To learn more, refer to the preceding paragraph.

The following diagram provides you with an understanding of what processing takes place when you capture a service order. The processing flow for service orders is similar to that for customer orders, but with some differences that you will learn about in this section.

\[Omitted image "service-order-fulfillment-workflow.png"\] Alt text: Infographic displaying the customer order review, approval, and decomposition processes. For the text description, refer to the steps that follow.

## Service order review, approval, and decomposition

After you capture a service order, the service order manager selects it in the Service Order Management workspace in Configurable Workspace Home. The service order manager verifies the service order, the service order line items, and the order characteristics, and then approves or rejects the service order.

**Note:** To process service orders, the service order manager uses the same forms that are used to manage customer orders. To learn more about service order management roles and the approval process, see the [Reviewing service orders for fulfillment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/service-order-mgt-review-approve-service-orders.md).

The following diagram details the service order review, approval, decomposition, and completion process.

\[Omitted image "service-order-review-approval-decomp-completion.png"\] Alt text: Infographic displays the service order review, approval, decomposition, and completion. For the text description, refer to the steps that follow.

If the service order manager rejects a service order because the data is incorrect or invalid, the following occurs:

-   The state of the service order moves to Rejected.
-   The service order may require several changes from the service order manager to bring it back to a normal state.

If the service order manager approves a service order, the following process occurs:

-   The **State** field changes to In Progress.
-   Service order decomposition takes place next. Decomposition is based on the service specification, specification relationships, and decomposition rules in the catalog. This process creates all required service and resource orders for each approved service order line item and then triggers the order fulfillment workflow for each domain order.
-   To learn more, see the following:
    -   [Create specification relationships, quantity mapping, and decomposition rules for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/order-mgt-specification-rels.md)
    -   [Approving and fulfilling service orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/service-order-mgt-fulfillment-processing.md)
    -   [Service order decomposition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/service-order-mgt-order-decomposition.md)

## Differences between the pre- and post-approval service orders

Like customer orders, captured service orders also have an ID with a prefix of ORD\(nnn\). The **Order Category** field in the order forms indicates if the order is for a **Product** \(a customer order\) or a **Service** \(a service order\). These labels enable you to identify the type of order.

When you approve a captured service order for fulfillment, the post-approval decomposition process generates actionable service orders and resource orders. You may see a single service order, multiple service orders, and resource orders that are associated with your approved service order.

-   Service orders with a prefix of SO\(nnn\) are referred to as domain orders. These orders, and their related resource orders, with a prefix of RO\(nnn\), must be fulfilled to complete the service order line items on the captured service orders.
-   The resource order manages the resources required to fulfill the services that the customer is requesting.
-   These domain orders manage the fulfillment of the requested service orders.

To learn more, see [Service order decomposition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/service-order-mgt-order-decomposition.md).

## Service order fulfillment tasks

After the decomposition process is complete, order tasks are assigned to a service order agent, who works through the tasks and updates the service order. If there are any remaining order tasks that can't be completed, you can create fallout records for tracking and further research. To learn more, see [Creating, reviewing, approving, and fulfilling service orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/service-order-mgt-fulfilling-service-orders.md).

After all fulfillment tasks are complete, the following actions occur:

-   The **State** field for the service order is set to Closed complete.
-   The **State** field for each of the individual service order line items is set to Completed.
-   The sold product record is updated with the state of Active for Add type service orders or Inactive for disconnect type service orders.
-   All characteristics of the service and resource specifications are updated in the Product Characteristics \[sn\_ind\_tmt\_orm\_product\_characteristics\] table.

**Note:** For more information, see [Review and update the service order fulfillment tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/service-order-mgt-service-order-tasks.md).

**Related topics**  


[Configuring Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/order-mgt-configuring.md)

