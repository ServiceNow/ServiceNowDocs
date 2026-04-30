---
title: Get Catalog Variables action
description: Select variables from multiple template catalog items and variable sets using the Get Catalog Variables action.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Get Catalog Variables action

Select variables from multiple template catalog items and variable sets using the Get Catalog Variables action.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

**Note:** This action only returns the value of catalog variables at the time it was run. If you expect the action to recognize when catalog variable values change, you must build that logic into your flow. For example, use a Wait For Condition action with a changes operator to get catalog variables when a field value changes. If the field value changes, you must add the action in the flow again.

## Inputs

Provide a value for each input that your flow needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **Submitted Request**

    Data type: **Record**

    The requested item record from the Requested Item \[sc\_req\_item\] table for which you want to get catalog variable values.

-   **Template Catalog Items and Variable Sets \[Catalog Items and Variable Sets\]**

    Data type: **Record**

    The Catalog Item \[sc\_cat\_item\] record you want to use to populate the catalog variables slush bucket. This input does not support any data pill values.

-   **Catalog Variables**

    Data type: **Slush Bucket**

    The list of catalog variables whose values you want to get from the requested item record. Each catalog variable that you select is displayed as a data pill in the data pane. You can define flow-specific variables that are displayed in the Available list. To define flow-specific variables, see [Create flow Service Catalog variables](../task/create-flow-catalog-variables.md).


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Catalog Variables**

    Data type: **Varies by catalog variable type**

    The data pane displays a separate data pill for each catalog variable selected from the Catalog Variables input. For a list of supported Service Catalog types, see [Supported Service Catalog variable types](supported-service-catalog-types.md).


## Get catalog variables for hardware items

![Configuration of Get Catalog Variables action](../images/example-get-catalog-variables-action.png)

In this example, a flow runs when someone requests an item from the Service Catalog. The first flow step looks up the Catalog item record of the requested item. The If flow logic uses the category value \(Sys ID\) of the catalog item to determine if request is for an item in the Hardware category. The Get Catalog Variables action uses the trigger record as the Submitted Request input. The Template Catalog Items and Variable Sets input uses the variables provided in the Standard Laptop catalog item. All three available catalog variables are selected and displayed as data pills in the data pane.

![Execution details of the Get Catalog Variables action](../images/example-get-catalog-variables-action-execution-details.png)

The flow execution details show that the Submitted Request links to a request for a standard laptop. Of the three catalog variables, the string variable is empty and the two Boolean variables are false.

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

