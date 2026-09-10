---
title: Intelligence for CSM release notes
description: The ServiceNow Intelligence for CSM applications enable customer service organizations and service operations to configure and implement Guided Decisions, Recommended Actions, and Task Intelligence features. The Intelligence for CSM applications were enhanced and updated in the Yokohama release.The ServiceNow Intelligence for CSM applications enable customer service organizations and service operations to configure and implement Guided Decisions, Recommended Actions, and Task Intelligence features. The Intelligence for CSM applications were enhanced and updated in the Yokohama release.The ServiceNow Intelligence for CSM applications enable customer service organizations and service operations to configure and implement Guided Decisions, Recommended Actions, and Task Intelligence features. The Intelligence for CSM applications were enhanced and updated in the Yokohama release.The ServiceNow Intelligence for CSM applications enable customer service organizations and service operations to configure and implement Guided Decisions, Recommended Actions, and Task Intelligence features. The Intelligence for CSM applications were enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 5
---

# Intelligence for CSM release notes

The ServiceNow® Intelligence for CSM applications enable customer service organizations and service operations to configure and implement Guided Decisions, Recommended Actions, and Task Intelligence features. The Intelligence for CSM applications were enhanced and updated in the Yokohama release.

## About Intelligence for CSM

-   Enabled Recommended Actions for chat interactions so that agents can select relevant actions that are based on the chat context.
-   Integrated enhanced knowledge guidance on the Front-line case page and enable agents to attach and add links to knowledge articles in comments, work notes, or emails by using modeless dialogs.
-   Enabled Recommended Actions – AI search for CSM default record page and CSM interaction record pages for the video, chat, walk-up, and email channels.
-   Automated the mapping configuration for search results along with default guidances.

See [Intelligence for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/intelligence-csm.md) for more information.

## Activation and other requirements

**Important:** The following applications are available in ServiceNow Store:

-   Recommended Actions \(sn\_nb\_action\)
-   Recommended Actions for Customer Service \(sn\_cs\_nb\_action\)
-   Task Intelligence for Customer Service \(com.snc.csm\_ml\_task\)

For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/t_ActivateCustomerService.md).

-   **Browser requirements**

    ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/browser-support.md).


**Parent Topic:**[Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/customer-service-mgmt-rn-landing.md)

## May 2025

The ServiceNow® Intelligence for CSM applications enable customer service organizations and service operations to configure and implement Guided Decisions, Recommended Actions, and Task Intelligence features. The Intelligence for CSM applications were enhanced and updated in the Yokohama release.

### What's new

-   **[Recommended Actions – AI search on CSM default record page, Front line case page, and CSM interaction record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/ra-csm-ai-search.md)**

    The Recommended Actions – AI search is introduced on the [CSM default record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/csm-default-record-page.md), [Front-line case page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/csm-front-line-case-page.md), and [CSM Interaction record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/csm-interaction-record-page.md) \(for the chat, video, walk-up, and email type channels\) and it’s enabled by default for new customers. The default guidance is also enabled for these pages. Agents can attach and share knowledge article links in comments, work notes, and emails.

-   **[Recommended Actions - Catalog item source type for AI search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/ra-csm-ai-search.md)**

    Search and filter the catalog items easily in the AI search tab of Recommended Actions in the CRM Workspace.

-   **[Recommended Actions - Ability to have multiple active contexts for the same table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/ra-csm-contexts.md)**

    Enables multiple active contexts for the same table, so that tailored recommendations are displayed in the CRM Workspace:

    -   For different user personas based on their requirements.
    -   For different Predictive Intelligence models or AI model variants.
    -   For the same record in different channels, such as chat, email, and so on.
-   **[Recommended Actions - Ability to inherit active rules and their recommendations from a parent table context to extended table context](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/ra-csm-contexts.md)**

    Assign the active rules and their recommendations from the parent table context to the extended context table for a streamlined process.

-   **[Recommended Actions - Asynchronous evaluation for recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/ra-csm-contexts.md)**

    Enables you to configure loading behavior at the context level by choosing between synchronous and asynchronous modes. In the asynchronous mode, recommendations load in the background without blocking the UI, allowing agents to interact with the record immediately.


## Yokohama Early Availability

The ServiceNow® Intelligence for CSM applications enable customer service organizations and service operations to configure and implement Guided Decisions, Recommended Actions, and Task Intelligence features. The Intelligence for CSM applications were enhanced and updated in the Yokohama release.

### What's new

-   **[Recommended Actions - Front-line case page integration with knowledge guidance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/csm-front-line-case-page.md)**

    Enable agents to attach and share knowledge article links in comments, work notes, or emails by using modeless dialogs.

-   **[Recommended Actions - Default guidance for search results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/ra-csm-guidances-default-guidance-search.md)**

    Enable agents to view search results for any records. Use a default guidance for any search sources that don't have a dedicated, mapped guidance.

-   **[Recommended Actions - Improved timeout handling for resource generators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/ra-csm-resource-generators.md)**

    Handle timeout errors when calling Machine Learning \(ML\) resource generators. The system uses a subflow API with a 1-second timeout ensures the RA generation engine prioritizes faster response times by terminating stalled ML prediction calls.

-   **[Recommended Actions - Custom guidances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/ra-csm-custom-guidances.md)**

    Use a custom guidance to provide actions that are based on the search results from the Case, Problem, Incident, or Change Request tables. Agents can use these actions to link records to the current case and copy resolution codes and notes from resolved cases.

-   **[Recommended Actions - Field values for predicted records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/ra-csm-guidances.md#section_lmj_cl3_c2c)**

    Leverage the actual field value for a predicted record and show it in a custom guidance in place of the display value.

-   **[Recommended Actions for Customer Service - Display Recommended Actions on the CSM Interaction record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/ra-csm-chat-interaction-record.md)**

    Enable agents to view Recommended Actions in the contextual side panel on the CSM Interaction record page. The search tab dynamically displays relevant actions based on the context of the chat interaction.

-   **[Recommended Actions for Customer Service - Interaction Context record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/ra-csm-context-records.md)**

    Use the Interaction Context record to display the search results from the Knowledge table. The results are based on the interaction's short description. This context record includes a search-mapping record that maps knowledge results to the Share KB in chat interactions guidance.


## Intelligence for CSM Patch 2 release notes

The ServiceNow® Intelligence for CSM applications enable customer service organizations and service operations to configure and implement Guided Decisions, Recommended Actions, and Task Intelligence features. The Intelligence for CSM applications were enhanced and updated in the Yokohama release.

### What's new

-   **[Recommended Actions - Question font size customization for a Decision tree](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/configure-decision-trees-gdb.md)**

    Enables you to customize the font size of questions in a Decision tree for a better look and feel. This font size is applied to the questions in the decision trees of playbooks, and recommendations, within the CRM Workspace and service portal.

-   **[Recommended Actions - Control the visibility of completed guidance information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/create-guidances.md)**

    Allows you to manage the visibility of the completed guidance history information of a decision tree in playbooks, and recommendations for an agent, within the CRM Workspace, and service portal for a streamlined experience.


