---
title: Field Service Task Bundling fields
description: The fields that are included in the details section of work order task bundles.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Components installed with additional plugins for Field Service Management, Field Service Management reference, Field Service Management]
---

# Field Service Task Bundling fields

The fields that are included in the details section of work order task bundles.

<table id="table_hsq_4tg_mr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated identification number for the bundle.

</td></tr><tr><td>

Parent

</td><td>

Work order this bundle is assigned to.

</td></tr><tr><td>

Asset

</td><td>

Parts required to execute the bundle.

</td></tr><tr><td>

Location

</td><td>

Geographical area where the work must be done. The location of the subtask in the \#1 order position determines the bundle's location. If you want to update the location of a bundle, change the location of the subtask in the first position rather than updating the location on the bundle.

</td></tr><tr><td>

Template

</td><td>

Template for creating this work order task bundle.

</td></tr><tr><td>

Skills

</td><td>

Agent abilities necessary to execute the bundle.

</td></tr><tr><td>

Under warranty

</td><td>

Indicator of an existing warranty for one or more configuration items that are related to tasks in the bundle.

</td></tr><tr><td>

State

</td><td>

Current state of the bundle. The field is automatically set as the agent completes the work for each consecutive state.

</td></tr><tr><td>

Dispatch Group

</td><td>

Group that can select an agent to complete the bundle.

</td></tr><tr><td>

Assignment group

</td><td>

Group that contains the individual agent who will complete the bundle. By default, this field shows the recommended assignment groups based on the location, asset, and skills for the bundle. If the field is empty, the system searches for the group covering the territory that includes the location of the bundle.

</td></tr><tr><td>

Assigned to

</td><td>

Individual agent to complete the bundle.

</td></tr><tr><td>

Work Type

</td><td>

Type of work to be performed to complete the bundle. The following choices are available:-   **Break Fix**
-   **Install**
-   **Planned Maintenance**

</td></tr><tr><td>

Allow assignment override

</td><td>

Option to show all the groups in the **Assignment group** field that belong to the selected territory and dispatch group regardless of the location, assets, and skills required for the tasks in the bundle.

</td></tr><tr><td>

Schedule lock

</td><td>

Locks the bundle from being scheduled by any scheduling mechanism. Locked bundles are excluded from automated scheduling mechanisms such as dynamic scheduling or intelligent task recommendations. Dispatchers can manually assign the bundle to an agent.**Note:** Subtasks of a bundle will reflect the same lock value as the parent bundle.

</td></tr><tr><td>

Short Description

</td><td>

Brief description of the bundle.

</td></tr><tr><td>

Description

</td><td>

Technical description of the work to be performed containing as much detail about the problem as possible to avoid additional communication with the customer in later stages of the work order life cycle.

</td></tr><tr><td>

Work notes

</td><td>

Information about the bundle as it progresses through each state. Work notes aren’t visible to customers.

</td></tr><tr><td>

Comments

</td><td>

Any additional information about the task as it progresses. Comments are visible to customers.

</td></tr><tr><td class="sub-head" colspan="2">

Planned

</td></tr><tr><td>

Window start

</td><td>

Start of the time window that is established for this bundle.

</td></tr><tr><td>

Window end

</td><td>

End of the time window established for this bundle. The elapsed time of the window can’t exceed the value in the **Estimated work duration** field.

</td></tr><tr><td>

Scheduled travel start

</td><td>

Date and time when the agent expects to travel to the location of the first task in the bundle. The travel start time is automatically set to one hour from the current time.

</td></tr><tr><td>

Scheduled start

</td><td>

Date and time when the work on the bundle is expected to begin.This field becomes required after the bundle reaches the Assigned state.

</td></tr><tr><td>

Estimated end

</td><td>

Date when the work on the bundle ends. The date is automatically calculated based on the **Scheduled start** and **Estimated work duration** field values.

</td></tr><tr><td>

Is fixed window

</td><td>

Option to indicate that the service window is fixed. A fixed service window can’t be shortened, extended, or rescheduled to accommodate other tasks in an agent's schedule. If this option isn’t selected, the service window is considered flexible and can be rescheduled.

</td></tr><tr><td>

Access hours

</td><td>

Option to schedule work order tasks during the explicitly defined access hours.

</td></tr><tr><td>

Acceptance duration

</td><td>

Task acceptance duration in number of days and time.

</td></tr><tr><td>

Estimated travel duration

</td><td>

Estimated travel time to the work site. The duration is updated when you assign the bundle to an agent or change the start date and time of the bundle.

</td></tr><tr><td>

Estimated work duration

</td><td>

Estimated amount of work time. The duration can’t exceed the total time of the window.

</td></tr><tr><td>

Estimated travel home time

</td><td>

Estimated time it takes to get from the location of the last subtask in a bundle to the agent's home.

</td></tr><tr><td class="sub-head" colspan="2">

Actual

</td></tr><tr><td>

Actual travel start

</td><td>

Date and time when agent traveled to the site.

</td></tr><tr><td>

Actual work start

</td><td>

Time when work began.

</td></tr><tr><td>

Actual work end

</td><td>

Time when work on the bundle was completed.

</td></tr><tr><td>

Actual travel duration

</td><td>

Amount of time spent traveling to the site.

</td></tr><tr><td>

Actual duration

</td><td>

Total amount of time spent completing the bundle. This value is automatically calculated based on the **Actual work start** and **Actual work end** field values.

</td></tr><tr><td>

Actual work duration

</td><td>

Total amount of time spent on the bundle after the agent starts the work and before the agent closes the work on the last subtask. This amount excludes the time paused on the work.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

