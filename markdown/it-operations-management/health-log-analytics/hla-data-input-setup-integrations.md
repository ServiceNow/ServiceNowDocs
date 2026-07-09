---
title: Set up integrations from Integrations Launchpad
description: Set up integrations for Health Log Analytics from the Event Management Integrations Launchpad in Service Operations Workspace for ITOM.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/health-log-analytics/hla-data-input-setup-integrations.html
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [ServiceNow, Health Log Analytics, HLA, data input setup, integration, Integrations Launchpad]
breadcrumb: [Setting up Health Log Analytics on your ServiceNow instance, Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Set up integrations from Integrations Launchpad

Set up integrations for Health Log Analytics from the Event Management Integrations Launchpad in Service Operations Workspace for ITOM.

## Integrations Launchpad

The Integrations Launchpad tool provides a unified interface for convenient integration with connectors that feed raw log messages from external sources into your ServiceNow instance for processing and analysis. For more information, see [Integrations Launchpad in Service Operations Workspace for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/service-operations-workspace-for-itom-apps/integrations-launchpad.md).

## Integrations for Health Log Analytics

The Integrations Launchpad enables the following integrations for Health Log Analytics:

-   **Pull integrations**

    These integrations pull log data from external data sources and stream the data to your instance via a MID Server. Select an integration in the table to open a page with the setup procedure.

<table id="table_qzq_kf1_mcc"><thead><tr><th>

Integration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Elasticsearch]()

</td><td>

Streams log data from Elasticsearch indices to your instance.

</td></tr><tr><td>

[ServiceNow System Logs Retriever]()

</td><td>

Sends log data from the ServiceNow System Log table to the Health Log Analytics AI engine.**Note:** Only a single ServiceNow System Logs Retriever data input can exist in the system, and only users with the admin role can create and configure it. This data input doesn't run on a MID Server.

</td></tr><tr><td>

[Apache Kafka]()

</td><td>

Streams log data from Apache Kafka to your instance.

</td></tr><tr><td>

[Splunk Poller]()

</td><td>

Pulls log data from Splunk to your ServiceNow instance periodically by query.

</td></tr><tr><td>

[Amazon CloudWatch]()

</td><td>

Streams log data from Amazon CloudWatch to your instance.

</td></tr><tr><td>

[Amazon S3]()

</td><td>

Streams log data from Amazon S3 \(Simple Storage Service\) buckets to your instance.

</td></tr><tr><td>

[Microsoft Azure Log Analytics]()

</td><td>

Streams log data from Microsoft Azure Log Analytics to your instance. The connector points the Health Log Analytics AI engine to a data source in your Microsoft Azure Log Analytics account.

</td></tr><tr><td>

[MID Server]()

</td><td>

Collects log messages from the MID Server and streams them to your instance.

</td></tr></tbody>
</table>-   **Push integrations**

    These integrations connect to external data sources that push log data to your instance via a MID Server. Select an integration in the table to open a page with the setup procedure.

    |Integration|Description|
    |-----------|-----------|
    |[UDP]()|Sends raw log messages to your instance directly over a UDP socket.|
    |[TCP]()|Sends raw log messages to your instance directly over a TCP/SSL socket.|
    |[REST API]()|Streams log data to your instance in JSON format.|
    |[GCP PubSub]()|Receives log messages that were published to a Google Cloud Pub/Sub topic and streams them to your instance.|
    |[Splunk UDP]()|Streams log messages to your ServiceNow instance over the UDP transport protocol using a Splunk heavy forwarder.|
    |[Splunk TCP]()|Streams log messages to your ServiceNow instance over the TCP transport protocol using a Splunk heavy forwarder.|
    |[Amazon Data Firehose]()|Streams log messages from Amazon Data Firehose directly to the collector service in ITOM Gateway, where it’s queued for Health Log Analytics processing.|
    |[Vector Agent]()|Enables Health Log Analytics to process log messages that are streaming into your instance via a Vector Agent.|


**Parent Topic:**[Setting up Health Log Analytics on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/health-log-analytics/hla-implement.md)

