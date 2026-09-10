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
|MCP Server Console \(inbound\)|Supported|Supported|Supported|
|Autonomous AI workforce \(AI Specialists\)|Not supported|Not supported|Supported|

|Foundation|Advanced|Prime|
|----------|--------|-----|
|AI skills, routine AI agents|Agentic workflows|Autonomous AI workforce|
|This solution provides task-based assistance using routine pattern recognition and categorization to accelerate understanding and help you work faster.|This solution automates entire steps in a workflow, working side-by-side with you while synthesizing new insights, understanding context, and applying deep domain knowledge.|This solution offers fully independent AI specialists to make and execute decisions autonomously. They apply deep, role-based expertise to master and run multiple agentic workflows.|

## AI platform enablers

Every offering has a set of platform-level AI capabilities powering the skills, agents, and governance experience across all product lines.

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-now-assist-platform.md)**

    Now Assist is the generative AI experience embedded throughout the ServiceNow AI Platform, delivering skills such as incident summarization, sentiment analysis, reply generation, and case resolution assistance. AI skills are available at every tier, across [ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-for-itsm-rn.md), CSM, ServiceNow Otto for HRSD, and industry solutions. For a full overview of the ServiceNow Otto panel and administration tools, see [Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md).

-   **[Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-ai-agents.md)**

    AI agents extend generative AI into autonomous agentic workflows. Using [AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-agent-studio.md), administrators can configure out-of-the-box agents at Foundation and Advanced tiers, or build net-new agents from natural language instructions at the Prime tier.

-   **AI Action Fabric**

    AI Action Fabric is the communication layer that enables ServiceNow AI agents to collaborate with each other and with third-party AI systems. It uses open protocols to facilitate this collaboration. These protocols include Agent-to-Agent \(A2A\) and Model Context Protocol \(MCP\). Foundation and Advanced tiers include A2A outbound connectivity; Prime adds inbound MCP Server Console capability, enabling external platforms to invoke ServiceNow agents directly. For implementation details, see [Enable MCP and A2A for your agentic workflows](https://www.servicenow.com/community/now-assist-articles/enable-mcp-and-a2a-for-your-agentic-workflows-with-faqs-updated/ta-p/3373907).

-   **[AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-landing.md)**

    AI Control Tower is included in every tier \(Foundation, Advanced, and Prime\) with the same capabilities at each. It discovers and visualizes ServiceNow AI assets automatically, and external AI with setup. It also allows you to manage ServiceNow AI assets \(governs, secures, observes, and measures\). Full management of external AI assets \(govern, secure, observe, measure\) requires a separate AI Control Tower for Enterprise AI license. For configuration guidance, see [Exploring AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-exploring.md) and [Configuring AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring.md).

-   **[Workflow Data Fabric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-integrations-applications.md)**

    Workflow Data Fabric grounds AI agents in real enterprise data by connecting any application, database, or system to the ServiceNow AI Platform — without requiring data to be moved or replicated. Workflow Data Fabric Foundation, including [Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integrationhub.md), [Robotic Process Automation \(RPA\) Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rpa-main-landing-page.md), [Automation Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center-landing-page.md), and [Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/data-catalog.md), is embedded in every tier edition. Workflow Data Fabric Advanced, adding [Zero Copy Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/zero-copy-connectors.md) and [Stream Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/stream-connect-quick-start.md), is available as a paid upgrade.

-   **[RaptorDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/raptordb.md)**

    RaptorDB is the next-generation ServiceNow database, purpose-built to deliver the performance and scale that AI-native workloads demand. RaptorDB Standard underpins every tier edition with improved response times and optimized query performance. RaptorDB Professional unlocks ultra-scale analytics, enhanced column-store capabilities, and advanced instance topology support for organizations running the most demanding generative AI and machine-scale data use cases.

-   **Moveworks for ServiceNow \(EmployeeWorks\)**

    ServiceNow EmployeeWorks brings together Moveworks' conversational AI and enterprise search with ServiceNow's unified portal and autonomous workflows. This combination gives employees a single, natural-language front door to enterprise services. The solution is available across Microsoft Teams, Slack, browser, and mobile. EmployeeWorks capability is bundled at a level aligned with each tier, ensuring that conversational access scales with your agentic AI investment. For more information, see the [Autonomous Workforce and EmployeeWorks announcement](https://newsroom.servicenow.com/press-releases/details/2026/ServiceNow-launches-Autonomous-Workforce-that-thinks-and-acts-adds-Moveworks-to-the-ServiceNow-AI-Platform/default.aspx).


## Get started

To begin implementing the capabilities offered at each tier on your instance, see the following resources.

-   [Now Assist overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-now-assist-platform.md) — Learn about the applications and features that make up the AI experience.
-   [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-landing.md) — Learn about the importance of AI governance to ensure responsible use, regulatory compliance, and alignment with enterprise goals.
-   [Data readiness](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sn-ai-impl-data-readiness.md) — Learn how to prepare your instance data for AI.

## Related ServiceNow applications and features

-   [Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md)
-   [Exploring Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-now-assist-platform.md)
-   [AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-agent-studio.md)
-   [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-landing.md)
-   [Workflow Data Fabric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-integrations-applications.md)
-   [RaptorDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/raptordb.md)
-   [Now Assist for ITSM release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-for-itsm-rn.md)

