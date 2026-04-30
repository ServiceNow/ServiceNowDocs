---
title: Create a flow with a Service Catalog trigger
description: Start a flow when a Service Catalog item is requested to automate the fulfillment process.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-08-13"
reading_time_minutes: 3
breadcrumb: [Create a flow in Workflow Studio, Building flows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create a flow with a Service Catalog trigger

Start a flow when a Service Catalog item is requested to automate the fulfillment process.

Getting started with flows in Workflow Studio 

## Before you begin

Role required: flow\_designer or admin

## About this task

Unlike a record trigger which runs on all records in a table, the Service Catalog trigger runs on all catalog item requests for a specific item when the catalog item is configured to run a specific flow. For example, you can define a flow that runs every time there is a request for a tablet. The requested item becomes the flow trigger record.

## Procedure

1.  If not already created, create the catalog item to associate with the flow.

    1.  Navigate to **Service Catalog** &gt; **Catalog Definition** &gt; **Maintain Items**.

        The Catalog Items \[sc\_cat\_item\] table opens.

    2.  Click **New**.

    3.  Complete the fields.

        For a detailed description of catalog item fields, see [Catalog Item form](https://www.servicenow.com/docs/access?context=catalog-item-form&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

        **Note:** If you plan to add stages to your flow, verify that there is not an existing workflow associated with the item that also has stages. Clear the values of the **Workflow** and **Execution Plan** fields to prevent conflicting stages from reporting to the requested item stage field.

2.  Create the flow to associate with the catalog item.

    When triggered, this flow processes the catalog item request.

    1.  Navigate to **Process Automation** &gt; **Flow Designer**.

    2.  Click **+ New** &gt; **New Flow**.

    3.  Define the flow properties.

        For more information, see [Create a flow in Workflow Studio](create-flow.md).

    4.  In the Trigger section, add a trigger and select **Service Catalog**.

        **Note:** Service Catalog triggers do not support catalog variables as part of the trigger condition. Instead, get or create catalog variables in the main body of the flow.

    5.  Create flow-specific catalog variables available only to flow actions.

        See [Create flow Service Catalog variables](create-flow-catalog-variables.md).

    6.  Add actions, subflows, and flow logic to the flow.

        Some actions enable you to manage catalog items. For example, the Create Catalog Task action generates a task for the requested item, and the Get Catalog Variables action enables you to access catalog variables as data pills in the flow. See [Create Catalog Task action](../reference/create-catalog-task-flow-designer.md) and [Get Catalog Variables action](../reference/get-cat-variables-flow-designer.md).

    7.  Add stages to the flow to report progress to the requester.

        See [Flow and subflow stages](../concept/flow-designer-stages.md).

    8.  Test the flow.

        Once behaving as desired, activate the flow. For more information, see [Test a flow](flow-test.md) and [Activate a flow](flow-activate.md).

        **Note:** You can't activate a flow if it references catalog variables that are inactive or don't exist.

3.  Add the flow to the **Flow** field of the catalog item you created.

    1.  Navigate to the catalog item.

    2.  In the **Flow** field, select the flow you created.

        **Note:** The **Flow** field only displays flows with a Service Catalog trigger. If the **Flow** field is not visible, configure the form to display it.

    3.  Click **Update**.


## Result

When the catalog item is requested, the associated flow triggers and runs the actions.

## What to do next

Create and deploy catalog item records to your instances.

**Note:** Service Catalog records are created in the global scope. They are not part of the source control or application repository transfer, and they are not part of the default Workflow Studio update set.

**Parent Topic:**[Create a flow in Workflow Studio](create-flow.md)

