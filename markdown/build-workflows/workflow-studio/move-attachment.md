---
title: Move Attachment action
description: Associates a record from the Attachment \[sys\_attachment\] table with a target record. Removes the attachment from any other associated records.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Move Attachment action

Associates a record from the Attachment \[sys\_attachment\] table with a target record. Removes the attachment from any other associated records.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

**Note:** Server-side validation rules, such as data policies, business rules, and dictionary-defined mandatory fields are enforced. UI policies do not apply.

## Fields

|Field|Description|
|-----|-----------|
|Source Attachment Record \[Attachment\]|Select an attachment record from the Attachments \[sys\_attachment\] table.|
|Target Record|Drag a Record data pill from the data panel to attach the **Source Attachment Record** to.|
|Table|Automatically populates with the **Source Record** table.|

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

