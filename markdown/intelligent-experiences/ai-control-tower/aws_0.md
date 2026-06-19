---
title: AI Service Graph Connector for Amazon
description: The AI Service Graph Connector for Amazon enables you to discover and import AI assets from your AWS environment into ServiceNow AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/aws\_0.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph Connector for Amazon

The AI Service Graph Connector for Amazon enables you to discover and import AI assets from your AWS environment into ServiceNow AI Control Tower.

The connector integrates with your AWS account to catalog AI systems, agents, models, and prompts. Usage data is automatically collected and populated into the AI Control Tower value dashboard, providing comprehensive visibility and governance of your AI operations.

## Download apps from the Store

Visit the  ServiceNow store website to download the [AI Service Graph Connector for Amazon](https://store.servicenow.com/store/app/74d7378e47a73a50cbbce551336d4356) application.

## Supported ServiceNow versions

This connector is supported on the following ServiceNow releases:

|Release|Status|
|-------|------|
|Australia|Supported|
|Zurich|Supported|
|Yokohama|Supported|

## User Roles

You must have one of the following roles assigned.

|Required Roles|
|--------------|
|sn\_ai\_disc.discovery\_admin|
|sn\_cmdb\_int\_util.sgc\_admin|

## ServiceNow Prerequisites

Complete the following setup steps once when configuring the connector for the first time.

**Note:** Updating data source access and clear cache is a prerequisite that needs to be completed only once, when setting up a new instance for the first time.

Update Data Source Access

The connector requires write permissions to the Data Source table to create data sources.

To enable data source creation:

1.  Select Global from the application picker.
2.  Navigate to Application Access.
3.  Select the Can create, Can update, and Can delete checkboxes.
4.  Select Update.
5.  Switch to the connector application scope.

Clear cache

Clear the cached data for the Data Source and Tables.

To clear the cache:

1.  Navigate to System Definition &gt; Background Scripts
2.  Paste the following script into the Run Script text box:

    ```
    GlideTableManager.invalidateTable('sys_data_source');
    GlideCacheManager.flushTable('sys_data_source');
    GlideTableManager.invalidateTable('sys_db_object');
    GlideCacheManager.flushTable('sys_db_object');
    
    ```

3.  Select Run Script.

    **Note:** The script may take several minutes to complete.

4.  After completion, switch to the connector application scope.

## AWS Prerequisites

Role required: IAM user

Before proceeding, confirm you have:

-   AWS Account- Active AWS account with access to the services you want to connect
-   IAM Credentials: AWS Access Key ID and Secret Access Key with read permissions for the services you plan to migrate
-   Service Access- API access enabled for Amazon Bedrock, Amazon SageMaker, Amazon CloudWatch, and Amazon Bedrock AgentCore

Required IAM Permissions

Your IAM user role or role needs these permissions.

-   Amazon Bedrock: bedrock:List\*, bedrock:Get\*
-   Amazon SageMaker: sagemaker:List\*, sagemaker:Describe\*
-   Amazon CloudWatch: logs:DescribeLogGroups, logs:DescribeLogStreams, cloudwatch:GetMetricData
-   Amazon Bedrock AgentCore: bedrock:ListAgents, bedrock:GetAgent

AWS Setup documentation

Use these AWS resources to set up credentials and enable services:

-   [AWS IAM- Managing Access Keys](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)
-   [Amazon Bedrock- Setting Up](https://docs.aws.amazon.com/bedrock/latest/userguide/setting-up.html)
-   [Amazon Bedrock Agents- Setup Guide](https://docs.aws.amazon.com/bedrock/latest/userguide/agents-setup.html)
-   [Amazon CloudWatch- Setup Guide](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/GettingSetup.html)
-   [Amazon SageMaker- Get Started](https://docs.aws.amazon.com/sagemaker/latest/dg/gs.html)

## Data Mapping

The following table lists the data sources, the staging tables, and the target tables  CMDB CI classes and non-CMDB  classes where data is stored for a  AWS  project.

<table id="table_jc1_m2r_l3c"><tbody><tr><td>

Data Source

</td><td>

Staging Table

</td><td>

Target Table

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