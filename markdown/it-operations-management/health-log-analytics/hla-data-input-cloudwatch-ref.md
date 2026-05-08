---
title: Amazon CloudWatch data input configuration fields
description: Description of the fields on the Amazon CloudWatch data input configuration form.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Data input configuration fields, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Amazon CloudWatch data input configuration fields

Description of the fields on the Amazon CloudWatch data input configuration form.

## Basic configuration

<table id="table_myk_sqb_x4b"><thead><tr><th>

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

 MID Server to which log data from Amazon CloudWatch is pulled. **Note:**

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

<table id="table_wf3_5xs_y4b"><thead><tr><th>

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

Protocol used to stream the log data.This data input uses Amazon CloudWatch to stream log data to your instance.

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
</table><table id="table_l5g_bct_y4b"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

From

</td><td>

The date and time to start reading the data. Data older than this date and time is not read.**Note:** Setting this value to a past date might require the system to read large amounts of data, causing congestion.

 This field is required.

</td><td>

Now -1 week

</td></tr><tr><td>

Group Name\(s\)

</td><td>

The log groups to search. If multiple log groups must be searched, specify the groups in a comma-separated list. To fetch log data from all groups, use an asterisk \(\*\) as a wildcard character.This field is required.

</td><td>

hla-cw-loggroup1,hla-cw-loggroup2

</td></tr><tr><td>

Prefix

</td><td>

Name prefix for the Amazon CloudWatch log streams to read from. The data input reads only from log streams with this name prefix.**Note:** Only a single log stream prefix per data item is supported. For multiple prefixes, create multiple data inputs.

</td><td>

hla-cw

</td></tr><tr><td>

Filter pattern

</td><td>

Pattern by which to filter incoming events. Various types of filter patterns are supported. For example:

-   A pattern for fetching log events that contain a single term.
-   A pattern for fetching log events that contain multiple terms.
-   A pattern for fetching log events that include a term and exclude another.

 **Note:** Filter patterns are case sensitive.

For more information, see [https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/FilterAndPatternSyntax.html](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/FilterAndPatternSyntax.html)

</td><td>

-   Pattern for fetching log events that contain a single term, "STATUS\_CODE":

"STATUS\_CODE"

-   Pattern for fetching log events that contain multiple terms, “STATUS\_CODE” and “200”:

“STATUS\_CODE 200”

-   Pattern for fetching log events that include a term, “STATUS\_CODE,” and exclude another term, “200”:

“STATUS\_CODE” – “200”


</td></tr></tbody>
</table><table id="table_izc_ydt_y4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AWS credentials

</td><td>

Field that refers to the AWS Credentials list \(aws\_credentials.list\). The list contains the AWS access and secret access keys.

</td></tr><tr><td>

AWS region

</td><td>

The AWS region where the Amazon CloudWatch cluster runs, for example, us-west-1. For a list of AWS regions, see [https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html\#concepts-regions](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html#concepts-regions)

 This field is required.

</td></tr></tbody>
</table>## Advanced configuration

|Field|Description|Default value|
|-----|-----------|-------------|
|Connection timeout|The number of milliseconds to wait before timing out the AWS connection attempt.|1000|
|Batch size|The maximum number of logs retrieved per query.|2500|
|Socket timeout|The number of milliseconds to wait before timing out a data transfer over an established connection.|10000|
|Default timezone|The default timezone if the log date and time doesn't include timezone information.|GMT|
|Sub sample drop ratio|The number of logs to batch together, out of which one will be discarded. This setting is used to reduce the number of fetched logs.|-1|
|Sub sample receive ratio|The number of logs to batch together, out of which all but one will be discarded. This setting is used to decrease the number of received logs.|-1|
|Max length in bytes|The maximum length of log messages, in bytes.|32766|
|Sleep interval|The interval, in seconds, to wait before querying again after a query has returned no logs.|60|
|Polling interval|The interval, in seconds, to wait before polling for new logs.|0|
|Drop if queue is full|Option to discard logs if there is a load on the MID Server.|False|

**Parent Topic:**[Data input configuration fields](../concept/hla-data-input-config-fields.md)

