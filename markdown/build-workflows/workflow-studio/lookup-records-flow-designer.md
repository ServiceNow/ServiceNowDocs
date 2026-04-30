---
title: Look Up Records action
description: Look up multiple records on any table using defined conditions.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Look Up Records action

Look up multiple records on any table using defined conditions.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your flow needs. To add dynamic values, you can also drag pills from the Data panel or select them from the pill picker.

-   **Table**

    Data type: **Table Name**

    Table name containing the records you want to look up.

-   **Conditions**

    Data type: **Conditions**

    Field names and field values that you want to use to search for records. To use an inline script to specify conditions, consider using the GlideRecord and GlideQueryCondition classes to build your query. See [GlideRecord - Global](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) and [GlideQueryCondition - Global](https://www.servicenow.com/docs/access?context=c_GlideQueryConditionAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

-   **Order by**

    Data type: **Field Name**

    Field you want to use to sort results.

-   **Sort Type**

    Data type: **Choice**

    Option to sort alphabetically in ascending or descending order.

-   **Max Results**

    Data type: **Integer**

    The maximum number of record results the action can return.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Records**

    Data type: **Records**

    List of record Sys IDs found based on the lookup criteria that you provided. For more information, see [Records.\[Table\] data type](records-data.md).

-   **Table**

    Data type: **Table Name**

    Table that contains the list of records.

-   **Count**

    Data type: **Integer**

    Number of records that the action returned.


## General guidelines

Use these general guidelines when working with the Look Up Records action.

-   **Process records with For Each flow logic**

    Use For Each flow logic to iterate through a list of records. For more information about using For Each flow logic, see [For Each flow logic](../concept/flow-logic-for-each.md).

-   **Set Max Results to improve performance**

    Set the Max Results input to 1000 records or lower to improve the performance of your flow. The more records that the system has to look up, the more system resources it takes to identify and process them.

-   **Use conditions to filter records**

    Use conditions to limit the number of records the action returns. The more specific conditions that you can provide, the better performance your flow has.


## Look up configuration items assigned to a change request user

![Configuration of Look Up Records action](../images/example-look-up-records-action.png)

In this example, the flow starts when an emergency change request is opened in the Network category. The Look Up Records action uses the Configuration Item \[cmdb\_ci\] table as the Table input. The Conditions input looks for configuration items assigned to the requester of the change request. The Order by input uses the Name field to perform an ascending alphabetical type sort.

![Execution details of Look Up Records action](../images/example-look-up-records-action-execution-details.png)

In the execution details, the Count output shows three configuration items that are assigned to the requester of the change request. The Records output shows the configuration items by name in the execution details page, but the data pill contains a series of Sys ID values. The Table output is the Configuration Item \[cmdb\_ci\] table.

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

