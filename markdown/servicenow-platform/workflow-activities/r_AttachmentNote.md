---
title: Attachment Note workflow activity
description: The Attachment Note activity adds an attachment to the current record.
locale: en-US
release: australia
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Task workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Attachment Note workflow activity

The **Attachment Note** activity adds an attachment to the current record.

**Note:** This activity is only available when the workflow runs on a table that extends Task.

This activity allows the use of irregular HTML tags to reference attachments, specifically the `[code]` tag. Entries in a journal field that use irregular HTML do not work if the **glide.ui.allow\_deep\_html\_validation** property is true. This property is set to false by default.

**Note:** Task activities run as the user whose actions complete the task the workflow was waiting for and advances the workflow.

## Results

**Finished:** the activity added the attachment to the record.

## Input variables

The following variables determine the behavior of the activity.

<table id="table_tdw_3kc_sp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="subhead" colspan="2">

General

</td></tr><tr><td>

Field

</td><td>

When this activity runs, it makes a note on the current record that a file has been attached. Specify the field on the current record in which you want this note to appear. The options are:-   **none** \(defaults to Work Notes\)
-   **Additional Comments**
-   **Work notes**

</td></tr><tr><td class="subhead" colspan="2">

Attachment note information

</td></tr><tr><td>

Attachment Name

</td><td>

When this activity runs, it creates a .txt file with the name you specify in this field.

</td></tr><tr><td>

Attachment Data

</td><td>

The content of the .txt file attachment. It can be in plain text or use variables to extract specific data from a table.

</td></tr></tbody>
</table>