---
title: Flow actions for fulfillment subflow definition
description: If you define your own fulfillment subflows in Workflow Studio, you can use the standard flow actions that are available in the ServiceNow AI Platform. Each action deals with different aspects of the fulfillment or inventory maintenance that provides some consistency in retrieving and updating data.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure order fulfillment, Order management, Configure, Sales and Order Management]
---

# Flow actions for fulfillment subflow definition

If you define your own fulfillment subflows in Workflow Studio, you can use the standard flow actions that are available in the ServiceNow AI Platform. Each action deals with different aspects of the fulfillment or inventory maintenance that provides some consistency in retrieving and updating data.

The fulfillment flows in the demo data that was shipped with the ServiceNow AI Platform use the flow actions in the following table.

<table id="table_fl5_gx4_v4b"><thead><tr><th>

Action name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Install Base Item and Installed Product

</td><td>

Flow action to create and manage the installed case items in the order fulfillment subflow. The flow action takes the customer order line, configuration item \(CI\), and sold product as input, and creates the install base item and installed product.

</td></tr><tr><td>

Update Configuration Item

</td><td>

Flow action that includes a prescriptive way to update the configuration items order fulfillment subflow. The flow action takes the sold product, product model ID, and comments as input, and updates the corresponding configuration item based on the install base Item.

</td></tr><tr><td>

Get Child Sold Product

</td><td>

Flow action that includes a prescriptive way to retrieve the sold products that are relevant to a specification in a customer order. The flow action takes the specification and the parent sold product as input and retrieves the child sold product from the respective hierarchy. Using this flow action helps the product inventory updates that occur at the end of the fulfillment process.

</td></tr><tr><td>

Get Customer Order Characteristic Value

</td><td>

Flow action that takes the customer order line Item and characteristic as input and returns a characteristic value from the customer order line item. If the characteristic is not present in the customer order line item, it returns the default value for the characteristic from the respective order line item offering.

</td></tr></tbody>
</table>**Parent Topic:**[Configure order fulfillment](../concept/configure-order-fulfillment.md)

**Related topics**  


[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=australia&pubname=australia-application-development&ft:locale=en-US)

[Flows](https://www.servicenow.com/docs/access?context=flows&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

[Create a flow](https://www.servicenow.com/docs/access?context=create-flow&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

