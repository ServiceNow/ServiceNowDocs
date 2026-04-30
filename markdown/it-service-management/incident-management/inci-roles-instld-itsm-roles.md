---
title: Components installed with ITSM Roles — Incident Management
description: Several user roles are installed with activation of the ITSM Roles — Incident Management plugin \(com.snc.itsm.roles.incident\_management\).
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Request ITSM Roles — Incident Management, Incident Management plugins, Reference, Incident Management, IT Service Management]
---

# Components installed with ITSM Roles — Incident Management

Several user roles are installed with activation of the ITSM Roles — Incident Management plugin \(com.snc.itsm.roles.incident\_management\).

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

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

</td></tr></tbody>
</table>**Parent Topic:**[Request ITSM Roles — Incident Management](../task/req-itsm-roles-inci-mgmt.md)

