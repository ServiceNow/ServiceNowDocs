---
title: AWS discovery solutions comparison
description: ITOM Visibility applications discover a variety of AWS resources and populate the relevant configuration item \(CI\) classes in the Configuration Management Database \(CMDB\) with their attributes.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-08-12"
reading_time_minutes: 4
keywords: [Patterns, AWS, Cloud, Discovery, Visibility, CMDB, Service Graph Connector, Configuration Item]
breadcrumb: [Reference, AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# AWS discovery solutions comparison

ITOM Visibility applications discover a variety of AWS resources and populate the relevant configuration item \(CI\) classes in the Configuration Management Database \(CMDB\) with their attributes.

## ITOM Visibility solutions

ITOM Visibility can offer you comprehensive visibility into your organization's cloud infrastructure. Each application offers unique strengths and capabilities, and by comparing them you can gain holistic insights on their capabilities and benefits.

<table id="table_sld_tvh_hfc"><thead><tr><th>

ITOM Visibility solution

</th><th>

Overview

</th><th>

Configuration

</th></tr></thead><tbody><tr><td>

Discovery and Service Mapping Patterns and Visibility Content

</td><td>

[Discovery patterns used by ITOM Visibility](https://www.servicenow.com/docs/access?context=c_MappingPatternsCustomization&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)

</td><td>

-   You must update your store apps to the latest release version.
-   You must provide ITOM Visibility with access permissions. For more information, see [Set up AWS service accounts](https://www.servicenow.com/docs/access?context=setup-aws-service-accounts&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)

</td></tr><tr><td>

Service Graph Connector for AWS

</td><td>

[Service Graph Connector for AWS](../../configuration-management/concept/cmdb-integration-aws-sg.md)

</td><td>

[Configure Service Graph Connector for AWS using the guided setup](../../configuration-management/task/configure-aws-integration.md)

</td></tr></tbody>
</table>**Note:**

The CI class, in most cases, is applicable to both solutions. If it's not applicable to one of the solutions, the solution is marked "N/A".

|Resource type|Supported by Cloud Discovery and Service Mapping Patterns|Supported by Cloud Service Graph Connectors|CI Class|
|-------------|---------------------------------------------------------|-------------------------------------------|--------|
|AWS::AppSync::API|Yes|No|cmdb\_aws\_appsync\_api|
|AWS::Athena::Workgroup|Yes|No|cmdb\_aws\_athena\_workgroup|
|AWS::Backup::BackupPlan|Yes|No|cmdb\_aws\_backup\_backup\_plan|
|AWS::Backup::BackupVault|Yes|No|cmdb\_aws\_backup\_backup\_vault|
|AWS::CloudFront::Distribution|Yes|N/A|cmdb\_aws\_cloudfront\_distribution|
|AWS::CloudFront::Distribution|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::CloudWatch::Log|Yes|No|cmdb\_aws\_cloudwatch\_log|
|AWS::CodeDeployment::Deployment|Yes|No|cmdb\_aws\_codedeploy\_deployment|
|AWS::CodePipeline::Pipeline|Yes|N/A|cmdb\_aws\_codepipeline\_pipeline|
|AWS::CodePipeline::Pipeline|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::DMS::Endpoint|Yes|No|cmdb\_aws\_dms\_endpoint|
|AWS::ElasticBeanstalk::Application|Yes|N/A|cmdb\_aws\_elastic\_beanstalk\_application|
|AWS::ElasticBeanstalk::Application|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::EMR::Cluster|Yes|No|cmdb\_aws\_emr\_cluster|
|AWS::EventBridge::EventBus|Yes|No|cmdb\_aws\_eventbridge\_event\_bus|
|AWS::FSx::Backup|Yes|No|cmdb\_aws\_fsx\_backup|
|AWS::FSx::FileSystem|Yes|No|cmdb\_aws\_fsx\_file\_system|
|AWS::Glue::Database|Yes|No|cmdb\_aws\_glue\_database|
|AWS::IAM::Policy|Yes|N/A|cmdb\_aws\_iam\_policy|
|AWS::IAM::Policy|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::IAM::Role|Yes|N/A|cmdb\_aws\_iam\_role|
|AWS::IAM::Role|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::IAM::User|Yes|N/A|cmdb\_aws\_iam\_user|
|AWS::IAM::User|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::KMS::Key|Yes|No|cmdb\_aws\_kms\_key|
|AWS::MQ::Broker|Yes|No|cmdb\_aws\_mq\_broker|
|AWS::MQ::Configuration|Yes|No|cmdb\_aws\_mq\_configuration|
|AWS::S3::GlacierVault|Yes|No|cmdb\_aws\_s3\_glacier\_vault|
|AWS::SageMaker::NotebookInstance|Yes|No|cmdb\_aws\_sagemaker\_notebook\_instance|
|AWS::SecretsManager::Secret|Yes|No|cmdb\_aws\_secrets\_manager\_secret|
|AWS::SimpleEmailService::Identity|Yes|No|cmdb\_aws\_simple\_email\_service\_identity|
|AWS::SQS::Queue|Yes|No|cmdb\_aws\_sqs\_queue|
|AWS::StepFunctions::StateMachine|Yes|No|cmdb\_aws\_step\_functions\_state\_machine|
|AWS::StorageGateway::Gateway|Yes|No|cmdb\_aws\_storage\_gateway\_gateway|
|AWS::SystemsManager::Document|Yes|No|cmdb\_aws\_systems\_manager\_document|
|AWS::SystemsManager::ParameterStore|Yes|No|cmdb\_aws\_systems\_manager\_parameter\_store|
|AWS::TransferFamily::Server|Yes|No|cmdb\_aws\_transfer\_family\_server|
|AWS::VPC::FlowLog|Yes|No|cmdb\_aws\_vpc\_flow\_log|
|AWS::VPC::ManagedPrefixList|Yes|No|cmdb\_aws\_vpc\_managed\_prefix\_list|
|AWS::XRay::SamplingRule|Yes|No|cmdb\_aws\_xray\_sampling\_rule|
|ec2:DescribeAvailabilityZones|Yes|Yes|cmdb\_ci\_availability\_zone|
|ec2:DescribeRegions|Yes|Yes|cmdb\_ci\_aws\_datacenter|
|AWS::Kinesis::Stream|Yes|No|cmdb\_ci\_aws\_kinesis\_data|
|AWS::KinesisAnalytics|Yes|No|cmdb\_ci\_aws\_kinesis\_data\_analytics|
|AWS::KinesisFirehose|Yes|No|cmdb\_ci\_aws\_kinesis\_firehose|
|AWS::KinesisVideo|Yes|No|cmdb\_ci\_aws\_kinesis\_video|
|AWS::Redshift::Cluster|Yes|N/A|cmdb\_ci\_aws\_redshift|
|AWS::Redshift::Cluster|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::CertificateManager::Certificate|Yes|No|cmdb\_ci\_certificate|
|AWS::Cognito::UserPool|Yes|No|cmdb\_ci\_cloud\_authentication|
|AWS::RDS::DBInstance|Yes|Yes|cmdb\_ci\_cloud\_database|
|AWS::ECS::Cluster|Yes|No|cmdb\_ci\_cloud\_ecs\_cluster|
|AWS::ECS::Service|Yes|No|cmdb\_ci\_cloud\_ecs\_service|
|AWS::ECS::TaskDefinition|Yes|No|cmdb\_ci\_cloud\_ecs\_task\_definition|
|AWS::Lambda::Function|Yes|Yes|cmdb\_ci\_cloud\_function|
|AWS::ApiGateway::RestApi|Yes|Yes|cmdb\_ci\_cloud\_gateway|
|ec2:DescribeInstanceTypes|Yes|Yes|cmdb\_ci\_cloud\_hardware\_type|
|AWS::EC2::Host|Yes|No|cmdb\_ci\_cloud\_host|
|AWS::EC2::KeyPair|Yes|No|cmdb\_ci\_cloud\_key\_pair|
|AWS::ElasticLoadBalancingV2::LoadBalancer|Yes|Yes|cmdb\_ci\_cloud\_load\_balancer|
|Amazon::S3::Bucket|Yes|Yes|cmdb\_ci\_cloud\_object\_storage|
|Organizations|Yes|Yes|cmdb\_ci\_cloud\_org or cmdb\_ci\_cloud\_service\_account|
|Organizations::AWS accounts|Yes|Yes|cmdb\_ci\_cloud\_service\_account|
|AWS::EC2::Subnet|Yes|Yes|cmdb\_ci\_cloud\_subnet|
|AWS SSM agents|Yes|No|cmdb\_ci\_cloud\_system\_management\_agent|
|AWS::EC2::Subnet|Yes|No|cmdb\_ci\_cloud\_subnet|
|AWS::WAF::WebACL|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::WAFRegional::WebACL|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::ACM::Certificate|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::Redshift::EventSubscription|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::RDS::DBSnapshot|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::Redshift::ClusterParameterGroup|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::AutoScaling::LaunchConfiguration|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::Redshift::ClusterSnapshot|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::CloudFormation::Stack|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::CodeBuild::Project|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::ElasticBeanstalk::ApplicationVersion|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::Redshift::ClusterSecurityGroup|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::CloudTrail::Trail|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::CloudFront::StreamingDistribution|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::WAF::RuleGroup|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::RDS::DBSecurityGroup|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::RDS::EventSubscription|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::WAF::Rule|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::AutoScaling::ScheduledAction|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::ElasticBeanstalk::Environment|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::AutoScaling::ScalingPolicy|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::Shield::Protection|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::CloudWatch::Alarm|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::XRay::EncryptionConfig|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::ShieldRegional::Protection|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::Redshift::ClusterSubnetGroup|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::IAM::Group|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::WAFRegional::RateBasedRule|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::WAFRegional::RuleGroup|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::WAF::RateBasedRule|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::RDS::DBSubnetGroup|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::SSM::AssociationCompliance|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::EC2::SecurityGroup|Yes|Yes|cmdb\_ci\_compute\_security\_group|
|ec2:DescribeInstanceTypes|Yes|Yes|cmdb\_ci\_compute\_template|
|AWS::ECR::Repository|Yes|No|cmdb\_ci\_container\_repository|
|AWS::EC2::CustomerGateway|Yes|No|cmdb\_ci\_customer\_gateway|
|Docker container|Yes|Yes|cmdb\_ci\_docker\_container|
|ecr:DescribeImages|Yes|No|cmdb\_ci\_docker\_image|
|AWS::DynamoDB::GlobalTable|Yes|Yes|cmdb\_ci\_dynamodb\_table|
|AWS::AutoScaling::AutoScalingGroup|Yes|N/A|cmdb\_ci\_instance\_scale\_set|
|AWS::AutoScaling::AutoScalingGroup|N/A|Yes|cmdb\_ci\_cmp\_resource|
|AWS::EC2::InternetGateway|Yes|No|cmdb\_ci\_internet\_gateway|
|AWS::EKS::Cluster|Yes|Yes|cmdb\_ci\_kubernetes\_cluster|
|WS::ElasticLoadBalancingV2::TargetGroup|Yes|No|cmdb\_ci\_lb\_pool|
|AWS::ElasticLoadBalancingV2::TargetGroup TargetDescription|Yes|No|cmdb\_ci\_lb\_pool\_member|
|AWS::ElasticLoadBalancingV2::Listener|Yes|No|cmdb\_ci\_lb\_service|
|AWS::EC2::NatGateway|Yes|No|cmdb\_ci\_nat\_gateway|
|AWS::EC2::VPC|Yes|Yes|cmdb\_ci\_network|
|AWS::EC2::NetworkAcl|Yes|No|cmdb\_ci\_network\_acl|
|AWS::EC2::NetworkInterface|Yes|Yes|cmdb\_ci\_nic|
|AWS::EC2::RouteTable|Yes|No|cmdb\_ci\_route\_table|
|AWS::EC2::VolumeAttachment|Yes|Yes|cmdb\_ci\_storage\_mapping|
|AWS::EC2::Volume|Yes|Yes|cmdb\_ci\_storage\_volume|
|AWS::EC2::VPNGateway|Yes|No|cmdb\_ci\_virtual\_pvt\_gateway|
|AWS::EC2::VPNConnection|Yes|No|cmdb\_ci\_vpn\_connection|
|AWS::WAFv2::WebACL|Yes|N/A|cmdb\_ci\_web\_acl|
|AWS::WAFv2::WebACL|N/A|Yes|cmdb\_ci\_cmp\_resource|
|Tags|Yes|Yes|cmdb\_key\_value|
|Kubernetes DaemonSet|No|Yes|cmdb\_ci\_kubernetes\_daemonset|
|Kubernetes deployment|No|Yes|cmdb\_ci\_kubernetes\_deployment|
|Kubernetes namespace|No|Yes|cmdb\_ci\_kubernetes\_namespace|
|Amazon EKS node|No|Yes|cmdb\_ci\_kubernetes\_node|
|Amazon EKS pod|No|Yes|cmdb\_ci\_kubernetes\_pod|
|Amazon EKS service|No|Yes|cmdb\_ci\_kubernetes\_service|
|Kubernetes Volume|No|Yes|cmdb\_ci\_kubernetes\_volume|
|AWS::SSM::ManagedInstanceInventory|No|Yes|cmdb\_ci\_spkg|
|AWS::EC2::VPCPeeringConnection|Yes|No|cmdb\_aws\_elastic\_compute\_cloud\_vpc\_peering\_connection|
|AWS::Elastic Compute Cloud::VPC Endpoint Service|Yes|No|cmdb\_aws\_elastic\_cloud\_compute\_vpc\_endpoint\_service|
|AWS::Elastic Compute Cloud::EBS Snapshot|Yes|No|cmdb\_aws\_elastic\_cloud\_compute\_ebs\_snapshot|
|AWS::Elastic Compute Cloud::Reserved Instance|Yes|No|cmdb\_aws\_elastic\_cloud\_compute\_reserved\_instance|
|AWS::RDS::DBSnapshot|Yes|No|cmdb\_aws\_relational\_database\_services\_db\_snapshot|
|AWS::SageMaker::Training Job|Yes|No|cmdb\_aws\_sagemaker\_training\_job|
|AWS::Elastic File System::File System|Yes|No|cmdb\_aws\_elastic\_file\_system\_file\_system|
|AWS::Redshift Serverless::Namespace|Yes|No|cmdb\_aws\_redshift\_serverless\_namespace|
|AWS::Redshift Serverless::Workgroup|Yes|No|cmdb\_aws\_redshift\_serverless\_workgroup|
|AWS::Redshift Serverless::Snapshot|Yes|No|cmdb\_aws\_redshift\_serverless\_snapshot|
|AWS::ElastiCache::Snapshot|Yes|No|cmdb\_aws\_elasticache\_snapshot|
|AWS::CloudTrail::Trail|Yes|No|cmdb\_aws\_cloudtrail\_trail|
|AWS::Batch::ComputeEnvironment|Yes|No|cmdb\_aws\_batch\_compute\_environment|
|AWS::StorageGateway::FileShare|Yes|No|cmdb\_aws\_storage\_gateway\_file\_share|
|AWS::DataSync::Task|Yes|No|cmdb\_aws\_datasync\_task|
|AWS::API Gateway::Domain Name|Yes|No|cmdb\_aws\_api\_gateway\_domain\_name|
|AWS DynamoDB Cluster|Yes|No|cmdb\_ci\_cluster\_node|
|AWS::GlobalAccelerator::Accelerator|Yes|No|cmdb\_aws\_global\_accelerator\_accelerator|
|AWS::Timestream::InfluxDBInstance|Yes|No|cmdb\_aws\_timestream\_for\_influxdb\_database\_instance|
|AWS::CloudHSM::HSM|Yes|No|cmdb\_aws\_cloudhsm\_hsm|
|AWS::MWAA::Environment|Yes|No|cmdb\_aws\_managed\_workflows\_for\_apache\_airflow\_environment|
|AWS::NetworkFirewall::Firewall|Yes|No|cmdb\_aws\_network\_firewall\_firewall|

**Parent Topic:**[Service Graph Connector for AWS reference](../../configuration-management/concept/sgc-cmdb-aws-reference.md)

