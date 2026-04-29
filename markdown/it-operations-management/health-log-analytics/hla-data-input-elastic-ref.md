---
title: Elasticsearch data input configuration fields
description: Description of the fields on the Elasticsearch data input configuration form.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Data input configuration fields, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Elasticsearch data input configuration fields

Description of the fields on the Elasticsearch data input configuration form.

## Basic configuration

<table id="table_s33_1lb_smb"><thead><tr><th>

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

Option to determine whether to use a specific MID Server or a MID Server cluster.This feature is supported in the Health Log Analytics application, Version 26.0.17 - February 2023 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td></tr><tr><td>

MID

</td><td>

\(Only when the **Execute on** field is set to Specific MID Server\)

 MID Server to which log data from Elasticsearch indices is pulled. **Note:**

-   You can select only MID Servers that support basic authentication. MID Servers that support mTLS are not listed.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.
-   If log ingestion is not enabled for the selected MID Server, Health Log Analytics enables it automatically.

This field is required.

</td></tr><tr><td>

MID Server Cluster

</td><td>

\(Only when the **Execute on** field is set to Specific MID Server Cluster\)

The MID Server cluster to which the log data is pulled.The data input runs on a single MID Server in the cluster until that MID Server fails. The system then moves all the data input tasks to the next available MID Server in the cluster according to the configured order.

 This feature is supported in the Health Log Analytics application, Version 26.0.17 - February 2023 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

 **Note:**

-   Health Log Analytics supports only failover MID Server clusters. In these clusters, multiple MID Servers are grouped together for failover protection. When selecting a cluster from the data input form, the MID Server Clusters list displays only failover clusters.
-   The MID Server cluster must include only MID Servers that support basic authentication. mTLS is not supported for log ingestion.
-   Log ingestion must be enabled for each MID Server in the cluster. If log ingestion is not enabled for the active MID Server, Health Log Analytics enables it automatically.
-   If Elasticsearch uses client certificate or CA certificate authentication, all MID Servers in the cluster must have the appropriate certificates.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. A cluster passes capacity validation if it contains at least one MID Server with fewer than 10 data inputs running on it, even when that MID Server is down.

For more information about MID Server clusters, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).This field is required.

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data. This field is required.**Note:** If no relevant service instance exists, [Create an service instance](https://www.servicenow.com/docs/access?context=create-it-services&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and add CIs to it. Set the status of the new service instance to Operational.

</td></tr></tbody>
</table>The following fields show read-only information:

<table id="table_zl5_1m1_pvb"><thead><tr><th>

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

Protocol used to stream the log data.This data input uses Elastic to stream log data to your instance.

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

</td></tr></tbody>
</table><table id="table_ljh_vtl_fnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Server URL

</td><td>

URL used to access the cluster. This field is required.

</td></tr><tr><td>

Max connections per route

</td><td>

Maximum number of connections to be opened per node. Default: 2.

</td></tr><tr><td>

Max scroll slices

</td><td>

The number of shards configured for the relevant index in Elasticsearch.This number tells Elastic how many parallel queries to execute in each polling request.

</td></tr><tr><td>

Proxy host

</td><td>

Host name of the HTTP proxy through which requests are sent.

</td></tr><tr><td>

Proxy port

</td><td>

Port of the HTTP proxy through which requests are sent.

</td></tr><tr><td>

Authentication method

</td><td>

The authentication method used to authenticate the data input to Elasticsearch. The options are: Basic auth, apiKey, or client certificate.**Note:** When you select the required authentication method, the corresponding credentials fields display on the form.

</td></tr><tr><td>

Basic auth credentials

</td><td>

User name and password used to connect to the Elasticsearch search engine.**Note:** Fill in either this field or the **AWS credentials** field.

</td></tr><tr><td>

AWS credentials

</td><td>

AWS credentials to use to connect to the AWS-hosted Elasticsearch search engine.**Note:** Fill in either this field or the **Basic auth credentials** field.

</td></tr><tr><td>

AWS region

</td><td>

AWS region where the Elasticsearch cluster runs.

</td></tr><tr><td>

API key credentials

</td><td>

The API key used to connect to the Elasticsearch search engine.

</td></tr><tr><td>

Client certificate

</td><td>

The client certificate used to connect to the Elasticsearch search engine.

</td></tr><tr><td>

Use MID certificate policy check

</td><td>

Option to enable the MID certificate policy check.Select this option if you want to ship your logs encrypted using SSL TLS. Then navigate to **All** &gt; **MID Server** &gt; **MID Security Policy** and add the MID certificate policy check to the table. For more information, see [MID Server certificate check policies](https://www.servicenow.com/docs/access?context=mid-security-checks&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table><table id="table_v4m_vmb_smb"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

From/To

</td><td>

From and to dates and time for reading the data.-   From: Don't read data older than this date.

**Note:** Setting this value to a past date might require the system to read large amounts of data, causing congestion.

-   To: Don't read data newer than this date. For live data, set this date far into the future.

</td><td>

From: 1970-01-01 15:59:59To: 2300-01-01 15:59:59

</td></tr><tr><td>

Use cross-cluster search

</td><td>

Option to search for data across Elasticsearch clusters.When this check box is selected, the **Clusters to search** field displays.

**Note:** Your settings in the **Use minimal privileges** check box and the **Delay in reading current timestamp \(seconds\)** field on the **Advanced configuration** form affect how data is collected across multiple clusters.

</td><td>

 

</td></tr><tr><td>

Clusters to search

</td><td>

The Elasticsearch clusters to search.This field displays only when the **Use cross-cluster search** check box is selected.

Do one of the following:

-   Leave this field empty or enter “\*” to search all the remote clusters defined in Elasticsearch.
-   Specify the clusters to search in a comma-separated list.

**Note:** To also search the local cluster, add a comma at the beginning or end, or add two commas in succession to the list. For example: “east,,west” or “,east,west” or “\*,”


</td><td>

east,west,south

</td></tr><tr><td>

Index prefix

</td><td>

Prefix for the Elasticsearch indices to read from. The data input reads only from indices with this prefix. This field is required.

</td><td>

only-read-these-indices-\*

</td></tr><tr><td>

Use minimal privileges

</td><td>

Option to read log data directly from the Elasticsearch indices with the configured prefix.-   When selected, the data input reads the log data directly from the Elasticsearch indices with the configured prefix. To perform this task, it needs only read privileges.

**Note:** When this check box is selected and you're using cross-cluster search, data is collected from all the clusters simultaneously.

-   When clear, the data input fetches all indices with the prefix, filters them, and reads the log data from the filtered indices. Performing this task requires additional privileges.

**Note:** Leaving this check box clear when using cross-cluster search affects how data is collected from the clusters. For more information, see the [Enabling and Using Cross-Cluster Search for Elasticsearch Data Inputs in Health Log Analytics \[KB1556079\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1556079) article in the Now Support Knowledge Base.


For additional information about streaming logs using the Elasticsearch data input, see the [Stream logs using Elasticsearch data input - Advanced guide \[KB1080162\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1080162) article in the Now Support Knowledge Base.

</td><td>

 

</td></tr><tr><td>

Document timestamp field

</td><td>

Timestamp field in documents stored in the read indices. This field is required.

</td><td>

 

</td></tr><tr><td>

Timestamp field format

</td><td>

Format of the timestamp field in the documents.If no format is specified, the default Unix epoch time format is used, in milliseconds. For example:

1684168407 \(May 15, 2023 4:33:27 PM\)

</td><td>

yyyy-MM-dd'T'HH:mm:ss.SSSSSSS'Z'

</td></tr><tr><td>

Term filters

</td><td>

JSON map of the terms to filter. **Note:** Avoid using the term query for text fields. If the target field is mapped as both text and keyword, reference the keyword by using fieldname.keyword.

</td><td>

\{"severity": \["error", "warning"\]\}

</td></tr><tr><td>

Max documents per query

</td><td>

Maximum number of documents fetched in a single query.

</td><td>

 

</td></tr><tr><td>

Sliced-scrolling tiebreaker

</td><td>

Value used to slice the data. Each slice is scrolled in parallel. Default: \_id

</td><td>

 

</td></tr><tr><td>

Search-after tiebreaker

</td><td>

Unique value per document to use as tiebreaker when sorting log entries by timestamp.

</td><td>

 

</td></tr><tr><td>

Use search-after API

</td><td>

Option to toggle between using sliced-scrolling and search-after APIs. **Note:** Sliced-scrolling APIs are preferable when reading historical data, while search-after APIs are better for reading real-time data.

</td><td>

 

</td></tr><tr><td>

Index time-suffix format

</td><td>

Format of the time suffix when using time-based index names, such as \[logstash-\]YYYY.MM.DD. When using aliases, leave this field empty.

</td><td>

uuuu.MM.dd

</td></tr></tbody>
</table>## Advanced configuration

<table id="table_sqw_tg4_gnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data reading timeout \(milliseconds\)

</td><td>

The duration of time, in milliseconds, before a request to the Elasticsearch cluster times out.

</td></tr><tr><td>

Index discovery interval \(seconds\)

</td><td>

The number of seconds between intermittent MID Server requests to the Elasticsearch cluster for new indices from which to read data.

</td></tr><tr><td>

Scroll context time \(milliseconds\)

</td><td>

The lifetime of the created scroll when using the scroll API to read data from Elasticsearch. For more information, see the Elasticsearch [scroll API documentation](https://www.elastic.co/guide/en/elasticsearch/reference/7.x/scroll-api.html#scroll-api-query-params).

</td></tr><tr><td>

Event processor workers

</td><td>

The maximum number of CPU cores used in parallel to process events fetched from Elasticsearch. A higher setting increases the data input throughput at the cost of higher CPU usage.

</td></tr><tr><td>

Worker queue size

</td><td>

The maximum number of batches to queue for processing. A higher setting increases throughput, at the cost of higher RAM usage.

</td></tr><tr><td>

Default timezone

</td><td>

The default timezone if the event date and time doesn't include timezone information.

</td></tr><tr><td>

Sub sample drop ratio

</td><td>

The number of events to batch together, out of which one will be discarded. This setting is used to reduce the number of fetched events.

</td></tr><tr><td>

Sub sample receive ratio

</td><td>

The number of events to batch together, out of which all but one will be discarded. This setting is used to decrease the number of received events.

</td></tr><tr><td>

Character encoding

</td><td>

The character encoding for this data input.

</td></tr><tr><td>

Sleep interval \(seconds\)

</td><td>

The interval, in seconds, to wait before querying again after a query has returned no data.

</td></tr><tr><td>

Max length in bytes

</td><td>

The maximum length, in bytes, of log messages.

</td></tr><tr><td>

Delay in reading current timestamp \(seconds\)

</td><td>

The number of seconds before current time to query to include delayed data.The configured number of seconds is subtracted from the current time for reading the last timestamp.

**Note:** If this value is 0 and data is collected from multiple clusters simultaneously, the query may not include data that was sent with a delay on one of the clusters,

</td></tr></tbody>
</table>**Parent Topic:**[Data input configuration fields](../concept/hla-data-input-config-fields.md)

