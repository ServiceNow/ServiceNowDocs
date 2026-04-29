---
title: Microsoft Azure Log Analytics integration configuration fields
description: Description of the fields on the Microsoft Azure Log Analytics integration configuration forms for Health Log Analytics.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Azure Log Analytics, data input, integration, configuration, field, description, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Integration configuration fields, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Microsoft Azure Log Analytics integration configuration fields

Description of the fields on the Microsoft Azure Log Analytics integration configuration forms for Health Log Analytics.

For the Microsoft Azure Log Analytics integration setup procedure, see [Set up a Microsoft Azure Log Analytics integration for Health Log Analytics](../task/il-connector-hla-azure-la.md).

<table id="table_pxx_hz1_42c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Name

</td><td>

Unique name of this integration. For example: My Azure Log Analytics integration. This field is required.**Note:** When you fill in this field, the generic name displayed on the form adjusts automatically to match the name you entered.

</td></tr><tr><td>

Execute on

</td><td>

Option to select whether to use a specific MID Server or a MID Server cluster. This field is required.

</td></tr><tr><td>

MID server name

</td><td>

\(Only when the **Execute on** field is set to Specific MID Server\)

 MID Server to which log data from Microsoft Azure Log Analytics is pulled. This field is required.**Note:**

-   You can select only MID Servers that support basic authentication. MID Servers that support mTLS are not listed.
-   The default maximum number of integrations streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.
-   If log ingestion is not enabled for the selected MID Server, Health Log Analytics enables it automatically.

</td></tr><tr><td>

MID MID Server Cluster

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

The source of the log data that the integration pulls to your ServiceNow instance: Azure Log Analytics. This field is read-only.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the integration to help identify it.

</td></tr></tbody>
</table><table id="table_gpq_jz1_42c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Redirect url

</td><td>

The redirect URL of the access log application. This field is required. The URL refers to the Microsoft Azure redirect\_uri authorization property. For more information, see the Authorization code URL \(GET request\) section in the [Microsoft Azure documentation](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/api/access-api).

</td></tr><tr><td>

Authentication method

</td><td>

The credentials used to access Microsoft Azure resources. This field is required.If no credentials exist, select **Create new Azure Service Principal credential**. Create a credential by filling in the fields and then selecting **Submit**. For information on the **Tenant ID**, **Client ID**, and **Secret key** fields, refer to the [Microsoft Azure documentation](https://learn.microsoft.com/en-us/azure/?product=popular). When you have created a credential, you can select it from the drop-down list.

</td></tr><tr><td>

Workspace ID

</td><td>

The Customer ID used to call the Microsoft Azure Log Analytics REST API. This field is required.

</td></tr><tr><td>

Table name

</td><td>

The name of the table in Microsoft Azure Log Analytics where the data input fetches the log data. For more information, see the View table information section in the [Microsoft Azure documentation](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/log-analytics-tutorial). This field is required.

</td></tr><tr><td>

Event time property name

</td><td>

The Microsoft Azure Log Analytics field in which to detect the event time. This field is required.

</td></tr></tbody>
</table><table id="table_cyy_kz1_42c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event Processor workers

</td><td>

The number of concurrent event processing workers, where each worker processes a batch of events independently.

</td></tr><tr><td>

Workers queue size

</td><td>

The queue size of the Event Processor workers.

</td></tr><tr><td>

Sub sample drop ratio

</td><td>

The number of events to batch together, out of which one will be discarded. This setting is used to reduce the number of fetched events.

</td></tr><tr><td>

Sub sample receive ratio

</td><td>

The number of events to batch together, out of which all but one will be discarded. This setting is used to decrease the number of received events.

</td></tr><tr><td>

Max documents per query

</td><td>

The highest number of rows retrieved in each query.

</td></tr><tr><td>

Columns to select

</td><td>

Comma-separated list of column names to return.**Note:** This field is ignored when you provide a custom query.

</td></tr><tr><td>

Character encoding

</td><td>

The character encoding for this data input.

</td></tr><tr><td>

Sleep interval \(seconds\)

</td><td>

The interval, in seconds, to wait before querying again after a query has returned no events.

</td></tr><tr><td>

Polling interval

</td><td>

The interval, in seconds, to wait before polling for new events.

</td></tr><tr><td>

Drop if queue is full

</td><td>

Option to discard logs if there is a load on the MID Server.

</td></tr><tr><td>

Log Query

</td><td>

Option to define your own Log Analytics query. This field overrides the values configured in the other query settings fields.**Note:** If this field is empty, Health Log Analytics generates the query using the values set in the other fields.

For your custom query, use the following JSON format:

`{"query": "query | where TimeGenerated > %s | take 500"}`

For example:

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
</table>**Parent Topic:**[Integration configuration fields](../concept/hla-connector-config-fields.md)

