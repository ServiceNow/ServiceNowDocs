---
title: Industrial Guided Task standard and task life cycles
description: A life cycle is the list of states that an Industrial Guided Task \(IGT\) standard or task can go through.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Industrial Guided Tasks, Reference, Digital Factory Workspace, Industrial Connected Workforce]
---

# Industrial Guided Task standard and task life cycles

A life cycle is the list of states that an Industrial Guided Task \(IGT\) standard or task can go through.

## Industrial Guided Task standard states

|State|Description|
|-----|-----------|
|Draft|The standard can be edited.|
|Review|Approval has been requested and the standard is being reviewed. The standard cannot be edited.|
|Published|The standard is active and published. The standard can be requested, which means a task can be created. The standard cannot be edited.|
|Retired|The standard is inactive, read-only, and can’t be requested. The standard cannot be edited.|
|Revised|End state. An older version that has been revised. The standard is available as read only for reference. The standard cannot be edited.|

## Industrial Guided Task standard approval states

|State|Description|
|-----|-----------|
|Not yet requested|The standard has not been submitted for approval yet.|
|Requested|The approval request has been submitted and is awaiting review. Any user from the assigned owner group can approve it for publishing.|
|Approved|The request has been reviewed and officially approved. The state of the standard changes to Published.|
|Rejected|The request was reviewed and not approved. When the request is rejected, the state of the standard moves back to Draft.|
|Canceled|The request was withdrawn before a decision was made.|
|No Longer Required|The request is obsolete due to changes.|

## Industrial Guided Task states

<table id="table_n25_srl_3fc"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ready

</td><td>

The task is created and ready to be picked up for execution.

 When a task transitions to this state, the system automatically captures the actual start time. On ICW mobile, the actual start is captured when the operator selects **Perform task**.

</td></tr><tr><td>

Work in Progress

</td><td>

The task is being executed on the shop floor.

</td></tr><tr><td>

On Hold

</td><td>

The task has been temporarily paused due to dependencies or external factors.

</td></tr><tr><td>

Submitted

</td><td>

The standard has been submitted, but some child sub tasks are still pending before the task is fully complete.When a task transitions to this state, the system automatically captures the actual end time and calculates the business duration.

</td></tr><tr><td>

Closed Complete

</td><td>

The task has been completed on the shop floor and submitted in the Workspace.

</td></tr><tr><td>

Closed Skipped

</td><td>

The task has expired.

</td></tr><tr><td>

Canceled

</td><td>

The task has been removed from the schedule. It won't be executed due to cancellation of the order, process changes, or other strategic decisions.

</td></tr></tbody>
</table>## Industrial Guided Task life cycle

When you start a task, you can make changes and select **Save**. The task then changes to Work in Progress but you can still change the state to On Hold. When you cancel the task, you must fill in the justification and then select **Cancel task**. If the task is a work in progress, the **Continue task** button is available. Once you select **Submit**, the state changes to Closed Complete.

When the state of a task changes it triggers an automatic tracking of task duration. The actual start time is recorded when the task moves to Work in Progress, and the actual end time is recorded when the task is submitted. The system captures the total duration spent on the task, from Work in Progress state till Submitted state. The duration value is then recorded in the business duration field.

**Parent Topic:**[Industrial Guided Tasks reference](industrial-guided-tasks-reference.md)

