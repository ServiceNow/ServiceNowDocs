---
title: Field Service Crew Operations components
description: The roles, tables, script includes, and business rules for the Field Service Crew Operations application.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Components installed with additional plugins, Reference, Field Service Management]
---

# Field Service Crew Operations components

The roles, tables, script includes, and business rules for the Field Service Crew Operations application.

Field Service Crew Operations adds the My Crew menu to the application navigator and the following modules:

-   My Crews: Enable managers and dispatchers to create and manage crews.
-   My Crew Tasks: Enable agents to view the crew tasks assigned to a crew they belong to.

## Roles

Field Service Crew Operations adds the following roles:

<table id="table_gzx_lz1_zlb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field Service Crew Moderator\[wm\_crew\_moderator\]

</td><td>

Enables dispatchers and managers to create crews, manage crew members, assign skills and locations, and assign them to assignment groups.

</td></tr></tbody>
</table>## Tables

Field Service Crew Operations adds the following tables:

<table id="table_vnw_mpt_fpb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Crewwm\_crew

</td><td>

Stores high-level information about the crew, such as the crew size, leader, location, schedule, travel radius.

</td></tr><tr><td>

Crew Groupwm\_crew\_group

</td><td>

Stores the mapping of crews to the selected assignment groups​.

</td></tr><tr><td>

Crew Memberwm\_crew\_member

</td><td>

Stores the various members of the crew and their effective availability in the crew​.

</td></tr><tr><td>

Crew Requirementwm\_crew\_requirement

</td><td>

Stores fine-grained requirements for a crew, such as the minimum crew size and recommended size.​

</td></tr><tr><td>

Crew Skillwm\_crew\_skill

</td><td>

Stores the skills that the crew members currently possess.

</td></tr><tr><td>

Task Assigneewm\_task\_assignee

</td><td>

Stores the mapping of all agents working on a work order task​.

</td></tr></tbody>
</table>## Script Includes

Field Service Crew Operations adds the following new script includes:

|Script Include|Description|
|--------------|-----------|
|CrewSchedulingUtils|Updates the crew members, crew skills, crew requirements, task assignees, and the crews an agent belongs to​.|
|CrewSchedulingClientUtils|Fetches the crews that an agent belongs to and the tasks assigned to those crews for client-side script use​​.|
|CrewLocationFromTask|Rates crews based on their location and distance to the task​.|
|CrewMatchingDimensionSkills|Rates crews based on their skills and the skills required for the task​​.|
|CrewTasksScheduleUtil|Determines crew and agent schedule​.|
|FSMUtil|Checks for crew radius, distance to the task, and whether the task needs a crew​.|
|SMDateValidation|Checks for task scheduling conflicts if an agent is already part of a crew, and whether an agent can be added to a crew depending on effective from or effective to dates.|
|SMGeoDistanceUtils|Extends agent functions to the crew, such as finding midnight of that day for the crew, finding the next task on the same day, getting multiple agent locations, and calculating travel duration.|
|TimeRecordingHelper|Modifies the information message to include an agent’s name​.|

## Business Rules

Field Service Crew Operations adds the following business rules:

<table id="table_g1z_3qt_fpb"><thead><tr><th>

Business Rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Abort deletion of crew​

</td><td>

Crew \[wm\_crew\]

</td><td>

Prevents deletion of a crew if the crew is referenced in any work order task.

</td></tr><tr><td>

Abort inactivation of crew

</td><td>

Crew \[wm\_crew\]

</td><td>

Prevents the inactivation of a crew if the crew has any active task assignments​.

</td></tr><tr><td>

Adds default skill level

</td><td>

User Skill\[sys\_user\_has\_skill\]

</td><td>

Adds default skill level.​

</td></tr><tr><td>

Add group and member for crew leader

</td><td>

Crew \[wm\_crew\]

</td><td>

Creates wm\_crew\_group and wm\_crew\_member records for the crew leader.

</td></tr><tr><td>

Add group skills to crew

</td><td>

Crew Group\[wm\_crew\_group\]

</td><td>

Adds new skills to the crew whenever a new group is added to the crew.

</td></tr><tr><td>

Add missing crew groups for crew member

</td><td>

Crew Member\[wm\_crew\_member\]

</td><td>

Updates a crew group when a new member is added to the crew.

</td></tr><tr><td>

Calculate estimated duration for crew

</td><td>

Work Order Task\[wm\_Task\]

</td><td>

Calculates the estimated travel duration of a crew.​

</td></tr><tr><td>

Check crew size

</td><td>

Crew \[wm\_crew\]

</td><td>

Validates the crew size at the time of crew creation.

</td></tr><tr><td>

Check crew size on creation

</td><td>

Crew Member\[wm\_crew\_member\]

</td><td>

Validates the crew size at the time of crew member addition.

</td></tr><tr><td>

Check crew size on updation

</td><td>

Crew Member\[wm\_crew\_member\]

</td><td>

Validates the number of members in a crew when a crew member record is updated or deleted.

</td></tr><tr><td>

Check duplicate members for same crew

</td><td>

Crew Member\[wm\_crew\_member\]

</td><td>

Prevents the addition of duplicate members in a crew​.

</td></tr><tr><td>

Check leader availability for task crew

</td><td>

Crew \[wm\_crew\]

</td><td>

Checks the availability of the crew leader at the time of assigning a task to the task-specific crew.

</td></tr><tr><td>

Check member is part of any active crew

</td><td>

Crew Member\[wm\_crew\_member\]

</td><td>

Ensures that a crew member is not part of multiple crews at the same time to avoid conflicts in the crew membership of a crew member.​

</td></tr><tr><td>

Check task conflicts for crew members

</td><td>

Crew Member\[wm\_crew\_member\]

</td><td>

Checks whether the crew member has any conflict due to existing task assignments.

</td></tr><tr><td>

Check task conflicts for task assignees

</td><td>

Work Order Task\[wm\_task\_assignee\]

</td><td>

Checks for any conflicts in the task assignee schedule due to the existing task assignment.

</td></tr><tr><td>

Crew radius check​

</td><td>

Work Order Task\[wm\_Task\]

</td><td>

Shows an information message when the task assigned to a crew is outside the covered radius​.

</td></tr><tr><td>

Date Checks

</td><td>

Crew Member\[wm\_crew\_member\]

</td><td>

Validates the effective from and effective to dates for crew members.

</td></tr><tr><td>

Deactive member when crew is inactive

</td><td>

Crew \[wm\_crew\]

</td><td>

Deactivates the crew members when a crew is not active​.

</td></tr><tr><td>

Deactivate task crews

</td><td>

Work Order Task\[wm\_Task\]

</td><td>

Marks the task-specific crew as inactive when the task is completed or canceled.​

</td></tr><tr><td>

Delete task assignees for task crews

</td><td>

Crew Member\[wm\_crew\_member\]

</td><td>

Deletes task assignees from a work order task when a member is removed from the task-specific crew​.

</td></tr><tr><td>

Disable completed/cancelled task crews​

</td><td>

Crew \[wm\_crew\]

</td><td>

Sets a crew to inactive after the assigned task is completed or canceled.​

</td></tr><tr><td>

Manage task crew requirement ​

</td><td>

Work Order Task\[wm\_Task\]

</td><td>

Creates and deletes the crew requirement of a work order task​.

</td></tr><tr><td>

Remove group skills from crew

</td><td>

Crew Group\[wm\_crew\_group\]

</td><td>

Deletes skills from the crew when a crew group is deleted from the crew.​

</td></tr><tr><td>

Restrict actions on crew leader

</td><td>

Crew Member\[wm\_crew\_member\]

</td><td>

Restrict actions on crew leader.

</td></tr><tr><td>

Restrict updates to primary leader​

</td><td>

Work Order Task\[wm\_task\_assignee\]

</td><td>

Restricts the ability to update or delete the primary leader of a crew in the task assignees related list.

</td></tr><tr><td>

Replicate crew member task travel time

</td><td>

Work Order Task\[Task\_time\_worked\]

</td><td>

Records the time taken by crew members to travel to the task location and the time they spent working on a work order task.

</td></tr><tr><td>

Set crew assigned to as crew leader

</td><td>

Work Order Task\[wm\_Task\]

</td><td>

Sets the **Assigned to** field with the crew leader name when a task is assigned to a crew​.

</td></tr><tr><td>

Set skill level inherited to false

</td><td>

Crew Skill\[wm\_crew\_skill\]

</td><td>

Sets the **Skill Level Inherited** field to false.

</td></tr><tr><td>

Task crew - check leader available​

</td><td>

Crew \[wm\_crew\]

</td><td>

Checks the availability of the crew leader when assigning a task to the task-specific crew​.

</td></tr><tr><td>

Update crew effective dates​

</td><td>

Work Order Task\[wm\_Task\]

</td><td>

Sets the effective dates for crew members similar to the task start and end dates for task-specific crews.​

</td></tr><tr><td>

Update initiated from task

</td><td>

Crew\[wm\_crew\]

</td><td>

Updates the**Initiated from** field with the work order task number.​

</td></tr><tr><td>

Update task assignees for task crew​

</td><td>

Crew Member\[wm\_crew\_member\]

</td><td>

Adds or updates the task assignees in a work order task when the task is assigned to the task-specific crew.​

</td></tr><tr><td>

Update travel duration on crew tasks​

</td><td>

Work Order Task\[wm\_Task\]

</td><td>

Updates the travel duration for work order tasks that require a crew based on the value of the **Assigned Crew** field.

</td></tr><tr><td>

Validate Crew

</td><td>

Crew \[wm\_crew\]

</td><td>

Validates the crew details when the crew is created.​

</td></tr><tr><td>

Validate crew group delete

</td><td>

Crew Group\[wm\_crew\_group\]

</td><td>

Prevents the deletion of a crew group when an active member is in the crew from this group​.

</td></tr><tr><td>

Validate crew member effective dates

</td><td>

Crew Member\[wm\_crew\_member\]

</td><td>

Validates the effective from and effective to dates for crew members.

</td></tr><tr><td>

Validate crew size

</td><td>

Crew Requirement\[wm\_crew\_requirement\]

</td><td>

Validates the minimum and recommended crew size for a work order task​.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

