---
title: Look up email attachments action
description: Look up files that are attached to an email so that you can perform an action on the files.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Look up email attachments action

Look up files that are attached to an email so that you can perform an action on the files.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Fields

|Field|Description|
|-----|-----------|
|Email record \[Email\]|Record from the Email \[sys\_email\] table. For example, select the email record from the flow trigger. After you select an email record, the related Email Attachment \[sys\_email\_attachment\] record and its fields become available as data pills.|

## Output

This action generates a list of Email Attachment \[sys\_email\_attachment\] records, which list the attachments that are associated with a given email record. To perform an action on an attachment, add flow logic that runs for each Attachment pill under the Email Attachment Record pill. For more information, see [For each flow logic](../concept/flow-logic-for-each.md).

## Example

In the following example, a process owner adds the Look up email attachments action under an inbound email trigger. In the **Email record \[Email\]** field, the user selects to look up files that are attached to the email that triggered the flow.

![Email attachments action in a flow](../images/lookup-email-attach-example.png "Email attachments action in a flow")

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

