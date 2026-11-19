---
title: Record numbering
description: In the base system, several tables are numbered, including Incident, Problem, Change Request, and Knowledge. You can also use these numbers anywhere that script is present, for example to generate watermarks for emails. Records in tables can be numbered automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/c\_ManagingRecordNumbering.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customize, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Record numbering

In the base system, several tables are numbered, including Incident, Problem, Change Request, and Knowledge. You can also use these numbers anywhere that script is present, for example to generate watermarks for emails. Records in tables can be numbered automatically.

Administrators can manage record numbering by navigating to **System Definition** &gt; **Number Maintenance**. The current number format for a table, including the prefix \(such as **INC** for incidents or **CHG** for changes\), is stored in a record on the Number \[sys\_number\] table.

\[Omitted image "Number1.png"\] Alt text: A sample of number records, organized alphabetically by prefix.

You can renumber auto-incremented tables that extend the task table or manage numbering with a database field named **Number this field**.

**Note:** If you reset numbering in Number Maintenance, it only renumbers new records. It leaves the numbering as-is for existing records in system tables.

-   **[Add auto-numbering records in a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/t_AutoNumberingRecordsInATable.md)**  
You can define one number format per table in the system.
-   **[Prepare to left-pad number fields in custom tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/t_PrepToLeftPadNumFldsInCustmTbls.md)**  
Before you configure left padding of number fields on a custom table or a table that does not extend the task table, you must prepare business rules and script includes.
-   **[Prevent numbering gaps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/t_PreventNumberingGaps.md)**  
By default, numbers are generated every time a new record is created.
-   **[Enforcing unique numbering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/c_EnforcingUniqueNumbering.md)**  
Although duplicate numbers are rare, numbering does not enforce uniqueness, by default.

**Parent Topic:**[Customizing fields on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/customize-fields-now-platform-landing.md)

