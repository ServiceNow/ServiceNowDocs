---
title: Service categories discovered in AWS
description: The Discovery process discovers AWS services.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Cloud accounts, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Service categories discovered in AWS

The Discovery process discovers AWS services.

## Services categories discovered in AWS

|Service Category|Name|CI Class|Pattern|Product|
|----------------|----|--------|-------|-------|
|Compute|AWS::CloudFormation::Stack|cmdb\_ci\_aws\_cloudformation\_stack| |AWS CloudFormation|
|Database|AWS::Datacenter|cmdb\_ci\_aws\_datacenter| | |
|Security|AWS::DirectoryService| | |AWS Directory Service|
|Compute|AWS::EC2::EIP|cmdb\_ci\_cloud\_ip\_address| |AWS Elastic Compute Cloud|
|Compute|AWS::EC2::Image|cmdb\_ci\_os\_template| |AWS Elastic Compute Cloud|
|Compute|AWS::EC2::Instance|cmdb\_ci\_vm\_instance| |AWS Elastic Compute Cloud|
|Compute|AWS::EC2::InstanceType|cmdb\_ci\_compute\_template| |AWS Elastic Compute Cloud|
|Security|AWS::EC2::Keypair|cmdb\_ci\_cloud\_key\_pair| |AWS Key Management Service|
|Network|AWS::EC2::NetworkInterface|cmdb\_ci\_nic| |AWS Virtual Private Cloud|
|Compute|AWS::EC2::SecurityGroup|cmdb\_ci\_compute\_security\_group| |AWS Elastic Compute Cloud|
|Network|AWS::EC2::Subnet|cmdb\_ci\_cloud\_subnet| |AWS Virtual Private Cloud|
|Storage|AWS::EC2::Volume|cmdb\_ci\_storage\_volume| |AWS Elastic Block Storage|
|Network|AWS::EC2::VPC|cmdb\_ci\_network| |AWS Virtual Private Cloud|
|Load Balancer|AWS::ElasticLoadBalancing::LoadBalancer|cmdb\_ci\_cloud\_load\_balancer|Amazon AWS Elastic Load Balancer Service|AWS Elastic Load Balancing|
|Load Balancer|AWS::ElasticLoadBalancingV2::LoadBalancer|cmdb\_ci\_cloud\_load\_balancer|Amazon AWS Elastic Load Balancer Service|AWS Elastic Load Balancing|
|Database|AWS::RDS::DBEvent| | |AWS Relational Database Service|
|Database|AWS::RDS::DBInstance|cmdb\_ci\_cloud\_database|Amazon AWS Relational Database Service|AWS Relational Database Service|
| |Availability zone|cmdb\_ci\_availability\_zone| |AWS Availability Zone|

**Note:** The full list of classes/resources matching can be found in the Cloud Resource Types \[sn\_capi\_resource\_type\] table.

**Parent Topic:**[Cloud accounts](../concept/cloud-accounts.md)

