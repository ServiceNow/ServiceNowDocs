---
title: Set up integrations from Integrations Launchpad
description: Set up integrations for Health Log Analytics from the Event Management Integrations Launchpad in Service Operations Workspace for ITOM.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2024-12-03"
reading_time_minutes: 6
keywords: [ServiceNow, Health Log Analytics, HLA, data input setup, integration, Integrations Launchpad]
breadcrumb: [Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Set up integrations from Integrations Launchpad

Set up integrations for Health Log Analytics from the Event Management Integrations Launchpad in Service Operations Workspace for ITOM.

## Integrations Launchpad

The Integrations Launchpad tool provides a unified interface for convenient integration with connectors that feed raw log messages from external sources into your ServiceNow instance for processing and analysis. For more information, see [Integrations Launchpad in Service Operations Workspace for ITOM](../../service-operations-workspace-itom/concept/integrations-launchpad.md).

## Integrations for Health Log Analytics

The Integrations Launchpad enables the following integrations for Health Log Analytics:

-   **Pull integrations**

    These integrations pull log data from external data sources and stream the data to your instance via a MID Server. Select an integration in the table to open a page with the setup procedure.

<table id="table_qzq_kf1_mcc"><thead><tr><th>

Integration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Elasticsearch](../task/il-connector-hla-elasticsearch.md)

</td><td>

Streams log data from Elasticsearch indices to your instance.

</td></tr><tr><td>

[ServiceNow System Logs Retriever](../task/il-connector-hla-glide-syslog.md)

</td><td>

Sends log data from the ServiceNow System Log table to the Health Log Analytics AI engine.**Note:** Only a single ServiceNow System Logs Retriever data input can exist in the system, and only users with the admin role can create and configure it. This data input doesn't run on a MID Server.

</td></tr><tr><td>

[Apache Kafka](../task/il-connector-hla-kafka.md)

</td><td>

Streams log data from Apache Kafka to your instance.

</td></tr><tr><td>

[Microsoft Azure Log Analytics](../task/il-connector-hla-azure-la.md)

</td><td>

Streams log data from Microsoft Azure Log Analytics to your instance. The connector points the Health Log Analytics AI engine to a data source in your Microsoft Azure Log Analytics account.

</td></tr><tr><td>

[MID Server](../task/il-connector-hla-mid.md)

</td><td>

Collects log messages from the MID Server and streams them to your instance.

</td></tr></tbody>
</table>-   **Push integrations**

    These integrations connect to external data sources that push log data to your instance via a MID Server. Select an integration in the table to open a page with the setup procedure.

    |Integration|Description|
    |-----------|-----------|
    |[UDP](../task/il-connector-hla-udp.md)|Sends raw log messages to your instance directly over a UDP socket.|
    |[TCP](../task/il-connector-hla-tcp.md)|Sends raw log messages to your instance directly over a TCP/SSL socket.|
    |[REST API](../task/il-connector-hla-rest-api.md)|Streams log data to your instance in JSON format.|
    |GCP PubSub|Receives log messages that were published to a Google Cloud Pub/Sub topic and streams them to your instance.|
    |[Splunk UDP](../task/il-connector-hla-splunkudp.md)|Streams log messages to your ServiceNow instance over the UDP transport protocol using a Splunk heavy forwarder.|
    |[Splunk TCP](../task/il-connector-hla-splunktcp.md)|Streams log messages to your ServiceNow instance over the TCP transport protocol using a Splunk heavy forwarder.|
    |[Amazon Data Firehose](../task/il-connector-hla-firehose.md)|Streams log messages from Amazon Data Firehose directly to the collector service in ITOM Gateway, where it’s queued for Health Log Analytics processing.|


-   **[Configure Elasticsearch integrations](../task/il-connector-hla-elasticsearch.md)**  
Configure an integration for seamless log data streaming from Elasticsearch indices to your instance for processing by Health Log Analytics.
-   **[Set up a GCP PubSub integration for Health Log Analytics](../task/il-connector-hla-gcp-pubsub.md)**  
Set up an integration for receiving log messages that were published to a Google Cloud Platform \(GCP\) Pub/Sub topic and streaming them to your ServiceNow instance.
-   **[Configure a ServiceNow System Logs connector](../task/il-connector-hla-glide-syslog.md)**  
Configure a push connector for streaming log data from the ServiceNow System Log table to the Health Log Analytics AI engine. Integrating with a connector is an essential step in setting up the Health Log Analytics \(HLA\) application.
-   **[Configure UDP integrations](../task/il-connector-hla-udp.md)**  
Configure an integration for sending log data to your ServiceNow instance directly over a UDP socket.
-   **[Configure TCP integrations](../task/il-connector-hla-tcp.md)**  
Configure an integration for sending log data to your ServiceNow instance directly over a TCP/SSL socket.
-   **[../task/il-connector-hla-rest-api.md](../task/il-connector-hla-rest-api.md)**  

-   **[Set up a Microsoft Azure Event Hubs integration for Health Log Analytics](../task/il-connector-hla-event-hubs.md)**  
Set up an integration for streaming events from Microsoft Azure Event Hubs to your ServiceNow instance.
-   **[Configure MID Server integrations](../task/il-connector-hla-mid.md)**  
Configure an integration for collecting and streaming MID Server log messages to your ServiceNow instance for processing by Health Log Analytics.
-   **[Configure Apache Kafka integrations](../task/il-connector-hla-kafka.md)**  
Configure an integration for streaming log data from Apache Kafka to your ServiceNow instance for processing by Health Log Analytics.
-   **[Configure Splunk UDP integrations](../task/il-connector-hla-splunkudp.md)**  
Configure an integration to stream log messages to your ServiceNow instance over the UDP transport protocol using a Splunk heavy forwarder. Health Log Analytics processes the ingested log data.
-   **[Configure Splunk TCP integrations](../task/il-connector-hla-splunktcp.md)**  
Configure an integration to stream log messages to your ServiceNow instance over the TCP transport protocol using a Splunk heavy forwarder. Health Log Analytics processes the ingested log data.
-   **[Configure Microsoft Azure Log Analytics integrations](../task/il-connector-hla-azure-la.md)**  
Configure an integration for streaming log data from Microsoft Azure Log Analytics to your ServiceNow instance. The integration points the Health Log Analytics AI engine to a data source in your Microsoft Azure Log Analytics account.
-   **[Configure Amazon Data Firehose integrations](../task/il-connector-hla-firehose.md)**  
Configure an integration to stream log data from Amazon Data Firehose directly to the ServiceNow data center, where it’s queued for Health Log Analytics processing. There’s no need to store AWS keys on your ServiceNow instance.
-   **[Review log data streaming status and sources of an integration](../task/il-connector-overview-tab.md)**  
Review the log data streaming status and sources of an active integration for Health Log Analytics on the integration's Overview tab. From this tab, you can investigate streaming issues and refine the integration's configuration.
-   **[Edit installed integrations](../task/il-connector-hla-edit.md)**  
Edit an installed integration for streaming log data to Health Log Analytics on the Integrations Launchpad. For example, you can switch to a different service instance.
-   **[Deactivate log data integrations](../task/il-connector-hla-deactivate.md)**  
Deactivate an integration for streaming log data to Health Log Analytics on the Integrations Launchpad.

**Parent Topic:**[Health Log Analytics data input setup](hla-implement.md)

