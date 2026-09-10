---
title: Install Live Connect on your ServiceNow instance
description: Install Live Connect to enable secure, read-only access to your instance data from external applications.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/install-sql-api-plugin.html
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Install Live Connect on your ServiceNow instance

Install Live Connect to enable secure, read-only access to your instance data from external applications.

## Before you begin

|Requirement|Details|
|-----------|-------|
|Entitlement|Check your entitlements to determine whether you have access to RaptorDB Professional v2.|
|Platform release|At least Zurich Patch 8 or Australia Patch 2 releases.|

Role required: admin

## About this task

Installing the Live Connect installs the SQL API plugin, which enables the ODBC and JDBC drivers to connect to your ServiceNow instance. BI tools and analytics platforms can then query the data to enhance their reporting and data analysis capabilities.

## Procedure

1.  Navigate to **All** &gt; **Application Manager**.

2.  Search for live connect and select the **Live Connect** tile.

    The SQL API plugin \[com.glide.rest.sqlapiserver\], which is a unified installer for ODBC and JDBC server side plugins, is selected for download during this installation.

3.  Select **Install** and review the installation instructions.

    -   To install immediately, select **Install now**.
    -   To schedule the installation, do the following:
        1.  Select **Install later**.
        2.  Set the **Start date** and **Start time**.
        3.  Select **Schedule**.
4.  Verify that the Live Connect plugin \(SQL API\) is installed successfully by selecting **View details**.


**Parent Topic:**[Configuring Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configuring-sql-api.md)

