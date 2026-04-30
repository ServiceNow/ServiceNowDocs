---
title: Roles in Service Operations Workspace for ITSM
description: You can configure the user access for Service Operations Workspace \(SOW\) pages using various roles.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Getting started, Service Operations Workspace for ITSM, IT Service Management]
---

# Roles in Service Operations Workspace for ITSM

You can configure the user access for Service Operations Workspace \(SOW\) pages using various roles.

<table id="table_qkn_j4g_1cc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Inherited roles

</th></tr></thead><tbody><tr><td>

itil

</td><td>

Provides access to all SOW pages.

</td><td>

sn\_sow.sow\_user

</td></tr><tr><td>

sn\_sow.sow\_user

</td><td>

Provides access to SOW. By default, the itil role contains the sn\_sow.sow\_user. In case a user has roles other than itil, ensure that sn\_sow.sow\_user role is assigned to the user to access SOW.

</td><td>

None

</td></tr><tr><td>

sn\_sow.sow\_home

</td><td>

Provides access to SOW home \(landing\) page.

</td><td>

sn\_sow.sow\_user

</td></tr><tr><td>

sn\_sow.sow\_list

</td><td>

Provides access to SOW list pages.

</td><td>

sn\_sow.sow\_user

</td></tr><tr><td>

admin

</td><td>

Provides access to all the pages in SOW including SOW Admin Center.A user with this role can perform configurations for all modules in SOW Admin Center.

</td><td>

None

</td></tr><tr><td>

sn\_sow\_itsm\_admin.sow\_admin\_user

</td><td>

Provides access to SOW Admin Center pages for SOW configuration. A user with this role can perform configurations related to Incident Management only.

</td><td>

None

</td></tr><tr><td>

sn\_sow\_admin.sow\_admin\_center\_user

</td><td>

Enables change managers to access the SOW Admin Center page. Change managers can use configurations for change features like modern change adoption, change models, DevOps change automation, and so on.

</td><td>

sn\_ace.ace\_user

</td></tr><tr><td>

awa\_agent

</td><td>

Provides access to inbox in SOW.

</td><td>

None

</td></tr><tr><td>

sn\_sow.it\_agent\_dashboard\_user

</td><td>

Provides access to IT Agent Dashboard.

</td><td>

None

</td></tr><tr><td class="sub-head" colspan="3">

Incident Management

</td></tr><tr><td>

sn\_incident\_read

</td><td>

Provides the read access to incident record pages.

</td><td>

sn\_sow.sow\_home and sn\_sow.sow\_listSo, users with the sn\_incident\_read role can access the SOW home \(landing\) and list pages.

</td></tr><tr><td>

sn\_incident\_write

</td><td>

Provides the write access to incident record pages.

</td><td>

sn\_sow.sow\_home and sn\_sow.sow\_listSo, users with the sn\_incident\_write role can access the SOW home \(landing\) and list pages.

</td></tr><tr><td>

incident\_manager

</td><td>

Manages incident properties, major incident trigger rules, create and edit communication plan definitions.

</td><td>

None

</td></tr><tr><td class="sub-head" colspan="3">

Major Incident Management

</td></tr><tr><td>

major\_incident\_manager

</td><td>

Promotes, manages, resolves and closes a major incident.

</td><td>

ia\_admin

</td></tr><tr><td class="sub-head" colspan="3">

Problem Management

</td></tr><tr><td>

problem\_task\_analyst

</td><td>

Works on a problem task and manages it through its life cycle.

</td><td>

None

</td></tr><tr><td>

problem\_coordinator

</td><td>

Works on a problem or problem task and manages it through its life cycle.

</td><td>

itil and problem\_task\_analyst

</td></tr><tr><td>

problem\_manager

</td><td>

Responsible for the overall Problem Management process and can configure Problem Management settings, as well as act as a problem coordinator.

</td><td>

problem\_coordinator

</td></tr><tr><td>

problem\_admin

</td><td>

A problem manager who can also delete problems and problem tasks.

</td><td>

problem\_manager

</td></tr><tr><td>

sn\_problem\_read

</td><td>

Provides the read access to problem record pages.

</td><td>

sn\_sow.sow\_home and sn\_sow.sow\_list allow users with the sn\_problem\_read role to access the SOW home \(landing\) and list pages.

</td></tr><tr><td>

sn\_problem\_write

</td><td>

Provides the write access to problem record pages.

</td><td>

sn\_sow.sow\_home and sn\_sow.sow\_list enable users with the sn\_problem\_write role to access the SOW home \(landing\) and list pages.

</td></tr><tr><td class="sub-head" colspan="3">

Change Management

</td></tr><tr><td>

sn\_change\_read

</td><td>

Provides the read access to change record pages.

</td><td>

sn\_sow.sow\_home and sn\_sow.sow\_listSo, users with the sn\_change\_read role can access the SOW home \(landing\) and list pages.

</td></tr><tr><td>

sn\_change\_write

</td><td>

Provides the write access to change record pages.

</td><td>

sn\_sow.sow\_home and sn\_sow.sow\_listSo, users with the sn\_change\_write role can access the SOW home \(landing\) and list pages.

</td></tr><tr><td>

change\_manager

</td><td>

Provides access to configurations related to Change Management in SOW Admin Center.

</td><td>

-   sn\_sttrm\_attribute\_read
-   sn\_sttrm\_condition\_read
-   sn\_chg\_soc.change\_soc\_admin
-   personalize\_decision\_table\_input
-   sn\_sow\_admin.sow\_admin\_center\_user
-   itil

</td></tr><tr><td>

sn\_devops.viewer

</td><td>

Provides access to view or add DevOps data to a change request.

</td><td>

None

</td></tr><tr><td class="sub-head" colspan="3">

Request Management

</td></tr><tr><td>

sn\_request\_read

</td><td>

Provides the read access to request record pages.

</td><td>

sn\_sow.sow\_home and sn\_sow.sow\_listSo, users with the sn\_request\_read role can access the SOW home \(landing\) and list pages.

</td></tr><tr><td>

sn\_request\_write

</td><td>

Provides the write access to request record pages.

</td><td>

sn\_sow.sow\_home and sn\_sow.sow\_listSo, users with the sn\_request\_read role can access the SOW home \(landing\) and list pages.

</td></tr><tr><td class="sub-head" colspan="3">

On-call Scheduling

</td></tr><tr><td>

oc\_read

</td><td>

Provides the read access to Schedules page.

</td><td>

Users with the oc\_read role can access the On-call Schedules, Experts On-call, Escalation Tracking, and other On-call features in Service Operations Workspace.

</td></tr><tr><td class="sub-head" colspan="3">

Password Reset

</td></tr><tr><td>

password\_reset\_service\_desk

</td><td>

Resets passwords on behalf of users, tracks password reset requests, and views logs.

</td><td>

None

</td></tr></tbody>
</table>