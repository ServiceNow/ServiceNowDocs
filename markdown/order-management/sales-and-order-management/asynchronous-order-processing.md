---
title: Asynchronous order processing for large customer and consumer orders
description: If you're an administrator for a communications service provider \(CSP\), you can support a high volume of enterprise, multi-site customer orders and consumer orders by using asynchronous order processing in the ServiceNow Order Management application.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Order Management, Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
---

# Asynchronous order processing for large customer and consumer orders

If you're an administrator for a communications service provider \(CSP\), you can support a high volume of enterprise, multi-site customer orders and consumer orders by using asynchronous order processing in the ServiceNow® Order Management application.

## Overview

CSPs support both enterprise customers and consumers. Usually, the orders from enterprise customers are large multi-site orders and the orders from consumers are high volume.

If you have a Telecommunications Service Management subscription, you can use the Product Order Open API to receive an order in the ServiceNow® Order Management application. Order processing goes through three stages:

-   Order validation
-   Order ingestion
-   Order creation

## How synchronous order processing works

With synchronous order processing, an order is received in the Order Management application through the API. Then, the order records are simultaneously created in a customer order table after the order validation.

As an administrator, you can activate or deactivate the order validation for synchronous order processing by setting the **create\_product\_order\_validation\_sync** and **create\_service\_order\_validation\_sync** system properties to True \(Default\) or False in the ServiceNow AI Platform. Synchronous order processing takes longer than asynchronous order processing when it comes to creating a large number of customer order records.

## How asynchronous order processing works

In asynchronous order processing, a high volume of orders or a large number of order payloads are received through the Product Order Open API \(Scripted Rest End Point\) in the Order Management application from the external Configure, Price, and Quote \(CPQ\) systems. The order details are first validated and are then inserted into the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table. If there are any validation errors, an error message is returned in the response.

This validation is managed by the **create\_product\_order\_validation\_async** system property for product orders and the **create\_service\_order\_validation\_async** system property for service orders. These properties control the validation in the asynchronous processing of orders before the orders are inserted into the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table. The default value is set to True.

When the order details are successfully validated, a scheduled job runs to pick up the records from the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table and then creates entries in the customer order table as shown in the following diagram.

![Workflow showing how an asynchronous order is created. For text description, refer to the steps that follow.](../image/asynchronous-order-processing.png "Asynchronous order processing workflow")

The asynchronous order processing follows these steps:

1.  You must activate the Product Order Open API. The new parameter mode enables the API to process the orders synchronously or asynchronously. For more information about the API, see [Product Order Open API](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).
2.  After you receive a high volume of orders or a large number of the order payloads through the Product Order Open API in the async mode, the order details are first validated. The order details include the product offering, order line items, order specifications, order line items characteristics, and the specification relationship of order line items.
3.  After the validation of the order details is complete, an entry for each order with a unique record ID is created in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table. The following diagram shows how the inbound queue state model works.

    ![Model for Inbound Queue State process. For text description, refer to step 3 in this section.](../image/asynchronous-order-processing-inbound-queue.png "Inbound Queue state model")

4.  When all the orders are captured in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table, a scheduled job runs to create the customer orders for the records in the New state.

