---
title: Order Management for providers with Service Exchange
description: The Service Exchange Order Management for Providers application enables service providers to use Order Management to create product offerings and service specifications that Service Exchange consumers can order from service catalogs in their ServiceNow instances. Order agents and fulfillers can then complete the orders and requests on the provider instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrate, Sales Customer Relationship Management]
---

# Order Management for providers with Service Exchange

The Service Exchange Order Management for Providers application enables service providers to use Order Management to create product offerings and service specifications that Service Exchange consumers can order from service catalogs in their ServiceNow instances. Order agents and fulfillers can then complete the orders and requests on the provider instance.

## Overview of Order Management for providers with Service Exchange

The Service Exchange Order Management for Providers application supports the sales order and fulfillment process over Service Exchange. Published product offers and service specifications generate remote record producers \(RRPs\). These remote record producers create the remote catalog items that your consumers can order from the Service Portal on their instance.

The workflow for generating these remote record producers involves these basic steps:

-   Product catalog admin or manager creates the product offerings and service specifications on a provider instance, specifying the distribution channel as Service Exchange and indicating that product offers are sellable items. When the offerings and service specifications are published, remote record producers \(RRPs\) are generated automatically to create the remote catalog items.
-   Service Exchange admin associates consumer criteria to the remote record producers.
-   Service Exchange admin reviews and activates the remote record producers on the provider instance. These remote record producers publish the remote catalog items to the service catalog on a consumer instance.
-   Consumers request services using the remote catalog items on the service portal in their consumer instance. The requests automatically create a provider task for fulfilling the requests on the provider instance.
-   On the provider instance, the order and order lines are created for order managers to approve and agents to fulfill.
-   On the consumer instance, consumers receive updates on the order state and worknote comments from order agents.

## Features

-   Support simple and bundled product offerings with composite specifications.
-   Support service specifications.
-   Support quantity orders for order line items and selection of optional products and services.
-   Synchronize product and service inventory records, which can be viewed by consumers in their instance.
-   Allow consumers to:
    -   Suspend, resume, and disconnect orders
    -   Cancel an order from the consumer instance if the order hasn't reached the point of no return \(PONR\).

## Benefits

-   Automates the generation of remote record producers that publish offerings and service specifications to a remote catalog.
-   Enables faster order fulfillment on the provider instance and improves order accuracy.
-   Facilitates communication by updating comments between the provider and customer instance as well as sharing frequent order status updates.

## Order state mapping

During order processing, note that order status states correspond to certain provider task states.

|Order state|Provider task state|
|-----------|-------------------|
|Draft|Received|
|Submitted|Received|
|Enrichment in progress|Received|
|Enrichment on hold|Received|
|New|Received|
|Acknowledged|Work in Progress|
|Scheduled|Work in Progress|
|Rejected|Awaiting info|
|In progress|Work in progress|
|Revision in progress|Received|
|Awaiting information|Awaiting info|
|On hold|Awaiting info|
|Assessing cancellation|Cancelled|
|Cancellation in progress|Work in Progress|
|Cancelled|Cancelled|
|Completed|Closed|

## Next step

As a Service Exchange admin, review the setup tasks in [Configuring Service Exchange Order Management for Providers](configuring-sb-om.md).

