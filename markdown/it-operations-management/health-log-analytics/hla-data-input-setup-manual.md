---
title: Set up data inputs in Health Log Analytics manually
description: Set up your Health Log Analytics data inputs for Health Log Analytics manually. Data input configuration is an essential step in setting up the Health Log Analytics application.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
keywords: [ServiceNow, Health Log Analytics, HLA, data input, connector, data input configuration, manual configuration, setup]
breadcrumb: [Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Set up data inputs in Health Log Analytics manually

Set up your Health Log Analytics data inputs for Health Log Analytics manually. Data input configuration is an essential step in setting up the Health Log Analytics application.

## Before you begin

**Note:** Consider using the Health Log Analytics data input guided setup, which ensures that you have the minimum required setup for the data input process. For more information, see [Set up data inputs in Health Log Analytics using guided setup](hla-data-input-setup-guided.md).

-   Verify that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   Unless the MID Server and external clients are on the same network, the MID Server must have a public IP address. This is required when its IP is exposed through network address translation \(NAT\), a load balancer, or a similar device. The public IP address enables external clients, such as Filebeat agents located outside its network, to reach the MID Server. Private IP addresses are not routable over the internet. Without a public IP, external clients cannot connect to the MID Server even if they are configured with its address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=australia&pubname=australia-servicenow-platform&section=t_SetMIDServerProperties&ft:locale=en-US). If the MID Server and external clients are on the same network, connections can be made using the private IP address.
-   For shipping your logs encrypted using SSL TLS, see the [Streaming Data With Rsyslog &amp; Filebeat Using SSL \[KB0866319\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0866319) article in the Now Support Knowledge Base.

-   For MID Server proxy requirements, see [MID Server proxy preconditions for streaming logs to Health Log Analytics](../reference/hla-mid-proxy-configure.md).

Role required: evt\_mgmt\_admin. For the ServiceNow System Logs data input: admin.

## Procedure

1.  Setup a data input manually by performing the relevant procedure described in the product documentation.

<table id="table_e2g_qbq_2pb"><thead><tr><th>

Data Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agent Client Collector

</td><td>

The data input streams log messages to your ServiceNow instance using the ServiceNow Agent Client Collector.This data input is supported for use with the [Agent Client Collector Log Analytics](../../agent-client-collector/concept/acc-log-analytics.md) application, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td></tr><tr><td>

[Amazon CloudWatch](hla-data-input-cloudwatch.md)

</td><td>

The data input streams log data from Amazon CloudWatch to your ServiceNow instance.

</td></tr><tr><td>

[Amazon S3 Bucket](hla-data-input-s3.md)

</td><td>

The data input streams log data from Amazon S3 \(Simple Storage Service\) buckets to your ServiceNow instance.

</td></tr><tr><td>

[Apache Kafka](hla-data-input-kafka.md)

</td><td>

The data input streams log data from Apache Kafka to your ServiceNow instance.

</td></tr><tr><td>

[Cribl](../../hardware-asset-management/task/hla-data-input-cribl.md)

</td><td>

The data input to enables Health Log Analytics to process Cribl log messages streaming into your ServiceNow instance.

</td></tr><tr><td>

[Edge Delta](hla-data-input-edge-delta.md)

</td><td>

The data input enables Health Log Analytics to process Edge Delta log messages streaming into your ServiceNow instance.

</td></tr><tr><td>

[Elasticsearch](hla-data-input-elastic.md)

</td><td>

The data input pulls log data from Elasticsearch indexes into your instance.

</td></tr><tr><td>

[GCP PubSub](hla-data-input-gcp-pubsub.md)

</td><td>

The data input receives log messages that are published to a Google Cloud Pub/Sub topic and streams them to your ServiceNow instance.

</td></tr><tr><td>

[Microsoft Azure Event Hubs](hla-data-input-event-hubs.md)

</td><td>

The data input streams events from Microsoft Azure Event Hubs to your ServiceNow instance.

</td></tr><tr><td>

[Microsoft Azure Log Analytics](hla-data-input-azure.md)

</td><td>

The data input streams log data from Microsoft Azure Log Analytics to your ServiceNow instance.

</td></tr><tr><td>

[MID Server](hla-data-input-mid-server.md)

</td><td>

The data input collects MID Server log files and streams them to your instance.

</td></tr><tr><td>

[REST API](hla-data-input-rest-api.md)

</td><td>

The data input streams log data to your ServiceNow instance in JSON format.

</td></tr><tr><td>

[Rsyslog or Beats](hla-data-input-rsyslog-beats.md)

</td><td>

The data input streams log data into your instance using Rsyslog or Beats.

</td></tr><tr><td>

[ServiceNow System Logs Retriever](hla-data-input-glide-syslog.md)

</td><td>

The data input streams log data from the ServiceNow System Log table to the Health Log Analytics AI engine.**Note:** Only a single ServiceNow System Logs Retriever data input can exist in the system, and only users with the admin role can create and configure it. This data input doesn't run on a MID Server.

</td></tr><tr><td>

[Splunk](hla-data-input-splunk.md)

</td><td>

The data input streams log data into your instance using Splunk.

</td></tr><tr><td>

[Splunk Polling](hla-data-input-splunk-polling.md)

</td><td>

The data input periodically pulls log data from Splunk by using a query.

</td></tr><tr><td>

[TCP](hla-data-input-tcp.md)

</td><td>

The data input sends raw log messages to your instance directly over a TCP/SSL socket.

</td></tr><tr><td>

[UDP](hla-data-input-udp.md)

</td><td>

The data input streams raw log messages to your ServiceNow instance directly over a UDP socket.

</td></tr><tr><td>

[Vector Agent](hla-data-input-vector-agent.md)

</td><td>

The data input enables Health Log Analytics to process log messages that are streaming into your ServiceNow instance via a Vector Agent.

</td></tr></tbody>
</table>    **Note:** Testing the connection to the MID Server at the end of the data input setup procedure ensures that your data input is configured correctly. You can only publish a data input configuration when the connection between the MID Server and the data repository has been established.

2.  Identify and address streaming issues to confirm that the data input is streaming log data to the MID Server from all sources.

    For more information, see [Identify and resolve a log streaming issue in Health Log Analytics](hla-data-input-streaming.md).

3.  Edit raw log data before Health Log Analytics maps and structures it.

    For more information, see [Edit your raw log data before processing](hla-data-input-preprocess.md).

4.  Determine how Health Log Analytics handles raw log data that is streaming into your instance.

    By default, every incoming log line is auto-mapped to the correct tag. If properties aren't discovered automatically, map the data input sources manually by defining a JavaScript function. For more information, see [Map the raw data](hla-data-input-mapping.md).

5.  Tweak the source type structure to make sure that Health Log Analytics extracts and classifies all properties correctly.

    For more information, see [Refine the source type structure in Health Log Analytics](hla-source-type-structure-refine.md).

6.  Perform additional data input setup tasks.

    For more information, see [Additional data input setup tasks in Health Log Analytics](../concept/hla-data-input-setup-extra.md).


-   **[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)**  
Configure the data input process manually in Health Log Analytics. Data input configuration is an essential step in setting up the Health Log Analytics application.
-   **[Identify and resolve a log streaming issue in Health Log Analytics](hla-data-input-streaming.md)**  
Find and address log streaming issues to verify that your data inputs are streaming log data to your instance properly.
-   **[Additional data input setup tasks in Health Log Analytics](../concept/hla-data-input-setup-extra.md)**  
After performing the initial data input setup and configuration in Health Log Analytics, continue with the remaining data input setup tasks.
-   **[Advanced data input configuration in Health Log Analytics](../concept/hla-data-input-adv-configuration.md)**  
When you have configured a data input successfully, Health Log Analytics adds a record to the Data Inputs table and attaches the configuration file to it. You can configure advanced settings for your data input. Configuring advanced settings is optional.
-   **[Stop or restart a data input in Health Log Analytics](hla-data-input-stop-start.md)**  
You can stop using a data input for streaming log messages to your ServiceNow instance. Restart the data input if you want it to resume streaming data.

**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](../concept/hla-implement.md)

**Related topics**  


[Supported data inputs for Health Log Analytics](../reference/hla-data-input-supported.md)

