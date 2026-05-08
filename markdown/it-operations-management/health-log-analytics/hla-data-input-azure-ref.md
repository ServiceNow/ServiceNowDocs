---
title: Microsoft Azure Log Analytics data input configuration fields
description: Description of the fields on the Microsoft Azure Log Analytics data input configuration form.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Data input configuration fields, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Microsoft Azure Log Analytics data input configuration fields

Description of the fields on the Microsoft Azure Log Analytics data input configuration form.

## Basic configuration

<table id="table_w1c_xbc_x4b"><thead><tr><th>

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

 MID Server to which log data from Microsoft Azure Log Analytics is pulled. **Note:**

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

For more information about MID Server clusters, see Configure a MID Server cluster.

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data.**Note:** If no relevant service instance exists, Create an service instance and add CIs to it. Set the status of the new service instance to Operational.

This field is required.

</td></tr></tbody>
</table>The following fields show read-only information:

<table id="table_xfr_rwz_y4b"><thead><tr><th>

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

Protocol used to stream the log data.This data input uses Microsoft Azure Log Analytics to stream log data to your instance.

</td></tr><tr><td>

Disabled since

</td><td>

The time when the data input stopped or failed.

</td></tr><tr><td>

Sources count

</td><td>

The number of log sources this data input has created.

</td></tr><tr><td>

Last log time

</td><td>

The time when the last log streamed in the data input.

</td></tr><tr><td>

Error message

</td><td>

The streaming error.This field is populated automatically. It displays only when a streaming error has occurred.

</td></tr></tbody>
</table><table id="table_agb_3xz_y4b"><thead><tr><th>

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

</td></tr><tr><td>

Data source name

</td><td>

The name of the table in Microsoft Azure Log Analytics where the data input fetches the log data. For more information, see the View table information section in the [Microsoft Azure documentation](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/log-analytics-tutorial). This field is required.

</td><td>

ContainerLog

</td></tr><tr><td>

Event time property name

</td><td>

The Microsoft Azure Log Analytics field in which to detect the event time. This field is required.

</td><td>

TimeGenerated

</td></tr><tr><td>

Max documents per query

</td><td>

The highest number of rows retrieved in each query.

</td><td>

500

</td></tr><tr><td>

Columns to select

</td><td>

Comma-separated list of column names to return.**Note:** This field is ignored when you provide a custom query.

</td><td>

LogEntry,LogEntrySource

</td></tr><tr><td>

Log query

</td><td>

A custom query for receiving log data from Microsoft Azure Log Analytics.The settings in this field override those in all other fields on the **Query settings** tab except the **From** field. If the **Log query** field is empty, Health Log Analytics generates the query using the values set in the other fields.

For the custom query, use the following JSON format:

`{"query": "query | where TimeGenerated > %s | take 500"}`

</td><td>

```
{
"query":"ContainerLog
                    | where LogEntry contains 'cartservice'
                    | where TimeGenerated > %s
                    | take 500",
"workspaces": ["defaultworkspace-3ab145ff-f9cd-433f-8533-d1b1ee24aee6-eus"],
"project": ["TimeGenerated", "LogEntry", "LogEntrySource"]
}
```

</td></tr></tbody>
</table><table id="table_rrh_5xz_y4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Redirect Url

</td><td>

The redirect URL of the access log application. The URL refers to the Microsoft Azure redirect\_uri authorization property. For more information, see the Authorization code URL \(GET request\) section in the [Microsoft Azure documentation](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/api/access-api).

This field is required.

</td></tr><tr><td>

Azure service principal credentials

</td><td>

The credentials used to access Microsoft Azure resources.Choose **Client Secret** from the drop-down list.

 **Note:** You do not need Azure Enterprise Agreement \(EA\) credentials.

 This field is required.

</td></tr><tr><td>

Workspace Id

</td><td>

The Customer ID used to call the Microsoft Azure Log Analytics REST API.

</td></tr></tbody>
</table>## Advanced configuration

|Field|Description|Default value|
|-----|-----------|-------------|
|Event Processor workers|The number of concurrent event processing workers, where each worker processes a batch of events independently.|4|
|Workers Queue Size|The queue size of the Event Processor workers.|5|
|Sub sample drop ratio|The number of events to batch together, out of which one will be discarded. This setting is used to reduce the number of fetched events.|-1|
|Sub sample receive ratio|The number of events to batch together, out of which all but one will be discarded. This setting is used to decrease the number of received events.|-1|
|Character encoding|The character encoding for this data input.|UTF-8|
|Sleep interval|The interval, in seconds, to wait before querying again after a query has returned no events.|60|
|Polling interval|The interval, in seconds, to wait before polling for new events.|0|
|Drop if queue is full|Option to discard logs if there is a load on the MID Server.|False|

**Parent Topic:**[Data input configuration fields](../concept/hla-data-input-config-fields.md)

