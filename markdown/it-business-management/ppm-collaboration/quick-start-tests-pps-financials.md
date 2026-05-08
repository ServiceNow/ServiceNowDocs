---
title: Quick start tests for Project Portfolio Management
description: Validate that Project Portfolio Management still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: PPM Collaboration
classification: ppm-collaboration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Project Portfolio Management reference, Project Portfolio Management, Strategic Portfolio Management]
---

# Quick start tests for Project Portfolio Management

Validate that Project Portfolio Management still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.

Project Portfolio Management quick start tests require activating the PPM Standard - ATF Tests plugin \(com.snc.financial\_planning\_pmo.atf\).

|Test|Description|Release version|
|----|-----------|---------------|
|PMO: Verify cost plan roll up to project/demand and program|Validate the total planned cost rollup from project and demand to program.|Madrid|
|PMO: Verify cost plan roll up to project/demand, program and portfolio|Validate the total planned cost rollup from project and demand to portfolio.|Madrid|
|PMO: Verify financials of Project created from Demand - Simple Financials|Validate the financial tab fields of a project created from a demand.|Madrid|
|PMO: Verify financials of Project created from Demand - With budget, cost plans, benefit plans|Validate the budget, cost plan, and benefit plan of a project created from a demand.|Madrid|
|PMO: Verify ETC/EAC at cost plan breakdown and project level|Validate the EAC and ETC values at cost plan breakdown and project level.|Tokyo|

|Test|Description|Release version|
|----|-----------|---------------|
|Validate state changes of Idea|Validate that the state of idea is changed when an idea is accepted, rejected, or any other task is created from an idea.|San Diego|

<table id="table_yct_vng_sjb"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

Validate PPM Cycle from Ideation to demand to project closure

</td><td>

Validate the flow of creating an idea, converting the idea to a demand, and then converting the demand to a project.**Note:** This test fails if the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is active.

</td><td>

Madrid

</td></tr><tr><td>

Validation of State and Date Rollup for Automatic Project

</td><td>

Validate the date and state rollup from tasks for a project of type Automatic.

</td><td>

Madrid

</td></tr><tr><td>

Validation of State and Date rollup for Manual Project

</td><td>

Validate the date and state rollup from tasks for a project of type Manual.

</td><td>

Madrid

</td></tr><tr><td>

Validation of project percent complete when all tasks are Closed Incomplete

</td><td>

Validate the project percent complete when all the tasks are closed as Closed Incomplete.

</td><td>

Orlando

</td></tr><tr><td>

Validate Project is not 100 percent complete if it has atleast one task as closed incomplete

</td><td>

Validate the project percent complete is not 100% when at least one of the tasks is closed as Closed Incomplete or Closed Skipped with task % complete less than 100%.

</td><td>

Orlando

</td></tr><tr><td>

Validate waterfall project does not show Agile Planning Board

</td><td>

Validate that the waterfall projects cannot use the following: -   Add stories or epics
-   Add agile phase
-   Access Agile board from the project

</td><td>

Orlando

</td></tr><tr><td>

Validate dates are rolled up from existing projects to program

</td><td>

Validate that the start and end dates of the project are rolled up to the program to which the project belongs.

</td><td>

Paris

</td></tr><tr><td>

Validate dates are rolled up from new projects to program

</td><td>

Validate that the start and end dates of a new project are rolled up to the program to which the project belongs.

</td><td>

Paris

</td></tr><tr><td>

Add projects and demands with risks or issues to program

</td><td>

Validate that the projects and demands with risks or issue records associated with them are added to the program.

</td><td>

Paris

</td></tr><tr><td>

Add projects and demands with benefit plans to program

</td><td>

Validate that the projects and demands with benefit plans associated with them are added to the program.

</td><td>

Paris

</td></tr><tr><td>

Add projects and demands with cost plans to program

</td><td>

Validate that the projects and demands with cost plans associated with them are added to the program.

</td><td>

Paris

</td></tr><tr><td>

Validate program dates on addition of existing demands

</td><td>

Validate that the start and end date of the program are adjusted on addition of an existing demand.

</td><td>

Paris

</td></tr><tr><td>

Validate program dates on addition of new demands

</td><td>

Validate that the start and end date of the program are adjusted on addition of a new demand.

</td><td>

Paris

</td></tr><tr><td>

Validate program state rollup

</td><td>

Validate that the program state is rolled up from state of all the projects in the program.

</td><td>

Paris

</td></tr><tr><td>

Verify Demand task due date column field value empty

</td><td>

Validate that the **Due date** field is empty for a new demand task.

</td><td>

Rome

</td></tr><tr><td>

Verify baseline is created on Project &amp; Demand when demand is converted to project

</td><td>

Validate that a project and demand baseline is created when a demand is converted to a project.

</td><td>

Rome

</td></tr><tr><td>

Verify timecard financial appears on Demand when time card submitted against demand task

</td><td>

Validate that the actual cost of the demand is updated when a time card is processed for a demand task.

</td><td>

Rome

</td></tr><tr><td>

Validate demand approved date

</td><td>

Validate that the approved dates for demand and the project created from the demand are the same.

</td><td>

Tokyo

</td></tr><tr><td>

Validate project preference "close project milestone tasks when they change to work state"

</td><td>

Validate that the milestone tasks are closed when their state is changed to Work in Progress after setting the project preference to "close project milestone tasks when they change to work state".

</td><td>

Tokyo

</td></tr><tr><td>

Validate project preference "Enable move project for WIP projects"

</td><td>

Validate that the project start date is changed appropriately for a project in WIP state when the project start date is changed after setting the project preference to "Enable move project for WIP projects".

</td><td>

Tokyo

</td></tr><tr><td>

Validate project preference "Rollup project start date from tasks"

</td><td>

Validate that the start date of a project task does not roll up to the project when the project planned dates are different than the project task start date after deselecting the project preference "Rollup project start date from tasks".

</td><td>

Tokyo

</td></tr></tbody>
</table><table id="table_xxp_gf5_ncc"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

Validate Planned start date of a project can be shifted by using the Move project action

</td><td>

Validate that the Planned start date of a project in Planning or Open state can be updated to a later or earlier date than the current planned start date using the Move project related link.

</td><td>

Orlando

</td></tr><tr><td>

Validate Move Project is disabled when Project is selected for execution

</td><td>

Validate that the Move Project option is not available if the Project is in Execution phase.

</td><td>

Orlando

</td></tr><tr><td>

Validate Move Project functionality with sprint dates populated for an agile phase

</td><td>

Validate that the sprint start and end dates are cleared when the project is moved using the Move Project related link.**Note:** This test is available only when Agile Development 2.0 plugin \(com.snc.sdlc.agile.2.0\) is activated.

</td><td>

Orlando

</td></tr><tr><td>

Validate Move Project functionality with external dependencies and related entities

</td><td>

Validate that the external dependencies and related entities are also shifted and redrawn when the project is moved using the Move Project related link.

</td><td>

Orlando

</td></tr><tr><td>

Validate Move Project functionality with different project states

</td><td>

Validate that the Move Project does not work when the project is in Work In Progress or Closed Complete state.

</td><td>

Orlando

</td></tr></tbody>
</table>|Test|Description|Release version|
|----|-----------|---------------|
|Verify RIDAC flow for Risk|Validate the RIDAC flow for a risk associated with a project.|Quebec|
|Verify RIDAC flow for Issue|Validate the RIDAC flow for an issue associated with a project.|Quebec|
|Verify RIDAC flow for Decision|Validate the RIDAC flow for a decision associated with a project.|Quebec|
|Verify RIDAC flow for Action|Validate the RIDAC flow for an action associated with a project.|Quebec|
|Verify changes in fields of risk form|Validate that any change is the Risk form fields such as Risk rank, Risk value, and Probability is updated successfully upon submission.|Quebec|

|Test|Description|Release version|
|----|-----------|---------------|
|Verify RIDAC flow for Risk|Validate the RIDAC flow for a risk associated with a demand.|Quebec|
|Verify RIDAC flow for Issue|Validate the RIDAC flow for an issue associated with a demand.|Quebec|
|Verify RIDAC flow for Decision|Validate the RIDAC flow for a decision associated with a demand.|Quebec|
|Verify RIDAC flow for Action|Validate the RIDAC flow for an action associated with a demand.|Quebec|
|Verify changes in fields of risk form|Validate that any change is the Risk form fields such as Risk rank, Risk value, and Probability is updated successfully upon submission.|Quebec|

<table id="table_bdt_vng_sjb"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

Verify user resource plan flow from Planned to Canceled state

</td><td>

Validate that the resource plan of a project can be moved to canceled state from planned state.

</td><td>

Madrid

</td></tr><tr><td>

Verify group resource plan flow from Planned to Complete state

</td><td>

Validate that the resource plan of a project can be moved to complete state from planned state.

</td><td>

Madrid

</td></tr><tr><td>

Verify role resource plan flow from Planned to Allocated state

</td><td>

Validate that the resource plan of a project can be moved to allocated state from planned state.

</td><td>

Madrid

</td></tr><tr><td>

Verify aggregated cost of all resource plans roll up to the corresponding project or demand fields

</td><td>

Validate that the aggregated cost of all resource plans on a project or demand roll up to the Planned Cost and Allocated Cost fields and the Resource Cost section of respective projects and demands.

</td><td>

Orlando

</td></tr><tr><td>

Verify Copy Resource plan option

</td><td>

Validate that the Copy Resource plan option creates an exact copy of the source resource plan in the Planning state

</td><td>

Orlando

</td></tr><tr><td>

Verify resource plan aggregate roll up from project/demand to program

</td><td>

Validate that the aggregated cost of all resource plans on a project or demand roll up to the total planned cost of the associated program.

</td><td>

Orlando

</td></tr><tr><td>

Verify records on completion of a resource plan

</td><td>

Validate the changes in a resource plan on completion:-   The state of the resource plan is updated to Completed.
-   If the completion date is earlier than the resource plan end date, the end date of the resource plan is updated with the completion date. If the completion date entered is later than the resource plan end date, the resource plan end date is retained.
-   All the requested and allocation records for the resource plan for the period after the completion date are deleted. If there are any actual hours logged against an allocation, that allocation is not deleted. For those allocation records, the allocated hours become zero and the actual hours are retained.
-   The available and allocated hours for resources are updated in the aggregate tables.

</td><td>

Orlando

</td></tr><tr><td>

Verify records on completion of a resource plan with Planned Duration as allocation type

</td><td>

Validate the following on completion of a resource plan with Planned Duration as allocation type:-   The state of the resource plan is updated to Completed.
-   Allocations are not deleted.
-   End date of the allocation is updated to the completion date.

</td><td>

Orlando

</td></tr><tr><td>

Verify the RP replan Capability

</td><td>

Validate that when a cancelled resource plan is re-planned, the state of the resource plan changes to Planning.

</td><td>

Orlando

</td></tr><tr><td>

Verify whether change in resource plan is reflected in corresponding cost plan

</td><td>

Validate that when a resource plan is updated, the corresponding cost plan is updated accordingly. For example, if the total planned cost is 500 USD, and the planned hours is 10, and you change the planned hours to 20, the total planned cost is updated to 1000 USD.

</td><td>

Paris

</td></tr><tr><td>

Resource-Test the default population of resource plan start &amp; end date

</td><td>

Validate the following on creating a user or group resource plan from the related list of a demand:-   If a demand is created without a start date and end date, the user or group resource plan has task as demand and no start and end date.
-   If a demand is created with a start date and end date, the user resource plan has task as demand and the start date and end date as added for the demand.

</td><td>

Paris

</td></tr><tr><td>

Validate that actual hours in operational resource plan and time card are equal

</td><td>

Validate that when a time card category is mapped with an operational work type, on submitting the time card for the operational resource plan associated with that work type, the actual hours in the resource plan and the time card are equal.

</td><td>

Quebec

</td></tr><tr><td>

Verify Resource plan auto population for Operational plans

</td><td>

Validate that the operational resource plans associated with a time card are automatically retrieved on the time card when time is logged.

</td><td>

Rome

</td></tr><tr><td>

Verify resource plan auto population for non-operational resource plans

</td><td>

Validate that the resource plans associated with a project, project task, or demand for a time card are automatically retrieved on the time card when time is logged.

</td><td>

Rome

</td></tr></tbody>
</table>**Parent Topic:**[Project Portfolio Management reference](../../../product/project-portfolio-suite-with-financials/reference/project-portfolio-management-reference.md)

**Related topics**  


[bundle-cadev.quick-start-tests]

