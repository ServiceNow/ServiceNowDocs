---
title: Look Up Attachment action
description: Looks up an attachment associated with a record and returns the Attachment Sys ID as a data pill.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Actions, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Look Up Attachment action

Looks up an attachment associated with a record and returns the Attachment Sys ID as a data pill.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your flow needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **File Name**

    Data type: **String**

    The name of the attachment that you want to look up. You can leave this input empty to look up all attachments for a record.

-   **Source Record**

    Data type: **Record**

    Record containing one or more attachments to look up. You can use the [Look Up Record action](lookup-record-flow-designer.md) to find an appropriate source record.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Attachment Sys ID**

    Data type: **String**

    Sys ID of the first matching attachment. You can use the [Look Up Record action](lookup-record-flow-designer.md) to convert this string value into a record output.

-   **Attachment List**

    Data type: **String**

    JSON formatted string containing all attachments that match the look up query. Each matching item is formatted as an object containing the Sys ID, the file name, and the file size in bytes of the attachment. You can use a custom action to parse this object as needed.


## Look up attachments from incident records

![Configuration of the Look Up Attachment action where the File Name input is empty, and the Source Record is mapped to the trigger incident.](../images/example-look-up-attachment-action.png)

This example looks up attachment from incident records so that they can be copied to related problem records. The File Name input is empty to find all attachments in the source record. The Source Record input uses the incident trigger record data pill.

![Execution details for flow step 1 showing a specific Sys ID string returned as output.](../images/example-look-up-attachment-action-execution-details.png)

In this example, the flow execution details show that the trigger incident had only one attachment. The Attachment Sys ID output lists the Sys ID of the attachment record as a string value. The Attachment List output is empty because there was only one attachment associated with the source record.

When the triggering incident record has two or more attachments matching the look up query, the action populates the Attachment List output with a JSON string.

```
[
  {
    "sys_id": "a8008849db7e4210497c1a481396193c",
    "file_name": "Root Cause Analysis",
    "file_size_in_bytes": "48955"
  },
  {
    "sys_id": "c0a298356f102100758ecb512e3ee409",
    "file_name": "Pasted Image",
    "file_size_in_bytes": "97236"
  }
]
```

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

