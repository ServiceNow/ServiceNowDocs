---
title: Configuring order tasks to respond to inflight revision and cancellation requests
description: Configure your order task records to respond to inflight order changes and cancellation requests using Workflow Studio.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-12-09"
reading_time_minutes: 3
breadcrumb: [Configuring inflight changes, Order management, Configure, Sales Customer Relationship Management]
---

# Configuring order tasks to respond to inflight revision and cancellation requests

Configure your order task records to respond to inflight order changes and cancellation requests using Workflow Studio.

The Create Order Task action contains flow actions that you use to define the order tasks for the inflight order revision and cancellation process.

To learn more about creating a flow and inflight order change processing, see:

-   [Create a flow](https://www.servicenow.com/docs/access?context=create-flow&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)
-   [Managing inflight order changes and cancellation requests](../concept/inflight-order-change-mgt-overview.md)

To see a sample Create Flow action, see the sample Change Cisco Firepower Monitoring system flow, in your demo data, which is installed with the ServiceNow AI Platform.

When you define a Create Order Task action, you can use the standard flow actions that are available in the ServiceNow AI Platform. See the following table for a list of these standard flow actions.

<table id="table_j3k_zk4_fqb"><thead><tr><th>

Create Order Task flow action field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Inflight Change Type**

</td><td>

Flow action to configure the order task to respond to the corresponding change type. You can select one of the following: -   **Contact**

The order task responds to changes made to contact information on an existing order line item.

-   **Price**

The order task responds to changes made to pricing information on an existing order line item.

-   **Quantity**

The order task responds to changes made to quantity information on an existing order line item.

-   **Characteristics**

The order task responds to changes made to characteristics information on an existing order line item.

-   **Related items**

The order task responds to changes made to related items information on an existing order line item.


If the task is not related to any inflight change type, you can leave it empty.

</td></tr><tr><td>

**Inflight Change Option**

</td><td>

Flow action to define if the order task is related in any characteristic changes, or only to a few characteristic changes from the corresponding request definition. You can select one of the following: -   **Not Applicable**

The order task should not respond to any characteristic changes made to the order.

-   **Characteristics From Request Definition**

The order task should respond to the specific set of characteristics that you define in the Request Definition Characteristic \[sn\_ind\_tmt\_orm\_req\_def\_char\] table. These records contain the mappings of the order tasks to specific sets of characteristics.

-   **Any Characteristics**

The order task should respond to any revisions made to the order line item characteristics that are available in the customer or service order.


</td></tr><tr><td>

**Inflight Task Fields \(Order Task\)**

</td><td>

Flow action to attach scripting that designates what redo actions, or field updates, if any, should take place in the order task.It is applied for revisions or cancellation requests for inflight orders that contain the inflight change types and options that are defined in the Inflight Change Type and Inflight Change Option.

</td></tr><tr><td>

**Cancel Task Fields \(Order Task\)**

</td><td>

Flow action to attach scripting that designates what undo actions, or cancellations, if any, should take place in the order task.It is applied for revisions or cancellation requests for inflight orders that contain the inflight change types and options that are defined in the Inflight Change Type and Inflight Change Option flow actions.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring inflight changes](../concept/configure-inflight-order-change-mgt.md)

**Related topics**  


[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

[Flows](https://www.servicenow.com/docs/access?context=flows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)

