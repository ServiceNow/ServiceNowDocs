---
title: ServiceNow product tiers
description: ServiceNow structures its products and packages in three tiers — Foundation, Advanced, and Prime. Each tier incorporates AI and builds progressively on the previous one with additional AI capabilities, agents, and governance tools.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-native-sku-overview.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [AI native, Foundation, Advanced, Prime, AI tiers, ITSM, CSM, HRSD, Industry]
breadcrumb: [Enable AI experiences]
---

# ServiceNow product tiers

ServiceNow structures its products and packages in three tiers — Foundation, Advanced, and Prime. Each tier incorporates AI and builds progressively on the previous one with additional AI capabilities, agents, and governance tools.

The Foundation tier delivers AI-assisted insights and routine automation. Advanced adds agentic workflows capable of synthesizing context across complex processes. Prime unlocks a fully autonomous workforce that executes multi-step tasks end to end.

This structure makes the path to greater automation simple, predictable, and scalable across your organization.

**Note:** Contact your ServiceNow account team for information about availability and entitlement details for your organization. The rollout of new product tiers is independent of your organization's upgrade cycle.

## Product tiers

All supported product lines offer these three tiers that include the features listed below.

|Feature|Foundation|Advanced|Prime|
|-------|----------|--------|-----|
|AI skills and routine AI agents|Supported|Supported|Supported|
|Configure out-of-the-box skills and agents|Supported|Supported|Supported|
|Agentic workflows with contextual AI synthesis|Supported|Supported|Supported|
|Platform Analytics Advanced|Not supported|Supported|Supported|
|Create net-new custom AI skills and agents|Not supported|Not supported|Supported|
|MCP Server \(inbound\)|Not supported|Not supported|Supported|
|Autonomous AI workforce \(AI Specialists\)|Not supported|Not supported|Supported|

|Foundation|Advanced|Prime|
|----------|--------|-----|
|AI skills, routine AI agents|Agentic workflows|Autonomous AI workforce|
|This solution provides task-based assistance using routine pattern recognition and categorization to accelerate understanding and help you work faster.|This solution automates entire steps in a workflow, working side-by-side with you while synthesizing new insights, understanding context, and applying deep domain knowledge.|This solution offers fully independent AI specialists to make and execute decisions autonomously. They apply deep, role-based expertise to master and run multiple agentic workflows.|

## AI platform enablers

Every offering has a set of platform-level AI capabilities powering the skills, agents, and governance experience across all product lines.

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-now-assist-platform.md)**

    Now Assist is the generative AI experience embedded throughout the ServiceNow AI Platform, delivering skills such as incident summarization, sentiment analysis, reply generation, and case resolution assistance. Now Assist skills are available at every tier, across [ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-for-itsm-rn.md), CSM, HRSD, and industry solutions. For a full overview of the Now Assist panel and administration tools, see [Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md).

-   **[Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-ai-agents.md)**

    Now Assist AI agents extend generative AI into autonomous agentic workflows. Using [AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-agent-studio.md), administrators can configure out-of-the-box agents at Foundation and Advanced tiers, or build net-new agents from natural language instructions at the Prime tier.

-   **AI Agent Fabric**

    AI Agent Fabric is the communication layer that enables ServiceNow AI agents to collaborate with each other and with third-party AI systems using open protocols — including Agent-to-Agent \(A2A\) and Model Context Protocol \(MCP\). Foundation and Advanced tiers include A2A outbound connectivity; Prime adds inbound MCP Server capability, enabling external platforms to invoke ServiceNow agents directly. For implementation details, see [Enable MCP and A2A for your agentic workflows](https://www.servicenow.com/community/now-assist-articles/enable-mcp-and-a2a-for-your-agentic-workflows-with-faqs-updated/ta-p/3373907).

-   **AI Control Tower**

    AI Control Tower is embedded at every tier, providing centralized governance, lifecycle management, and real-time visibility across all AI assets — whether built natively on ServiceNow or sourced from external vendors. At Foundation and Advanced, AI Control Tower discovers and manages ServiceNow AI assets; Prime extends full management and assist metering to external AI assets as well. For configuration guidance, see [Exploring AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/exploring-ai-control-tower.md) and [Configure AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/configuring-ai-governance.md).

-   **Workflow Data Fabric**

    Workflow Data Fabric grounds AI agents in real enterprise data by connecting any application, database, or system to the ServiceNow AI Platform — without requiring data to be moved or replicated. WDF Foundation, including Integration Hub, Robotic Process Automation Hub, Automation Center, and Data Catalog, is embedded in every tier edition. WDF Advanced, adding Zero Copy Connectors and Stream Connect, is available as a paid upgrade.

-   **RaptorDB**

    RaptorDB is the next-generation ServiceNow database, purpose-built to deliver the performance and scale that AI-native workloads demand. RaptorDB Standard underpins every tier edition with improved response times and optimized query performance; RaptorDB Professional unlocks ultra-scale analytics, enhanced column-store capabilities, and advanced instance topology support for organizations running the most demanding generative AI and machine-scale data use cases.

-   **Moveworks for ServiceNow \(EmployeeWorks\)**

    ServiceNow EmployeeWorks combines Moveworks' conversational AI and enterprise search with ServiceNow's unified portal and autonomous workflows, giving employees a single, natural-language front door to enterprise services — available across Teams, Slack, browser, and mobile. EmployeeWorks capability is bundled at a level aligned with each tier, ensuring that conversational access scales with your agentic AI investment. For more information, see the [Autonomous Workforce and EmployeeWorks announcement](https://newsroom.servicenow.com/press-releases/details/2026/ServiceNow-launches-Autonomous-Workforce-that-thinks-and-acts-adds-Moveworks-to-the-ServiceNow-AI-Platform/default.aspx).


## Get started

To begin implementing the capabilities offered at each tier on your instance, see the following resources.

-   [Now Assist overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-now-assist-platform.md) — Learn about the applications and features that make up the Now Assist experience.
-   AI governance — Learn about the importance of AI governance to ensure responsible use, regulatory compliance, and alignment with enterprise goals.
-   Data readiness — Learn how to prepare your instance data for Now Assist.

## Related ServiceNow applications and features

-   [Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md)
-   [Exploring Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-now-assist-platform.md)
-   [AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-agent-studio.md)
-   AI Control Tower
-   [AI Control Tower Home](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-control-tower-home-page.md)
-   [Exploring AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/exploring-ai-control-tower.md)
-   [AI Control Tower dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-governance.md)
-   [AI Control Tower release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/ai-control-tower-rn.md)
-   Workflow Data Fabric
-   RaptorDB
-   [Now Assist for ITSM release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-for-itsm-rn.md)

