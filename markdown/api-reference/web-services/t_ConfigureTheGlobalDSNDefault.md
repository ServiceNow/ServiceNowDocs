---
title: Configure the global DSN default
description: Configure the global default used by all newly created DSNs.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring the ODBC driver, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configure the global DSN default

Configure the global default used by all newly created DSNs.

## Before you begin

You must have administrator-level access for the Windows computer on which you want to configure the global DSN default.

## About this task

A default DSN is preloaded with the ODBC driver installation ServiceNow data source. This preloaded DSN connects using the default connection URL, which is set to `https://demo.service-now.com`. To change the global default for the instance URL, do the following.

## Procedure

1.  In Windows, navigate to **Start** &gt; **Programs** &gt; **ServiceNow ODBC** &gt; **Management Console**.

2.  Expand the Console Root tree using the following path:

    `OpenAccess SDK 6.0 Manager\<installation location>\Services\ServiceNow_ODBC\Data Source Settings\ServiceNow\IP Parameters`

    ![ODBC Management Console](../image/OdbcManagementConsole.png)

3.  Double-click the **DataSourceIPProperties** attribute for the ServiceNow data source setting to open the Properties dialog box.

4.  Change the value to the URL of your instance, using the following format, and then click **OK**:

    `https://<your instance>.service-now.com`

    ![ODBC Management Console](../image/OdbcManagementConsole2.png)


**Parent Topic:**[Configuring the ODBC driver](../concept/configuring-odbc.md)

