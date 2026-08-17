---
title: Now Assist in AI Search release notes
description: The ServiceNow Now Assist in AI Search application combines the power of search with the Now LLM Service agentic AI model to provide actionable AI-generated or AI-selected answers in user searches. Now Assist in AI Search was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-07-16"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
---

# Now Assist in AI Search release notes

The ServiceNow® Now Assist in AI Search application combines the power of search with the Now LLM Service agentic AI model to provide actionable AI-generated or AI-selected answers in user searches. Now Assist in AI Search was enhanced and updated in the Yokohama release.

## Now Assist in AI Search highlights for the Yokohama release

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Simplify setup with automatic activation of Now Assist Multi-Content Response Genius Results for search profiles when you use Guided Setup to activate the Now Assist panel.
-   Increase search precision and contextual relevance for knowledge article, Catalog Item, external content, and topic retrieval searches with hybrid search.
-   Improve the enhanced chat experience by configuring the system to use AI Search as the source for Ask Now Assist suggestions.
-   Provide more focused auto-complete suggestions for enhanced chat that honor the search user's domain restriction and the exclusion list for unwanted suggestions.

[Yokohama Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-6.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Increase search recall with semantic indexing of Catalog Item short descriptions.

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   Prompt users to log in to Microsoft SharePoint Online as needed to see files shared with them when viewing Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers.

Yokohama Early Availability

-   Improve incident deflection for portal users by configuring record producers to display actionable and relevant Genius Results suggestions during submission of cases, incidents, problems, and similar tasks.

See  for more information.

**Important:** Now Assist in AI Search is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **Automatic activation for Now Assist Multi-Content Response Genius Results**

    When you use Guided Setup to activate the Now Assist panel, Now Assist Multi-Content Response Genius Results are automatically activated for relevant search profiles.

-   **Hybrid search**

    Hybrid search blends keyword search and semantic vector search. It offers a blend of superior search recall and contextual relevance for knowledge article, Catalog Item, external content, and topic retrieval searches.

-   ****

    Admins can configure the system to use AI Search as the source for Ask Now Assist suggestions, enabling suggestion term highlighting and more flexible search operators in enhanced chat.


-   **New third-party AI model provider options available for all Now Assist applications**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


-   **AI Search Genius Results widget for record producers**

    Administrators can configure the AI Search Genius Results widget on record producers to enhance the user experience when creating an incident. The widget displays actionable Genius Result suggestions relevant to the user's incident description. Users can select from these Genius Result suggestions to address their own issues, or can continue with their incident submission if none of the suggestions resolve their problem.


## Changed in this release

-   **Now Assist in Virtual Agent conversational prompt auto-complete suggestions**

    Auto-complete suggestions for Now Assist in Virtual Agent conversational prompts are only returned from the search user's domain. Suggestions are disabled if they match any exclusion rule entry from the Search Suggestion Exclusion List \[sys\_search\_suggestion\_blacklist\] table. The system scores suggestions based on how search users interact with and rate their Genius Result responses, and preferentially displays higher-scored suggestions.

-   **Changes to Now Assist usage measurement**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **Some Now Assist skills are turned on by default**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **Configure ACLs for AI agents and agentic workflows**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **Semantic vector search indexing includes Catalog Item short descriptions**

    Semantic indexing now indexes short descriptions from Catalog Item source records to improve search recall and make field indexing more consistent between legacy \(keyword\) and semantic indexing.


-   **Microsoft SharePoint Online login prompts in Knowledge Graph user citations**

    If you're not logged in to Microsoft SharePoint Online, Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers now prompt you to log in. When logged in, you can check any user citation in a Genius Result answer to see the list of files the cited user has shared with you in Microsoft SharePoint Online.

-   ****

    The Now Assist Q&amp;A Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see .

-   ****

    The Now Assist Actions Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see .


## Activation information

Now Assist in AI Search is installed when you install any of the following licensed applications from the ServiceNow Store.

-   [ServiceNow Otto for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-apo.md)
-   
-   [ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-csm.md)
-   [ServiceNow Otto for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/now-assist-ea.md)
-   [ServiceNow Otto for Operational Sustainability \(formerly ESG\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/environmental-social-governance/now-assist-for-esg.md)
-   [ServiceNow Otto for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/now-assist-fsm.md)
-   [ServiceNow Otto for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/now-assist-for-financial-services-operations.md)
-   
-   
-   
-   
-   
-   
-   [ServiceNow Otto for PSDS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/government-industry/now-assist-for-psds.md)
-   
-   [ServiceNow Otto for Security Incident Response \(SIR\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-security-incident-landing.md)
-   
-   [ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo.md)
-   [ServiceNow Otto for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-spm.md)
-   [ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-slo.md)
-   [ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-spmc.md)
-   
-   
-   
-   [Now Assist in Conversational Spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/conv-spokes-na.md)
-   

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Localization information

Now Assist in AI Search supports  in Now Assist Genius Results. For details, see  and .

## Related ServiceNow applications and features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    ServiceNow Now Assist uses agentic AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   ****

    The ServiceNow AI Search application provides a consumer-grade search engine for ServiceNow Service Portal, ServiceNow Now Mobile®, and ServiceNow Virtual Agent. Intelligent query features help you quickly find the answers you need.


**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)

