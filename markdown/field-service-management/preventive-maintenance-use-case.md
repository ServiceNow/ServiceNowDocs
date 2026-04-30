---
title: Field Service preventive maintenance workflow example
description: This Field Service preventive maintenance workflow example provides an example of an aircraft maintenance manager setting up a maintenance plan to trigger a diagnostic alert after every 25 hours of flight time.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Example workflows, Explore, Field Service Management]
---

# Field Service preventive maintenance workflow example

This Field Service preventive maintenance workflow example provides an example of an aircraft maintenance manager setting up a maintenance plan to trigger a diagnostic alert after every 25 hours of flight time.

An aircraft maintenance manager, Lisa, sets up a maintenance plan to trigger a diagnostic alert after every 25 flight hours. Lisa found their paper-based planning processes inefficient and lacking real-time visibility. This led to grounded aircraft and financial losses. Implementing ServiceNow Field Service Management with Asset Management made a significant difference.

Now, Lisa automates maintenance plans for each aircraft, triggering alerts and generating work orders for diagnostic tasks after every 25 and 600 hours of flight time. The system assigns tasks to avionics field agents based on location, skills, and availability, ensuring the best-qualified and closest field agent is sent to avoid delays.

Field agents log in to accept or reroute tasks and view aircraft details, service history, and parts to be checked from the integrated asset management system. They can also view recommendations from articles and past work orders. When they complete diagnostic tasks, the system schedules the next maintenance tasks. All work order information is saved for analysis, reporting, audits, and compliance.

With Field Service Management, Lisa ensures passenger and crew safety, boosts revenue by optimizing aircraft availability, and meets compliance needs by reviewing work order data to spot trends.

## Field Service Preventive maintenance workflow diagram

![image.preventive-maintenance-use-case]

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

