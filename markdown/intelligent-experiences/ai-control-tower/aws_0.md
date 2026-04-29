---
title: AI Service Graph Connector for Amazon
description: Use the  AI Service Graph Connector for Amazon to discover AI assets such as AI systems, agents, models, tools, and prompts and well as usage data for these AI agents within your ServiceNow AI Control Tower. This usage information is consumed by the AI Control Tower value dashboard.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph Connector for Amazon

Use the  AI Service Graph Connector for Amazon to discover AI assets such as AI systems, agents, models, tools, and prompts and well as usage data for these AI agents within your ServiceNow AI Control Tower. This usage information is consumed by the AI Control Tower value dashboard.

## Download apps from the Store

Visit the  [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to download the AI Service Graph Connector for Amazon app.

## Supported ServiceNow versions

-   Australia
-   Zurich patch 7
-   Yokohama patch 11

## User roles

Roles required in the ServiceNow environment:

-   sn\_ai\_disc.discovery\_admin
-   sn\_cmdb\_int\_util.sgc\_admin

## Prerequisites from AWS

Role required: IAM user

**AWS Prerequisites**

Before proceeding, ensure you have:

-   AWS Account- Active AWS account with access to the services you want to connect.
-   IAM Credentials: AWS Access Key ID and Secret Access Key with read permissions for the services you plan to migrate.
-   Service Access- API access enabled for Amazon Bedrock, Amazon SageMaker, Amazon CloudWatch, and/or Amazon Bedrock AgentCore.

**Required IAM Permissions**

Your IAM user role or role needs these permissions.

-   Amazon Bedrock: bedrock:List\*, bedrock:Get\*
-   Amazon SageMaker: sagemaker:List\*, sagemaker:Describe\*
-   Amazon CloudWatch: logs:DescribeLogGroups, logs:DescribeLogStreams, cloudwatch:GetMetricData
-   Amazon Bedrock AgentCore: bedrock:ListAgents, bedrock:GetAgent

**AWS Setup documentation**

Use these AWS resources to set up credentials and enable services:

-   [AWS IAM- Managing Access Keys](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)
-   [Amazon Bedrock- Setting Up](https://docs.aws.amazon.com/bedrock/latest/userguide/setting-up.html)
-   [Amazon Bedrock Agents- Setup Guide](https://docs.aws.amazon.com/bedrock/latest/userguide/agents-setup.html)
-   [Amazon CloudWatch- Setup Guide](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/GettingSetup.html)
-   [Amazon SageMaker- Get Started](https://docs.aws.amazon.com/sagemaker/latest/dg/gs.html)

## Data mapping

The following table lists the data sources, the staging tables, and the target tables  CMDB CI classes and non-CMDB  classes where data is stored for a  AWS  project.

<table id="table_jc1_m2r_l3c"><tbody><tr><td>

**Data Source**

</td><td>

**Staging Table**

</td><td>

**Target Table**

</td></tr><tr><td>

SGawsBedrockAIAssetDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_bedrock\_ai\_asset

</td><td>

sn\_ai\_disc\_aws\_sgc\_bedrock\_ai\_system \(routes to other staging tables\)

</td></tr><tr><td>

SGawsBedrockAISystemDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_bedrock\_ai\_system

</td><td>

alm\_ai\_system\_digital\_asset

</td></tr><tr><td>

SGawsBedrockAIModelDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_bedrock\_ai\_model

</td><td>

alm\_ai\_model\_digital\_asset

</td></tr><tr><td>

SGawsBedrockAIToolDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_bedrock\_ai\_tool

</td><td>

sn\_ent\_ai\_tool

</td></tr><tr><td>

SGawsBedrockAIPromptDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_bedrock\_ai\_prompt

</td><td>

alm\_ai\_prompt\_digital\_asset

</td></tr><tr><td>

SGawsBedrockAISbcompM2mDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_bedrock\_sbcomp\_m2m

</td><td>

sn\_ent\_ai\_system\_subcomponent\_m2m

</td></tr><tr><td>

SGawsBedrockAIUsageDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_bedrock\_ai\_usage

</td><td>

sn\_ai\_disc\_ai\_usage

</td></tr><tr><td>

SGAgentCoreDataSourceUtil \(importAgentRuntimesByID\)

</td><td>

sn\_ai\_disc\_aws\_sgc\_agentcore\_ai\_system

</td><td>

alm\_ai\_system\_digital\_asset

</td></tr><tr><td>

SGAgentCoreDataSourceUtil \(importCodeInterpretersByID, importBrowsersByID, importTargetsByID\)

</td><td>

sn\_ai\_disc\_aws\_sgc\_agentcore\_ai\_tool

</td><td>

sn\_ent\_ai\_tool

</td></tr><tr><td>

SGAgentCoreDataSourceUtil \(getAWSAgentCoreUsage\)

</td><td>

sn\_ai\_disc\_aws\_sgc\_agentcore\_ai\_usage

</td><td>

sn\_ai\_disc\_ai\_usage

</td></tr><tr><td>

SGSageMakerAIModelDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_sg\_awssagemaker\_model

</td><td>

alm\_ai\_model\_digital\_asset

</td></tr><tr><td>

SGSageMakerModelCardDSUtilSNC

</td><td>

sn\_ai\_disc\_aws\_sgc\_sg\_awssagemaker\_model

</td><td>

alm\_ai\_model\_digital\_asset

</td></tr></tbody>
</table>