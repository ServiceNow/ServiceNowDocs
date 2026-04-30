---
title: Splunk Poller integration configuration fields
description: Description of the fields on the Splunk Poller integration configuration forms for Health Log Analytics.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Splunk Polling, data input, integration, configuration, field, description, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Integration configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Splunk Poller integration configuration fields

Description of the fields on the Splunk Poller integration configuration forms for Health Log Analytics.

For the Splunk Poller integration setup procedure, see [Set up a Splunk Poller integration for Health Log Analytics](../task/il-connector-hla-splunk-polling.md).

<table id="table_fhy_yq1_m2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Name

</td><td>

Unique name of this integration. This field is required.**Note:** When you fill in this field, the generic name displayed on the form adjusts automatically to match the name you entered.

</td></tr><tr><td>

Execute on

</td><td>

Option to select whether to use a specific MID Server or a MID Server cluster. This field is required.

</td></tr><tr><td>

MID server name

</td><td>

\(Only when the **Execute on** field is set to Specific MID Server\)

MID Server to which log data from Splunk is pulled. This field is required.**Note:**

-   You can select only MID Servers that support basic authentication. MID Servers that support mTLS are not listed.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.
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

For more information about MID Server clusters, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Service instance

</td><td>

The service instance \(formerly the application service\) to which to bind the log data. This field is required.

</td></tr><tr><td>

Data source

</td><td>

The source of the log data that the integration pulls to your ServiceNow instance: Splunk. This field is read-only.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the integration to help identify it.

</td></tr></tbody>
</table><table id="table_ns2_1r1_m2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

REST API Server URL

</td><td>

The URL used to access the Splunk REST API. This field is required.**Note:**

-   By default, the Splunk REST API endpoint is available on port 8089. Therefore, the default endpoint for the Splunk REST API is: `http://<splunk-server>:8089`.
-   The REST API endpoint is different from the front-end endpoint.

</td></tr><tr><td>

Authentication method

</td><td>

The credential alias to be used. This field is required.The Splunk integration uses credential aliases instead of direct references to credentials for authentication. The credential aliases are listed by type: aliases that contain basic auth credentials, and those that contain token auth credentials. If an alias holds both credential types, it appears in both categories.

You can select **Manage credential aliases** to manage your credential aliases and create new ones in the **Connection &amp; Credential Aliases** list.

</td></tr><tr><td>

Query

</td><td>

The query Splunk uses to search your data. This field is required.For example, the query `sourcetype="adc_access_log"` instructs the Splunk Poller integration to retrieve all logs with the source type adc\_access\_log.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Max documents per query|The maximum number of documents retrieved each time log data is fetched from Splunk. Default: 10,000.|
|Splunk Request Timeout \(seconds\)|The maximum time, in seconds, allowed for data retrieval before the request times out.|

**Parent Topic:**[Integration configuration field descriptions](../concept/hla-connector-config-fields.md)

