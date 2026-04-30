---
title: Amazon S3 data input configuration fields
description: Description of the fields on the Amazon S3 data input configuration form.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Data input configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Amazon S3 data input configuration fields

Description of the fields on the Amazon S3 data input configuration form.

## Basic configuration

<table id="table_rdw_xvb_x4b"><thead><tr><th>

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

 MID Server to which log data from Amazon S3 is pulled. **Note:**

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

For more information about MID Server clusters, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data. **Note:** If no relevant service instance exists, [Create an service instance](https://www.servicenow.com/docs/access?context=create-it-services&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) and add CIs to it. Set the status of the new service instance to Operational.

This field is required.

</td></tr></tbody>
</table>The following fields show read-only information:

<table id="table_x1v_nlt_y4b"><thead><tr><th>

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

Protocol used to stream the log data.This data input uses Amazon S3 to stream log data to your instance.

</td></tr><tr><td>

Sources count

</td><td>

The number of log sources this data input has created.

</td></tr><tr><td>

Disabled since

</td><td>

Time when the data input stopped or failed.

</td></tr><tr><td>

Last log time

</td><td>

Time when the last log streamed in the data input.

</td></tr><tr><td>

Error message

</td><td>

The streaming error.This field is populated automatically. It displays only when a streaming error has occurred.

</td></tr></tbody>
</table><table id="table_glh_4nt_y4b"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

From/To

</td><td>

Starting and ending dates and time for reading the data.-   From: Data older than this date and time is not read.

**Note:** Setting this value to a past date might require the system to read large amounts of data, causing congestion.

-   To: Data newer than this date and time is not read. For live data, set this date far into the future.

This field is required.

</td><td>

From: Now -1 weekTo: 2300-01-01 15:59:59

</td></tr><tr><td>

Bucket name

</td><td>

The Amazon S3 bucket to stream. This field is required.

</td><td>

my-s3-bucket

</td></tr><tr><td>

Prefix

</td><td>

Prefix for the objects to be fetched. The data input fetches only objects that begin with this prefix. This field is typically used to fetch only specific folders in a bucket.

</td><td>

/only/this/folder/

</td></tr><tr><td>

Include

</td><td>

File or object to include when the system performs pattern matching.

</td><td>

.\*include-me.\*

</td></tr><tr><td>

Exclude

</td><td>

File or object to exclude when the system performs pattern matching.

</td><td>

.\*skip-me.\*

</td></tr></tbody>
</table><table id="table_arg_1pt_y4b"><thead><tr><th>

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

The AWS region where the Amazon S3 bucket is located, for example, us-west-1. For a list of AWS regions, see [https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html\#concepts-regions](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html#concepts-regions)

 This field is required.

</td></tr></tbody>
</table>## Advanced configuration

|Field|Description|Default value|
|-----|-----------|-------------|
|Anonymous|Option to force accessing the Amazon S3 bucket without credentials, while ignoring default credentials if they exist.|False|
|Traverse|Option to access each directory in the bucket.|False|
|Object sorted by Last Modified Time|Option to fetch objects if the objects in the bucket are sorted by time.|False|
|Connection timeout|The number of milliseconds to wait before timing out the attempt to establish a connection to AWS.|100|
|Threadpool size|The number of concurrent threads that are downloading files from the bucket.|1|
|Buffer size|Size of the download buffer, in bytes.|100MB|
|Socket timeout|The number of milliseconds to wait before timing out data transfer over an established connection.|10000|
|Max retry for file|The maximum number of times to retry file processing in case of failure.|10|
|Default timezone|The default timezone if the log doesn't include timezone information.|UTC|
|Sub sample drop ratio|The number of events to batch together, out of which one will be discarded. This setting is used to reduce the number of fetched events.|-1|
|Sub sample receive ratio|The number of events to batch together, out of which all but one will be discarded. This setting is used to decrease the number of received events.|-1|
|Rate limit|The maximum number of events per second that this data input processes.|-1|
|Max length in bytes|The maximum length, in bytes, of events.|32766|
|Character encoding|The character encoding for this data input.|UTF-8|
|Sleep interval|The interval, in seconds, to wait before querying again after a query has returned no events.|60|
|Polling interval|The interval, in seconds, to wait before polling for new events.|0|
|Drop if queue is full|Option for selecting to discard logs if there is a load on the MID Server.|False|

**Parent Topic:**[Data input configuration field descriptions](../concept/hla-data-input-config-fields.md)

