---
title: View the list of affected reports
description: You can view a list of all impacted reports identified by the ACL assessment for reports. Use this list to remediate affected reports and users.
locale: en-US
release: yokohama
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [ACL Assessment for Reports, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# View the list of affected reports

You can view a list of all impacted reports identified by the ACL assessment for reports. Use this list to remediate affected reports and users.

## Before you begin

Roles required: admin and security\_admin.

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **ACL Assessment for Reports** &gt; **Affected Reports List**.

    The list report shows the affected reports.

<table id="simpletable_pkr_42l_4pba"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Report

</td><td>

The report name with a hyperlink to its form.

</td></tr><tr><td>

Table

</td><td>

The source table of the report.

</td></tr><tr><td>

DBView Referenced ACL Table

</td><td>

When this column is populated, the report is affected because of an ACL on one of the tables that the [database view](../../performance-analytics/concept/performance-analytics-glossary.md#) is based on.Sometimes an affected report is based on a database view with an ACL. In this case, the name of the database view appears below the name of the table in the Table column.

</td></tr><tr><td>

Dot Walk Fields

</td><td>

When this column is populated, the report is affected because of an ACL on an extended table. For more information, see [Report on extended tables](t_AccessFieldExtendedTable.md#).

</td></tr><tr><td>

Total executions

</td><td>

The number of times a user has viewed the report. This column is empty if the property **run\_scan\_based\_on\_report\_execution\_only** is false.

</td></tr><tr><td>

Last execution

</td><td>

The timestamp of the most recent time execution of the report. This column is populated if the property **run\_scan\_based\_on\_report\_execution\_only** is true.

</td></tr><tr><td>

is global

</td><td>

True / False. If true, the report owner has shared it with all users. If false, the report owner has shared it with specific users, groups, or roles.

</td></tr><tr><td>

Shared to roles

</td><td>

Roles the report owner has shared it with \(regardless of access control list\). This field is empty if the report is global.

</td></tr><tr><td>

Shared to users

</td><td>

Users the report owner has shared it with \(regardless of access control list\). This field is empty if the report is global.

</td></tr><tr><td>

Shared to groups

</td><td>

Groups the report owner has shared it with \(regardless of access control list\). This field is empty if the report is global.

</td></tr><tr><td>

Is blocked by read ACL

</td><td>

This column shows true if a read ACL blocks a user.

</td></tr><tr><td>

Read ACL table

</td><td>

Shows the name of the table checked if the user is blocked by a read ACL.

</td></tr><tr><td>

Is blocked without RVA or Read ACL

</td><td>

This column shows true if a report is blocked because the table the report is based on has neither a report\_view ACL nor a read ACL.

</td></tr><tr><td>

Blocked by table ACLs

</td><td>

If a table ACL \(or column ACL that applies to all columns in a table\) blocks a user, this column shows the name of the ACL.

</td></tr><tr><td>

Blocked by table ACLs roles

</td><td>

The roles defined in the table ACL whose members can view reports based on the ACL. A user needs at least one of these roles to see the report.

</td></tr><tr><td>

Table ACLs link

</td><td>

Click the link to view a list of the table ACLs that apply to the impacted report. The **Role** field in the list shows the required roles. A user must have one of the roles to view reports based on the table.

</td></tr><tr><td>

Blocked by column ACLs

</td><td>

If a specific column ACL blocks a user, this column shows the name of the ACL.

</td></tr><tr><td>

Blocked by column ACLs roles

</td><td>

The roles defined in the column ACL whose members can view reports based on the column. A user needs at least one of these roles to see the report.

</td></tr><tr><td>

Column ACLs link

</td><td>

Click the link to view the column ACLs that apply to the impacted report. The **Role** field in the list shows the required roles. A user must have one of the roles to view reports based on the column.

</td></tr></tbody>
</table>2.  Address the affected reports and users as described in [Manage Report ACL assessments](view-report-acl-remediation.md#).


**Parent Topic:**[ACL Assessment for Reports](../concept/report-view-acl-dashboard.md)

