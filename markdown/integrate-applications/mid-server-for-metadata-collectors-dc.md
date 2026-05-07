---
title: MID Server for metadata collectors
description: Set up a MID Server to host metadata collectors that harvest metadata from on-premises and privately networked data sources.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# MID Server for metadata collectors

Set up a MID Server to host metadata collectors that harvest metadata from on-premises and privately networked data sources.

For the Data Catalog capability within Workflow Data Fabric \(WDF\), the MID Server hosts metadata collectors that harvest metadata — schemas, tables, columns, and lineage — from on-premises and privately networked data sources, then securely uploads them to the ServiceNow instance for cataloging, governance, and AI-ready workflows.

The Management, Instrumentation, and Discovery \(MID\) Server facilitates secure communication and data movement between your ServiceNow instance and external data sources. You must have a configured and validated MID Server to connect to the data source. For more information, see the [MID server documentation](https://www.servicenow.com/docs/access?context=mid-server-landing&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## System requirements

Verify that the host running the MID Server meets the following minimum hardware requirements before configuring metadata collectors.

|Item|Requirement|
|----|-----------|
|RAM|8 GB|
|CPU|4 GHz processor|

## Recommended MID Server configuration

Consider the following recommendations when sizing and configuring the MID Server for metadata collectors:

-   **Dedicated MID Server:** Use a dedicated MID Server for metadata collectors that connect to external data sources to avoid resource contention with other applications.
-   **Minimum memory guidance:** Start with a minimum of 8 GB JVM memory. Actual requirements vary based on data volume and complexity.
-   **Size-based planning:** Estimate data volume in advance and size MID Server resources accordingly.

Consider your data volume and processing requirements when configuring your MID Server. Depending on your environment, you may want to adjust memory allocation to support your workload.

**Note:** If you experience out-of-memory errors or performance issues, refer to the [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) documentation for guidance on adjusting your configuration.

**Parent Topic:**[Configuring metadata collectors](configure-metadata-collectors-dc.md)

