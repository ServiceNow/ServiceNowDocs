---
title: Order capture process in Order Management
description: You can capture, manage, and fulfill the orders from your customers by using APIs, Service Exchange, or direct order capture with the Order Management application.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Order Management, Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
---

# Order capture process in Order Management

You can capture, manage, and fulfill the orders from your customers by using APIs, Service Exchange, or direct order capture with the Order Management application.

The following scenarios represent typical situations in which you capture orders for processing in the ServiceNow AI Platform.

## Scenario 1: Using APIs for order capture and upload

Your current order capture systems can be integrated with ServiceNow instances by using TMF622-based APIs. With this integration, your order capture system can submit requests for products or services, which can then be fulfilled in your ServiceNow instance.

**Note:** To learn more about the ServiceNow - supplied API that is based on the TMF622 Product Ordering API REST Specification, see [Standardized Product Order OpenAPI](https://www.servicenow.com/docs/access?context=tmf622_product_ordering-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

This diagram shows how the TMF622-based API operates within the telecommunications order capture and upload process.

![Infographic showing an API-based workflow scenario for Order Management for Telecommunications in which the fulfillment manager and fufillment agents complete orders from a sales user.](../image/TMF622-API-order-workflow.png "API-based workflow scenario for Order Management")

## Scenario 2: Using Service Exchange for order capture and upload

Your ServiceNow instances can be integrated with the instances of your customers by using Service Exchange. With this integration, you can create and publish product offerings to your customer's instances. Enterprise customers can then submit requests for products or services, which you can then fulfill.

**Note:** For detailed benefits on using the current Service Exchange applications, see [Learn about Service Exchange](https://www.servicenow.com/docs/access?context=service-bridge-v2-benefits&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US).

This diagram shows how Service Exchange operates within the telecommunications order capture and upload process.

![Infographic displaying the service bridge workflow. For the text description, refer to the preceding paragraph.](../image/order-mgt-e2e-2.png "Service Bridge workflow scenario for Order Management")

