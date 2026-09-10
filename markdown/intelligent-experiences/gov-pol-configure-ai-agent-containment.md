---
title: Configure automatic AI agent containment
description: Connect an identity provider and the AI agent runtime platforms to AI Control Tower so a Threat Response policy can automatically contain an AI agent using kill switch protocol.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-pol-configure-ai-agent-containment.html
release: australia
topic_type: task
last_updated: "2026-08-31"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI, Policies, Threat Response, Control Enforcement Points, kill switch protocol]
breadcrumb: [Configure, Controlling AI asset usage, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Configure automatic AI agent containment

Connect an identity provider and the AI agent runtime platforms to AI Control Tower so a Threat Response policy can automatically contain an AI agent using kill switch protocol.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

To let a Threat Response policy automatically contain an AI agent using kill switch protocol, you must have:

-   A connection between AI Control Tower and each AI agent runtime or infrastructure platform that hosts the agents the policy covers. These connectors are supported:
    -   AWS Bedrock
    -   AWS Bedrock Agent Core
    -   Gemini Enterprise Agent Platform \(agents with unique identities only\)
    -   Azure AI Foundry
    -   ServiceNow Agents
    -   Agent Client Collector \(ACC\)
-   A connection between AI Control Tower and an identity provider is optional. Okta is supported.

## Procedure

1.  Navigate to **AI Control Tower** &gt; **Settings** &gt; **Integrations** &gt; **Control Enforcement Points**.

2.  Select the connector from the **Available connectors** sub-tab and follow the guided setup wizard.

    For more information, see [Configuring security connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-security-connections.md).


## Result

You can now create a Threat Response policy that automatically contains an AI agent using kill switch protocol on the connected platforms. For details, see [Create a Threat Response policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-pol-create-threat-response-policy.md).

