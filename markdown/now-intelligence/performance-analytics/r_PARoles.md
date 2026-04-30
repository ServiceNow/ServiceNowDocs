---
title: Performance Analytics roles
description: Assign roles to ensure that users can perform all necessary actions.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Performance Analytics reference, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Performance Analytics roles

Assign roles to ensure that users can perform all necessary actions.

## Roles and personas

**Warning:** Giving someone the pa\_admin or pa\_data\_collector role is equivalent to giving them admin, from a security perspective.

<table id="table_ydm_wzd_4v"><thead><tr><th>

Role

</th><th>

Authorizations

</th><th>

Typical persona

</th></tr></thead><tbody><tr><td>

No role

</td><td>

-   View Performance Analytics visuals on the Service Portal.
-   View dashboards that have been shared with this user.

Some dashboards require a subject matter related role for viewing, such as sn\_hr\_core\_basic for the HR Agent dashboard. Dashboard owners and administrators can also restrict dashboard access by role. For more information, see [Dashboard permissions](../../dashboards/concept/c_DashboardRoles.md).


</td><td>

Requester who does not need any access to Performance Analytics beyond certain visualizations of results

</td></tr><tr><td>

Any role \(not necessarily a Performance Analytics role\)

</td><td>

-   Create dashboards.
-   Restrict access by role to a dashboard they create.
-   Share dashboards they own.

</td><td>

 

</td></tr><tr><td>

pa\_viewerContained by: All roles except pa\_contributor

</td><td>

Before Quebec, this role was necessary for the following actions. It may still be necessary on upgraded instances.

-   View Analytics Hub.
-   Create personal thresholds and targets for indicators.
-   Read, Update, and Delete thresholds and targets that they created.
-   View text analytics widgets on dashboards.

</td><td>

Requester who needs and understands the details of key performance indicators

</td></tr><tr><td>

sn\_pa\_diagnostics.pa\_diagnosticContained by: pa\_admin

</td><td>

-   Read from the Diagnostics tables.
-   Activate or deactivate a diagnostic.
-   Run diagnostics.
-   Delete message records and diagnostic logs.

</td><td>

No specific persona, but this role would typically be assigned to individual business analysts or groups of fulfillers.

</td></tr><tr><td>

pa\_contributorContained by: pa\_power\_user, pa\_admin

</td><td>

For indicators for which the user is designated as a **Contributor**:-   Read and update scores in scoresheets.
-   View the Analytics Hub.

This user can also read dashboards that have been shared with them.

</td><td>

No specific persona, but this role would typically be assigned to individual fulfillers or groups, who are allowed to set indicator scores manually

</td></tr><tr><td>

pa\_kpi\_signal\_adminContained by: admin

</td><td>

Enables the user to dismiss a signal or reset the baseline for [KPI Signals](../../par-for-workspace/concept/process-behavior-charts-for-kpis.md).

</td><td>

Process owner who also has some training in Performance Analytics. Also needs the pa\_viewer role.

</td></tr><tr><td>

pa\_target\_adminContained by: pa\_power\_user, pa\_admin

</td><td>

-   Create targets.
-   Read, update, and delete all targets, including those that they do not own.
-   Assign targets to indicators.

</td><td>

Manager who knows what targets to set but may not have any further input to Performance Analytics

</td></tr><tr><td>

pa\_threshold\_adminContained by: pa\_power\_user, pa\_admin

</td><td>

-   Create global thresholds.
-   Read, update, and delete all thresholds, including those that they do not own.
-   Assign thresholds to indicators.

</td><td>

Manager who knows what thresholds to set but may not have any further input to Performance Analytics

</td></tr><tr><td>

pa\_analystContained by: pa\_power\_user, pa\_admin

</td><td>

-   CRUD text analytics keywords, phrases, and stop words
-   Read indicator sources.

</td><td>

No specific persona, but this role would be assigned to individual fulfillers or groups whose expertise includes keywords, phrases, and stop words for word clouds.

</td></tr><tr><td>

pa\_power\_userContained by: pa\_admin

 The pa\_power\_user role contains the viz\_admin, pa\_viewer, pa\_contributor, pa\_target\_admin, pa\_analyst, and pa\_threshold\_admin roles.

</td><td>

-   CRUD indicators and breakdowns.
-   CRUD widgets
-   Add Performance Analytics widgets to dashboards.
-   CRUD text index configurations for text analytics.
-   CRUD bucket groups.
-   CRUD indicator groups

</td><td>

Business analyst and visualization designer. Understands the use cases for Performance Analytics and the requirements for indicators and breakdowns.

</td></tr><tr><td>

pa\_data\_collectorContained by: pa\_admin

</td><td>

-   CRUD, schedule, and run [data collection jobs](../concept/performance-analytics-glossary.md#)
-   CRUD indicator and breakdown sources
-   Read some system properties
-   CRUD system units
-   CRUD scripts and automated notifications
-   CRUD bucket groups

</td><td>

Technical expert who understands the underlying database record structure of Performance Analytics

</td></tr><tr><td>

pa\_adminThe pa\_admin role contains the pa\_power\_user, sn\_pa\_diagnostics.pa\_diagnostic, viz\_admin, and pa\_data\_collector roles.

</td><td>

-   Read Performance Analytics properties.
-   Access Admin Console
-   Launch Dependency Assessment

</td><td>

Performance Analytics technical expert who also understands business needs.

</td></tr><tr><td>

admin

</td><td>

The system administrator role. Users with the admin role can perform all pa\_admin functions, edit properties, create [database views](../concept/performance-analytics-glossary.md#), CRUD any dashboard, and assign ownership to dashboards.

</td><td>

System administrator

</td></tr></tbody>
</table>## Spotlight roles

<table id="table_qrp_kxz_dhb"><thead><tr><th>

Role

</th><th>

Authorization

</th><th>

Typical persona

</th></tr></thead><tbody><tr><td>

pa\_spotlightContains: pa\_viewer, pa\_spotlight\_copy\_breakdown

</td><td>

CRUD Spotlight groups and criteria.

</td><td>

Expert who understands the business logic of what records require reminders.

</td></tr><tr><td>

pa\_spotlight\_viewer

</td><td>

Access to the dashboards from the Analytics and Reporting Spotlight Solutions.

</td><td>

Fulfiller who needs more than simple Priority setting to remind them of records that require action.

</td></tr><tr><td>

pa\_spotlight\_copy\_breakdown

</td><td>

Can copy Spotlight groups to multiple elements of a breakdown.

</td><td>

Spotlight expert or business analyst who understands the applicability of a Spotlight group by breakdown element.

</td></tr><tr><td>

pa\_spotlight\_copy\_domain

</td><td>

Can copy Spotlight groups to multiple domains

</td><td>

Domain administrator with Performance Analytics expertise

</td></tr></tbody>
</table>## Role hierarchy

Certain roles such as pa\_power\_user and pa\_admin include other roles. For example, pa\_power\_user includes pa\_contributor. This diagram shows the role hierarchy.

![The pa_admin role hierarchy.](../image/pa_role-hierarchy.png)

## Required roles for actions

<table id="table_sps_5pq_d2b"><thead><tr><th>

Module

</th><th>

Action

</th><th>

Minimal required role

</th></tr></thead><tbody><tr><td>

Admin Console

</td><td>

Access

</td><td>

pa\_admin

</td></tr><tr><td>

Analytics Hub \(Scorecards\)

</td><td>

View

</td><td>

None, since Quebec. However, upgraded instances may still require pa\_viewer.

</td></tr><tr><td>

Automated indicators

</td><td>

CRUD

</td><td>

pa\_power\_user

</td></tr><tr><td>

Automation schedules

</td><td>

Read and delete \(other security restrictions likely apply\)

</td><td>

pa\_data\_collector

</td></tr><tr><td>

Automation scripts

</td><td>

CRUD

</td><td>

pa\_data\_collector

</td></tr><tr><td>

Breakdowns and elements, including breakdown relations

</td><td>

CRUD

</td><td>

pa\_data\_collector or pa\_power\_user

</td></tr><tr><td>

Bucket groups

</td><td>

CRUD

</td><td>

pa\_data\_collector or pa\_power\_user

</td></tr><tr><td>

Color schemes for charts and targets

</td><td>

CRUD

</td><td>

pa\_power\_user

</td></tr><tr><td>

Dashboards \(Responsive or Platform Analytics\)

</td><td>

Create a dashboard. Update a dashboard they created, including restricting access by role.

</td><td>

Any roles necessary to access the data to display, or any one role

</td></tr><tr><td>

Responsive dashboards

</td><td>

Add Performance Analytics widgets to responsive dashboards you own.

</td><td>

pa\_power\_user

</td></tr><tr><td>

Dashboards \(Responsive or Platform Analytics\)

</td><td>

Read a dashboard that has been shared with you

</td><td>

No role by default, but dashboards can require roles to view their data. For more information, see [Dashboard permissions](../../dashboards/concept/c_DashboardRoles.md).

</td></tr><tr><td>

Dashboards \(Responsive or Platform Analytics\)

</td><td>

Update, delete, or share a dashboard that you own.

</td><td>

pa\_power\_user

</td></tr><tr><td>

Dashboards \(Responsive or Platform Analytics\)

</td><td>

Update, delete, or share any dashboard. Reassign ownership of any dashboard.

</td><td>

admin \(and dashboard role dashboard\_admin\)

</td></tr><tr><td>

Data collector jobs

</td><td>

Read, write, execute

</td><td>

pa\_data\_collector

</td></tr><tr><td>

Dependency assessment

</td><td>

Launch dependency assessment from indicator or breakdown form

</td><td>

pa\_admin

</td></tr><tr><td>

External indicators and breakdowns

</td><td>

CRUD

</td><td>

pa\_data\_collector or pa\_power\_user

</td></tr><tr><td>

Formula and manual indicators

</td><td>

CRUD

</td><td>

pa\_power\_user

</td></tr><tr><td>

Indicator Groups

</td><td>

CRUD

</td><td>

pa\_power\_user

</td></tr><tr><td>

Sources, either indicator or breakdown

</td><td>

CRUD

</td><td>

pa\_data\_collector

</td></tr><tr><td>

Indicator targets

</td><td>

Read and edit targets that you do not own

</td><td>

pa\_target\_administrator

</td></tr><tr><td>

Indicator targets or thresholds

</td><td>

Create new. Read or edit ones you own.

</td><td>

None, since Quebec. However, upgraded instances may still require pa\_viewer.

</td></tr><tr><td>

Indicator thresholds

</td><td>

Read and edit thresholds that you do not own

</td><td>

pa\_threshold\_administrator

</td></tr><tr><td>

In-form analytics

</td><td>

CRUD

</td><td>

pa\_power\_user

</td></tr><tr><td>

KPI Signals

</td><td>

Reset baseline or dismiss signal

</td><td>

pa\_kpi\_signal\_admin

</td></tr><tr><td>

Lists in all applications

</td><td>

Access an interactive analysis

</td><td>

No role by default, but some interactive analyses require roles to view their tables

</td></tr><tr><td>

Manage diagnostics

</td><td>

Read, execute, delete

</td><td>

sn\_pa\_diagnostics.pa\_diagnostic

</td></tr><tr><td>

Scheduled email summary jobs

</td><td>

CRUD

</td><td>

pa\_power\_user

</td></tr><tr><td>

Scoresheets

</td><td>

CRUD

</td><td>

pa\_power\_user

</td></tr><tr><td>

Service Portal

</td><td>

View Performance Analytics visuals

</td><td>

No role

</td></tr><tr><td>

System Properties

</td><td>

Edit

</td><td>

admin

</td></tr><tr><td>

System Properties

</td><td>

Read

</td><td>

pa\_data\_collector for some, pa\_admin for all

</td></tr><tr><td>

System Units

</td><td>

CRUD

</td><td>

pa\_data\_collector

</td></tr><tr><td>

Text Analytics

</td><td>

Set up text index configurations

</td><td>

pa\_power\_user

</td></tr><tr><td>

Text Analytics

</td><td>

View a text widget on a dashboard

</td><td>

None, since Quebec. However, upgraded instances may still require pa\_viewer.

</td></tr><tr><td>

Text analytics keywords, phrases, or stop words

</td><td>

CRUD

</td><td>

pa\_analyst

</td></tr><tr><td>

What's on the Move News Rules and Statistics Generators

</td><td>

Read, edit

</td><td>

pa\_power\_user

</td></tr><tr><td>

Visualizations that contain indicator information

</td><td>

CRUD

</td><td>

pa\_power\_user

</td></tr></tbody>
</table>**Parent Topic:**[Performance Analytics reference](../concept/performance-analytics-reference.md)

**Related topics**  


[Dashboard permissions](../../dashboards/concept/c_DashboardRoles.md)

[Administering reports](../../reporting/concept/c_AdminsteringReports.md)

