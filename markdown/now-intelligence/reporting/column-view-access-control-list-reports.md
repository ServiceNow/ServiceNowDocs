---
title: Column view access control for list reports
description: For list reports, the glide.report.add\_to\_list\_supported system property enables the add\_to\_list access control list. This access control list \(ACL\) prevents users from reporting on list report columns with sensitive data.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Column view access control for list reports

For list reports, the **glide.report.add\_to\_list\_supported** system property enables the add\_to\_list access control list. This access control list \(ACL\) prevents users from reporting on list report columns with sensitive data.

A manager can prevent users from reporting on the **Assigned to** column when creating a report, for example. If a table field is restricted for the user, it doesn't appear in the **Available** column. Users are therefore not able to select it in the reports they create.

**Note:** When the property is enabled: A user who doesn't pass the add\_to\_list access control list for a column sees the restricted columns that are already included in the report in the **Selected** column. This user also sees those columns' data in the report. If the user removes the column from the **Selected** column, it’s no longer listed in the **Available** column. The user isn't able to select it again to include in a report.

The add\_to\_list ACL only applies to the top-level table that the report is based on.

This property is inactive by default. To enable it, navigate to **sys\_properties.list** \(System Property table\) and set **glide.report.add\_to\_list\_supported** to **true**. Admin role required.

After you enable the property, existing reports aren't affected. Columns are only invisible on newly created list reports with fields that you specify as restricted.

**Parent Topic:**[Administering reports](c_AdminsteringReports.md)

**Related topics**  


[ACL rule types](https://www.servicenow.com/docs/access?context=acl-rule-types&version=australia&pubname=australia-platform-security&ft:locale=en-US)

