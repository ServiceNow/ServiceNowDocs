---
title: MID Server for metadata collectors
description: When your source is behind a firewall or requires on-premises handling, deploy metadata collectors on a MID Server you host to harvest metadata from on-premises and privately networked data sources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/mid-server-for-metadata-collectors-dc.html
release: australia
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 1
keywords: [MID Server]
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# MID Server for metadata collectors

When your source is behind a firewall or requires on-premises handling, deploy metadata collectors on a MID Server you host to harvest metadata from on-premises and privately networked data sources.

To harvest metadata from on-premises and privately networked data sources, you deploy metadata collectors on a MID Server within your network. This is one of two [deployment models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/metadata-collector-deployment-models.md) available for metadata collectors.

The Management, Instrumentation, and Discovery \(MID\) Server facilitates secure communication and data movement between your ServiceNow instance and external data sources. A configured and validated MID Server is required to connect to the data source. For more information, see the [MID Server documentation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server-landing.md).

## System requirements

The host running the MID Server must meet the following minimum hardware requirements:

|Item|Requirement|
|----|-----------|
|RAM|8 GB|
|CPU|4 GHz processor|

## MID Server configuration guidelines

The following guidelines apply when sizing and configuring the MID Server for metadata collectors:

-   Dedicated MID Server: Use a dedicated MID Server for metadata collectors that connect to external data sources to avoid resource contention with other applications.
-   Minimum memory guidance: Start with a minimum of 8 GB JVM memory. Actual requirements vary based on data volume and complexity.
-   Size-based planning: Estimate data volume in advance and size MID Server resources accordingly.

Consider your data volume and processing requirements when configuring your MID Server. Depending on your environment, you can adjust memory allocation to support your workload.

**Note:** If you experience out-of-memory errors or performance issues, refer to the [MID Server system requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/r_MIDServerSystemRequirements.md) documentation for guidance on adjusting your configuration.

**Parent Topic:**[Configuring metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/configure-metadata-collectors-dc.md)

