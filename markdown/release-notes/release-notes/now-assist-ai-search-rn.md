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

[Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)

-   Search can prompt users with clarifying questions for broad queries, improving intent matching and control.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Simplify setup with automatic activation of Now Assist Multi-Content Response Genius Results for search profiles when you use Guided Setup to activate the Now Assist panel.
-   Increase search precision and contextual relevance for knowledge article, Catalog Item, external content, and topic retrieval searches with hybrid search.
-   Improve the enhanced chat experience by configuring the system to use AI Search as the source for Ask Now Assist suggestions.
-   Provide more focused auto-complete suggestions for enhanced chat that honor the search user's domain restriction and the exclusion list for unwanted suggestions.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.
-   Improve search recall and accuracy with semantic vector indexing of Catalog Item short descriptions.
-   Prompt users to log in to Microsoft SharePoint Online as needed to see files shared with them when viewing Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers

See [Now Assist in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-ais.md) for more information.

**Important:** Now Assist in AI Search is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Configure disambiguation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/nava-configure-disambiguation-manually.md)**

    If a search is broad or unclear, Now Assist in AI Search may ask follow-up questions before answering. This disambiguation step helps clarify what the user is looking for and is configurable.


-   **[Automatic activation for Now Assist Multi-Content Response Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-multi-content-qna-genius-results.md)**

    When you use Guided Setup to activate the Now Assist panel, Now Assist Multi-Content Response Genius Results are automatically activated for relevant search profiles.

-   **[Hybrid search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/hybrid-search-ais.md)**

    Hybrid search blends keyword search and semantic vector search to offer a blend of superior search recall and contextual relevance for knowledge article, Catalog Item, external content, and topic retrieval searches.

-   **[Configure AI Search as the source for Ask Now Assist suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/configure-ai-search-source-ask-now-assist-suggestions.md)**

    Admins can configure the system to use AI Search as the source for Ask Now Assist suggestions, enabling suggestion term highlighting and more flexible search operators in enhanced chat.


-   **[New third-party AI model provider options available for all AI applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Google Gemini and AWS Claude are available for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Now Assist in Virtual Agent conversational prompt auto-complete suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/auto-complete-suggestion-types-na-ais.md)**

    Auto-complete suggestions for Now Assist in Virtual Agent conversational prompts are only returned from the search user's domain. Suggestions are disabled if they match any exclusion rule entry from the Search Suggestion Exclusion List \[sys\_search\_suggestion\_blacklist\] table. The system scores suggestions based on how search users interact with and rate their Genius Result responses, and preferentially displays higher-scored suggestions.


-   **[Semantic vector search indexing includes Catalog Item short descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/semantic-search-ais.md)**

    Semantic indexing now indexes short descriptions from Catalog Item source records to improve search recall and make field indexing more consistent between legacy \(keyword\) and semantic indexing.

-   **[Now Assist Q&amp;A Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-qna-genius-results.md)**

    The Now Assist Q&amp;A Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-multi-content-qna-genius-results.md).

-   **[Now Assist Actions Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-catalog-ordering-gr.md)**

    The Now Assist Actions Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-multi-content-qna-genius-results.md).

-   **[Microsoft SharePoint Online login prompts in Knowledge Graph user citations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-multi-content-qna-genius-results.md)**

    If you're not logged in to Microsoft SharePoint Online, Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers now prompt you to log in. When logged in, you can check any user citation in a Genius Result answer to see the list of files the cited user has shared with you in Microsoft SharePoint Online.


## Activation information

Now Assist in AI Search is installed when you install any of the following licensed applications from the ServiceNow Store.

-   [Now Assist for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/now-assist-apo.md)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/now-assist-landing-cmdb.md)
-   [Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/now-assist-csm.md)
-   [Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-portfolio-management/now-assist-ea.md)
-   [Now Assist for Operational Sustainability Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/environmental-social-governance/now-assist-for-esg.md)
-   [Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/field-service-management/now-assist-fsm.md)
-   [Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/now-assist-for-financial-services-operations.md)
-   [Now Assist for Hardware Asset Management \(HAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/now-assist-ham.md)
-   [Now Assist for Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-hs-landing.md)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-hrsd.md)
-   [Now Assist for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-itom.md)
-   [Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm.md)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-lsd-landing.md)
-   [Now Assist for Public Sector Digital Services \(PSDS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/government-industry/now-assist-for-psds.md)
-   [Now Assist for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/now-assist-for-irm.md)
-   [Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-security-incident-landing.md)
-   [Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/now-assist-sam.md)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/now-assist-spo.md)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/now-assist-spm.md)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/now-assist-slo.md)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/now-assist-spmc.md)
-   [Now Assist for Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/now-assist-tprm.md)
-   [Now Assist for Workplace Service Delivery \(WSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-wsd-landing.md)
-   [Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-now-assit-landing.md)
-   [Now Assist in Conversational Spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/conv-spokes-na.md)
-   [ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/servicenow-lens-landing-page.md)

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Localization information

Now Assist in AI Search supports [Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/dynamic-translation-overview.md) in Now Assist Genius Results. For details, see [Dynamic Translation for Now Assist Q&amp;A Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/dynamic-translation-na-gr.md) and [Dynamic Translation for Now Assist Actions Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/dynamic-translation-na-actions-gr.md).

## Related ServiceNow applications and features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    ServiceNow Now Assist uses agentic AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   **[AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/overview-ais.md)**

    The ServiceNow AI Search application provides a consumer-grade search engine for ServiceNow Service Portal, ServiceNow Now Mobile®, and ServiceNow Virtual Agent. Intelligent query features help you quickly find the answers you need.


**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

