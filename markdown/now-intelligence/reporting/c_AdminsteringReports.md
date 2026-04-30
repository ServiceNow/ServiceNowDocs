---
title: Administering reports
description: Learn about the tasks report administrators typically perform, the objects that they work with, and the roles and rules that apply.
locale: en-US
release: yokohama
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Administering reports

Learn about the tasks report administrators typically perform, the objects that they work with, and the roles and rules that apply.

To administer reports, reporting roles, and report sources, navigate to **Reports** &gt; **Administration** and select the area to administer.

Provides management practices for reports to ensure that they deliver the intended value without impacting system performance.

## Reporting roles

**Note:**

-   Users must have the report\_user role to see the **Reports** module on the application navigator \(left navigation pane\).
-   Users with any reporting role or the itil role can access the following report options for all reports that are visible to them: **Insert**, **Insert and Stay**, **Add to Dashboard**, and **Export to PDF**.
-   In the table below, the term manage indicates access to the following report options: **Update** \(edit\), **Delete**, and **Export settings**.

|Role title\[name\]|Description|
|------------------|-----------|
|No role|Can view reports that are shared with them.|
|ACL-based|The report\_view access controls on tables and fields limits the ability to read, edit and create reports. Administrators can create other ACL rules. You need a role that gives you access to the data that is the subject of the report. For more information, see [Restrict report creation with an ACL rule](../task/t_RestrictRepCreationWAnACLRule.md) and [Report\_view access control](report-view-access-control.md).|
|report user \[report\_user\], itil|Can create reports and view reports that have been shared with them. Cannot share, edit, or delete reports that have been shared with them.|
|report scheduler \[report\_scheduler\]|Can **Schedule** emailing of all reports that they can see, including reports they cannot manage. Users with this role must also have another role that grants permission to create, edit, and share reports.|
|group report user \[report\_group\]|Can manage and share reports that are shared with the groups they are members of \(listed in **Group**\).|
|global report user \[report\_global\]|Can manage reports that are shared with everyone \(listed in **Global**\).|
|report administrator \[report\_admin\]|Can manage, share, publish, and schedule all reports. Can access **Reports** &gt; **Administration** and manage all report-related objects. The report\_admin role inherits all other report roles.|
|report description administrator \[report\_description\_admin\]|Can read and update table and field descriptions for reports.|

-   **[Restrict report creation with an ACL rule](../task/t_RestrictRepCreationWAnACLRule.md)**  
Create an access control list rule to restrict who can create a report on a table, data source, or database view.
-   **[Report\_view access control](report-view-access-control.md)**  
The report\_view operation is a record type access control list \(ACL\) that restricts access to reports. Only users who have one of the required roles can view reports that contain the restricted resource.
-   **[ACL Assessment for Reports](report-view-acl-dashboard.md)**  
Use the ServiceNow® ACL Assessment for Reports to identify reports that are blocked by report\_view ACLs \(access control lists\).
-   **[Column view access control for list reports](column-view-access-control-list-reports.md)**  
For list reports, the **glide.report.add\_to\_list\_supported** system property enables the add\_to\_list access control list. This access control list \(ACL\) prevents users from reporting on list report columns with sensitive data.
-   **[Report permission issues](../reference/report-permission-issues.md)**  
There are several reasons why a report is showing less information than expected or possibly no data at all. These include insufficient permissions on the report and the report not being shared.
-   **[Report statistics](report-statistics.md#)**  
The **Report Stats** list enables you to view how often each of your Core UI reports is run and how long it takes for the reports to run.
-   **[Report sources](c_ReportSources.md#)**  
Report sources are predefined data sets for creating reports.
-   **[Report ranges](c_ReportRanges.md#)**  
Use a report range to define intervals that break up continuous timespan data in table fields. It is necessary to break this data into discreet chunks for presentation.
-   **[Using imported report data](imported-report-data.md)**  
Imported Excel spreadsheets enable you to generate reports based on data maintained outside of your instance and to distribute those reports.
-   **[Reporting on system tables](c_ReportOnSystemTables.md)**  
System tables are excluded from reporting by default. However, you can exempt system tables from the prohibition. Some system tables are exempt from the restriction by default. Be very careful when creating reports on these system tables.
-   **[Map report administration](c_AdministeringMapReports.md)**  
Learn how about the different objects that are used in map reports, and how to create and modify them.
-   **[Administer table and field descriptions](../task/admin-table-field-descriptions.md#)**  
Users with the report\_description\_admin role can add and edit table and field descriptions that users see when they create reports.
-   **[Create coloring rules for multilevel pivot reports](../task/t_DefineAPivotTableColoringRule.md)**  
Configure rules for how numerical values are displayed in a multilevel pivot table report. Coloring rules make it easy to highlight the more important values. The color rule is applied to the content of cells in pivot reports.
-   **[Create coloring rules for single score reports](../task/single-score-report-coloring-rules.md)**  
Configure rules for how numerical values are displayed in single score reports, to highlight why a value is important.
-   **[Domain separation and Reporting](domain-separation-in-reporting.md)**  
Domain separation is supported in reporting and relates to report creation and administration. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Quick start tests for Reporting](../../../administer/atf-quick-start-tests/reference/quick-start-tests-reporting.md#)**  
Validate that Reporting still works after you make any configuration change such as applying an upgrade. Copy and customize these quick start tests to pass when using your instance-specific data.
-   **[Customize calendar reports](c_CustomizeCalendarReports.md)**  
You can specify the fields that are displayed in calendar tasks.
-   **[Translate a report’s grouping labels](translate-row-column-field-label.md)**  
When executing reports that group results by a Translated Text field, to ensure that individual field labels and values display as translated, use the translated\_text type.
-   **[Report Administration module](../reference/r_AdministerReports.md)**  
Learn how to administer reports on the ServiceNow platform using the **Reports** &gt; **Administration** module.

**Parent Topic:**[Reporting](../reference/reporting-landing-page.md)

**Related topics**  


[Performance Analytics roles](../../performance-analytics/reference/r_PARoles.md)

[Dashboard permissions](../../dashboards/concept/c_DashboardRoles.md)

