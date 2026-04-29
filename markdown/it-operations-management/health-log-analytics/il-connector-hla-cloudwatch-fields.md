---
title: Amazon CloudWatch integration configuration fields
description: Description of the fields on the Amazon CloudWatch integration configuration forms for Health Log Analytics.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [CloudWatch, data input, integration, configuration, field, description, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Integration configuration fields, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Amazon CloudWatch integration configuration fields

Description of the fields on the Amazon CloudWatch integration configuration forms for Health Log Analytics.

For the Amazon CloudWatch integration setup procedure, see [Set up an Amazon CloudWatch integration for Health Log Analytics](../task/il-connector-hla-aws-cloudwatch.md).

<table id="table_znf_rmf_shc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Name

</td><td>

Unique name of this integration. For example: My CloudWatch integration. This field is required.**Note:** When you fill in this field, the generic name displayed on the form adjusts automatically to match the name you entered.

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

The MID Server to which log data from Amazon CloudWatch is pulled. This field is required.**Note:**

-   You can select only MID Servers that support basic authentication. MID Servers that support mTLS are not listed.
-   The default maximum number of integrations streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.
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

For more information about MID Server clusters, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Data source

</td><td>

The source of the log data that the integration pulls to your ServiceNow instance: CloudWatch. This field is read-only.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the integration to help identify it.

</td></tr></tbody>
</table><table id="table_efv_sqf_shc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

How to extract data from AWS CloudWatch?

</td></tr><tr><td>

Authentication method

</td><td>

The AWS credentials needed to access resources in AWS service accounts. This field is required.Choose AWS credentials from the list, or add new AWS credentials to the list by selecting **Manage Credentials** and then defining new credentials on the **AWS Credentials** page.

</td></tr><tr><td>

Group Name\(s\)

</td><td>

The log group\(s\) to fetch log data from in Amazon CloudWatch. This field is required.If you want the integration to search multiple log groups, specify the relevant groups in a comma-separated list. To fetch log data from all groups, use an asterisk \(\*\) as a wildcard character.

</td></tr><tr><td>

AWS Region

</td><td>

The AWS region where the Amazon CloudWatch cluster is hosted. For example: us-west-1. This field is required.For a list of AWS regions, see [https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html\#concepts-regions](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html#concepts-regions)

</td></tr><tr><td colspan="2">

Which data to send to ServiceNow?

</td></tr><tr><td>

Filter pattern

</td><td>

The pattern by which to filter incoming events.Various types of filter patterns are supported. For example:

-   A pattern for fetching log events that contain a single term.
-   A pattern for fetching log events that contain multiple terms.
-   A pattern for fetching log events that include a term and exclude another.

**Note:** Filter patterns are case sensitive.

 For more information, see [https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/FilterAndPatternSyntax.html](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/FilterAndPatternSyntax.html)

</td></tr><tr><td>

Prefix

</td><td>

Option to define a name prefix for Amazon CloudWatch log streams to read from. The integration reads only from log streams with this name prefix.**Note:** Only a single log stream prefix per data item is supported. For multiple prefixes, create multiple integrations.

</td></tr></tbody>
</table><table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection timeout \(ms\)

</td><td>

The number of milliseconds to wait before timing out the AWS connection attempt.

</td></tr><tr><td>

Socket timeout \(ms\)

</td><td>

The number of milliseconds to wait before timing out a data transfer over an established connection.

</td></tr><tr><td>

Sub sample drop ratio

</td><td>

The number of logs to batch together, out of which one will be dropped. The default value is -1: No logs are dropped.This setting is used to reduce the number of fetched logs. For example, if you want one log out of every five to be dropped, change the value to 5.

</td></tr><tr><td>

Polling interval

</td><td>

The interval, in seconds, to wait before polling for new logs.

</td></tr><tr><td>

Character encoding

</td><td>

The character encoding used for this integration: UTF-8.

</td></tr><tr><td>

Batch size

</td><td>

The maximum number of logs retrieved per query.

</td></tr><tr><td>

Max length in bytes

</td><td>

The maximum length of log messages, in bytes.

</td></tr><tr><td>

Sub sample receive ratio

</td><td>

The number of logs to batch together, out of which one log will be received and the remaining ones dropped. The default value is -1: No logs are received. This setting is used to reduce the number of received logs. For example, if you want to receive one log out of every five, change the value to 5.

</td></tr><tr><td>

Sleep interval \(seconds\)

</td><td>

The interval, in seconds, to wait before querying again after a query has returned no logs.

</td></tr><tr><td>

Default timezone

</td><td>

The default timezone if the log date and time doesn't include timezone information.

</td></tr><tr><td>

Drop if queue is full

</td><td>

Option to select discarding logs if there is a load on the MID Server.

</td></tr></tbody>
</table>**Parent Topic:**[Integration configuration fields](../concept/hla-connector-config-fields.md)

