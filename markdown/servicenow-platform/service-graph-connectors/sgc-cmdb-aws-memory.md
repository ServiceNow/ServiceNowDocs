---
title: Handling memory utilization errors for Service Graph Connector for AWS
description: You can use the SgAwsApplicationProperties script include to avoid memory utilization errors when importing a large number of configuration items \(CIs\) from an AWS instance via the Service Graph Connector for AWS.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Additional features, AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Handling memory utilization errors for Service Graph Connector for AWS

You can use the `SgAwsApplicationProperties` script include to avoid memory utilization errors when importing a large number of configuration items \(CIs\) from an AWS instance via the Service Graph Connector for AWS.

By making multiple database calls to ingest AWS data in smaller batches, the `SgAwsApplicationProperties` script include avoids overloading of the Robust Transform Engine \(RTE\) and results in reduced memory usage. However, for the script include to function properly, verify that the AWS Config aggregator is enabled on your AWS instance.

To access the script include, navigate to **All** &gt; **System Definitions** &gt; **Script Includes**, and then search for and select `SgAwsApplicationProperties`. For more information, see [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

In the `SgAwsApplicationProperties` script include, you can modify the functions as described in the following table to resolve memory utilization errors.

<table id="table_qnt_srm_plb"><thead><tr><th>

Functionality

</th><th>

Implementation

</th></tr></thead><tbody><tr><td>

Enable multiple database calls to import the AWS Config data.

</td><td>

Set the value of the isConfigDbLoadEnabled function to `true`. For the function to work correctly, verify that the AWS Config aggregator is enabled.**Note:** Enabling isConfigDbLoadEnabled might impact the import set load time as multiple database calls are being made instead of a single database call.

Enabling the isConfigDbLoadEnabled function resolves the memory utilization error for the following data sources:

-   SG-AWS-API-Gateway
-   SG-AWS-DynamoDb
-   SG-AWS-EC2
-   SG-AWS-EKS-Cluster
-   SG-AWS-ELB-V1
-   SG-AWS-ELB-V2
-   SG-AWS-Generic-Resources
-   SG-AWS-Lambda
-   SG-AWS-Network-Interface
-   SG-AWS-RDS
-   SG-AWS-S3
-   SG-AWS-Security-Group
-   SG-AWS-Storage-Volume
-   SG-AWS-Subnets
-   SG-AWS-VPC

</td></tr><tr><td>

Enable multiple database calls to import the tag-related data from your AWS service account.

</td><td>

Set the value of the isConfigTagsDbLoadEnabled function to `true`. For the function to work correctly, verify that both the AWS Config aggregator and the isConfigDbLoadEnabled function are enabled.Enabling the isConfigTagsDbLoadEnabled function facilitates the AWS Config aggregator to reduce the load time for tag-related data in the following data sources:

-   SG-AWS-Lambda
-   SG-AWS-DynamoDb
-   SG-AWS-ELB-V1
-   SG-AWS-ELB-V2

</td></tr></tbody>
</table>