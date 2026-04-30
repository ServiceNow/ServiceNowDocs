---
title: Components installed with ITSM Roles — Request Management
description: Several user roles are installed with the activation of the ITSM Roles - Request Management plugin \(com.snc.itsm.roles.request\_management\).
locale: en-US
release: zurich
product: Request Management
classification: request-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Request ITSM Roles - Request Management, Reference, Request Management, IT Service Management]
---

# Components installed with ITSM Roles — Request Management

Several user roles are installed with the activation of the ITSM Roles - Request Management plugin \(com.snc.itsm.roles.request\_management\).

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_service\_desk\_agent

</td><td>

Write access to the Request \(sc\_request\) or Requested Item \(sc\_req\_item\).

</td><td>

sn\_request\_write

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

</td></tr></tbody>
</table>**Parent Topic:**[Request ITSM Roles - Request Management](request-itsm-roles-rm.md)

