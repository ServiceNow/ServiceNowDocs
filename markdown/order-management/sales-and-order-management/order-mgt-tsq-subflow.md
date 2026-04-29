---
title: Process Qualification Request subflow
description: The Process Qualification Request subflow generates a qualification request based on the customer order, sends the request to the third party inventory system, and executes the integration request.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service qualification requests, Managing service orders, Order Management, Use, Sales and Order Management]
---

# Process Qualification Request subflow

The Process Qualification Request subflow generates a qualification request based on the customer order, sends the request to the third party inventory system, and executes the integration request.

## Generate a qualification request

In the first step of the subflow, a TMF-641 compatible payload to be sent to the inventory system is generated. The `serviceQualificationItem` list in the payload consists of the service order information, the hierarchy, and all the characteristics. A sample payload is shown in the following example:

![Infographic displaying the process qualification request subflow. For more information, refer to the text that follows.](../image/order-mgt-tsq-process-subflow.png)

In this example, you can see that the `serviceQualificationItem` has multiple service orders and you can also see the hierarchy or the parent and child relationships between them.

## Execute integration request

This step launches the Order Qualification Request integration request type from the Spoke selector. The payload information specified in the first step of the subflow and the top order line item from the customer order are accepted as inputs. This information is then sent using an API call to the third party inventory system and the response is received either synchronously or asynchronously and Result field is updated in the customer order.

If the response is received asynchronously, the response should be passed to the Process Qualification Response. Along with the result, if the response has additional information related to alternate service proposal or eligibility unavailability reason, this information is updated for the corresponding service order. A sample response is shown here:

![Infographic displaying the sample qualification response. For more information, refer to the text that follows.](../image/order-mgt-tsq-process-response.png)

In this example response, the `qualificationresult` is set to Qualified for all the service orders in the hierarchy and the final `result` is also set to Qualified.

**Parent Topic:**[Service qualification requests](../concept/order-mgt-tsq-about.md)

