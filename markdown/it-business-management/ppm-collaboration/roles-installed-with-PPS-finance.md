---
title: Roles installed with PPM Standard \(Project Portfolio Management\)
description: Roles are added with activation of PPM Standard plugin.
locale: en-US
release: xanadu
product: PPM Collaboration
classification: ppm-collaboration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Components installed with Project Portfolio Management \(PPM\) Standard, Reference, Project Portfolio Management, Strategic Portfolio Management]
---

# Roles installed with PPM Standard \(Project Portfolio Management\)

Roles are added with activation of PPM Standard plugin.

## Project Portfolio Suite roles

Project Portfolio Suite adds the following roles.

<table id="roles_PPS"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Portfolio manager\[it\_portfolio\_manager\]

</td><td>

Has access to all portfolios. Has the same access permissions as a project user and a demand user. Also has budget owner role is added as part of Financial Management.

</td><td>

-   it\_demand\_user
-   it\_project\_manager
-   it\_project\_user
-   portfolio\_manager
-   it\_demand\_manager
-   it\_project\_portfolio\_user

</td></tr><tr><td>

PPS admin\[it\_pps\_admin\]

</td><td>

Can view and modify the preferences, configurations, and settings for projects, demands, programs, portfolios, resources, time cards, agile development, and timeline visualization.

</td><td>

-   it\_program\_manager
-   it\_portfolio\_manager
-   it\_project\_manager
-   it\_demand\_manager
-   pps\_admin
-   timeline\_admin
-   rate\_model\_admin

</td></tr></tbody>
</table>## Demand management roles

Demand management adds the following roles.

<table id="roles_DemandMgmt"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Demand manager\[it\_demand\_manager\]

</td><td>

Can access all the modules of the Demand Management application.

</td><td>

-   it\_project\_user
-   resource\_user
-   timeline\_user
-   demand\_manager
-   it\_demand\_user
-   rate\_model\_user

</td></tr><tr><td>

Demand user\[it\_demand\_user\]

</td><td>

Can access the Demand and Stakeholders modules of the Demand Management application.

</td><td>

-   demand\_user
-   pps\_resource

</td></tr></tbody>
</table>## Project management roles

Project management adds the following roles.

<table id="roles_ProjectMgmt"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Portfolio user\[it\_project\_portfolio\_user\]

</td><td>

User who can view IT Portfolio Project records.

</td><td>

project\_portfolio\_user

</td></tr><tr><td>

Project user\[it\_project\_user\]

</td><td>

Can only view Project form fields. Can modify additional fields on the Project Task form, such as **Time constraint** and **State**.

</td><td>

-   it\_project\_portfolio\_user
-   project\_user

</td></tr><tr><td>

Project manager\[it\_project\_manager\]

</td><td>

Has access to all Project Management application features and functionality. This role enables project managers to create and manage projects, tasks, and resource plans. For configuration access to modify application settings and preferences, use the PPS admin \[it\_pps\_admin\] role instead.

</td><td>

-   resource\_user
-   it\_demand\_manager
-   it\_project\_user
-   project\_manager

The project\_manager role also contains the timecard\_approver role.

-   timeline\_user
-   rate\_model\_user

</td></tr></tbody>
</table>## Program management roles

Program management adds the following roles.

<table id="roles_ProgramMgmt"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Program manager\[it\_program\_manager\]

</td><td>

Program managers have access to all programs.

</td><td>

-   resource\_user
-   it\_project user
-   program\_manager
-   it\_demand\_user

</td></tr></tbody>
</table>## Resource management roles

Resource management adds the following roles.

<table id="roles_ResourceMgmt"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Resource manager\[resource\_manager\]

</td><td>

Users with this role can: -   Review resource plans, confirm, and allocate resources to tasks.
-   Create skills and view them in the User Skills list.
-   Read schedules.
-   Create a group of type pps\_resource.
-   Add users to or remove them from any groups.
-   Update group name, group email, parent, description, manager, average daily FTE hours/hours per person day, and hourly rate.

</td><td>

-   resource\_user
-   timecard\_approver
-   skill\_admin
-   rate\_model\_user

</td></tr><tr><td>

Resource user\[resource\_user\]

</td><td>

Users with this role can create resource plans and request resources. Project managers are typically given this role. Resource users cannot make changes to plans in the Confirmed or Allocated state.

</td><td>

None

</td></tr><tr><td>

PPS resource\[pps\_resource\]

</td><td>

Only users with the PPS Resource role are considered for resource planning, and only users or groups with the PPS resource role appear in resource plans.

</td><td>

None

</td></tr></tbody>
</table>## Innovation management roles

Innovation Management adds the following roles:

<table id="roles_innovation_management"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Idea admin\[idea\_admin\]

</td><td>

-   Creates idea module.
-   Defines idea categories.
-   Configures mapping of idea categories with idea module.
-   Manages ideas and creates tasks such as story, epic, feature, project, or demand from an idea.

</td><td>

idea\_manager

</td></tr><tr><td>

Idea manager\[idea\_manager\]

</td><td>

Manages ideas and creates tasks such as project or demand from an idea.

</td><td>

None

</td></tr><tr><td>

Idea manager professional\[idea\_manager\_professional\]

</td><td>

Manages ideas and creates tasks such as story, epic, feature, project, or demand from an idea.

</td><td>

None

</td></tr></tbody>
</table>## Time card management roles

Time card management adds the following roles.

<table id="roles_TimeCardMgmt"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Time card admin\[timecard\_admin\]

</td><td>

Has write access to all time cards.

</td><td>

-   timecard\_user
-   timecard\_approver

</td></tr><tr><td>

Time card approver\[timecard\_approver\]

</td><td>

Approves or rejects time cards for time card users.

</td><td>

timecard\_user

</td></tr><tr><td>

Time card user\[timecard\_user\]

</td><td>

Creates time cards for self.

</td><td>

None

</td></tr></tbody>
</table>## Rate model roles

<table id="table_t4p_vmt_gfb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Rate model admin\[it\_rate\_model\_admin\]

</td><td>

Manages rate models and rate lines. Has all privileges within rate model, including configuring attributes, export and import of rate lines, and administration.

</td><td>

-   rate\_model\_user
-   import\_set\_loader
-   import\_transformer
-   import\_admin

</td></tr><tr><td>

Rate model user\[rate\_model\_user\]

</td><td>

View rate model and rate lines.

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Project Portfolio Management \(PPM\) Standard](r_InstalledWithProjectPortfolioSuiteWithFinancials.md)

