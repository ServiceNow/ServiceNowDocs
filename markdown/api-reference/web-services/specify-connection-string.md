---
title: Specify a connection string
description: You can specify a connection string instead of defining a DSN.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring the ODBC driver, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Specify a connection string

You can specify a connection string instead of defining a DSN.

## Before you begin

You must have administrator-level access for the Windows computer on which you want to specify a connection string.

## About this task

This is an alternative method of connecting with different instance URLs. See also [Create a new DSN](t_CreatingANewDSN.md).

A connection string must follow this format:

```
Driver=ServiceNow ODBC driver 32-bit;ServiceName=ServiceNow_ODBC;UID=youruser;PWD=yourpassword;ServerDataSource=ServiceNow;CustomProperties=url=https://<instance>.service-now.com

```

The driver name varies depending on whether you use the 32-bit or 64-bit version of the ODBC driver. To determine your driver name, do the following.

## Procedure

1.  In Windows, navigate to **Start** &gt; **Programs** &gt; **Service-now ODBC** &gt; **ODBC Administrator**.

2.  Select the **System DSN** tab.

3.  Note the value in the **Driver** column for the ServiceNow data source.


**Parent Topic:**[Configuring the ODBC driver](../concept/configuring-odbc.md)

