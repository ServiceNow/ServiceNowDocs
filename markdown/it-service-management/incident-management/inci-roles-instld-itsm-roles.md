---
title: Components installed with ITSM Roles — Incident Management
description: Several user roles are installed with activation of the ITSM Roles — Incident Management plugin \(com.snc.itsm.roles.incident\_management\).
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Request ITSM Roles — Incident Management, Incident Management plugins, Reference section for Incident Management, Incident Management, IT Service Management]
---

# Components installed with ITSM Roles — Incident Management

Several user roles are installed with activation of the ITSM Roles — Incident Management plugin \(com.snc.itsm.roles.incident\_management\).

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Incident read\[sn\_incident\_read\]

</td><td>

Read access to the Incident Management application and related records.**Note:** An ESS user \(user with no role\) can view only those incidents that they create or someone else creates on their behalf. A user with the sn\_incident\_read role can view all incidents as well as the major incident workbench.

</td><td>

-   dependency\_views
-   agent\_workspace\_user
-   view\_changer
-   cmdb\_read
-   cmdb\_query\_builder\_read

</td></tr><tr><td>

Incident write\[sn\_incident\_write\]

</td><td>

Write access to the Incident Management application and related records.

</td><td>

-   sn\_incident\_read
-   template\_editor

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

 With the installation of the ITSM Gen AI \(com.sn.itsm.gen.ai\) plugin, the following roles are also available:

-   knowledge\_user
-   now\_assist\_panel\_user

</td></tr><tr><td>

Incident Manager \[incident\_manager\]

\(Existing role with added responsibilities\)

</td><td>

-   Manages incident properties and major incident trigger rules.
-   Can create and edit Communication Plan Definitions.

</td><td>

itil

</td></tr><tr><td>

Incident Admin\[sn\_incident\_admin\]

</td><td>

Configures all Incident Management features including incident management properties.

</td><td>

-   incident\_manager
-   sn\_sow\_inc.sn\_incident\_sow\_admin
-   sn\_bm\_client\_benchmark\_data\_viewer

</td></tr></tbody>
</table>**Parent Topic:**[Request ITSM Roles — Incident Management](../task/req-itsm-roles-inci-mgmt.md)

