---
title: Intelligence for CSM release notes
description: The ServiceNow Intelligence for Customer Service Management \(CSM\) applications enable customer service organizations and service operations to configure and implement Guided Decisions, Recommended Actions, and Task Intelligence features. The Intelligence for CSM applications were enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Intelligence for CSM release notes

The ServiceNow® Intelligence for Customer Service Management \(CSM\) applications enable customer service organizations and service operations to configure and implement Guided Decisions, Recommended Actions, and Task Intelligence features. The Intelligence for CSM applications were enhanced and updated in the Australia release.

## Intelligence for CSM highlights for the Australia release

[Australia Patch 2](../quality/australia-patch-2.md)

-   Automatically evaluate post-interaction customer conversations using AI models that score against a configurable quality rubric, eliminating manual effort.
-   Receive intelligent email reply recommendations on extended table record pages in Now Assist for CSM, helping agents respond faster with less manual effort.

[Australia Patch 1](../quality/australia-patch-1.md)

-   Availability of filter controls in Now Assist Guardian for Now Assist for CSM.
-   Availability of AI Workflow tab in Core UI.

-   Use AI to populate interaction wrap-up codes and notes, saving agents time.
-   Simplify metadata management by granting developer roles and privileges to your granular admin users.

See [Intelligence for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/intelligence-csm.md) for more information.

**Important:** The following applications are available in ServiceNow Store:

-   Guided Decisions Experience \(sn\_ga\_exp\)
-   Recommended Actions \(sn\_nb\_action\)
-   Recommended Actions for Customer Service \(sn\_cs\_nb\_action\)
-   Task Intelligence for Customer Service \(com.snc.csm\_ml\_task\)

For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Quality assurance management skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/quality-assurance-management.md)**

    Automatically evaluate agent activity on closed cases using AI models that score each interaction against a configurable quality rubric, eliminating manual sampling and ensuring consistent, objective assessments at scale.

-   **[Extended table support for email reply recommendation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/configure-extended-table-support-for-the-email-reply-recommendation-skill.md)**

    Automatically receive email reply recommendations on extended table record pages in Now Assist for CSM, allowing agents to quickly respond to customers, provide intelligent recommendations and reducing manual effort.


-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[AI workflow tab added in Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/ai-workflow-pattern-in-customer-service-management.md)**

    Availability of AI Workflow tab within case view of case table records and email interaction view of interaction records in Core UI, showing agentic workflows and actionable AI-driven insights directly in the record UI.

-   **[Filter controls in Now Assist Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-guardian-csm-filters.md)**

    Availability of filter controls for CSM in the Now Assist Guardian interface, allowing users to toggle the base system filters on and off. Filtered results display in a user-friendly format for quick case review and action.


-   **[Guided Decisions - UI Layout tab for the Guided Decision with inputs/outputs activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/add-gd-input-output-playbook.md)**

    Configure the display of knowledge articles directly from the UI Layout tab by setting a default article height and choosing whether articles appear collapsed by default in the playbook.

-   **[Guided Decisions - Restart option for the Guided Decision with inputs and outputs activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/add-gd-input-output-playbook.md)**

    As an agent, you can restart a Guided Decision with inputs and outputs activity in a playbook by selecting the **Restart Activity** option when the activity is in a complete, skipped, or error state and the stage is still in progress.

-   **[Recommended Actions - Hybrid search in AI search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-hybrid-search.md)**

    Recommended Actions in CSM Configurable Workspace now uses hybrid search, combining keyword and semantic matching to surface more relevant KB articles and guided actions in the AI search tab, even when agent queries do not match article content exactly.

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


## Activation information

Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/t_ActivateCustomerService.md).

## Plugin information

-   **Renamed or changed plugins**

    The following plugin has been renamed or changed:

    Recommended Actions for Customer Service \(sn\_cs\_nb\_action\):Renamed to Recommended Actions for Service \(sn\_cs\_nb\_action\) starting with v31.0.


## Browser requirements

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/browser-support.md).

## Related ServiceNow applications and features

-   **[Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_CustomerServiceManagement.md)**

    Provide the service and support that your external customers need with Customer Service Management.

-   **[Now Assist for CSM](../analytics-intelligence-reporting/now-assist-rn.md)**

    Summarize customer chat conversations on interactions, summarize case details, and generate case resolution notes with the ServiceNow® Now Assist for CSM application.

-   **[Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/document-intelligence/document-intelligence-landing.md)**

    Extract the data from documents and integrate the data into automation workflows to save time and resources by using the Document Intelligence AI solution.

-   **[Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/predictive-intelligence-landing.md)**

    Improve processes across the platform, such as automatically populating fields when a case is created, categorizing and routing work, and suggesting case resolutions through Predictive Intelligence AI.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

