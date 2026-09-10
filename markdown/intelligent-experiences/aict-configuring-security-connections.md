---
title: Configuring security connections
description: Connect AI Control Tower to the platforms where your AI agents run and to your identity provider so that policies and AI agent containment using kill switch protocol can act on agents wherever they're hosted.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-configuring-security-connections.html
release: australia
topic_type: concept
last_updated: "2026-07-29"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring integrations, Configure, AI Control Tower, Enable AI experiences]
---

# Configuring security connections

Connect AI Control Tower to the platforms where your AI agents run and to your identity provider so that policies and AI agent containment using kill switch protocol can act on agents wherever they're hosted.

## Key benefits

-   Connect AI Control Tower to these platforms that host your AI agents: Agent Client Collector \(ACC\), AWS Bedrock, AWS Bedrock Agent Core, Gemini Enterprise Agent Platform, Azure AI Foundry, and ServiceNow Agents. Also, you can use Okta as an identity provider, so policy and containment actions can reach agents no matter where they run.
-   Deactivate an AI agent through Deny Resource policies applied directly on the hyperscaler platform, without requiring a separate identity provider connection.
-   Add an Okta connection to strengthen containment: when an agent's identity is federated through Okta, deactivating the agent also prevents future tokens from being issued to it.

## Security connections and AI agent containment

A security connection authenticates AI Control Tower to the platform or identity provider where an AI agent runs, so that policies and AI agent containment using kill switch protocol can act on that agent. Each connector uses a different authentication model — access key credentials for AWS Bedrock and AWS Bedrock Agent Core, OAuth 2.0 with a JWT Bearer grant for Gemini Enterprise Agent Platform, an Azure AD app registration for Azure AI Foundry, and an API key for Okta — but every connector ultimately creates a security connector record that appears under the **Established connections** tab.

Behind the scenes, AI agent containment is enforced differently depending on which connections you have in place:

-   On a supported hyperscaler platform \(AWS, Gemini Enterprise Agent Platform, and ServiceNow\), deactivating an AI agent using kill switch protocol applies a Deny Resource policy directly on that platform. This alone is enough to fully disable the agent.
-   On Azure AI Foundry, deactivating an AI agent using kill switch protocol disables the agent application directly through the Azure Resource Manager API, rather than applying a Deny Resource policy.
-   If you also add an Okta connection, and the AI agent's identity is federated through Okta \(AWS Bedrock, AWS Bedrock Agent Core, Gemini Enterprise Agent Platform, and ServiceNow Agents\), deactivating the agent additionally prevents future tokens from being assigned to it.

**Important:** AI agent containment for Gemini Enterprise Agent Platform agents is supported only for agents that have a unique agent identity configured. See [Add a Gemini Enterprise Agent Platform connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-gcp-vertex-ai-security-connection.md).

-   **[Add an AWS Bedrock or AWS Bedrock Agent Core connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-aws-bedrock-security-connection.md)**  
Connect AWS Bedrock or AWS Bedrock Agent Core to AI Control Tower so policies and AI agent containment using kill switch protocol can reach and act on agents running on AWS.
-   **[Add an Azure AI Foundry connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-azure-foundry-security-connection.md)**  
Connect Azure AI Foundry to AI Control Tower so that policies and AI agent containment using kill switch protocol can reach and act on agents running on Azure AI Foundry.
-   **[Add a Gemini Enterprise Agent Platform connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-gcp-vertex-ai-security-connection.md)**  
Connect Gemini Enterprise Agent Platform to AI Control Tower using a service account and OAuth 2.0 JWT Bearer authentication, so policies and AI agent containment using kill switch protocol can reach and act on agents running on Gemini Enterprise Agent Platform.
-   **[Add an Okta connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-okta-security-connection.md)**  
Connect Okta to AI Control Tower so that policies and AI agent containment with kill switch protocol prevent future tokens from being issued to a deactivated AI agent. If your AI agent is on ServiceNow or AWS Bedrock, the agent's identity is federated through Okta.
-   **[Add an Agent Client Collector \(ACC\) connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configure-acc-cep.md)**  
Block and unblock AI usage on managed devices by configuring Agent Client Collector \(ACC\) as a control enforcement point.

**Parent Topic:**[Configuring integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-integrations.md)

