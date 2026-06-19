---
title: Use the ODBC driver in Crystal Reports
description: After installing the ODBC driver and its associated DSN, use it in Crystal Reports as a data source provider.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/t\_UseODBCDriverCrysRpts.html
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ODBC and client applications, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Use the ODBC driver in Crystal Reports

After installing the ODBC driver and its associated DSN, use it in Crystal Reports as a data source provider.

## About this task

**Note:** Crystal Reports includes the configuration file CRConfig.xml that contains the JVM minimum heap size \(Xms\) and maximum heap size \(Xmx\) values. When configuring the ODBC driver with Crystal Reports, ensure that the ODBC driver uses the same minimum and maximum JVM heap size as Crystal Reports. If these values do not match, update the ODBC driver settings, not the Crystal Reports settings.

## Procedure

1.  Create a new Standard Report.

    \[Omitted image "CrystalStandard.png"\] Alt text: Crystal Reports Standard Report

2.  Create a new connection using the ServiceNow DSN.

    \[Omitted image "ServiceNowDSN.png"\] Alt text: Creating a New Connection Using the ServiceNow DSN

3.  Select a table from the list of available tables.

    \[Omitted image "AvailableTables.png"\] Alt text: Selecting a Table from List of Available Tables

4.  Select the available fields from the selected table.

    \[Omitted image "AvailableFields.png"\] Alt text: Selecting the Available Fields from the Selected Table

5.  Click **Finish** to render the report.

    \[Omitted image "RenderedCrystalReport.png"\] Alt text: Rendered Crystal Report


**Parent Topic:**[ODBC and client applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/r_ODBCAndClientApplications.md)

