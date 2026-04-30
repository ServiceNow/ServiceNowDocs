---
title: MID Server proxy preconditions for streaming logs to HLA
description: Requirements for using a MID Server proxy to stream log data to Health Log Analytics.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Health Log Analytics reference, Health Log Analytics, ITOM Health, IT Operations Management]
---

# MID Server proxy preconditions for streaming logs to HLA

Requirements for using a MID Server proxy to stream log data to Health Log Analytics.

-   Use a Squid MID Server proxy to enable streaming log data to Health Log Analytics. For more information, see [Proxy server configuration for MID Servers used for Cloud Discovery and Cloud Provisioning and Governance](../../it-operations-management/reference/mid-server-proxy.md).
-   Install and configure the MID Server proxy with the log ingestion capability enabled.

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    In addition, configure the following properties:

    -   mid.proxy.use\_proxy = true
    -   mid.proxy.host = &lt;proxy\_ip&gt;
    -   mid.proxy.port = &lt;proxy\_port&gt;

**Parent Topic:**[Health Log Analytics reference](../concept/hla-reference.md)

