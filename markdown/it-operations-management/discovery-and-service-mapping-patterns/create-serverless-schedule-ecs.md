---
title: Create a serverless schedule for Amazon ECS discovery
description: Create a serverless schedule to discover Amazon Elastic Container Service \(Amazon ECS\) and Amazon Elastic Container Registry \(ECR\) resources in a standalone discovery.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2025-05-05"
reading_time_minutes: 2
breadcrumb: [Amazon ECS resource, Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create a serverless schedule for Amazon ECS discovery

Create a serverless schedule to discover Amazon Elastic Container Service \(Amazon ECS\) and Amazon Elastic Container Registry \(ECR\) resources in a standalone discovery.

## Before you begin

Verify you have an AWS service account ID and have created AWS credentials. For more information, see the prerequisites section in [Amazon ECS resource discovery](../reference/aws-ecs-fargate-discovery.md).

Role required: discovery\_admin

## About this task

Discovering ECR resources requires running the Amazon AWS - ECS pattern before using Aqua Trivy to scan container images. To discover only ECS and ECR resources without performing a full AWS pattern discovery, create a serverless discovery schedule using the Amazon AWS - ECS pattern.

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules**.

2.  Create the discovery schedule record.

    1.  Select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name for this discovery schedule.|
        |Discover|Scan type, which should be Serverless.|
        |MID server|Name of the MID Server to use for this schedule.|
        |Active|Enables this schedule for discovery.|
        |Run|Determines the run schedule of the discovery.|

    3.  Select **Submit**.

3.  Create the execution pattern.

    1.  In the Discovery Schedules page, select the record you created.

    2.  In the **Serverless Execution Patterns** tab, select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Descriptive name for this record.|
        |Pattern|Pattern to be used for this schedule, which should be Amazon AWS - ECS.|
        |Proxy Host|Fully qualified domain name of the machine on which you're installing the proxy server, which should be Global.|
        |Active|Enables this schedule for discovery.|

    4.  Select **Submit**.

4.  Set the pattern launcher parameters.

    1.  In the **Discovery Pattern Launcher Parameters** tab, select the record you created.

    2.  On the form, fill in the fields.

        |Parameter|Value|
        |---------|-----|
        |cloud\_account\_id|AWS cloud service account ID.|
        |cloud\_cred\_id|Sys\_id of the AWS credentials you created on the ServiceNow AI Platform.|
        |cloud\_datacenter\_type|Name of the AWS Datacenter table, which should be cmdb\_ci\_aws\_datacenter.|

    3.  Select **Submit**.


## What to do next

Either execute discovery immediately by selecting **Discover now** or wait until the predefined schedule triggers the discovery.

**Parent Topic:**[Amazon ECS resource discovery](../reference/aws-ecs-fargate-discovery.md)

**Related topics**  


[Amazon ECS resource discovery](../reference/aws-ecs-fargate-discovery.md)

[Scan container images](container-image-task.md)

