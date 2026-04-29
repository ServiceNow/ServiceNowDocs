---
title: Get Attachments on Record action
description: Access the list and count of the attachments associated with the provided source record as data pills in a flow. Use flow logic or scripting to process each attachment in the list of the attachments that the action returns.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Actions, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Get Attachments on Record action

Access the list and count of the attachments associated with the provided source record as data pills in a flow. Use flow logic or scripting to process each attachment in the list of the attachments that the action returns.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your flow needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **File name**

    Data type: **String**

    Search string containing a partial or entire file name of an attachment file. You can use this input as a query filter to find one or more attachments that have the listed file name. If you leave this input empty, the action returns all attachments associated with the source record.

-   **Source Record**

    Data type: **Document ID**

    Record that you want to get attachments for. Typically this input uses a data pill from the data panel.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Attachment List**

    Data type: **Records**

    Sys ID values of Attachment records found.

-   **Count**

    Data type: **Integer**

    Number of attachment records.


## Get attachments from an incident record

![Flow with a create record trigger that runs the Get attachments on record action](../images/get-attachments-on-record.png "Inputs used for Get attachments on record")

This example illustrates getting all attachments from an incident record. Leaving the File name input empty returns all attachment records.

![Execution details of getting attachments from an incident record](../images/get-attachments-on-record-execution-details.png "Execution details for get attachment on record")

In this example, the incident record contained two attachments.

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

