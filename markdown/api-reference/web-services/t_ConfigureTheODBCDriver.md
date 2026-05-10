---
title: Configure the ODBC driver
description: Configure the ODBC driver to connect to your ServiceNow instance.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring the ODBC driver, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configure the ODBC driver

Configure the ODBC driver to connect to your ServiceNow instance.

## Before you begin

You must have administrator-level access for the Windows computer on which you want to configure the ODBC driver.

## About this task

After the driver is installed, configure it for your instance. The driver is preconfigured to connect to `https://demoodbc.service-now.com` using the DSN ServiceNow. There are two ways to configure connectivity for the driver.

-   Configure the global default used by all newly created DSNs.
-   Configure each new DSN with its own connection.

## Procedure

1.  In Windows, navigate to **Start** &gt; **Programs** &gt; **ServiceNow ODBC Management Console**.

2.  Expand the Console Root tree to: `ServiceNow ODBC Manager\Manager\<installation location>\Services\ServiceNow_ODBC\Data Source Settings\ServiceNow\IP Parameters`.

3.  Double-click the **DataSourceIPProperties** attribute.

4.  Change the **Value** to the URL of your instance, such as `https://<instance>.service-now.com`.

    If integrating the ODBC driver with Edge Encryption, change the **Value** to the URL of your encryption proxy. See [Edge Encryption ODBC driver integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/c_IntegrateODBCWithEdge.md) for more information.

5.  Click **OK**.


**Parent Topic:**[Configuring the ODBC driver](../concept/configuring-odbc.md)

