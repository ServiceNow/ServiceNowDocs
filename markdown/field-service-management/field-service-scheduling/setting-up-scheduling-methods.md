---
title: Setting up a Field Service scheduling method
description: In Field Service Management, a scheduling method is the process used to assign tasks to field technicians. As an administrator, you can choose the scheduling method that best meets your organization's needs.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Configure, Field Service Management]
---

# Setting up a Field Service scheduling method

In Field Service Management, a scheduling method is the process used to assign tasks to field technicians. As an administrator, you can choose the scheduling method that best meets your organization's needs.

## Configuration overview

1.  Choose and configure a scheduling method. Refer the following table to understand each scheduling method.

<table id="table_rgn_2hr_k1c"><thead><tr><th>

Scheduling Method

</th><th>

Key Features

</th></tr></thead><tbody><tr><td>

[Schedule Optimization](schedule-optimization-engine.md)

</td><td>

Schedule Optimization aims for global efficiency by minimizing driving time, balancing workloads, etc. Proactive and holistic policy-based engine that takes a snapshot of all assigned and pending tasks across all agents, analyzing multiple possibilities for task assignment. It runs as often as every 15 minutes, or can be triggered on demand from the Dispatcher Workspace.Considers all assigned and pending tasks across all agents, analyzing multiple possibilities for task assignment.

You can also use Intraday Optimization to re-optimize schedules in real-time based on changing conditions. Useful when tasks are canceled, delayed, or new tasks come in. For example: a cable service provider deals with last-minute cancellations and new installations.

</td></tr><tr><td>

[Dynamic Scheduling](Configure-dynamic-scheduling.md)

</td><td>

Dynamic Scheduling assigns tasks as they come in, checking agent schedules for availability. Examines each incoming task individually. If there's no free time, it swaps out less important tasks. It's a quick, task-by-task approach. Dynamic Scheduling can be set to run automatically at an interval or manually using the Auto Assign option. It works based on set criteria like skills and location. It's great for routine tasks and can adjust when things change, like when a tech is unavailable due to vacation or illness.

</td></tr><tr><td>

Manual Scheduling

</td><td>

Drag and drop method. Suitable for small teams with limited tasks but prone to errors

</td></tr><tr><td>

[Intelligent task recommendations](administer-task-recommendations.md)

</td><td>

Recommends tasks to fill gaps in agent's schedule. Maximizes agent productivity by utilizing available time. When Intelligent Task Recommendation is invoked in Dispatcher Workspace, any free time that agents have between tasks and events is displayed as white space in the agent's calendar. It recommends the best available tasks to fill these gaps in the schedule. This feature is available to both dispatchers in the Dispatcher Workspace and to field agents in the ServiceNow® Agent Mobile Application

</td></tr><tr><td>

[Route Optimization](configuring-route-optimization.md)

</td><td>

Route Optimization concentrates solely on minimizing travel time for a single agent. It does not consider swapping tasks between agents. However, Schedule Optimization looks at the entire schedule and considers swapping tasks between agents to make everything more efficient.Route Optimization is agent-centric and aims to reduce travel time for individual agents.

</td></tr></tbody>
</table>2.  Depending on the selected scheduling method, you can choose to set up the following additional scheduling and dispatching capabilities.

    | | |
    |---|---|
    |[Capacity Management](configuring-capacity-management.md)|Optimize workloads and prevent service outages through smart capacity rules. Capacity and Reservations Management allows Field Service managers to optimize workload distribution among agents and contractors. This is done through smart capacity rules, which prioritize tasks and prevent service unavailability due to overloading. For example, In the healthcare industry, a hospital can reserve 30% of their technicians' capacity for emergency equipment repairs, ensuring that crucial machinery like ventilators are always operational.|
    |[Crew Operations](configuring-crew-operations.md)|Field Service Crew Operations streamlines the scheduling process by allowing the creation of dedicated crews of Field Service agents. Crews can be repeatedly assigned to recurring tasks for a defined time period, enhancing operational efficiency. The crew leader can easily document each member's contributions via a mobile application. For example, In the utilities sector, a recurring monthly task to inspect and maintain power lines can be assigned to the same crew. This ensures familiarity with the equipment and terrain, improving the quality and efficiency of the work.|
    |[Equipment/Resource Scheduling](configure-equipment-scheduling.md)|Offers features like equipment categorization, availability calendars, and mobile tracking for equipment status. This ensures that crews have the right tools for the job, and equipment usage is efficiently managed. For example, In the construction industry, project managers can assign specialized equipment like cranes or excavators to specific crews. They can also set up availability calendars to prevent double-booking, thereby maximizing equipment utilization.|
    |[Appointment Booking](appointment-booking-administer.md)|With the appointment booking feature, customers can view available appointment windows, make a selection, and book a service appointment from the service portal. Agents and dispatchers can also book appointments on behalf of customers. Booking an appointment creates a work order and one or more work order tasks, depending on the type of service. Booked appointments can be rescheduled and canceled within time constraints identified in the configuration.|
    |[Contractor Management](configuring-fsm-contractor-management.md)|Field Service Contractor Management facilitates the outsourcing of work order tasks by seamlessly integrating third-party contractor companies into your ServiceNow workflow. This feature allows for dynamic assignment based on a variety of criteria, including skill sets and coverage areas. Contractor managers can review, accept, or reject tasks through a dedicated Contractor Portal. For example, In retail, during high-traffic seasons like holidays, a store can outsource inventory management tasks to external groups. If internal teams are already at capacity, the system can automatically route tasks to available contractors, ensuring SLAs are consistently met.|
    |[Task Bundling](configuring-fsm-task-bundling.md)|Dynamic Task Bundling allows administrators to create custom policies and rules that automatically group tasks, rising up the FSM efficiency. Automate task groupings through custom policies to increase efficiency. Ideal for large-scale operations for example, waste management, where task clustering can drive operational efficiency.|
    |[Configuring Multi-day scheduling](configuring-multi-day-scheduling.md)|Field Service Multi-Day Task Scheduling enables dispatchers to schedule tasks that span multiple days, accommodating the complexities of tasks that can't be wrapped up in a single work shift. The system considers agent availability, work hours, and even breaks to allocate tasks efficiently. It supports both manual and dynamic scheduling methods, allowing for flexibility in task assignments.|
    |[Field Service Marketplace](configuring-contractor-marketplace.md)|Contractor Marketplace enables dispatchers to push tasks to marketplace when internal agents are unavailable.|

3.  Optionally, set up one or more additional options to enhance your scheduling configuration tailored to optimize task allocation and agent assignments.

    | | |
    |---|---|
    |[Calculate travel time and location tracking of agents](google-maps-api-keys.md)|Set up properties to track field agents' locations in real-time to help estimate travel times accurately. Agents' locations are updated whenever they work on tasks, giving dispatchers current information. By default, updates happen every 5 minutes, but this can be changed. Dispatchers can manage these settings in Geolocation Properties. They can also check agent movements in Geolocation History. Agents need to enable location services and opt-in for tracking. Dispatchers can choose between Google Maps API, straight-line estimates, or Beans for travel time calculation. If Google Maps API is off, the system uses task estimates instead.|
    |[Business rules](../../planning-and-policy/reference/r_BRIWFieldServiceManagement.md)|Set up the business rules **Allow assignment override is updated** and **Populate Window End Based on SLA**, and **Sync up Delivery Time with WOT**.|
    |[Workforce Optimization for Field Service](configuring-wfo-fsm.md)|There are key differences in how agent schedules are defined and managed if you are using Workforce Optimization for Field Service. For example, when Workforce Optimization for Field Service is installed and ‘Shift Scheduling for FSM’ is enabled in the field service configuration, then schedules and shifts are managed using Manager Workspace.|
    |[Soft Booking](setting-up-soft-booking.md)|Soft booking allows dispatchers to schedule tasks without immediately triggering notifications and downstream workflows. When a task is soft booked, it's kept in a scheduling state. You can use Update task state from Scheduled to Assigned property to checks if the task is close to its start time. Once it reaches that time, the task is moved from the scheduling state to the assignment state, and notifications are then sent out.|


**Related topics**  


[Scheduling and dispatching work order tasks to agents](scheduling-and-dispatching-agents.md)

[Optimizing Scheduling and Dispatching operations](optimizing-scheduling-and-dispatching-operations.md)

