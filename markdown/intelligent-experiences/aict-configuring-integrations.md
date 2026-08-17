---
title: Configuring integrations
description: Connect AI Control Tower to external AI platforms so you can discover AI assets, collect trace data for monitoring, and synchronize governance across multiple ServiceNow instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-configuring-integrations.html
release: zurich
topic_type: concept
last_updated: "2026-06-29"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI, integrations, connectors, traces, multi-instance, security]
breadcrumb: [Configure, AI Control Tower, Enable AI experiences]
---

# Configuring integrations

Connect AI Control Tower to external AI platforms so you can discover AI assets, collect trace data for monitoring, and synchronize governance across multiple ServiceNow instances.

## Connectors

Connectors let you discover AI assets from external cloud hyperscalers and SaaS applications and bring them into your AI asset inventory. When you establish a connector, AI Control Tower periodically scans the connected platform, discovers AI assets, and adds them to your inventory as unmanaged assets. You can then review the discovered assets and move them to a managed state.

The **Connectors** tab has two views: **Available connectors**, which lists the platforms you can connect to, and **Established connections**, which lists your active and inactive connections. Each established connection shows the source system, the connection state, and the processing state.

To set up a new connector, select a platform from the Available connectors view and follow the guided setup wizard. Each connector has provider-specific prerequisites, which are linked from the first step of the wizard.

## Traces

Trace connections let you collect observability data from external AI systems and route it into AI Control Tower for quality and safety monitoring. When you establish a trace connection to a supported platform, AI Control Tower collects trace data at a configurable frequency and makes it available on the **Monitor** tab of AI asset records and in the Monitoring overview.

The information collected from traces is entered into the inventory for discovery. It is also sent to the observability service within ServiceNow, which generates evaluation metrics and security metrics.

Trace connections are the recommended route for collecting observability data from supported platforms. For external AI systems hosted on unsupported platforms or third-party agents, you can send trace data to AI Control Tower using the API instead. For a comparison of both methods and the list of supported platforms, see [Configuring trace connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configuring-trace-connections.md).

## Multi-instance

Multi-instance setup lets a production \(manager\) instance control, manage, and communicate with multiple sub-prod \(managed\) instances for AI Control Tower. When multi-instance management is configured, the production instance synchronizes AI asset data, governance rules, and configuration preferences across connected sub-prod instances so that governance stays consistent across your ServiceNow environment.

**Note:** Starting with the May 2026 release, verify that both the prod and sub-prod instances are running the same AI Control Tower core version \(6.2.4\), which is the minimum supported version.

If there’s any upgrade to version 6.2.4 in a sub-prod, then it’s advisable to upgrade the prod instance to 6.2.4 to confirm Multi-instance functions correctly.

Multi-instance setup synchronizes the following:

-   AI inventory information, including AI systems, AI models, prompts, data sets, and AI agents across connected instances

    **Note:** State of the assets while configuring Multi-instance management.

    The AI inventory in production reflects the true state of your assets like models, datasets, or skills from a production standpoint. Even if a model or dataset is active in a sub prod \(lower\) environment, it's still considered as under development from a prod perspective, since it's being tested and not yet live.

    For this reason, you don’t synchronize asset states across environments. An asset’s state changes to deployed only when the asset and its related records are activated in the production system.

    In summary, the state represents the overall lifecycle of the asset, not its local status in a specific environment.

-   Data sharing preferences from the production instance to all sub-prod instances, when enabled
-   Data overflow processing and bursting preferences from the production instance to all sub-prod instances, when enabled

Asset states aren't synchronized across environments. An asset that is active in a sub-prod environment is still considered under development from the production perspective. An asset's state changes to deployed only when the asset and its related records are activated in the production system.

When multi-instance management is configured, all synchronizable preferences on sub-prod instances is set to read-only.

**Note:** Multi-instance management is not supported on Government Community Cloud \(GCC\) or on-premises instances. The `com.glide.mif.mtls` plugin must be active before you configure multi-instance management. If the plugin is not active, submit a support request with Customer Service and Support for MIF features.

## Security

Connectors in the Security tab let you monitor and enforce guardrails for AI assets from external identity providers, cloud hyperscalers, and SaaS applications. When you establish a connector, AI Control Tower you can then contain AI agents with kill switch protocol.

The **Security** tab has two views: **Available connectors**, which lists the platforms you can connect to, and **Established connections**, which lists your active and inactive connections. Each established connection shows the source system, the connection state, and the processing state.

To set up a new connector, select an identity provider or platform from the Available connectors view and follow the guided setup wizard. Each connector has provider-specific prerequisites, which are linked from the first step of the wizard. For more information, see [Configure AI agent containment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configure-ai-agent-containment.md).

Supported connectors are:

-   AWS Bedrock
-   AWS Bedrock Agent Core
-   Azure AI Foundry
-   GCP Vertex AI
-   ServiceNow Agents

The supported identity provider is Okta.

-   **[Configuring Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/configuring-connectors.md)**  
Configuring connectors in AI Control Tower to create AI connections to discover and import AI assets for centralized visibility and governance.
-   **[Configuring trace connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configuring-trace-connections.md)**  
Collect trace data from AI agents running on supported cloud platforms and monitoring services to generate evaluation metrics, populate AI inventory, and support security monitoring in AI Control Tower.
-   **[Configuring Multi-instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/configure-multi-instance.md)**  
The Multi-instance setup enables a prod \(manager\) instance to manage multiple sub-prod \(managed\) instances and facilitate communication for AI Control Tower.
-   **[Configuring security connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configuring-security-connections.md)**  
Connect AI Control Tower to the platforms where your AI agents run and to your identity provider so that AI agent containment using kill switch protocol can deactivate rogue agents wherever they're hosted.

**Parent Topic:**[Configuring AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configuring.md)

