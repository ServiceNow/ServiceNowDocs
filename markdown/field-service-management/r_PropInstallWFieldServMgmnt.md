---
title: Properties installed with Field Service Management
description: System properties provided with the Field Service Management application.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 20
breadcrumb: [Components installed, Reference, Field Service Management]
---

# Properties installed with Field Service Management

System properties provided with the Field Service Management application.

<table id="table_properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.ui.wm\_order\_activity.fields

</td><td>

Determines which fields are tracked in the activities list for work orders. The system automatically synchronizes the values in this property and the selections made by customizing activities.-   Type: String
-   Default value: opened\_by, work\_notes
-   Location: System Properties \[sys\_properties\] table

</td></tr><tr><td>

glide.ui.wm\_task\_activity.fields

</td><td>

Determines which fields are tracked in the activities list for work order tasks. The system automatically synchronizes the values in this property and the selections made by customizing activities.-   Type: String
-   Default value: work\_notes, assigned\_to
-   Location: System Properties \[sys\_properties\] table

</td></tr><tr><td>

work.management.agent.geo.history.update.duration

</td><td>

Set the duration \(in minutes\) of the latest system update that you want to consider for calculating the agent's geolocation history relative to current time. If the duration of the last geolocation history update is more than the duration set for this property, the system uses the agent's task or home location instead of the geolocation history to determine the agent's current location.-   Type: Integer
-   Default value: 240
-   Location: System Properties list

</td></tr><tr><td>

work.management.allow.doublebooking.dynamicscheduling

</td><td>

When set to true, dispatchers can double-book agents manually even when dynamic scheduling is enabled. -   Type: true/false
-   Default value: false
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

work.management.allow.auto.metric\_cleanup

</td><td>

The frequency in number of days that the metric instance table should be purged of [work order task](../../field-service-management/concept/close-wo-wot-mobile.md#) information to avoid an unnecessary amount of data in the table.-   Type: Integer
-   Default value: 365
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

work.management.default.end.time

</td><td>

Default end time for all work agents when no schedule is set, formatted in a 24-hour clock.-   Type: String
-   Default value: 17:00
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_fsm.set\_schedule\_lock\_by\_state

</td><td>

Determines the state to lock work order task and also prevents from reassignment. For example, you can set the work order tasks to automatically get locked when the state is **Assigned** and further excludes in automated scheduling mechanisms such as dynamic scheduling, intelligent task recommendations. -   Type: String
-   Default value: None
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_fsm.update\_potential\_assignment\_groups

</td><td>

Calculates and automatically populates the potential assignment groups. Updates the **wm\_work\_order\_task\_potential\_assignment\_groups** table with potential assignment groups for the work order task.-   Type: Boolean
-   Default value: No
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

**Note:** The **wm\_work\_order\_task\_potential\_assignment\_groups** table is populated only when:

-   The **sn\_fsm.update\_potential\_assignment\_groups** [system property](r_PropInstallWFieldServMgmnt.md) is set to true.
-   More than one assignment group is found for the location.
-   Territory model is inactive.

</td></tr><tr><td>

work.management.default.start.time

</td><td>

Default start time for all work agents when no schedule is set. This value sets the start time for a day other than the current day, when no scheduled task exists or is continued from the previous day. This property uses a 24-hour clock.-   Type: String
-   Default value: 08:00
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.allow.auto.timecard

</td><td>

Automatically create a time card for a work order task when the task is . Every time the task is resumed, the time taken to work on the task is recorded in the time card. The **Actual Work Duration** field captures the cumulative amount of time worked on the task.-   Type: true/false
-   Default value: false
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.allow.travel.task.timecard

</td><td>

Enables recording the amount of time an agent spent to execute a work order task. The time card is generated when an agent clicks **Start work**.-   Type: true/false
-   Default value: false
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

work.management.limit.location

</td><td>

By default, the list of available dispatch groups is filtered by their proximity to the work order task location. When this property is set to false, the system displays all dispatch groups for selection without considering location.-   Type: true/false
-   Default value: true
-   Location: **Field Service** &gt; **Administration** &gt; **Properties** &gt; **Dispatch Properties for Field Service**

</td></tr><tr><td>

work.management.max.agents.processed

</td><td>

Sets the maximum number of agents processed by auto-dispatch at a time. The system has an absolute limit of 300 agents and sets the value at that level. If you specify more than 300, then the system can’t auto-dispatch a task for a dispatch group that contains more agents than the value configured.-   Type: Integer
-   Default value: 100
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.work.spacing

</td><td>

Amount of time \(in minutes\) to add between the end of a task and the travel start of the next. An example of a valid time value is 10.-   Type: Integer
-   Default value: 0
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

com.snc.wm.wo.task\_window\_days

</td><td>

Default days for a window of a task.-   Type: Integer
-   Default value: 14
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.use.mandatory.skills

</td><td>

Enables the mandatory skills feature and indicates that the Task Skills \[task\_m2m\_skill\] table is being used for work orders and work order tasks. -   Type: true/false
-   Default value: false
-   Location: System Properties list

</td></tr><tr><td>

work.management.rejected.technician.duration

</td><td>

The number of hours after which a work order task can be dynamically scheduled to the agent who rejected the work order task.-   Type: Integer
-   Default value: 24
-   Location: System Properties list

</td></tr><tr><td>

skills\_management.migration

</td><td>

Lists the task tables to migrate to the Task Skills \[task\_m2m\_skill\] table when an admin runs the Migrate Skills to Task Skill M2M script. -   Type: choice list
-   Default value: wm\_task,customerservice\_case,wm\_order
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

com.snc.skills\_management.task\_skill\_migrated\_tables

</td><td>

Contains a list of tables for which the **Skills** field has already been migrated to the Task Skills \[task\_m2m\_skill\] table. If the table name is listed in this property, the data has been migrated and will not be migrated again. -   Type: choice list
-   Default value: none
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

work.management.assignment.ignoreTravelTimeCalculation

</td><td>

When set to true, ignores the travel calculation check for field service agents.-   Type: true/false
-   Default value: false
-   Location: System Properties list

</td></tr><tr><td>

sn\_fsm\_service\_loc.max\_new\_location\_per\_day

</td><td>

Sets the maximum number of new locations allowed per day for external users.-   Type: Integer
-   Default value: 10
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_fsm\_crew.work.management.allow.undersized.crew.taskassignment

</td><td>

Enables dispatchers to assign task to a crew manually even when the crew size doesn’t meet the minimum required agents criterion. -   Type: true/false
-   Default value: false
-   Location: System Properties list

</td></tr><tr><td>

work.management.optimization.conflict\_handling

</td><td>

Manages the assignment of tasks scheduled outside the agent working hours when optimizing the task route for agent. Choose any of the following route optimization behaviour to avoid conflicts that may occur due to the overflow tasks:-   stop\_action: Terminate the optimize route action and return the original route status to the agent.
-   unassign\_task: Unassign the tasks that are scheduled outside the agent working hours.
-   Extend\_tasks: Adjust the unassigned tasks towards the end of the agent schedule when optimizing the route based on tasks.

 -   Type: choice list
-   Default value: stop\_action
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_crew.default.duration.in.days.of.crew.member

</td><td>

Sets the default number of days that an agent is part of a crew.-   Type: Integer
-   Default value: 1
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_task\_grouping.log.verbosity

</td><td>

Logs the details of Dynamic Bundling. Registers information such as how many tasks were bundled, bundle task numbers, subtask numbers, policies, rules, and qualifiers used to created bundles.-   **Type**: choice\_list
-   **Default value**: OFF
-   **Location**: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

work.management.default.scheduled.start

</td><td>

Default scheduled start date added to work order task. If value set to false, then the scheduled start won't populate until tasks enter the scheduled state. If the value is set to true, then the schedule start will populate when tasks enter the pending dispatch state.-   **Type**: string
-   **Default value**: false
-   **Location**: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm.wm\_weekly\_resource\_span

</td><td>

Turns table denormalization for Field Service Management on or off.-   Type: true/false
-   Default value: true
-   Location: System Properties list \[sys\_properties\] table


**Warning:** Only system administrators should update this value.

</td></tr><tr><td>

sn\_fsm.wm\_weekly\_resource\_span.number\_of\_ weeks\_in\_past

</td><td>

The number of weeks in past that the denormalized table stores data. If you navigate past the default weeks in the past data is still available but isn’t retrieved from the denormalized table.You can store a total of 20 weeks worth of data in the flat table. This must include one week for the current week, and then the sum of past and future weeks together can’t exceed 19 weeks.

-   Type: string
-   Default value: 2
-   Location: System Properties list \[sys\_properties\] table


**Warning:** Only system administrators should update this value.

</td></tr><tr><td>

sn\_fsm.wm\_weekly\_resource\_span.number\_of\_weeks\_in future

</td><td>

The number of weeks in the future that the denormalized table stores data. If you navigate past the default weeks in the future data is still available but isn’t retrieved from the denormalized table.You can store a total of 20 weeks worth of data in the flat table. This must include one week for the current week, and then the sum of past and future weeks together can’t exceed 19 weeks.

-   Type: string
-   Default value: 8
-   Location: System Properties list \[sys\_properties\] table


</td></tr><tr><td>

Enable/Disable Onsite Check-in for Agents

</td><td>

Enables a substate on tasks to reflect when technicians arrive at locations.-   Type: Choice
-   Default value: Disabled
-   Location: **All** &gt; **Field Service** &gt; **Administration** &gt; **Configuration**

If enabled, you can set a value for any work order task.

</td></tr><tr><td>

sn\_schedule\_optim.schedule\_state\_type

</td><td>

Enables admin to adjust the drip feed requirements based on the number of tasks or the duration of the tasks.-   Type: Choice
-   Default value: duration

</td></tr><tr><td>

sn\_schedule\_optim.scheduled\_state\_count\_of\_task

</td><td>

Enables admin to control how many tasks are assigned to a technician at any given time.-   Type: Integer
-   Default value: 1

</td></tr><tr><td>

google.maps.map\_id

</td><td>

Enables Field Service Management to use the map ID for Google Maps used for cloud-based maps styling, vector map, advanced markers. You must obtain your own map ID, to do so visit [https://developers.google.com/maps/documentation/javascript/map-ids/get-map-id](https://developers.google.com/maps/documentation/javascript/map-ids/get-map-id).**Important:** You must add `FSM_Map` as the value to use advanced markers.

-   Type: String
-   Default value: `Blank`

</td></tr></tbody>
</table>## Properties for calculating estimated travel time and distance

<table id="table_orw_mrf_phb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

work.management.autodispatch.geolocation

</td><td>

Requires geolocation to be used to calculate the estimated travel time for dynamic scheduling and auto assignment of tasks.-   Type: true/false
-   Default value: true
-   Location: **Field Service** &gt; **Administration** &gt; **Properties** &gt; **Dispatch Properties for** Field Service Management

 **Note:** To use the Google Maps API with dynamic scheduling, you must also enable the **Use Google for travel time and traffic data** check box on the [Dynamic Scheduling Configuration](../../field-service-management/task/create-dynamic-scheduling-config.md#) form.

</td></tr><tr><td>

work.management.travel.calculation.dynamic\_scheduling

</td><td>

Uses the Google Maps API or straight-line estimates to calculate estimated agent travel time and distance to task locations when agents are assigned tasks using dynamic scheduling. -   Type: choice list
-   Default value: Use straight line estimate
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.travel.calculation.auto\_assignment

</td><td>

Uses the Google Maps API or straight-line estimates to calculate estimated agent travel time and distance to task locations when agents are assigned tasks using auto assignment. -   Type: choice list
-   Default value: Use Google Maps API
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.travel.calculation.manual\_assignment

</td><td>

Uses the Google Maps API, Beans.AI, or straight-line estimates to calculate estimated agent travel time and distance to task locations when tasks are manually assigned to agents. **Note:** Map providers operate on a bring your own license \(BYOL\) licensing model.

-   Type: choice list
-   Default value: Use straight line estimate
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.travel.calculation.route\_optimization

</td><td>

Uses the Google Maps API, Beans.AI, or straight-line estimates to calculate estimated agent travel time and distance to task locations when agent route is optimized.**Note:** Map providers operate on a bring your own license \(BYOL\) licensing model.

-   Type: choice list
-   Default value: Use Google Maps API
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.travel.calculation.bundle\_route\_optimization

</td><td>

Enables Route Optimization to optimize the subtasks within work order task bundles.-   **Type**: true/false
-   Default value: false
-   **Location**: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.travel.calculation.expected\_arrival

</td><td>

Uses the Google Maps API or straight-line estimates to calculate estimated agent travel time and distance between the task location and the agent's location when agent starts to travel. If an agent leaves before or after the Scheduled travel start time, then the Scheduled travel start, Scheduled start, Estimated end, and Estimated travel duration values for the task are updated.-   Type: choice list
-   Default value: Use Google Maps API
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

 **Note:** Select `Use Google API real time traffic` as the default value to calculate the agent's estimated time of arrival using the real-time traffic data.

</td></tr><tr><td>

work.management.travel.calculation.schedule\_assistant

</td><td>

Uses the Google Maps API, Beans.AI, or straight-line estimates to calculate estimated agent travel time and distance to task locations for assignment assistance calculation.-   Type: choice list
-   Default value: Use straight line estimate
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

use\_default\_duration

</td><td>

The create work order task form displays two fields, **Estimated travel duration** and **Estimated work duration**. For both the fields, the default duration is one hour, which is defined at the schema level, but the values can be changed manually in the form. If the property value is set to **false**, the work order task records the values overridden by the user in these fields. However, if the property value is set to **true**, these two fields retain their default values even if the user overrides them.-   Type: true/false
-   Default value: true
-   Location: System Properties list

</td></tr></tbody>
</table>## Part sourcing properties

<table id="table_ovq_jnw_b5b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Part Search Criteria

</td><td>

Sets the criteria to search parts. The stockrooms that contains the parts with the requested quantity appear per the selected search criteria.-   Type: choice list
-   Default value: No restrictions
    -   **No Restrictions**: Search all warehouse stockrooms and peers' personal stockrooms.
    -   **Only Assignment Group**: Search all stockrooms of the peer agents who are part of the assignment groups of the logged-in field service agent.
    -   **Only Preferred Stockrooms**: Search all preferred stockrooms of all the assignment groups irrespective of the radius mentioned in the logged-in agent's profile.
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Use part request approvals

</td><td>

Enables sending and receiving mobile notifications as field service agents request parts from peer agents.-   Type: Boolean
-   Default value: Yes
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Create part requests for part requirement sourcing

</td><td>

Creates a part request when a part is added to the part requirement.-   Type: Boolean
-   Default value: Yes
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr></tbody>
</table>## Geolocation properties

<table id="table_GeolocationProperties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

work.management.map.merge.task.agent.markers

</td><td>

Merges task and agent markers on geolocation maps with a new purple marker. When this property is true, agent and task markers that are close together are merged into a purple cluster that displays the count of both marker types. The pop-up information window for the purple marker displays the items for all agents and tasks. If this property is false, agents and tasks will only be gathered into their own clusters and not into the single, purple cluster.-   Type: true/false
-   Default value: false
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.evening.rush.hours

</td><td>

Evening rush hour span, formatted as 14:30-16:00. This property uses a 24 hour clock. All times are expressed as a range, separated by a dash with no spaces. Times not using this format are ignored. This property must be used with the **work.management.morning.rush.hours** and **work.management.rush.travel.buffer** properties.-   Type: String
-   Default: 0
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.morning.rush.hours

</td><td>

Morning rush hour span, formatted as 06:30-08:00. This property uses a 24 hour clock. All times are expressed as a range, separated by a dash with no spaces. Times not using this format are ignored. This property must be used with the **work.management.evening.rush.hours** and **work.management.rush.travel.buffer** properties.-   Type: String
-   Default: 0
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.rush.travel.buffer

</td><td>

Percentage to add to all rush hour travel times. The system uses this percentage to calculate schedules when optimizing task routes for agents. Use this property when both morning and evening rush hour times are defined. An example of a valid time buffer percentage is 15.-   Type: Integer
-   Default value: 0
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.travel.buffer

</td><td>

Percentage to add to all travel times. An example of a valid percentage value is 15.-   Type: Integer
-   Default value: 0
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.allow.toll.roads

</td><td>

Allows the system to use toll roads when auto-routing or optimizing task routes for agents.-   Type: true/false
-   Default value: true
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr></tbody>
</table>## Dynamic Scheduling properties

<table id="table_cn4_wck_fpb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

work.management.allow.doublebooking.dynamicscheduling

</td><td>

Enables dispatchers to double-book agents manually even when dynamic scheduling is enabled. -   Type: true/false
-   Default value: false
-   Location: **Field Service** &gt; **Dynamic Scheduling Administration** &gt; **Properties**

</td></tr><tr><td>

com.snc.dynamic.scheduling.ignoreAgentTravelTimeDuringScheduling

</td><td>

When this property is set to true, the agent's assigned tasks using dynamic scheduling no longer have an estimated travel time calculated.-   Type: true/false
-   Default value: false
-   Location: **Field Service** &gt; **Dynamic Scheduling Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.travel.calculation.dynamic\_scheduling

</td><td>

Uses the Google Maps API or straight-line estimates to calculate estimated agent travel time and distance to task locations when agents are assigned tasks using dynamic scheduling. -   Type: choice list
-   Default value: Use straight line estimate
-   Location: **Field Service** &gt; **Dynamic Scheduling Administration** &gt; **Properties**

</td></tr><tr><td>

com.snc.dynamic.scheduling.optimize\_travel\_time\_rating

</td><td>

Used to provide a more precise optimization rating for each work block for agents. Property includes work.management.morning.rush.hours and work.management.rush.travel.buffer.

 -   Type: Choice list
-   Default: include\_all\_travel
-   Location: **Field Service** &gt; **Dynamic Scheduling Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.distance.calculation.dynamic\_scheduling

</td><td>

Uses Google Maps API or straight line estimates to calculate estimated distance to task locations when agents are assigned tasks using dynamic scheduling. -   Type: choice list
-   Default value: Use straight line estimate
-   Location: **Field Service** &gt; **Dynamic Scheduling Administration** &gt; **Properties**

</td></tr><tr><td>

com.snc.dynamic.scheduling.showlogs

</td><td>

Enable this property to display recommended eligible agents to the dispatchers while scheduling the tasks using dynamic scheduling. -   Type: true/false
-   Default value: false
-   Location: **Field Service** &gt; **Dynamic Scheduling Administration** &gt; **Properties**

</td></tr><tr><td>

com.snc.dynamic.scheduling.bundle\_before\_scheduling

</td><td>

Ensures dynamic bundling runs before dynamic scheduling. Tasks in the Pending Dispatch state are bundled before running dynamic scheduling. -   **Type**: true/false
-   **Default value**: false
-   Location: **Field Service** &gt; **Dynamic Scheduling Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_fsm\_multiday.minDurationForFirstWorkSchedule

</td><td>

Set minimum work duration to be booked for the first work schedule of the task \(in minutes\).-   Type: integer
-   Default value: 60
-   Location: **Field Service** &gt; **Dynamic Scheduling Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.enable.optimizing.travel

</td><td>

Enables dynamic scheduling to reassign work order tasks to the nearest agent regardless of availability. -   Type: true/false
-   Default value: false
-   Location: **Field Service** &gt; **Dynamic Scheduling Administration** &gt; **Properties**

</td></tr><tr><td>

work.management.travel.time.threshold.minutes

</td><td>

Sets the travel time \(in minutes\) that assigns a work order task to the nearest agent if they are within the travel distance.-   Type: integer
-   Default value: 0
-   Location: **Field Service** &gt; **Dynamic Scheduling Administration** &gt; **Properties**

</td></tr></tbody>
</table>## Dispatcher Workspace properties

<table id="table_ndm_qzl_kbc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.agent\_metrics\_setting

</td><td>

Enable agent metrics settings.-   Type: true/ false
-   Default value: false
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.autorefresh

</td><td>

Enable auto-refresh.-   Type: true/ false
-   Default value: false
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.calendarDisplayDays

</td><td>

Default number of days dispatcher can view on calendar.-   Type: choice list
-   Default value: 7
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.calendar\_resources\_page\_size

</td><td>

Minimum number of resources to load on dispatcher workspace calendar. The value must be between 1 and 30.-   Type: integer
-   Default value: 15
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.cluster\_label

</td><td>

Set the label on marker clusters \(marker for number of markers, item for total number of items\).-   Type: choice list
-   Default value: \(blank\)
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.cluster\_zoom\_level

</td><td>

Set maximum auto zoom level for marker clustering. Valid values are 1 to 20.-   Type: integer
-   Default value: 15
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.dateTimeField

</td><td>

Select the date/time property to use for calendar navigation to task assignment window.-   Type: choice list
-   Default value: window\_start
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.enable\_straight\_line\_location\_history\_route

</td><td>

Enable simple straight line for drawing agent location history routes.-   Type: true/ false
-   Default value: true
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.enable\_straight\_line\_route

</td><td>

Enable simple straight line for drawing routes.-   Type: true/ false
-   Default value: false
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.event\_hover\_popover

</td><td>

Enable on event hover popover on the dispatcher workspace.-   Type: true/ false
-   Default value: true
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.firstDayOfWeek

</td><td>

Default first day of the week.-   Type: choice list
-   Default value: 1
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.group\_metrics\_setting

</td><td>

Enable group metrics setting-   Type: true/ false
-   Default value: false
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.hideOffShiftAgents

</td><td>

Enable hiding off shift agents-   Type: true/false
-   Default value: true
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.hideOffShiftAgents

</td><td>

Enable hiding off shift agents-   Type: true/ false
-   Default value: true
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.hide\_map

</td><td>

Hide Map.-   Type: true/ fasle
-   Default value: false
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.scheduled\_travel\_start\_as\_scheduled\_start

</td><td>

Schedule based on travel start time-   Type: true/ false
-   Default value: true
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.showIconOnCalendarEvent

</td><td>

Enable icon display on calendar event-   Type: true/ false
-   Default value: true
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.taskDateFieldToCalendarSync

</td><td>

Enable navigation to task assignment window.-   Type: true/ false
-   Default value: triue
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.task\_panel\_page\_size

</td><td>

Default page size of task panel on dispatcher workspace-   Type: choice list
-   Default value: 20
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.use\_task\_assignment\_modal

</td><td>

Enable task assignment modal.-   Type: true/ false
-   Default value: false
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.display\_map\_on\_assignment\_confirmation

</td><td>

Displays the map on task assignment confirmation in Dispatcher Workspace-   Type: true/ false
-   Default value: false
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.enable\_optimize\_route

</td><td>

Enable dispatcher workspace optimize route-   Type: true/ false
-   Default value: false
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.sn\_fsm.dispatch\_ws\_map.initial\_zoom\_level

</td><td>

Initial zoom level.-   Type: string
-   Default value: 5
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.sn\_fsm.dispatch\_ws\_map.map\_style

</td><td>

Apply a preferred style to light mode map.-   Type: string
-   Default value: \(blank\)
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.sn\_fsm.dispatch\_ws\_map.map\_style\_dark

</td><td>

Apply a preferred style to dark mode map.-   Type: string
-   Default value: \(blank\)
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.sn\_fsm.dispatch\_ws\_map.map\_type

</td><td>

Select the map type to view locations-   Type: choice list
-   Default value: roadmap
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.sn\_fsm.dispatch\_ws\_map.maximum\_auto\_zoom\_level

</td><td>

Set maximum auto zoom level. Valid values are 1 to 20.-   Type: string
-   Default value: 12
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.sn\_fsm.dispatch\_ws\_map.route\_enabled

</td><td>

Enable display of agent routes on the map.-   Type: true/ false
-   Default value: false
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.sn\_fsm.dispatch\_ws\_map.route\_type

</td><td>

Select map route type.-   Type: choice list
-   Default value: street\_level
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.sn\_fsm.dispatch\_ws\_map.street\_view\_enabled

</td><td>

Use street view on the map or use panoramas directly within the map-   Type: true/ fasle
-   Default value: true
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.use\_overlapping\_territory\_modal\_for\_opt

</td><td>

Use overlapping territory modal for optimization.-   Type: true/ false
-   Default value: false
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm.show\_paginated\_taskPanel\_markers

</td><td>

This toggle is to only show the paginated task panel task markers. Instead of displaying all the task panel task markers on the map.**Warning:** Setting this value to false will load all task markers at once which may cause performance issues.

-   Type: true/ false
-   Default value: true
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.task\_panel\_sla\_timer

</td><td>

Enable the SLA timer shown within the Work order task cards inside the Task Panel of Dispatcher Workspace.-   Type: true/ false
-   Default value: true
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.task\_panel\_sla\_timer\_type

</td><td>

Enable the SLA timer on work order task cards to update in real-time \(Live\) or update once on the initial Dispatcher Workspace load \(NonLive\).-   Type: choice list
-   Default value: NonLive
-   Location: System Properties list \[sys\_properties\] table


</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.show\_advanced\_resource\_filter

</td><td>

Property that controls the advanced resource filter in Dispatcher Workspace. When enabled dispatchers can use the advanced resource filter to create and save their own advanced filters. Administrators can setup advanced filters for all dispatchers to use.**Important:**

The advanced resource filter is only available for filtering agents and crews. If you currently use contractors or equipment, continue to use the default filter shown in the contextual side panel.

-   Type: true/ false
-   Default value: false
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.enableEmptyState

</td><td>

Property that controls if an empty state loads when Dispatcher Workspace opens. If true Dispatcher Workspace opens without Assignment Groups or Territories loaded until the dispatcher saves defaults.-   Type: true/ false
-   Default value: true
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

work.management.task\_state\_color.use\_hex

</td><td>

Enable administrators to use hex colors to update the colors on work order tasks in Dispatcher Workspace. The default value, false, doesn't allow for updating task state colors.

 -   Type: true/ false
-   Default value: false
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

work.management.enable.resource.time.indicator

</td><td>

Controls time zone display for work order task. When set to "true", date time fields show on record page forms, task assignment confirmation forms and the time indicator in Dispatcher Workspace is segmented and corresponds with the technician's time zone.

 -   Type: true/ false
-   Default value: false
-   Location: System Properties list \[sys\_properties\] table

</td></tr></tbody>
</table>## Database View

The Field Service Mobile plugin \(com.sn\_fsm\_mobile\) adds the Mobile live location database view. The Field Service Mobile plugin is activated when you activate the Field Service Management \(com.snc.work\_management\) plugin.

<table id="table_bcj_wq5_sxb"><thead><tr><th>

Database view

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mobile live location\[sn\_fsm\_mobile\_live\_location\_view​\]

</td><td>

Mobile live location of Field Service agents.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Field Service Management](r_InstalledWithFSM.md)

