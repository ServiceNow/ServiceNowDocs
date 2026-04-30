---
title: Microsoft Azure Event Hubs integration configuration fields
description: Description of the fields on the Microsoft Azure Event Hubs integration configuration forms for Health Log Analytics.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Azure Event Hubs, data input, integration, configuration, field, description, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Integration configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Microsoft Azure Event Hubs integration configuration fields

Description of the fields on the Microsoft Azure Event Hubs integration configuration forms for Health Log Analytics.

For the Microsoft Azure Event Hubs integration setup procedure, see [Set up a Microsoft Azure Event Hubs integration for Health Log Analytics](../task/il-connector-hla-event-hubs.md).

<table id="table_t11_vvw_jfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Name

</td><td>

Unique name of this integration. For example: My Event Hubs integration. This field is required.**Note:** When you fill in this field, the generic name displayed on the form adjusts automatically to match the name you entered.

</td></tr><tr><td>

Service Instance

</td><td>

The service instance \(formerly the application service\) to which to bind the log data. This field is required.

</td></tr><tr><td>

Source

</td><td>

The source of the log data that the integration pulls to your ServiceNow instance: PubSub. This field is read-only.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the integration to help identify it.

</td></tr><tr><td>

Execute on

</td><td>

Option to select whether to use a specific MID Server or a MID Server cluster. This field is required.

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

\(Only when **Execute on** is set to Specific MID Server cluster.\)

The MID Server cluster to which the log data is pulled. This field is required.The data input runs on a single MID Server in the cluster until that MID Server fails. The system then moves all the data input tasks to the next available MID Server in the cluster according to the configured order.

**Note:**

-   Health Log Analytics supports only failover MID Server clusters. In these clusters, multiple MID Servers are grouped together for failover protection. When selecting a cluster from the data input or integration form, the MID Server clusters list displays only failover clusters.
-   The MID Server cluster must include only MID Servers that support basic authentication. mTLS is not supported for log ingestion.
-   Log ingestion must be enabled for each MID Server in the cluster. If log ingestion is not enabled for the active MID Server, Health Log Analytics enables it automatically.
-   The default maximum number of data inputs or integrations streaming logs to a single MID Server is 10. A cluster passes capacity validation if it contains at least one MID Server with fewer than 10 data inputs or integrations running on it, even when that MID Server is down.

For more information about MID Server clusters, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table><table id="table_dy2_g5t_ngc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Event Hubs namespace

</td><td>

The scoping container for the event hub or hubs. This field is required.

</td></tr><tr><td>

Event Hub name

</td><td>

The event hub from which to fetch log data. This field is required.

</td></tr><tr><td>

Consumer Group name

</td><td>

The Consumer Group to use. This field is required.Enter an existing Consumer group or create one in the event hub. The default value is $Default.

</td></tr><tr><td>

Event Hub Credentials

</td><td>

The Event Hub credentials to use. This field is required.Select existing Azure Shared Access Signature \(SAS\) credentials or create the Azure SAS credentials to use. If you create new Azure SAS credentials, you must provide the SAS policy name and key.

</td></tr></tbody>
</table><table id="table_zgg_xvw_jfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Restore point rate

</td><td>

The number of logs the integration can read before a restore point is saved.

</td></tr><tr><td>

Processor threads count

</td><td>

The total number of processor threads.

</td></tr><tr><td>

Sub sample drop ratio

</td><td>

The ratio of logs to discard.This setting determines the number of logs to group together, out of which one is dropped. It reduces the number of fetched logs.

The default value is -1: no logs are discarded. For example, if you want one log out of every five to be dropped, change the value to 5.

</td></tr><tr><td>

Sub sample receive ratio

</td><td>

The ratio of logs to receive. This setting determines the number of logs to group together, out of which one is received. It reduces the number of logs you receive.

The default value is -1, meaning no logs are received. For example, if you want to receive one log out of every five, change the value to 5.

</td></tr><tr><td>

Operation timeout \(seconds\)

</td><td>

The number of seconds to wait before timing out event hubs operations.

</td></tr><tr><td>

Receive idle timeout \(seconds\)

</td><td>

The number of seconds to wait before timing out receive operations.

</td></tr><tr><td>

Max length in bytes

</td><td>

The maximum length, in bytes, of log messages. The default value is 32766.

</td></tr><tr><td>

Prefetch count

</td><td>

The number of logs received in advance of event hubs operations.

</td></tr><tr><td>

Max batch size

</td><td>

The maximum number of events passed to a single process call. The default value is 100.

</td></tr><tr><td>

Default timezone

</td><td>

The default time zone of logs. The system uses this default when the log does not specify a time zone. The default value is GMT.

</td></tr><tr><td>

Character encoding

</td><td>

The character encoding for this integration. The default value is UTF-8.

</td></tr><tr><td>

Drop if queue is full

</td><td>

Option to select discarding logs if there is a load on the MID Server.

</td></tr></tbody>
</table>**Parent Topic:**[Integration configuration field descriptions](../concept/hla-connector-config-fields.md)

