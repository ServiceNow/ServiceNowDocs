---
title: Create an AI connection for Azure AI Foundry \(v3.0.0\)
description: Create an AI connection for Azure AI Foundry in AI Control Tower using the  AI Service Graph Connector for Microsoft \(version 3.0.0\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/create-an-ai-connection-for-azure-ai-foundry-v3-0-0.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-07-03"
reading_time_minutes: 3
breadcrumb: [Microsoft, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# Create an AI connection for Azure AI Foundry \(v3.0.0\)

Create an AI connection for Azure AI Foundry in AI Control Tower using the  AI Service Graph Connector for Microsoft \(version 3.0.0\).

## Azure Foundry prerequisites

Complete the following steps in your Azure environment before creating an Azure Foundry connection.

-   Configure OAuth Credentials
-   The connector uses OAuth to authenticate with Azure APIs. To obtain credentials, register an application in Microsoft Entra ID

For full instructions, see the [Azure documentation](https://learn.microsoft.com/en-us/rest/api/azure/#register-your-client-application-with-azure-ad)

The Azure client application requires the following roles:

-   Reader role at the subscription or resource group level to discover resources.
-   Azure User role in the Azure AI Foundry resources.

**Note:** As of March 2026, ServiceNow supports the New Azure AI Foundry alongside the original Azure AI Foundry. The New Foundry treats each agent version as a distinct entity.

Discovery scope

Configure the scope of Azure Foundry discovery using the following options:

-   Tenant-wide discovery \(default\): Leave the Resource Name and Region fields empty to discover all Al agents across your entire Azure tenant.
-   Filter by resource \(optional\): To limit discovery to specific resources, enter resource names as comma-separated values \(examples: resource1, resource2\).
-   Filter by region \(optional\): To limit discovery to specific Azure regions, enter region names as comma-separated values \(for examples: eastus, westus2\).

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

Account &amp; Resource Hierarchy

The connector supports three Azure service variants, each with its own resource hierarchy:

-   ML Services \(AI Hub\) Subscriptions → Resource Groups → ML Workspaces → Agents
-   AI Services/Old Foundry \(Cognitive Services\) Subscriptions → Resource Groups → Cognitive Services Accounts → Projects → Agents
-   New Foundry Subscriptions → Resource Groups → Accounts → Projects → Agents → Agent Versions

The key distinction with New Foundry is that each agent version is treated as a distinct entity, which the other two variants don't support.

Discovered per agent

For each agent discovered across all three variants, the connector collects:

-   AI Agents \(assistants\)- The primary entity.
-   AI Models- Deployed models \(GPT-4o, Llama, Claude, etc.\) via deployment enrichment.
-   AI Prompts- System instructions attached to agents.
-   AI Tools- With type coverage varying by variant: ML &amp; AI Services: functions, connected\_agent, and others.
-   Sub-component Relationships- M2M links between agents and their sub agents/tools.
-   Usage/Execution Metrics- Aggregated run counts by agent, date, and session.

## Procedure

1.  Navigate to **Al Control Tower workspace** &gt; **Configurations** &gt; **AI connections**.

2.  Select **AI connector for Microsoft** from the available connectors and then select **Create connection**.

3.  Select Azure Foundry check box.

4.  Review setup instructions page displays.

    **Note:** Verify to follow all the prerequisite steps.

5.  Select **Continue**.

6.  Setup page appears.

7.  Enter the Configure and test ML services connection:

    1.  Enter the **Connection Name**.

    2.  Enter the **Regions**.

        **Note:** The region field is optional. If the field is empty, it will discover for all the region or If you can give comma- separated value of regions \(examples: eastus, westus2\).

    3.  Enter the **OAuth client ID**.

    4.  Enter the **OAuth client secret**.

    5.  Enter the **Tenant ID**.

    6.  Select **Create and test connection**.

    7.  Select **Continue**.

8.  Enter the details on Configure and test AI services connection:

    1.  Enter the **Connection Name**.

    2.  Enter the **Resources**.

        **Note:** To limit discovery to specific resources, enter the resource names as comma-separated values \(examples: resource1, resource2\). If the field is empty, it will discover for all the available resources.

    3.  Enter the **OAuth client ID**.

    4.  Enter the **OAuth client secret**.

    5.  Enter the **Tenant ID**.

9.  Configure Azure import schedule:

    1.  Verify that both the parent-scheduled jobs, Discovery and Execution are active as they’re shipped out inactive.

        **Note:** Ensure to execute the Discovery-scheduled job first.

    2.  Select Run according to your preference.

    3.  To run frequency by demand, select **Execute Now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    4.  Select **Continue**.

10. Select the **Confirm connection setup** activity to verify whether the connection was configured.


## Result

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

