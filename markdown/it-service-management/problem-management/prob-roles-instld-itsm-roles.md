---
title: Components installed with ITSM Roles — Problem Management
description: Several user roles are installed with activation of the ITSM Roles — Problem Management plugin \(com.snc.itsm.roles.problem\_management\).
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Request ITSM Roles — Problem Management, Problem Management plugins, Configuring Problem Management, Problem Management, IT Service Management]
---

# Components installed with ITSM Roles — Problem Management

Several user roles are installed with activation of the ITSM Roles — Problem Management plugin \(com.snc.itsm.roles.problem\_management\).

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

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
</table>**Parent Topic:**[Request ITSM Roles — Problem Management](../task/req-itsm-roles-prob-mgmt.md)

