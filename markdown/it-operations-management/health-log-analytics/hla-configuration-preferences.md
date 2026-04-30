---
title: Health Log Analytics configuration preferences
description: Commonly used settings for Health Log Analytics properties and general configuration.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Health Log Analytics configuration preferences

Commonly used settings for Health Log Analytics properties and general configuration.

## MID Server settings

-   The MID Server log ingestion capability must be enabled.

    **Note:** Enabling **All capabilities** on the MID Server includes enabling the log ingestion capability.

-   Use dedicated MID Servers for log ingestion whenever possible.
-   To enable MID Servers to run multiple products, Health Log Analytics must have at least the Java Virtual Machine \(JVM\) memory setting for the standard product for each MID Server thread configuration.

The preferred MID Server settings for Health Log Analytics are:

-   -   CPUs: 8
-   RAM: 32 GB
-   Network Bandwidth: Up to 10 Gbps
-   EBS Bandwidth: Up to 4,750 Mbps
-   Maximum Java heap size for MID Server: 8,192 MB
    With the above specifications, the expected log ingestion throughput on a Washington DC instance is as follows:

    -   For a log message of 300 bytes: 20,000
    -   For a log message of 1.1 KB: 12,300
    -   For a log message of 2 KB: 7,970
    The minimum requirements for streaming logs to Health Log Analytics are:

    -   CPUs: 4
    -   RAM: 16 GB
    -   Java heap size for MID Server: 8 GB
    For general information, see: [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

-   To increase log ingestion throughput, you can either increase the ulimit or the network bandwidth, or decrease the size of the logs being streamed. The ulimit setting can be configured on an individual MID Server. However, the correlation between the ulimit and the throughput can’t be modified.

    The following table lists the ulimit settings for open files relating to network throughput on the MID Server. It shows the size of the logs being streamed from the MID Server to the agent, and the gRPC streaming rate equivalent to the throughput.

    |Queue Type|Log line size|gRPC rate|
    |----------|-------------|---------|
    |In Memory Queue|300 bytes|18,000|
    |In Memory Queue|1.1 KB|13,000|
    |In Memory Queue|2 KB|10,000|
    |Disk-based Queue|300 bytes|11,000|
    |Disk-based Queue|1.1 KB|5,000|
    |Disk-based Queue|2 KB|3,000|

    Starting from the August 2024 release, you can enhance MID Server communication with the ServiceNow instance by using the Lightning gRPC client, which can increase log streaming speeds to Health Log Analytics by up to six times. The Lightning gRPC client requires manual configuration to activate. For more information, see the [Lightning gRPC client - Enabling the new MID gRPC streaming architecture \[KB1648419\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1648419) article in the Now Support Knowledge Base.

-   By default, the number of data inputs per MID Server is limited to 10. You can configure this limitation for an individual MID Server or for all MID Servers.
-   Both in FIPS and non-FIPS mode, MID Servers with Health Log Analytics capability must run on the Java Runtime Environment \(JRE\) 11 or above.

    **Note:** To support BC-FIPS version 2.0, Health Log Analytics requires an upgrade to version 34.0.37, December 2024.


## Log source retention settings

By default, log retention per source is set to three days. This setting can't be modified.

When using Health Log Analytics application, Version 22.0.12 - December 2021 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home), you can modify the log retention policy per source or for multiple sources together. For more information, see [Modify the log source retention period](../task/hla-log-retention.md).

**Parent Topic:**[Health Log Analytics reference](../concept/hla-reference.md)

