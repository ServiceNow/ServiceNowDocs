---
title: Set partition size for AWS API Gateway accounts
description: You can optimize their performance of AWS API Gateway data sources by setting the partition size in the PartitionSize connection property.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-01-20"
reading_time_minutes: 1
keywords: [SGC-AWS-API, SGC AWS API, SGC for AWS API, AWS API SGC, Service Graph Connector for AWS API Gateway, AWS API Gateway data sources, SG-AWS API Gateway data sources, SG-AWS API Gateway, AWS API Gateway parallel loading, AWS API Gateway partition size, aws\_account\_partition\_size]
breadcrumb: [Additional features, AWS API Gateway, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Set partition size for AWS API Gateway accounts

You can optimize their performance of AWS API Gateway data sources by setting the partition size in the **PartitionSize** connection property.

## Before you begin

Set the application scope to API Service Graph Connector for AWS API Gateway using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Role required: admin

## About this task

The parallel loading feature is available for the following AWS API Gateway data sources:

-   Frontend Backend REST
-   Frontend V2
-   Backend V2
-   Deployment Rest
-   Deployment V2

This feature determines how many Managed APIs execute as parallel jobs to retrieve configuration item \(CI\) data. The partition size specifies how many Managed APIs a single parallel thread evaluates for data retrieval. For example, if you set the **PartitionSize** property to `5` and there are `25` Managed APIs, the application generates `5` parallel jobs during data loading.

**Note:** If the **PartitionSize** property isn't configured, the partition size computation feature of the Integration Commons for CMDB application automatically determines the partition size for parallel loading at runtime. See [Partition size computation for parallel loading in Integration Commons for CMDB](../concept/integration-commons-part-size.md).

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **AWS API Gateway** &gt; **Connections**.

2.  From the **Name** column of the Service Graph Connections list, select a connection.

3.  From the **Property** column of the Service Graph Connection Properties related list, select **PartitionSize**.

4.  In the **Value** field, enter a numeric value greater than `0` for the partition size.

5.  Select **Update**.


