---
title: Creating action items in events
description: Starting with BCM release 9.0.x, crisis managers can create action tasks for recovery members or teams anytime during a crisis event or exercise, as long as the event remains open. Crisis managers can create these tasks on the fly without mapping them to event assets or recovery plans. These action tasks are also not included in the event recovery timeline.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Creating action items in events

Starting with BCM release 9.0.x, crisis managers can create action tasks for recovery members or teams anytime during a crisis event or exercise, as long as the event remains open. Crisis managers can create these tasks on the fly without mapping them to event assets or recovery plans. These action tasks are also not included in the event recovery timeline.

## Action items in real-time

Action items can be used to assign tasks in real-time. For example, a crisis manager can assign an action item to verify that there are no injuries at a specific office location after an exercise or they can request someone to review the business continuity plan before proceeding to the next steps.

You can also use action items to conduct assessments during a crisis event. For example, in the event of a fire, you can assign an action item to assess the situation, determining the severity, and identify affected employees and buildings. You can perform an assessment and assign an action item.

## Fields and states associated with Action items

The Action items tab contains these details related to the ad-hoc tasks:

-   Actual start date
-   Actual end date
-   Total time taken
-   Event \(Reference\)
-   Short description
-   Description
-   Due date
-   Task numbers
-   Type
-   Task
-   Assessment

The states associated with action items are listed in the table.

|State|Description|
|-----|-----------|
|**Open**|First state of the action item.|
|**Work in progress**|State of the action item when its work begins. When an action item moves to the **Work in progress** state, the system auto-captures its start time.|
|**Skipped**|Assigned state of the action item when it is not relevant. When an action item is skipped and considered not relevant, its time fields are removed, resulting in a total time of 0.|
|**Closed \(complete, incomplete\)**|Final state of the action item task. When an action item has been completed, the system auto-captures its end time.|

BCM managers or planners can update the action items and can re-open the ad-hoc tasks associated with them.

You can assign the action item tasks to the groups or team members by using these fields:

-   **Assignment group**
-   **Assigned to**
-   **Additional assignee list**

## Comparison between event tasks and action items

The action items are distinct from the event tasks in crises and events. The table outlines the differences between event tasks and action items.

<table id="table_gtp_vfc_zfc"><thead><tr><th>

Fields/Criteria

</th><th>

Event task

</th><th>

Action items

</th></tr></thead><tbody><tr><td>

Details

</td><td>

-   Short description
-   Description
-   Task numbers
-   Dependencies
-   Activated plan
-   Impacted assets
-   Task ID

</td><td>

-   Short description
-   Description
-   Task numbers
-   Type

</td></tr><tr><td>

Assignment

</td><td>

-   Assignment group
-   Assigned to
-   Recovery team
-   Additional assignee list

</td><td>

-   Assignment group
-   Assigned to
-   Additional assignee list

</td></tr><tr><td>

Access

</td><td>

-   Plan owner, Program manager can create/update/delete action items.
-   Event recovery members can read/update action items that they are assigned to.

</td><td>

-   Plan owner, Program manager can create/update/delete action items.
-   Event recovery members can read/update action items that they are assigned to.

</td></tr><tr><td>

Workflow

</td><td>

Pending -&gt; Open -&gt; Work in progress -&gt; Skipped -&gt; Closed \(complete, incomplete, failed\)

</td><td>

Open -&gt; Work in progress -&gt; Skipped -&gt; Closed \(complete, incomplete\)

</td></tr><tr><td>

Dependencies

</td><td>

Yes

</td><td>

No

</td></tr><tr><td>

Automation

</td><td>

Yes

</td><td>

No

</td></tr><tr><td>

Orders

</td><td>

Yes, auto calculated based on dependencies.

</td><td>

No. Order is not calculated for the action item tasks.

</td></tr><tr><td>

Time calculation

</td><td>

Event tasks time is rolled up to activated plans, and impacted assets

</td><td>

No. Time is not rolled up for the action item tasks.

</td></tr></tbody>
</table>## Roles associated with action items

The roles associated with action items are listed in the table.

|Role|Description|
|----|-----------|
|Plan owner|Can create, read, update, and delete action items when the plan owner is the event owner.|
|Program managers|Can create, read, update, and delete action items for all events.|
|Viewers|Can read all action items.|
|Recovery event/Plan owner|Can read and update all action items that they are assigned to.|

-   **[Create task and assessment-type action items in events](../task/create-action-items-in-events.md)**  
Use integration of events and Smart Assessment for creating necessary action items related to an event.

**Parent Topic:**[Structured workflows for exercises](performing-tasks-to-manage-exercise-events.md)

