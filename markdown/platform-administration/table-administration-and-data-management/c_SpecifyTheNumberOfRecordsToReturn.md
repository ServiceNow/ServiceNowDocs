---
title: Configuring the number of records to return
description: Specify the number of records to return for a database view when the view is used in a script.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/table-administration-and-data-management/c\_SpecifyTheNumberOfRecordsToReturn.html
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Joining tables, Work with database views, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring the number of records to return

Specify the number of records to return for a database view when the view is used in a script.

A property called **glide.db.max\_view\_records** controls the maximum number of rows returned when running a GlideRecord query in a script. The default value for this property is 10000. To change this value, [add the property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md) to the System Property \[sys\_properties\] table and edit the property's **Value** field, which determines the number of rows to return.

This property only applies when querying a database view table in a script. When the database view table is used in a list or report, this property doesn’t apply. Reports or lists based on the database view use all rows in the view.

**Parent Topic:**[Joining tables using database views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_CreatingDatabaseViews.md)

**Previous topic:**[Relabel a column](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/t_RelabelAColumn.md)

**Next topic:**[Test the database view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/t_TestTheDatabaseView.md)

