---
title: Configure Power BI metadata scanning
description: Enable metadata scanning to access detailed data source information including tables and columns.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-metadata-scan.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Prepare to run the PowerBI collector, PowerBI metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Configure Power BI metadata scanning

Enable metadata scanning to access detailed data source information including tables and columns.

## Before you begin

Role required: admin

You must be a Power BI administrator to enable metadata scanning settings.

## About this task

[Metadata scanning](https://learn.microsoft.com/en-us/fabric/governance/metadata-scanning-overview) provides access to detailed data source information, such as tables and columns, through Power BI read-only admin APIs. The collector uses the Power BI Scanner APIs to establish lineage to source tables and columns. Review the [limitations to the scanner APIs](https://learn.microsoft.com/en-us/power-bi/enterprise/service-admin-metadata-scanning) before configuring the collector.

## Procedure

1.  Enable metadata scanning based on your authentication method.

    -   For service principal authentication:

        1.  Follow the [Power BI documentation](https://learn.microsoft.com/en-us/power-bi/enterprise/service-premium-service-principal) to enable service principal authentication for Power BI read-only APIs
        2.  Enable the following enhanced tenant settings for metadata scanning:
            -   Enhance admin APIs responses with detailed metadata
            -   Enhance admin APIs responses with DAX and mashup expressions
    -   For username and password authentication, enable the following enhanced tenant settings for metadata scanning:

        **Important:** The user must have administrator rights \(Microsoft 365 Global Administrator or Power BI Service Administrator\) to use metadata scanning. For details, see the [Power BI documentation](https://learn.microsoft.com/en-us/power-bi/enterprise/service-admin-metadata-scanning).

        -   Enhance admin APIs responses with detailed metadata
        -   Enhance admin APIs responses with DAX and mashup expressions

**Parent Topic:**[Prepare to run the PowerBI collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-powerbi-collector.md)

