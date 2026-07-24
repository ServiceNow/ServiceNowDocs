---
title: Workflows in Flow Designer
description: By using the Telecommunications Network Inventory function catalog and subflows, you can access the functions that help you to automate the network inventory's design and assign process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/telecommunication-network-inventory-workflows-flow-designer.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Telecommunications Network Inventory]
---

# Workflows in Flow Designer

By using the Telecommunications Network Inventory function catalog and subflows, you can access the functions that help you to automate the network inventory's design and assign process.

## Telecommunications Network Inventory function catalog

You can use the Telecommunications Network Inventory functions to create, update, and retrieve a configuration item \(CI\) while you’re performing the Design and Assign process. For example, you can do the following actions:

-   Create telco equipment
-   Add an interface card

The following table lists the Telecommunications Network Inventory functions that are categorized by their functionality.

<table id="table_nkk_1h1_yyb"><thead><tr><th>

Function Type

</th><th>

Function Name

</th></tr></thead><tbody><tr><td>

Create

</td><td>

-   TNI Create CI From Template
-   Create Logical Connection
-   Create Logical Interface
-   Create Physical Connection
-   Path Search

</td></tr><tr><td>

Read

</td><td>

-   Allocate Free Number
-   Get Interface Summery
-   Lookup Next Hub

</td></tr><tr><td>

Update

</td><td>

Cascade Update

</td></tr><tr><td>

Helper function

</td><td>

-   Split String
-   Get Index From Array

</td></tr></tbody>
</table>To learn more about the network inventory functions, see [Telecommunications Network Inventory function catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/tni-flow-action.md).

The following example shows the functions that are available in the Workflow Studio action library under the **Network Inventory Advanced** option. You can use these functions to perform the inventory-related data operations.

\[Omitted image "tni-flow-action-list.png"\] Alt text: Infographic displaying all default options of Network Inventory Advanced.

You can also use these functions as Workflow Studio actions in the Telecommunications Network Inventory workflow because the Design and Assign is a series of actions. The reusable Workflow Studio actions can automate repetitive work, such as creating a logical connection in the workflow. To learn more about Workflow Studio actions, see [Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/flow-designer.md).

## Telecommunications Network Inventory subflows

In Workflow Studio, you can give the inputs and outputs to pass the data to and from the subflow while you’re performing the Design and Assign process. If necessary, you can add more fields in the subflows. To learn more about working with the subflows, see [Building subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/subflows.md). To learn more about the Workflow Studio, see [Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/flow-designer.md).

The Telecommunications Network Inventory application has the following subflows:

-   **Logical Connection Creation**

    Creates a logical connection record in the Telecommunications Network Inventory application based on the input that you receive when you instantiate an inventory. To learn more, see [Logical Connection Creation subflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/logical-connection-creation-subflow.md).

-   **Physical Connection Creation**

    Creates a physical connection record in the Telecommunications Network Inventory application based on the input that you receive when you instantiate an inventory. To learn more, see [Physical connection creation subflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/physical-connection-creation-subflow.md).


The following example shows the subflows that are available in the Workflow Studio action library under the **Network Inventory Advanced** option. You can use these functions to perform the inventory-related data operations.

\[Omitted image "tni-subflow.png"\] Alt text: Infographic displaying all default options of network inventory subflows in the Flow Designer action library.

**Related topics**  


[Telecommunications Network Inventory function catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/tni-flow-action.md)

[Telecommunications Network Inventory subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/subflow.md)

