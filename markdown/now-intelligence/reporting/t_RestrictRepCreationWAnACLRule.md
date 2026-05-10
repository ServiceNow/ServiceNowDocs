---
title: Restrict report creation with an ACL rule
description: Create an access control list rule to restrict who can create a report on a table, data source, or database view.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Restrict report creation with an ACL rule

Create an access control list rule to restrict who can create a report on a table, data source, or database view.

## Before you begin

Role required: security\_admin.

**Note:** In addition to [report\_on ACLs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/acl-rule-types.md) for specific tables, a write ACL on the \[sys\_report\] table controls write access for all reports. If this ACL prevents you from saving the current report, the **Save** button in the Report Designer is disabled. For example, when you view a report that another user shared with you. If you have the correct security settings, click **Save** &gt; **Insert** to save an editable copy of the report.

## Procedure

1.  Navigate to **System Security** &gt; **Access Control \(ACL\)**.

2.  Add an access control record with the following information.

<table id="choicetable_ojc_l32_s4"><tbody><tr><td id="d175875e110">

**_Type_**

</td><td>

`record`

</td></tr><tr><td id="d175875e125">

**_Operation_**

</td><td>

``report_on``

</td></tr><tr><td id="d175875e143">

**_Name_ \(table\)**

</td><td>

&lt;select the table name&gt;

</td></tr></tbody>
</table>3.  Define the rules that determine whether a user can report on a table.

    If a user does not have `report_on` access for a table, the table does not appear in the **Table** field when the user creates a report. Data sources based on tables for which a user does not pass the `report_on` ACL do not appear in the **Data Source** list in the Report Designer. To restrict one or more users from seeing a data source in the **Report Source** list, create a new read ACL on the \[sys\_report\_source\] table that excludes those users.

    **Note:**

    -   Users can view and run reports on tables even if they cannot create reports due to report\_on ACL restrictions.
    -   System tables are not reportable by default. To allow reporting against system tables, administrators can configure the **glide.ui.permitted\_tables** property. To learn more, see [Reporting on system tables](../concept/c_ReportOnSystemTables.md).
    -   The ACL `report_on` operation grants the right to report on the target table.
    -   [Database views](../../performance-analytics/concept/performance-analytics-glossary.md#) have their own ACLs. If a user has `report_on` rights to all the tables in a database view, they still require report\_on rights on the database view to create reports on it. See [Database views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DatabaseViews.md).

**Parent Topic:**[Administering reports](../concept/c_AdminsteringReports.md)

**Related topics**  


[Create an ACL rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/t_CreateAnACLRule.md)

[Access control rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-control-rules.md)

