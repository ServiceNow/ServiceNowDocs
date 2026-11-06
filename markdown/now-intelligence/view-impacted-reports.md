---
title: Guide to report view ACL assessments
description: The Report view ACL assessments table shows the impacted data visualizations and Core UI reports identified by the ACL Assessment for Data Visualizations. Use this list to remediate affected visualizations and users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/view-impacted-reports.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Manage report view ACL assessments, ACL Assessment for Data Visualizations, Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Guide to report view ACL assessments

The Report view ACL assessments table shows the impacted data visualizations and Core UI reports identified by the ACL Assessment for Data Visualizations. Use this list to remediate affected visualizations and users.

The Report view ACL assessments table \(report\_view\_acl\_assessment\_list\) is located at **All** &gt; **Platform Analytics Administration** &gt; **ACL Assessment for Data Visualizations** &gt; **Affected Data Visualizations** or at report\_view\_acl\_assessment\_list.do. The admin role with elevation to security\_admin is required to view it.

To view an individual report\_view ACL assessment record, hover over the beginning of the row and select the information icon. A preview of the record opens. Then select **Open record**.

**Note:** The term "visualization" on its own can refer to Core UI reports or Platform Analytics data visualizations.

<table id="simpletable_pkr_42l_4pba"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Visualization

</td><td>

Name of the data visualization or Core UI report if it is in the Data visualizations library. Either Visualization or Dashboard has a value.

</td></tr><tr><td>

Dashboard

</td><td>

SysID of the dashboard that contains the data visualization, if the data visualization exists only on that dashboard

</td></tr><tr><td>

Dashboard tab

</td><td>

SysID of the tab of the dashboard that contains the data visualization, if the data visualization exists only on that dashboard

</td></tr><tr><td>

Table

</td><td>

The data source table of the visualization. If the visualization has a database view with an ACL as its source, the name of the database view appears after the name of the table.

</td></tr><tr><td>

DBView Referenced ACL Table

</td><td>

When this column is populated, the visualization has a database view as its source. Furthermore, the visualization is affected because of an ACL on one of the tables that the database view is based on

</td></tr><tr><td>

Dot Walk Fields

</td><td>

When this column is populated, the visualization is affected because of an ACL on an extended table. For more information, see [Dot-walking from reference fields in a data visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/ext-table-fields-dot-walk-vis-des.md) or [Report on extended tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/reporting/t_AccessFieldExtendedTable.md).

</td></tr><tr><td>

Total executions

</td><td>

The number of times a user has viewed the visualization. This column is empty if the property **run\_scan\_based\_on\_report\_execution\_only** is false.

</td></tr><tr><td>

Last execution

</td><td>

The timestamp of the most recent time execution of the visualization. This column is populated if the property **run\_scan\_based\_on\_report\_execution\_only** is true.

</td></tr><tr><td>

is global

</td><td>

True / False. If true, the report owner has shared it with all users. If false, the report owner has shared it with specific users, groups, or roles. Applies only to Core UI reports.

</td></tr><tr><td>

Shared to roles

</td><td>

Roles the visualization owner has shared it with \(regardless of ACL\).

</td></tr><tr><td>

Shared to users

</td><td>

Users the visualization owner has shared it with \(regardless of ACL\).

</td></tr><tr><td>

Shared to groups

</td><td>

Groups the visualization owner has shared it with \(regardless of ACL\).

</td></tr><tr><td>

Is blocked by read ACL

</td><td>

This column shows true if a read ACL blocks a user through .

</td></tr><tr><td>

Read ACL table

</td><td>

Shows the name of the table checked if the user is blocked by a read ACL.

</td></tr><tr><td>

Is blocked without RVA or Read ACL

</td><td>

This column shows true if a visualization is blocked because the table the visualization is based on has neither a report\_view ACL nor a read ACL.

</td></tr><tr><td>

Blocked by table ACLs

</td><td>

If a table report\_view ACL \(or field ACL that applies to all fields in a table\) blocks a user, this column shows the name of the ACL.

</td></tr><tr><td>

Blocked by table ACLs roles

</td><td>

The roles defined in the table report\_view ACL whose members can view visualizations based on the ACL. A user needs at least one of these roles to see the visualization.

</td></tr><tr><td>

Table ACLs link

</td><td>

Select the link to view a list of the table ACLs that apply to the impacted visualization. The **Role** field in the list shows the required roles. A user must have one of the roles to view visualizations based on the table.

</td></tr><tr><td>

Blocked by column ACLs

</td><td>

If a specific field ACL blocks a user, this column shows the name of the ACL.

</td></tr><tr><td>

Blocked by column ACLs roles

</td><td>

The roles defined in the column ACL whose members can view visualizations based on the column. A user needs at least one of these roles to see the visualization.

</td></tr><tr><td>

Column ACLs link

</td><td>

Select the link to view the column ACLs that apply to the impacted visualization. The **Role** field in the list shows the required roles. A user must have one of the roles to view visualizations based on the column.

</td></tr></tbody>
</table>**Parent Topic:**[Manage report view ACL assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/view-report-acl-remediation.md)

