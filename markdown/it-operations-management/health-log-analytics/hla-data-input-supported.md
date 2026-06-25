---
title: Supported data inputs for Health Log Analytics
description: Health Log Analytics \(HLA\) enables you to connect your ServiceNow instance to several types of data input.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/health-log-analytics/hla-data-input-supported.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [data input process, listeners, pullers, passive data inputs, active data inputs, native ServiceNow data inputs]
breadcrumb: [Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Supported data inputs for Health Log Analytics

Health Log Analytics \(HLA\) enables you to connect your ServiceNow instance to several types of data input.

HLA supports the following data input types:

-   Passive data inputs \(listeners\), which wait for log data to be pushed to them. These data inputs require a network port to be open on the MID Server:

    -   [Rsyslog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-rsyslog-beats.md)
    -   [Beats](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-rsyslog-beats.md)
    -   [Splunk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-splunk.md)
    -   [TCP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-tcp.md)
    -   [UDP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-udp.md)
    -   [MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-mid-server.md)
    -   [GCP PubSub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-gcp-pubsub.md)
    -   [REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-rest-api.md)
    The Agent Client Collector data input is supported for use with the [Agent Client Collector Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-log-analytics.md) application, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

-   Active data inputs \(pullers\), which pull data from repositories:

    -   [Elasticsearch](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-elastic.md)
    -   [Splunk Polling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-splunk-polling.md)
    -   [Amazon CloudWatch](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-cloudwatch.md)
    -   [Amazon S3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-s3.md)
    -   [Microsoft Azure Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-azure.md)
    -   [Microsoft Azure Event Hubs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-event-hubs.md)
    -   [Apache Kafka](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-kafka.md)
    For all active data inputs, Health Log Analytics supports MID Server clusters for failover protection. The active data input runs on a single MID Server in the cluster. If that MID Server fails, the system moves its tasks to the next available MID Server in the cluster in a configured order.

    The Elasticsearch data input fetches data from a data repository or database using credentials. If your data is in Elasticsearch, Health Log Analytics must have the following:

    -   Permissions to query Elasticsearch

        One of the following types of credentials:

        -   Basic authentication \(user and password\)
        -   AWS, for Elasticsearch on Amazon AWS Cloud
    -   Network connectivity to the relevant Elasticsearch cluster
    **Note:** Health Log Analytics must be pointed to the correct index to start pulling the data.


In addition, Health Log Analytics supports [Crible](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-cribl.md), [Edge Delta](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-edge-delta.md), and [Vector Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-vector-agent.md) data inputs. These data inputs enable HLA to process log messages that are streaming from these tools into your instance.

## Native ServiceNow data inputs

-   **Streaming logs from Cloud Observability to Health Log Analytics**

    Health Log Analytics can process log data it ingests from the ServiceNow® Cloud Observability application, formerly  Lightstep. HLA automatically sets up the configuration needed to enable log streaming from Cloud Observability as part of its native integration. Setting up the connection from Cloud Observability to HLA must be done in the Cloud Observability application. In HLA, you handle log records from Cloud Observability in the same way as any other Data Input Mapping and Source Type Structure records, as explained in [Log data auto-mapping and mapping in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-automapping.md) and [Source type structure adjustment in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-source-type-structure-adjustment.md). For more information about Cloud Observability, see [Explore Cloud Observability documentation](https://docs.lightstep.com/).


**Parent Topic:**[Health Log Analytics reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-reference.md)

**Related topics**  


[Set up Health Log Analytics on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-implement.md)

