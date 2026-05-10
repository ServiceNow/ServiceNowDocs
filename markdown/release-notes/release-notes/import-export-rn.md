---
title: Import and Export release notes
description: The ServiceNow Import and Export applications enable you to import and export data to and from the ServiceNow AI Platform. Import and Export were enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Import and Export release notes

The ServiceNow® Import and Export applications enable you to import and export data to and from the ServiceNow AI Platform. Import and Export were enhanced and updated in the Australia release.

## Import and Export highlights for the Australia release

-   Enable large exports with parallel export sets. Exporting data in parallel can enable your integrations to finish in less time and create less of an impact on other tasks.
-   Configure a separate connection alias for JDBC data sources. Configuring the connection alias separately enables you to reuse it rather than having to reconfigure it with each JDBC data source.

See [Imports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/imports-overview-page.md) and [Exports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/exports-overview-page.md) for more information.

## New in the Australia release

-   **[Enable large exports with parallel export sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-export-sets/parallel-exports.md)**

    Export data with multiple small attachments in parallel. Exporting data in parallel can enable your integrations to finish in less time and create less of an impact on other tasks.

-   **[Use a connection alias for a JDBC data source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/r_JDBCTypeDataSource.md)**

    Configure a separate connection alias for JDBC data sources. Configuring the connection alias separately enables you to reuse it rather than having to reconfigure it with each JDBC data source.


## Changed in this release

-   **The mssql-jdbc.7.4.1.jre8 jar file is no longer part of the MID Server distribution**

    If you have a JDBC data source integration that uses this jar file \(that is, any MSSQL connections\) install this jar file or the vendor recommended jar file according to KB0862383.


## Activation information

Import and Export is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[ServiceNow AI Platform capabilities release notes](../now-platform-capabilities/now-platform-capabilities-rn-landing.md)

