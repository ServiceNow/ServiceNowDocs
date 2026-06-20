---
title: Look Up Record action
description: Look up a record from any table based on defined conditions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/build-workflows/workflow-studio/lookup-record-flow-designer.html
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Look Up Record action

Look up a record from any table based on defined conditions.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag pills from the Data panel or select them from the pill picker.

-   **Table**

    Data type: **Table Name**

    Table name containing the records you want to look up.

-   **Conditions**

    Data type: **Conditions**

    Field names and field values that you want to use to search for records. To use an inline script to specify conditions, consider using the GlideRecord and GlideQueryCondition classes to build your query. See  and .

-   **Order by**

    Data type: **Field Name**

    Field you want to use to sort results.

-   **Sort Type**

    Data type: **Choice**

    Option to sort alphabetically in ascending or descending order.

-   **If multiple records are found**

    Data type: **Choice**

    Option to determine what information to return when more than one record matches the defined conditions.

    -   Return only the first record
    -   Fail the step
-   **Don't fail on error**

    Data type: **Boolean**

    Option whether to fail the flow when the lookup can't find a record.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Record**

    Data type: **Record**

    Record found based on the conditions you specified in the **Conditions** input.

-   **Table**

    Data type: **Table**

    Name of the table associated with the returned record.

-   **Status**

    Data type: **Choice**

    0 if a record was found successfully, and 1 if there was an error.

-   **Error Message**

    Data type: **String**

    Message containing details about why the record could not be found.

    **Note:** This output's value is only populated if the **Status** output's value is 1.


## Example

\[Omitted image "flow-example-look-up-record.png"\] Alt text: Example Look Up Record action in a flow.

**Parent Topic:**[Workflow Studio actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/build-workflows/workflow-studio/flow-actions.md)

