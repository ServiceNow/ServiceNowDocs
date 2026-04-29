---
title: AWS resources used by the Service Graph Connector for AWS
description: Get familiar with the AWS concepts to learn how the Service Graph Connector for AWS is integrated with Amazon Web Services \(AWS\).
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure the AWS environment, AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# AWS resources used by the Service Graph Connector for AWS

Get familiar with the AWS concepts to learn how the Service Graph Connector for AWS is integrated with Amazon Web Services \(AWS\).

## AWS Config service and configuration recorder

**Important:** The AWS Config service and AWS configuration recorder are required for setting up the connector.

The AWS Config service monitors and records changes to your AWS resource configurations.

The AWS configuration recorder detects changes in resource configurations and captures these changes as configuration items \(CIs\). The is required for setting up the connector. The configuration recorder enables recording all hardware data in AWS Config. See [What Is AWS Config?](https://docs.aws.amazon.com/config/latest/developerguide/WhatIsConfig.html) on the AWS Documentation site.

The Service Graph Connector for AWS includes the EnableAWSConfig.yml script to enable the AWS Config service that instead enables the configuration recorder. See [Executing scripts required for setting up AWS](sgc-cmdb-aws-script-op.md).

**Note:** Ensure that the AWS Config service is enabled for all applicable AWS accounts and regions.

## AWS Config aggregator

**Important:** The AWS Config aggregator is optional for setting up the connector.

The AWS Config aggregator collects the AWS Config configuration and compliance data from the following sources:

-   Multiple accounts and multiple regions
-   Single account and multiple regions
-   An organization in AWS organizations and all the accounts within the organization that have AWS Config enabled.

The advantages of using an AWS Config aggregator with the Service Graph Connector for AWS are:

-   Gets all the data from a single location.
-   Gets the bootstrap updates \(baseline configurations\) and the incremental updates \(new configurations added after the last update\).
-   Doesn't require looping into each account and region.
-   Accelerates pulling data.

Due to these advantages, consider leveraging the AWS Config aggregator for pulling data from multiple accounts or multiple regions.

**Note:** For detecting any deleted resources, the connector uses the config:ListDiscoveredResources API to loop through each AWS account and region and update the CMDB CI accordingly. As a date range for selecting resources can't be specified in the ListDiscoveredResources API, the connector might make multiple API calls to gather all the data that might impact the performance of the connector.

For more information on setting up an AWS Config aggregator, see [Multi-Account Multi-Region Data Aggregation](https://docs.aws.amazon.com/config/latest/developerguide/aggregate-data.html) and [Setting Up an Aggregator Using the Console](https://docs.aws.amazon.com/config/latest/developerguide/setup-aggregator-console.html) on the AWS Documentation site.

## AWS Systems Manager and AWS Systems Manager Inventory

**Important:** AWS Systems Managerand AWS Systems Manager Inventory are required for setting up the deep discovery feature.

The AWS Systems Manager enables fetching server data, also called as deep discovery data, from EC2 instances across AWS accounts and regions through SSM documents. The deep discovery data includes host name, serial number, CPU data, TCP data, and process information.

The AWS Systems Manager Inventory imports the software data installed on the EC2 instances. The Inventory resource group in AWS Systems Manager collects information about the EC2 instances and the software applications installed on them.

Ensure that the following items are configured in all AWS accounts:

-   The AWS Systems Manager Agent \(SSM Agent\) is installed on all managed EC2 instances.
-   The AmazonSSMForInstancesRole IAM instance profile role is attached as the instance profile on EC2 instances.
-   The AWS Systems Manager Inventory is configured in each AWS region.
-   The AWS Systems Manager has access to the managed EC2 instances.

    **Note:** By default, AWS Systems Manager doesn’t have permission to perform actions on EC2 instances. You can grant access by attaching the AmazonSSMForInstancesRole IAM instance profile role to the EC2 instance. See [Setting up AWS Systems Manager](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-prereqs.html) on the AWS Documentation site.


The advantages of using AWS Systems Manager and AWS Systems Manager Inventory are:

-   The AWS Systems Manager enables getting the detailed server data such as host name, serial number, CPU data, TCP data, and process information.
-   The AWS Systems Manager Inventory enables the server classification and getting the software data.

