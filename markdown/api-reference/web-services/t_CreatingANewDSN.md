---
title: Create a new DSN
description: Use the ODBC driver and the ServiceNow data source to create an unlimited number of DSNs configured to connect with different instance URLs.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring the ODBC driver, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Create a new DSN

Use the ODBC driver and the ServiceNow data source to create an unlimited number of DSNs configured to connect with different instance URLs.

## Before you begin

You must have administrator-level access for the Windows computer that you want to create a new DSN on.

Role required: admin

## About this task

Select the target instance for your ODBC connection by DSN name. As an option during installation or upgrade, you can elect to keep the DSNs when you uninstall.

Instead of creating a new DSN, you can [Specify a connection string](specify-connection-string.md) to connect with different instance URLs.

## Procedure

1.  In Windows, navigate to **Start** &gt; **Programs** &gt; **Service-now ODBC** &gt; **ODBC Administrator**.

    ![ODBC DSN.](../image/OdbcDsn.png)

2.  To create a system DSN, select the **System DSN** tab, and then click **Add**.

    ![Add an ODBC DSN.](../image/OdbcDsnAdd.png)

3.  Select ServiceNow **ODBC driver 32-bit** from the list, and then click **Finish**.

4.  Configure the driver and its connection URL by specifying the url= parameter value in the **Custom Properties** field.

    For example: `url=https://myinstance.service-now.com`

    ![ODBC DSN driver setup.](../image/OdbcDsnConfDriver.png)

5.  Click **OK**.


## Result

You can now use the new driver.

**Parent Topic:**[Configuring the ODBC driver](../concept/configuring-odbc.md)

