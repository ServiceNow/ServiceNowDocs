---
title: Splunk Polling data input configuration fields
description: Description of the fields on the Splunk Polling data input configuration form.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Data input configuration fields, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Splunk Polling data input configuration fields

Description of the fields on the Splunk Polling data input configuration form.

## Basic configuration

<table id="table_lgv_scp_mdc"><thead><tr><th>

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

\(Only when the **Execute on** field is set to Specific MID Server.\)The MID Server to which the logs are streamed.

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

For more information about MID Server clusters, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data. This field is required.**Note:** If no relevant service instance exists, [create a service instance](https://www.servicenow.com/docs/access?context=create-it-services&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and add CIs to it. Set the status of the new service instance to Operational.

</td></tr><tr><td>

Transport

</td><td>

The protocol used for streaming log messages to your ServiceNow instance.

</td></tr><tr><td>

Sources count

</td><td>

The number of log sources this data input has created.

</td></tr><tr><td>

Status

</td><td>

Status of the data input.

</td></tr><tr><td>

Disabled since

</td><td>

The time when the data input stopped or failed.

</td></tr><tr><td>

Last log time

</td><td>

The time when the last log streamed in the data input.

</td></tr></tbody>
</table>## Advanced configuration

<table id="table_bxk_thp_mdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Server URL

</td><td>

The URL used to access the Splunk REST API.

</td></tr><tr><td>

Query

</td><td>

The query Splunk uses to search your data.

</td></tr><tr><td>

Authentication Type

</td><td>

The authentication type.-   Basic authentication: Sends a username and password with each HTTP request. Basic authentication is simpler than token-based authentication, but less secure.
-   Token authentication: The client obtains a token from an authentication server and uses that token to authenticate against Splunk.

</td></tr><tr><td>

Splunk Poll Credential Alias

</td><td>

The credential alias to be used. Specify a Splunk Poll credential alias by selecting the magnifying glass icon and then either selecting an existing credential alias from the **Connection &amp; Credential Aliases** list, or selecting **New** to create a new record. The selected credential alias can hold one Basic Auth credential and one Token Auth credential.

For information about creating a credential alias, see [Credential aliases for Discovery](https://www.servicenow.com/docs/access?context=discovery-credential-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

From

</td><td>

The date and time from which Splunk searches the data.

</td></tr><tr><td>

To

</td><td>

The date and time until which Splunk searches the data.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Max documents per query|The maximum number of documents retrieved each time log data is fetched from Splunk. Default: 10,000.|
|Splunk request timeout \(seconds\)|The maximum time, in seconds, allowed for data retrieval before the request times out.|

**Parent Topic:**[Data input configuration fields](../concept/hla-data-input-config-fields.md)

