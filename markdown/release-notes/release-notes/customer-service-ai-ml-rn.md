---
title: Intelligence for CSM release notes
description: The ServiceNow Intelligence for CSM applications enable customer service organizations and service operations to configure and implement Guided Decisions, Recommended Actions, and Task Intelligence features. The Intelligence for CSM applications were enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
---

# Intelligence for CSM release notes

The ServiceNow® Intelligence for CSM applications enable customer service organizations and service operations to configure and implement Guided Decisions, Recommended Actions, and Task Intelligence features. The Intelligence for CSM applications were enhanced and updated in the Yokohama release.

## Intelligence for CSM highlights for the Yokohama release

-   Enabled Recommended Actions for chat interactions so that agents can select relevant actions that are based on the chat context.
-   Integrated enhanced knowledge guidance on the Front-line case page and enable agents to attach and add links to knowledge articles in comments, work notes, or emails by using modeless dialogs.
-   Enabled Recommended Actions – AI search for CSM default record page and CSM interaction record pages for the video, chat, walk-up, and email channels.
-   Automated the mapping configuration for search results along with default guidances.

See [Intelligence for CSM](https://www.servicenow.com/docs/access?context=intelligence-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) for more information.

**Important:** The following applications are available in ServiceNow Store:

-   Recommended Actions \(sn\_nb\_action\)
-   Recommended Actions for Customer Service \(sn\_cs\_nb\_action\)
-   Task Intelligence for Customer Service \(com.snc.csm\_ml\_task\)

For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Recommended Actions - Front-line case page integration with knowledge guidance](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enable agents to attach and share knowledge article links in comments, work notes, or emails by using modeless dialogs.

-   **[Recommended Actions - Default guidance for search results](https://www.servicenow.com/docs/access?context=ra-csm-guidances-default-guidance-search&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enable agents to view search results for any records. Use a default guidance for any search sources that don't have a dedicated, mapped guidance.

-   **[Recommended Actions - Improved timeout handling for resource generators](https://www.servicenow.com/docs/access?context=ra-csm-resource-generators&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Handle timeout errors when calling Machine Learning \(ML\) resource generators. The system uses a subflow API with a 1-second timeout ensures the RA generation engine prioritizes faster response times by terminating stalled ML prediction calls.

-   **[Recommended Actions - Custom guidances](https://www.servicenow.com/docs/access?context=ra-csm-custom-guidances&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use a custom guidance to provide actions that are based on the search results from the Case, Problem, Incident, or Change Request tables. Agents can use these actions to link records to the current case and copy resolution codes and notes from resolved cases.

-   **[Recommended Actions - Field values for predicted records](https://www.servicenow.com/docs/access?context=ra-csm-guidances&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US#section_lmj_cl3_c2c)**

    Leverage the actual field value for a predicted record and show it in a custom guidance in place of the display value.

-   **[Recommended Actions for Customer Service - Display Recommended Actions on the CSM Interaction record page](https://www.servicenow.com/docs/access?context=ra-csm-chat-interaction-record&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enable agents to view Recommended Actions in the contextual side panel on the CSM Interaction record page. The search tab dynamically displays relevant actions based on the context of the chat interaction.

-   **[Recommended Actions for Customer Service - Interaction Context record](https://www.servicenow.com/docs/access?context=ra-csm-context-records&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use the Interaction Context record to display the search results from the Knowledge table. The results are based on the interaction's short description. This context record includes a search-mapping record that maps knowledge results to the Share KB in chat interactions guidance.

-   **[Recommended Actions - Question font size customization for a Decision tree](https://www.servicenow.com/docs/access?context=configure-decision-trees-gdb&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enables you to customize the font size of questions in a Decision tree for a better look and feel. This font size is applied to the questions in the decision trees of playbooks, and recommendations, within the CSM Configurable Workspace and service portal.

-   **[Recommended Actions - Control the visibility of completed guidance information](https://www.servicenow.com/docs/access?context=create-guidances&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Allows you to manage the visibility of the completed guidance history information of a decision tree in playbooks, and recommendations for an agent, within the CSM Configurable Workspace, and service portal for a streamlined experience.

-   **[Recommended Actions – AI search on CSM default record page, Front line case page, and CSM interaction record page](https://www.servicenow.com/docs/access?context=ra-csm-ai-search&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    The Recommended Actions – AI search is introduced on the [CSM default record page](https://www.servicenow.com/docs/access?context=csm-default-record-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US), [Front-line case page](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US), and [CSM Interaction record page](https://www.servicenow.com/docs/access?context=csm-interaction-record-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) \(for the chat, video, walk-up, and email type channels\) and it’s enabled by default for new customers. The default guidance is also enabled for these pages. Agents can attach and share knowledge article links in comments, work notes, and emails.

-   **[Recommended Actions - Catalog item source type for AI search](https://www.servicenow.com/docs/access?context=ra-csm-ai-search&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Search and filter the catalog items easily in the AI search tab of Recommended Actions in the CSM Configurable Workspace.

-   **[Recommended Actions - Ability to have multiple active contexts for the same table](https://www.servicenow.com/docs/access?context=ra-csm-contexts&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enables multiple active contexts for the same table, so that tailored recommendations are displayed in the CSM Configurable Workspace:

    -   For different user personas based on their requirements.
    -   For different Predictive Intelligence models or AI model variants.
    -   For the same record in different channels, such as chat, email, and so on.
-   **[Recommended Actions - Ability to inherit active rules and their recommendations from a parent table context to extended table context](https://www.servicenow.com/docs/access?context=ra-csm-contexts&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Assign the active rules and their recommendations from the parent table context to the extended context table for a streamlined process.

-   **[Recommended Actions - Asynchronous evaluation for recommendations](https://www.servicenow.com/docs/access?context=ra-csm-contexts&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enables you to configure loading behavior at the context level by choosing between synchronous and asynchronous modes. In the asynchronous mode, recommendations load in the background without blocking the UI, allowing agents to interact with the record immediately.


## Activation information

Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

## Browser requirements

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Provide the service and support that your external customers need with Customer Service Management.

-   **[Now Assist for CSM](../analytics-intelligence-reporting/now-assist-rn.md)**

    Summarize customer chat conversations on interactions, summarize case details, and generate case resolution notes with the ServiceNow® Now Assist for CSM application.

-   **[Document Intelligence](https://www.servicenow.com/docs/access?context=document-intelligence-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Extract the data from documents and integrate the data into automation workflows to save time and resources by using the Document Intelligence artificial intelligence \(AI\) solution.

-   **[Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Improve processes across the platform, such as automatically populating fields when a case is created, categorizing and routing work, and suggesting case resolutions through the Predictive Intelligence artificial intelligence.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

