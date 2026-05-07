---
title: Asynchronous order processing for large customer and consumer orders
description: Asynchronous order processing handles high-volume enterprise and consumer orders without waiting for immediate processing, improving system performance for communications service providers \(CSP\) using Order Management.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-23"
reading_time_minutes: 4
breadcrumb: [Order management, Configure, Sales Customer Relationship Management]
---

# Asynchronous order processing for large customer and consumer orders

Asynchronous order processing handles high-volume enterprise and consumer orders without waiting for immediate processing, improving system performance for communications service providers \(CSP\) using Order Management.

## Overview of asynchronous order processing

CSPs support both enterprise customers and consumers. Enterprise customers typically place large multi-site orders, while consumers place high-volume orders. Asynchronous order processing enables you to create bulk or high-volume orders without waiting for each order to be processed immediately, improving efficiency and system performance.

When you submit an asynchronous order request, the system responds with a `202 Accepted` status and an order ID. This indicates the order is received for processing but not yet created. This differs from synchronous processing, which returns `201 Created` when the order is immediately created.

If you have a Telecommunications Service Management subscription, you can use the Product Order Open API to receive an order in the Order Management application. Order processing goes through three stages:

-   Order validation
-   Order ingestion
-   Order creation

## How synchronous order processing works

With synchronous order processing, an order is received in the Order Management application through the API. Then, the order records are simultaneously created in a customer order table after the order validation.

As an administrator, you can activate or deactivate the order validation for synchronous order processing by setting the **create\_product\_order\_validation\_sync** and **create\_service\_order\_validation\_sync** system properties to True \(Default\) or False in the ServiceNow AI Platform. Synchronous order processing takes longer than asynchronous order processing when it comes to creating a large number of customer order records.

## How asynchronous order processing works

In asynchronous order processing, high-volume orders or large numbers of order payloads are received through the Product Order Open API in the Order Management application from external Configure, Price, and Quote \(CPQ\) systems.

The order details are first validated and then inserted into the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table. If validation errors occur, an error message is returned in the response. The actual order creation happens later when a scheduled job processes entries from this queue, allowing for bulk or delayed processing.

This validation is managed by the **create\_product\_order\_validation\_async** system property for product orders and the **create\_service\_order\_validation\_async** system property for service orders. These properties control the validation in the asynchronous processing of orders before the orders are inserted into the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table. The default value is set to True.

When the order details are successfully validated, a scheduled job runs to pick up the records from the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table and then creates entries in the customer order table as shown in the following diagram.

![Workflow showing how an asynchronous order is created. For text description, refer to the steps that follow.](../image/asynchronous-order-processing.svg "Asynchronous order processing workflow")

The asynchronous order processing follows these steps:

1.  You must activate the Product Order Open API. The new parameter mode enables the API to process orders synchronously or asynchronously. For more information about the API, see [Product Order Open API](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&version=australia&pubname=australia-api-reference&ft:locale=en-US).
2.  After you receive high-volume orders or large numbers of order payloads through the Product Order Open API in asynchronous mode, the system responds with a `202 Accepted` status and an order ID. The order details are validated first and include the product offering, order line items, order specifications, order line item characteristics, and the specification relationship of order line items. For more information on how the validation works, see [Validating your orders through asynchronous order processing](asynchronous-order-validation.md).
3.  After the validation of the order details is complete, an entry for each order with a unique record ID is created in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table. To learn more about how the order entries are created, see [Create order entries manually during the asynchronous order processing](creation-of-order-entries-in-the-asynchronous-order-processing.md).
4.  When all the orders are captured in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table, a scheduled job runs to create the customer orders for the records in the New state. You can also manually trigger order creation from the Inbound Queue module by selecting the **Create Order** button, bypassing the wait for the automated job. After processing, you can verify the created orders in the customer orders section. To learn how a scheduled job creates orders, see [Configure a scheduled job for asynchronous order creation](../task/running-scheduled-job.md).

-   **[Validating your orders through asynchronous order processing](asynchronous-order-validation.md)**  
You can validate your orders before the order records are created in the customer order table during asynchronous order processing in the ServiceNow® Order Management application.
-   **[Create order entries manually during the asynchronous order processing](creation-of-order-entries-in-the-asynchronous-order-processing.md)**  
Skip the scheduled job and create order entries manually in the Order Management application for asynchronous order requests.
-   **[Configure a scheduled job for asynchronous order creation](../task/running-scheduled-job.md)**  
Run a scheduled job in the Order Management application to create a customer order from the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table.

**Parent Topic:**[Configuring Order Management](order-mgt-configuring.md)

**Related topics**  


[Inbound request states](../reference/inbound-queue-states.md)

