---
title: Document Intelligence release notes
description: The ServiceNow Document Intelligence application is an artificial intelligence \(AI\) solution that quickly and accurately categorizes and extracts information from documents. Document Intelligence was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [DocIntel, Document Intelligence]
---

# Document Intelligence release notes

The ServiceNow® Document Intelligence application is an artificial intelligence \(AI\) solution that quickly and accurately categorizes and extracts information from documents. Document Intelligence was enhanced and updated in the Zurich release.

## Document Intelligence highlights for the Zurich release

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

See [Document Intelligence](https://www.servicenow.com/docs/access?context=document-intelligence-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

**Important:** Document Intelligence is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Removed in this release

The Document Intelligence application has been removed from the application navigator.

## Deprecations

-   Starting with Zurich release, the document extraction feature in Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see .
-   The Document Intelligence Admin \(sn\_docintel\_admin\) plugin is planned for deprecation in the B release.

## Activation information

Install Document Intelligence by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html). The Document Intelligence application \(sn\_docintel\) depends on the Document Intelligence plugin \(com.glide.platform\_ml\_di\), the Predictive Intelligence plugin \(com.glide.platform\_ml\), and the Document Intelligence UIB component \(com.sn\_docintel\_iframe\). For more details, see [Install Document Intelligence](https://www.servicenow.com/docs/access?context=install-document-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Accounts Payable Operations](https://www.servicenow.com/docs/access?context=integrate-docintel-apo&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use Document Intelligence for ServiceNow® Accounts Payable Operations to extract information quickly and accurately from invoice documents that are received as attachments via email, as well as create invoice records in the Accounts Payable Operations application.

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=integrate-docintel-csm&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use Document Intelligence for ServiceNow® Customer Service Management \(CSM\) to extract relevant information from email and case attachments, such as account numbers or customer addresses, and add that information to cases.

-   **[Financial Services Operations](https://www.servicenow.com/docs/access?context=integrate-docintel-fso&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use Document Intelligence integrated with the digital workflows in the ServiceNow® Financial Services Operations applications to help your organization quickly automate document processing and accurately extract information from documents to the ServiceNow AI Platform.

-   **[Automation Center](https://www.servicenow.com/docs/access?context=automation-center-landing-page&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Use Document Intelligence for ServiceNow® Automation Center to discover automation opportunities for document processing using DocIntel automation metrics.


**Parent Topic:**[AI Experiences release notes](intelligent-experiences-rn-landing.md)

