---
title: MID Server for metadata collectors
description: When your source is behind a firewall or requires on-premises handling, deploy metadata collectors on a MID Server you host to harvest metadata from on-premises and privately networked data sources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/mid-server-for-metadata-collectors-dc.html
release: australia
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 2
keywords: [MID Server]
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# MID Server for metadata collectors

When your source is behind a firewall or requires on-premises handling, deploy metadata collectors on a MID Server you host to harvest metadata from on-premises and privately networked data sources.

To harvest metadata from on-premises and privately networked data sources, you deploy metadata collectors on a MID Server within your network. This is one of two [deployment models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/metadata-collector-deployment-models.md) available for metadata collectors.

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

## MID Server routing models

When a metadata collector is deployed on a MID Server, a routing model determines which MID Server or cluster executes each collection job. The routing model applies to all runs and can be changed by an administrator at any time.

-   **Auto-select**

    The system selects any available MID Server at job execution time. This is the default routing model. Auto-select supports two optional constraints: selection can be restricted to MID Servers that advertise specific capabilities, or narrowed to MID Servers running a particular application.

-   **Designated MID Server**

    The collection job always runs on a single, named MID Server. If that MID Server is unavailable at job execution time, the job fails with an error identifying it by name. This model is suited for sources that require a specific network path, credential set, or capability that only one MID Server in the environment provides.

-   **Designated MID cluster**

    The collection job runs on any available MID Server within a named cluster. This model supports load distribution and failover across MID Servers that share access to the source.


**Parent Topic:**[Configuring metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/configure-metadata-collectors-dc.md)

