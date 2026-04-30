---
title: Quick start tests for Field Service Management
description: Validate that Field Service Management still works after you make any configuration change, such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Activate Field Service Management, Configuring Field Service Management, Field Service Management]
---

# Quick start tests for Field Service Management

Validate that Field Service Management still works after you make any configuration change, such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.

Field Service Management quick start tests are available when you enable the Field Service Management plugin \(com.snc.work\_management\). Enable the demo data plugin \(com.snc.work\_management.demo\) in a non-production instance to start using the quick start tests available with your application. Activate Field Service Contractor Management plugin \(com.snc.fsm\_contractor\_management\) to execute the External contractor related tests. You can also modify existing data and customize it to run the quick tests.

<table id="table_agf_nfg_h1c"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

FSM: Create Initiate Qualify Dispatch and assign Work Order Task

</td><td>

-   Create a work order.
-   Initiate and qualify a work order.
-   Dispatch a work order.
-   Assign a work order task to an agent.

</td><td>

Madrid

</td></tr><tr><td>

FSM: Part Sourcing

</td><td>

-   Source any part to an agent's stock room from the work order task.
-   Create a transfer order line for the part sourcing.
-   Use this part for any work order to consume it using the **Part Usage** action.

</td><td>

Madrid

</td></tr><tr><td>

FSM: Part Usage

</td><td>

-   Source any part to an agent's stock room from the work order task.
-   Use this part for any work order to consume it using the Part Usage action.

</td><td>

Madrid

</td></tr><tr><td>

FSM: Questionnaire

</td><td>

Create a questionnaire and associate it with a work order task.

</td><td>

Madrid

</td></tr><tr><td>

FSM: Field Service Configuration

</td><td>

Verify that the default configuration such as task assignment method, qualification requirement, PDF summary and agent's ability to accept or reject tasks is preserved.

</td><td>

New York

</td></tr><tr><td>

FSM: Planned Maintenance

</td><td>

Create a planned maintenance work order with weekly interval time for printer maintenance.

</td><td>

New York

</td></tr><tr><td>

FSM: Appointment Booking Configuration

</td><td>

Verify that the default configuration for appointment booking is preserved and that the point of sale service and catalog item exists in the system.

</td><td>

New York

</td></tr><tr><td>

FSM: Create Work or Personal Schedules

</td><td>

Create personal or work schedule for agents.

</td><td>

Orlando

</td></tr><tr><td>

FSM: Field Service Property Settings

</td><td>

Verify that the field service system properties preserve expected values.

</td><td>

Orlando

</td></tr><tr><td>

FSM: Work Groups

</td><td>

Verify that field service agents can be added to work groups.

</td><td>

Orlando

</td></tr><tr><td>

FSM: Dynamic Scheduling - Preferred Technician assignment with mandatory parts reservation

</td><td>

With Dynamic scheduling:-   Preferred technician should be picked for task assignment.
-   Mandatory parts should be reserved in the agent stock room.

 **Note:** Activate Customer service management demo data plugin.

</td><td>

Paris

</td></tr><tr><td>

FSM: Create Time Card

</td><td>

Verify that a time card is created for an agent in the work order task.

</td><td>

Quebec

</td></tr><tr><td>

FSM: Create incidental

</td><td>

Verify that an incidental is created for an agent in the work order task.

</td><td>

Quebec

</td></tr><tr><td>

FSM: Onboarding contractor company

</td><td>

Verify that a contractor company is onboarded with assignment group, external manager, and external agent.**Note:** Activate Field Service Contractor Management plugin.

</td><td>

Quebec

</td></tr><tr><td>

FSM: Onboarding contractor agent by external manager

</td><td>

Verify that an external contractor manager can onboard external agents from the Field Service Contractor Management portal.

</td><td>

Quebec

</td></tr><tr><td>

FSM: External contractor manager fulfil the work order task

</td><td>

Verify that a contractor manager or an agent is able to fulfil the assigned work order task.

</td><td>

Quebec

</td></tr><tr><td>

FSM: Assign work order task to Vendor group

</td><td>

Verify that a work order task is assigned to the external assignment group based on the defined criteria, such as task location and configuration parameters.

</td><td>

Quebec

</td></tr><tr><td>

FSM: Pause and Resume work order task

</td><td>

Verify that an agent can pause and resume work for a work order tasks.

</td><td>

Rome

</td></tr><tr><td>

FSM: Dynamic Scheduling - Assign technician with matching skills

</td><td>

With Dynamic Scheduling: Verify that a work order task is assigned to a technician who possesses all mandatory skills mentioned in the task.

</td><td>

Rome

</td></tr><tr><td>

FSM: Off boarding contractor agent by external manager

</td><td>

Verify that an external contractor manager can off board external agents from the Field Service Contractor Management portal.

</td><td>

Rome

</td></tr><tr><td>

FSM: External contractor manager asset sourcing and usage

</td><td>

Verify that an external contractor manager is able to perform the following actions: -   Request parts from stockroom.
-   Pick the part.
-   Close the transfer order.
-   Perform work using the part.

</td><td>

San Diego

</td></tr><tr><td>

FSM: External contractor agent fulfil the work order task

</td><td>

Verify that a contractor agent is able to fulfil the work order task that is assigned by the external contractor manager.

</td><td>

San Diego

</td></tr><tr><td>

FSM: Capacity Scheduling - Assign work to field service agents based on capacity

</td><td>

Verify that the rules and values mentioned in the capacity definition and capacity assignment module are evaluated to assign work to the agent based on capacity.

</td><td>

Tokyo

</td></tr><tr><td>

FSM: Onboarding external contractor agent as additional manager for the external assignment group

</td><td>

Verify that when onboarding an external agent for the contractor company, you can assign the additional manager role to the agent.

</td><td>

Tokyo

</td></tr><tr><td>

FSM: Dispatcher Workspace - Assign crews to work order tasks that require a group of agents to work on them

</td><td>

-   Verify that a dispatcher with the crew moderator role can create a crew in the Dispatcher Workspace.
-   Verify that a dispatcher with the crew moderator role can assign a work order task to the planned crew in the Dispatcher Workspace

</td><td>

Tokyo

</td></tr><tr><td>

FSM: Work order task supports Multi-day task scheduling

</td><td>

Verify the Multiday task scheduling functionality:-   Create Work order, work order task, and agent schedule records.
-   Select the Assign across schedule entries option in the work order task.
-   Assign an agent to the work order task for which the task duration is more than a day.
-   Verify that work order task is assigned successfully to the agent and the estimated end time is populated correctly.

</td><td>

Tokyo

</td></tr><tr><td>

Verify creating a work order from a case and assigning a work order task to an agent from CSM/ FSM Configurable Workspace

</td><td>

-   Verify you can create a work order from a case.
-   Qualify the work order and verify a work order task is created.
-   Assign the work order task to an agent and verify the agent it is assigned to is updated correctly.

</td><td>

Xanadu

</td></tr><tr><td>

FSM: Appointment Booking unified UI modal validation in platform

</td><td>

-   Create work order and work order task.
-   Launch Seismic Appointment Booking calender in Platform.
-   Verify that **Today** and **Next week** options displays the correct calender.

</td><td>

Yokohama

</td></tr><tr><td>

Create and qualify a work order, then assign the work order from Dispatcher Workspace as a dispatcher

</td><td>

-   As a dispatcher, from the CSM/FSM Configurable workspace go to the **List** view and create a new work order.
-   Then as an administrator, qualify the work order and verify if a work order task is created.
-   Then as a dispatcher, assign the work order task to a Field Service agent and verify the Assigned to field is update correctly.

</td><td>

Yokohama

</td></tr><tr><td>

Clone a work order task

</td><td>

-   From from the CSM/FSM Configurable workspace, open any work order task record page.
-   Select **Clone Work order task**, and verify that a new work order task is created with all details populated from the original work order task.

</td><td>

Yokohama

</td></tr></tbody>
</table>**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)

