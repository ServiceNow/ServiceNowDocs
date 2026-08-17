---
title: Configure overview security metrics
description: If you have external AI agent data you want reflected in the Privileged AI agents metric, set up a Traceloop connection to the external AI server and perform other setup to make sure agent data appears in the metric. Or, set up a static connection for Amazon Web Services \(AWS\) or Azure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-sec-configure-overview.html
release: australia
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Managing AI asset security, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Configure overview security metrics

If you have external AI agent data you want reflected in the Privileged AI agents metric, set up a Traceloop connection to the external AI server and perform other setup to make sure agent data appears in the metric. Or, set up a static connection for Amazon Web Services \(AWS\) or Azure.

## Before you begin

Role required: AI Control Tower admin \[sn\_ai\_observe.ai\_observability\_admin\]

## About this task

You can configure your data connection for the Privileged AI agents metric using trace-based analysis configuration which connects to any third-party AI system vendor. A trace-based configuration is more dynamic than a static analysis configuration.

Or, you can configure your connection using the static analysis configuration, which is more deterministic than a trace-based configuration. Only Azure and AWS connections are supported.

## Static \(metadata-based\) analysis configuration \(AWS and Azure only\)

Azure Foundry AI agents shown in the Privileged AI agents metric are agents whose project identities hold high-risk Azure roles \(owner, contributor, or custom-defined roles\). There are two default Azure privileged roles: owner and contributor. If you have other high-risk Azure roles, you can add them to a privileged role definitions list so that AI Control Tower can monitor and surface agent data tied to those roles in the Privileged AI agents metric.

As a prerequisite, in Azure set up a connection alias named “Azure IAM for AICT-AISP” with credentials that have read access to Azure Management APIs.

**Note:** The service principal used for the credential must have read access to query Azure role definitions and role assignments. Specifically, Microsoft.Authorization/roleAssignments/read and Microsoft.Authorization/roleDefinitions/read.

You can also show AWS Bedrock AI agents in the Privileged AI agents metric. As prerequisites, you must have an AWS account configured for your instance, enable AiSP AWS IAM Privileged Policy Checker, and add its connection for AWS. Also, confirm the following are in place:

-   An active MID Server installed and configured in your ServiceNow instance.
-   Cloud credentials for authenticating ServiceNow to your cloud provider.
-   The AWS region where your AI agents are deployed.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Settings** &gt; **Integrations** &gt; **Traces**.

2.  Select **Add**.

3.  Select your cloud provider, then select **Continue**.

    Supported cloud providers:

    -   AWS AgentCore
    -   Azure Foundry
4.  Fill in the trace connection fields.

    |Field|Description|
    |-----|-----------|
    |Name|Descriptive name for this trace connection. Used when reviewing collection status, troubleshooting, or managing multiple connections.|
    |Credential|Cloud provider credentials for authenticating trace collection. If the credential does not appear in the list, verify it has been created in the ServiceNow Credentials module.|
    |Collection frequency \(minutes\)|Interval, in minutes, at which the MID Server polls the cloud provider to collect new trace data. Collecting traces more frequently increases cost.|
    |MID Server|MID Server that executes trace collection from the cloud provider. The MID Server must have a status of **Active** and be validated before proceeding.|
    |AWS region|AWS region where your AI agents are deployed. Applies to AWS AgentCore connections only.|

5.  Select **Save**.


**Parent Topic:**[Configuring security metrics in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configuring.md)

## Trace-based analysis configuration \(vendor-agnostic\)

### Before you begin

Role required: AI Control Tower admin \[sn\_ai\_observe.ai\_observability\_admin\]

External AI systems require trace data so it can be shown in the Privileged AI agents metric. Unlike ServiceNow AI systems, which are automatically instrumented, external AI systems must be connected to send trace data to AI Control Tower.

There are two ways to establish this connection:

-   SDK instrumentation: Instrument your AI agent code using the Traceloop SDK and authenticate with an API key. Use this method for any third-party AI agent framework that is not hosted on a supported cloud hyperscaler.
-   Hyperscaler trace connection: Connect directly to AWS, GCP, or Azure through cloud credentials and a MID Server. Use this method when your AI agents run on a supported cloud platform. No API key or code instrumentation is required.

### Procedure

1.  Configure a trace connection for your external AI system.

    For more information, see [Configuring trace connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-trace-connections.md).

2.  Generate an API key to authenticate trace data requests from your external AI system.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Create credentials of type **API Key Credentials**.

        Fill out these fields and select **Submit**.

        |Field|Description|
        |-----|-----------|
        |Name|Traceloop API Key|
        |Applies to|All MID servers|
        |Active|Selected.|
        |Order|100|
        |API Key Header|Authorization|
        |API Key Prefix|Bearer|
        |API Key|\[Your Traceloop API key\]|
        |Credential alias|Locked.|

    For more information, see [API key credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/API-key-credential-form.md).

3.  Link the API key to your trace connection.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections**.

    2.  From the connections list, select the **Traceloop Warehouse** connection.

        Fill out these fields and select **Update**.

        |Field|Description|
        |-----|-----------|
        |Name|Traceloop Warehouse|
        |Active|Selected.|
        |Credential|Traceloop API Key \(from step 2b\)|
        |Domain|global|
        |Connection alias|sn\_ai\_security.Traceloop\_API|
        |URL builder|N/A|
        |Connection URL|https://api.traceloop.com|
        |Use MID server|N/A|
        |Connection timeout|N/A|

        The scheduled job will now automatically pull privileged AI agent data from the linked Traceloop environment.

    For more information, see [Create an HTTP\(s\) connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/create-https-connection.md).

4.  Configure the Traceloop SDK in your agent code by adding these ServiceNow attributes when initializing Traceloop.

    These are unique user-defined identifiers for tracking.

    ```
    Traceloop.init(
        app_name="your_agent_name",
        api_key=traceloop_api_key,
        resource_attributes={
            "sn.aict.system.id": "your_agent_system_id",
            "sn.aict.system.name": "your_agent_name",
            "sn.aict.system.version": "1.0.0",
            "sn.aict.system.source": "your_source"
        }
    )
    ```

    For more information about configuring Traceloop in your agent, see [Traceloop - Guardrails](https://www.traceloop.com/docs/evaluators/guardrails).

5.  Make sure that the AiSP AWS IAM Privileged Policy Checker AI skill is enabled.

    For more information, see [Activate an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-a-now-assist-skill.md).

6.  To add custom roles for Azure Foundry agents, navigate to **All** &gt; **AI Security and Privacy** &gt; **Privileged Role Definitions**.

    1.  In the External Role ID field, enter the Azure role name of the custom role that your organization considers to be privileged.

    2.  Select **Update**.

    Return to the AI Control Tower Security tab and refresh the page. Select the Overview tab and verify that Privileged AI agents metric is populated.


