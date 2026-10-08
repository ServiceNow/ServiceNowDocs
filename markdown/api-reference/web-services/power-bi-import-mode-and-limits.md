---
title: Power BI Desktop data import mode and limits
description: The ServiceNow ODBC driver for Power BI Desktop supports only import mode, not DirectQuery. Understanding this distinction helps you plan refresh schedules and avoid dataset size and large-table filtering issues in your reports.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/web-services/power-bi-import-mode-and-limits.html
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-09-18"
reading_time_minutes: 2
keywords: [Power BI Desktop, import mode, DirectQuery, ODBC driver, dataset size limit]
breadcrumb: [Integrate, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Power BI Desktop data import mode and limits

The ServiceNow ODBC driver for Power BI Desktop supports only import mode, not DirectQuery. Understanding this distinction helps you plan refresh schedules and avoid dataset size and large-table filtering issues in your reports.

## Connection modes

DirectQuery mode is preferable for large tables, but the ServiceNow ODBC driver supports only import mode. Selecting **Load** or **Transform Data** when you connect to ServiceNow instance imports the queried data directly into the Power BI Desktop file.

## How it works

Import mode and DirectQuery mode differ in where data is stored and when it is retrieved:

-   **Import mode**

    Copies the queried rows into the Power BI Desktop file at connection time. The report reads from this local copy, so the data does not update again until a refresh occurs.

-   **DirectQuery mode**

    Keeps the data on the source system. The Power BI Desktop file stores only metadata and any transformation steps. Data is fetched from the source each time a user runs the report, so each report interaction triggers a new connection and data retrieval from the source.


Because import mode copies data into the file, the data becomes stale until it is refreshed. You can refresh manually or set a refresh schedule. Refresh frequency depends on the Power BI license you have. DirectQuery does not require a refresh schedule because each report run fetches current data from the source.

A Power BI Gateway is required to refresh an imported dataset on a schedule from the Power BI Service.

Joins that you create in the Power BI Model view are processed locally in Power BI, not on the ServiceNow instance. Only joins written directly in a SQL statement are pushed down to the source for processing.

For guidance on when to use DirectQuery versus other connectivity modes, see [DirectQuery in Power BI: When to use, limitations, alternatives](https://learn.microsoft.com/en-us/power-bi/connect-data/desktop-directquery-about#quick-decision-guide).

## Dataset size limits

Power BI Pro licenses cap published datasets at 10 GB in the Power BI Service. Because the ServiceNow ODBC driver supports only import mode, this limit applies to every report you build with this connection. DirectQuery datasets aren't affected by this limit because they store only metadata, but DirectQuery is not available with this driver.

The Power BI Desktop file is saved locally before you publish it. When you publish, Power BI compresses the file and uploads it to the Power BI Service, where it counts against your storage allocation.

## Considerations

-   When you select a table in the graphical Navigator interface, column value profiling is based on only the first 1,000 rows. Selecting **Load more** on a large table, such as incident, fetches the entire table dataset. This can exceed limits such as a transaction timeout or the Power BI memory limit. This behavior is reliable only for small tables, such as core\_company and cmn\_location.
-   Incremental refresh may be available to limit a scheduled refresh to recently changed rows, but the setup steps and licensing requirements are unconfirmed.

**Parent Topic:**[Integrate Live Connect Drivers with third-party BI tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/configure-drivers-bi-tools.md)

