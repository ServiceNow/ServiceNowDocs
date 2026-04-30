---
title: Configure stages and add them to a flow
description: Configure when stages display to a user, define stage state labels, and add stages to a flow or subflows within Workflow Studio.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Flow and subflow stages, Building flows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Configure stages and add them to a flow

Configure when stages display to a user, define stage state labels, and add stages to a flow or subflows within Workflow Studio.

## Before you begin

This task assumes that you are familiar with flow and subflow stages, stage fields, and stage sets. For more information about stages, see [Flow and subflow stages](../concept/flow-designer-stages.md).

Role required: flow\_designer or admin

## Procedure

1.  If not already present, create a stage field on the table that triggers the flow.

    A stage field stores and displays the stage state and details about a specific record as a flow or subflow runs. The Service Catalog Requested Items \[sc\_req\_item\] table has a stage field by default.

    For a stage field to report stages on a record-based flow, a stage field must be present on the same table as the triggering record.

    To add a field to a table, see [Add and customize a field in a table](https://www.servicenow.com/docs/access?context=t_CreatingNewFields&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

2.  If adding stages to a flow with a Service Catalog trigger, select the flow in the **Flow** field of the Service Catalog Item \[sc\_cat\_item\] table.

    If using the Service Catalog trigger, the flow must be associated with the Service Catalog item through the **Flow** field. Remove any workflows associated with the item by clearing the **Workflow** and **Execution Plan** fields. This enables a request for a catalog item to initiate a flow specific to that catalog item.

3.  Open the flow or subflow in Workflow Studio.

    **Note:** While you can add stages to a flow that has a scheduled trigger, the stages are never displayed to an end user because there is no associated trigger record for the stage field. Only add stages to flows and subflows that have a trigger or input record.

4.  Create and configure stages.

    1.  Click ![The More Actions icon](../images/more-actions-menu-icon.png) and select **Flow stages**.

        The Flow stages menu opens.

    2.  From **Add stages from a template**, select a stage set to import existing stages from the Stage Sets table, and select **Add stages**.

        To learn more about stage sets, see [Workflow stage sets](../../using-workflows/concept/c_WorkflowStageSets.md#). Any changes made to the copy do not affect the original stage set record.

        In general, use stage sets when you want to reuse stages across multiple flows or subflows.

    3.  Click **Add new stage** to manually create and configure stage options inline.

        |Field|Description|
        |-----|-----------|
        |Name|Display name for the stage. Must be unique.|
        |Value|Internal name for the stage. Must be unique.|
        |Duration|Estimated duration displayed to the user. If you want to update stages based on flow run times, consider adding one or more Wait for a duration flow logic blocks. For more information, see [Wait for a duration flow logic](../concept/flow-logic-wait-for-a-duration.md).|
        |Always Show|If selected, the stage always displays in the stage field, even if the stage is set within a flow logic block that might not execute.|

        In general, create stages inline when you do not plan to reuse stages in other flows or subflows.

    4.  Order stages from top to bottom in the order you want the stage field to display them.

        The stage at the top appears first in the stage field, and the stage at the bottom appears last in the stage field.

        **Note:** If you create stages inline, the Flow Stages menu displays them in the order they were created, not in the order they appear in the flow.

5.  Add stages to the flow or subflow.

    1.  Point to a location in the flow or subflow.

    2.  Click **Add a Stage**.

    3.  Select an existing stage.

    Stages can be applied at the beginning of any Workflow Studio action or flow logic block, or within an If block.

    **Important:** Stages are unavailable from within a **For Each** flow logic block. You can only add stages before and after a **For Each** flow logic block.

    ![Add a stage to a flow.](../images/add-stage.png)

6.  Create stages inline.

    1.  Point to a location in the flow or subflow.

    2.  Select **Add a Stage**.

    3.  Select **+**.

    **Important:** When you create stages inline, stage fields display the stages in the order they were created, not in the order they appear in the flow. To configure or change the order of stages you create inline, open the More Actions menu ![The More Actions icon](../images/more-actions-menu-icon.png).

7.  Set a stage to the Error state within a conditional flow logic block.

    1.  Point to a location.

    2.  Select **Set "Error" State**.

        Note the following requirements to set a stage to the Error stage:

        -   The flow or subflow must have at least one stage defined.
        -   The Error can only be set within a stage. When an Error condition is reached, the current stage is set to Error.
        -   The Error can only be set within a conditional flow logic block.
        ![Set a stage to the Error state.](../images/set-error-example.png)

    When the flow reaches the indicated point, the currently executing stage is set to Error in the stage field.


## Result

When the flow runs, the stage details appear in any field of type Workflow. In a flow with a record-based trigger, the Workflow field of the triggering table displays the current stage state. In a flow with a Service Catalog trigger, the **Stage** field of the Requested Items \[sc\_req\_item\] table displays the current stage state.

**Parent Topic:**[Flow and subflow stages](../concept/flow-designer-stages.md)

