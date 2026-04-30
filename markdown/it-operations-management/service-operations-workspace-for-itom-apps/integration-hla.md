---
title: Configure a connector for Health Log Analytics
description: Integrate log data connectors with your ServiceNow instance to enable seamless streaming of log messages for Health Log Analytics.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2024-08-14"
reading_time_minutes: 3
keywords: [Health Log Analytics, connectors, data inputs, integration]
breadcrumb: [Integrations Launchpad in Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Configure a connector for Health Log Analytics

Integrate log data connectors with your ServiceNow instance to enable seamless streaming of log messages for Health Log Analytics.

Health Log Analytics supports numerous connectors to pull or push log data from external sources into your instance. The connectors are available from the [ServiceNow store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) as well as from third parties. The Integrations Launchpad provides a unified interface for convenient integration with log data connectors. For more information, see [Integrations Launchpad in Service Operations Workspace for ITOM](integrations-launchpad.md).

## Integrations for Health Log Analytics

The Integrations Launchpad enables the following integrations for Health Log Analytics:

-   **Pull integrations**

    These integrations pull log data from external data sources and stream the data to your instance via a MID Server. Select an integration in the table to open a page with the setup procedure.

<table id="table_qzq_kf1_mcc"><thead><tr><th>

Integration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Elasticsearch](../../health-log-analytics-admin/task/il-connector-hla-elasticsearch.md)

</td><td>

Streams log data from Elasticsearch indices to your instance.

</td></tr><tr><td>

[ServiceNow System Logs Retriever](../../health-log-analytics-admin/task/il-connector-hla-glide-syslog.md)

</td><td>

Sends log data from the ServiceNow System Log table to the Health Log Analytics AI engine.**Note:** Only a single ServiceNow System Logs Retriever data input can exist in the system, and only users with the admin role can create and configure it. This data input doesn't run on a MID Server.

</td></tr><tr><td>

[Apache Kafka](../../health-log-analytics-admin/task/il-connector-hla-kafka.md)

</td><td>

Streams log data from Apache Kafka to your instance.

</td></tr><tr><td>

[Microsoft Azure Log Analytics](../../health-log-analytics-admin/task/il-connector-hla-azure-la.md)

</td><td>

Streams log data from Microsoft Azure Log Analytics to your instance. The connector points the Health Log Analytics AI engine to a data source in your Microsoft Azure Log Analytics account.

</td></tr><tr><td>

[MID Server](../../health-log-analytics-admin/task/il-connector-hla-mid.md)

</td><td>

Collects log messages from the MID Server and streams them to your instance.

</td></tr></tbody>
</table>-   **Push integrations**

    These integrations connect to external data sources that push log data to your instance via a MID Server. Select an integration in the table to open a page with the setup procedure.

    |Integration|Description|
    |-----------|-----------|
    |[UDP](../../health-log-analytics-admin/task/il-connector-hla-udp.md)|Sends raw log messages to your instance directly over a UDP socket.|
    |[TCP](../../health-log-analytics-admin/task/il-connector-hla-tcp.md)|Sends raw log messages to your instance directly over a TCP/SSL socket.|
    |[REST API](../../health-log-analytics-admin/task/il-connector-hla-rest-api.md)|Streams log data to your instance in JSON format.|
    |GCP PubSub|Receives log messages that were published to a Google Cloud Pub/Sub topic and streams them to your instance.|
    |[Splunk UDP](../../health-log-analytics-admin/task/il-connector-hla-splunkudp.md)|Streams log messages to your ServiceNow instance over the UDP transport protocol using a Splunk heavy forwarder.|
    |[Splunk TCP](../../health-log-analytics-admin/task/il-connector-hla-splunktcp.md)|Streams log messages to your ServiceNow instance over the TCP transport protocol using a Splunk heavy forwarder.|
    |[Amazon Data Firehose](../../health-log-analytics-admin/task/il-connector-hla-firehose.md)|Streams log messages from Amazon Data Firehose directly to the collector service in ITOM Gateway, where it’s queued for Health Log Analytics processing.|


