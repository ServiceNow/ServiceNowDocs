---
title: Delete Attachment action
description: Removes one or all attachments associated with a record and deletes the attachment record from the Attachments \[sys\_attachment\] table.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Actions, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Delete Attachment action

Removes one or all attachments associated with a record and deletes the attachment record from the Attachments \[sys\_attachment\] table.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Fields

<table id="table_zmc_z3f_kcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Record

</td><td>

Drag a Record data pill from the data panel to delete one or all attachment records from.

</td></tr><tr><td>

Table

</td><td>

Automatically populates with the **Source Record** table.

</td></tr><tr><td>

Attachment File Name

</td><td>

Enter the name of the attachment file to delete a single attachment associated with the selected record.

 **Note:** If a record has multiple attachments with same name, all matching attachments are deleted.

</td></tr><tr><td>

Delete All Attachments?

</td><td>

Select to delete all attachments associated with the selected record.

</td></tr></tbody>
</table>**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

