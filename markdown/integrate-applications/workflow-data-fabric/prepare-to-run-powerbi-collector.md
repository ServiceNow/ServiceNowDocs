---
title: Prepare to run the PowerBI collector
description: Set up Azure application registration, authentication, and permissions before running the collector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/prepare-to-run-powerbi-collector.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [PowerBI metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the PowerBI collector

Set up Azure application registration, authentication, and permissions before running the collector.

## Before you begin

Role required: admin

**Important:** A Power BI Administrator is needed to enable settings in the Power BI Admin Portal.

## About this task

The collector uses Azure application registration and supports two authentication methods: service principal or username and password. You must register an application, configure authentication, enable metadata scanning, and retrieve the tenant ID. Optionally, configure report image harvesting and lineage mapping.

## Procedure

1.  Register an application in Azure and create client credentials.

    See [Register Power BI application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-powerbi-collector-register-app.md).

2.  Configure authentication based on your preferred method.

    -   For service principal authentication, see [Configure Power BI service principal authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-service-principal-auth.md).

    -   For username and password authentication, see [Configure Power BI username and password authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-username-auth.md).

3.  Enable metadata scanning to access detailed data source information.

    See [Configure Power BI metadata scanning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-metadata-scan.md).

4.  Get the Power BI tenant ID.

    See [Get Power BI tenant ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-get-tenant-id.md).

5.  Configure report image harvesting to collect preview images from Power BI reports.

    See [Configure Power BI report image harvesting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-report-image-harvest.md).

6.  Configure lineage mapping for ODBC connections, server aliases, or custom SQL statements.

    See [Configure Power BI lineage mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-lineage-mapping.md) .


-   **[Register Power BI application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-powerbi-collector-register-app.md)**  
Register an application in Azure and create client credentials for Power BI collector authentication.
-   **[Configure Power BI service principal authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-service-principal-auth.md)**  
Set up service principal authentication to enable Power BI metadata collection.
-   **[Configure Power BI username and password authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-username-auth.md)**  
Set up API permissions for username and password authentication to enable Power BI metadata collection.
-   **[Configure Power BI metadata scanning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-metadata-scan.md)**  
Enable metadata scanning to access detailed data source information including tables and columns.
-   **[Get Power BI tenant ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-get-tenant-id.md)**  
Retrieve the tenant ID from the Power BI application.
-   **[Configure Power BI report image harvesting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-report-image-harvest.md)**  
Enable report image harvesting to collect preview images from Power BI reports.
-   **[Configure Power BI lineage mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-lineage-mapping.md)**  
Create a YAML file to map data sources for lineage harvesting.

**Parent Topic:**[PowerBI metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/powerbi-metadata-collector.md)

