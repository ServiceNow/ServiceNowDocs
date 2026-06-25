---
title: AI Control Tower release notes
description: The ServiceNow AI Control Tower application provides a centralized workspace for AI stewards to manage and monitor AI within the enterprise. AI Control Tower was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 10
---

# AI Control Tower release notes

The ServiceNow® AI Control Tower application provides a centralized workspace for AI stewards to manage and monitor AI within the enterprise. AI Control Tower was enhanced and updated in the Australia release.

## AI Control Tower highlights for the Australia release

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   Customize the AI asset security score calculation to reflect your security requirements.
-   Use new security metrics to monitor your LLM and AI agent output for potential security and content policy violations, potential PII, and other potential threats.
-   Gain visibility into MCP client-server interactions routed through this instance's AI Gateway.
-   Configure and create automation rules to set AI assets as managed assets.
-   Manage the end-to-end life cycles of your agentic AI systems.
-   Define the intended use and purpose of an AI system so that you can determine its benefits and risks.

[Early availability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-all-other-fixes.md)

-   AI assets—including AI models, AI systems, prompts, datasets, and MCP servers can be categorized as either managed or unmanaged.
-   AI connections are introduced in AI Control Tower using Service Graph Connectors \(SGC\).
-   The AI model providers supported by ServiceNow contains providers such as Now LLM Service, AWS Claude, Now LLM LTS model, and so on.
-   The AI model providers configured by your organization contains providers such as Perplexity, IBM Watson, and so on.
-   AI Gateway offers Global MCP clients, which once created can be used across all MCP servers.
-   A Gateway offers MCP Catalog to choose while adding MCP servers into AI Control Tower.

For more information on AI Control Tower, see [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower-landing.md).

**Important:** AI Control Tower is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower-landing.md) to Australia

Not applicable.

## New in the Australia release

-   **[Publish ServiceNow agents to Microsoft Agent 365](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/publish-servicenow-agents-to-microsoft-agent-365.md)**

    Publish the ServiceNow Agents to Microsoft Agent 365 ensuring the ServiceNow agents are sent to external registries.

    -   **[Service Graph Connectors for AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/service-graph-connectors-for-ai-control-tower.md)**

        AI Service Graph Connector for Databricks discover AI agents and import to AI Control Tower from Databricks environment.


-   **[Security &amp; privacy tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/security-privacy-tab.md)**
    -   Customize the AI asset security score by weighting LLM guardrail categories that comprise the score. The score formula was changed to an average across all AI assets. The score was renamed to the AI asset security score.
    -   Measure whether your model's output or behavior potentially violates predefined LLM guardrail policies using the Data integrity incident detection chart.
    -   Review potential threats in AI agent output in Agent goal deviation, output with PII detected, and Agentic output injection detection charts.
    -   Monitor MCP server access by AI Gateway with these new charts: Clients connecting to MCP servers, authorized access attempts, and failed access attempts.
    -   The Prompt injection, Offensive content, and Sensitive data tabs have been removed and replaced by the **Access** and **Guardrails** tabs. Metrics have been reorganized into those two tabs.
    -   In **Configurations**, under **Data**, the **Data privacy** tab was renamed to **Security &amp; privacy**. In that tab, the data leak detection and anonymization section was renamed to sensitive data input and anonymization.
-   **[Data section on Configurations page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/data.md)**

    Enable and set up data integrity incident detection, agent goal deviation, and output screening metrics. These metrics measure the integrity of your data model and potential threats in LLM output.

-   **[Manage agentic AI system life cycles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-ai-system-assets.md)**

    Create AI system assets to track and manage the complete life cycles of your agentic AI systems, from onboarding to deployment. Gain comprehensive insight into each agentic AI system and take any necessary actions to successfully complete each life-cycle stage. By managing the life cycles of your agentic AI systems, you can extend their lifespans, reduce downtime, and optimize licensing costs.

-   **[Define the use and purpose of an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-ai-system-assets.md)**

    Specify the intended use and purpose of an AI system. Provide insight into who is using the AI system, what the AI system is being used for, and how the AI system works and provides value. This information can help you determine the benefits and risks that are associated with the AI system. For more information on classifying AI systems based on regulatory risk at intake by applying a configured Risk Assessment Methodology \(RAM\), see, [AI Risk and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-ai-risk-and-compliance-rn.md) [Assessment templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-assessment-templates.md)and [Risk assessment methodologies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-rams.md).

-   **[Associate additional related AI asset types with AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-ai-system-assets.md)**

    Associate the following additional related AI asset types with your AI systems:

    -   If an AI system has an Asset type of Generative AI or Agentic AI, you can associate it with any of its supported components or subsystems.
    -   If an AI system has an Asset type of Agentic AI, you can associate it with any of its integrated AI tools.
-   **[Create change and offboarding requests for additional AI asset types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/creating-ai-asset-requests.md)**

    Create change requests for the following additional AI asset types:

    -   AI systems with an Asset type of Agentic AI
    -   Datasets
    In addition, create offboarding requests for the following additional AI asset types:

    -   AI systems with an Asset type of Agentic AI
    -   AI models
    -   Datasets
    -   MCP servers
-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[AI connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enterprise-ai-discovery.md)**

    AI connections are created using AI Service Graph Connectors. AI connections are a combination of hyperscalers, AI apps, and agentic AI frameworks.

    The following AI Service Graph Connectors are available from March 2026

    -   [AWS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aws_0.md)
    -   [Microsoft](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/microsoft.md)- Azure Foundry and Copilot
    -   [Google Cloud Platform \(GCP\) Vertex AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gcp-vertex-ai.md)
    -   [n8n](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/n8n.md)
    -   [LangGraph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/langgraph.md)
    -   [Salesforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/salesforce.md)
-   **[Managed and unmanaged AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/assets-list-managing-and-unmanaging-assets.md)**

    Managed assets benefit from AI Control Tower features such as governance, lifecycle management, value assessment, risk classification, security, and privacy. Unmanaged assets, on the other hand, do not have access to these AI Control Tower capabilities.

-   **[AI Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-gateway-overview.md)**

    AI Gateway offers MCP Global Clients, which can be used across all servers.

    A Gateway offers MCP Catalog to choose while adding MCP servers.

    MCP server can be added to an AI Asset inventory from AI Control Tower.


## UI changes

-   **[Drop-down menu for associating AI assets with related assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/view-ai-assets-lifecycle-stage.md)**

    In both the AI asset creation forms and AI asset records, the **Add new** button that previously enabled you to associate AI assets with other related assets has changed into an Add from inventory drop-down menu with the **Add from inventory** and **Create** options. The **Add from inventory** menu option enables you to associate AI assets with related assets that are currently available in your asset inventory. The **Create** menu option enables you to associate AI assets with related assets that are not currently available in your asset inventory.

-   **[Editable asset details fields on the Details tab of AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/view-ai-assets-lifecycle-stage.md)**

    You can now modify asset details fields directly on the **Details** tab of your AI asset records.

-   **[Related asset lists in AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/view-ai-assets-lifecycle-stage.md)**

    The lists of related assets in each AI asset record has moved from the **Related assets** tab to the **Details** tab.


-   **AI record type label**

    The AI assets \(sn\_grc\_ai\_gov\_ai\_system\) table has been renamed to AI records \(sn\_grc\_ai\_gov\_ai\_system\). The **Record type** field on AI system, AI model, and dataset records in the AI Control Tower inventory now displays **AI record** instead of the previous asset-specific labels.


## Changed in this release

-   **[Additional regulatory frameworks in the AI Risk and Compliance content pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-content-pack.md)**

    After AI Risk and Compliance is updated to version 22.3.0 and the new frameworks are activated, authority documents, agency mappings, and citations for the Transparency in Frontier Artificial Intelligence Act \(SB 53\) and the Colorado Artificial Intelligence Act \(SB 205\) appear in the compliance posture and related views on the **Risk and compliance** tab. For more information, see [AI Risk and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-ai-risk-and-compliance-rn.md), [AI Risk and Compliance Content Pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-content-pack.md), [Activate or update the Transparency in Frontier Artificial Intelligence Act \(SB 53\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/activate-or-update-sb53.md), and [Activate or update the Colorado Artificial Intelligence Act](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/activate-or-update-colorado-ai-act.md).

-   **[Impact assessment field auto-population](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-intake.md)**

    After upgrading to version 22.3.5, if you have the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] or AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\] role, the screening question responses that capture the AI system's intended use and operational context from the Use and Purpose section of the AI use case request form are automatically populated in the corresponding Use and Purpose fields of a new impact assessment. This synchronization reduces manual entry and helps ensure that impact assessment responses are consistent with the information submitted at intake. For more information, see [AI Risk and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-ai-risk-and-compliance-rn.md) and [Intake requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-intake.md).


## Removed in this release

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md) The Autonomous vs. supervised AI tools chart has been removed from the Security &amp; privacy tab.

[Early availability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-all-other-fixes.md)

-   Adding legacy AI connections via Service Graph Connectors \(SGC\) is deprecated. In AI connections, under Legacy connections, the **New** button has been removed to block users from creating new connections using SGC.


## Deprecated features

-   The ability to add hyperscalers from the AICT configuration section is no longer available. You can find any previously created hyperscaler connections in the AI connections section, under Legacy connections.

## Activation information

Install AI Control Tower by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

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

-   **[AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-and-compliance.md)**

    Enable risk and compliance managers to verify organizational compliance with regulations and policies governing AI systems by using the AI Risk and Compliance application, along with the AI Control Tower.

-   **[Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/goal-management-in-alignment-planner-workspace.md)**

    Prioritize, roadmap, and track work when using traditional, agile, or hybrid methodologies with ServiceNow® Strategic Planning. Align strategy to execution by defining and tracking goals across your organization. When the Strategic Planning application is installed, the **AI strategy** tab appears in the AI Control Tower workspace, featuring different widgets for AI strategies, goals, targets, costs of planning items, prioritized work, and RIDAC details.

    Strategic Planning is available with an SPM Professional license.

-   **[Goal Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/goal-framework.md)**

    Create goals, set targets for them, and evaluate the progress of the goals and targets to accomplish your organizational plans and drive business outcomes with the ServiceNow® Goal Framework application. When the Goal Framework application is installed, the **AI strategy** tab appears in the AI Control Tower workspace, featuring different widgets for AI strategies, goals, and targets.

    Goal Framework is available with an SPM Standard license.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/intelligent-experiences-rn-landing.md)

