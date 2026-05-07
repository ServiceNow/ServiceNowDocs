---
title: AI connections
description: Explore the AI connections page and the features.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# AI connections

Explore the AI connections page and the features.

## AI connections overview

The AI connections page enables you to integrate the third-party systems to discover AI assets and track data usage from hyperscalars, AI apps, and agentic AI frameworks via Service Graph Connectors \(SGC\) to set AI connections. AI stewards can access the AI connections page and on this page, you can find a list of data sources displayed in columns.

**Note:** The AI connections page appears only when the plugins com.sn\_ai\_disc and sn\_sgc\_central are installed.

Agents are discovered according to the set run frequency, but you can also manually discover agents or collect usage data by selecting a connection and choosing the run option. AI stewards can perform this action, including activating or deactivating the AI connection by selecting the State column in the list. Admins can adjust the run frequency by accessing the connection alias.

**Note:** Uninstall the AWS AI Discovery plugin before installing the AI Discovery plugin \(sn\_ai\_disc\) to use the AI connections.

There are two types of scheduled jobs on AI connections.

-   **Discovery**

    To discover AI assets from hyperscalars, AI apps, and agentic AI frameworks.

-   **Execution**

    To process usage data and the data is visible on the Performance analytics page for every individual discovered agent.

    **Note:** Confirm that the AI discovery daily data collection job is active, which is the key element in collecting the data.


AI connections are a combination of hyperscalars, AI apps, and agentic AI frameworks created using Service Graph Connectors. AI connections can discover and imports AI agents and as well as usage data from the AI agents.

Navigate to the AI connections page in the AI Control Tower, you’re able to create AI connections as well as manage the existing ones. The existing connections appear under the section Legacy connections.

Starting March 2026, these AI Service Graph Connectors  are available.

-   [AWS](aws_0.md)
-   [GCP Vertex AI](gcp-vertex-ai.md)
-   [LangGraph](langgraph.md)
-   [Microsoft](microsoft.md)
-   [n8n](n8n.md)
-   [Salesforce](salesforce.md)

![](../image/ai-connections.png)

## AI connection record

The AI connection record has the following tabs:

Details- Displays the connection details of the AI connection.

Data sources- Represent a running unit, which defines what data is fetched from a third‑party system.

Import schedules- Run the parent data import and execute the job to discover AI Agents and track usage data.

