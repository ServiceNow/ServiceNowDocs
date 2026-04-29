---
title: Roles in Service Operations Workspace for ITSM
description: You can configure the user access for Service Operations Workspace \(SOW\) pages using various roles.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Getting started with Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Roles in Service Operations Workspace for ITSM

You can configure the user access for Service Operations Workspace \(SOW\) pages using various roles.

**Note:** You must install and activate the ITSM Roles plugin \(com.snc.itsm.roles\) to correctly utilize all the SOW user roles including the granular admin roles.

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

sn\_sow\_itsm\_admin\_sow\_admin\_user

</td><td>

Provides access to the ITSM section of the Admin Center for SOW configuration.

</td><td>

sn\_sow\_admin\_sow\_admin\_center\_user

</td></tr><tr><td>

sn\_sow\_admin\_sow\_admin\_center\_user

</td><td>

Provides access to the Admin Center pages.

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

</td></tr><tr><td>

sn\_sow\_admin.sn\_sow\_admin

</td><td>

Provides access to the SOW Admin Center page for configurations. Admins can use the role to configure SOW features and maintain organizational policies.**Note:** To configure SOW features, you also require additional roles along with the SOW admin role to access specific sections and pages in SOW admin center. For more information, see [Additional roles for SOW admin](additional-roles-sow-admin.md).

</td><td>

-   sn\_sow\_inc.sn\_incident\_sow\_admin
-   sn\_sow\_problem.sn\_problem\_sow\_admin
-   sn\_sow\_chg.sn\_change\_sow\_admin
-   sn\_sow\_mim.sn\_mim\_sow\_admin
-   sn\_sow\_interaction.sn\_interaction\_sow\_admin
-   sn\_sow\_collab.sn\_collab\_sow\_admin
-   sn\_sow\_srm.srm\_admin
-   sn\_sow\_on\_call.sn\_on\_call\_sow\_admin

</td></tr><tr><td>

Service desk agent\[sn\_service\_desk\_agent\]

</td><td>

Enables gathering, and verifying information, as well as delivering quick resolutions for tier 1 service desk agents. This user role is available when the ITSM Roles plugin \(com.snc.itsm.roles\) is installed.

</td><td>

-   sn\_incident\_write
-   sn\_problem\_write
-   sn\_change\_write
-   sn\_request\_write
-   tracked\_file\_reader

 With the installation of the ITSM Gen AI \(com.sn.itsm.gen.ai\) plugin, the following roles are also assigned:

-   knowledge\_user
-   now\_assist\_panel\_user

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

incident\_manager\(Existing role with added responsibilities\)

</td><td>

-   Manages incident properties and major incident trigger rules.
-   Can create and edit Communication Plan Definitions.

</td><td>

itil

</td></tr><tr><td>

sn\_sow\_inc.sn\_incident\_sow\_admin

</td><td>

Provides access to SOW Admin Center for configurations related to Incident Management features.

</td><td>

-   sn\_incident\_write
-   sn\_sow\_itsm\_admin\_sow\_admin\_user

</td></tr><tr><td>

sn\_incident\_admin

</td><td>

Configures all Incident Management features including incident management properties.

</td><td>

-   incident\_manager
-   sn\_sow\_inc.sn\_incident\_sow\_admin
-   sn\_bm\_client\_benchmark\_data\_viewer

</td></tr><tr><td class="sub-head" colspan="3">

Major Incident Management

</td></tr><tr><td>

major\_incident\_manager

</td><td>

A major incident manager can:-   Initiate the major incident process by assessing and approving major incident candidates or creating a major incident.
-   Reject a major incident candidate.
-   Demote a major incident after it is accepted so that the incident can be handled as a regular incident.
-   Maintain the ownership and accountability for the life cycle of the incident.
-   Identifies the users and groups to be involved in the resolution activities.
-   Creates adhoc communication plans and tasks.
-   Edits a communication plan that is attached to a major incident.
-   Close a major incident.

</td><td>

This role inherits the ia\_admin role.

</td></tr><tr><td>

communication\_manager

</td><td>

-   Manages communications for major incidents and is responsible for communicating with all stakeholders.
-   Creates adhoc communication plans and tasks.
-   Edits a communication plan that is attached to a major incident.

</td><td>

This role inherits the ia\_admin role.

</td></tr><tr><td>

sn\_sow\_mim.sn\_mim\_sow\_admin

</td><td>

Provides access to the SOW Admin Center pages for configurations related to MIM features.However, to perform configuration of the following MIM features from Admin Center, along with sn\_mim\_sow\_admin role, you must also have additional role that provides access to the specific table where you want to configure:

-   MIM Trigger rules - incident\_manager or major\_incident\_manager
-   Configure email - mail\_client\_template\_read
-   Configure SMS - notify\_admin or notify\_view
-   Communication plans - sn\_comm\_management.comm\_plan\_viewer

In case, you do not have the relevant additional role, you still can access the Major Incident Management \(MIM\) configuration section of the Admin Center but the **Configure** option is not enabled and you cannot configure the specific MIM feature.

</td><td>

sow\_admin\_user

</td></tr><tr><td>

sn\_mim\_admin

</td><td>

Configure all Major Incident Management features including major incident properties and trigger rules.

</td><td>

-   mim\_manager
-   sn\_iam\_admin
-   sn\_sow\_mim.sn\_mim\_sow\_admin

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

</td></tr><tr><td>

sn\_sow\_problem.sn\_problem\_sow\_admin

</td><td>

Provides access to the SOW Admin Center pages for Problem Management configurations.

</td><td>

sn\_problem\_write

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

</td></tr><tr><td>

rota\_admin

</td><td>

Provides access to Teams, Schedules, and Home pages in SOW. By default, for a user with this role, the Teams page is displayed.**Note:** The sn\_on\_call\_admin role, which configures all on-call schedule features including its properties and trigger rules, contains the rota\_admin role.

</td><td>

-   sn\_sow.sow\_home
-   oc\_read

</td></tr><tr><td>

sn\_sow\_on\_call.sn\_on\_call\_sow\_admin

</td><td>

Provides access to the SOW Admin Center pages for on-call configurations.**Note:** The sn\_on\_call\_admin role, which configures all on-call schedule features including its properties and trigger rules, contains the sn\_sow\_on\_call.sn\_on\_call\_sow\_admin role.

</td><td>

-   sn\_sow\_itsm\_admin.sow\_admin\_user
-   sn\_help\_setup\_player

</td></tr></tbody>
</table>