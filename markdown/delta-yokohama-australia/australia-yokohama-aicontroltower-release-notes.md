---
title: Combined AI Control Tower release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for AI Control Tower from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-aicontroltower-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 22
breadcrumb: [Products combined by family]
---

# Combined AI Control Tower release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for AI Control Tower from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family AI Control Tower release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading AI Control Tower to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Upgrade information**

General availability release, no upgrade.


</td></tr><tr><td>

Zurich

</td><td>

-   **Upgrade information**

For details on upgrading to the redesigned AI Control Tower experience, see the [AI Control Tower Migration \[KB3144679\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3144679) article in Now Support.


</td></tr><tr><td>

Australia

</td><td>

-   **Upgrade information**

For details on upgrading to the redesigned AI Control Tower experience, see the [AI Control Tower Migration \[KB3144679\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3144679) article in Now Support.


</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for AI Control Tower.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Explore AI model providers](https://www.servicenow.com/docs/access?context=ai-model-providers&family=yokohama&ft:locale=en-US)**

Enable choice for third party model providers powering ServiceNow® skills and agents.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Security and privacy tab](https://www.servicenow.com/docs/access?context=security-privacy-tab&family=zurich&ft:locale=en-US)**
    -   Measure whether your model's output or behavior potentially violates predefined LLM guardrail policies using the Data integrity incident detection chart.
    -   Review potential threats in AI agent output in Agent goal deviation, Output with PII detected, and Agentic output injection detection charts.
    -   Monitor MCP server access by AI Gateway with these new charts: Clients connecting to MCP servers, authorized access attempts, and failed access attempts.
-   **[Data section on Configurations page](https://www.servicenow.com/docs/access?context=data&family=zurich&ft:locale=en-US)**

Set up data integrity incident detection, agent goal deviation, and output screening metrics to measure the integrity of your data model and potential threats in LLM output.

-   **[Manage agentic AI system life cycles](https://www.servicenow.com/docs/access?context=create-ai-system-assets&family=zurich&ft:locale=en-US)**

Create AI system assets to track and manage the complete life cycles of your agentic AI systems, from onboarding to deployment. Gain comprehensive insight into each agentic AI system and take any necessary actions to successfully complete each life-cycle stage. By managing the life cycles of your agentic AI systems, you can extend their lifespans, reduce downtime, and optimize licensing costs.

-   **[Define the use and purpose of an AI system](https://www.servicenow.com/docs/access?context=create-ai-system-assets&family=zurich&ft:locale=en-US)**

Specify the intended use and purpose of an AI system. Provide insight into who is using the AI system, what the AI system is being used for, and how the AI system works and provides value. This information can help you determine the benefits and risks that are associated with the AI system. For more information on classifying AI systems based on regulatory risk at intake by applying a configured Risk Assessment Methodology \(RAM\), see [Assessment templates and risk assessment methodologies](https://www.servicenow.com/docs/access?context=assessment-templates-rams&family=zurich&ft:locale=en-US) and [Request an AI use case](https://www.servicenow.com/docs/access?context=request-ai-system&family=zurich&ft:locale=en-US).

-   **[Associate additional related AI asset types with AI systems](https://www.servicenow.com/docs/access?context=create-ai-system-assets&family=zurich&ft:locale=en-US)**

Associate the following additional related AI asset types with your AI systems:

    -   If an AI system has an Asset type of Generative AI or Agentic AI, you can associate it with any of its supported components or subsystems.
    -   If an AI system has an Asset type of Agentic AI, you can associate it with any of its integrated AI tools.
-   **[Create change and offboarding requests for additional AI asset types](https://www.servicenow.com/docs/access?context=creating-ai-asset-requests&family=zurich&ft:locale=en-US)**

Create change requests for the following additional AI asset types:

    -   AI systems with an Asset type of Agentic AI
    -   Datasets
In addition, create offboarding requests for the following additional AI asset types:

    -   AI systems with an Asset type of Agentic AI
    -   AI models
    -   Datasets
    -   MCP servers

</td></tr><tr><td>

Australia

</td><td>

-   **[Security &amp; privacy tab in AI Governance](https://www.servicenow.com/docs/access?context=security-privacy-tab&family=australia&ft:locale=en-US)**
    -   Customize the AI asset security score by weighting LLM guardrail categories that comprise the score. The score formula was changed to an average across all AI assets. The score was renamed to the AI asset security score.
    -   Measure whether your model's output or behavior potentially violates predefined LLM guardrail policies using the Data integrity incident detection chart.
    -   Review potential threats in AI agent output in Agent goal deviation, output with PII detected, and Agentic output injection detection charts.
    -   Monitor MCP server access by AI Gateway with these new charts: Clients connecting to MCP servers, authorized access attempts, and failed access attempts.
    -   The Prompt injection, Offensive content, and Sensitive data tabs have been removed and replaced by the **Access** and **Guardrails** tabs. Metrics have been reorganized into those two tabs.
    -   In **Configurations**, under **Data**, the **Data privacy** tab was renamed to **Security &amp; privacy**. In that tab, the data leak detection and anonymization section was renamed to sensitive data input and anonymization.
-   **[Data section on Configurations page](https://www.servicenow.com/docs/access?context=data&family=australia&ft:locale=en-US)**

Enable and set up data integrity incident detection, agent goal deviation, and output screening metrics. These metrics measure the integrity of your data model and potential threats in LLM output.

-   **[Manage agentic AI system life cycles](https://www.servicenow.com/docs/access?context=create-ai-system-assets&family=australia&ft:locale=en-US)**

Create AI system assets to track and manage the complete life cycles of your agentic AI systems, from onboarding to deployment. Gain comprehensive insight into each agentic AI system and take any necessary actions to successfully complete each life-cycle stage. By managing the life cycles of your agentic AI systems, you can extend their lifespans, reduce downtime, and optimize licensing costs.

-   **[Define the use and purpose of an AI system](https://www.servicenow.com/docs/access?context=create-ai-system-assets&family=australia&ft:locale=en-US)**

Specify the intended use and purpose of an AI system. Provide insight into who is using the AI system, what the AI system is being used for, and how the AI system works and provides value. This information can help you determine the benefits and risks that are associated with the AI system. For more information on classifying AI systems based on regulatory risk at intake by applying a configured Risk Assessment Methodology \(RAM\), see, [AI Risk and Compliance release notes](https://www.servicenow.com/docs/access?context=grc-ai-risk-and-compliance-rn&family=australia&ft:locale=en-US) [Assessment templates](https://www.servicenow.com/docs/access?context=airc-assessment-templates&family=australia&ft:locale=en-US)and [Risk assessment methodologies](https://www.servicenow.com/docs/access?context=airc-rams&family=australia&ft:locale=en-US).

-   **[Associate additional related AI asset types with AI systems](https://www.servicenow.com/docs/access?context=create-ai-system-assets&family=australia&ft:locale=en-US)**

Associate the following additional related AI asset types with your AI systems:

    -   If an AI system has an Asset type of generative AI or agentic AI, you can associate it with any of its supported components or subsystems.
    -   If an AI system has an Asset type of agentic AI, you can associate it with any of its integrated AI tools.
-   **[Create change and offboarding requests for additional AI asset types](https://www.servicenow.com/docs/access?context=creating-ai-asset-requests&family=australia&ft:locale=en-US)**

Create change requests for the following additional AI asset types:

    -   AI systems with an Asset type of agentic AI
    -   Datasets
In addition, create offboarding requests for the following additional AI asset types:

    -   AI systems with an Asset type of agentic AI
    -   AI models
    -   Datasets
    -   MCP servers
-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing AI Control Tower features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&family=yokohama&ft:locale=en-US)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Zurich

</td><td>

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Drop-down menu for associating AI assets with related assets](https://www.servicenow.com/docs/access?context=view-ai-assets-lifecycle-stage&family=zurich&ft:locale=en-US)**

The **Add new** button in AI asset creation forms and records is now the **Add from inventory** drop-down menu. Select **Add from inventory** to associate an AI asset with a related asset that already exists in your inventory. Select **Create** to associate it with a related asset that doesn't exist in your inventory yet.

-   **[Editable asset details fields on the Details tab of AI asset records](https://www.servicenow.com/docs/access?context=view-ai-assets-lifecycle-stage&family=zurich&ft:locale=en-US)**

You can now modify asset details fields directly on the **Details** tab of your AI asset records.

-   **[Related asset lists in AI asset records](https://www.servicenow.com/docs/access?context=view-ai-assets-lifecycle-stage&family=zurich&ft:locale=en-US)**

The lists of related assets in each AI asset record has moved from the **Related assets** tab to the **Details** tab.


 -   **[Security and privacy tab](https://www.servicenow.com/docs/access?context=security-privacy-tab&family=zurich&ft:locale=en-US)**
    -   The Autonomous vs. supervised AI tools chart has been removed.
    -   The Prompt injection, Offensive content, and Sensitive data tabs have been removed and replaced by Access and Guardrails tabs. Metrics have been reorganized into those two tabs.
    -   In **Configurations**, under **Data**, the **Data privacy** tab was renamed to **Security &amp; privacy**. In that tab, the data leak detection and anonymization section was renamed to sensitive data input and anonymization.

</td></tr><tr><td>

Australia

</td><td>

-   **[AI record type label](https://www.servicenow.com/docs/access?context=view-ai-assets-lifecycle-stage&family=australia&ft:locale=en-US)**

The AI assets \(sn\_grc\_ai\_gov\_ai\_system\) table has been renamed to AI records \(sn\_grc\_ai\_gov\_ai\_system\). The **Record type** field on AI system, AI model, and dataset records in the AI Control Tower inventory now displays **AI record** instead of the previous asset-specific labels.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some AI Control Tower features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some AI Control Tower features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

AI Gateway application is deprecated from the Yokohama release and are no longer supported.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Now LLM Service deprecation notice](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=zurich&ft:locale=en-US)**

Starting with the September 2026 release, Now LLM Service is being prepared for future deprecation. The Now LLM Service is no longer the default model provider for new or inactive AI assets, and it is no longer selected by default in AI Control Tower. A third-party LLM is now selected by default for AI assets, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Australia

</td><td>

-   AI Control Tower \(legacy\) removed in [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US):

The Autonomous vs. supervised AI tools chart has been removed from the Security &amp; privacy tab.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate AI Control Tower.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Activation information**

The AI Control Tower application is installed as part of the generative AI Controller.


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install AI Control Tower by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install AI Control Tower by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for AI Control Tower we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for AI Control Tower we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Browser requirements**

The AI Control Tower application supports all the browsers.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for AI Control Tower, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Accessibility information**

The AI Control Tower application supports all the platform accessibility features.


</td></tr><tr><td>

Zurich

</td><td>

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for AI Control Tower we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Localization information**
    -   **[Yokohama Patch 3](https://www.servicenow.com/docs/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)**

The AI Control Tower application isn’t localized


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for AI Control Tower we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

[Yokohama Patch 11](https://www.servicenow.com/docs/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   AI connections are introduced in AI Control Tower using Service Graph Connectors. AI connections are combination of hyperscalars, AI apps, and agentic AI frameworks. The AI Service Graph Connectors available from March 2026:
    -   [AWS](https://www.servicenow.com/docs/access?context=aws_0&family=yokohama&ft:locale=en-US)
    -   [Microsoft](https://www.servicenow.com/docs/access?context=microsoft&family=yokohama&ft:locale=en-US)- Azure Foundry and Copilot
    -   [n8n](https://www.servicenow.com/docs/access?context=n8n&family=yokohama&ft:locale=en-US)
    -   [GCP Vertex AI](https://www.servicenow.com/docs/access?context=gcp-vertex-ai&family=yokohama&ft:locale=en-US)
    -   [LangGraph](https://www.servicenow.com/docs/access?context=langgraph&family=yokohama&ft:locale=en-US)
    -   [Salesforce](https://www.servicenow.com/docs/access?context=salesforce&family=yokohama&ft:locale=en-US)

 [Yokohama Patch 6](https://www.servicenow.com/docs/access?context=yokohama-patch-6&family=yokohama&ft:locale=en-US)

-   Monitor the performance of guardrails enabled through AI Guardian using the Health tab.
-   Measure and improve the quality of interactions with virtual agents using the Evaluation tab.

 [Yokohama Patch 3](https://www.servicenow.com/docs/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)

-   AI Control Tower helps customers manage and oversee performance, risk profile &amp; workforce transformation while also helping to seamlessly embed AI into enterprise strategy.

 -   -   Create an AI steward role.
-   Use the AI Asset inventory to catalog AI-related artifacts.
-   Use the AI skills Approvals to review and approval flows.
-   Create a AI Control Tower Workspace.

</td></tr><tr><td>

Zurich

</td><td>

AI Control Tower highlights in Zurich patch 13:

-   Detect unsanctioned AI usage across your enterprise and apply policies to control it.
-   Apply policies to block AI activity and respond to AI threats.
-   Add evaluation metrics for a specific AI system without changing your organization's global metric configuration.
-   Discard session, trace, and span data to reduce storage usage, while retaining quality and safety scores.
-   Use AI Control Tower on a domain-separated instance.
-   Starting in the September 2026 release, AI Gateway is available in AI Control Tower.
-   The MCP and CIMD registered clients can be edited to update their configuration from the AI Gateway Setup tab.
-   The AI Gateway proxy URL format has changed. The new format is:

`https://<instance-url>/sncapps/aigw/mcp/<mcp-server>`

Previously, the URL format was:

`https://<instance-url>/sncapps/awh/<mcp-server>/mcp`


 AI Control Tower highlights in [Zurich Patch 11](https://www.servicenow.com/docs/access?context=zurich-patch-11&family=zurich&ft:locale=en-US):

-   Manage your AI governance work in a redesigned AI Control Tower experience that lets you find information and complete tasks using natural language.
-   Resolve important issues using auto-generated recommendations and AI insights that direct your attention to the AI governance work that matters most.
-   Detect quality and safety regressions in AI systems before they escalate, using automated scoring and trend analysis for AI interactions in production.
-   Use ServiceNow Otto premium chat in AI Control Tower for a better conversational experience with unified search and chat capabilities, including integrated web search and file uploads.
-   Contain rogue AI agents by using kill switch protocol to limit damage, preserve your security posture, and provide business continuity for your users.
-   Make a managed AI agent discoverable to external systems by publishing it to the External Registry. The Microsoft integration provides two methods to publish an agent so that Microsoft can discover it.
    -   Publish agents from the AI asset record page.
    -   Publish agents while onboarding an asset.
-   Detect AI assets in your inventory that perform the same function using deduplication. Deduplication enables AI stewards to review and consolidate redundant entries instead of governing them independently.
-   ServiceNow Otto is the new AI experience brand. This change is reflected in AI Control Tower. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
-   The AI Control Tower home page includes a Guided Setup widget that walks you through the initial configuration of AI Control Tower.
-   AI Service Graph Connectors integrate with AI Control Tower to create AI connections for discovering AI assets and tracking data usage. For information about connectors, prerequisites, and the configuration process, see [AI Control Tower- AI Discovery Connectors \[KB2986990\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB2986990) article in the Now Support Knowledge Base.
-   AI Service Graph Connectors and versions available for August 2026 release:
    -   AI Service Graph Connector for Microsoft \(version 3.1.6\)
    -   AI Service Graph Connector for GCP Vertex AI \(version 1.2.3\)
    -   AI Service Graph Connector for Anthropic \(version 2.0.6\)

 AI Control Tower \(legacy\) highlights in [Zurich Patch 8](https://www.servicenow.com/docs/access?context=zurich-patch-8&family=zurich&ft:locale=en-US): Configure and create automation rules to set AI assets as managed assets.

 AI Control Tower \(legacy\) highlights in [Zurich Patch 7](https://www.servicenow.com/docs/access?context=zurich-patch-7&family=zurich&ft:locale=en-US):

-   Use new security metrics to monitor your LLM and AI agent output for potential security and content policy violations, potential PII, and other potential threats.
-   Gain visibility into MCP client-server interactions routed through this instance’s AI Gateway.
-   AI assets—Including AI models, AI systems, prompts, datasets, and MCP servers can be categorized as either managed or unmanaged. Managed assets benefit from AI Control Tower features such as governance, lifecycle management, value assessment, risk classification, security, and privacy. Unmanaged assets, on the other hand, don’t have access to these AI Control Tower capabilities.
-   AI connections are introduced in AI Control Tower using Service Graph Connectors. AI connections are a combination of hyperscalars, AI apps, and agentic AI frameworks. The AI Service Graph Connectors available from March 2026:
    -   [AWS](https://www.servicenow.com/docs/access?context=aws_0&family=zurich&ft:locale=en-US)
    -   [Microsoft](https://www.servicenow.com/docs/access?context=microsoft&family=zurich&ft:locale=en-US)- Azure Foundry and Copilot
    -   [Google Cloud Platform \(GCP\) Vertex AI](https://www.servicenow.com/docs/access?context=gcp-vertex-ai&family=zurich&ft:locale=en-US)
    -   [n8n](https://www.servicenow.com/docs/access?context=n8n&family=zurich&ft:locale=en-US)
    -   [LangGraph](https://www.servicenow.com/docs/access?context=langgraph&family=zurich&ft:locale=en-US)
    -   [Salesforce](https://www.servicenow.com/docs/access?context=salesforce&family=zurich&ft:locale=en-US)
-   Manage the end-to-end life cycles of your agentic AI systems.
-   Define the intended use and purpose of an AI system so that you can determine its benefits and risks.
-   AI Gateway offers MCP Global Clients, which can be used across all servers.
-   AI Gateway offers MCP Catalog to choose while adding MCP servers.
-   MCP server can be added to an AI Asset inventory from AI Control Tower.

 AI Control Tower \(legacy\) highlights in [Zurich Patch 5](https://www.servicenow.com/docs/access?context=zurich-patch-5&family=zurich&ft:locale=en-US): Review changes to Now Assist usage measurement.

 AI Control Tower \(legacy\) highlights in [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US):

-   Identify ServiceNow® AI assets that impact your security posture using the ServiceNow® AI security score and AI insights.
-   Access and monitor security for AWS Bedrock agents running as privileged users, autonomous vs. Supervised tools, and dormant agents.
-   Monitor sensitive data detection, prompt injection, and offensive content metrics to help identify and mitigate AI-driven security and compliance risks before they impact workflows or expose sensitive information.
-   See more details in the access map about agent access issues to help you troubleshoot quickly.
-   Audit logs capture configuration changes made on Data, Approvals, and AI model providers categories.
-   Discover AI assets built and deployed in Google Cloud Platform \(GCP\) Vertex AI, Copilot Studio, and Azure AI Foundry.
-   AI Gateway enables enterprises to actively manage, govern, and observe their MCP traffic, ensuring secure operation of agentic workflows across enterprise boundaries.

 AI Control Tower \(legacy\) highlights in [Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US):

-   Monitor the performance of guardrails enabled through AI Guardian using the **Health** tab.
-   Measure and improve the quality of interactions with virtual agents using the **Evaluation** tab.
-   Display data based on the chosen allowed model providers and the status of the fallback in the Impact Summary table on the AI model providers section.
-   Synchronize AI agents automatically when an AI asset is synchronized.

 AI Control Tower \(legacy\) highlights in Zurich:

-   Enhance the Product Owner experience with a personalized home page, value management tools to manage AI investments, and enhanced visibility into AI assets to simplify task management.
-   Evaluate AI productivity and adoption across the enterprise using defined value metrics and performance indicators to drive data-informed decisions and maximize AI impact.
-   Access and security monitoring for ServiceNow® AI agents, especially around access issues, agents running as privileged users and dormant agents.
-   Discover AI assets built and deployed in AWS Bedrock and Azure Foundry.
-   Enable choice for third-party model providers powering ServiceNow® skills and agents.
-   Access to aggregated risk scores to improve decision-making, manage risks, and help to promote ethical and transparent AI practices.
-   Monitor performance, track progress, and make informed decisions related to your AI strategies, goals, targets, and the associated work from the **AI strategy** tab.
-   Track costs of your AI projects, epics, demands, and track key project risks, issues, decisions, actions, and changes from the **AI strategy** tab.

 For more information on the new AI Control Tower experience, see [AI Governance](https://www.servicenow.com/docs/access?context=aict-landing&family=zurich&ft:locale=en-US).

 For more information on the legacy AI Control Tower experience, see [AI Governance \(legacy\)](https://www.servicenow.com/docs/access?context=ai-control-tower-landing&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

AI Control Tower highlights in Australia patch 6:

-   Detect unsanctioned AI usage across your enterprise and apply policies to control it.
-   Apply policies to block AI activity and respond to AI threats.
-   Add evaluation metrics for a specific AI system without changing your organization's global metric configuration.
-   Discard session, trace, and span data to reduce storage usage, while retaining quality and safety scores.
-   Use AI Control Tower on a domain-separated instance.
-   AI Inventory Intelligence Agent analyzes the AI asset inventory, identifies assets with incomplete metadata, and generates enrichment recommendations to improve data quality and governance readiness.
-   The GCP Vertex AI connector is renamed to Gemini Enterprise Platform Agent
-   The AI Service Graph Connector for GCP application is renamed to AI Service Graph Connector for Google.
-   The Salesforce connector is renamed to AI Connector for Salesforce.
-   The Microsoft connector introduces A365 agent platform to discover and import AI assets into ServiceNow AI Control Tower.
-   Starting in the September 2026 release, AI Gateway is available in AI Control Tower.
-   The MCP and CIMD registered clients can be edited to update their configuration from the AI Gateway Setup tab.
-   The AI Gateway proxy URL format has changed. The new format is:

`https://<instance-url>/sncapps/aigw/mcp/<mcp-server>`

Previously, the URL format was:

`https://<instance-url>/sncapps/awh/<mcp-server>/mcp`


 AI Control Tower highlights in [Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US):

-   Manage your AI governance work in a redesigned AI Control Tower experience that lets you find information and complete tasks using natural language.
-   Resolve important issues using auto-generated recommendations and AI insights that direct your attention to the AI governance work that matters most.
-   Detect quality and safety regressions in AI systems before they escalate, using automated scoring and trend analysis for AI interactions in production.
-   Use ServiceNow Otto premium chat in AI Control Tower for a better conversational experience with unified search and chat capabilities, including integrated web search and file uploads.
-   Contain rogue AI agents by using kill switch protocol to limit damage, preserve your security posture, and provide business continuity for your users.
-   Make a managed AI agent discoverable to external systems by publishing it to the External Registry. The Microsoft integration provides two methods to publish an agent so that Microsoft can discover it.
    -   Publish agents from the AI asset record page.
    -   Publish agents while onboarding an asset.
-   Detect AI assets in your inventory that perform the same function using deduplication. Deduplication enables AI stewards to review and consolidate redundant entries instead of governing them independently.
-   ServiceNow Otto is the new AI experience brand. This change is reflected in AI Control Tower. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
-   The AI Control Tower home page includes a Guided Setup widget that walks you through the initial configuration of AI Control Tower.
-   AI Service Graph Connectors integrate with AI Control Tower to create AI connections for discovering AI assets and tracking data usage. For information about connectors, prerequisites, and the configuration process, see [AI Control Tower- AI Discovery Connectors \[KB2986990\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB2986990) article in the Now Support Knowledge Base.
-   AI Service Graph Connectors and versions available for August 2026 release:
    -   AI Service Graph Connector for Microsoft \(version 3.1.7\)
    -   AI Service Graph Connector for GCP Vertex AI \(version 1.2.4\)
    -   AI Service Graph Connector for Anthropic \(version 2.0.7\)
-   Model Preview Program \(MPP\) is an opt-in program that gives eligible users an early access to AI models that aren't yet Generally Available \(GA\).

 AI Control Tower \(legacy\) highlights in [Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US):

-   The AI asset list in AI Inventory includes Asset State and Asset Status columns.
-   The system assigns a unique ID to every asset. The ID appears in the Asset tag field under Asset details.
-   AI Service Graph Connectors for OpenAI, Moveworks, IBM, and OCI are available in AI Control Tower for AI connections.
-   The AI Service Graph Connector for OpenAI discovers AI models and tracks model usage.
-   When you mark a managed asset as unmanaged, the asset's active workflows, tasks, and governance processes are canceled, and the asset is excluded from value tracking.
-   When you mark an unmanaged asset as managed, the asset is actively monitored and governed, making it visible and eligible for governance workflows and value tracking.

 AI Control Tower \(legacy\) highlights in [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US):

-   Customize the AI asset security score calculation to reflect your security requirements.
-   Use new security metrics to monitor your LLM and AI agent output for potential security and content policy violations, potential PII, and other potential threats.
-   Gain visibility into MCP client-server interactions routed through this instance's AI Gateway.
-   Configure and create automation rules to set AI assets as managed assets.
-   Manage the end-to-end life cycles of your agentic AI systems.
-   Define the intended use and purpose of an AI system so that you can determine its benefits and risks.

 AI Control Tower \(legacy\) highlights in [Early availability](https://www.servicenow.com/docs/access?context=australia-all-other-fixes&family=australia&ft:locale=en-US):

-   AI assets—including AI models, AI systems, prompts, datasets, and MCP servers can be categorized as either managed or unmanaged.
-   AI connections are introduced in AI Control Tower using Service Graph Connectors \(SGC\).
-   The AI model providers supported by ServiceNow contains providers such as Now LLM Service, AWS Claude, Now LLM LTS model, and so on.
-   The AI model providers configured by your organization contains providers such as Perplexity, IBM Watson, and so on.
-   AI Gateway offers Global MCP clients, which once created can be used across all MCP servers.
-   AI Gateway offers MCP Catalog to choose while adding MCP servers into AI Control Tower.

 For more information on the new AI Control Tower experience, see [AI Governance](https://www.servicenow.com/docs/access?context=aict-landing&family=australia&ft:locale=en-US).

 For more information on the legacy AI Control Tower experience, see [AI Governance \(legacy\)](https://www.servicenow.com/docs/access?context=ai-control-tower-landing&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

