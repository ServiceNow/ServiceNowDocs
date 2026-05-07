---
title: Create AI connection for Azure Foundry
description: Create an AI connection for Azure Foundry in AI Control Tower using the  AI Service Graph Connector for Microsoft.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft, Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# Create AI connection for Azure Foundry

Create an AI connection for Azure Foundry in AI Control Tower using the  AI Service Graph Connector for Microsoft.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and n\_cmdb\_int\_util.sgc\_admin

Account &amp; Resource Hierarchy

The connector supports three Azure service variants, each with its own resource hierarchy:

-   ML Services \(AI Hub\) Subscriptions → Resource Groups → ML Workspaces → Agents
-   AI Services/Old Foundry \(Cognitive Services\) Subscriptions → Resource Groups → Cognitive Services Accounts → Projects → Agents
-   New Foundry Subscriptions → Resource Groups → Accounts → Projects → Agents → Agent Versions

The key distinction with New Foundry is that each agent version is treated as a distinct entity, which the other two variants don't support.

Discovered per agent

For each agent discovered across all three variants, the connector collects:

-   **AI Agents \(assistants\)**- The primary entity.
-   **AI Models**- Deployed models \(GPT-4o, Llama, Claude, etc.\) via deployment enrichment.
-   **AI Prompts**- System instructions attached to agents.
-   **AI Tools**- With type coverage varying by variant:
    -   ML &amp; AI Services: `functions`, `connected_agent`, others
    -   New Foundry adds: `mcp`, `openapi`, `a2a_preview`
-   **Sub-component Relationships**- M2M links between agents and their sub agents/tools
-   **Usage/Execution Metrics**- Aggregated run counts by agent, date, and session.

## Procedure

1.  Navigate to **Al Control Tower workspace** &gt; **Configurations** &gt; **AI connections**.

2.  Select **Add**.

3.  Select **AI connector for Microsoft** from all the available connectors.

4.  Select **Create connection**.

5.  Select Azure Foundry check box.

6.  Review setup instructions page displays.

    **Note:** Verify to follow all the prerequisite steps.

7.  Select **Continue**.

8.  Setup page appears

9.  **Configure and test ML services connection**

    1.  Enter the **Connection Name**.

    2.  Enter the **Connection URL** \(https://&lt;region&gt;api.azureml.ms\).

        **Note:** The region is available under project details.

    3.  Enter the **OAuth client ID**OAuth client ID.

    4.  Enter the **OAuth client secret**.

    5.  Enter the **OAuth token URL** \([https://login.microsoftonline.com/&lt;tenantid&gt;/oauth2/v2.0/token](https://login.microsoftonline.com/%3ctenantid%3e/oauth2/v2.0/token)\).

        The tenant id can be found in the URL of every page. It’s abbreviated as tid.

    6.  Select **Update and test connection**

    7.  Select **Continue**.

10. **Configure and test AI services connection**

    1.  Enter the **Connection Name**.

    2.  Enter the **Connection URL** \(https://&lt;resource-name&gt;services.ai.azure.com\)

        **Note:** To obtain the resource name, make sure that you're on New Foundry \(Enable the New Foundry toggle\) and select the project. Once you're on the home page, look for the Project endpoint to view the resource name.

        Starting from March 2026 onwards, ServiceNow provides support to the New Foundry along with the old Foundry.

    3.  Enter the **OAuth client ID**.

    4.  Enter the **OAuth client secret**.

    5.  Enter the **OAuth token URL**.

11. **Configure import schedule**

    1.  Verify that both the parent-scheduled jobs, Discovery and Execution are active as they’re shipped out inactive.

        verify to execute the Discovery-scheduled job first.

    2.  Select **Execute now** to run.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    3.  Select **Continue**.

    4.  Select **View all connections** to view the newly created connection.


## Result

An AI connection is created for Azure Foundry.

