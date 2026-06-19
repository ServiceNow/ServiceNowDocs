---
title: AI connections setup
description: Explore the AI connections setup page and its features.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/ai-discovery-setup.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Gen AI, Generative AI]
breadcrumb: [AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# AI connections setup

Explore the AI connections setup page and its features.

## AI connections overview

Use the AI connections page to integrate third-party systems and discover AI assets. You can track data usage from hyperscalers, AI apps, and agentic AI frameworks using Service Graph Connectors \(SGC\). AI stewards have access to the AI connections page, where data sources are listed in columns.

**Note:** The AI connections page is visible only when both the com.sn\_ai\_disc and sn\_sgc\_central plugins are installed.

Agents are discovered according to the set run frequency, but you can also manually discover agents or collect usage data by selecting a connection and choosing the run option. AI stewards can perform this action, including activating or deactivating the AI connection by selecting the State column in the list. Admins can adjust the run frequency by accessing the connection alias.

**Note:** Uninstall the AWS AI Discovery plugin before installing the AI Discovery plugin \(sn\_ai\_disc\) to use the AI connections.

On AI connections, there are two categories of scheduled jobs.

-   **Discovery**

    To discover AI assets from hyperscalers, AI apps, and agentic AI frameworks.

-   **Execution**

    To process usage data and the data is visible on the Performance analytics page for every individual discovered agent.

    **Note:** Confirm that the AI discovery daily data collection job is active, which is the key element in collecting the data.


AI connections are a combination of hyperscalers, AI apps, and agentic AI frameworks created using Service Graph Connectors. AI connections can discover and import AI agents and as well as usage data.

Navigate to AI connections page to create AI connections and manage your existing ones. The connections that were set up without Service Graph Connectors appear in the Legacy connections section.

\[Omitted image "ai-connections.png"\] Alt text:

## AI connection record

The AI connection record has the following tabs:

Details- Displays the connection details of the AI connection.

Data sources- Represent a running unit, which defines what data is fetched from a third‑party system.

Import schedules- Run the parent data import and execute the job to discover AI agents and track usage data.

