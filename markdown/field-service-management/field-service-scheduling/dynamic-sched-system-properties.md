---
title: Dynamic scheduling system properties
description: Set up properties to customize the behavior and functionality of the dynamic scheduling process according to your organization's needs.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Configuring Dynamic Scheduling, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Dynamic scheduling system properties

Set up properties to customize the behavior and functionality of the dynamic scheduling process according to your organization's needs.

The following properties allow you to control aspects such as the frequency of scheduling, automatic assignment, travel time calculations, and optimization iterations. Adjusting these properties helps optimize task assignments, improve efficiency, and align the dynamic scheduling process with your specific requirements.

Navigate to **All** &gt; **Field Service** &gt; **Dynamic Scheduling Administration** &gt; **Properties**.

<table id="table_fyv_dtr_bs"><thead><tr><th>

Property label

</th><th>

Property name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow dispatchers to manually double-book agents

</td><td>

work.management.allow. doublebooking.dynamicscheduling

</td><td>

Allows dispatchers to double-book agents manually even when dynamic scheduling is enabled. -   Type: true/false
-   Default value: false

</td></tr><tr><td>

Property to ignore calculation of travel time for agents to task location based on schedule

</td><td>

com.snc.dynamic.scheduling. ignoreAgentTravelTimeDuringScheduling

</td><td>

Assigns work order tasks automatically without considering travel time for agents. The **Ignore Travel** option appears in the work order task form, allowing dynamic scheduling to assign tasks to the highest ranked agents regardless of travel time.

Set up the following parameters related to dynamic scheduling when **Ignore Travel** is enabled:

**Note:**

-   Double booking must be enabled for the system to assign tasks to the agent automatically.
-   If access hours are defined in a work order task, the system ignores the defined access hours limit when auto-assigning that task to agents. Access hours are activated using Field Service Access Hours Management \(com.snc.fsm\_access\_hours\) plugin.

-   Type: true/false
-   Default value: false

</td></tr><tr><td>

Optimize work block travel time rating

</td><td>

com.snc.dynamic.scheduling.optimize\_travel\_time\_rating

</td><td>

Optimize work block travel time rating.-   Type: choice list
-   Default value: Include all travel

The following is more details on the property options:

-   **Include travel to task** - Ideal when on-time arrival is a key business metric. Only the time it takes to travel to the task is considered in the rating. Any travel after the task is ignored for scoring.
-   **Include travel after task** - Ideal when the order of tasks matters and incorrect sequencing could increase overall route time. This is best if you want to factor in the impact a task has on travel time to the next task. This method ignores how far the agent has to go to the task, but includes the impact that traveling to the task has on the rest of the route.
-   **Include all travel** - This is ideal for route efficiency if you want to minimize the total travel time across a technician’s day. This method considers both the travel to a task, and the travel after a task.
-   **Include no travel** - Ideal for remote tasks, virtual support, or dispatch scenarios where the technician is static since travel is not a factor in work block rating.

</td></tr><tr><td>

Travel calculation method

</td><td>

work.management.travel.calculation. dynamic\_scheduling

</td><td>

Uses Google Maps API, Beans.AI, or straight line estimates to calculate estimated agent travel time and distance to task locations when agents are assigned tasks using dynamic scheduling.

</td></tr><tr><td>

Distance calculation method

</td><td>

work.management.distance.calculation.dynamic\_scheduling

</td><td>

Calculates agent’s estimated travel time and distance to the task location based on either Google Maps API, Beans.AI, or straight-line.If the **Use Google Maps API for travel time estimates** geolocation property is enabled, then you can select **Google Maps API** or **straight-line estimates** in the properties for calculating estimated travel time and distance.

If the **Use Google Maps API for travel time estimates** is not enabled, then the system uses the value in the **Estimated Travel Duration** field in the work order task to determine task assignment for the agent.

-   Type: choice list
-   Default value: Use straight line estimate.

</td></tr><tr><td>

Show advanced agent recommendation logs to user

</td><td>

com.snc.dynamic.scheduling.showlogs

</td><td>

Displays recommended eligible agents to the dispatchers while scheduling the tasks using dynamic scheduling. Type: true/false Default value: false

</td></tr><tr><td>

Dynamic Bundling before Dynamic Scheduling

</td><td>

com.snc.dynamic.scheduling.bundle\_before\_scheduling

</td><td>

Ensures dynamic bundling runs before dynamic scheduling. Tasks in the Pending Dispatch state are bundled before running dynamic scheduling. -   Type: true/false
-   Default value: false

</td></tr><tr><td>

Enable the feature of assigning task to agent with travel time within threshold

</td><td>

work.management.enable.optimizing.travel

</td><td>

Enables dynamic scheduling to assign work order tasks to the nearest agent regardless of availability. -   Type: true/false
-   Default value: false

</td></tr><tr><td>

Assign task to agent with travel time within the threshold in minutes

</td><td>

work.management.travel.time.threshold.minutes

</td><td>

Sets the travel time \(in minutes\) that assigns a work order task to the nearest agent if they are within the travel distance.-   Type: integer
-   Default value: 5

</td></tr><tr><td>

Allow Dynamic Scheduling to only use work schedule/WFO

</td><td>

com.snc.dynamic.scheduling.useWorkScheduleOnly

</td><td>

Controls whether dynamic scheduling and workforce optimization can fall back to the default work schedule when scheduling agents. When set to `true`, the scheduling engine does not fall back to the default work schedule. When set to `false`, the scheduling engine falls back to the default work schedule if an agent's work schedule expires or is unavailable.-   Type: true/false
-   Default value: true

</td></tr></tbody>
</table>## Work Order Task Start and End Dates

Dynamic scheduling uses **Window start date** and **Window end date** field values in the work order task to schedule tasks. Additionally, the system properties, business rules, and client scripts are considered during set up and configuration.

-   If both the Window start and Window end dates are present in the work order tasks, dynamic scheduling uses these dates.
-   If the task has a Window start date but the date has passed, dynamic scheduling uses the current date and time for this value.
-   If the task has a Window start date but no Window end date, dynamic scheduling uses the com.snc.wm.wo.task\_window\_day property to determine this value.
-   If the task has no Window start date but has a Window end date, dynamic scheduling uses the current time for this value.
-   If the task has neither a Window start nor a Window end date, dynamic scheduling uses the current time and date for the Window start and the com.snc.wm.wo.task\_window\_day property for the Window end.
-   If a task is created, the Window end date gets automatically populated based on the latest SLA breach date from its parent work order. The business rules Populate Window End Based On SLA for both Task SLA \[task\_sla\] and Work Order Task \[wm\_task\] tables, and the client script Calculate Window End has to be set to true.
-   If a task is created and Fixed window is enabled, the business rules and client scripts doesn't execute and Window end time is not updated. If a work order is created based on an appointment and there is an SLA associated with the work order, the Window end time is populated based on the appointment and not on the SLA.

The **Window start date** field gets updated based on the delivery date of the transfer order only for the work orders that are not assigned. The business rule **Sync up Delivery Time with WOT** has to be set to **True**. For multiple transfer orders containing mandatory part requirements, the **Window start date** is set to the latest delivery time of the transfer order\(s\). Window start date is updated based on transfer orders only when the part requirement associated with the transfer order is mandatory. However, you can manually edit the window start time and override the existing date that is populated based on the transfer order.

**Note:** The Window start date is not updated if the work order task is one or more of the following:

-   Associated with an appointment
-   Fixed Window
-   Window end is populated and is before the delivery by date.

**Related topics**  


[Example - Dynamic Scheduling](../concept/example-for-dynamic-scheduling.md)

[Configure dynamic scheduling](../task/create-dynamic-scheduling-config.md#)

