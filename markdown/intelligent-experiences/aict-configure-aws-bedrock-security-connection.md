---
title: Add an AWS Bedrock or AWS Bedrock Agent Core connection
description: Connect AWS Bedrock or AWS Bedrock Agent Core to AI Control Tower so AI agent containment using kill switch protocol can reach and deactivate agents running on AWS.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-configure-aws-bedrock-security-connection.html
release: australia
topic_type: task
last_updated: "2026-07-29"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring security connections, Configuring integrations, Configure, AI Control Tower, Enable AI experiences]
---

# Add an AWS Bedrock or AWS Bedrock Agent Core connection

Connect AWS Bedrock or AWS Bedrock Agent Core to AI Control Tower so AI agent containment using kill switch protocol can reach and deactivate agents running on AWS.

## Before you begin

Confirm the following:

-   You have an AWS Identity and Access Management \(IAM\) service account with the permissions required for the connector you're configuring:
    -   For **AWS Bedrock Agent Core**, in the `bedrock-agentcore:` namespace on `runtime/*` resources: `GetResourcePolicy`, `PutResourcePolicy`, `DeleteResourcePolicy`.
    -   For **AWS Bedrock Agent** \(classic\), in the `bedrock:` namespace on `agent/*` and `agent-alias/*` resources: `ListAgentAliases`, `UpdateAgentAlias`, `TagResource`, `UntagResource`, `ListTagsForResource`.
-   The AWS access key ID and secret access key for that service account are available.

Role required: sn\_ai\_governance.ai\_steward

## About this task

Adding this connection has two parts: first you create a Connection &amp; Credential Alias that stores your AWS credentials, then you attach that alias to the security connector in AI Control Tower.

## Procedure

1.  Navigate to **Connection &amp; Credential Aliases** \(`sys_alias.list`\).

2.  Select **New**, set **Type** to **Credential**, and select **Submit**.

3.  In the resulting alias record, create a credential and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Credential type**|Select **AWS Credentials**.|
    |**AWS Access Key**|Access key ID for the AWS service account.|
    |**Secret Key**|Secret access key for the AWS service account.|
    |**Auth algorithm**|Select **Amazon Bedrock AgentCore AICT-AiSP** if you're configuring AWS Bedrock Agent Core, or **Amazon Bedrock Agent AICT-AiSP** if you're configuring AWS Bedrock Agent \(classic\).|

4.  Select **Submit**.

    The Connection &amp; Credential Alias record now has this credential attached.

5.  Navigate to **AI Control Tower** &gt; **Settings** &gt; **Integrations** &gt; **Security**.

6.  On the **Available connectors** sub-tab, select **AWS Bedrock Agent Core** or **AWS Bedrock**, matching the auth algorithm you selected earlier.

7.  Fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|Unique, descriptive name for this connection.|
    |**Connection Alias**|The Connection &amp; Credential Alias record you created in the previous steps.|
    |**Active**|Select this option.|

8.  Select **Submit**.


## Result

The connector appears on the **Established connections** sub-tab. AI Control Tower can now use this connection to apply AI agent containment using kill switch protocol to agents running on the connected AWS Bedrock or AWS Bedrock Agent Core service.

**Parent Topic:**[Configuring security connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-security-connections.md)

