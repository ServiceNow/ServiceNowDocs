---
title: Telecommunication Network Inventory workflows in Flow Designer
description: By using the Telecommunications Network Inventory function catalog and subflows, you can access the functions that help you to automate the network inventory's design and assign process.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Telecommunication Network Inventory workflows in Flow Designer

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
</table>To learn more about the network inventory functions, see [Telecommunications Network Inventory function catalog](tni-flow-action.md).

The following example shows the functions that are available in the Workflow Studio action library under the **Network Inventory Advanced** option. You can use these functions to perform the inventory-related data operations.

![Infographic displaying all default options of Network Inventory Advanced.](../image/tni-flow-action-list.png "Network Inventory Function Catalog Location")

You can also use these functions as Workflow Studio actions in the Telecommunications Network Inventory workflow because the Design and Assign is a series of actions. The reusable Workflow Studio actions can automate repetitive work, such as creating a logical connection in the workflow. To learn more about Workflow Studio actions, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## Telecommunications Network Inventory subflows

In Workflow Studio, you can give the inputs and outputs to pass the data to and from the subflow while you’re performing the Design and Assign process. If necessary, you can add more fields in the subflows. To learn more about working with the subflows, see [Building subflows](https://www.servicenow.com/docs/access?context=subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US). To learn more about the Workflow Studio, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

The Telecommunications Network Inventory application has the following subflows:

-   **Logical Connection Creation**

    Creates a logical connection record in the Telecommunications Network Inventory application based on the input that you receive when you instantiate an inventory. To learn more, see [Logical Connection Creation subflow](logical-connection-creation-subflow.md).

-   **Physical Connection Creation**

    Creates a physical connection record in the Telecommunications Network Inventory application based on the input that you receive when you instantiate an inventory. To learn more, see [Physical Connection Creation subflow](physical-connection-creation-subflow.md).


The following example shows the subflows that are available in the Workflow Studio action library under the **Network Inventory Advanced** option. You can use these functions to perform the inventory-related data operations.

![Infographic displaying all default options of network inventory subflows in the Flow Designer action library.](../image/tni-subflow.png "Network Inventory Subflow Location")

**Related topics**  


[Telecommunications Network Inventory function catalog](tni-flow-action.md)

[Telecommunications Network Inventory subflows](subflow.md)

