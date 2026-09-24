---
title: Combined Predictive AI for CSM release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Predictive AI for CSM from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/delta-yokohama-australia/australia-yokohama-predictiveaiforcsm-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 20
breadcrumb: [Products combined by family]
---

# Combined Predictive AI for CSM release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Predictive AI for CSM from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Predictive AI for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Predictive AI for CSM to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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
</table>## New features

Between your current release family and Australia, new features were introduced for Predictive AI for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Recommended Actions – AI search on CSM default record page, Front line case page, and CSM interaction record page](https://www.servicenow.com/docs/access?context=ra-csm-ai-search&family=yokohama&ft:locale=en-US)**

The Recommended Actions – AI search is introduced on the [CSM default record page](https://www.servicenow.com/docs/access?context=csm-default-record-page&family=yokohama&ft:locale=en-US), [Front-line case page](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&family=yokohama&ft:locale=en-US), and [CSM Interaction record page](https://www.servicenow.com/docs/access?context=csm-interaction-record-page&family=yokohama&ft:locale=en-US) \(for the chat, video, walk-up, and email type channels\) and it’s enabled by default for new customers. The default guidance is also enabled for these pages. Agents can attach and share knowledge article links in comments, work notes, and emails.

-   **[Recommended Actions - Catalog item source type for AI search](https://www.servicenow.com/docs/access?context=ra-csm-ai-search&family=yokohama&ft:locale=en-US)**

Search and filter the catalog items easily in the AI search tab of Recommended Actions in the CRM Workspace.

-   **[Recommended Actions - Ability to have multiple active contexts for the same table](https://www.servicenow.com/docs/access?context=ra-csm-contexts&family=yokohama&ft:locale=en-US)**

Enables multiple active contexts for the same table, so that tailored recommendations are displayed in the CRM Workspace:

    -   For different user personas based on their requirements.
    -   For different Predictive Intelligence models or AI model variants.
    -   For the same record in different channels, such as chat, email, and so on.
-   **[Recommended Actions - Ability to inherit active rules and their recommendations from a parent table context to extended table context](https://www.servicenow.com/docs/access?context=ra-csm-contexts&family=yokohama&ft:locale=en-US)**

Assign the active rules and their recommendations from the parent table context to the extended context table for a streamlined process.

-   **[Recommended Actions - Asynchronous evaluation for recommendations](https://www.servicenow.com/docs/access?context=ra-csm-contexts&family=yokohama&ft:locale=en-US)**

Enables you to configure loading behavior at the context level by choosing between synchronous and asynchronous modes. In the asynchronous mode, recommendations load in the background without blocking the UI, allowing agents to interact with the record immediately.


 -   **[Recommended Actions - Front-line case page integration with knowledge guidance](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&family=yokohama&ft:locale=en-US)**

Enable agents to attach and share knowledge article links in comments, work notes, or emails by using modeless dialogs.

-   **[Recommended Actions - Default guidance for search results](https://www.servicenow.com/docs/access?context=ra-csm-guidances-default-guidance-search&family=yokohama&ft:locale=en-US)**

Enable agents to view search results for any records. Use a default guidance for any search sources that don't have a dedicated, mapped guidance.

-   **[Recommended Actions - Improved timeout handling for resource generators](https://www.servicenow.com/docs/access?context=ra-csm-resource-generators&family=yokohama&ft:locale=en-US)**

Handle timeout errors when calling Machine Learning \(ML\) resource generators. The system uses a subflow API with a 1-second timeout ensures the RA generation engine prioritizes faster response times by terminating stalled ML prediction calls.

-   **[Recommended Actions - Custom guidances](https://www.servicenow.com/docs/access?context=ra-csm-custom-guidances&family=yokohama&ft:locale=en-US)**

Use a custom guidance to provide actions that are based on the search results from the Case, Problem, Incident, or Change Request tables. Agents can use these actions to link records to the current case and copy resolution codes and notes from resolved cases.

-   **[Recommended Actions - Field values for predicted records](https://www.servicenow.com/docs/access?context=ra-csm-guidances&family=yokohama&ft:locale=en-US)**

Leverage the actual field value for a predicted record and show it in a custom guidance in place of the display value.

-   **[Recommended Actions for Customer Service - Display Recommended Actions on the CSM Interaction record page](https://www.servicenow.com/docs/access?context=ra-csm-chat-interaction-record&family=yokohama&ft:locale=en-US)**

Enable agents to view Recommended Actions in the contextual side panel on the CSM Interaction record page. The search tab dynamically displays relevant actions based on the context of the chat interaction.

-   **[Recommended Actions for Customer Service - Interaction Context record](https://www.servicenow.com/docs/access?context=ra-csm-context-records&family=yokohama&ft:locale=en-US)**

Use the Interaction Context record to display the search results from the Knowledge table. The results are based on the interaction's short description. This context record includes a search-mapping record that maps knowledge results to the Share KB in chat interactions guidance.


 -   **[Recommended Actions - Question font size customization for a Decision tree](https://www.servicenow.com/docs/access?context=configure-decision-trees-gdb&family=yokohama&ft:locale=en-US)**

Enables you to customize the font size of questions in a Decision tree for a better look and feel. This font size is applied to the questions in the decision trees of playbooks, and recommendations, within the CRM Workspace and service portal.

-   **[Recommended Actions - Control the visibility of completed guidance information](https://www.servicenow.com/docs/access?context=create-guidances&family=yokohama&ft:locale=en-US)**

Allows you to manage the visibility of the completed guidance history information of a decision tree in playbooks, and recommendations for an agent, within the CRM Workspace, and service portal for a streamlined experience.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Guided Decisions - Enable Guided Decisions as a Playbook Activity with Inputs and Outputs](https://www.servicenow.com/docs/access?context=add-gd-input-output-playbook&family=zurich&ft:locale=en-US)**

Added support for the Guided Decision with Inputs and Outputs activity in Playbook. Use this activity to embed decision trees that accept inputs and generate outputs, guiding users through complex decisions within your playbooks.


 -   **[Recommended Actions - Filter search results across multiple sources in the Contextual side panel](https://www.servicenow.com/docs/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

Filter search results corresponding to multiple sources in the AI search tab of the Recommended Actions contextual side panel. You can also filter the search results at the facet-level.

-   **[Recommended Actions – Track the AI search usage trends with the AI search analytics dashboard](https://www.servicenow.com/docs/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

Track and analyze the AI search usage in Recommended Actions using the AI search analytics dashboard. The AI search events and actions performed by the agent are captured in the Search Events, Search Source Events, Search Signal Events, Search Result Event, and Search Result Event Action tables. This data is used in the AI search analytics dashboard.

-   **[Recommended Actions - Read-only access to TI solutions for the Resource Generator author role](https://www.servicenow.com/docs/access?context=ra-csm-installed-components&family=zurich&ft:locale=en-US)**

Access Task Intelligence \(TI\) solution definitions in read-only mode as a Resource Generator author \[sn\_nb\_action.resource\_generator\_author\] to configure recommendations with Machine Learning \(ML\) solutions from TI models. In other words, the sn\_ti\_admin.tia\_user role is added to the Resource Generator author role.


 -   **[Recommended Actions - Filter search results across multiple sources on the Search page](https://www.servicenow.com/docs/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

Filter search results corresponding to multiple sources on the Search page. You can also filter the search results at facet-level.


 -   **[Recommended Actions - View the relevancy score of the AI search results](https://www.servicenow.com/docs/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

View the relevancy score on the search result recommendation cards in the Search tab of the Recommended Actions panel for the default guidance for search results, Attach and share article, Share KB in chat interactions, and all no-code \( Link incident to current case, Link problem to current case, and Link change request to current case\) guidances. To enable this feature, you must enable the Show relevancy score for results check box in the Context form.

-   **[Recommended Actions – Limit the number of search results for more precise output](https://www.servicenow.com/docs/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

Limit the number of search results \(Top N\) that appear in the AI search tab in the Recommended Actions context side panel. To configure top N search results, you must enable the Top N check box in the Context form and then define the Search Results Limit in the Search Application Configuration.

-   **[Recommended Actions - Optimize the Recommended Actions refresh behavior by excluding non-critical field updates](https://www.servicenow.com/docs/access?context=ra-csm-contexts-create&family=zurich&ft:locale=en-US)**

Exclude the non-critical fields from triggering a Recommended Actions refresh on the record pages by adding the non-critical fields to the **Exclude fields** field on a context record. In a child context, you can also include the field exclusions of the parent context. You can enhance a user’s UI experience when you prevent excessive UI updates and still ensure that relevant updates trigger as intended.

-   **[Recommended Actions - Trigger Refresh for Recommendations explicitly or based on UI events](https://www.servicenow.com/docs/access?context=ra-csm-config-data-broker&family=zurich&ft:locale=en-US)**

Trigger recommendations refresh in the Recommended Actions tab on the contextual side panel when a UI or back-end event update is made. This provides dynamic and more contextually relevant recommendations based on the outcome of UI and back-end events. To trigger a recommendations refresh:

    -   configure UI component’s Data Broker in the UI builder for UI events
    -   execute the ForceRefreshRecommendationsscript include for back-end events
-   **[Recommended Actions - Configure dynamic JSON-based context inputs](https://www.servicenow.com/docs/access?context=ra-csm-create-context-inputs&family=zurich&ft:locale=en-US)**

Configure JSON-based context inputs in a context to populate accurate recommendations corresponding to dynamically changing contexts. You can conﬁgure parameters associated with the context table along with context table parameters. To support scenarios where a single workflow may leverage multiple active contexts simultaneously to generate recommendations. This uses the context inputs in rule condition builders, resource generators, and recommendation-action mappings, with minimal performance impact and backward compatibility.

-   **[Recommended Actions - Enhanced KB article sharing for Agents](https://www.servicenow.com/docs/access?context=ra-csm-guidances-attach-share-article&family=zurich&ft:locale=en-US)**

Identify the Knowledge Base \(KB\) articles that are not accessible to the case requester with the help of a Lock icon. In the recommendations on the contextual side panel of the CRM Workspace, a Lock icon on a recommendation card denotes that the recommended KB article cannot be accessed by the case requester.

-   **[Process Mining - SLA breach analysis](https://www.servicenow.com/docs/access?context=csm-integration-po&family=zurich&ft:locale=en-US)**

Identify and analyze cases where service level agreements \(SLAs\) have been violated. The SLA breach analysis project provides insights into the root causes of breaches, highlights bottlenecks, and recommends improvements to optimize the performance of your processes.

-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&family=zurich&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Australia

</td><td>

-   **[Recommended Actions - Support for the Now Assist Multi-Content Response \(MCR\) genius model](https://www.servicenow.com/docs/access?context=ra-configuring-ai-search&family=australia&ft:locale=en-US)**

Recommended Actions now supports the Now Assist Multi-Content Response \(MCR\) genius model. When an author configures a recommendation backed by the MCR model, the agent sees a single MCR recommendation card in the Suggested Actions tab. The card appears in the Recommended Actions Contextual Side Panel in the agent workspace. The MCR recommendation card displays all its content blocks and citations grouped together under that one card.


 -   **[Real-time AI assistance for voice interactions using Live Agent Assist](https://www.servicenow.com/docs/access?context=add-gd-input-output-playbook&family=australia&ft:locale=en-US)**

Live Agent Assist brings real-time AI assistance to agents during live voice interactions in Agent Workspace. Select the **Get Recommendations** button in the Otto panel during a call. The AI agent determines the customer query from the live call transcript. It generates answers drawn from the customer context such as customer account, interaction history, and relevant knowledge articles. This capability reduces handling time and improves first-contact resolution.

-   **[Add a playbook as an action type in Recommended Actions](https://www.servicenow.com/docs/access?context=add-gd-input-output-playbook&family=australia&ft:locale=en-US)**

As an admin, you can configure playbooks as an action type in Recommended Actions, and the Recommended Actions rule engine recommends the right playbook based on context. Playbooks surface inline as cards in the Recommended Actions panel in Agent Workspace and walk Agents through branching decision trees for support, sales, and troubleshooting scenarios. Embedded actions such as creating a task or triggering a workflow can be executed from within the playbook in the Recommended Actions panel in Agent Workspace.


 -   **[Now Assist for CSM Major Issue Management](https://www.servicenow.com/docs/access?context=configure-na-for-csm-major-issue-management&family=australia&ft:locale=en-US)**

Use AI to proactively detect emerging issues from case patterns and automatically propose major cases when similar cases trend together. The system monitors recent cases for correlated patterns across the product model hierarchy. When it identifies a developing issue that no existing major case covers, it proposes a case as a major case candidate for review. Major issue managers gain earlier visibility into developing case patterns and can escalate to major case status faster, reducing the time customers experience disruption.

-   **[Now Assist for CSM- Case insights section](https://www.servicenow.com/docs/access?context=now-assist-csm-summarize-case&family=australia&ft:locale=en-US)**

Resolve cases faster with a new case insights section that brings together key case details, customer summary, issue history, sentiment scores, and special handling notes in one consolidated view.

-   **[Customer Service Management AI agent collection- Voice-driven case status retrieval and updates:](https://www.servicenow.com/docs/access?context=voice-ai-agent&family=australia&ft:locale=en-US)**

Reduce live agent dependency by enabling customers to check open case statuses and submit case updates through guided voice interactions across Genesys, Twilio, NICE, Five9, 3CLogic, and Amazon Connect CCaaS platforms.

-   **[Customer sentiment analysis on email interaction page](https://www.servicenow.com/docs/access?context=analyze-sentiments-in-now-assist-for-csm&family=australia&ft:locale=en-US)**

View automated sentiment scores and trends from conversation directly on the email interaction page in ServiceNow Otto for CSM. The system reads customer emails and gives a score to show how the customer is feeling, so agents and managers can quickly check the customer's mood without reading the whole conversation.

-   **[Now Assist for CSM Case Playbook for Complaints](https://www.servicenow.com/docs/access?context=accelerate-complaint-case-handling&family=australia&ft:locale=en-US)**

Replaced the Agent Assist tab in the side panel with a Recommended Actions tab.

-   **[Configure extended tables](https://www.servicenow.com/docs/access?context=configure-extended-table-support-for-the-resolution-notes-skill&family=australia&ft:locale=en-US)**

Automatically receive concise summaries of case resolutions in ServiceNow Otto for CSM, with the extended table, enabling customer agents to quickly understand resolution details and respond to customers.


 -   **[Recommended Actions - Search query term available as an action input mapping value](https://www.servicenow.com/docs/access?context=ra-create-search-result-mapping-for-ai-search&family=australia&ft:locale=en-US)**

Added the search query term as a new pill picker value in the action input mapping for search result configurations. This provides the ability for agents to include the search query term as a guidance input.


 -   **[Now Assist for CSM- Quality assurance management skill](https://www.servicenow.com/docs/access?context=quality-assurance-management&family=australia&ft:locale=en-US)**

Automatically evaluate agent activity on closed cases using AI models that score each interaction against a configurable quality rubric, eliminating manual sampling and ensuring consistent, objective assessments at scale.

-   **[Now Assist for CSM-Extended table support for email reply recommendation skill](https://www.servicenow.com/docs/access?context=configure-extended-table-support-for-the-email-reply-recommendation-skill&family=australia&ft:locale=en-US)**

Automatically receive email reply recommendations on extended table record pages in ServiceNow Otto for CSM, allowing agents to quickly respond to customers, provide intelligent recommendations and reducing manual effort.


 -   **[Availability of MCP Server in ServiceNow Otto for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=csm-mcp-server&family=australia&ft:locale=en-US)**

ServiceNow Otto for Customer Service Management \(CSM\) can now provide key data and AI actions through MCP connectors, bringing intelligent case management to third-party interfaces seamlessly. CSM customers can now use subflow and actions such as retrieve cases and case task details or AI skills such as generate summaries and resolution notes, analyze sentiment, and draft activity responses when using any AI-enabled MCP client, such as Moveworks or frontier LLM model channels such as Claude in the web


 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Now Assist for CSM-AI workflow tab added in Core UI](https://www.servicenow.com/docs/access?context=ai-workflow-pattern-in-customer-service-management&family=australia&ft:locale=en-US)**

Availability of AI Workflow tab within case view of case table records and email interaction view of interaction records in Core UI, showing agentic workflows and actionable AI-driven insights directly in the record UI.

-   **[Now Assist for CSM-Filter controls in Now Assist Guardian](https://www.servicenow.com/docs/access?context=now-assist-guardian-csm-filters&family=australia&ft:locale=en-US)**

Availability of filter controls for CSM in the AI Guardian interface, allowing users to toggle the base system filters on and off. Filtered results display in a user-friendly format for quick case review and action.


 -   **[AI interaction wrap-up](https://www.servicenow.com/docs/access?context=interaction-wrapup-ai-generated&family=australia&ft:locale=en-US)**

Provides agents with AI assistance during the interaction wrap-up period. This feature generates wrap-up content for interaction records, such as the wrap-up code and notes.

-   **[Process mining - Pre‑configured templates for CSM Process Mining Projects](https://www.servicenow.com/docs/access?context=process-opt-csm&family=australia&ft:locale=en-US)**

Select pre‑configured templates from the Process Mining Content Pack for CSM to quickly set up customer service case projects with default settings already applied. These templates help accelerate project creation by providing standardized configurations tailored for common Customer Service Management scenarios.


 -   **[Guided Decisions - UI Layout tab for the Guided Decision with inputs/outputs activity](https://www.servicenow.com/docs/access?context=add-gd-input-output-playbook&family=australia&ft:locale=en-US)**

Configure the display of knowledge articles directly from the UI Layout tab by setting a default article height and choosing whether articles appear collapsed by default in the playbook.

-   **[Guided Decisions - Restart option for the Guided Decision with inputs and outputs activity](https://www.servicenow.com/docs/access?context=add-gd-input-output-playbook&family=australia&ft:locale=en-US)**

As an agent, you can restart a Guided Decision with inputs and outputs activity in a playbook by selecting the **Restart Activity** option. This option is available when the activity is in a complete, skipped, or error state and the stage is still in progress.

-   **[Recommended Actions - Hybrid search in AI search](https://www.servicenow.com/docs/access?context=ra-hybrid-search&family=australia&ft:locale=en-US)**

Recommended Actions in CSM Configurable Workspace now uses hybrid search, combining keyword and semantic matching to surface more relevant search results in the AI search tab, even when agent queries don't match article content exactly.

-   **[Recommended Actions - View the relevancy score on the Case resolution guidance](https://www.servicenow.com/docs/access?context=nba-use-ai-search&family=australia&ft:locale=en-US)**

View the relevancy score, which indicates how well a search result matches the agent's query, on the search result recommendation cards in the Search tab of the Recommended Actions panel for the Case resolution guidance.

-   **[Recommended Actions – Configure contextual filtering of AI search results](https://www.servicenow.com/docs/access?context=ra-configure-contextual-filtering&family=australia&ft:locale=en-US)**

Enhance search accuracy by ensuring results are contextually relevant to the record being viewed by the agent. Search results are dynamically filtered based on contextual information passed through additional context parameters. To configure the contextual filtering of the Search results, enable the dynamic filter for a search source in a Search profile and then create the AisDynamicFilter implementation for the source which holds the filtering conditions.

-   **[Recommended Actions – Support for mandatory Contextual Inputs](https://www.servicenow.com/docs/access?context=ra-csm-create-context-inputs&family=australia&ft:locale=en-US)**

As an RA author, you can mark specific context inputs as mandatory by selecting the Mandatory check box in the Context Inputs form. When one or more context inputs are configured as mandatory, you must set the values for these contextual inputs directly on Recommended Actions component on the record page in the UI Builder for the recommendations to be generated.

-   **[Recommended Actions - Manage and conﬁgure metadata with delegated developer approach](https://www.servicenow.com/docs/access?context=ra-csm-installed-components&family=australia&ft:locale=en-US)**

Grant granular admin users delegated developer privileges and required roles to manage and configure metadata. This includes the Manage update set permission, domain\_picker role, and metadata\_scope\_viewer role for viewing and modifying the application scope of metadata records.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Predictive AI for CSM features.

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

-   **[Recommended Actions - The primary call-to-action changes on the KB article recommendation card](https://www.servicenow.com/docs/access?context=ra-csm-contexts&family=zurich&ft:locale=en-US)**

The primary call-to-action \(CTA\) on a recommended knowledge base article is determined by the source channel of the case. If the case originates from an email, the primary CTA displayed is Attach and share link in the email. For all the other channels, the primary CTA is Attach and add link in comments. If the article isn’t accessible to the requester, the primary CTA is set to Read article. Accessible articles display the full set of actions \(Attach and add link in comments, Add link in work note, and so on\). Inaccessible articles are limited to internal-use actions only \(Read article, Share link in work notes, and so on\).

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


</td></tr><tr><td>

Australia

</td><td>

-   **[Now Assist &gt; ServiceNow Otto announcement](https://www.servicenow.com/docs/access?context=sn-ai-implementation-landing&family=australia&ft:locale=en-US)**

ServiceNow Otto® introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


 -   **[Now LLM service deprecation](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

-   **[Automated quality assurance dashboard](https://www.servicenow.com/docs/access?context=quality-assurance-management&family=australia&ft:locale=en-US)**

Enable admins to filter scoring parameters and sort agent and case lists. Admins can sort data, manage filters, and easily organize cases on the dashboard with the new sorting, visibility, and skill management capabilities.

-   **[Activate Now Assist skills](https://www.servicenow.com/docs/access?context=activate-now-assist-for-customer-service-management-csm-skills_0&family=australia&ft:locale=en-US)**

Enable admins to view detailed information about each Now Assist skill to make faster and more informed decisions about enabling skill capabilities.


 -   **[Knowledge generation](https://www.servicenow.com/docs/access?context=configure-knowledge-generation-in-now-assist_0&family=australia&ft:locale=en-US)**

Enable users with the **sn\_skill\_builder.admin** role to generate knowledge base articles in ServiceNow Otto for CSM by selecting the required input fields from a task record, reducing manual effort and streamlining the knowledge base generation process.

-   **[Sidebar summarization](https://www.servicenow.com/docs/access?context=configure-sidebar-summarization-in-now-assist&family=australia&ft:locale=en-US)**

Enable customer agents to generate summaries built from the required case and task tables in ServiceNow Otto for CSM as default tables can now be pre-selected and locked.

-   **[Provide Customer 360 insights agentic workflow](https://www.servicenow.com/docs/access?context=customer-service-management-ai-agent-collection-customer-360&family=australia&ft:locale=en-US)**

Enhanced Provide Customer 360 Insights with Enterprise Graph and AI agent deep research for richer, more contextual query results.

-   **[Triage cases agentic workflow](https://www.servicenow.com/docs/access?context=case-resolving-use-case&family=australia&ft:locale=en-US)**

Multilingual and localization flows in the Triage Cases workflow are now fully supported.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Predictive AI for CSM features or functionality were removed.

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

Between your current release family and Australia, some Predictive AI for CSM features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate Predictive AI for CSM.

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

-   **Activation information**

Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&family=australia&ft:locale=en-US).

Now Assist features are available with activation of the ServiceNow Otto for CSM plugin. For more information, see [Install plugins for ServiceNow Otto](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&family=australia&ft:locale=en-US).

Starting with Vancouver Patch 4, ServiceNow Otto for CSM is supported.

Starting with Zurich Patch 7, Customer Service Management AI agent collection is supported. Check your entitlements to determine whether you have access to the ServiceNow Otto for CSM


**Important:** The following applications are available in ServiceNow Store:

-   Now Assist for CSM \(sn\_csm\_gen\_ai\)
-   Guided Decisions Experience \(sn\_ga\_exp\)
-   Recommended Actions \(sn\_nb\_action\)
-   Recommended Actions for Customer Service \(sn\_cs\_nb\_action\)
-   Task Intelligence for Customer Service \(com.snc.csm\_ml\_task\)

For details, see the "Activation information" section of these release notes.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Predictive AI for CSM we have noted them here.

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

If any specific browser requirements were introduced or changed for Predictive AI for CSM we have noted them here.

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

-   **Browser requirements**

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Predictive AI for CSM, such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for Predictive AI for CSM we have noted them here.

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
</table>## Highlight information

If there are specific highlight considerations for Predictive AI for CSM we have noted them here.

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

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

-   Starting with Zurich Patch 12, ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Customer Service Management \(CSM\). Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

 [Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   Resolve cases faster with a new case insights section that consolidates key case details, customer history, sentiment scores, and special handling notes into a single view.
-   Use AI to proactively detect emerging issues from case patterns and automatically propose major cases when similar cases trend together.
-   View automated sentiment scores and trends from conversations directly on the email interaction page.
-   Enable customers to make case updates through AI voice agent.
-   Use Live Agent Assist for voice calls to generate recommendations during live voice calls.

 [Australia Patch 2](https://www.servicenow.com/docs/access?context=australia-patch-2&family=australia&ft:locale=en-US)

-   Automatically evaluate post-interaction customer conversations using AI models that score against a configurable quality rubric, eliminating manual effort.
-   Receive intelligent email reply recommendations on extended table record pages in ServiceNow Otto for CSM, helping agents respond faster with less manual effort.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   Availability of filter controls in Now Assist Guardian for ServiceNow Otto for CSM.
-   Availability of AI Workflow tab in Core UI.

 -   Use AI to populate interaction wrap-up codes and notes, saving agents time.
-   Simplify metadata management by granting developer roles and privileges to your granular admin users.

 See [Intelligence for CSM](https://www.servicenow.com/docs/access?context=intelligence-csm&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/delta-yokohama-australia/rn-combined-intro.md)

