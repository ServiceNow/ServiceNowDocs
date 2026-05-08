---
title: Move Email Attachments to Record action
description: Move attachments from an email to a record so that the files are available to your users when they view the record.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Actions, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Move Email Attachments to Record action

Move attachments from an email to a record so that the files are available to your users when they view the record.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your flow needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **Email Record**

    Data type: **Record**

    Email \[sys\_mail\] record containing one or more attachments that you want to move. You must enable email receiving to have valid email records. For more information about email services and setup, see Email Administration.

-   **Target Record**

    Data type: **Record**

    Record to which you want to move one or more attachments. You can use the [Look Up Record action](lookup-record-flow-designer.md) to find an appropriate target record.


## Output

This action has no outputs. Instead it updates the source Email Attachment \[sys\_email\_attachment\] record to move any attachments to the target record.

## Move email attachments to incident record

![Move Email Attachments to Record configuration](../images/example-move-email-attachments-to-record.png)

This example extends the sample flow for inbound email flow handling to add the Move Email Attachments to Record action. This examples assumes that you have previously set up your instance to receive emails, and that there are one or more email records with attachments. The Email Record input uses the data pill for the email that triggers the flow. The Target Record input uses the data pill for the incident record that was updated in flow step 1.

![Execution details of Move Email Attachments to Record](../images/example-move-email-attachments-to-record-execution-details.png)

In this example, the Email Record was a received email that contained multiple attachments. The runtime value is the Sys ID reference to the received email record. The Target record was incident record INC0010220, which was updated by the email in flow step 1.

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

