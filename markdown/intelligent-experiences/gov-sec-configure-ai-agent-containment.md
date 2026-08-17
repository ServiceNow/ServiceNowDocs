---
title: Configure AI agent containment
description: Connect identity providers and hyperscalers to ServiceNow to let you contain and enforce guardrails for AI assets at runtime using kill switch protocol.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/gov-sec-configure-ai-agent-containment.html
release: zurich
topic_type: task
last_updated: "2026-07-21"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Managing AI asset security, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Configure AI agent containment

Connect identity providers and hyperscalers to ServiceNow to let you contain and enforce guardrails for AI assets at runtime using kill switch protocol.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\]

## About this task

To deactivate or reinstate an AI agent using kill switch protocol, you must have:

-   A connection between ServiceNow and each hyperscaler that hosts governed AI assets. These connectors are supported:
    -   AWS Bedrock
    -   AWS Bedrock Agent Core
    -   GCP Vertex AI \(agents with unique identities only\)
    -   ServiceNow Agents
-   A connection between ServiceNow and an identity provider is optional. Okta is supported.

## Procedure

1.  In AI Control Tower, navigate to **Settings** &gt; **Integrations** &gt; **Connectors** &gt; **Security**.

2.  Select the connector from the Available connectors view and follow the guided setup wizard.

    For more information, see [Configuring security connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configuring-security-connections.md).

3.  If you want to manage only ServiceNow AI agents, select ServiceNow Agents from the Established connectors view and follow the guided setup wizard.

4.  After you set up connectors, navigate to the **Security** tab and refresh the page.


## Result

You can now deactivate and reinstate AI agents using kill switch protocol. For more information, see [Manage AI agents using kill switch protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-manage-ai-agents-using-kill-switch-protocol.md).

**Parent Topic:**[Configuring security metrics in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configuring.md)

