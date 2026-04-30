---
title: Configure data collection using VPC Flow Logs
description: Enable Service Mapping to perform discovery based on data collected using Virtual Private Cloud \(VPC\) logs. This method is relevant for organizations using Amazon Web Services \(AWS\).
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Data collection and discovery using VPC Flow Logs, Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Configure data collection using VPC Flow Logs

Enable Service Mapping to perform discovery based on data collected using Virtual Private Cloud \(VPC\) logs. This method is relevant for organizations using Amazon Web Services \(AWS\).

## Before you begin

Verify that credentials for the AWS account are configured in the Credentials module of the platform by navigating to **Service Mapping** &gt; **Credentials** &gt; **AWS Credentials**. For more information about AWS credentials, see [Cloud credentials](https://www.servicenow.com/docs/access?context=r_CloudManagementCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

Role required: admin or service\_mapping\_admin

## About this task

In base systems, which are the default or standard configurations, traffic-based discovery relies solely on TCP-related data collected using the **netstat**, **ss**, and **lsof** commands. Discovery based on Netflow and VPC logs requires additional configuration. You can enrich your traffic-based discovery by configuring Service Mapping to use VPC Flow Logs. For more information about the Service Mapping discovery flow based on VPC Flow logs, see [Data collection and discovery using VPC Flow Logs](../concept/data-collection-vpc-mapping.md).

Amazon VPC hosts Amazon Elastic Compute Cloud \(EC2\) instances that provide Amazon Web Services. VPC flow logs collect data on IP traffic going to and from network interfaces in the VPC.

Configure the ServiceNow connector to trigger MID Server to collect the data from the flow log and processes it. In deployments with multiple flow log groups, configure a dedicated connector that works with one MID Server for every flow log group. Multiple flow log groups my use the same AWS credentials.

## Procedure

1.  Configure VPC Flow Logs on the Amazon EC2 console as described in the official AWS documentation.

2.  Configure Service Mapping to work with VPC Flow Logs:

    1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Flow Connectors**.

    2.  Click **New**.

    3.  Click **AWS VPC flow logs**.

    4.  On the AWS VPC flow logs page, configure the connector parameters as follows:

        |Field|Description|
        |-----|-----------|
        |**Name**|A descriptive name for the connector.|
        |**Group name**|The name of the central flow log group to which Amazon EC2 instances forward their log streams.|
        |**MID Server**|The MID Server that Service Mapping uses to collect the data from the flow log group on AWS.|
        |**AWS Credentials**|Select AWS credentials relevant for the account for which you want to collect flow logs.|

    5.  Click **Submit**.

3.  Verify that Service Mapping collects data using VPC Flow Logs:

    1.  On the **AWS VPC flow logs** form, select the newly configured connector and click **Run now** to start the data collection flow and populate the Flow Connection \[sa\_flow\_connection\] table.

    2.  Navigate to **System Definitions** &gt; **Tables**.

    3.  Click the Flow Connection \[sa\_flow\_connection\] table.

    4.  Under **Related Links**, click **Show List**.

    5.  Verify that the table contains data.


