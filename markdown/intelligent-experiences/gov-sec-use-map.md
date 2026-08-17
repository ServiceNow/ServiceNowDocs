---
title: Discover your agent network with the map
description: Use the agent map to visualize your entire agentic ecosystem, including ServiceNow and third-party AI assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/gov-sec-use-map.html
release: zurich
topic_type: task
last_updated: "2026-05-02"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Managing AI asset security, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Discover your agent network with the map

Use the agent map to visualize your entire agentic ecosystem, including ServiceNow and third-party AI assets.

## About this task

The agent map shows a holistic view of the relationships between your AI providers, AI models, MCP servers, AI agents, agentic workflows, and tools. You can use the map to review these relationships and get details about the AI assets in your enterprise.

Below the map, all of your managed agentic AI assets are listed.

\[Omitted image "gov-sec-access-map.png"\] Alt text: Agent map with managed agentic assets list below it.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\]

Configure Veza access intelligence to show risk score and other information for each AI asset in the map. For more information, see [Configure Veza access intelligence in the agent map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configure-veza-access-intelligence.md).

## Procedure

1.  Navigate to **AI Control Tower** &gt; **Govern** &gt; **Security**.

2.  On the **Overview** tab, select the agent map to go to the agent map details.

3.  On the agent map, select agentic assets to view details such as type and domain.

    -   To find an asset in the map, enter a partial or entire name in the search box in the map.
    -   To identify asset symbols, select **Legend**.
    -   To zoom and refresh the map, use the controls in the map.
<table><thead><tr><th>

Node

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Agent and AI Model

</td><td>

-   **Agent risk**

The severity of risk as defined by the Veza tenant for your instance. Risks can be classified Critical, High, Medium, and Low. For more information, see [Risk level tiers in Veza documentation](https://docs.veza.com/4yItIzMvkpAvMVFAamTf/features/access-reviews/how-to/access-path-risk-score#risk-level-tiers).

-   **Risk score**

A score representing the risk of the agent or model. Risk scores in Veza are calculated for each AI asset based on the number of associated risks and their risk levels. The scoring system weighs both the severity of risks and their cumulative impact using an algorithm designed to provide comparable scores across all AI assets in the agent map. For more information, see [How risk scoring works in Veza documentation](https://docs.veza.com/4yItIzMvkpAvMVFAamTf/features/insights/risks#how-risk-scoring-works).

-   **Nonhuman identity**

The user of the AI agent or model.

-   **Human owner**

The creator of the AI agent or model.

</td></tr></tbody>
</table><table><thead><tr><th>

Node

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Agentic workflow

</td><td>

-   **Description**

A brief description of the workflow.

-   **Type**

This value is always Agentic Workflow.

-   **Domain**

The domain scope of the workflow.

-   **Execution mode**

How the workflow is executed \(autonomous or manual\).

-   **Created by**

The creator of the workflow.

</td></tr><tr><td>

Agent

</td><td>

-   **Description**

A brief description of the AI agent.

-   **Type**

This value is always Agent.

-   **Domain**

The domain scope of the AI agent.

-   **Created by**

The creator of the AI agent.

-   **Source system**

The external AI system.

-   **Provider**

The AI provider.

 **Note:** Only agents with access issues display the **Access issues** details.

 -   **Access issues**

The resources and operations causing the access issues.

-   **Resource**

The resource the agent is having issues accessing.

-   **Operation**

The operation the agent attempted.

-   **Count**

The number of times of the agent encountered the issue.

</td></tr><tr><td>

AI model

</td><td>

-   **Type**

This value is always AI Model.

</td></tr><tr><td>

MCP

</td><td>

-   **Type**

This value is always MCP.

</td></tr><tr><td>

Provider

</td><td>

-   **Type**

This value is always Provider.

</td></tr><tr><td>

Tool

</td><td>

-   **Description**

The description of the tool.

-   **Type**

This value is always Tool.

-   **Domain**

The domain scope of the tool.

-   **Execution mode**

The execution mode of the tool \(supervised or autonomous\).

-   **Tool type**

The type of the tool. For example, `action`.

-   **Target record**

The record the tool modifies.

-   **Created by**

The creator of the tool.

 **Note:** Select **Open tool record** to view additional tool details.

</td></tr></tbody>
</table>
