---
title: Now Assist in AI Search release notes
description: The ServiceNow Now Assist in AI Search application combines the power of search with the Now LLM Service agentic AI model to provide actionable AI-generated or AI-selected answers in user searches. Now Assist in AI Search was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-12"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
---

# Now Assist in AI Search release notes

The ServiceNow® Now Assist in AI Search application combines the power of search with the Now LLM Service agentic AI model to provide actionable AI-generated or AI-selected answers in user searches. Now Assist in AI Search was enhanced and updated in the Zurich release.

## Now Assist in AI Search highlights for the Zurich release

[Zurich Patch 8](../quality/zurich-patch-8.md)

-   Search can prompt users with clarifying questions for broad queries, improving intent matching and control.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Simplify setup with automatic activation of Now Assist Multi-Content Response Genius Results for search profiles when you use Guided Setup to activate the Now Assist panel.
-   Increase search precision and contextual relevance for knowledge article, Catalog Item, external content, and topic retrieval searches with hybrid search.
-   Improve the enhanced chat experience by configuring the system to use AI Search as the source for Ask Now Assist suggestions.
-   Provide more focused auto-complete suggestions for enhanced chat that honor the search user's domain restriction and the exclusion list for unwanted suggestions.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Improve search recall and accuracy with semantic vector indexing of Catalog Item short descriptions.
-   Prompt users to log in to Microsoft SharePoint Online as needed to see files shared with them when viewing Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers

See [Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

**Important:** Now Assist in AI Search is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Configure disambiguation](https://www.servicenow.com/docs/access?context=nava-configure-disambiguation-manually&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    If a search is broad or unclear, Now Assist in AI Search may ask follow-up questions before answering. This disambiguation step helps clarify what the user is looking for and is configurable.


-   **[Automatic activation for Now Assist Multi-Content Response Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    When you use Guided Setup to activate the Now Assist panel, Now Assist Multi-Content Response Genius Results are automatically activated for relevant search profiles.

-   **[Hybrid search](https://www.servicenow.com/docs/access?context=hybrid-search-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Hybrid search blends keyword search and semantic vector search to offer a blend of superior search recall and contextual relevance for knowledge article, Catalog Item, external content, and topic retrieval searches.

-   **[Configure AI Search as the source for Ask Now Assist suggestions](https://www.servicenow.com/docs/access?context=configure-ai-search-source-ask-now-assist-suggestions&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Admins can configure the system to use AI Search as the source for Ask Now Assist suggestions, enabling suggestion term highlighting and more flexible search operators in enhanced chat.


-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Now Assist in Virtual Agent conversational prompt auto-complete suggestions](https://www.servicenow.com/docs/access?context=auto-complete-suggestion-types-na-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Auto-complete suggestions for Now Assist in Virtual Agent conversational prompts are only returned from the search user's domain. Suggestions are disabled if they match any exclusion rule entry from the Search Suggestion Exclusion List \[sys\_search\_suggestion\_blacklist\] table. The system scores suggestions based on how search users interact with and rate their Genius Result responses, and preferentially displays higher-scored suggestions.


-   **[Semantic vector search indexing includes Catalog Item short descriptions](https://www.servicenow.com/docs/access?context=semantic-search-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Semantic indexing now indexes short descriptions from Catalog Item source records to improve search recall and make field indexing more consistent between legacy \(keyword\) and semantic indexing.

-   **[Now Assist Q&amp;A Genius Results](https://www.servicenow.com/docs/access?context=now-assist-qna-genius-results&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    The Now Assist Q&amp;A Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

-   **[Now Assist Actions Genius Results](https://www.servicenow.com/docs/access?context=now-assist-catalog-ordering-gr&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    The Now Assist Actions Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

-   **[Microsoft SharePoint Online login prompts in Knowledge Graph user citations](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    If you're not logged in to Microsoft SharePoint Online, Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers now prompt you to log in. When logged in, you can check any user citation in a Genius Result answer to see the list of files the cited user has shared with you in Microsoft SharePoint Online.


## Activation information

Now Assist in AI Search is installed when you install any of the following licensed applications from the ServiceNow Store.

-   [Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)
-   [Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)
-   [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)
-   [Now Assist for Operational Sustainability Management](https://www.servicenow.com/docs/access?context=now-assist-for-esg&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)
-   [Now Assist for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)
-   [Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)
-   [Now Assist for Hardware Asset Management \(HAM\)](https://www.servicenow.com/docs/access?context=now-assist-ham&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)
-   [Now Assist for Health and Safety](https://www.servicenow.com/docs/access?context=now-assist-hs-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
-   [Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=now-assist-itom&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
-   [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
-   [Now Assist for Public Sector Digital Services \(PSDS\)](https://www.servicenow.com/docs/access?context=now-assist-for-psds&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)
-   [Now Assist for Integrated Risk Management \(IRM\)](https://www.servicenow.com/docs/access?context=now-assist-for-irm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)
-   [Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)
-   [Now Assist for Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=now-assist-sam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)
-   [Now Assist for Third-party Risk Management \(TPRM\)](https://www.servicenow.com/docs/access?context=now-assist-tprm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)
-   [Now Assist for Workplace Service Delivery \(WSD\)](https://www.servicenow.com/docs/access?context=now-assist-wsd-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
-   [Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-now-assit-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
-   [Now Assist in Conversational Spokes](https://www.servicenow.com/docs/access?context=conv-spokes-na&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)
-   [ServiceNow AI Lens](https://www.servicenow.com/docs/access?context=servicenow-lens-landing-page&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Localization information

Now Assist in AI Search supports [Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) in Now Assist Genius Results. For details, see [Dynamic Translation for Now Assist Q&amp;A Genius Results](https://www.servicenow.com/docs/access?context=dynamic-translation-na-gr&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) and [Dynamic Translation for Now Assist Actions Genius Results](https://www.servicenow.com/docs/access?context=dynamic-translation-na-actions-gr&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    ServiceNow Now Assist uses agentic AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   **[AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    The ServiceNow AI Search application provides a consumer-grade search engine for ServiceNow Service Portal, ServiceNow Now Mobile®, and ServiceNow Virtual Agent. Intelligent query features help you quickly find the answers you need.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

