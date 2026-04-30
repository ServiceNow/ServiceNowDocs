---
title: Configuring Auto Assignment scheduling
description: The auto assignment feature can be enabled for requests or tasks, depending on the Service Management \(SM\) application's configuration settings.Automatically assign a task to a dispatch group when the Requests are assigned using auto-assignment option is set in the SM application's configuration.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Configuring Auto Assignment scheduling

The auto assignment feature can be enabled for requests or tasks, depending on the Service Management \(SM\) application's configuration settings.

When auto-assignment is enabled and a task is qualified or marked as **Ready for Work**, the system automatically assigns an appropriate agent to the task and moves it to the **Assigned** state. If the task can’t be auto-assigned, a user with the dispatcher role must adjust the values in the request, or task form and then save the record.

-   If the **Requests are assigned via auto-assignment** option is enabled, requests are automatically assigned.
-   If the **Tasks are assigned via auto-assignment** option is enabled, the tasks in a request are automatically assigned.

The system uses the following criteria to assign agents automatically.

<table id="table_inq_crd_lr"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Geolocation

</td><td>

You can configure whether an agent's home location should be considered when auto-assigning a task.To calculate the estimate time it takes for an agent to get to the task location, consider the following:

 -   If the **Use Google Maps API for travel time estimates** geolocation property is enabled, then you can select Google Maps API or straight-line estimates in the properties for calculating estimated travel time and distance.
-   If the **Use Google Maps API for travel time estimates** isn’t enabled, then the system uses the value in the Estimated Travel Duration field in the work order task to determine task assignment for the agent.
-   For more information, see [Components installed with Field Service Management](../../planning-and-policy/reference/r_InstalledWithFSM.md).

 **Note:** Set up the following configurations:

-   Enable **Use agent or task scheduling** to calculate the estimated time to arrive.
-   Enable **Auto-selection of agents will consider location of agents** to configure the agent’s home location.

For more information about enabling the configurations, see [Global domain configurations.](../../planning-and-policy/task/t_ConfigureFieldService.md)

</td></tr><tr><td>

Skills

</td><td>

You can configure whether an agent's skills should be considered when auto-assigning a task.If you’re assigning tasks to agents based on [mandatory skills](../../customer-service-management/concept/configure-mandatory-skills-feature.md) requirements, you can’t auto-assign tasks if the agent doesn't have the mandatory skills required to perform the task.

 **Note:** The work.management.use.mandatory.skills [system property](../../planning-and-policy/reference/r_InstalledWithFSM.md) must be enabled to configure the agent's skills.

</td></tr><tr><td>

Availability

</td><td>

Auto-assignment considers an agent's existing schedule when auto-assigning additional tasks.

</td></tr><tr><td>

Task windows

</td><td>

Auto-assignment attempts to schedule within configured task windows. If a window can’t be scheduled for any available agents, auto-assignment fails.

</td></tr><tr><td>

Task dependencies

</td><td>

Auto-assignment considers any upstream task dependencies when auto-assigning a task.

</td></tr><tr><td>

Agent schedules

</td><td>

Auto-assignment considers agents schedules from Workforce Optimization for Field Service application to auto-assign a task only if the **Enable Shift Scheduling for FSM to Determine Availability** property is enabled. For more information, see [Global domain configurations](../../planning-and-policy/task/t_ConfigureFieldService.md).

</td></tr></tbody>
</table>**Parent Topic:**[Additional scheduling configuration options](advanced-scheduling-and-dispatching-capabilities.md)

## Auto assignment of a request and a task

Automatically assign a task to a dispatch group when the **Requests are assigned using auto-assignment** option is set in the SM application's configuration.

### Before you begin

Role required: wm\_qualifier, wm\_initiator

### Procedure

1.  In any SM application, do one of the following:

    -   Open a request in the **Awaiting Qualification** state, or one that has been qualified automatically, and then open a task in the **Draft** state.
    -   Open a task in the **Ready for Work** state.
2.  Select an **Assignment group**.

3.  If the **Tasks are assigned via auto-assignment** and **Auto-selection of agents will consider location of agents** configuration options are set, enter a location.

    Auto-dispatch fails unless the task contains a valid location.

4.  If the **Tasks are assigned via auto-assignment** option is enabled, create a schedule for this task in the **Planned** section, or let the system determine the times.

    By default, ServiceNow enters the current date and time in the **Window start** field. If you don’t create a schedule or a fixed window, ServiceNow uses the **start** value to look for an agent who has that time slot open.

    For instructions, see [Creating Work Order Tasks](../../planning-and-policy/task/t_CreateAWorkOrderTask.md).

5.  Click **Qualified** or **Ready for Work**.

    The view returns to the previous page, and a success message appears. The system assigns an agent to the task, enters the agent's assignment group in the task record, and moves the state to **Assigned**.

    If auto-assignment fails, the message indicates either that no agent was available or that the task didn’t specify a location. The system moves tasks that fail auto-assignment to the **Remain in the Pending Dispatch** state.

6.  To auto-assign a task that failed previously, enter any missing information or change the schedule, and save the record.


