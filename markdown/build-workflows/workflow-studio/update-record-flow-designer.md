---
title: Update Record action
description: Update an existing record in a table. You can dynamically add and configure fields for the record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/update-record-flow-designer.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Actions, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Update Record action

Update an existing record in a table. You can dynamically add and configure fields for the record.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your flow needs. To add dynamic values, you can also drag pills from the Data panel or select them from the pill picker.

-   **Record**

    Data type: **Record**

    The record to be updated. Drag-and-drop a record data pill or use the data pill picker to select a record.

    **Warning:** When using script to select a record, always add a condition to check for a matching record. Some GlideRecord methods return a list of records whenever the method query produces no results. Without a condition check, the action may update all records in a table. For example, this script uses an If condition to verify that a record exists. If the record exists, it returns a Sys ID value. If no record exists, it returns a null result.

    ```
    var configurationItem = new GlideRecord('cmdb_ci');
    if (configurationItem.get(fd_data.trigger.cmdb_ci.sys_id))
    return configurationItem;
    else
    return null;
    
    ```

-   **Table**

    Data type: **Table Name**

    The table associated with the record to update.

-   **Field Values**

    Data type: **Template Value**

    The values of fields in the record to be updated. Select **Add field value** to display options to select a field and set a value. For example, to set the short description to a certain value, select **Short description** and set the desired value.

    If adding the action to a subflow, you can [Create a template value input](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/template-value.md).


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Record**

    Data type: **Record**

    The record that was updated.

-   **Table Name**

    Data type: **Table Name**

    The table associated with the updated record.


## Update trigger record

\[Omitted image "example-update-record-action.png"\] Alt text: Sample flow containing an Update record action

In this example, the Update Record action updates values provided by the trigger problem record. The action updates both the Additional comments and Assignment group fields of a problem record.

**Parent Topic:**[Workflow Studio actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-actions.md)

