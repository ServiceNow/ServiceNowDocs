---
title: AI Control Tower release notes
description: The ServiceNow AI Control Tower application provides a centralized workspace for AI stewards to manage and monitor AI within the enterprise. AI Control Tower was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
---

# AI Control Tower release notes

The ServiceNow® AI Control Tower application provides a centralized workspace for AI stewards to manage and monitor AI within the enterprise. AI Control Tower was enhanced and updated in the Australia release.

## AI Control Tower highlights for the Australia release

[Australia Patch 1](../quality/australia-patch-1.md)

-   Customize the AI asset security score calculation to reflect your security requirements.
-   Use new security metrics to monitor your LLM and AI agent output for potential security and content policy violations, potential PII, and other potential threats.
-   Gain visibility into MCP client-server interactions routed through this instance's AI Gateway.
-   Configure and create automation rules to set AI assets as managed assets.
-   Manage the end-to-end life cycles of your agentic AI systems.
-   Define the intended use and purpose of an AI system so that you can determine its benefits and risks.

[Early availability](../quality/australia-all-other-fixes.md)

-   AI assets—including AI models, AI systems, prompts, datasets, and MCP servers can be categorized as either managed or unmanaged.
-   AI connections are introduced in AI Control Tower using Service Graph Connectors \(SGC\).
-   The AI model providers supported by ServiceNow contains providers such as Now LLM Service, AWS Claude, Now LLM LTS model, and so on.
-   The AI model providers configured by your organization contains providers such as Perplexity, IBM Watson, and so on.
-   AI Gateway offers Global MCP clients, which once created can be used across all MCP servers.
-   A Gateway offers MCP Catalog to choose while adding MCP servers into AI Control Tower.

For more information on AI Control Tower, see AI Control Tower.

**Important:** AI Control Tower is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading AI Control Tower to Australia

Not applicable.

## New in the Australia release

-   **Security &amp; privacy tab in AI Control Tower**
    -   Customize the AI asset security score by weighting LLM guardrail categories that comprise the score. The score formula was changed to an average across all AI assets. The score was renamed to the AI asset security score.
    -   Measure whether your model's output or behavior potentially violates predefined LLM guardrail policies using the Data integrity incident detection chart.
    -   Review potential threats in AI agent output in Agent goal deviation, output with PII detected, and Agentic output injection detection charts.
    -   Monitor MCP server access by AI Gateway with these new charts: Clients connecting to MCP servers, authorized access attempts, and failed access attempts.
    -   The Prompt injection, Offensive content, and Sensitive data tabs have been removed and replaced by the **Access** and **Guardrails** tabs. Metrics have been reorganized into those two tabs.
    -   In **Configurations**, under **Data**, the **Data privacy** tab was renamed to **Security &amp; privacy**. In that tab, the data leak detection and anonymization section was renamed to sensitive data input and anonymization.
-   **Data section on Configurations page**

    Enable and set up data integrity incident detection, agent goal deviation, and output screening metrics to measure the integrity of your data model and potential threats in LLM output.

-   **Manage agentic AI system life cycles**

    Create AI system assets to track and manage the complete life cycles of your agentic AI systems, from onboarding to deployment. Gain comprehensive insight into each agentic AI system and take any necessary actions to successfully complete each life-cycle stage. By managing the life cycles of your agentic AI systems, you can extend their lifespans, reduce downtime, and optimize licensing costs.

-   **Define the use and purpose of an AI system**

    Specify the intended use and purpose of an AI system. Provide insight into who is using the AI system, what the AI system is being used for, and how the AI system works and provides value. This information can help you determine the benefits and risks that are associated with the AI system. For more information on classifying AI systems based on regulatory risk at intake by applying a configured Risk Assessment Methodology \(RAM\), see [AI Risk and Compliance release notes](../governance-risk-compliance/grc-ai-risk-and-compliance-rn.md) and Assessment templates and risk assessment methodologies.

-   **Associate additional related AI asset types with AI systems**

    Associate the following additional related AI asset types with your AI systems:

    -   If an AI system has an Asset type of Generative AI or Agentic AI, you can associate it with any of its supported components or subsystems.
    -   If an AI system has an Asset type of Agentic AI, you can associate it with any of its integrated AI tools.
-   **Create change and offboarding requests for additional AI asset types**

    Create change requests for the following additional AI asset types:

    -   AI systems with an Asset type of Agentic AI
    -   Datasets
    In addition, create offboarding requests for the following additional AI asset types:

    -   AI systems with an Asset type of Agentic AI
    -   AI models
    -   Datasets
    -   MCP servers
-   **ServiceNow product tiers**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **Enterprise AI discovery: Unlock Visibility, Governance &amp; Value**

    AI connections are created using AI Service Graph Connectors. AI connections are a combination of hyperscalers, AI apps, and agentic AI frameworks.

    The AI Service Graph Connectors are available from March 2026

    -   AWS
    -   Microsoft- Azure Foundry and Copilot
    -   Google Cloud Platform \(GCP\) Vertex AI
    -   n8n
    -   LangGraph
    -   Salesforce
-   **Assets list managed and unmanaged assets**

    Managed assets benefit from AI Control Tower features such as governance, lifecycle management, value assessment, risk classification, security, and privacy. Unmanaged assets, on the other hand, do not have access to these AI Control Tower capabilities.

-   **AI Gateway**

    AI Gateway offers MCP Global Clients, which can be used across all servers.

    A Gateway offers MCP Catalog to choose while adding MCP servers.

    MCP server can be added to an AI Asset inventory from AI Control Tower.


## UI changes

-   **Drop-down menu for associating AI assets with related assets**

    In both the AI asset creation forms and AI asset records, the **Add new** button that previously enabled you to associate AI assets with other related assets has changed into an Add from inventory drop-down menu with the **Add from inventory** and **Create** options. The **Add from inventory** menu option enables you to associate AI assets with related assets that are currently available in your asset inventory. The **Create** menu option enables you to associate AI assets with related assets that are not currently available in your asset inventory.

-   **Editable asset details fields on the Details tab of AI asset records**

    You can now modify asset details fields directly on the **Details** tab of your AI asset records.

-   **Related asset lists in AI asset records**

    The lists of related assets in each AI asset record has moved from the **Related assets** tab to the **Details** tab.


## Changed in this release

Not applicable.

## Removed in this release

[Australia Patch 1](../quality/australia-patch-1.md) The Autonomous vs. supervised AI tools chart has been removed from the Security &amp; privacy tab.

[Early availability](../quality/australia-all-other-fixes.md)

-   Adding legacy AI connections via Service Graph Connectors \(SGC\) is deprecated. In AI connections, under Legacy connections, the **New** button has been removed to block users from creating new connections using SGC.


## Deprecated features

-   The ability to add hyperscalers from the AICT configuration section is no longer available. You can find any previously created hyperscaler connections in the AI connections section, under Legacy connections.

## Activation information

Install AI Control Tower by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    -   com.sn\_ai\_disc - Enables the AI connections page in the AI Control Tower configuration.
    -   sn\_sgc\_central - Enables the Service Graph Connector \(SGC\) feature in the AI connections page.

## Browser requirements

The AI Control Tower application supports all browsers.

## Accessibility information

The AI Control Tower application supports all platform accessibility features.

## Localization information

The AI Control Tower application is localized.

## Related ServiceNow applications and features

-   **AI Risk and Compliance**

    Enable risk and compliance managers to verify organizational compliance with regulations and policies governing AI systems by using the AI Risk and Compliance application, along with the AI Control Tower.

-   **Strategic Planning**

    Prioritize, roadmap, and track work when using traditional, agile, or hybrid methodologies with ServiceNow® Strategic Planning. Align strategy to execution by defining and tracking goals across your organization. When the Strategic Planning application is installed, the **AI strategy** tab appears in the AI Control Tower workspace, featuring different widgets for AI strategies, goals, targets, costs of planning items, prioritized work, and RIDAC details.

    Strategic Planning is available with an SPM Professional license.

-   **Goal Framework**

    Create goals, set targets for them, and evaluate the progress of the goals and targets to accomplish your organizational plans and drive business outcomes with the ServiceNow® Goal Framework application. When the Goal Framework application is installed, the **AI strategy** tab appears in the AI Control Tower workspace, featuring different widgets for AI strategies, goals, and targets.

    Goal Framework is available with an SPM Standard license.


**Parent Topic:**[AI Experiences release notes](intelligent-experiences-rn-landing.md)

