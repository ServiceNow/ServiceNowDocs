---
title: Configure the ODBC driver for large data sets
description: You can set two ODBC driver properties to deal with errors you receive when using queries that return large amounts of data.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring the ODBC driver, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configure the ODBC driver for large data sets

You can set two ODBC driver properties to deal with errors you receive when using queries that return large amounts of data.

## Before you begin

You must have administrator-level access for the Windows computer on which you want to configure the ODBC driver for large data sets.

## About this task

These properties are set using the ODBC Management Console available on Windows operating systems. For more information, see [ODBC management console properties](../reference/r_SettingODBCProperties.md#ODBC_mgmt_console_properties).

## Procedure

1.  In Windows, navigate to **Start** &gt; **Programs** &gt; **ServiceNow ODBC** &gt; **Management Console**.

2.  Navigate to **Data Source Settings** &gt; **ServiceNow** &gt; **IP Parameters**.

3.  Set the **Timeout** property to be more than the glide.soap.request\_processing\_timeout.odbc value in seconds.

    ODBC makes SOAP calls on the instance. The glide.soap.request\_processing\_timeout.odbc system property is the timeout for the ODBC driver.

4.  Navigate to **Services** &gt; **Service Settings** &gt; **SQL Engine Parameters**.

5.  Increase the **ServiceSQLDiskCacheMaxSize** property.

    Typically, when running a query that returns 50,000 rows, the default value of 200 MB must be increased.


**Parent Topic:**[Configuring the ODBC driver](../concept/configuring-odbc.md)

