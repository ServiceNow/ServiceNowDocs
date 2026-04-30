---
title: Field Service preventive maintenance workflow example
description: This Field Service preventive maintenance workflow example provides an example of an aircraft maintenance manager setting up a maintenance plan to trigger a diagnostic alert after every 25 hours of flight time.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Field Service Management workflow examples, Exploring Field Service Management, Field Service Management]
---

# Field Service preventive maintenance workflow example

This Field Service preventive maintenance workflow example provides an example of an aircraft maintenance manager setting up a maintenance plan to trigger a diagnostic alert after every 25 hours of flight time.

As an aircraft maintenance manager, Lisa was dissatisfied with their paper-based aircraft maintenance planning processes. Coordinating schedules and spreadsheets for multiple aircraft was time-consuming, and Lisa had no real-time visibility into the status of each aircraft and availability of technicians. As a result, Lisa's aircraft company was losing money because airplanes were grounded for maintenance when they could have been in service.

Implementing ServiceNow Field Service Management with Asset Management changed all that.

Now, Lisa works with the administrator to automate maintenance plans for each aircraft. The plans trigger diagnostics alerts and automatically generate work orders for a different set of diagnostic tasks after every 25 and 600 hours of flight time for each aircraft. The work orders contain the diagnostic tasks appropriate for each type of aircraft.

Field Service Management automatically assigns tasks to avionics technicians based on their location, skills, and availability. Technicians log in to accept or reroute each task, and to view aircraft details, service history, and parts to be checked from the integrated Asset Management system.

Technicians can also view recommendations from knowledge articles and previous work orders. When a technician marks diagnostic tasks as complete, Field Service Management automatically schedules and assigns the work order tasks for the next maintenance appointment. The system saves all the information for the work order to support future analysis, reporting, audits and compliance activity.

Field Service Management enabled Lisa to maintain a high level of safety for passengers and crew, while helping to generate more revenue by optimizing aircraft availability for more flights. In addition, Lisa can review work order data to discover maintenance trends and patterns, and to satisfy compliance requirements.

-   **Key benefits**
    -   Keep assets operating to keep your business running.
    -   Avoid delays in completing maintenance or diagnostic tasks by automatic assignment of the best qualified and closest technicians.
    -   Prevent issues by executing planned regular maintenance work orders.
-   **User roles**
    -   Initiator -– Aircraft maintenance manager
    -   Field Service agent
-   **Products**
    -   Asset Management
    -   Field Service Management

## Field Service Preventive maintenance workflow diagram

![Preventive maintenance workflow in Field Service Management](../image/FSM-preventative-maintenance-asset0012977final.png)

## Field Service Preventive maintenance workflow steps

The following table provides the steps for the Field Service preventive maintenance workflow.

|Steps|Description|
|-----|-----------|
|1. Define workflow|The aircraft maintenance manager creates a maintenance plan and schedules maintenance, for example, so that diagnostic verification must be completed before 60 hours and more extensive checks performed every 200 hours, depending on the aircraft type.|
|2. Auto-generate work orders|The maintenance plan automatically creates one or more work orders when a trigger threshold is met. Templates containing the appropriate series of repeatable tasks for each aircraft type are used to create tasks for each work order. These tasks are assigned automatically to agents based on their location, availability, and skills.|
|3. Notify technician|The field agent is notified about the task assignment. The agent can log in to see and accept \(or reroute\) the task that needs to be executed to finish the maintenance diagnostic.|
|4. Provide comprehensive maintenance|With integrated Asset Management, the agent can see asset details, such as subcomponents, service history, and information on which parts need to be replaced or serviced. In addition, the technician can get recommendations, directions, tips from knowledge articles, and information from previous work orders to help complete the task.|
|5. Complete the work order tasks|Once the technician finishes the maintenance and updates the task, the next planned maintenance appointment is scheduled and assigned automatically.|
|6. Provide audit trail|All completed tasks and data are tracked in the maintenance plan records for future reference, so administrators can easily pull data needed for trend analysis, reports, and audits to satisfy compliance requirements.|
|7. Report and analyze|Track tasks and data in a maintenance plan to support future analysis, reporting, audits, and compliance activity.|

**Parent Topic:**[Field Service Management workflow examples](fsm-use-cases.md)

