---
title: Set up integrations for Health Log Analytics from the Integrations Launchpad
description: Set up integrations from the Event Management Integrations Launchpad in Service Operations Workspace for ITOM.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/health-log-analytics/hla-data-input-setup-integrations.html
release: brazil
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 7
keywords: [ServiceNow, Health Log Analytics, HLA, data input setup, integration, Integrations Launchpad]
breadcrumb: [Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Set up integrations for Health Log Analytics from the Integrations Launchpad

Set up integrations from the Event Management Integrations Launchpad in Service Operations Workspace for ITOM.

## Integrations Launchpad

The Integrations Launchpad tool provides a unified interface for convenient integration with connectors that feed raw log messages from external sources into your ServiceNow instance for processing and analysis. For more information, see [Integrations Launchpad in Service Operations Workspace for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/integrations-launchpad.md).

## Integrations for Health Log Analytics

The Integrations Launchpad enables the following integrations for Health Log Analytics:

-   **Pull integrations**

    These integrations pull log data from external data sources and stream the data to your instance, typically via a MID Server. Select an integration in the table to open a page with the setup procedure.

<table id="table_qzq_kf1_mcc"><thead><tr><th>

Integration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Amazon CloudWatch]()

</td><td>

Streams log data from Amazon CloudWatch to your instance.

</td></tr><tr><td>

[Amazon S3]()

</td><td>

Streams log data from Amazon S3 \(Simple Storage Service\) buckets to your instance.

</td></tr><tr><td>

[Apache Kafka]()

</td><td>

Streams log data from Apache Kafka to your instance.

</td></tr><tr><td>

[Elasticsearch]()

</td><td>

Streams log data from Elasticsearch indices to your instance.

</td></tr><tr><td>

[Microsoft Azure Event Hubs]()

</td><td>

Streams events from Microsoft Azure Event Hubs to your instance.

</td></tr><tr><td>

[Microsoft Azure Log Analytics]()

</td><td>

Streams log data from Microsoft Azure Log Analytics to your instance. The connector points the Health Log Analytics AI engine to a data source in your Microsoft Azure Log Analytics account.

</td></tr><tr><td>

[MID Server]()

</td><td>

Collects log messages from the MID Server and streams them to your instance.

</td></tr><tr><td>

[ServiceNow System Logs Retriever]()

</td><td>

Sends log data from the ServiceNow System Log table to the Health Log Analytics AI engine.This integration doesn't run on a MID Server.

**Note:** Only a single ServiceNow System Logs Retriever data input can exist in the system, and only users with the admin role can create and configure it.

</td></tr><tr><td>

[Splunk Poller]()

</td><td>

Pulls log data from Splunk to your ServiceNow instance periodically by query.

</td></tr></tbody>
</table>-   **Push integrations**

    These integrations connect to external data sources that push log data to your instance, typically via a MID Server. Select an integration in the table to open a page with the setup procedure.

    |Integration|Description|
    |-----------|-----------|
    |[ACC Log Analytics]()|The ACC-L agent is installed on the monitored host and sends raw log data to your instance via the MID Server.|
    |[Cribl]()|Enables Health Log Analytics to process Cribl log messages streaming into the ServiceNow instance.|
    |[Edge Delta REST]()|Enables Health Log Analytics to process logs it receives from Edge Delta in a distinct format. These logs stream into the ServiceNow instance via REST.|
    |[Edge Delta TCP]()|Enables Health Log Analytics to process logs it receives from Edge Delta in a distinct format. These logs stream into the ServiceNow instance over the TCP transport protocol.|
    |[GCP PubSub]()|Receives log messages that were published to a Google Cloud Pub/Sub topic and streams them to your instance.|
    |[REST API]()|Streams log data to your instance in JSON format.|
    |[Splunk TCP]()|Streams log messages to your ServiceNow instance over the TCP transport protocol using a Splunk heavy forwarder.|
    |[Splunk UDP]()|Streams log messages to your ServiceNow instance over the UDP transport protocol using a Splunk heavy forwarder.|
    |[TCP]()|Sends raw log messages to your instance directly over a TCP/SSL socket.|
    |[UDP]()|Sends raw log messages to your instance directly over a UDP socket.|
    |[Vector Agent]()|Enables Health Log Analytics to process log messages that are streaming into the ServiceNow instance via a Vector Agent.|

-   **MID-less integrations**

    These integrations stream log data directly to your ServiceNow instance, without a MID Server.

    |Integration|Description|
    |-----------|-----------|
    |[AWS Firehose]()|Streams log messages from Amazon Data Firehose directly to the collector service in ITOM Gateway, where it's queued for Health Log Analytics processing.|
    |[Cribl Stream]()|Streams Cribl log data directly to your ServiceNow instance.|
    |[Microsoft Azure Event Hubs \(MID-less\)]()|Streams events from Microsoft Azure Event Hubs to your instance.|
    |[OpenTelemetry Collector]()|Streams log data directly to your ServiceNow instance using the OpenTelemetry \(OTLP\) protocol.|
    |[Splunk OpenTelemetry Collector]()|Streams Splunk log data directly to your ServiceNow instance using the OpenTelemetry \(OTLP\) protocol.|


-   **[MID-less integrations for Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/health-log-analytics/hla-mid-less-integrations-concept.md)**  
Health Log Analytics \(HLA\) supports integrations that stream log data directly to your ServiceNow instance without a MID Server. Use these integrations to simplify your deployment and reduce infrastructure overhead.

**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/health-log-analytics/hla-implement.md)

