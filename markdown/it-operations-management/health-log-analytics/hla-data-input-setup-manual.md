---
title: Set up data inputs for Health Log Analytics manually
description: Set up your data inputs for Health Log Analytics manually. Data input configuration is an essential step in setting up the Health Log Analytics application.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 9
keywords: [ServiceNow, Health Log Analytics, HLA, data input, connector, data input configuration, manual configuration, setup]
breadcrumb: [Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Set up data inputs for Health Log Analytics manually

Set up your data inputs for Health Log Analytics manually. Data input configuration is an essential step in setting up the Health Log Analytics application.

## Before you begin

**Note:** Consider using the Health Log Analytics data input guided setup, which ensures that you have the minimum required setup for the data input process. For more information, see [Set up data inputs using Health Log Analytics guided setup](hla-data-input-setup-guided.md).

**Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   Ensure that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   If the MID Server IP address is exposed by network address translation \(NAT\), a load balancer, or a similar device, it must have a public IP address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=xanadu&pubname=xanadu-servicenow-platform&section=t_SetMIDServerProperties&ft:locale=en-US).
-   For shipping your logs encrypted using SSL TLS, see the [Streaming Data With Rsyslog &amp; Filebeat Using SSL \[KB0866319\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0866319) article in the Now Support Knowledge Base.

-   For MID Server proxy requirements, see [MID Server proxy preconditions for streaming logs to HLA](../reference/hla-mid-proxy-configure.md).

Role required: evt\_mgmt\_admin. For the Glide Syslog data input: admin.

## Procedure

1.  Configure a data input by performing the procedure in the relevant product documentation.

<table id="table_e2g_qbq_2pb"><thead><tr><th>

Data Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Rsyslog or Beats](hla-data-input-rsyslog-beats.md)

</td><td>

The data input streams log data into your instance using Rsyslog or Beats.

</td></tr><tr><td>

[Splunk](hla-data-input-splunk.md)

</td><td>

The data input streams log data into your instance using Splunk.

</td></tr><tr><td>

[Elasticsearch](hla-data-input-elastic.md)

</td><td>

The data input pulls log data from Elasticsearch indexes into your instance.

</td></tr><tr><td>

[TCP](hla-data-input-tcp.md)

</td><td>

The data input sends raw log messages to your instance directly over a TCP/SSL socket.

</td></tr><tr><td>

[UDP](hla-data-input-udp.md)

</td><td>

The data input streams raw log messages to your ServiceNow instance directly over a UDP socket.

</td></tr><tr><td>

[GCP Pub/Sub](hla-data-input-gcp-pubsub.md)

</td><td>

The data input receives log messages that are published to a Google Cloud Pub/Sub topic and streams them to your ServiceNow instance.

</td></tr><tr><td>

[MID Server](hla-data-input-mid-server.md)

</td><td>

The data input collects MID Server log files and streams them to your instance.

</td></tr><tr><td>

[Amazon CloudWatch](hla-data-input-cloudwatch.md)

</td><td>

The data input streams log data from Amazon CloudWatch to your ServiceNow instance.

</td></tr><tr><td>

[Amazon S3](hla-data-input-s3.md)

</td><td>

The data input streams log data from Amazon S3 \(Simple Storage Service\) buckets to your ServiceNow instance.

</td></tr><tr><td>

[Microsoft Azure Log Analytics](hla-data-input-azure.md)

</td><td>

The data input streams log data from Microsoft Azure Log Analytics to your ServiceNow instance.

</td></tr><tr><td>

[Microsoft Azure Event Hubs](hla-data-input-event-hubs.md)

</td><td>

The data input streams events from Microsoft Azure Event Hubs to your ServiceNow instance.

</td></tr><tr><td>

[Apache Kafka](hla-data-input-kafka.md)

</td><td>

The data input streams log data from Apache Kafka to your ServiceNow instance.

</td></tr><tr><td>

[REST API](hla-data-input-rest-api.md)

</td><td>

The data input streams log data to your ServiceNow instance in JSON format.

</td></tr><tr><td>

[ServiceNow System Logs Retriever](hla-data-input-glide-syslog.md)

</td><td>

The data input streams log data from the ServiceNow System Log table to the Health Log Analytics AI engine.**Note:** Only a single ServiceNow System Logs Retriever data input can exist in the system, and only users with the admin role can create and configure it. This data input doesn't run on a MID Server.

</td></tr><tr><td>

Agent Client Collector

</td><td>

The data input streams log messages to your ServiceNow instance using the ServiceNow Agent Client Collector.This data input is supported for use with the [Agent Client Collector Log Analytics](../../agent-client-collector/concept/acc-log-analytics.md) application, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td></tr></tbody>
</table>    **Note:** Selecting **Test connection** at the end of the procedure ensures that your data input is configured correctly. You can only publish a data input configuration when the connection between the MID Server and the data repository has been established.

2.  Identify and address streaming issues to ensure that the data input is streaming log data to the MID Server from all sources.

    For more information, see [Identify and resolve log streaming issues](hla-data-input-streaming.md).

3.  Determine how Health Log Analytics handles raw log data that is streaming into your instance.

    By default, every incoming log line is auto-mapped to the correct tag. If properties aren't discovered automatically, map the data input sources manually by defining a JavaScript function. For more information, see [Map the raw data](hla-data-input-mapping.md).

4.  Modify raw log data before Health Log Analytics maps and structures it.

    For more information, see [Edit your raw log data before processing](hla-data-input-preprocess.md).

5.  Refine the source type structure to make sure that Health Log Analytics extracts and classifies all properties correctly.

    For more information, see [Refine the source type structure](hla-source-type-structure-refine.md).


-   **[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)**  
Configure the data input process manually inHealth Log Analytics . Data input configuration is an essential step in setting up the Health Log Analytics application.
-   **[Identify and resolve log streaming issues](hla-data-input-streaming.md)**  
Identify and address log streaming issues to ensure that the data inputs you have configured for Health Log Analytics are streaming data properly to your ServiceNow instance.
-   **[Edit raw log data before processing](hla-data-input-preprocess.md)**  
You can modify raw log data and drop or break up log messages before they are processed in the MID Server, and therefore before Health Log Analytics maps and structures it. For example, you could prevent sensitive data from reaching the system by replacing user names and passwords with an asterisk \(\*\).
-   **[Log data auto-mapping and mapping](../concept/hla-data-input-automapping.md)**  
By default, the Health Log Analytics AI engine tries to auto-map every incoming log line to the correct tags. You can change automatic mapping results manually by defining a JavaScript function.
-   **[Configure source type capabilities](hla-source-types.md)**  
Health Log Analytics extracts source types automatically in the mapping process. You can add timestamp formats and specify, delete, or exclude keywords for individual source types.
-   **[Add source types manually](hla-source-types-manual.md)**  
Create a source type manually before you configure a data input if you want to stream log data to a specific source type rather than to the source type automatically extracted by Health Log Analytics during the mapping process.
-   **[Source type structure adjustment](../concept/hla-source-type-structure-adjustment.md)**  
Health Log Analytics enables you to reclassify auto-classified properties and change auto-mapped labels. These adjustments help Health Log Analytics machine learning to better understand your priorities.
-   **[Review the properties extracted from a source type in Health Log Analytics](hla-sts-properties-table.md)**  
View the properties that were extracted from all the source types in a source type structure in a single table to identify any setup issues.
-   **[Review the patterns extracted from a source type in Health Log Analytics](hla-view-source-type-patterns.md)**  
View all learned patterns extracted from a source type in a source type structure, together with the log sources in which these patterns appeared. Reviewing these patterns can provide valuable insights into the log message patterns that Health Log Analytics tracks for each source type and log source.
-   **[Additional data input setup tasks](../concept/hla-data-input-setup-extra.md)**  
After performing the initial data input setup and configuration, continue with the remaining data input setup tasks.

**Parent Topic:**[Health Log Analytics data input setup](../concept/hla-implement.md)

**Related topics**  


[Supported data inputs for Health Log Analytics](../reference/hla-data-input-supported.md)

