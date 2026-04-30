---
title: Workforce Optimization for ITSM components
description: The Workforce Optimization for ITSM application has tables to store user and application data or database views and a schedule job to collect data for indicators.
locale: en-US
release: yokohama
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Workforce Optimization for ITSM reference, Advanced configurations for Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Workforce Optimization for ITSM components

The Workforce Optimization for ITSM application has tables to store user and application data or database views and a schedule job to collect data for indicators.

## Roles

To transition to the Workforce Optimization for ITSM base system roles, see [https://www.servicenow.com/community/workforce-optimization-blog/workforce-optimization-for-itsm-wfo-itsm-transitioning-to-the/ba-p/2995242](https://www.servicenow.com/community/workforce-optimization-blog/workforce-optimization-for-itsm-wfo-itsm-transitioning-to-the/ba-p/2995242)

<table id="table_fbd_qxp_dlb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Workforce Optimization User \[sn\_wfo.user\]

</td><td>

Grants read access to primary group and additional managers.

</td><td>

-   pa\_analyst
-   sn\_agent\_forecast.user
-   approver\_user

</td></tr><tr><td>

Workforce Optimization Admin \[sn\_wfo.admin\]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) additional managers.

</td><td>

-   sn\_wfo.user
-   pa\_analyst
-   sn\_agent\_forecast.admin

</td></tr><tr><td>

Workforce Optimization ITSM Employee \[sn\_wfo\_cfg\_itsm.employee\]

</td><td>

Grants read rights for Coaching, Scheduling and Teams applications.

</td><td>

-   sn\_wfo.user
-   sn\_shift\_planning.agent
-   sn\_coaching.trainee
-   sn\_team\_perf.team\_performance\_user
-   awa\_agent
-   canvas\_user
-   sn\_wfo\_skillreview.user

</td></tr><tr><td>

Workforce Optimization ITSM Manager \[sn\_wfo\_cfg\_itsm.manager\]

</td><td>

Grants rights to create, read, or update, Coaching, Scheduling, Teams, or Channel Management applications.

</td><td>

-   sn\_wfo\_cfg\_ws.manager
-   itil
-   sn\_walkup.walkup\_manager
-   sn\_agent\_forecast.user
-   sn\_shift\_planning.admin
-   sn\_coaching.coach
-   sn\_team\_perf.team\_performance\_manager
-   sn\_channel\_mgmt.user
-   sn\_sre.user
-   pa\_target\_admin
-   awa\_agent
-   skill\_manager
-   sn\_wfo\_skillreview.manager
-   sn\_wfo\_work\_sched.manager
-   sn\_cti\_core.user\_manager

**Note:** This role is automatically installed if you have integrated Workforce Optimization for ITSM with ServiceNow Voice.

-   sn\_process\_optimization\_analyst

</td></tr><tr><td>

Workforce Optimization ITSM Admin \[sn\_wfo\_cfg\_itsm.admin\]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) Coaching, Scheduling, Teams, or Channel Management applications.

</td><td>

-   sn\_wfo\_cfg\_itsm.manager
-   sn\_shift\_planning.admin
-   sn\_coaching.admin
-   sn\_team\_perf.team\_performance\_admin
-   sn\_agent\_forecast.admin
-   sn\_sre.admin
-   skill\_admin
-   sn\_process\_optimization\_analyst
-   sn\_wfo\_work\_sched.admin

</td></tr><tr><td>

Workforce Optimization for ITSM Manager base system role \[sn\_wfo\_cfg\_itsm.base\_manager\]

</td><td>

Grants access to the manager workspace landing page and the list module.

</td><td>

-   sn\_wfo\_cfg\_itsm.base\_employee
-   sn\_sre.user
-   pa\_target\_admin
-   skill\_manager
-   awa\_agent
-   sn\_walkup.walkup\_manager
-   sn\_wfo\_cfg\_ws.manager
-   survey\_creator

</td></tr><tr><td>

Workforce Optimization for ITSM Agent base system role \[sn\_wfo\_cfg\_itsm.base\_employee\]

</td><td>

Grants access to the Service Operations Workspace landing page.

</td><td>

-   canvas\_user
-   sn\_sow.sow\_user
-   sn\_wfo.user
-   awa\_agent
-   itil

</td></tr></tbody>
</table>## Filter Configuration Tables

<table id="table_ipf_lwt_jnb"><thead><tr><th>

Module Name

</th><th>

Module Tables / Database View

</th></tr></thead><tbody><tr><td>

Schedule

</td><td>

-   User \[sys\_user\]
-   User Skill \[sys\_user\_has\_skill\]
-   Agent Schedule \[sys\_shift\_planning\_agent\_schedule\]
-   Schedule Event \[sn\_shift\_planning\_event\]
-   Manager Groups database view \[sn\_wfo\_manager\_group\]

</td></tr><tr><td>

Coaching

</td><td>

-   Skill \[cmn\_skill\]
-   Skill Category M2M \[cmn\_skill\_m2m\_category\]
-   Group Member \[sys\_user\_grmember\]

</td></tr><tr><td>

Channels

</td><td>

Manager Groups database view \[sn\_wfo\_manager\_groups\]**Note:** The filters for your channels have been custom built so that you can navigate using Advanced Work Assignment channels and queues. Because they were custom built, you can't create or customize filters for channels module.

</td></tr></tbody>
</table>## Scheduled job

|Name|Description|
|----|-----------|
|WFO data collection|Runs the job on demand and collects data for all Workforce Optimization for ITSM indicators.|

**Parent Topic:**[Workforce Optimization for ITSM reference](workforce-optimization-itsm-reference.md)

