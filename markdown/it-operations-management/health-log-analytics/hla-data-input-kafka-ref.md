---
title: Apache Kafka data input configuration fields
description: Description of the fields on the Apache Kafka data input configuration form.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Data input configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Apache Kafka data input configuration fields

Description of the fields on the Apache Kafka data input configuration form.

## Basic configuration

<table id="table_vny_z2c_x4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the new data input. This field is required.

</td></tr><tr><td>

Description

</td><td>

Description of the data input.

</td></tr><tr><td>

Execute on

</td><td>

Option to select whether to use a specific MID Server or a MID Server cluster. This field is required.

</td></tr><tr><td>

MID

</td><td>

\(Only when the **Execute on** field is set to Specific MID Server\)

 MID Server to which log data from Apache Kafka is pulled. **Note:**

-   You can select only MID Servers that support basic authentication. MID Servers that support mTLS are not listed.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.
-   If log ingestion is not enabled for the selected MID Server, Health Log Analytics enables it automatically.

This field is required.

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

For more information about MID Server clusters, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data. **Note:** If no relevant service instance exists, [Create an service instance](https://www.servicenow.com/docs/access?context=create-it-services&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) and add CIs to it. Set the status of the new service instance to Operational.

This field is required.

</td></tr></tbody>
</table>The following fields show read-only information:

<table id="table_hds_jcb_z4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status

</td><td>

Status of the data input.

</td></tr><tr><td>

Transport

</td><td>

Protocol used to stream the log data.This data input uses Apache Kafka to stream log data to your instance.

</td></tr><tr><td>

Sources count

</td><td>

The number of log sources this data input has created.

</td></tr><tr><td>

Disabled since

</td><td>

The time when the data input stopped or failed.

</td></tr><tr><td>

Last log time

</td><td>

The time when the last log streamed in the data input.

</td></tr><tr><td>

Error message

</td><td>

The streaming error.This field is populated automatically. It displays only when a streaming error has occurred.

</td></tr></tbody>
</table><table id="table_z51_vcb_z4b"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

From

</td><td>

Starting date and time for reading the data. Data older than this date and time is not read.**Note:** Setting this value to a past date might require the system to read large amounts of data, causing congestion.

 This field is required.

</td><td>

Now -1 week

</td></tr></tbody>
</table><table id="table_m1j_5g4_3pb"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Kafka node names

</td><td>

A comma-separated list in the format HOST:PORT,HOST:PORT. The list does not have to include all the Apache Kafka Cluster servers.

</td><td>

123.4.5.6:9092,123.3.4.5:9093

</td></tr><tr><td>

Topics

</td><td>

A comma-separated list of topics to which the data input must subscribe.This field is required.

</td><td>

FirstTopic,SecondTopic,ThirdTopic

</td></tr><tr><td>

Kafka credentials

</td><td>

Reference to the Apache Kafka credentials.You can display the Kafka SSL credentials form by selecting the Search icon \(![](../../../common/image/List_SearchIcon.png)\) and opening a record. The form enables you to choose the security protocol used for authenticating with Apache Kafka from the following options:

-   **SSL** - SSL channel.
-   **SASL\_SSL** - SASL authenticated, SSL channel.
-   **SASL\_PLAINTEXT** - SASL authenticated, non-encrypted channel.

For a description of the fields on the Kafka SSL credentials form, see [Kafka SSL credentials fields](hla-data-input-kafka-credentials.md).

</td><td>

None

</td></tr><tr><td>

Group Id

</td><td>

The name of the Apache Kafka Consumer Group.

</td><td>

logs

</td></tr></tbody>
</table>## Advanced configuration

|Field|Description|Default value|
|-----|-----------|-------------|
|Timeout|The time, in milliseconds, spent waiting in the poll if data is not available in the topics.|500|
|Node discovery timeout|The time, in milliseconds, before node discovery times out.|30|
|Default timezone|The default timezone if the log doesn't include timezone information.|GMT|
|Sub sample drop ratio|The number of events to batch together, out of which one will be discarded. This setting is used to reduce the number of fetched events.|-1|
|Sub sample receive ratio|The number of events to batch together, out of which all but one will be discarded. This setting is used to decrease the number of received events.|-1|
|Max length in bytes|The maximum length, in bytes, of events.|32766|
|Character encoding|The character encoding for this data input.|UTF-8|
|Drop if queue is full|Option for selecting to discard logs if there is a load on the MID Server.|False|

-   **[Kafka SSL credentials fields](hla-data-input-kafka-credentials.md)**  
Description of the fields on the Kafka SSL credentials form.

**Parent Topic:**[Data input configuration field descriptions](../concept/hla-data-input-config-fields.md)

