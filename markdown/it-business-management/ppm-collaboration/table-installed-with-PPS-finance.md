---
title: Tables installed with PPM Standard \(Project Portfolio Management\)
description: Tables are added with activation of PPM Standard plugin.
locale: en-US
release: xanadu
product: PPM Collaboration
classification: ppm-collaboration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Components installed with Project Portfolio Management \(PPM\) Standard, Reference, Project Portfolio Management, Strategic Portfolio Management]
---

# Tables installed with PPM Standard \(Project Portfolio Management\)

Tables are added with activation of PPM Standard plugin.

## PPM Standard tables

PPM Standard adds the following tables.

<table id="table_PPSWithFin"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cost Plan \[cost\_plan\]

</td><td>

Cost plan for the resources required for the project.

</td></tr><tr><td>

Cost Plan Breakdown \[cost\_plan\_breakdown\]

</td><td>

Cost breakdown of resources based on project, program, or portfolio. These records are rollups of all costs. Project task cost plans are not rolled up to the project.

</td></tr><tr><td>

Cost Type Definition \[resource\_type\_definition\]

</td><td>

Definitions of cost types, which specify either an operating expense or capital expense, and can link accounts in the General Ledger \[itfm\_gl\_accounts\] table. The General Ledger table is installed with the Financial Management application.

</td></tr><tr><td>

Project Funding \[project\_funding\]

</td><td>

Project or demand target and budget expense values for both capital and operating expenses. The records in this table are for a single fiscal year.

</td></tr><tr><td>

Benefit Plan\[benefit\_plan\]

</td><td>

Benefit plan for the potential benefits that the project or demand can accrue.

</td></tr><tr><td>

Benefit Breakdown\[benefit\_plan\_breakdown\]

</td><td>

Benefit breakdown for the project or demand. These records are rollups of all benefits.

</td></tr><tr><td>

Budget Reference Rates\[itfm\_fx\_rate\]

</td><td>

The exchange rates that budgets use.

</td></tr></tbody>
</table>## Project Portfolio Suite tables

Project Portfolio Suite adds the following tables.

<table id="table_jvx_5cf_my"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Project Stakeholder\[pm\_m2m\_project\_stakeholder\]

</td><td>

Stores all stakeholders who are associated with one or more projects.

</td></tr><tr><td>

Project Time Card Exception\[project\_timecard\_exception\]

</td><td>

Stores time card information such as Week starts on, User, Project, and State of the time cards.

</td></tr><tr><td>

Project Time Category\[project\_time\_category\]

</td><td>

Stores project sub-categories created for time cards.

</td></tr><tr><td>

Time Sheet Exception\[time\_sheet\_exception\]

</td><td>

Stores time sheet information such as Week starts on, User, and State of the time sheets.

</td></tr></tbody>
</table>## Demand management tables

Demand management adds the following tables.

<table id="table_DemandManagement"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Demand \[dmn\_demand\]

</td><td>

Stores all demands.

</td></tr><tr><td>

Decision \[dmn\_decision\]

</td><td>

Stores all decisions.

</td></tr><tr><td>

Stakeholder Register \[dmn\_stakeholder\_register\]

</td><td>

Stores all stakeholders.

</td></tr><tr><td>

Requirement \[dmn\_requirement\]

</td><td>

Stores all requirements.

</td></tr><tr><td>

Demand Stakeholder \[dmn\_m2m\_demand\_stakeholder\]

</td><td>

Stores all stakeholders who are associated with one or more demands.

</td></tr><tr><td>

Demand Stage Config \[dmn\_stage\_config\]

</td><td>

Stores the images displayed in the demand stage pop-up window.

</td></tr><tr><td>

Idea \[idea\]

</td><td>

Stores all ideas.

</td></tr><tr><td>

Demand Task \[dmn\_demand\_task\]

</td><td>

Stores tasks associated with demands. Extends the planned\_task table to support demand-level task tracking and resource allocation.

</td></tr></tbody>
</table>## Project management tables

Project management adds the following tables.

<table id="table_ProjectManagement"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Goal \[goal\]

</td><td>

Project goals.

</td></tr><tr><td>

Issue \[issue\]

</td><td>

Project issues.

</td></tr><tr><td>

Personalize Workbench \[workbench\_config\_user\]

</td><td>

Configuration settings for each user that utilizes the workbench.

</td></tr><tr><td>

Portfolio \[pm\_portfolio\]

</td><td>

Portfolios.

</td></tr><tr><td>

Portfolio Project \[pm\_portfolio\_project\]

</td><td>

Portfolio projects.

</td></tr><tr><td>

Portfolio Project Goal \[pm\_portfolio\_goal\]

</td><td>

Portfolio project goals.

</td></tr><tr><td>

Portfolio Project Issue \[pm\_portfolio\_issue\]

</td><td>

Portfolio project issues.

</td></tr><tr><td>

Portfolio Project Relationships \[pm\_m2m\_portfolio\_project\]

</td><td>

All relationships between a portfolio and each project in the portfolio.

</td></tr><tr><td>

Portfolio Project Risk \[pm\_portfolio\_risk\]

</td><td>

Portfolio project risks.

</td></tr><tr><td>

Project \[pm\_project\]

</td><td>

All projects.

</td></tr><tr><td>

Project Task \[pm\_project\_task\]

</td><td>

All tasks used in projects.

</td></tr><tr><td>

Project Task Link \[pm\_project\_task\_link\]

</td><td>

All records for linked changes \(installed with the v3 plugin\).

</td></tr><tr><td>

Project Template \[project\_template\]

</td><td>

Project templates.

</td></tr><tr><td>

Project Template Configuration \[project\_template\_config\]

</td><td>

Configuration settings for project templates.

</td></tr><tr><td>

Project Template Task \[project\_template\_task\]

</td><td>

Tasks in project templates.

</td></tr><tr><td>

Risk \[risk\]

</td><td>

Project risks.

</td></tr><tr><td>

Project Change Request \[project\_change\_request\]

</td><td>

Project change requests.

</td></tr><tr><td>

Status Report \[project\_status\]

</td><td>

Project status reports.

</td></tr><tr><td>

Teamspace \[pm\_app\_config\]

</td><td>

All teamspaces, which refer to the tables that are created for the teamspaces. See [Installed with teamspaces](../../project-management/reference/r_InstalledWithTeamspaces.md) for a list of teamspace tables.

</td></tr><tr><td>

Planned task Relationship \[planned\_task\_rel\_planned\_task\]

</td><td>

Predecessor and successor tasks in a dependent relationship, including task lag values.

</td></tr><tr><td>

Baseline \[planned\_task\_baseline\]

</td><td>

All baselines.

</td></tr><tr><td>

Baseline Item \[planned\_task\_baseline\_item\]

</td><td>

All tasks that are part of baselines.

</td></tr><tr><td>

Task Relationship \[task\_rel\_task\]

</td><td>

Predecessor and successor tasks in a dependent relationship.

</td></tr><tr><td>

Planned task Recalculation Exclusions \[planned\_task\_recalculation\_exclusions\]

</td><td>

Defines tables that are excluded from recalculation \(start and end dates\). For example, the table is used for all sub tables under planned\_task to exclude tables from being recalculated. This table allows you to configure the tables from which you would not like to perform the recalculation from.

</td></tr></tbody>
</table>## Program management tables

Program management adds the following tables.

<table id="table_ProgramManagement"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Program Task \[pm\_program\_task\]

</td><td>

All the tasks in program

</td></tr><tr><td>

Program \[pm\_program\]

</td><td>

All programs

</td></tr></tbody>
</table>## Resource management tables

Resource management adds the following tables.

<table id="table_ResourceManagement"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group Resource Rolesgroup\_has\_resource\_role

</td><td>

Stores the resource roles for the groups with pps\_resource\_role. The roles in this table are populated from the User Resource Role \[user\_has\_resource\_role\] table of the users that are part of a group.The table is read-only.

</td></tr><tr><td>

Requested Allocation Daily\[requested\_allocation\_daily\]

</td><td>

Stores day-level breakdown for requested allocations.The table is read-only.

</td></tr><tr><td>

Resource Allocation\[resource\_allocation\]

</td><td>

Allocations for resources.

</td></tr><tr><td>

Resource Allocation Daily\[resource\_allocation\_daily\]

</td><td>

On a day-to-day basis, stores the events that are created through a resource plan. Also stores:-   User created calendar events as records.
-   Actual hours that a user has spent on a task, project, or any other type of activity, such as meeting or admin work.

</td></tr><tr><td>

Resource Aggregate Daily\[resource\_aggregate\_daily\]

</td><td>

On a day-to-day basis, stores aggregated values, such as capacity, allocated hours in a project, confirmed hours in a project, non-project time, actual hours, and availability of every user.This table is not enabled by default. To generate daily aggregates and store them in this table, create the **com.snc.resource\_management.generate\_daily\_aggregates** property and set the value to true.

</td></tr><tr><td>

Resource Aggregate Weekly\[resource\_aggregate\_weekly\]

</td><td>

On a weekly basis, stores aggregated values, such as capacity, allocated hours in a project, confirmed hours in a project, non-project time, actual hours, and availability of every user. The values in the table are asynchronously updated on every insert/update/delete to the Resource Allocation Daily \[resource\_allocation\_daily\] table.

</td></tr><tr><td>

Resource Aggregate Monthly\[resource\_aggregate\_monthly\]

</td><td>

On a monthly basis, stores aggregated values, such as capacity, allocated hours in a project, confirmed hours in a project, non-project time, actual hours, and availability of every user. The values in the table are asynchronously updated on every insert/update/delete to the Resource Allocation Daily \[resource\_allocation\_daily\] table.

</td></tr><tr><td>

Requested Allocation \[requested\_allocation\]

</td><td>

Allocations for resource plans.

</td></tr><tr><td>

Resource Event\[resource\_event\]

</td><td>

Stores events that are created for a user.

</td></tr><tr><td>

Resource Event Color \[resource\_event\_color\]

</td><td>

The colors that the application displays for each event type.

</td></tr><tr><td>

Resource Plan \[resource\_plan\]

</td><td>

All resource plans. These columns were added for Helsinki: `top_task`, `program`, `portfolio`.

</td></tr><tr><td>

Resource Plan Logs\[resource\_plan\_logs\]

</td><td>

Stores errors and warning that might occur during the resource allocation for a resource plan.

</td></tr><tr><td>

Resource Report \[resource\_report\]

</td><td>

Resource reports that you can generate and save.

</td></tr><tr><td>

Resource Report Chart \[resource\_report\_chart\]

</td><td>

This table is not used.

</td></tr><tr><td>

Resource Report Daily \[resource\_report\_daily\]

</td><td>

Daily resource reports that you can generate and save.

</td></tr><tr><td>

Resource Report Export \[resource\_report\_export\]

</td><td>

Saves JPG and PNG exports of resource management reports.

</td></tr><tr><td>

Resource Report Monthly \[resource\_report\_monthly\]

</td><td>

Monthly resource reports that you can generate and save.

</td></tr><tr><td>

Resource Role \[resource\_role\]

</td><td>

Stores project specific roles.

</td></tr><tr><td>

User Resource Role \[user\_has\_resource\_role\]

</td><td>

Stores the resource roles for a user.

</td></tr><tr><td>

User Calendar Event \[user\_calendar\_event\]

</td><td>

Stores events that are created in the calendar of a user.

</td></tr><tr><td>

User Schedule\[user\_has\_schedule\]

</td><td>

Stores the schedule for a user.

</td></tr></tbody>
</table>## Innovation management tables

Innovation Management adds the following tables.

<table id="table_innovation_management"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Idea\[im\_idea\_core\]

</td><td>

Default table which stores all the information related to the Idea portal. Extends the Task table.

</td></tr><tr><td>

Idea Category\[im\_category\]

</td><td>

Stores the list of static idea categories.

</td></tr><tr><td>

Idea Category Configuration\[im\_category\_config\]

</td><td>

Stores idea category definition information such as the table to use, field name, and hierarchy of the idea category. Also stores mapping information between idea categories table and the Idea module.

</td></tr><tr><td>

Idea Categories\[im\_m2m\_idea\_category\]

</td><td>

Stores mapping information between idea categories and ideas.

</td></tr><tr><td>

Idea Module\[im\_module\]

</td><td>

Configuration for the Idea portal such as module name, module id, and idea table to use. Create a separate table for each Idea module.

</td></tr></tbody>
</table>## Time card management tables

Time card management adds the following tables.

<table id="table_TimeCardManagement"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Time Card \[time\_card\]

</td><td>

Stores time logged by the user against a category such as a task, meeting, or training.

</td></tr><tr><td>

Time Sheet \[time\_sheet\]

</td><td>

Groups all time cards for the user for a week.

</td></tr><tr><td>

Time Sheet Policytime\_sheet\_policy

</td><td>

Stores all time sheet policies.

</td></tr><tr><td>

Time Card Daily\[time\_card\_daily\]

</td><td>

Stores the time logged in a time card on daily basis.

</td></tr></tbody>
</table>## Rate model tables

Rate model add the following tables.

<table id="table_RateModel"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rate Model\[rate\_model\]

</td><td>

Stores rate model definition.

</td></tr><tr><td>

Rate Model Entity\[rate\_model\_entity\]

</td><td>

List of entities from which the attributes can be selected.

</td></tr><tr><td>

Rate Model Entity Attribute\[rate\_model\_entity\_attribute\]

</td><td>

List of attributes in the entities.

</td></tr><tr><td>

Rate Model Line\[rate\_model\_line\]

</td><td>

Stores rate line values.

</td></tr><tr><td>

Rate Model Line Attribute\[rate\_model\_line\_attribute\]

</td><td>

Stores rate line attributes that are added from the entities.

</td></tr><tr><td>

Rate Line Import Set\[imp\_rate\_model\_line\]

</td><td>

Stores import sets that you imported into the instance.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Project Portfolio Management \(PPM\) Standard](r_InstalledWithProjectPortfolioSuiteWithFinancials.md)

