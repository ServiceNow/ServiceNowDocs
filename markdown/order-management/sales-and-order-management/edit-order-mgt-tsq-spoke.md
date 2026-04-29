---
title: Edit the Order Qualification Request
description: Use the Order Qualification Request integration request type in the Order Management for Telecommunications application to process the customer order qualification requests and retrieve the results from the external inventory systems.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service qualification requests, Managing service orders, Order Management, Use, Sales and Order Management]
---

# Edit the Order Qualification Request

Use the Order Qualification Request integration request type in the Order Management for Telecommunications application to process the customer order qualification requests and retrieve the results from the external inventory systems.

## Before you begin

Role required: admin

## About this task

The Order Qualification Request type is used to integrate order management with third-party inventory systems. You can specify the following information:

-   Integration request inputs: Inputs for the customer order qualification request which include the top order line item and payload details.
-   Integration request definition: Definition for the condition and the subflow that invokes the API call to the third-party inventory system.

## Procedure

1.  Navigate to **All** &gt; **Spoke selector** &gt; **Request type**.

2.  Click the **Order Qualification Request** integration request type.

    In the Order Qualification Request integration request type page, you can see the Demo Order Qualification Implementation request definition listed under the Integration request definitions tab. This is a sample request definition that invokes the Demo Order Qualification \(Mock Response\) subflow, simulates the response from a third-party inventory system, and updates the qualification request.

    You must add a new request definition, specify the conditions and create a subflow that you can use to invoke the API call to the third-party inventory system. You can create one or more request definitions depending on the number of external systems being used.

3.  Click **New** to add a new request definition.

    **Note:** To add a new request definition, you must be in the Order Management for Telecom, Media and Tech scope.

4.  Enter the name for the request definition and specify the conditions.

5.  In the Request adapter field, select the subflow that will communicate with the third-party system to update the customer order and click **Submit**.

    -   Each request type can have multiple request definitions. For example, if you have multiple inventory systems or vendors, depending on the system you want to invoke, you can add multiple request definitions for each system. You must create a separate spoke to interact with each vendor or third-party system, create a flow in the spoke, and point the request adapter to this flow.
    -   For more information on how to create a spoke, see [Spokes](https://www.servicenow.com/docs/access?context=spokes&version=australia&pubname=australia-build-workflows&ft:locale=en-US). As shown in the demo subflow, ensure that the response from the third-party system passed to the Process Qualification Response block.
    -   When the Process Qualification Request subflow is invoked, the response from the third-party inventory system is received either synchronously or asynchronously, and the Result is updated in the customer order.

**Parent Topic:**[Service qualification requests](../concept/order-mgt-tsq-about.md)

