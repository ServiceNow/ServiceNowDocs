---
title: Now Assist in AI Search release notes
description: The ServiceNow Now Assist in AI Search application combines the power of search with the Now LLM Service agentic AI model to provide actionable AI-generated or AI-selected answers in user searches. Now Assist in AI Search was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-11-17"
reading_time_minutes: 7
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
---

# Now Assist in AI Search release notes

The ServiceNow® Now Assist in AI Search application combines the power of search with the Now LLM Service agentic AI model to provide actionable AI-generated or AI-selected answers in user searches. Now Assist in AI Search was enhanced and updated in the Yokohama release.

## Now Assist in AI Search highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Simplify setup with automatic activation of Now Assist Multi-Content Response Genius Results for search profiles when you use Guided Setup to activate the Now Assist panel.
-   Increase search precision and contextual relevance for knowledge article, Catalog Item, external content, and topic retrieval searches with hybrid search.
-   Improve the enhanced chat experience by configuring the system to use AI Search as the source for Ask Now Assist suggestions.
-   Provide more focused auto-complete suggestions for enhanced chat that honor the search user's domain restriction and the exclusion list for unwanted suggestions.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Increase search recall with semantic indexing of Catalog Item short descriptions.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Prompt users to log in to Microsoft SharePoint Online as needed to see files shared with them when viewing Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers.

Yokohama Early Availability

-   Improve incident deflection for portal users by configuring record producers to display actionable and relevant Genius Results suggestions during submission of cases, incidents, problems, and similar tasks.

See [Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

**Important:** Now Assist in AI Search is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Automatic activation for Now Assist Multi-Content Response Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    When you use Guided Setup to activate the Now Assist panel, Now Assist Multi-Content Response Genius Results are automatically activated for relevant search profiles.

-   **[Hybrid search](https://www.servicenow.com/docs/access?context=hybrid-search-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Hybrid search blends keyword search and semantic vector search to offer a blend of superior search recall and contextual relevance for knowledge article, Catalog Item, external content, and topic retrieval searches.

-   **[Configure AI Search as the source for Ask Now Assist suggestions](https://www.servicenow.com/docs/access?context=configure-ai-search-source-ask-now-assist-suggestions&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Admins can configure the system to use AI Search as the source for Ask Now Assist suggestions, enabling suggestion term highlighting and more flexible search operators in enhanced chat.


-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


-   **[AI Search Genius Results widget for record producers](https://www.servicenow.com/docs/access?context=cfg-ais-genius-results-widget&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Administrators can configure the AI Search Genius Results widget on record producers to enhance the user experience when creating an incident. The widget displays actionable Genius Result suggestions relevant to the user's incident description. Users can select from these Genius Result suggestions to address their own issues, or can continue with their incident submission if none of the suggestions resolve their problem.


## Changed in this release

-   **[Now Assist in Virtual Agent conversational prompt auto-complete suggestions](https://www.servicenow.com/docs/access?context=auto-complete-suggestion-types-na-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Auto-complete suggestions for Now Assist in Virtual Agent conversational prompts are only returned from the search user's domain. Suggestions are disabled if they match any exclusion rule entry from the Search Suggestion Exclusion List \[sys\_search\_suggestion\_blacklist\] table. The system scores suggestions based on how search users interact with and rate their Genius Result responses, and preferentially displays higher-scored suggestions.

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Semantic vector search indexing includes Catalog Item short descriptions](https://www.servicenow.com/docs/access?context=semantic-search-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Semantic indexing now indexes short descriptions from Catalog Item source records to improve search recall and make field indexing more consistent between legacy \(keyword\) and semantic indexing.


-   **[Microsoft SharePoint Online login prompts in Knowledge Graph user citations](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    If you're not logged in to Microsoft SharePoint Online, Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers now prompt you to log in. When logged in, you can check any user citation in a Genius Result answer to see the list of files the cited user has shared with you in Microsoft SharePoint Online.

-   **[Now Assist Q&amp;A Genius Results](https://www.servicenow.com/docs/access?context=now-assist-qna-genius-results&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    The Now Assist Q&amp;A Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

-   **[Now Assist Actions Genius Results](https://www.servicenow.com/docs/access?context=now-assist-catalog-ordering-gr&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    The Now Assist Actions Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).


## Activation information

Now Assist in AI Search is installed when you install any of the following licensed applications from the ServiceNow Store.

-   [Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)
-   [Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)
-   [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)
-   [Now Assist for Operational Sustainability \(formerly ESG\)](https://www.servicenow.com/docs/access?context=now-assist-for-esg&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)
-   [Now Assist for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)
-   [Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)
-   [Now Assist for Hardware Asset Management \(HAM\)](https://www.servicenow.com/docs/access?context=now-assist-ham&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)
-   [Now Assist for Health and Safety](https://www.servicenow.com/docs/access?context=now-assist-hs-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=now-assist-itom&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
-   [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for PSDS](https://www.servicenow.com/docs/access?context=now-assist-for-psds&version=yokohama&pubname=yokohama-government-industry&ft:locale=en-US)
-   [Now Assist for Integrated Risk Management \(IRM\)](https://www.servicenow.com/docs/access?context=now-assist-for-irm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)
-   [Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Now Assist for Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=now-assist-sam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)
-   [Now Assist for Third-party Risk Management \(TPRM\)](https://www.servicenow.com/docs/access?context=now-assist-tprm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)
-   [Now Assist for Workplace Service Delivery \(WSD\)](https://www.servicenow.com/docs/access?context=now-assist-wsd-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-now-assit-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist in Conversational Spokes](https://www.servicenow.com/docs/access?context=conv-spokes-na&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)
-   [ServiceNow AI Lens](https://www.servicenow.com/docs/access?context=servicenow-lens-landing-page&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Localization information

Now Assist in AI Search supports [Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) in Now Assist Genius Results. For details, see [Dynamic Translation for Now Assist Q&amp;A Genius Results](https://www.servicenow.com/docs/access?context=dynamic-translation-na-gr&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and [Dynamic Translation for Now Assist Actions Genius Results](https://www.servicenow.com/docs/access?context=dynamic-translation-na-actions-gr&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    ServiceNow Now Assist uses agentic AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   **[AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    The ServiceNow AI Search application provides a consumer-grade search engine for ServiceNow Service Portal, ServiceNow Now Mobile®, and ServiceNow Virtual Agent. Intelligent query features help you quickly find the answers you need.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

