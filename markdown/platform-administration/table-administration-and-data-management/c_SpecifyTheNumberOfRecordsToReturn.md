---
title: Specify the number of records to return
description: Specify the number of records to return for a database view when the view is used in a script.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-03-26"
reading_time_minutes: 1
breadcrumb: [Database view creation, Work with database views, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Specify the number of records to return

Specify the number of records to return for a database view when the view is used in a script.

A property called **glide.db.max\_view\_records** controls the maximum number of rows returned when running a GlideRecord query in a script. The default value for this property is 10000. To change this value, [add the property](../../../administer/reference-pages/reference/r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table and edit the property's **Value** field, which determines the number of rows to return.

This property only applies when querying a database view table in a script. When the database view table is used in a list or report, this property doesn’t apply. Reports or lists based on the database view use all rows in the view.

**Parent Topic:**[Database view creation](../task/c_CreatingDatabaseViews.md)

**Previous topic:**[Relabel a column](../task/t_RelabelAColumn.md)

**Next topic:**[Test the database view](../task/t_TestTheDatabaseView.md)

