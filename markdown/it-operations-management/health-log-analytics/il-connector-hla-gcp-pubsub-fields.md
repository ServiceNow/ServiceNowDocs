---
title: GCP PubSub integration configuration fields
description: Description of the fields on the GCP PubSub integration configuration forms for Health Log Analytics.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-08-26"
reading_time_minutes: 4
keywords: [GCP PubSub, data input, integration, configuration, field, description, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Configure GCP PubSub integrations, Set up integrations from Integrations Launchpad, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# GCP PubSub integration configuration fields

Description of the fields on the GCP PubSub integration configuration forms for Health Log Analytics.

<table id="table_ptx_ylg_lgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Name

</td><td>

Unique name of this integration. For example: My GCP PubSub integration. This field is required.**Note:** When you fill in this field, the generic name displayed on the form adjusts automatically to match the name you entered.

</td></tr><tr><td>

Service Instance

</td><td>

The service instance \(formerly the application service\) to which to bind the log data. This field is required.

</td></tr><tr><td>

Execute on

</td><td>

Option to determine whether to use a specific MID Server or a MID Server cluster.This feature is supported in the Health Log Analytics application, Version 26.0.17 - February 2023 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td></tr><tr><td>

MID Server name

</td><td>

\(Only when **Execute on** is set to Specific MID Server.\)

The MID Server to which the logs are streamed. **Note:**

-   You can only select a MID Server with log ingestion capability that supports basic authentication. MID Servers that support mTLS are not listed.
-   If log ingestion is not enabled on the selected MID Server, Health Log Analytics enables it automatically.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.

This field is required.

</td></tr><tr><td>

MID Server cluster

</td><td>

\(Only when the **Execute on** field is set to Specific MID Server Cluster\)

The MID Server cluster to which the log data is pulled.The data input runs on a single MID Server in the cluster until that MID Server fails. The system then moves all the data input tasks to the next available MID Server in the cluster according to the configured order.

 This feature is supported in the Health Log Analytics application, Version 26.0.17 - February 2023 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

 **Note:**

-   Health Log Analytics supports only failover MID Server clusters. In these clusters, multiple MID Servers are grouped together for failover protection. When selecting a cluster from the data input form, the MID Server Clusters list displays only failover clusters.
-   The MID Server cluster must include only MID Servers that support basic authentication. mTLS is not supported for log ingestion.
-   Log ingestion must be enabled for each MID Server in the cluster. If log ingestion is not enabled for the active MID Server, Health Log Analytics enables it automatically.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. A cluster passes capacity validation if it contains at least one MID Server with fewer than 10 data inputs running on it, even when that MID Server is down.

For more information about MID Server clusters, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).This field is required.

</td></tr><tr><td>

Source

</td><td>

The source of the log data that the integration pulls to your ServiceNow instance: PubSub. This field is read-only.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the integration to help identify it.

</td></tr></tbody>
</table><table id="table_fxz_2mg_lgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Project ID

</td><td>

The project ID of the Google Cloud project. For example, my-project-id. This field is required.You can obtain the project ID from your Google Cloud homepage by selecting My Project. The project ID will be displayed.

</td></tr><tr><td>

Authentication method

</td><td>

The credential alias ServiceNow® uses to access Google Cloud. The default value is sn\_occ.HLA\_Credential\_Alias. This field is required**Note:** You can add more credential aliases to the list of available aliases to choose from by selecting **Manage credential aliases** from the list and adding a credential alias.

</td></tr><tr><td>

Topic name

</td><td>

The Google Cloud Pub/Sub topic to which to subscribe Health Log Analytics. For example, my\_topic. This field is required.You can obtain the topic name from your Google Cloud homepage by searching for Pub/Sub. All topic names will be displayed.

</td></tr><tr><td>

Subscription name

</td><td>

The subscription Health Log Analytics uses to receive log data that is published on the Google Cloud Pub/Sub topic.If you leave this field blank, Health Log Analytics uses ServiceNow-Subscription.

</td></tr></tbody>
</table><table id="table_j5p_f4g_lgc"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

Subscriber thread pool size

</td><td>

The number of concurrent threads that are downloading files from the Google Cloud Pub/Sub topic.

</td><td>

1

</td></tr><tr><td>

Sub sample receive ratio

</td><td>

The ratio of logs to receive. This setting determines the number of logs to group together, out of which one is received. It reduces the number of logs you receive.

The default value is -1, meaning no logs are received. For example, if you want to receive one log out of every five, change the value to 5.

</td><td>

-1

</td></tr><tr><td>

Max length in bytes

</td><td>

The maximum length of log messages, in bytes.

</td><td>

32,766

</td></tr><tr><td>

Character encoding

</td><td>

The character encoding for this data input. This field is read-only.

</td><td>

UTF-8

</td></tr><tr><td>

Sub sample drop ratio

</td><td>

The ratio of logs to discard.This setting determines the number of logs to group together, out of which one is dropped. It reduces the number of fetched logs.

The default value is -1: no logs are discarded. For example, if you want one log out of every five to be dropped, change the value to 5.

</td><td>

-1

</td></tr><tr><td>

Rate limit

</td><td>

The maximum number of events per second that this data input processes.

</td><td>

-1

</td></tr><tr><td>

Default timezone

</td><td>

The default time zone of events. The system uses this default when the log does not specify a time zone.

</td><td>

GMT

</td></tr><tr><td>

Drop if queue is full

</td><td>

Option for selecting to discard logs if many processes are waiting in the queue to access the MID Server.

</td><td>

Clear

</td></tr></tbody>
</table>**Parent Topic:**[Set up a GCP PubSub integration for Health Log Analytics](../task/il-connector-hla-gcp-pubsub.md)

