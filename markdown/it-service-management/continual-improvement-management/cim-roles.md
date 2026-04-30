---
title: CIM roles
description: Roles are added with installation of Continual Improvement Management.
locale: en-US
release: yokohama
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Continual Improvement Management reference, Continual Improvement Management, IT Service Management]
---

# CIM roles

Roles are added with installation of Continual Improvement Management.

<table id="table_wq3_tps_ycb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Improvement Requester\[sn\_cim.improvement\_requester\]

</td><td>

Can perform the following application functions:-   Create improvement initiative
-   View and track improvement initiatives they've submitted
-   View all CIM requests within the organization
-   Follow and monitor improvements by adding them to the Watched CIM Initiatives list

</td><td>

None

</td></tr><tr><td>

Improvement Coordinator\[sn\_cim.improvement\_coordinator\]

</td><td>

Can perform Improvement Manager functions for improvements that they’re assigned to as Improvement Coordinator. -   Coordinate improvements within their area of expertise at the process or service level
-   Access the Continual Improvement Workbench

 Improvement Coordinators can’t perform these functions:

-   Create enterprise strategies
-   Delete improvement

</td><td>

-   sn\_cim.improvement\_requester
-   app\_service\_user
-   certification
-   cmdb\_query\_builder
-   dependency\_views
-   itil

Problem/change/incident records can be added.

-   knowledge
-   pa\_analyst
-   pa\_contributor
-   pa\_power\_user

Can assess existing Performance Analytics indicators and create new ones.

-   pa\_target\_admin
-   pa\_threshold\_admin
-   pa\_viewer
-   sn\_bm\_client.benchmark\_data\_viewer
-   sn\_bm\_client.benchmark\_recommendation\_viewer

Can view Benchmarks data and recommendations and create improvement initiatives from Benchmarks recommendations.

-   template\_editor
-   view\_changer
-   sn\_coaching.admin
-   scrum\_story\_creator

</td></tr><tr><td>

Improvement Manager\[sn\_cim.improvement\_manager\]

</td><td>

Can perform all application functions and is responsible for all improvements.-   Accept new improvement requests
-   Assign improvements to Improvement Coordinators for implementation
-   Access the Continual Improvement Workbench
-   Monitor the progress of improvements
-   Review and close improvements

</td><td>

-   sn\_cim.improvement\_coordinator
-   sn\_process\_optimization\_viewer

</td></tr></tbody>
</table>For information about assigning user roles, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Automatic assignment of the Improvement Requester role

The Improvement Requester \(sn\_cim.improvement\_requester\) role is automatically assigned to the roles listed in the following table when CIM is activated.

<table id="table_cfn_yvb_zdb"><thead><tr><th>

Application

</th><th class="sub-head">

Role

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Strategic Portfolio Management \(only if SPM plugins are active\)

</td></tr><tr><td>

Agile Development

</td><td>

scrum\_master

</td></tr><tr><td>

Demand Management

</td><td>

it\_demand\_manager

</td></tr><tr><td>

Portfolio Management

</td><td>

it\_portfolio manager

</td></tr><tr><td>

Program Management

</td><td>

it\_program\_manager

</td></tr><tr><td>

Project Management

</td><td>

it\_project\_manager

</td></tr><tr><td>

Test Management

</td><td>

tm\_test\_manager

</td></tr><tr><td class="sub-head" colspan="2">

ITSM

</td></tr><tr><td>

Benchmarks

</td><td>

-   sn\_bm\_client.benchmark\_admin
-   sn\_bm\_client.benchmark\_recommendation\_viewer

</td></tr><tr><td>

Change Management

</td><td>

change\_manager

</td></tr><tr><td>

Coaching

</td><td>

sn\_coaching.admin

</td></tr><tr><td>

Incident Management

</td><td>

incident\_manager

</td></tr><tr><td>

ITSM

</td><td>

itil

</td></tr><tr><td>

Survey ManagementAssessments

</td><td>

-   survey\_admin
-   survey\_reader

</td></tr><tr><td class="sub-head" colspan="2">

Performance Analytics and Reporting

</td></tr><tr><td>

Performance Analytics

</td><td>

-   pa\_admin
-   pa\_power\_user
-   pa\_viewer

</td></tr></tbody>
</table>## Email notifications by role

Email notifications are sent when the state of the improvement request changes or when the target date is breached based on the user role.

|Improvement action|Improvement Manager|Improvement Coordinator|Improvement Requester|Watch list|Task assignee|
|------------------|-------------------|-----------------------|---------------------|----------|-------------|
|Canceled|No|Yes|Yes|Yes|No|
|Approved|Yes|Yes|No|Yes|No|
|Closed|Yes|Yes|Yes|Yes|No|
|Target review date is breached|Yes|Yes|No|Yes|No|
|CIM task assigned|No|No|No|No|Yes|
|CIM task closed|No|Yes|No|No|Yes|

**Parent Topic:**[Continual Improvement Management reference](cim-reference.md)

