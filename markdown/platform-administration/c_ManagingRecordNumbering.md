---
title: Record numbering
description: In the base system, several tables are numbered, including Incident, Problem, Change Request, and Knowledge. You can also use these numbers anywhere that script is present, for example to generate watermarks for emails. Records in tables can be numbered automatically.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customize, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Record numbering

In the base system, several tables are numbered, including Incident, Problem, Change Request, and Knowledge. You can also use these numbers anywhere that script is present, for example to generate watermarks for emails. Records in tables can be numbered automatically.

Administrators can manage record numbering by navigating to **System Definition** &gt; **Number Maintenance**. The current number format for a table, including the prefix \(such as **INC** for incidents or **CHG** for changes\), is stored in a record on the Number \[sys\_number\] table.

![](../image/Number1.png "Number table")

You can renumber auto-incremented tables that extend the task table or manage numbering with a database field named **Number this field**.

**Note:** If you reset numbering in Number Maintenance, it only renumbers new records. It leaves the numbering as-is for existing records in system tables.

-   **[Add auto-numbering records in a table](../task/t_AutoNumberingRecordsInATable.md)**  
You can define one number format per table in the system.
-   **[Prepare to left-pad number fields in custom tables](../task/t_PrepToLeftPadNumFldsInCustmTbls.md)**  
Before you configure left padding of number fields on a custom table or a table that does not extend the task table, you must prepare business rules and script includes.
-   **[Prevent numbering gaps](../task/t_PreventNumberingGaps.md)**  
By default, numbers are generated every time a new record is created.
-   **[Enforcing unique numbering](c_EnforcingUniqueNumbering.md)**  
Although duplicate numbers are rare, numbering does not enforce uniqueness, by default.

**Parent Topic:**[Customizing fields on the ServiceNow AI Platform](customize-fields-now-platform-landing.md)

