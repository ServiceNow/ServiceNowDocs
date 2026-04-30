---
title: Wait for a duration flow logic
description: Use this flow logic to give your users time to act during automated processes or to wait for a specific date and time to complete actions.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Flow logic, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Wait for a duration flow logic

Use this flow logic to give your users time to act during automated processes or to wait for a specific date and time to complete actions.

## Inputs

<table id="table_dzc_n4g_p2b"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Duration Type

</td><td>

-   **Explicit Duration**: Wait for a specific time period, such as 5 minutes.
-   **Relative Duration**: Wait for a specific time period from a selected Duration data pill or date/time value, such as 5 minutes after the flow start.
-   **Percentage Duration**: Type to specify a certain percentage of time duration between the start of the flow logic and specified end time.

**Note:** The percentage value must be from **0** through **100** only.


</td></tr><tr><td>

Wait for

</td><td>

Set this value manually or select a Duration data pill from the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\). For example, use a Look Up Record action to select an SLA Definition record and return the value of the **Duration** field.-   **Explicit Duration**: Wait duration in hours, minutes, and seconds.
-   **Relative Duration**: Wait duration in hours, minutes, and seconds before or after a specific time. Select **Relative Duration** to specify a wait duration from a specific date.

**Note:** Past dates don't affect the wait duration.


You can enter a wait value of up to 999 hours.**Note:** The actual wait duration can vary due to the instance processing time. The flow always waits for the time that you specify for this field, but other work in the queue may add to the wait time.

</td></tr><tr><td>

Wait for Percentage

</td><td>

Wait duration as a percentage of the time period between the start of flow logic and specified end time. If you select a past date for the end time, the wait duration is set to **0**. This field appears when **Percentage Duration** is selected from the Duration Type list.

</td></tr><tr><td>

During the following schedule

</td><td>

Select the schedule used to calculate the **Scheduled End date/time** value from the selected wait duration. For example, waiting for a 10-hour duration as part of an 8-5 weekdays schedule causes the flow to wait for one or more business days. If you leave this field blank, the timer runs without a schedule. For information on creating schedules, see [Define a schedule](https://www.servicenow.com/docs/access?context=t_DefineASchedule&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>## Outputs

|Output|Description|
|------|-----------|
|Duration|Total time that the flow ran in milliseconds. You can drag this data pill into the duration fields.|
|Date/time|Date/time that the flow completed. You can drag this data pill into the date/time fields.|

## Close an incident if it has been in the resolved state for 10 days

In this example, a flow starts when the incident state changes to Resolved.

![Flow trigger.](../images/duration-example-1.png "Flow trigger")

## Wait 10 days after the last update to a record

In this example, the flows waits for 10 days after the incident record has been resolved.

![Wait for Duration flow logic.](../images/duration-example-2.png "Wait for Duration flow logic")

## Update a record after 10 days

In this example, the flows closes the incident record 10 days after it was resolved.

![Action used to close the incident.](../images/duration-example-3.png "Action used to close the incident")

## Wait for a duration of 50% of the time between the start of the flow logic and the due date

In this example, the flows send a notification email to the relevant manager when a critical problem is created and 50% of the time between the problem record creation and the problem due date has lapsed.

![Wait for percentage time duration flow logic.](../images/wait-percentage-duration.png "Wait for percentage time duration flow logic")

## Relative Duration type

When the duration type is **Relative Duration**, the flow logic first evaluates the relative date and time, the schedule, and finally, the duration. Schedules, dates, and times set in the past don't affect the wait duration. This table provides examples of how the flow processes the wait duration in these scenarios.

|Duration Setting|Relative Date/Time|Schedule|Effect|
|----------------|------------------|--------|------|
|Set to 0.|None|None|Duration ends immediately.|
|Greater than 0.|Past date|None|Duration ends immediately.|
|Greater than 0.|Future date|None|Flow waits for the date/time, and then waits for the duration.|
|Greater than 0.|Past date|Future date|Flow waits for schedule, and then waits for the duration.|
|Greater than 0.|Future date|Past date|Flow waits for the date/time, and then waits for the duration.|
|Greater than 0.|Future date|Future date|Flow waits for the future date, then for the schedule, and then for the duration.|

The timer waits for the next instance of a selected schedule. For example, if you set a schedule for Monday through Friday from 8 a.m. to 5 p.m., and the timer is initiated on Saturday, the timer waits until Monday at 8 a.m. before starting.

## Execution details

![Example execution details for a wait for a duration flow.](../images/ex-details-wait-for-duration.png "Execution details for Wait for a duration flow logic")

1.  The header shows the state, start time, and runtime for the flow logic.

    **Note:** The runtime value in the header only includes the time that it takes to execute the flow logic and doesn't include the wait duration that is specified in the flow.

2.  The Configuration Details section shows details about the variables that are used by the flow, including the type, configuration, and runtime values for each variable.

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

[For Each flow logic](flow-logic-for-each.md)

[Get Flow Outputs flow logic](../reference/get-flow-outputs-flow-logic.md)

[Go back to flow logic](../reference/go-back-to-flow-logic.md)

[If flow logic](flow-logic-if.md)

[Make a decision flow logic](flow-logic-make-decision.md)

[Set Flow Variables flow logic](flow-logic-set-flow-variables.md)

[Skip Iteration flow logic](../reference/skip-iteration-flow-logic.md)

[Try flow logic](flow-logic-try.md)

