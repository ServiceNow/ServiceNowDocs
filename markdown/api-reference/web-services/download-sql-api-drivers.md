---
title: Download the SQL API drivers on client machine
description: Download the ODBC and JDBC drivers from the ServiceNow store to your client machine to enable SQL API connectivity.
locale: en-us
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Download the SQL API drivers on client machine

Download the ODBC and JDBC drivers from the ServiceNow store to your client machine to enable SQL API connectivity.

## Before you begin

Role required: admin

## About this task

After configuring the SQL API plugin on your ServiceNow instance, you must download the ODBC and JDBC drivers to your client machine. These drivers enable your Business Intelligence tools and data analysis platforms to connect to your ServiceNow data.

## Procedure

1.  Go to [ServiceNow Store](http://store.servicenow.com).

2.  Search for `SQL API`.

    The SQL API Drivers page appears.

3.  Select **Get**.

    The ServiceNow SQL API Driver ZIP file is downloaded on your client machine.

    The ZIP file contains two folders:

    -   `ServiceNow SQL API- ODBC driver`: This folder contains the ODBC driver executables for both 32-bit and 64-bit architectures, and a dependencies folder with JAR files.
    -   `ServiceNow SQL API- JDBC driver`: This folder contains the JDBC driver JAR files.

## Result

The SQL API drivers are downloaded to your client machine and ready for installation and configuration.

## What to do next

After downloading the drivers, proceed to install and configure them on your client machine.

-   For ODBC driver installation, see [Install ServiceNow SQL API ODBC driver on client machine](install-odbc-driver.md).
-   For JDBC driver configuration, see [Configure ServiceNow SQL API JDBC driver on client machine](configure-jdbc-driver.md).

**Parent Topic:**[Configuring SQL API](../concept/configuring-sql-api.md)

