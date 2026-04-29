---
title: Flow actions for fulfillment subflow definitions
description: If you define your own fulfillment subflows for the Smart Assessment Engine application in Workflow Studio, you can use the standard flow actions that are available in the ServiceNow AI Platform. Each action deals with the different aspects of the fulfillment or inventory maintenance, which can help bring some consistency in how data is retrieved and updated.
locale: en-US
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Flow actions for fulfillment subflow definitions

If you define your own fulfillment subflows for the Smart Assessment Engine application in Workflow Studio, you can use the standard flow actions that are available in the ServiceNow AI Platform. Each action deals with the different aspects of the fulfillment or inventory maintenance, which can help bring some consistency in how data is retrieved and updated.

The fulfillment flows in the demo data that was shipped with the ServiceNow AI Platform use the flow actions in the following table.

<table id="table_fl5_gx4_v4b"><thead><tr><th>

Action name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Trigger Smart Assessment action

</td><td>

Flow action to create and assign an assessment. The flow action takes the customer order line, configuration item \(CI\), and sold product as input, and creates the install base item and installed product.

</td></tr><tr><td>

Update Configuration Item

</td><td>

Flow action that includes a prescriptive way to update the configuration items order fulfillment subflow. The flow action takes the sold product, product model ID, and comments as input, and updates the corresponding configuration item that is based on the install base Item.

</td></tr><tr><td>

Get Child Sold Product

</td><td>

Flow action that includes a prescriptive way to retrieve the sold products that are relevant to a specification in a customer order. The flow action takes the specification and the parent sold product as input and retrieves the child sold product from the respective hierarchy. Using this flow action helps with the product inventory updates that occur at the end of the fulfillment process.

</td></tr><tr><td>

Get Customer Order Characteristic Value

</td><td>

Flow action that takes the customer order line Item and characteristic as input and returns a characteristic value from the customer order line item. If the characteristic isn’t present in the customer order line item, it returns the default value for the characteristic from the respective order line item offering.

</td></tr></tbody>
</table>**Related topics**  


[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=australia&pubname=australia-application-development&ft:locale=en-US)

[Building flows](https://www.servicenow.com/docs/access?context=flows&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

[Create a flow in Workflow Studio](https://www.servicenow.com/docs/access?context=create-flow&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

