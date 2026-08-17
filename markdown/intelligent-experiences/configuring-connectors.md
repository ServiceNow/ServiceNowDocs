---
title: Configuring Connectors
description: Configuring connectors in AI Control Tower to create AI connections to discover and import AI assets for centralized visibility and governance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/configuring-connectors.html
release: zurich
topic_type: concept
last_updated: "2026-07-28"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring integrations, Configure, AI Control Tower, Enable AI experiences]
---

# Configuring Connectors

Configuring connectors in AI Control Tower to create AI connections to discover and import AI assets for centralized visibility and governance.

## Creating an AI connection

To use a connector, you create an AI connection from **AI Control Tower &gt; Settings &gt; Integrations &gt; Connectors**. Each connector uses a guided playbook that walks you through selecting the source system, entering credentials, testing the connection, and configuring the import schedule.

**Note:** The Connectors page is available only when the com.sn\_ai\_disc and sn\_sgc\_central plugins are installed.

Once the connection is established and the discovery job runs, the external AI assets appear in **Inventory &gt; AI Assets**.

Connectors are the mechanism; the AI connection is the configured instance of a connector on your instance. A single connector type — for example, AI Connector for Amazon can support multiple AI connections if you want to connect to different accounts or environments.

## Connectors tab in AI Control Tower

AI connections combine hyperscalers, AI apps, and agentic AI frameworks using Service Graph Connectors. To view the available connectors, navigate to **AI Control Tower &gt; Settings &gt; Integrations &gt; Connectors &gt; Available Connectors**. For the established connections, navigate to the Established connections tab.

AI connections include two types of scheduled jobs:

-   Discovery: Discovers AI assets from hyperscalers, AI applications, and agentic AI frameworks.
-   Execution: Processes usage data and makes it visible on the Performance Analytics page for each discovered agent.

**Note:** Ensure that the AI discovery daily data collection job is active, which is the key element in collecting the data.

For information about connectors, prerequisites, and the configuration process, see [AI Control Tower- AI Discovery Connectors \[KB2986990\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB2986990) article in the Now Support Knowledge Base.

The AI Service Graph Connectors are a specialized subset of Service Graph Connectors built specifically for AI Control Tower. For more information, see 

**Parent Topic:**[Configuring integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configuring-integrations.md)

