---
title: Set page size for AWS API Gateway accounts
description: When retrieving data from an AWS API Gateway service, you can control the number of records fetched per API call by setting the PageSize connection property. This affects pagination behavior when calling APIs.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-01-20"
reading_time_minutes: 1
keywords: [SGC-AWS-API, SGC AWS API, SGC for AWS API, AWS API SGC, Service Graph Connector for AWS API Gateway, AWS API Gateway data sources, SG-AWS API Gateway data sources, SG-AWS API Gateway, AWS API Gateway parallel loading, AWS API Gateway partition size, aws\_account\_partition\_size]
breadcrumb: [Additional features, AWS API Gateway, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Set page size for AWS API Gateway accounts

When retrieving data from an AWS API Gateway service, you can control the number of records fetched per API call by setting the **PageSize** connection property. This affects pagination behavior when calling APIs.

## Before you begin

Set the application scope to API Service Graph Connector for AWS API Gateway using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

Role required: admin

## About this task

The **PageSize** property controls how many records are retrieved in each API request to AWS. This property affects pagination behavior across all data sources.

Example: If you set the **PageSize** property to `50` and there are `200` REST APIs in your API Service Graph Connector for AWS API Gateway account, the connector makes `4` API calls to retrieve all records.

**Note:** For AWS Config Aggregator setups, the page size must not exceed `100` due to AWS API limitations on the SelectAggregateResourceConfig API.

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **AWS API Gateway** &gt; **Connections**.

2.  From the **Name** column of the Service Graph Connections list, select a connection.

3.  From the **Property** column of the Service Graph Connection Properties related list, select **PageSize**.

4.  In the **Value** field, enter a numeric value depending on the configuration type.

    |Configuration type|Description|
    |------------------|-----------|
    |**Config aggregator setup**|Enter a value between `1` and `100`.|
    |**Other configurations**|Enter a value between `1` and `500`.|

5.  Select **Update**.


