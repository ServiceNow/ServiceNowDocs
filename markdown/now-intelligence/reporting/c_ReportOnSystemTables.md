---
title: Reporting on system tables
description: System tables are excluded from reporting by default. However, you can exempt system tables from the prohibition. Some system tables are exempt from the restriction by default. Be very careful when creating reports on these system tables.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Reporting on system tables

System tables are excluded from reporting by default. However, you can exempt system tables from the prohibition. Some system tables are exempt from the restriction by default. Be very careful when creating reports on these system tables.

Prohibited system tables include, but are not limited to:

-   Log \[`syslog`\]
-   Transaction Log \[`syslog_transaction`\]
-   Attachment \[`sys_attachment`\]
-   Email \[`sys_email`\]

If you must report on a system table, you can add it to the **glide.ui.permitted\_tables** system property. Several system tables are listed in this property by default. Only admin users can create reports on the tables permitted in this property.

Use extreme caution when creating a report or a data visualization on any system table. Consider the Audit \[sys\_audit\] table, which is allowed in reports and data visualizations by default. Typically, this table is the largest table in any instance. It is not unusual for the Audit table, in even a mid-sized instance, to be several gigabytes. In a large installation, this table can be 50GB or more.

When you access a table like Audit programmatically, you know what your query pattern is going to look like, so you can add appropriate data indexes to match your queries. This means that when you bring up, for example, the history of an incident, the database can use an index to efficiently pull back the few dozen rows it needs for that query.

With reports and data visualizations, however, you cannot predict what your query pattern is going to look like. Maybe you want to group by `fieldname` or sort by `oldvalue`. Thus, your queries might not be indexed queries. You can end up asking the database to table scan a multiple gigabyte file, which is bad for these reasons:

-   It is slow, so your report or data visualization will take an unacceptably long time to run.
-   While the database is scanning your table, your instance will slow down or even become unavailable because other queries cannot get the resources they need.

**Parent Topic:**[Administering reports](c_AdminsteringReports.md)

