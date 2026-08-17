---
title: Predictive AI for CSM release notes
description: The ServiceNow Predictive AI for Customer Service Management \(CSM\) applications enable customer service organizations and service operations to configure and implement ServiceNow Otto for Customer Service Management \(CSM\), Guided Decisions, Recommended Actions, and Task Intelligence features. The Predictive AI for CSM applications were enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 12
---

# Predictive AI for CSM release notes

The ServiceNow® Predictive AI for Customer Service Management \(CSM\) applications enable customer service organizations and service operations to configure and implement ServiceNow Otto for Customer Service Management \(CSM\), Guided Decisions, Recommended Actions, and Task Intelligence features. The Predictive AI for CSM applications were enhanced and updated in the Australia release.

## Predictive AI for CSM highlights for the Australia release

[Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-5.md)

-   Starting with Zurich Patch 12, ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Customer Service Management \(CSM\). Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

-   Resolve cases faster with a new case insights section that consolidates key case details, customer history, sentiment scores, and special handling notes into a single view.
-   Use AI to proactively detect emerging issues from case patterns and automatically propose major cases when similar cases trend together.
-   View automated sentiment scores and trends from conversations directly on the email interaction page.
-   Enable customers to make case updates through AI voice agent.
-   Use Live Agent Assist for voice calls to generate recommendations during live voice calls.

[Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)

-   Automatically evaluate post-interaction customer conversations using AI models that score against a configurable quality rubric, eliminating manual effort.
-   Receive intelligent email reply recommendations on extended table record pages in ServiceNow Otto for CSM, helping agents respond faster with less manual effort.

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   Availability of filter controls in Now Assist Guardian for ServiceNow Otto for CSM.
-   Availability of AI Workflow tab in Core UI.

-   Use AI to populate interaction wrap-up codes and notes, saving agents time.
-   Simplify metadata management by granting developer roles and privileges to your granular admin users.

See [Intelligence for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/intelligence-csm.md) for more information.

**Important:** The following applications are available in ServiceNow Store:

-   Now Assist for CSM \(sn\_csm\_gen\_ai\)
-   Guided Decisions Experience \(sn\_ga\_exp\)
-   Recommended Actions \(sn\_nb\_action\)
-   Recommended Actions for Customer Service \(sn\_cs\_nb\_action\)
-   Task Intelligence for Customer Service \(com.snc.csm\_ml\_task\)

For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Recommended Actions - Support for the Now Assist Multi-Content Response \(MCR\) genius model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-configuring-ai-search.md)**

    Recommended Actions now supports the Now Assist Multi-Content Response \(MCR\) genius model. When an author configures a recommendation backed by the MCR model, the agent sees a single MCR recommendation card in the Suggested Actions tab. The card appears in the Recommended Actions Contextual Side Panel in the agent workspace. The MCR recommendation card displays all its content blocks and citations grouped together under that one card.

-   **[Real-time AI assistance for voice interactions using Live Agent Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/add-gd-input-output-playbook.md)**

    Live Agent Assist brings real-time AI assistance to agents during live voice interactions in Agent Workspace. Select the **Get Recommendations** button in the Otto panel during a call. The AI agent determines the customer query from the live call transcript. It generates answers drawn from the customer context such as customer account, interaction history, and relevant knowledge articles. This capability reduces handling time and improves first-contact resolution.

-   **[Add a playbook as an action type in Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/add-gd-input-output-playbook.md)**

    As an admin, you can configure playbooks as an action type in Recommended Actions, and the Recommended Actions rule engine recommends the right playbook based on context. Playbooks surface inline as cards in the Recommended Actions panel in Agent Workspace and walk Agents through branching decision trees for support, sales, and troubleshooting scenarios. Embedded actions such as creating a task or triggering a workflow can be executed from within the playbook in the Recommended Actions panel in Agent Workspace.

-   **[Now Assist for CSM Major Issue Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-na-for-csm-major-issue-management.md)**

    Use AI to proactively detect emerging issues from case patterns and automatically propose major cases when similar cases trend together. The system monitors recent cases for correlated patterns across the product model hierarchy. When it identifies a developing issue that no existing major case covers, it proposes a case as a major case candidate for review. Major issue managers gain earlier visibility into developing case patterns and can escalate to major case status faster, reducing the time customers experience disruption.

-   **[Now Assist for CSM- Case insights section](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-csm-summarize-case.md)**

    Resolve cases faster with a new case insights section that brings together key case details, customer summary, issue history, sentiment scores, and special handling notes in one consolidated view.

-   **[Customer Service Management AI agent collection- Voice-driven case status retrieval and updates:](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/voice-ai-agent.md)**

    Reduce live agent dependency by enabling customers to check open case statuses and submit case updates through guided voice interactions across Genesys, Twilio, NICE, Five9, 3CLogic, and Amazon Connect CCaaS platforms.

-   **[Customer sentiment analysis on email interaction page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/analyze-sentiments-in-now-assist-for-csm.md)**

    View automated sentiment scores and trends from conversation directly on the email interaction page in ServiceNow Otto for CSM. The system reads customer emails and gives a score to show how the customer is feeling, so agents and managers can quickly check the customer's mood without reading the whole conversation.

-   **[Now Assist for CSM Case Playbook for Complaints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/accelerate-complaint-case-handling.md)**

    Replaced the Agent Assist tab in the side panel with a Recommended Actions tab.

-   **[Configure extended tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-extended-table-support-for-the-resolution-notes-skill.md)**

    Automatically receive concise summaries of case resolutions in ServiceNow Otto for CSM, with the extended table, enabling customer agents to quickly understand resolution details and respond to customers.


-   **[Now Assist for CSM- Quality assurance management skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/quality-assurance-management.md)**

    Automatically evaluate agent activity on closed cases using AI models that score each interaction against a configurable quality rubric, eliminating manual sampling and ensuring consistent, objective assessments at scale.

-   **[Now Assist for CSM-Extended table support for email reply recommendation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-extended-table-support-for-the-email-reply-recommendation-skill.md)**

    Automatically receive email reply recommendations on extended table record pages in ServiceNow Otto for CSM, allowing agents to quickly respond to customers, provide intelligent recommendations and reducing manual effort.


-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Now Assist for CSM-AI workflow tab added in Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ai-workflow-pattern-in-customer-service-management.md)**

    Availability of AI Workflow tab within case view of case table records and email interaction view of interaction records in Core UI, showing agentic workflows and actionable AI-driven insights directly in the record UI.

-   **[Now Assist for CSM-Filter controls in Now Assist Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-guardian-csm-filters.md)**

    Availability of filter controls for CSM in the AI Guardian interface, allowing users to toggle the base system filters on and off. Filtered results display in a user-friendly format for quick case review and action.


-   **[Guided Decisions - UI Layout tab for the Guided Decision with inputs/outputs activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/add-gd-input-output-playbook.md)**

    Configure the display of knowledge articles directly from the UI Layout tab by setting a default article height and choosing whether articles appear collapsed by default in the playbook.

-   **[Guided Decisions - Restart option for the Guided Decision with inputs and outputs activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/add-gd-input-output-playbook.md)**

    As an agent, you can restart a Guided Decision with inputs and outputs activity in a playbook by selecting the **Restart Activity** option. This option is available when the activity is in a complete, skipped, or error state and the stage is still in progress.

-   **[Recommended Actions - Search query term available as an action input mapping value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-create-search-result-mapping-for-ai-search.md)**

    Added the search query term as a new pill picker value in the action input mapping for search result configurations. This provides the ability for agents to include the search query term as a guidance input.

-   **[Recommended Actions - Hybrid search in AI search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-hybrid-search.md)**

    Recommended Actions in CSM Configurable Workspace now uses hybrid search, combining keyword and semantic matching to surface more relevant search results in the AI search tab, even when agent queries don't match article content exactly.

-   **[Recommended Actions - View the relevancy score on the Case resolution guidance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/nba-use-ai-search.md)**

    View the relevancy score, which indicates how well a search result matches the agent's query, on the search result recommendation cards in the Search tab of the Recommended Actions panel for the Case resolution guidance.

-   **[Recommended Actions – Configure contextual filtering of AI search results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-configure-contextual-filtering.md)**

    Enhance search accuracy by ensuring results are contextually relevant to the record being viewed by the agent. Search results are dynamically filtered based on contextual information passed through additional context parameters. To configure the contextual filtering of the Search results, enable the dynamic filter for a search source in a Search profile and then create the AisDynamicFilter implementation for the source which holds the filtering conditions.

-   **[Recommended Actions – Support for mandatory Contextual Inputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-csm-create-context-inputs.md)**

    As an RA author, you can mark specific context inputs as mandatory by selecting the Mandatory check box in the Context Inputs form. When one or more context inputs are configured as mandatory, you must set the values for these contextual inputs directly on Recommended Actions component on the record page in the UI Builder for the recommendations to be generated.

-   **[Recommended Actions - Manage and conﬁgure metadata with delegated developer approach](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-csm-installed-components.md)**

    Grant granular admin users delegated developer privileges and required roles to manage and configure metadata. This includes the Manage update set permission, domain\_picker role, and metadata\_scope\_viewer role for viewing and modifying the application scope of metadata records.

-   **[AI interaction wrap-up](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/interaction-wrapup-ai-generated.md)**

    Provides agents with AI assistance during the interaction wrap-up period. This feature generates wrap-up content for interaction records, such as the wrap-up code and notes.

-   **[Process mining - Pre‑configured templates for CSM Process Mining Projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/process-opt-csm.md)**

    Select pre‑configured templates from the Process Mining Content Pack for CSM to quickly set up customer service case projects with default settings already applied. These templates help accelerate project creation by providing standardized configurations tailored for common Customer Service Management scenarios.


## Changed in this release

-   **[Now Assist &gt; ServiceNow Otto announcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sn-ai-implementation-landing.md)**

    ServiceNow Otto® introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


-   **[Now LLM service deprecation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

-   **[Automated quality assurance dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/quality-assurance-management.md)**

    Enable admins to filter scoring parameters and sort agent and case lists. Admins can sort data, manage filters, and easily organize cases on the dashboard with the new sorting, visibility, and skill management capabilities.

-   **[Activate Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-now-assist-for-customer-service-management-csm-skills_0.md)**

    Enable admins to view detailed information about each Now Assist skill to make faster and more informed decisions about enabling skill capabilities.


-   **[Configure knowledge generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-knowledge-generation-in-now-assist_0.md)**

    Enable users with the **sn\_skill\_builder.admin** role to generate knowledge base articles in ServiceNow Otto for CSM by selecting the required input fields from a task record, reducing manual effort and streamlining the knowledge base generation process.

-   **[Configure Sidebar Summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-sidebar-summarization-in-now-assist.md)**

    Enable customer agents to generate summaries built from the required case and task tables in ServiceNow Otto for CSM as default tables can now be pre-selected and locked.

-   **[Provide Customer 360 insights agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-service-management-ai-agent-collection-customer-360.md)**

    Enhanced Provide Customer 360 Insights with Enterprise Graph and AI agent deep research for richer, more contextual query results.

-   **[Triage cases agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/case-resolving-use-case.md)**

    Multilingual and localization flows in the Triage Cases workflow are now fully supported.


## Activation information

Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/t_ActivateCustomerService.md).

Now Assist features are available with activation of the ServiceNow Otto for CSM plugin. For more information, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

Starting with Vancouver Patch 4, ServiceNow Otto for CSM is supported.

Starting with Zurich Patch 7, Customer Service Management AI agent collection is supported. Check your entitlements to determine whether you have access to the ServiceNow Otto for CSM

## Plugin information

-   **Renamed or changed plugins**

    The following plugin has been renamed or changed:

    Recommended Actions for Customer Service \(sn\_cs\_nb\_action\): renamed to Recommended Actions for Service \(sn\_cs\_nb\_action\) starting with v31.0.


## Browser requirements

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/browser-support.md).

## Related ServiceNow applications and features

-   **[Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_CustomerServiceManagement.md)**

    Provide the service and support that your external customers need with Customer Service Management.

-   **[Now Assist for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-rn.md)**

    Summarize customer chat conversations on interactions, summarize case details, and generate case resolution notes with the ServiceNow® ServiceNow Otto for CSM application.

-   **[Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/document-intelligence-landing.md)**

    Extract the data from documents and integrate the data into automation workflows to save time and resources by using the Document Intelligence AI solution.

-   **[Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence-landing.md)**

    Improve processes across the platform, such as automatically populating fields when a case is created, categorizing and routing work, and suggesting case resolutions through Predictive Intelligence AI.

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md)**

    Use the Now Assist admin console to provide you with quick and easy access to the important information that you must set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use this conversational interface in CSM Configurable Workspace to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills.md)**

    Use ServiceNow Otto products to provide generative AI skills to meet the needs of users in different workflows. These skills include case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/customer-service-mgmt-rn-landing.md)

