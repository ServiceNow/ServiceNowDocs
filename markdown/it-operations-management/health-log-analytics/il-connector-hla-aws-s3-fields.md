---
title: Amazon S3 integration configuration fields
description: Description of the fields on the Amazon S3 integration configuration forms for Health Log Analytics.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Amazon S3, data input, integration, configuration, field, description, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Integration configuration fields, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Amazon S3 integration configuration fields

Description of the fields on the Amazon S3 integration configuration forms for Health Log Analytics.

For the Amazon S3 integration setup procedure, see [Set up an Amazon S3 integration for Health Log Analytics](../task/il-connector-hla-aws-s3.md).

<table id="table_ub4_l2h_shc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Name

</td><td>

Unique name of this integration. For example: My S3 integration. This field is required.**Note:** When you fill in this field, the generic name displayed on the form adjusts automatically to match the name you entered.

</td></tr><tr><td>

Service instance

</td><td>

The service instance \(formerly the application service\) to which to bind the log data. This field is required.

</td></tr><tr><td>

Execute on

</td><td>

Option to select whether to use a specific MID Server or a MID Server cluster. This field is required.

</td></tr><tr><td>

MID server name

</td><td>

\(Only when the **Execute on** field is set to Specific MID Server\)

The MID Server to which log data from Amazon S3 is pulled. This field is required.**Note:**

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

For more information about MID Server clusters, see Configure a MID Server cluster.

</td></tr><tr><td>

Data source

</td><td>

The source of the log data that the integration pulls to your ServiceNow instance: S3. This field is read-only.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the integration to help identify it.

</td></tr></tbody>
</table><table id="table_cgt_w2h_shc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Bucket name

</td><td>

The Amazon S3 bucket to stream. This field is required.

</td></tr><tr><td>

Region

</td><td>

The AWS region where the Amazon CloudWatch cluster is hosted. For example: us-east-2. This field is required.For a list of AWS regions, see [https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html\#concepts-regions](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html#concepts-regions)

</td></tr><tr><td>

Authentication method

</td><td>

The AWS credentials needed to access resources in AWS service accounts. This field is required.Choose AWS credentials from the drop-down list, or add new AWS credentials to the list by selecting **Manage Credentials** and then defining new credentials on the **AWS Credentials** page.

</td></tr></tbody>
</table><table id="table_dkd_1fh_shc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Include

</td><td>

The file or object to include when the system performs pattern matching.

</td></tr><tr><td>

Exclude

</td><td>

The file or object to exclude when the system performs pattern matching.

</td></tr><tr><td>

Bucket prefix

</td><td>

The prefix for the objects to be fetched. The integration fetches only objects with this prefix. **Note:** This field is typically used to fetch only specific folders within a bucket.

</td></tr><tr><td>

Buffer size

</td><td>

The size of the download buffer, in bytes.

</td></tr><tr><td>

Threadpool size

</td><td>

The number of concurrent threads that are downloading files from the bucket.

</td></tr><tr><td>

Anonymous

</td><td>

Option to force accessing the bucket without credentials, while ignoring default credentials if they exist.

</td></tr><tr><td>

Traverse

</td><td>

Option to access each directory in the bucket.

</td></tr><tr><td>

Sorting object by last modified time

</td><td>

Option to fetch objects if the objects in the bucket are sorted by time.

</td></tr><tr><td>

Sub sample drop ratio

</td><td>

The number of logs to batch together, out of which one will be dropped. The default value is -1: No logs are dropped.This setting is used to reduce the number of fetched logs. For example, if you want one log out of every five to be dropped, change the value to 5.

</td></tr><tr><td>

Sleep interval \(seconds\)

</td><td>

The interval, in seconds, to wait before querying again after a query has returned no events.

</td></tr><tr><td>

Max length in bytes

</td><td>

The maximum length, in bytes, of events.

</td></tr><tr><td>

Connection timeout \(ms\)

</td><td>

The number of milliseconds to wait before timing out the attempt to establish a connection to AWS.

</td></tr><tr><td>

Max retry per file

</td><td>

The maximum number of times to retry file processing in case of failure.

</td></tr><tr><td>

Socket timeout \(ms\)

</td><td>

The number of milliseconds to wait before timing out data transfer over an established connection.

</td></tr><tr><td>

Default timezone

</td><td>

The default timezone if the log doesn't include timezone information.

</td></tr><tr><td>

Sub sample receive ratio

</td><td>

The number of logs to batch together, out of which one log will be received and the remaining ones dropped. The default value is -1: No logs are received. This setting is used to reduce the number of received logs. For example, if you want to receive one log out of every five, change the value to 5.

</td></tr><tr><td>

Polling interval

</td><td>

The interval, in seconds, to wait before polling for new events.

</td></tr><tr><td>

Character encoding

</td><td>

The character encoding used for this integration: UTF-8

</td></tr><tr><td>

Drop if queue is full

</td><td>

Option to select discarding logs if there is a load on the MID Server.

</td></tr></tbody>
</table>**Parent Topic:**[Integration configuration fields](../concept/hla-connector-config-fields.md)

