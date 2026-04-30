---
title: Set up integrations from Integrations Launchpad
description: Set up integrations for Health Log Analytics from the Event Management Integrations Launchpad in Service Operations Workspace for ITOM.
locale: en-US
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

[Splunk Poller](../task/il-connector-hla-splunk-polling.md)

</td><td>

Pulls log data from Splunk to your ServiceNow instance periodically by query.

</td></tr><tr><td>

[Amazon CloudWatch](../task/il-connector-hla-aws-cloudwatch.md)

</td><td>

Streams log data from Amazon CloudWatch to your instance.

</td></tr><tr><td>

[Amazon S3](../task/il-connector-hla-aws-s3.md)

</td><td>

Streams log data from Amazon S3 \(Simple Storage Service\) buckets to your instance.

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
    |[GCP PubSub](../task/il-connector-hla-gcp-pubsub.md)|Receives log messages that were published to a Google Cloud Pub/Sub topic and streams them to your instance.|
    |[Splunk UDP](../task/il-connector-hla-splunkudp.md)|Streams log messages to your ServiceNow instance over the UDP transport protocol using a Splunk heavy forwarder.|
    |[Splunk TCP](../task/il-connector-hla-splunktcp.md)|Streams log messages to your ServiceNow instance over the TCP transport protocol using a Splunk heavy forwarder.|
    |[Amazon Data Firehose](../task/il-connector-hla-firehose.md)|Streams log messages from Amazon Data Firehose directly to the collector service in ITOM Gateway, where it’s queued for Health Log Analytics processing.|
    |[Vector Agent](../task/il-connector-hla-vector.md)|Enables Health Log Analytics to process log messages that are streaming into your instance via a Vector Agent.|


**Parent Topic:**[Setting up Health Log Analytics on your ServiceNow instance](hla-implement.md)

