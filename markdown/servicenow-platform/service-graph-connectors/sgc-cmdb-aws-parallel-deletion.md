---
title: Handling parallel deletion of CIs in Service Graph Connector for AWS
description: Parallel deletion of configuration items \(CIs\) in the Service Graph Connector for AWS optimizes performance.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Additional features, AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Handling parallel deletion of CIs in Service Graph Connector for AWS

Parallel deletion of configuration items \(CIs\) in the Service Graph Connector for AWS optimizes performance.

The parallel deletion feature is available for the following data sources from Washington DC patch 5 after the parallel job plugin is activated:

-   SG-AWS-API-Gateway
-   SG-AWS-DynamoDb
-   SG-AWS-EC2
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

**Note:** If you upgraded to Service Graph Connector for AWS version 2.9.1 before the parallel job plugin was activated, you must run the `SGC - Parallel Loading Fix` script to enable parallel deletion.

Multiple jobs are created for deleting CIs based on the number of accounts in your configuration. You can modify the number of jobs that are created by setting the partition size in the **aws\_account\_partition\_size** connection property. See [Set partition size for parallel loading-enabled AWS accounts](../task/sgc-aws-partition-size-prop.md).

**Note:** Only one job is created to import new and updated CIs.

