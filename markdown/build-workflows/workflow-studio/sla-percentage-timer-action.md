---
title: SLA Percentage Timer action
description: Identify when a task SLA record reaches a specific percentage value and perform other actions or flow logic that is based on the SLA percentage. For example, send a notification when an SLA percentage timer completes.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Actions, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# SLA Percentage Timer action

Identify when a task SLA record reaches a specific percentage value and perform other actions or flow logic that is based on the SLA percentage. For example, send a notification when an SLA percentage timer completes.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Fields

|Field|Description|
|-----|-----------|
|Percentage|The positive integer percentage of the total SLA duration used to compute an end time. For example, a 50% percentage results in the system computing an end date-time value that is 50% of the total SLA duration. If an SLA requires tasks to be completed within 24-hours, then 50% of that SLA would be 12 hours.|

## Scheduled End Date/Time

The **Scheduled End Date/Time** output data pill lists the computed time that the SLA percentage timer action is expected to end. The computed end date is determined by the input Task SLA record and the input Percentage. This date/time value is independent of any elapsed time field values in the Task SLA record.

-   If the end date is in the future, the system creates a system event to continue running the action at that future date. While the system waits for the scheduled end date, it pauses the flow and action.
-   If the end date is in the past, the system immediately sets the **Status** of the SLA Percentage Timer action.

## Status

The **Status** data pill contains the result of the SLA percentage timer.

|Status|Description|
|------|-----------|
|Completed|The timer action reached its scheduled end date/time. Flow designers can build specific flow logic for this action status.|
|Paused|The timer was paused before its scheduled end date/time. If the timer resumes running, Workflow Studio generates a new scheduled end date/time value. Flow designers can build specific flow logic for this action status.|
|Repair|The flow is running in repair mode, and the scheduled end date/time is in the past. Flow designers can build specific flow logic for this action status.|
|Skipped|The timer did not run because the scheduled end date/time is in the past. Flow designers can build specific flow logic for this action status.|
|Waiting|The timer is running and has yet to reach the scheduled end date/time.|

Workflow Studio sets the action status when the SLA state matches an [SLA condition](https://www.servicenow.com/docs/access?context=c_SLAConditions&version=australia&pubname=australia-it-service-management&ft:locale=en-US) or when certain UI actions are selected.

<table id="table_gqk_nvt_1jb"><thead><tr><th>

SLA state

</th><th>

Action status set

</th><th>

Flow run state

</th></tr></thead><tbody><tr><td>

SLA attaches and the scheduled end date/time is in the future.

</td><td>

Set action status to **Waiting**.

</td><td>

The flow waits until the SLA timer completes, is cancelled, or is paused.

</td></tr><tr><td>

SLA attaches and the scheduled end date/time is in the past.

</td><td>

-   If the flow was started in Repair mode, set action status to **Repair**.
-   Otherwise, set action status to **Skipped**.

</td><td>

The flow runs the next action or flow logic in the flow sequence.

</td></tr><tr><td>

SLA Cancels.

</td><td>

Set action status to a null value.

</td><td>

The flow stops with a state of **Cancelled**.

</td></tr><tr><td>

SLA Pauses.

</td><td>

Set action status to **Paused**.

</td><td>

The flow waits until the SLA Task flow is cancelled or is resumed.

</td></tr><tr><td>

SLA reaches Scheduled End Date/Time.

</td><td>

Set action status to **Completed**.

</td><td>

The flow runs the next action or flow logic in the flow sequence.

</td></tr><tr><td>

SLA Resumes.

</td><td>

Set action status to **Waiting**.

</td><td>

The flow waits until the SLA timer completes, is cancelled, or is paused.

</td></tr><tr><td>

SLA Stops.

</td><td>

Set action status to a null value.

</td><td>

The flow stops with a state of **Cancelled**.

</td></tr></tbody>
</table>## Total Duration

The **Total Duration** data pill lists the total number of seconds that the action ran. The total duration is computed from the action start time and the time when the action reached the **Completed** status. Status values other than **Completed** produce a null value **Total Duration**.

## General guidelines

Follow these general guidelines when creating flows that contain Service Level Agreement \(SLA\) Percentage Timer actions.

-   **Add SLA Percentage Timer actions only to flows with an SLA Task trigger**

    An SLA Percentage Timer action can only run when the flow starts from an SLA Task trigger. You cannot activate a subflow containing an SLA Percentage Timer action.

-   **Create conditional flow logic for expected Status values**

    Use the value of the **Status** field as a condition for flow logic. Build flow logic for expected **Status** values such as **Completed**, **Repair**, and **Skipped**. For example, add an **If** flow logic block to send a notification when the SLA Percentage Timer has a status of **Completed**.

-   **Assign each SLA Percentage Timer action a unique cumulative Wait for percentage value**

    Each SLA Percentage Timer action computes its own Scheduled End Date/Time using its Wait for percentage value. If you create multiple SLA Percentage Timer actions, give each action its own unique cumulative Wait for percentage value. For example, create three separate actions with different percentage complete values such as 25%, 50%, and 75% complete. Setting all three actions to the same percentage complete value such as 25% causes the timers to complete at the same time.

-   **Copy existing flows to make customizations**

    Reduce development time by copying the default SLA flows and customizing the copies with your own logic. Select a customized flow to run from the SLA definition. See [Create an SLA definition](https://www.servicenow.com/docs/access?context=t_CreateAnSLADefinition&version=australia&pubname=australia-it-service-management&ft:locale=en-US) .


**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

