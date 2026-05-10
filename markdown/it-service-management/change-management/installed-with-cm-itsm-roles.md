---
title: Components installed with ITSM Roles - Change Management
description: Several user roles are installed with the activation of the ITSM Roles — Change Management plugin \(com.snc.itsm.roles.change\_management\). Security ACLs to support the security model for Change Management and related functionality are also installed.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Request ITSM Roles- Change Management, Change Management plugins, Configure, Change Management, IT Service Management]
---

# Components installed with ITSM Roles - Change Management

Several user roles are installed with the activation of the ITSM Roles — Change Management plugin \(com.snc.itsm.roles.change\_management\). Security ACLs to support the security model for Change Management and related functionality are also installed.

When you install the ITSM Roles — Change Management plugin \(com.snc.itsm.roles.change\_management\), the plugin updates the Security Access Control Lists \(ACLs\), integrating revised scripts, and other files to overhaul the security model for these applications.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Change admin\[sn\_change\_admin\]

</td><td>

Provides configuration and authorization access for system properties in the Change Management application. Provides a granular, application-specific write access replacing the global admin role.

</td><td>

-   sn\_change\_write
-   sn\_change\_cab.cab\_manager
-   change\_manager

</td></tr><tr><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Change read\[sn\_change\_read\]

</td><td>

Read access to the Change Management application and related records.**Note:** A user with the sn\_change\_read role can view all change requests as well as the CAB workbench.

</td><td>

-   sn\_cmdb\_user
-   dependency\_views
-   view\_changer
-   cmdb\_read
-   app\_service\_user
-   cmdb\_query\_builder\_read

</td></tr><tr><td>

Change write\[sn\_change\_write\]

</td><td>

Write access to the Change Management application and related records.

</td><td>

-   sn\_change\_read
-   template\_editor
-   cmdb\_query\_builder

</td></tr><tr><td>

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

Problem read\[sn\_problem\_read\]

</td><td>

Read access to the Problem Management application and related records.

</td><td>

NA

</td></tr><tr><td>

Problem write\[sn\_problem\_write\]

</td><td>

Write access to the Problem Management application and related records.

</td><td>

-   sn\_problem\_read
-   template\_editor

</td></tr><tr><td>

sn\_request\_read

</td><td>

Read access to the Request \(sc\_request\) or Requested Item \(sc\_req\_item\) only for a user who is also an approver of the request or requested item.**Note:** As there are future updates expected for the sn\_request\_read role, do not assign it to users without the business\_stakeholder role.

</td><td>

NA

</td></tr><tr><td>

sn\_request\_write

</td><td>

Write access to the Request \(sc\_request\) or Requested Item \(sc\_req\_item\).

</td><td>

-   task\_editor
-   dependency\_views
-   agent\_workspace\_user
-   view\_changer
-   cmdb\_read
-   cmdb\_query\_builder\_read
-   sn\_request\_read

</td></tr><tr><td>

sn\_request\_comment\_write

</td><td>

Write access to the comments for the Requested Item \(sc\_req\_item\).**Note:** The sn\_request\_comment\_write role alone does not give access to comments write, you will need write access for the table.

</td><td>

NA

</td></tr><tr><td>

\[sn\_service\_desk\_agent\]

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

</td></tr></tbody>
</table>**Parent Topic:**[Request ITSM Roles- Change Management](../task/request-itsm-roles-cm.md)

