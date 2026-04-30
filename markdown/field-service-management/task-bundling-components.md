---
title: Field Service Task Bundling components
description: Several types of components are installed with the activation of the Field Service Task Bundling feature including business rules, task filters and task grouping rules.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Components installed with additional plugins, Reference, Field Service Management]
---

# Field Service Task Bundling components

Several types of components are installed with the activation of the Field Service Task Bundling feature including business rules, task filters and task grouping rules.

## Business Rules

Field Service Task Bundling adds the following business rules.

|Business Rule|Table|Description|
|-------------|-----|-----------|
|Bundle Actual Time Field Update|Work Order Task \[wm\_task\]|Updates the **Actual travel start** and **Actual onsite arrival** fields of the bundle.|
|Bundle Assignment|Work Order Task \[wm\_task\]|Updates bundled subtask assignment.|
|Bundle Assignment Before|Work Order Task \[wm\_task\]|Prevents bundling when bundle **Window start** is before the subtask **Window start**. Prevents bundling when bundle **Expected Start** is before bundle **Window start**.|
|Bundle Change After|Work Order Task \[wm\_task\]|Validates and updates bundles based on bundled subtasks, or validates and updates unbundled subtasks based on their previous bundle.|
|Bundle Change Before|Work Order Task \[wm\_task\]|Validates and updates bundles when subtasks are added to or removed from the bundle.|
|Bundle Scheduled Start Change|Work Order Task \[wm\_task\]|Initiates the scheduling of bundled subtasks.|
|Bundle Siblings Prevention|Work Order Task \[wm\_task\]|Prevents duplicate task bundles from being created for the same work order.|
|Bundle state change|Work Order Task \[wm\_task\]|Updates the bundle state.|
|Bundle subtask assignment changes|Work Order Task \[wm\_task\]|Prevents bundled subtask assignment based on subtask state or current agent assignment.|
|Bundle Subtasks Changes Info Message|Work Order Task \[wm\_task\]|Informs the user when no changes have occurred.|
|Bundle Task SubState Update|Work Order Task \[wm\_task\]|Updates the substate of the bundle based on the bundle state and action taken by the agent.|
|Cancel Task Bundle|Work Order Task \[wm\_task\]|Unbundles all subtasks in a bundle.|
|Confirm Assignment on Bundle Task|Work Order Task \[wm\_task\]|Updates and syncs subtask state to the bundle state upon assignment by a dispatcher.|
|Enforce bundle mandatory fields|Task Grouping Qualifier \[sn\_task\_grouping\_qualifier\]|Prevents dynamic bundling when mandatory fields are empty.|
|Grouping rule info message for wm\_task|Task Grouping Rule \[sn\_task\_grouping\_rule\]| |
|Lock and Unlock Subtasks|Work Order Task \[wm\_task\]|Updates subtasks schedule lock state to match bundle when bundle schedule lock is changed.|
|On bundle state change from Draft to PD|Work Order Task \[wm\_task\]|Updates subtasks state to match bundle state when bundle is set to **Pending Dispatch**. Validates subtask state and provides error message when a subtask failed to update.|
|On change bundle Assignment Group|Work Order Task \[wm\_task\]|Updates subtasks assignment group to match bundle when bundle assignment group is changed.|
|Prevent bundle location changes|Work Order Task \[wm\_task\]|Validates that the bundle location equals the location of the first subtask in the bundle. Prevents bundle location from being different from the location of the first subtask in the bundle.|
|Prevent duplicate/multiple qualifiers|Task Grouping Qualifier \[sn\_task\_grouping\_qualifier\]|Prevents bundling when both or neither **Assignment group** or **Territory** qualifiers are active. Prevents bundling when identical qualifier exists.|
|Prevent schedule lock update on subtasks|Work Order Task \[wm\_task\]|Prevents subtask schedule lock from being different from parent bundle schedule lock.|
|Push initial subtask location to bundle|Work Order Task \[wm\_task\]|Updates bundle location to the location of the first subtask in the bundle.|
|Remove subtasks they are in diff state|Work Order Task \[wm\_task\]|Removes subtasks from bundle when subtask state is different from the bundle state.|
|Reschedule after Subtask Order Change|Work Order Task \[wm\_task\]|Reschedules the bundle when order of subtasks is changed.|
|Set name for territory|Task Grouping Qualifier \[sn\_task\_grouping\_qualifier\]|Sets the **Name** value of the **Territory** qualifier.|
|Subtask Order Validation|Work Order Task \[wm\_task\]|Validates that the **Order** value of subtasks are unique and not empty.|
|SubTask Schedule State Change|Work Order Task \[wm\_task\]|Updates the bundle and subtask states from **Assigned** to **Scheduled** when a dispatcher schedules the bundle.|
|Subtasks field change - not supported|Work Order Task \[wm\_task\]|Prevents subtask estimated work duration from being manually updated based on subtask state.|
|Sync bundle with subtasks|Work Order Task \[wm\_task\]|Syncs bundle with subtask values.|
|Sync Bundle Work Duration to subtasks|Work Order Task \[wm\_task\]|Syncs bundle duration to the total estimated work duration of its subtasks.|
|Validate Min &amp; Max Tasks|Task Grouping Policy \[sn\_task\_grouping\_policy\]|Validates that the number of subtasks in a bundle created from a policy falls between the policy minimum and maximum range.|
|Work duration change on bundle|Work Order Task \[wm\_task\]|Validates that the subtask estimated work duration is less than the subtask duration of the bundle.|

## Task Grouping Policies

Field Service Task Bundling adds the following task grouping policy.

<table id="table_qpt_vpd_5xb"><thead><tr><th>

Task Grouping Policy

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default Policy

</td><td>

-   Minimum records: 2
-   Maximum records: 10
-   -   WOT's in Same Location Within Next 30 Days
-   WOT's In Same Territory With Required Skill Set Within Next 30 Days
-   WOT's In Same Territory Within Next 30 Days
-   WOT's That Need Same Asset Within Next 30 Days
-   WOT's With Similar Required Parts
-   WOT's With Similar Task Skills

</td></tr></tbody>
</table>## Task Grouping Rules

Field Service Task Bundling adds the following task grouping rules.

|Task Grouping Rule|Policy|Description|
|------------------|------|-----------|
|WOT's in Same Location Within Next 30 Days|Default Policy|Bundles tasks that are in the same Location within the next 30 days.|
|WOT's In Same Territory With Required Skill Set Within Next 30 Days|Default Policy|Bundles tasks that are in the same Territory and require specific skills within the next 30 days.|
|WOT's In Same Territory Within Next 30 Days|Default Policy|Bundles tasks that are in the same Territory within the next 30 days.|
|WOT's That Need Same Asset Within Next 30 Days|Default Policy|Bundles tasks that require the same Asset within the next 30 days.|
|WOT's With Similar Required Parts|Default Policy|Bundles tasks that require similar parts.|
|WOT's With Similar Task Skills|Default Policy|Bundles tasks that require similar skills.|

## Task Filters

Field Service Task Bundling adds the following task filters, task filter criteria, to Dynamic Scheduling.

<table id="table_ahq_zrg_5xb"><thead><tr><th>

Task Filter

</th><th>

Conditions

</th><th>

Criterion

</th><th>

Function

</th></tr></thead><tbody><tr><td>

Assignment : Assign Pending Dispatch Task Bundle

</td><td>

-   IsBundle = true
-   State = Pending Dispatch
-   Substate is not auto-assigned or empty.

</td><td>

-   Bundle: Ignore Rejected Technician
-   Bundle: Matching Skills for Dynamic Scheduling
-   Current Distance From Task

</td><td>

Assigns bundles that are in the Pending Dispatch state.

</td></tr><tr><td>

Bundle Reassignment : reassign unassigned task bundles

</td><td>

-   IsBundle = true
-   Schedule lock = false
-   State is one of scheduled, assigned, accepted

</td><td>

-   Bundle: Ignore Rejected Technician
-   Bundle: Matching Skills for Dynamic Scheduling
-   Current Distance From Task

</td><td>

Reassigns unassigned task bundles.

</td></tr></tbody>
</table>|Criterion|Function|
|---------|--------|
|Bundle: Ignore Rejected Technician|Ignores agents who have rejected a task from the bundle previously. Prevents bundles with rejected tasks from being assigned to the rejecting agent.|
|Bundle: Matching Skills For Dynamic Scheduling|Matches bundles that have skill requirements with agents who have those skills.|
|Bundle: Matching Mandatory Parts for Dynamic Scheduling|Matches bundles that have part requirements with agents who have those parts.|

-   **[Field Service Task Bundling fields](work-order-task-bundling-fields.md)**  
The fields that are included in the details section of work order task bundles.

**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

