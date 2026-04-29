---
title: Flow and subflow stages
description: Communicate the current stage of a request, flow, or subflow with an end user.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Build flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Flow and subflow stages

Communicate the current stage of a request, flow, or subflow with an end user.

When configuring stages in Workflow Studio, you can:

-   Add stages to a flow or subflow
-   Change stage labels and names.
-   Configure the estimated duration for a stage.
-   Import a copy of a pre-defined stage set from the Stage Sets table. To learn more about stage sets, see [Workflow stage sets](../../using-workflows/concept/c_WorkflowStageSets.md#). Any changes made to the copy do not affect the original stage set record.

You can view the stages of a flow or subflow from its execution details.

## Displaying stages in a stage field

A stage field stores and displays the stage state and details about a specific record as a flow or subflow runs. For example, the Service Catalog table uses the **Stage** field to indicate the progress of a request as it is processed.

Stage fields display:

-   Stage details for the specific record that triggered the flow or that was used as a subflow input. For example, the current state of a specific Service Catalog requested item.
-   Stage names and states defined in the associated flow or subflow. If the associated flow calls another flow, stages set on the child flow do not display.
-   Stage details from flows or subflows that have started. If a flow or subflow is not running for a record, that record will not have any stage field details.

State icons in stage fields cannot be modified. Limit the number of stages and the length of each stage name to prevent wrapping text and icons onto multiple lines.

**Note:** Only add one stage field per table. If there is more than one stage field, the system only displays stages from the first stage field defined in the table dictionary entry.

## Stage field and trigger types

Associating a flow to a stage field depends on the flow trigger type.

<table id="table_i5y_rxt_ddb"><thead><tr><th>

Flow trigger type

</th><th>

Requirements

</th></tr></thead><tbody><tr><td>

Record

</td><td>

For a stage field to report stages on a record-based flow, a stage field must be present on the same table as the triggering record. When a flow has stages, Workflow Studio communicates the status of each stage back to the triggering table and displays the current stage state as an icon. If more than one stage field exists on the table, only the first stage field defined in the table's dictionary definition is used.

 **Note:** Avoid creating stages for multiple flows that trigger from the same table. A stage field only displays the stages of the final flow to run. Add different conditions to each flow to ensure that the stages of one flow do not overwrite another flow.

</td></tr><tr><td>

Service Catalog

</td><td>

If using the [Service Catalog trigger](../task/create-sc-flow.md), the flow must be associated with the Service Catalog item through the **Flow** field. Remove any workflows associated with the item by clearing the **Workflow** and **Execution Plan** fields. The **Stage** field displays the current stage state on any list view of the Requested Items \[sc\_req\_item\] table.

</td></tr></tbody>
</table>**Note:** While you can add stages to a flow that has a scheduled trigger, the stages are never displayed to an end user because there is no associated trigger record for the stage field. Only add stages to flows and subflows that have a trigger or input record.

## Stage states

During flow or subflow execution, each stage can be in one of six states.

<table id="table_wwy_pgk_cdb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Pending

</td><td>

This stage has not yet started.

</td></tr><tr><td>

In progress

</td><td>

This stage is executing.

</td></tr><tr><td>

Skipped

</td><td>

This stage was skipped and did not run. Typically, this state is reached when a conditional flow logic block is not executed.

</td></tr><tr><td>

Complete

</td><td>

This stage is complete.

</td></tr><tr><td>

Cancelled

</td><td>

This stage was cancelled.

</td></tr><tr><td>

Error

</td><td>

This stage has reached an error condition.

 When designing a flow or subflow, you can manually set its to report an Error state. To set an Error state:

-   The flow or subflow must have at least one stage defined.
-   The Error can only be set within a stage. When an Error condition is reached, the current stage is set to Error.
-   The Error can only be set within a conditional flow logic block.

</td></tr></tbody>
</table>Each stage can have its own custom state labels. For example, suppose that you have a flow with two stages. Stage 1 could have the Pending state with the label Waiting, and Stage 2 could have a Pending state with a label of Not yet started. Workflow Studio provides options to generate either the default states or approval states.

## Seeing subflow stages in a parent flow

![List of parent flow stages including the Manager Approval, Fulfillment Subflow stages, and Completed stages.](../images/example-subflow-stages-05-parent-flow-stages.png "Sample flow and subflow stages")

The Flow Stages dialog box can display subflow stages from a parent flow. Use the **Show Subflow Stages** option when configuring a subflow to include subflow stages in the parent flow.

## System properties

You can use these system properties to configure how a flow or subflow displays approval details.

-   **com.glide.hub.flow\_engine.stage\_display.show\_approvers**

    Show or hide the list of approvers assigned to a stage from a stage field. Set the value to true to show the list of approvers assigned to a stage. Set the value to false to hide the list of approvers assigned to a stage.

    -   Type: true \| false
    -   Default value: true
    -   Location: Add to the System Properties \[sys\_properties\] table
-   **com.glide.hub.flow\_engine.stage\_display.show\_approvers\_limit**

    Specify the maximum number of approvers to display in a stage field as an integer value. Setting this value above 10 risks causing rendering errors in a list view. The stage field for one record can become so big that the list cannot display additional records in the list.

    -   Type: integer
    -   Default value: 5
    -   Location: Add to the System Properties \[sys\_properties\] table

## General guidelines

Follow these general guidelines when creating flows or subflows with stages.

-   **Avoid defining stages that depend on a For Each flow logic**

    Flow Designer prevents you from adding stages within a **For Each** block. You can only add stages before or after a **For Each** block.

-   **Avoid creating stages for the same records in different flows or subflows**

    A stage field always displays the stage information provided by the last flow or subflow to run on a table's record. If multiple flows or subflows run on the same records, then the stages defined in one flow or subflow can in theory overwrite the stages from another flow or subflow. To avoid multiple flows or subflows overwriting each other's stages, define unique trigger or start conditions for each flow or subflow.

-   **Avoid updating stage fields from outside a flow or subflow**

    If you manage stages with a flow or subflow, avoid directly updating record stage fields from outside the flow or subflow. Manually updating the value of a stage field may produce unexpected or undesired results.

-   **Ensure that each flow on a table has unique trigger conditions**

    Adding unique trigger conditions to each flow ensures the flows only run under those conditions and prevents the stages from one flow overwriting the stages of another flow. Specifying unique trigger conditions makes it easier to troubleshoot flows by limiting the number of flow executions that can produce record changes.

-   **Use error stages to communicate with the user**

    The flow error state does not affect flow execution. A flow continues running even if it reaches an error stage. Use a conditional flow logic block to set the error stage and communicate to the user that the state of the current stage is Error. For example, if an approval is not approved within the required limit, you may want to communicate an error to the user.

-   **Use the error stage to stop processing a flow**

    Use a conditional flow logic block to identify when a flow enters the error stage. Use the flow logic to stop processing the flow or take some kind of remediation action. For example, you may want to change the record state or assignment when a flow reaches an error state.


-   **[Configure stages and add them to a flow](../task/add-stages.md)**  
Configure when stages display to a user, define stage state labels, and add stages to a flow or subflows within Workflow Studio.
-   **[Show subflow stages in a parent flow](../task/show-subflow-stages-in-a-parent-flow.md)**  
Show subflow stages as part of the execution details of a parent flow.

**Parent Topic:**[Building flows](flows.md)

