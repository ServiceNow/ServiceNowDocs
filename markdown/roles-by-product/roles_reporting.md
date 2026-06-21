---
title: Reporting roles
description: These roles are available for the application
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/roles-by-product/roles\_reporting.html
release: australia
topic_type: reference
last_updated: "2024-03-11"
reading_time_minutes: 1
breadcrumb: [Roles for all products]
---

# Reporting roles

These roles are available for the application

<table><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th><th>

Groups with this role

</th><th>

Special considerations

</th></tr></thead><tbody><tr><td>

Global report user \[report\_global\]

</td><td>

Can share a report that is shared with everyone. This role can share with everyone. Cannot share a report that is shared with the user or a group.

</td><td>

None

</td><td>

None.

</td><td>

None.

</td></tr><tr><td>

Group report user \[report\_group\]

</td><td>

Can manage and share reports that are shared with the groups they are members of \(listed in Group\).

</td><td>

None

</td><td>

None.

</td><td>

None.

</td></tr><tr><td>

Report administrator \[report\_admin\]

</td><td>

Manage, share, publish, and schedule all reports. Access **Reports** &gt; **Administration** and manage all report-related objects.

</td><td>

-   report\_scheduler
-   analytics\_filter\_admin
-   report\_global
-   report\_group
-   gauge\_maker
-   viz\_admin

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

Report description administrator \[report\_description\_admin\]

</td><td>

Read and update table and field descriptions for reports. Included in the plugin Table and field description configuration for report \[com.glideapp.report.description\_config\].

</td><td>

None.

</td><td>

None.

</td><td>

For more information, see .

</td></tr><tr><td>

Report scheduler \[report\_scheduler\]

</td><td>

Schedule emailing of all reports that they can see, including reports they cannot manage. Users with this role must also have another role that grants permission to create, edit, and share reports.

</td><td>

None

</td><td>

None.

</td><td>

None.

</td></tr><tr><td>

Report user \[report\_user\]

</td><td>

Create and view reports that have been shared with them. Cannot share, edit, or delete reports that have been shared with them. Users with the itil role also have these limitations.

</td><td>

None

</td><td>

None.

</td><td>

None.

</td></tr></tbody>
</table>**Parent Topic:**[Roles for all products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/roles-by-product/roles-for-all-products.md)

