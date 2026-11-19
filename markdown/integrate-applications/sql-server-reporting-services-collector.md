---
title: SQL Server Reporting Services \(SSRS\) metadata collector
description: The SQL Server Reporting Services \(SSRS\) metadata collector extracts metadata from your SSRS environment into the data catalog. Extracted metadata includes datasets, data sources, folders, KPIs, reports, and linked reports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/sql-server-reporting-services-collector.html
release: australia
topic_type: concept
last_updated: "2026-09-16"
reading_time_minutes: 3
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# SQL Server Reporting Services \(SSRS\) metadata collector

The SQL Server Reporting Services \(SSRS\) metadata collector extracts metadata from your SSRS environment into the data catalog. Extracted metadata includes datasets, data sources, folders, KPIs, reports, and linked reports.

This collector provides you with an effective solution for extracting metadata from your SSRS environment into the catalog. The integration facilitates the automated extraction, organization, and presentation of specific metadata elements from the SSRS system. It gives valuable insights into your datasets, data sources, folders, KPIs, reports, and linked reports – all within the data catalog.

With the SSRS collector, you can:

-   Learn more about your reports and data, including who created a report or dataset and when they were last updated, helping you understand and trust your data.
-   See the lineage of which datasets were used in a report, allowing you a comprehensive view of the data flowing into a report.
-   Keep track of KPIs from SSRS and integrate them with business metrics from other source systems, all within one easy-to-use catalog, leading to better data-informed decisions.

## Metadata cataloged

The following table lists the objects and information cataloged by the SSRS metadata collector.

|Object|Information cataloged|
|------|---------------------|
|Report|ID, Name, Description, Creation Time, Modified Time, Created By, Modified By, Path, Type, Hidden, Size, Data Sources, Favorite, Content Type, Policies|
|Linked Report|ID, Name, Description, Creation Time, Modified Time, Created By, Modified By, Path, Type, Hidden, Size, Content Type, Policies|
|Data Source|ID, Name, Description, Creation Time, Modified Time, Created By, Modified By, Path, Type, Hidden, Size, Parent Folder ID, Connection String, Connection String Overridden, Data Source Type, Credential Retrieval, Content Type, Enabled, Original Connection String Expression Based, Policies|
|Dataset|ID, Name, Description, Creation Time, Modified Time, Created By, Modified By, Path, Type, Hidden, Size, Policies|
|KPI|ID, Name, Description, Creation Time, Modified Time, Created By, Modified By, Path, Type, Hidden, Size, Content Type, Currency, Value Format, Visualization, Content Type, Policies|
|Folder|ID, Name, Description, Creation Time, Modified Time, Created By, Modified By, Path, Type, Hidden, Size, Content Type, Policies|

## Relationship between objects

The following table lists the relationships between SSRS objects cataloged by the metadata collector.

<table><thead><tr><th>

Resource page

</th><th>

Relationship

</th></tr></thead><tbody><tr><td>

Report

</td><td>

-   Integrated Data Source contained within the Report
-   Referenced Datasets contained within the Report
-   Integrated Datasets contained within the Report

</td></tr><tr><td>

Linked Report

</td><td>

The Report that the Linked Report links to / parameterizes

</td></tr><tr><td>

Dataset

</td><td>

Referenced Data Source embedded within the Dataset

</td></tr><tr><td>

KPI

</td><td>

-   Dataset referenced by KPI
-   Data source associated with the KPI Report

</td></tr><tr><td>

Data Source

</td><td>

Dataset that contain a Data Source

</td></tr><tr><td>

Folder

</td><td>

-   SSRS Resources \(KPI, Datasets, Data Sources, Reports, Linked Report\) Contained in Folder
-   Sub-folders contained within the Folder

</td></tr></tbody>
</table>## Lineage for SSRS

The following table lists the lineage information available for SSRS objects.

<table><thead><tr><th>

Object

</th><th>

Lineage available

</th></tr></thead><tbody><tr><td>

Dataset

</td><td>

-   Data Source that the dataset sources its data from
-   Reports that use its data from the dataset

</td></tr><tr><td>

Data source

</td><td>

-   Datasets that sources data from this data source
-   Reports that use data from this data source

</td></tr><tr><td>

Report

</td><td>

-   Datasets from which this report sources data
-   Data sources from which this report sources data

</td></tr></tbody>
</table>## Versions supported

The collector supports SQL Server Reporting Services 2022 configured for Native mode. SSRS running in Sharepoint Mode is not supported.

## Authentication supported

The collector supports Basic authentication and NTLM authentication for SSRS. For details, see the Microsoft documentation at [Authentication with the Report Server](https://learn.microsoft.com/en-us/sql/reporting-services/security/authentication-with-the-report-server?view=sql-server-ver16).

-   **[Prepare SSRS for metadata collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/preparing-to-run-sql-server-reporting-services-collector.md)**  
Configure SQL Server Reporting Services \(SSRS\) authentication and permissions to enable the metadata collector to harvest data sources, reports, and policies.
-   **[Create a SQL Server Reporting Services metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/create-sql-server-reporting-services-metadata-collector.md)**  
Create a collector to import metadata from SQL Server Reporting Services \(SSRS\).

**Parent Topic:**[Configuring metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/configure-metadata-collectors-dc.md)

