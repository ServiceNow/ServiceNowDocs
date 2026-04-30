---
title: GCP PubSub data input configuration fields
description: Description of the fields on the GCP PubSub data input configuration form.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Data input configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# GCP PubSub data input configuration fields

Description of the fields on the GCP PubSub data input configuration form.

## Basic configuration

<table id="table_c5d_gpc_lvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the new data input. This field is required.

</td></tr><tr><td>

Port

</td><td>

The port for the MID Server. Select a unique port from the array. The placeholder shows the range of ports from which to choose. Make sure that your organization’s security team opens the selected port.

This field is required.

</td></tr><tr><td>

Execute on

</td><td>

Option to select whether to use a specific MID Server or a MID Server cluster. This field is required.

</td></tr><tr><td>

MID

</td><td>

\(Only when the **Execute on** field is set to Specific MID Server\)

 The MID Server to which the logs are streamed. **Note:**

-   You can select only MID Servers with log ingestion capability that support basic authentication. MID Servers that support mTLS are not listed.
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

For more information about MID Server clusters, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data. This field is required.**Note:** If no relevant service instance exists, [Create an service instance](https://www.servicenow.com/docs/access?context=create-it-services&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) and add CIs to it. Set the status of the new service instance to Operational.

</td></tr></tbody>
</table>The fields in the following table show read-only information.

|Field|Description|
|-----|-----------|
|Transport|Protocol used to send the log data: PubSub.|
|Sources count|The number of log sources this data input has created.|
|Status|Status of the data input.|
|Disabled since|The time when the data input stopped or failed.|
|Last log time|The time when the last log streamed in the data input.|

<table id="table_irj_gqc_lvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Project ID

</td><td>

The project ID of the Google Cloud project. For example, my-project-id.

</td></tr><tr><td>

Topic Name

</td><td>

The Google Cloud Pub/Sub topic to which to subscribe Health Log Analytics. For example, my\_topic.

</td></tr><tr><td>

GCP Credential Alias

</td><td>

The credential alias to be used. Specify one GCP credential alias by selecting the magnifying glass icon and then either selecting an existing credential alias from the **Connection &amp; Credential Aliases** list, or selecting **New** to create a new record. The default is sn\_occ.HLA\_Credential\_Alias.

 For information about creating a credential alias, see [Credential aliases for Discovery](https://www.servicenow.com/docs/access?context=discovery-credential-alias&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Subscription Name

</td><td>

The subscription Health Log Analytics uses to receive log data that is published on the Google Cloud Pub/Sub topic.If you leave this field blank, Health Log Analytics uses ServiceNow-Subscription.

</td></tr></tbody>
</table>## Advanced configuration

|Field|Description|Default value|
|-----|-----------|-------------|
|Subscriber Thread Pool Size|The number of concurrent threads that are downloading files from the Google Cloud Pub/Sub topic.|1|
|Default timezone|The default time zone of events. The system uses this default when the log does not specify a time zone.|GMT|
|Max length in bytes|The maximum length of log messages, in bytes.|32,766|
|Character encoding|\(Read-only\) The character encoding for this data input.|UTF-8|
|Sub sample drop ratio|The ratio of events to drop.|-1|
|Sub sample receive ratio|The ratio of events to receive.|-1|
|Rate limit|The maximum number of events per second that this data input processes.|-1|
|Drop if queue is full|Option for selecting to discard logs if many processes are waiting in the queue to access the MID Server.|Clear|

**Parent Topic:**[Data input configuration field descriptions](../concept/hla-data-input-config-fields.md)

