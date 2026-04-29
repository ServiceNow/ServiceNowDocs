---
title: Look Up Records step
description: Look up multiple records on any table using defined conditions.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Steps, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Look Up Records step

Look up multiple records on any table using defined conditions.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag pills from the Data panel or select them from the pill picker.

-   **Table**

    Data type: **Table Name**

    Table name containing the records you want to look up.

-   **Conditions**

    Data type: **Conditions**

    Field names and field values that you want to use to search for records. To use an inline script to specify conditions, consider using the GlideRecord and GlideQueryCondition classes to build your query. See [GlideRecord - Global](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US) and [GlideQueryCondition - Global](https://www.servicenow.com/docs/access?context=c_GlideQueryConditionAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).

-   **Order by**

    Data type: **Field Name**

    Field you want to use to sort results.

-   **Sort Type**

    Data type: **Choice**

    Option to sort alphabetically in ascending or descending order.

-   **Max Results**

    Data type: **Integer**

    The maximum number of record results the step can return.


## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


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

    Number of records that the step returned.


## General guidelines

Use these general guidelines when working with the Look Up Records action.

-   **Process records with For Each flow logic**

    Use For Each flow logic to iterate through a list of records. For more information about using For Each flow logic, see [For Each flow logic](../concept/flow-logic-for-each.md). Alternatively, you can use a Script step to process a list of records within a custom action.

-   **Set Max Results to improve performance**

    Set the Max Results input to 1000 records or lower to improve the performance of your action. The more records that the system has to look up, the more system resources it takes to identify and process them.

-   **Use conditions to filter records**

    Use conditions to limit the number of records the step returns. The more specific conditions that you can provide, the better performance your action has.


## Example

![Example Look Up Records step in an action.](../images/look-up-records-example.png)

**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

