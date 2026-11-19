---
title: MID Server proxy preconditions for streaming logs to Health Log Analytics
description: Requirements for using a MID Server proxy to stream log data to Health Log Analytics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/health-log-analytics/hla-mid-proxy-configure.html
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# MID Server proxy preconditions for streaming logs to Health Log Analytics

Requirements for using a MID Server proxy to stream log data to Health Log Analytics.

-   Use a Squid MID Server proxy to enable streaming log data to Health Log Analytics. For more information, see [Proxy server configuration for MID Servers used for Cloud Discovery and Cloud Provisioning and Governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/mid-server-proxy.md).
-   Install and configure the MID Server proxy with the log ingestion capability enabled.

    \[Omitted image "hla-mid-log-ingestion.png"\] Alt text: MID Server configuration with Log Ingestion capability enabled.

    In addition, configure the following properties:

    -   mid.proxy.use\_proxy = true
    -   mid.proxy.host = &lt;proxy\_ip&gt;
    -   mid.proxy.port = &lt;proxy\_port&gt;

**Parent Topic:**[Health Log Analytics reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-reference.md)

