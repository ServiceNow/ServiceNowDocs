---
title: Add an AWS CloudWatch trace connection
description: Monitor AI agents built with AWS Bedrock AgentCore by adding an AWS CloudWatch trace connection. AI Control Tower collects trace data through your AWS credentials and a MID Server, without requiring SDK instrumentation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-configure-aws-cloudwatch-trace.html
release: australia
topic_type: task
last_updated: "2026-06-30"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring trace connections, Configuring integrations, Configure, AI Control Tower, Enable AI experiences]
---

# Add an AWS CloudWatch trace connection

Monitor AI agents built with AWS Bedrock AgentCore by adding an AWS CloudWatch trace connection. AI Control Tower collects trace data through your AWS credentials and a MID Server, without requiring SDK instrumentation.

## Before you begin

Confirm the following:

-   Your AI agents are built using AWS Bedrock AgentCore.
-   Tracing is enabled for each AWS Bedrock AgentCore agent you want to monitor.
-   An active MID Server is installed and configured in your ServiceNow instance. See [MID Server installation](https://www.servicenow.com/docs/r/servicenow-platform/mid-server/mid-server-installation.html).
-   An AWS access key ID and secret access key with permission to read trace data from CloudWatch is available.
    -   This connector supports access key authentication only. Connections using an assumed role or external ID aren't currently supported.
    -   The access key must be created and its IAM policy configured in AWS. For details, see the [Work Instruction \| How to Create AWS Credentials on a Glide Instance \[KB3143433\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3143433) article in Now Support.
    -   After the access key ID and secret access key are created, work with your instance administrator to store them as a new AWS credential record in **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.
-   You know the AWS region where your AI agents are deployed, such as `us-east-2`.

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Integrations** &gt; **Traces**.

2.  On the **Available** sub-tab, select **AWS CloudWatch**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|Descriptive name for this trace connection. Use a name that distinguishes this connection from others you create, such as one that identifies the account, project, or environment.|
    |**Collection frequency \(minutes\)**|Interval, in minutes, at which the MID Server polls for new trace data. The default is 30. Set a lower value to return results sooner or set a higher value to reduce overhead for lower-volume systems.|
    |**Region**|AWS region where your AI agents are deployed, such as `us-east-2`.|
    |**Credential**|AWS credential that authenticates AI Control Tower to CloudWatch. The credential must have permission to read trace data.|
    |**MID server**|MID Server that runs trace collection. The MID Server must be active and validated. Select **Go to Mid server installation** to install or configure one.|
    |**Log group source**|AWS CloudWatch log group that this connection collects trace data from. Select **Agent Core Log Group** to collect from the log group used by agents built with AWS Bedrock AgentCore. Select **Other Log Groups** to collect from a different log group. Select both to create a separate connection for each.|
    |**Active**|Option to begin collecting traces when you save the connection. Clear it to save the connection without starting collection. You can activate the connection later from its record.|

4.  Select **Save**.


## Result

One or more trace connections appear on the **Established** sub-tab. If you selected both log group options, two connections appear, distinguished by a log group suffix on the connection name. If a connection is active, AI Control Tower begins collecting trace data after the first polling interval.

## What to do next

Choose which metrics to include in evaluation scoring. See [Activate evaluation scoring for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-monitor-external-ai-system.md).

**Parent Topic:**[Configuring trace connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-trace-connections.md)

