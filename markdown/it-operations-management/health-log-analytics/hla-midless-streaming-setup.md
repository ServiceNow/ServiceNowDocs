---
title: Set up log streaming via ITOM Gateway for Health Log Analytics
description: Set up log streaming via ITOM Gateway to enable Health Log Analytics \(HLA\) to receive log data directly from external sources without a MID Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/health-log-analytics/hla-midless-streaming-setup.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-05-04"
reading_time_minutes: 3
breadcrumb: [MID-less log streaming, MID-less integrations, Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Set up log streaming via ITOM Gateway for Health Log Analytics

Set up log streaming via ITOM Gateway to enable Health Log Analytics \(HLA\) to receive log data directly from external sources without a MID Server.

## Before you begin

-   Review the [MID-less log streaming via ITOM Gateway in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-midless-streaming.md) documentation.
-   Verify that Health Log Analytics version 36.0.19 or higher is installed on your instance.
-   Verify that HLA provisioning is complete. Confirm that the AI Engine and Elasticsearch show green status at: `https://<instance>.service-now.com/xmlstats.do?include=services_status`.
-   Verify that ITOM Cloud Services Core is installed on your instance.
-   Verify that a JWT provider and token are configured on your instance. For more information, see [Configure a JSON Web Token \(JWT\) provider and token for Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-jwt-token-config.md).
-   \(High-volume deployments only\) If you expect 30,000 or more log events per second, contact ServiceNow Support to request infrastructure scaling. Proceed to the log streaming via ITOM Gateway setup procedure only after ServiceNow confirms that scaling is complete.

    Provide the following information:

    |Information|Example|
    |-----------|-------|
    |Expected maximum log events per second|100,000 log events per second from all sources|
    |Environment URL or URLs|&lt;customer&gt;prod.service-now.com|
    |Preferred migration date and time|Sundays, overnight US time preferred|

    **Note:** Scaling requires a 6-hour change window and expected HLA downtime of 2–6 hours.


Role required: evt\_mgmt\_admin

## About this task

Log streaming via ITOM Gateway removes the MID Server from the log ingestion path. External log sources send data directly to the ITOM Gateway, which routes it through the  Hermes  Messaging Service to the HLA AI Engine. For more information, see [MID-less log streaming via ITOM Gateway in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-midless-streaming.md).

Setup involves two stages: enabling ITOM Gateway and Hermes on your instance, and creating an integration from Integrations Launchpad.

Supported log sources include [AWS Firehose](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/il-connector-hla-firehose.md), Cribl Stream, and OpenTelemetry Collector.

## Procedure

1.  Enable ITOM Gateway and the  Hermes  Messaging Service.

    1.  Navigate to **All**.

    2.  In the navigation filter, enter **sys\_service.list** and press Enter.

    3.  In the **Services** table, verify that an entry for `itom-hla-gw` exists with a corresponding `sys_service_endpoint` entry.

    4.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

    5.  Search for the property `mid.hla.itom_gateway_streaming.enabled` and set it to true.

        All MID Servers automatically switch to ITOM Gateway streaming mode.

    **Note:** MID Servers re-establish gRPC connections. Data inputs are not restarted.

2.  Set up the integration from Integrations Launchpad.

    For more information, see [Set up integrations for Health Log Analytics from the Integrations Launchpad](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-setup-integrations.md).

3.  On the **Overview** tab of the integration, confirm that the ITOM Gateway URL, Integration ID, and Token values are populated.

    If these values appear, log streaming via ITOM Gateway setup is complete.


**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-implement.md)

