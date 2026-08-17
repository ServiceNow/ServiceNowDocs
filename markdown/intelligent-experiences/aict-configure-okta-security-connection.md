---
title: Add an Okta connection
description: Connect Okta to AI Control Tower so that AI agent containment with kill switch protocol prevents future tokens from being issued to a deactivated AI agent. If your AI agent is on ServiceNow or AWS Bedrock, the agent's identity is federated through Okta.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-configure-okta-security-connection.html
release: australia
topic_type: task
last_updated: "2026-07-29"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring security connections, Configuring integrations, Configure, AI Control Tower, Enable AI experiences]
---

# Add an Okta connection

Connect Okta to AI Control Tower so that AI agent containment with kill switch protocol prevents future tokens from being issued to a deactivated AI agent. If your AI agent is on ServiceNow or AWS Bedrock, the agent's identity is federated through Okta.

## Before you begin

Confirm the following:

-   You have an Okta tenant with admin access to generate an API token.
-   A security connection is already established for the platform hosting the AI agent — AWS Bedrock, AWS Bedrock Agent Core, or ServiceNow Agents. An Okta connection extends containment for agents whose identity is federated through one of those platforms; it doesn't replace the platform connection. See [Add an AWS Bedrock or AWS Bedrock Agent Core connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-aws-bedrock-security-connection.md) or [Add a ServiceNow Agents connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-servicenow-agents-security-connection.md).
-   The AI agents you want covered are actively configured on the Okta tenant — in other words, their identity is federated through Okta.

Role required: Creating the Connection Alias, credential, and HTTP connection in steps 1–3 below typically requires an instance admin or integration admin role. Creating the security connector in steps 4–6 requires sn\_ai\_governance.ai\_steward.

## About this task

An Okta connection is optional but strengthens how AI agent containment using kill switch protocol works. Without Okta configured, deactivating an agent relies on Deny Resource policies applied directly on the hyperscaler platform, which is enough to fully disable the agent on its own.

When Okta is configured and the agent's identity is federated through Okta, deactivating the agent additionally prevents future tokens from being assigned to it.

## Procedure

1.  Create the Connection Alias.

    Navigate to **Connection &amp; Credential Aliases** \(`sys_alias.list`\) and select **New**.

    |Field|Description|
    |-----|-----------|
    |**Name**|Descriptive name, such as `Okta Identity Sync Alias`.|
    |**Type**|Select **Connection**.|
    |**Connection Type**|Select **HTTP Connection**.|
    |**Is Internal**|Clear this option.|
    |**Multiple Connections**|Clear this option.|
    |**Retry Policy**|Select **Default HTTP Retry Policy**.|
    |**Application / Scope**|Select **AI Security and Privacy**.|

    Select **Submit**.

2.  Create the API key credential.

    Navigate to **Credentials** \(`discovery_credentials.list`\), select **New**, and choose credential type **API Key Credentials**.

    |Field|Description|
    |-----|-----------|
    |**Name**|Descriptive name, such as `Okta SSWS Token - <your_okta_tenant_name>`.|
    |**Active**|Select this option.|
    |**Type**|Select **API Key**.|
    |**API Key**|Your Okta API token.|
    |**API Key Prefix**|`SSWS`.|
    |**Application**|Select **AI Security and Privacy**.|

    **Note:** The `SSWS` prefix is automatically prepended to the token in the Authorization header. Don't include `SSWS` in the API Key field itself.

    Select **Submit**.

3.  Create the HTTP connection.

    Navigate to **HTTP Connections** \(`http_connection.list`\), or select **New** from the **Connections** related list on the Connection Alias record you created earlier.

    |Field|Description|
    |-----|-----------|
    |**Name**|Descriptive name, such as `Okta Dev Tenant - <your_okta_tenant_name>`.|
    |**Active**|Select this option.|
    |**Connection URL**|`https://<your_okta_tenant>.oktapreview.com`|
    |**Connection Alias**|The Connection Alias record from the first step.|
    |**Credential**|The API key credential from the previous step.|
    |**Protocol**|**https**|
    |**Host**|`<your_okta_tenant>.oktapreview.com`|
    |**Application Scope**|Select **AI Security and Privacy**.|
    |**Use MID**|Clear this option.|
    |**MID Selection**|Select **Auto select**.|
    |**Mutual Auth**|Clear this option.|

    Select **Submit**.

4.  Navigate to **AI Control Tower** &gt; **Settings** &gt; **Integrations** &gt; **Security**.

5.  On the **Available security connectors** sub-tab, select **Okta**.

6.  In the **Configure connector** panel, fill in the fields and select **Submit**.

    |Field|Description|
    |-----|-----------|
    |**Name**|Unique, descriptive name for this connection, such as `Okta - Dev Tenant`.|
    |**Provider Type**|Select **Okta**.|
    |**Connection Alias**|The Connection Alias you created in the first step.|
    |**Active**|Select this option.|


## Result

The connector appears on the **Established connections** sub-tab. If Okta deactivation is skipped and only hyperscaler deactivation is performed, the AI agent is still effectively disabled; the Okta connection adds token-level containment on top of that.

To verify the setup:

-   Open the Connection Alias record and confirm the HTTP connection appears in its **Connections** related list.
-   Optionally, test the connection with a GET request to `https://<tenant>.oktapreview.com/api/v1/ai-agents?limit=200` using the alias, and confirm a `200 OK` response.

**Parent Topic:**[Configuring security connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-security-connections.md)

