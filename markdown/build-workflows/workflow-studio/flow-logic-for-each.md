---
title: For Each flow logic
description: Apply one or more actions to each record in a list of records.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Flow logic, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# For Each flow logic

Apply one or more actions to each record in a list of records.

The **For Each** flow logic applies one or more actions to a list of records. The flow applies the actions contained within the flow logic to each record in the list.

**Note:** When you set a data pill value from inside a For each item branch of flow logic, the data pill value is only available to other actions in the same branch. Referencing a data pill value that was set inside a For each branch from outside of the flow logic branch produces a null value.

Iterating over a large number of records can be resource intensive, especially when the For Each logic block includes complex actions for each iteration. To avoid performance issues, turn off reporting using the **com.snc.process\_flow.reporting.level** system property. For more information, see [Workflow Studio flow system properties](../reference/flow-designer-system-properties.md).

## Inputs

-   **Items**

    Data type: **Records**

    List of Sys ID values or Records data pill specifying the records to process in sequence. You can use a Look Up Records action to generate a list of records. For more information, see [Look Up Records action](../reference/lookup-records-flow-designer.md).

    **Note:** If you want to process items in a particular order, you must first sort the items in this input in advance. For example, use the Order by option to sort the results of a Look Up Records action.


## Outputs

-   **\[Table name\] Record**

    Data type: **Record**

    Current record in the loop.

    **Note:** By default, all flow loops only store execution details for the first and last iterations of a loop. To report on all iterations of a loop, create a flow execution setting record for each flow that you want to collect loop execution details. For more information about flow execution settings, see [Flow execution settings](flow-execution-settings.md).


## Send an email for each configuration item potentially affected by a change

![Configuration of the For Each flow logic using a list of Configuration Item records](../images/example-for-each-flow-logic.png)

This example flow starts when a change request record is created. The flow uses a Look Up Records action to find Configuration Item records assigned to the requester of the change request. The flow uses For Each flow logic to send an email about each configuration that might be affected by the change request. The output of the Look Up Records action contains the list of records to process.

![Flow execution details of the For Each flow logic](../images/example-for-each-flow-logic-execution-details.png)

The flow execution details show the configuration item record used for each iteration of the loop.

## General guidelines

Use these general guidelines with a For Each flow logic.

-   **Avoid adding more than 1000 items**

    Avoid iterating over lists with more than 1000 records. Keep your list of records smaller to optimize flow performance. To iterate over lists with more than 1000 records, divide the list into smaller sections and use multiple flows.

-   **Avoid defining stages that depend on a For Each flow logic**

    Flow Designer prevents you from adding stages within a **For Each** block. You can only add stages before or after a **For Each** block.

-   **Avoid nested For Each loops**

    Avoid nested For Each loops that process many records. Nested loops may cause the flow to run until it is stopped by the flow transaction quota rule, which prevents flows from running longer than an hour. For more information about transaction quotas, see [Transaction quotas](https://www.servicenow.com/docs/access?context=c_TransactionQuotas&version=australia&pubname=australia-platform-administration&ft:locale=en-US).


**Parent Topic:**[Workflow Studio flow logic](flow-logic.md)

**Related topics**  


[Append to Flow Variables flow logic](../reference/append-to-flow-variables-flow-logic.md)

[Assign subflow outputs flow logic](flow-logic-assign-subflow-outputs.md)

[Call a workflow flow logic](flow-logic-call-workflow.md)

[Do the following until flow logic](flow-logic-do-until.md)

[Do the following in parallel flow logic](flow-logic-do-following-in-parallel.md)

[Dynamic flows flow logic](flow-logic-dynamic-flow.md)

[End Flow flow logic](flow-logic-end-action.md)

[Exit Loop flow logic](../reference/exit-loop-flow-logic.md)

[Get Flow Outputs flow logic](../reference/get-flow-outputs-flow-logic.md)

[Go back to flow logic](../reference/go-back-to-flow-logic.md)

[If flow logic](flow-logic-if.md)

[Make a decision flow logic](flow-logic-make-decision.md)

[Set Flow Variables flow logic](flow-logic-set-flow-variables.md)

[Skip Iteration flow logic](../reference/skip-iteration-flow-logic.md)

[Try flow logic](flow-logic-try.md)

[Wait for a duration flow logic](flow-logic-wait-for-a-duration.md)

