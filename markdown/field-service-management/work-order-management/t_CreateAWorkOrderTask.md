---
title: Create a work order task
description: Create work order tasks to define the technical details, skills, scheduling window, and resource requirements needed to complete a work order.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/work-order-management/t\_CreateAWorkOrderTask.html
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Manage work order tasks, Prepare work orders, Use, Field Service Management]
---

# Create a work order task

Create work order tasks to define the technical details, skills, scheduling window, and resource requirements needed to complete a work order.

## Before you begin

Role required: wm\_qualifier or [qualifier combination role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/r_UserRoleInstallWFieldSrvMgmnt.md)

## About this task

Use this procedure to create one or more work order tasks under a work order. Each task can be assigned to a different technician, location, or skill set, giving qualifiers the flexibility to coordinate complex work across multiple resources.

The following roles can edit schedule times, including task windows and planned durations, at different task states:

|Role|State|
|----|-----|
|wm\_qualifier|Draft|
|wm\_dispatcher|Pending Dispatch|
|wm\_admin|Draft or Pending Dispatch|
|wm\_task\_initiator|Draft|

**Note:** To create tasks from an applied template without qualifying the work order in the Draft state, you must enable the **Apply Work Order template in draft status** option and assign the **wm\_task\_initiator** role. For more information about these configurations, see [Global domain configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/t_ConfigureFieldService.md) and [Roles installed with Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/r_UserRoleInstallWFieldSrvMgmnt.md).

## Procedure

1.  Open a work order.

2.  Select the Work Order Tasks related list.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_hsq_4tg_mr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated identification number for the task.

</td></tr><tr><td>

Parent

</td><td>

Work order this task is assigned to.

</td></tr><tr><td>

Cloned from

</td><td>

Record number of the work order task that this task was cloned from, if any.

</td></tr><tr><td>

Priority

</td><td>

Priority of this task.

</td></tr><tr><td>

Asset

</td><td>

Parts required to execute the task.

</td></tr><tr><td>

Install base item

</td><td>

The install base item that user has issue with.

</td></tr><tr><td>

Location

</td><td>

Geographical area where the work needs to be done. The location is critical for determining the agent assigned to the task.If you don't want to use the auto-populated location, you can add an ad hoc location. For more information, see [Setting ad-hoc locations in work orders and work order tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/service-locations-work-orders.md).

</td></tr><tr><td>

Template

</td><td>

Template for creating this work order task. Select the lookup icon and select a template.

</td></tr><tr><td>

Skills

</td><td>

Abilities necessary to execute the task. This field is automatically set based on the values in the **Affected CI** field on the parent work order. If you change the affected CI on the work order,then any skills required by the new CI are added here.If you want to identify mandatory skills for technicians executing the tasks, configure the Work Order Task form to use the Task Skills table. For more information, see [Configuring mandatory skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/configure-mandatory-skills-feature.md).

</td></tr><tr><td>

Under warranty

</td><td>

Indicator of an existing warranty for one or more configuration items that are associated with the task.

</td></tr><tr><td>

State

</td><td>

Current state of the task. The field is automatically set as users complete the work for each successive state.

</td></tr><tr><td>

Sub state

</td><td>

Provides a more detailed status update within the broader **State** field.-   When a technician begins travel, the system automatically updates the sub state to **On Route**.
-   When a technician reaches the work location, the system automatically updates the sub state to **Onsite Arrival**.
These updates are triggered by geofencing technology or other location-based tracking methods.

</td></tr><tr><td>

Territory

</td><td>

When the Territory Planning is active and the territory model is enabled, the system automatically populates the best-matched territory based on the task's location. If there are multiple eligible territories, the system populates the highest priority territory. When the Field Service Territory plugin is installed, capacity and reservations are also taken into account.

</td></tr><tr><td>

Dispatch Group

</td><td>

Group that can select a technician to complete the task. By default, you can only select groups that belong to the location of the task. When no dispatch groups exist for the location, all dispatch groups are listed. When the Field Service territory model is enabled, the best-matched dispatch group is automatically populated based on the task's territory. For more information, see [Enable the Field Service territory model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/enable-territory-model.md).

**Note:** If multiple dispatch groups are populated, you must select one manually from the list.

</td></tr><tr><td>

Assignment group

</td><td>

Group that has the technician or vendor who will complete the task. By default, this field shows the recommended assignment groups based on the location, asset, and skills for the task. When the field is empty, the system searches for the group covering the territory that includes the location of the task. When multiple assignment groups are found, the system automatically populates the potential assignment groups.

This applies only when:-   The **sn\_fsm.update\_potential\_assignment\_groups** [system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/r_PropInstallWFieldServMgmnt.md) is set to true.
-   More than one assignment group is found for the location.
-   The territory model is inactive.


</td></tr><tr><td>

Assigned to

</td><td>

Technician, vendor, or crew assigned to complete the task.This field lists only the members who have the required skills, if defined. When no member has all the required skills, the field lists all members from the assignment group.

When the assignment group is of type **Vendor**, this field is automatically set to the vendor manager of the vendor group. When there is no manager, the field is empty.

When the **Needs crew** option is selected, this field name changes to **Assigned crew**.

</td></tr><tr><td>

Work Type

</td><td>

Type of work to be performed to complete the task. Select one of the following options:-   Break Fix — Unplanned work to repair or resolve an issue.
-   Install — Work to install or set up new equipment or components.
-   Planned Maintenance — Work to create, maintain, and schedule regular maintenance for equipment.


</td></tr><tr><td>

Agent efficiency criteria

</td><td>

Criteria used to accurately calculate the work duration for this task. When using automated scheduling methods such as Dynamic Scheduling or Intelligent Task Recommendation, this field is automatically populated. For manual scheduling, select a criteria from the list. **Note:** This field appears only when the Agent Efficiency plugin is activated and Agent Efficiency criteria are configured. For more information, see [Create or modify Agent Efficiency criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/create-or-modify-agent-efficiency-criteria.md).

</td></tr><tr><td>

Needs crew

</td><td>

Option to indicate that a crew is required to complete the task. When selected, the **Assigned to** field name changes to **Assigned crew**. **Note:** This option appears only when the Crew Operations plugin is activated.

</td></tr><tr><td>

Resource requirements

</td><td>

Option to add resources with specific skills to work on the tasks.This option displays only when the **Needs crew** option is selected.

</td></tr><tr><td>

Allow assignment override

</td><td>

Option to show all the groups in the **Assignment group** field that belongs to the selected territory and dispatch group irrespective of the location, assets and skills for the task.

</td></tr><tr><td>

Schedule lock

</td><td>

Locks the task from getting scheduled by any scheduling mechanism. Tasks that are locked are excluded from automated scheduling mechanisms such as Schedule Optimization, Dynamic scheduling, Intelligent task recommendations. However, dispatchers can manually assign the task to agent.Schedule lock only honors valid tasks. If a task is missing required information, it will not be locked. To verify the status of your tasks and ensure they have all necessary details, check the [Scheduling Health dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/scheduling-health-dashboard.md).

**Note:** Work order tasks that are marked for **Multi day**, **Needs crew**, or **Assigned/Accepted** state in sn\_fsm.set\_schedule\_lock\_by\_state [property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/r_PropInstallWFieldServMgmnt.md) are locked automatically for all scheduling mechanisms.

</td></tr><tr><td>

Potential territories for Schedule Optimization

</td><td>

When selected, considers the task for Schedule Optimization. The Schedule Optimization engine determines and assigns the best territory for the task.**Note:** Appears only when the Schedule Optimization is activated.

</td></tr><tr><td>

Assigned vendor

</td><td>

Individual vendor who should complete the task, selected from the **Assignment group**. This field is available only when **Vendor** is selected from the **Assignment group** field.

</td></tr><tr><td>

Vendor reference

</td><td>

Reference number for tracking the selected vendor's work activities. This field is available only when **Vendor** is selected from the **Assignment group** field.

</td></tr><tr><td>

Short Description

</td><td>

Brief explanation of the task.

</td></tr><tr><td>

Description

</td><td>

Exact technical description of the work to be performed. Provide as much detail about the problem as possible to avoid extra communication with the customer in later stages of the work order life cycle.

</td></tr><tr><td>

Work notes

</td><td>

Information about the task as it progresses through each state. Work notes are not visible to customers.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

Any additional information about the task as it progresses. Additional comments are visible to customers. Therefore update the details about the task as many times as necessary to correspond with the submitter of the task.

</td></tr><tr><td>

Check-In status

</td><td>

When an agent clicks the **Check-In** button at their designated work location, the system will automatically populate the **Check-In** status as **Geofence Validation Successful**. This status confirms that the agent has successfully entered the specified geofenced area associated with their work location. However, if agents bypass the check-in option, an appropriate status populates in this field.**Note:** This option appears only when you add to the form.

</td></tr><tr><td class="sub-head" colspan="2">

Planned

</td></tr><tr><td>

Window start

</td><td>

Start of the time window that is established for this task.

</td></tr><tr><td>

Window end

</td><td>

End of the time window established for this task. The elapsed time of the window cannot exceed the value in the **Estimated work duration** field.

</td></tr><tr><td>

Scheduled travel start

</td><td>

Date and time when the agent expects to travel to the site. The travel start time is automatically set to one hour from the current time. If the task is in the Pending Dispatch state, you can edit this field.

</td></tr><tr><td>

Scheduled start

</td><td>

Date and time when the work on the task is expected to begin.This field becomes mandatory from the Assigned state onwards.

 If you have enabled auto-assignment, the application auto-populates the **Start scheduled** field with the current date. Otherwise, you must enter the date manually.

</td></tr><tr><td>

Estimated end

</td><td>

Date when the work on the task will end. The date is automatically calculated based on the **Scheduled start** and **Estimated work duration**.

</td></tr><tr><td>

Window end buffer duration

</td><td>

Option to specify a time buffer that allows tasks to still be scheduled beyond the recorded window end. Adding a window end buffer duration doesn't change the recorded window end of the task, keeping reports accurate. If you enter a value that exceeds one day, the record is not saved and you receive an error message. For the buffer to take effect, the **Is fixed window** field must not be selected.

**Important:**

**Window end buffer duration** is only used by Schedule Optimization.

</td></tr><tr><td>

Is fixed window

</td><td>

Option to indicate that the service window is fixed. A fixed service window can't be shortened, extended, or rescheduled to accommodate other tasks in a technician's schedule. If not selected, the window is flexible and can be rescheduled. Fixed windows are excluded from route optimization and auto-assignment. If a fixed window task doesn't fit a technician's schedule, it isn't assigned.Set this field to false to enable the **Window end buffer** for Schedule Optimization. When configured, Schedule Optimization treats the window end as a soft constraint, keeping the task eligible for scheduling past the original window end.

</td></tr><tr><td>

Assign across the schedule entries

</td><td>

Option to schedule work order tasks spanning multiple schedule entries or days.This option appears only if the Field Service Multi-Day Task Scheduling plugin is activated.

</td></tr><tr><td>

Access hours

</td><td>

Option to schedule work order tasks during the explicitly defined access hours.This option appears only if the Field Service Management Access Hours Management plugin is activated.

</td></tr><tr><td>

Acceptance duration

</td><td>

Task acceptance duration in number of days and time.

</td></tr><tr><td>

Acceptance due date

</td><td>

Due date for the acceptance. This field is calculated based on the task assigned time and **Acceptance duration**.

</td></tr><tr><td>

Estimated travel duration

</td><td>

Estimated travel time to the work site. The duration is updated when you assign the task to an agent, change the order in which the task is executed, or change the start date and time of the task. This field is automatically set to an hour. It is calculated based on the agent's location and schedule. The agent can also manually update it. If the task is in the Pending Dispatch state, you can edit this field.

</td></tr><tr><td>

Estimated onsite buffer duration

</td><td>

Dispatchers can project duration required for agents to reach the designated work site. Indicates the approximate amount of time it will take for agents to arrive at the work site from their current location.

</td></tr><tr><td>

Onsite arrival geofence radius

</td><td>

The radius of a virtual fence or perimeter around the work site location. Specifies the distance from the center of the work site location to the outer boundary of a virtual geofence. The geofence acts as a boundary within which agents are considered to have arrived at the work site. Once agents enter this radius, it indicates their physical presence at the designated location.

</td></tr><tr><td>

Onsite arrival geofence distance unit

</td><td>

The unit used to measure the distance between an agent's current location and the work site location within a geofence. Indicates the unit of measurement utilized to quantify the distance between an agent's current position and the work site location within the geofence. Units are measured in kilometers and miles.**Note:** The **Onsite arrival geofence radius** and **Onsite arrival geofence distance unit** fields in the work order task are automatically populated with default values based on the configuration set in the OnsiteGeofenceConfig extension point. For more information, see [Extension points in Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/extension-points-field-service.md).

</td></tr><tr><td>

Planned work duration

</td><td>

Expected amount of work time irrespective of the agent assigned to the work order task. The default duration is set to an hour.This field appears only if Field Service Agent Efficiency is activated. This field can be updated only if the work order task is not assigned.

</td></tr><tr><td>

Estimated work duration

</td><td>

Estimated amount of work time. The duration cannot exceed the total time of the window. This field is automatically set to an hour. If the task is in the Draft or Pending Dispatch states, you can edit this field.**Note:** If Field Service Agent Efficiency is activated, Estimated work duration is automatically calculated based on the Agent Efficiency.

</td></tr><tr><td class="sub-head" colspan="2">

Actual

</td></tr><tr><td>

Actual travel start

</td><td>

Date and time when agent traveled to the site.

</td></tr><tr><td>

Actual travel duration

</td><td>

Amount of time spent traveling to the site.

</td></tr><tr><td>

Actual onsite arrival

</td><td>

The precise time at which an agent physically arrives at the designated work site.

</td></tr><tr><td>

Actual onsite arrival buffer duration

</td><td>

Automatically populates the duration of time an agent spends at the work site before commencing actual work. Represents the amount of time agents remains at the work site after their arrival but before they begin performing their assigned tasks.

</td></tr><tr><td>

Actual work start

</td><td>

Time when work began. This field is available only when the **Actual travel start** field is manually added, or when the **Start Travel** button is clicked.

</td></tr><tr><td>

Actual work end

</td><td>

Time when work on the task was completed.

</td></tr><tr><td>

Actual travel duration

</td><td>

Amount of time spent traveling to the site.

</td></tr><tr><td>

Actual duration

</td><td>

Total amount of time spent completing the task. This value is automatically calculated based on the **Actual work start** and **Actual work end** times.

</td></tr><tr><td>

Actual work duration

</td><td>

Total amount of time spent on the task after you start the work and before you close the work on the task. This amount excludes the time paused on the work.

</td></tr><tr><td class="sub-head" colspan="2">

Scheduling

</td></tr><tr><td>

Scheduling preference

</td><td>

Preferred method by which work order tasks are prioritized during scheduling. The options available are:-   Prioritize Rating
-   Prioritize ETA
-   Prioritize Nearest


</td></tr><tr><td>

Scheduling method

</td><td>

Scheduling method used to assign the work order task such as Schedule Optimization, intelligent task recommendation, dynamic scheduling, route optimization, or manual assignment.

</td></tr><tr><td>

Allow overtime

</td><td>

Authorizes additional work time that exceeds the regular working hours.

</td></tr><tr><td>

Optimization value

</td><td>

Value that is utilized to guide the Schedule Optimization engine in prioritizing a task for scheduling purposes. Higher numbers indicate higher priority.

</td></tr><tr><td>

Penalty due

</td><td>

Due date marking the commencement of penalties for Schedule Optimization on the engine. This date is automatically populated when there is an active Task SLA on the task. This date can be added or changed manually.

</td></tr><tr><td>

Penalty fixed cost

</td><td>

Total fixed penalty cost incurred after the penalty due date has passed.

</td></tr><tr><td>

Penalty per minute cost

</td><td>

Penalty cost incurred every minute after penalty due date has passed. The penalty due date must be entered. If the penalty due field is empty, the fixed cost will be used.

</td></tr></tbody>
</table>    **Important:** Value and penalty fields are used for Schedule Optimization

5.  Click **Submit**.

    The work order task is created.


## Result

When a work order task is created, customers receive SMS and email notifications. If the task is in a territory and **sn\_fsm.use\_query\_rules** is enabled, only linked agents, dispatchers, and qualifiers can see it. Access is based on entitlement, controlled by administrators through **sn\_fsm.use\_query\_rules** system property.

