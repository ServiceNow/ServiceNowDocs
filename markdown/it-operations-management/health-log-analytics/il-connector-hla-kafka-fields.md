---
title: Apache Kafka integration configuration fields
description: Description of the fields on the Apache Kafka integration configuration forms for Health Log Analytics.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Kafka, data input, integration, configuration, field, description, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Integration configuration fields, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Apache Kafka integration configuration fields

Description of the fields on the Apache Kafka integration configuration forms for Health Log Analytics.

For the Apache Kafka integration setup procedure, see [Set up an Apache Kafka integration for Health Log Analytics](../task/il-connector-hla-kafka.md).

<table id="table_cnt_1x5_l2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Name

</td><td>

Unique name of this integration. For example: My Kafka integration. This field is required.**Note:** When you fill in this field, the generic name displayed on the form adjusts automatically to match the name you entered.

</td></tr><tr><td>

Execute on

</td><td>

Option to select whether to use a specific MID Server or a MID Server cluster. This field is required.

</td></tr><tr><td>

MID server name

</td><td>

\(Only when the **Execute on** field is set to Specific MID Server\)

MID Server to which log data from Apache Kafka is pulled. This field is required.**Note:**

-   You can select only MID Servers that support basic authentication. MID Servers that support mTLS are not listed.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. You can modify the maximum number by adding the property `sn.occ.log_ingestion.max_datainputs_per_mid` to the MID Server and then changing the default value.
-   If log ingestion is not enabled for the selected MID Server, Health Log Analytics enables it automatically.

</td></tr><tr><td>

MID Server Cluster

</td><td>

\(Only when **Execute on** is set to Specific MID Server cluster.\)

The MID Server cluster to which the log data is pulled. This field is required.The data input runs on a single MID Server in the cluster until that MID Server fails. The system then moves all the data input tasks to the next available MID Server in the cluster according to the configured order.

**Note:**

-   Health Log Analytics supports only failover MID Server clusters. In these clusters, multiple MID Servers are grouped together for failover protection. When selecting a cluster from the data input or integration form, the MID Server clusters list displays only failover clusters.
-   The MID Server cluster must include only MID Servers that support basic authentication. mTLS is not supported for log ingestion.
-   Log ingestion must be enabled for each MID Server in the cluster. If log ingestion is not enabled for the active MID Server, Health Log Analytics enables it automatically.
-   The default maximum number of data inputs or integrations streaming logs to a single MID Server is 10. A cluster passes capacity validation if it contains at least one MID Server with fewer than 10 data inputs or integrations running on it, even when that MID Server is down.

For more information about MID Server clusters, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Service instance

</td><td>

The service instance \(formerly the application service\) to which to bind the log data. This field is required.

</td></tr><tr><td>

Data source

</td><td>

The source of the log data that the integration pulls to your ServiceNow instance: Kafka. This field is read-only.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the integration to help identify it.

</td></tr></tbody>
</table><table id="table_x11_2x5_l2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Kafka node names

</td><td>

A comma-separated list in the format HOST:PORT,HOST:PORT. This field is required.The list does not have to include all the Apache Kafka Cluster servers.

</td></tr><tr><td>

Topics

</td><td>

A comma-separated list of topics to which the data input must subscribe. This field is required.

</td></tr><tr><td>

Kafka credentials

</td><td>

The Apache Kafka credentials.You can select existing Kafka SSL credentials, or create new ones by selecting **Create Kafka credentials** from the drop-down list. For a description of the fields on the Kafka SSL credentials form, see [Kafka SSL credentials fields](hla-data-input-kafka-credentials.md).

</td></tr><tr><td>

Group ID

</td><td>

The name of the Apache Kafka Consumer Group.

</td></tr></tbody>
</table><table id="table_h5d_fx5_l2c"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

Timeout

</td><td>

The time, in milliseconds, spent waiting in the poll if data is not available in the topics.

</td><td>

500

</td></tr><tr><td>

Default timezone

</td><td>

The time zone of events that the system will use if a log does not specify the time zone.By default, the system uses GMT in such cases, but you can specify a different time zone.

</td><td>

GMT

</td></tr><tr><td>

Sub sample receive ratio

</td><td>

The number of events to batch together, out of which all but one will be discarded. This setting is used to decrease the number of received events.

</td><td>

-1

</td></tr><tr><td>

Character encoding

</td><td>

The character encoding for this data input. This field is read-only.

</td><td>

UTF-8

</td></tr><tr><td>

Node discovery timeout

</td><td>

The time, in milliseconds, before node discovery times out.

</td><td>

30

</td></tr><tr><td>

Sub sample drop ratio

</td><td>

The number of events to batch together, out of which one will be discarded. This setting is used to reduce the number of fetched events.

</td><td>

-1

</td></tr><tr><td>

Max length in bytes

</td><td>

The maximum length, in bytes, of events.

</td><td>

32766

</td></tr><tr><td>

Drop if queue is full

</td><td>

Option to discard logs if there is a load on the MID Server.

</td><td>

False

</td></tr></tbody>
</table>**Parent Topic:**[Integration configuration fields](../concept/hla-connector-config-fields.md)

