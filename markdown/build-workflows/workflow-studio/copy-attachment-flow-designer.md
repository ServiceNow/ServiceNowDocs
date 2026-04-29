---
title: Copy Attachment action
description: Copies an attachment from the Attachments \[sys\_attachment\] table to a target record.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Actions, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Copy Attachment action

Copies an attachment from the Attachments \[sys\_attachment\] table to a target record.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your flow needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **Source Attachment Record \[Attachment\]**

    Data type: **Record**

    Attachment record containing the attachment you want to copy. You can either manually select a record from the Attachment \[sys\_attachment\] table or look up the attachment record. You can use the [Look Up Attachment action](lookup-attachment-flow-designer.md) to provide one or more Sys ID values of attachments with a given file name in a specific source record. If you use the Look Up Attachment action, you must also use a [Look Up Record action](lookup-record-flow-designer.md) to convert the Sys ID value returned by the Look Up Attachment action into a usable record data pill. See the example section for an illustration of converting the Sys ID output of the Look Up Attachment action into a record data pill.

-   **Target Record**

    Data type: **Record**

    Record where you want to add a copy of the attachment. You can use the [Look Up Record action](lookup-record-flow-designer.md) to find an appropriate target record.

-   **Table**

    Data type: **Table Name**

    Table containing the target record. This system sets this input value for you if you select a data pill for the target record.


## Outputs

This action has no outputs.

## Copy attachments from incident records to a problem records

![Look Up Record action configured to return a record data pill from a Look Up Attachment action Sys ID output.](../images/example-look-up-attachment-action-02.png)

This example copies attachments from the trigger incident record into an associated problem record. This example assumes that there is only one source attachment to copy. If you need to copy multiple attachments, add a For Each flow logic. The flow first uses the Look Up Attachment action to find the attachment within the trigger incident. The Sys ID value of produced by this action is used as an input in the Look Up Record action in step 3. The flow next looks up a problem record associated with the incident record.

![Configuration of the Copy Attachment action using the outputs of two Look Up Record actions.](../images/example-copy-attachment-action.png)

In this example, the Source Attachment Record input gets its value from the Look Up Record action for the Attachment \[sys\_attachment\] table, because you can't use the string output of the Look Up Attachment action directly. The Target Record input gets its value from the Look Up Record action for the Problem \[problem\] table. The Table input inherits its value from the Target Record data pill.

![Execution details of flow step 3 Look Up Record for the Attachment table. The Record output links to the Attachment record.](../images/example-look-up-attachment-execution-details-02.png)

The execution details for flow step 3 show that the Look Up Record action has found a specific attachment record. This record is used as the input for flow step 4 Copy Attachment.

![Execution details for flow step 4 Copy Attachment. The step completed successfully.](../images/example-copy-attachment-action-execution-details.png)

The execution details for flow step 4 show that both input values use the output data pills of Look Up Record actions. The Source Attachment Record input uses the data pill from flow step 3, and its runtime value is a specific Attachment record. The Target Record input uses the data pill from flow step 2, and its runtime value is a specific problem record.

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

