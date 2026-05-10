---
title: Components installed with Operational Technology Change Management
description: Several types of components may be installed with activation of the Operational Technology Change Management \(sn\_ot\_chg\_mgmt\) application, including the user roles.
locale: en-US
release: australia
product: Operational Technology Change Management
classification: operational-technology-change-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Operational Technology Change Management, Operational Technology]
---

# Components installed with Operational Technology Change Management

Several types of components may be installed with activation of the Operational Technology Change Management \(sn\_ot\_chg\_mgmt\) application, including the user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Change Manager \[sn\_ot\_change\_manager\]

</td><td>

Can manage OT change model records.

</td><td>

-   sn\_ot\_change\_write
-   sn\_sttrm\_condition\_read

</td></tr><tr><td>

Change Admin \[sn\_ot\_change\_admin\]

</td><td>

Can create, view, delete, and edit OT change records. Can configure categories and system properties.

</td><td>

-   cmdb\_ot\_isa\_viewer\_all
-   sn\_ot\_change\_write

</td></tr><tr><td>

Change Write user \[sn\_ot\_change\_write\]

</td><td>

Can create, view, and edit OT change records.Can also be assigned IT change tasks, and can edit and close the IT change task they're assigned to.

For more information, see [Managing change requests across sites](../concept/visibility-of-changes-across-sites.md).

</td><td>

-   cmdb\_ot\_viewer
-   cmdb\_ot\_isa\_viewer
-   sn\_ot\_change\_read

</td></tr><tr><td>

Change Read user \[sn\_ot\_change\_read\]

</td><td>

Can only view OT change records.

</td><td>

-   cmdb\_ot\_viewer
-   cmdb\_ot\_isa\_viewer

</td></tr></tbody>
</table>**Parent Topic:**[Operational Technology Change Management reference](oper-tech-change-management-reference.md)

