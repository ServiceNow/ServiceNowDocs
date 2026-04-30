---
title: Set partition size for parallel loading-enabled AWS accounts
description: When using the SG-AWS-Image-Private, SG-AWS-Tags, SG-AWS-SendCommand, and AWS-SSM-GetS3Object data sources, you can optimize their performance by setting the partition size in the aws\_account\_partition\_size connection property.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-08-06"
reading_time_minutes: 1
keywords: [SGC-AWS, SGC AWS, SGC for AWS, AWS SGC, Service Graph Connector for AWS, AWS data sources, SG-AWS data sources, SG-AWS, AWS parallel loading, AWS partition size, aws\_account\_partition\_size]
breadcrumb: [Additional features, AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Set partition size for parallel loading-enabled AWS accounts

When using the SG-AWS-Image-Private, SG-AWS-Tags, SG-AWS-SendCommand, and AWS-SSM-GetS3Object data sources, you can optimize their performance by setting the partition size in the **aws\_account\_partition\_size** connection property.

## Before you begin

Set the application scope to Service Graph Connector for AWS using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

Role required: admin

## About this task

The parallel loading feature is available for the SG-AWS-Image-Private, SG-AWS-Tags, SG-AWS-SendCommand, and AWS-SSM-GetS3Object data sources from the Washington DC Patch 5 release. This feature determines the number of AWS accounts that can be executed as parallel jobs to retrieve configuration item \(CI\) data. Partition size determines how many AWS accounts a single parallel-thread evaluates for data retrieval. For example, if you set the **aws\_account\_partition\_size** property to `5` and there are `25` AWS accounts, the application generates `5` parallel jobs during data loading.

**Note:** If the **aws\_account\_partition\_size** property isn't configured, the partition size computation feature of the Integration Commons for CMDB application automatically determines the partition size for parallel loading at runtime. See [Partition size computation for parallel loading in Integration Commons for CMDB](../concept/integration-commons-part-size.md).

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **AWS** &gt; **Connections**.

2.  From the **Name** column of the Service Graph Connections list, select a connection.

3.  From the **Property** column of the Service Graph Connection Properties related list, select **aws\_account\_partition\_size**.

4.  In the **Value** field, enter a numeric value greater than `0` for the partition size.

5.  Select **Update**.


