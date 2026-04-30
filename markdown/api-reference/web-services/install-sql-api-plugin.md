---
title: Install SQL API plugin on your ServiceNow instance
description: Installing the SQL API on your instance enables secure, read-only access to your instance data from external applications. You can integrate your data with external tools and analytics platforms to enhance your reporting and data analysis capabilities.
locale: en-us
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Install SQL API plugin on your ServiceNow instance

Installing the SQL API on your instance enables secure, read-only access to your instance data from external applications. You can integrate your data with external tools and analytics platforms to enhance your reporting and data analysis capabilities.

## Before you begin

You must have an appropriate RaptorDB Pro entitlement to install the SQL API plugin.

Role required: admin

## About this task

Install the SQL API plugin to enable the ODBC and JDBC drivers to connect to your ServiceNow instance.

## Procedure

1.  Navigate to **All** &gt; **Application Manager**.

2.  Search for `SQL API` and select the **SQL API** tile.

3.  Select **Install**.

    ![UI screen for installing SQL API on your ServiceNow instance](../image/install-sql-api-on-instance-welcome.png)

4.  Review the installation details and do one of the following:

    -   To install the ODBC and JDBC driver plugins immediately, select **Install now**.
    -   To schedule the installation later, do the following:
        1.  Select **Install later**.
        2.  Set the **Start date** and **Start time**.
        3.  Select **Schedule**.
    ![UI screen to install immediately or schedule for later](../image/sql-api-instance-schedule.png)

5.  Verify the plugin installation by selecting **View details**.


## Result

The SQL API plugin is installed on your ServiceNow instance. You can proceed to [Configure SQL API plugin on your ServiceNow instance](../task/configure-sql-api-overview.md) and create service accounts, set up access control lists, and define IP filter criteria.

**Parent Topic:**[Configuring SQL API](configuring-sql-api.md)

