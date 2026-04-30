---
title: Edit settings form reference
description: The Edit settings form displays information about the Amazon Web Services \(AWS\) settings used to record and deliver the AWS events to the listening endpoint.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Cloud Discovery reference, Discovery reference, Discovery, ITOM Visibility, IT Operations Management]
---

# Edit settings form reference

The Edit settings form displays information about the Amazon Web Services \(AWS\) settings used to record and deliver the AWS events to the listening endpoint.

<table id="table_alv_5k1_wvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

General settings

</td></tr><tr><td>

Resource types to record

</td><td>

Resource types for which you want to record the configuration change.Also specify whether you want to record the configuration change for global resources such as AWS AMI resources.

 For more information, see the [Selecting Which Resources AWS Config Records](https://docs.aws.amazon.com/config/latest/developerguide/select-resources.html) topic in the AWS documentation.

</td></tr><tr><td>

Data retention period

</td><td>

\(Optional\) Retention policy for the recorded events.

</td></tr><tr><td>

AWS Config role

</td><td>

An AWS role that can access the following services and resources:-   Simple Notification Service \(SNS\)
-   AWS Config service
-   Resource types for which you want to track the configuration change

</td></tr><tr><td colspan="2">

Delivery method

</td></tr><tr><td>

AWS S3 bucket

</td><td>

An AWS S3 bucket to store the recorded events.Create an AWS S3 bucket or select an existing AWS S3 bucket to which you have access.

</td></tr><tr><td>

Stream configuration changes and notifications to an Amazon SNS topic

</td><td>

Option to publish the event notifications to the SNS topic.

</td></tr><tr><td>

Amazon SNS topic

</td><td>

Amazon SNS topic to which the AWS Config service should publish the events.1.  Select the **Choose a topic from your account** option.
2.  Select the Amazon SNS topic created in step [3](../task/aws-config-service-cloud-mgt.md#create-sns-topic) from the SNS topic name drop-down list.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Discovery reference](../../discovery/reference/cloud-discovery-reference.md)

