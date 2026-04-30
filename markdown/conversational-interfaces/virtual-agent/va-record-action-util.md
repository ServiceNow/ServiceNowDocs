---
title: Record Action utility
description: Use the Record Action utility in a Virtual Agent topic to create or update a ServiceNow record in a table.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Virtual Agent Designer utilities, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Record Action utility

Use the Record Action utility in a Virtual Agent topic to create or update a ServiceNow record in a table.

## Record Action utility properties

<table id="table_jc5_kht_lsb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name that identifies this record action node in the topic flow.

</td></tr><tr><td>

Variable name

</td><td>

Name of the variable that stores the created or updated record values. The variable name is automatically created from the **Node name** property.This option is not visible when the Action Type is **Update a Record**.

</td></tr><tr><td>

Action type

</td><td>

The type of action to perform. Select one of the following:-   **Create a Record**: Creates a new record in the table that you specify.
-   **Update a Record**: Updates an existing record based on the context of the conversation.

</td></tr><tr><td>

Table

</td><td>

If you’re creating a record, select any table that is available in the instance.If you’re updating a record, select a variable for a record that is referenced in the conversation. For example, **User**.

</td></tr><tr><td>

Field

</td><td>

Select one or more fields in the ServiceNow table to be modified. For each field, select a valid value or specify input variables or script variables.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td>

Attach file to record

</td><td>

A low-code method of attaching an image or other file to a record of your choosing.

**Note:** Ensure that you've an uploaded file using the File Picker node before attaching it to a record with the Record Action node. The uploaded file is initially linked to the conversation table. When the incident is created with the uploaded file using the Record Action node, the file is linked to the incident table. It is no longer referenced through the conversation table, but the incident instead.

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Example Record Action utility

![Record Action utility displaying the various basic properties for updating a record.](../images/va-record-action-utility-properties-vancouver.png "Record Action utility basic properties")

**Parent Topic:**[Virtual Agent Designer utilities](va-utilities.md)

