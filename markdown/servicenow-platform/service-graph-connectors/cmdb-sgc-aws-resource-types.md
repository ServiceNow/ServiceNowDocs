---
title: Supported AWS resource types
description: Several AWS resource types are imported as CMDB data by the Service Graph Connector for AWS.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Reference, AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Supported AWS resource types

Several AWS resource types are imported as CMDB data by the Service Graph Connector for AWS.

## AWS Config resources

When the AWS Config aggregator is enabled, the following APIs are invoked:

-   [ListDiscoveredResources](https://docs.aws.amazon.com/config/latest/APIReference/API_ListDiscoveredResources.html)
-   [BatchGetAggregateResourceConfig](https://docs.aws.amazon.com/config/latest/APIReference/API_BatchGetAggregateResourceConfig.html)
-   [SelectAggregateResourceConfig](https://docs.aws.amazon.com/config/latest/APIReference/API_SelectAggregateResourceConfig.html)

When the AWS Config aggregator is disabled, the following APIs are invoked:

-   [ListDiscoveredResources](https://docs.aws.amazon.com/config/latest/APIReference/API_ListDiscoveredResources.html)
-   [SelectResourceConfig](https://docs.aws.amazon.com/config/latest/APIReference/API_SelectResourceConfig.html)
-   [BatchGetResourceConfigAction](https://docs.aws.amazon.com/config/latest/APIReference/API_BatchGetResourceConfig.html)

**Note:** For a list of AWS resource types supported by AWS Config, see [Supported Resource Types](https://docs.aws.amazon.com/config/latest/developerguide/resource-config-reference.html) on the AWS documentation site.

<table id="table_xgj_tjm_q1c"><thead><tr><th>

CMDB CI classes

</th><th>

AWS resource type

</th><th>

AWS Config resource identifier

</th></tr></thead><tbody><tr><td>

Cloud Network \[cmdb\_ci\_network\]

</td><td>

Amazon VPC

</td><td>

AWS::EC2::VPC

</td></tr><tr><td>

Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]

</td><td>

Amazon subnet

</td><td>

AWS::EC2::Subnet

</td></tr><tr><td>

Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]

</td><td>

Amazon Elastic network interface

</td><td>

AWS::EC2::NetworkInterface

</td></tr><tr><td>

Compute Security Group \[cmdb\_ci\_compute\_security\_group\]

</td><td>

Amazon EC2 security group

</td><td>

AWS::EC2::SecurityGroup

</td></tr><tr><td>

Storage Volume \[cmdb\_ci\_storage\_volume\]

</td><td>

Amazon EBS volume

</td><td>

AWS::EC2::Volume

</td></tr><tr><td>

Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

</td><td>

Classic load balancer

</td><td>

AWS::ElasticLoadBalancing::LoadBalancer

</td></tr><tr><td>

Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

</td><td>

Application load balancer, network load balancer, or gateway load balancer

</td><td>

AWS::ElasticLoadBalancingV2::LoadBalancer

</td></tr><tr><td>

Cloud Gateway \[cmdb\_ci\_cloud\_gateway\]

</td><td>

API gateway with WebSocket APIs or HTTP APIs

</td><td>

AWS::ApiGatewayV2::Api

</td></tr><tr><td>

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

</td><td>

Amazon EC2 instance

</td><td>

AWS::EC2::Instance

</td></tr><tr><td>

Server \[cmdb\_ci\_server\]

</td><td>

Amazon EC2 instance

</td><td>

AWS::EC2::Instance

</td></tr><tr><td>

Cloud DataBase \[cmdb\_ci\_cloud\_database\]

</td><td>

Amazon RDS DB instance

</td><td>

AWS::RDS::DBInstance

</td></tr><tr><td>

Cloud Function \[cmdb\_ci\_cloud\_function\]

</td><td>

Lambda function

</td><td>

AWS::Lambda::Function

</td></tr><tr><td>

Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]

</td><td>

Amazon S3 bucket

</td><td>

AWS::S3::Bucket

</td></tr><tr><td>

DynamoDB Table \[cmdb\_ci\_dynamodb\_table\]

</td><td>

DynamoDB table

</td><td>

AWS::DynamoDB::Table

</td></tr><tr><td>

Software \[cmdb\_ci\_spkg\]

</td><td>

Software configuration for managed instances

</td><td>

AWS::SSM::ManagedInstanceInventory

</td></tr><tr><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td><td>

Amazon EKS cluster

</td><td>

AWS::EKS::Cluster

</td></tr><tr><td>

Amazon Redshift \[cmdb\_ci\_aws\_redshift\]

</td><td>

Amazon Redshift

</td><td>

AWS::Redshift::Cluster

</td></tr></tbody>
</table>## Amazon EC2 resources

<table id="id_jfw_yjm_q1c"><thead><tr><th>

CMDB CI classes

</th><th>

AWS resource type

</th><th>

AWS API action

</th></tr></thead><tbody><tr><td>

Availability Zone \[cmdb\_ci\_availability\_zone\]

</td><td>

AWS availability zone

</td><td>

None

</td></tr><tr><td>

Hardware Type \[cmdb\_ci\_compute\_template\]

</td><td>

Amazon EC2 instance types

</td><td>

[DescribeInstanceTypes](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeInstanceTypes.html)

</td></tr><tr><td>

Image \[cmdb\_ci\_os\_template\]

</td><td>

Amazon Machine Image \(AMI\)

</td><td>

[DescribeImages](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeImages.html)

</td></tr><tr><td>

Cloud Image \[cmdb\_ci\_cloud\_os\_image\]

</td><td>

Amazon Machine Image \(AMI\)

</td><td>

[DescribeImages](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeImages.html)

</td></tr><tr><td>

Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]

</td><td>

Amazon EC2 instance types

</td><td>

[DescribeInstanceTypes](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeInstanceTypes.html)

</td></tr></tbody>
</table>## AWS Systems Manager resources

All AWS Systems Manager resources invoke the [SendCommand](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_SendCommand.html) API action.

<table id="table_j5g_cv3_r1c"><thead><tr><th>

CMDB CI classes

</th><th>

AWS resource type

</th><th>

AWS API action

</th></tr></thead><tbody><tr><td>

Running Process \[cmdb\_running\_process\]

</td><td>

Running process in EC2 instances

</td><td rowspan="10">

[SendCommand](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_SendCommand.html)

</td></tr><tr><td>

TCP Connections \[cmdb\_tcp\]

</td><td>

TCP connections in EC2 instances

</td></tr><tr><td>

Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]

</td><td>

Amazon EKS node

</td></tr><tr><td>

Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

</td><td>

Amazon EKS pod

</td></tr><tr><td>

Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]

</td><td>

Amazon EKS service

</td></tr><tr><td>

Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\]

</td><td>

Kubernetes DaemonSet

</td></tr><tr><td>

Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]

</td><td>

Kubernetes namespace

</td></tr><tr><td>

Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]

</td><td>

Kubernetes deployment

</td></tr><tr><td>

Docker Container \[cmdb\_ci\_docker\_container\]

</td><td>

Docker container

</td></tr><tr><td>

Kubernetes Volume \[cmdb\_ci\_kubernetes\_volume\]

</td><td>

Kubernetes Volume

</td></tr></tbody>
</table>## Organizations resources

<table id="table_t2y_2jm_q1c"><thead><tr><th>

CMDB CI classes

</th><th>

AWS resource type

</th><th>

AWS API action

</th></tr></thead><tbody><tr><td>

Cloud Organizations \[cmdb\_ci\_cloud\_org\]

</td><td>

AWS Organizations

</td><td>

[DescribeOrganization](https://docs.aws.amazon.com/organizations/latest/APIReference/API_DescribeOrganization.html)

</td></tr><tr><td>

Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

</td><td>

AWS accounts

</td><td>

[ListAccounts](https://docs.aws.amazon.com/organizations/latest/APIReference/API_ListAccounts.html)

</td></tr><tr><td>

AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]

</td><td>

AWS regions

</td><td>

[DescribeRegions](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeRegions.html)

</td></tr></tbody>
</table>## Resource Group Tagging resources

<table id="table_nzd_kcj_r1c"><thead><tr><th>

CMDB classes

</th><th>

AWS resource type

</th><th>

AWS API action

</th></tr></thead><tbody><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Tags for AWS Lambda, Amazon DynamoDB, ELBv1, and ELBv2

</td><td>

[GetResources](https://docs.aws.amazon.com/resourcegroupstagging/latest/APIReference/API_GetResources.html)

</td></tr></tbody>
</table>## Generic resources

Generic resources are stored in the Cloud Resource \[cmdb\_ci\_cmp\_resource\] CMDB CI class.

<table id="table_tvd_3tq_k1c"><thead><tr><th>

CMDB CI class

</th><th>

AWS resource type

</th><th>

AWS API action

</th></tr></thead><tbody><tr><td rowspan="41">

Cloud Resource \[cmdb\_ci\_cmp\_resource\]

</td><td>

State Manager association compliance

</td><td>

AWS::SSM::AssociationCompliance

</td></tr><tr><td>

Database subnet group

</td><td>

AWS::RDS::DBSubnetGroup

</td></tr><tr><td>

AWS WAF rate based rule

</td><td>

AWS::WAF::RateBasedRule

</td></tr><tr><td>

AWS WAF regional rule group

</td><td>

AWS::WAFRegional::RuleGroup

</td></tr><tr><td>

AWS WAF regional rate based rule

</td><td>

AWS::WAFRegional::RateBasedRule

</td></tr><tr><td>

Managed policies and inline policies

</td><td>

AWS::IAM::Policy

</td></tr><tr><td>

AWS WAF Web ACL rule

</td><td>

AWS::WAF::WebACL

</td></tr><tr><td>

AWS WAF Regional Web ACL rule

</td><td>

AWS::WAFRegional::WebACL

</td></tr><tr><td>

AWS Certificate Manager \(ACM\) certificate

</td><td>

AWS::ACM::Certificate

</td></tr><tr><td>

Amazon EC2 Auto Scaling group

</td><td>

AWS::AutoScaling::AutoScalingGroup

</td></tr><tr><td>

IAM user for AWS account

</td><td>

AWS::IAM::User

</td></tr><tr><td>

Amazon Redshift event subscription

</td><td>

AWS::Redshift::EventSubscription

</td></tr><tr><td>

Amazon RDS DB snapshot

</td><td>

AWS::RDS::DBSnapshot

</td></tr><tr><td>

Amazon Redshift cluster parameter group

</td><td>

AWS::Redshift::ClusterParameterGroup

</td></tr><tr><td>

Amazon EC2 Auto Scaling group launch configuration

</td><td>

AWS::AutoScaling::LaunchConfiguration

</td></tr><tr><td>

Amazon Redshift cluster snapshot

</td><td>

AWS::Redshift::ClusterSnapshot

</td></tr><tr><td>

AWS CloudFormation stack

</td><td>

AWS::CloudFormation::Stack

</td></tr><tr><td>

AWS CodeBuild project

</td><td>

AWS::CodeBuild::Project

</td></tr><tr><td>

AWS Elastic Beanstalk application version

</td><td>

AWS::ElasticBeanstalk::ApplicationVersion

</td></tr><tr><td>

AWS CodePipeline pipeline

</td><td>

AWS::CodePipeline::Pipeline

</td></tr><tr><td>

Amazon Redshift security group

</td><td>

AWS::Redshift::ClusterSecurityGroup

</td></tr><tr><td>

Amazon CloudFront distribution

</td><td>

AWS::CloudFront::Distribution

</td></tr><tr><td>

AWS CloudTrail trail

</td><td>

AWS::CloudTrail::Trail

</td></tr><tr><td>

Amazon CloudFront streaming distribution

</td><td>

AWS::CloudFront::StreamingDistribution

</td></tr><tr><td>

AWS WAF rule group

</td><td>

AWS::WAF::RuleGroup

</td></tr><tr><td>

Amazon RDS DB security group

</td><td>

AWS::RDS::DBSecurityGroup

</td></tr><tr><td>

Amazon RDS event subscription

</td><td>

AWS::RDS::EventSubscription

</td></tr><tr><td>

AWS WAF regional rule

</td><td>

AWS::WAFRegional::Rule

</td></tr><tr><td>

AWS WAF rule

</td><td>

AWS::WAF::Rule

</td></tr><tr><td>

IAM role for AWS account

</td><td>

AWS::IAM::Role

</td></tr><tr><td>

Amazon EC2 Auto Scaling scheduled action

</td><td>

AWS::AutoScaling::ScheduledAction

</td></tr><tr><td>

AWS Elastic Beanstalk environment

</td><td>

AWS::ElasticBeanstalk::Environment

</td></tr><tr><td>

AWS Redshift cluster

</td><td>

AWS::Redshift::Cluster

</td></tr><tr><td>

Amazon EC2 Auto Scaling group scaling policy

</td><td>

AWS::AutoScaling::ScalingPolicy

</td></tr><tr><td>

AWS Shield protected AWS resource

</td><td>

AWS::Shield::Protection

</td></tr><tr><td>

Amazon CloudWatch alarm

</td><td>

AWS::CloudWatch::Alarm

</td></tr><tr><td>

EncryptionConfig - AWS X-Ray

</td><td>

AWS::XRay::EncryptionConfig

</td></tr><tr><td>

AWS Shield protected AWS region

</td><td>

AWS::ShieldRegional::Protection

</td></tr><tr><td>

Amazon Redshift subnet group

</td><td>

AWS::Redshift::ClusterSubnetGroup

</td></tr><tr><td>

AWS Elastic Beanstalk application

</td><td>

AWS::ElasticBeanstalk::Application

</td></tr><tr><td>

IAM group for AWS account

</td><td>

AWS::IAM::Group

</td></tr></tbody>
</table>**Parent Topic:**[Service Graph Connector for AWS reference](../concept/sgc-cmdb-aws-reference.md)

