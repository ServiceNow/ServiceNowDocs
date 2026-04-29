---
title: Now Assist release notes
description: The ServiceNow Now Assist experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. Now Assist was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Now Assist release notes

The ServiceNow® Now Assist experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. Now Assist was enhanced and updated in the Australia release.

## Now Assist highlights for the Australia release

-   **[Merge duplicate articles](https://www.servicenow.com/docs/access?context=merge-duplicate-articles&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

    Merge selected duplicate knowledge articles into a new consolidated article using Now Assist in Knowledge Management. The merge preserves references to source articles and helps maintain a clean, high‑quality knowledge base.


**Important:** Now Assist is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist to Australia

If you customized actions on the user interface or other items that are associated with Now Assist skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions might not work as expected.

If you run into issues when you're upgrading a Now Assist product, see the [Issues and mitigation for Now Assist \(generative AI\) Applications and Plugin updates \[KB1637452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) article in the Now Support Knowledge Base. Log in to view the article.

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform. These changes include a new read\_only\_option field with granular control levels, including strict\_read\_onlyand client\_script\_modifiable. The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen instance security while preserving flexibility. If you have custom client scripts that modify read‑only fields using `g_form.setValue()` or `g_form.clearValue()`, refer to the [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) article in the Now Support Knowledge Base to identify affected fields and adjust the settings.

The existing access control lists \(ACLs\) have been updated to replace the admin role with purpose-driven granular roles within scripts or security attributes. As part of this update, the `getRoles()` API is replaced with the `hasRole()` API for authorization purposes. Additionally, all references to the admin role in the code have been substituted with the granular roles for authorization use cases. For more information, see [https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html](https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html).

## New in the Australia release

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow AI Platform now brings you an AI native experience with three licensing tiers available:

    -   Foundation: AI agents and skills to deliver insights
    -   Advanced: AI agents and skills to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI agents and skills, and create your own
-   **[Merge duplicate articles](https://www.servicenow.com/docs/access?context=merge-duplicate-articles&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

    Use Now Assist in Knowledge Management to merge selected duplicate knowledge articles into a single consolidated article, preserving references to the original sources and maintaining a high‑quality, well‑organized knowledge base.


## Changed in this release

-   **[Now Assist Conversational Help](https://www.servicenow.com/docs/access?context=conversational-help-skills&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    The discovery of Conversational Help Skills from Now Assist panel is no longer configured as auto-enabled.


## Activation information

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    Now Assist features are available with activation of any Now Assist plugin from ServiceNow Store. The following plugins are available:

    -   [Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
    -   [Now Assist for App Engine](https://www.servicenow.com/docs/access?context=add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise&version=australia&pubname=australia-application-development&ft:locale=en-US)
    -   [Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)
    -   [Now Assist for Collaborative Work Management \(CWM\)](https://www.servicenow.com/docs/access?context=now-assist-for-cwm-landing&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
    -   
    -   [Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)
    -   [Now Assist for Employee Experience](https://www.servicenow.com/docs/access?context=now-assisit-employee-exp&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
    -   [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)
    -   [Now Assist for Operational Sustainability \(formerly ESG\)](https://www.servicenow.com/docs/access?context=now-assist-for-esg&version=australia&pubname=australia-environmental-social-governance&ft:locale=en-US)
    -   [Now Assist for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=australia&pubname=australia-field-service-management&ft:locale=en-US)
    -   [Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)
    -   [Now Assist for Hardware Asset Management \(HAM\)](https://www.servicenow.com/docs/access?context=now-assist-ham&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)
    -   [Now Assist for Health and Safety](https://www.servicenow.com/docs/access?context=now-assist-hs-landing&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
    -   [Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
    -   [Now Assist for Integrated Risk Management \(IRM\)](https://www.servicenow.com/docs/access?context=now-assist-for-irm&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
    -   [Now Assist for ITOM](https://www.servicenow.com/docs/access?context=now-assist-itom&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)
    -   [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)
    -   [Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-landing&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
    -   [Operational Technology \(OT\) Manager Foundation](https://www.servicenow.com/docs/access?context=now-assist-for-otm-landing&version=australia&pubname=australia-operational-technology&ft:locale=en-US)
    -   [Now Assist for Operational Technology Service Management \(OTSM\)](https://www.servicenow.com/docs/access?context=now-assist-for-operational-technology-service-management&version=australia&pubname=australia-operational-technology&ft:locale=en-US)
    -   [Now Assist for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-management&version=australia&pubname=australia-order-management&ft:locale=en-US)
    -   [Now Assist for Public Sector Digital Services \(PSDS\)](https://www.servicenow.com/docs/access?context=now-assist-for-psds&version=australia&pubname=australia-government-industry&ft:locale=en-US)
    -   [Now Assist for Sales Force Automation \(SFA\)](https://www.servicenow.com/docs/access?context=now-assist-for-sales-and-order-management-som&version=australia&pubname=australia-order-management&ft:locale=en-US)
    -   [Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&version=australia&pubname=australia-security-management&ft:locale=en-US)
    -   [Now Assist for Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=now-assist-sam&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)
    -   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
    -   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)
    -   [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
    -   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)
    -   [Now Assist for Third-party Risk Management \(TPRM\)](https://www.servicenow.com/docs/access?context=now-assist-tprm&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
    -   [Now Assist for Workplace Service Delivery \(WSD\)](https://www.servicenow.com/docs/access?context=now-assist-wsd-landing&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)
    -   [Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=now-assist-for-vulnerability-response-landing&version=australia&pubname=australia-security-management&ft:locale=en-US)
    -   [Now Assist for Zero Copy Connector](https://www.servicenow.com/docs/access?context=now-assist-for-zero-copy-connector-for-erp&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)

## Plugin information

-   **[Now Assist Conversational Help](https://www.servicenow.com/docs/access?context=conversational-help-skills&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    The following plugin is planned for deprecation in a future release:

    Conversational Help Skills: Planned for deprecation in May 2026. Install the External Content Connectors Application Suite from the [ServiceNow store](https://store.servicenow.com/store/app/dd69bc781bd9a650396216db234bcb0b). For configuration guidance, see [External Content Connectors](https://www.servicenow.com/docs/access?context=ext-cont-connectors-landing-page&version=australia&pubname=australia-platform-administration&ft:locale=en-US) .


## Additional requirements

The Next Experience UI Framework must be enabled before you can use the Now Assist panel.

## Browser requirements

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Internet Explorer.

## Localization information

Now Assist supports Dynamic Translation for Australia.

## Related ServiceNow applications and features

-   **[AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

    The ServiceNow® AI Search application provides a consumer-grade search engine for Service Portal, Now Mobile, and Virtual Agent. Intelligent query features help you quickly find the answers that you need.

-   **[Document Intelligence](https://www.servicenow.com/docs/access?context=document-intelligence-landing&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow®Document Intelligence \(DocIntel\) application is an AI solution that enables any organization to automate and accelerate the process of extracting data from documents. That data can easily be integrated into larger automation workflows to save time and resources.

-   **[Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

    The ServiceNow® Dynamic Translation application enables you to dynamically translate text entered in an application or chat window for a seamless localization experience.

-   **[Generative AI Controller](https://www.servicenow.com/docs/access?context=generative-ai-controller&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow® Generative AI Controller helps you integrate third-party LLMs with your workflows.

-   **[Knowledge Management](https://www.servicenow.com/docs/access?context=knowledge-management&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

    The ServiceNow® Knowledge Management application enables the sharing of information in Knowledge Base. A Knowledge Base contains articles that provide users with information such as self-help, troubleshooting, and task resolution.

-   **[Knowledge Center](https://www.servicenow.com/docs/access?context=knowledge-center&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

    The ServiceNow® Knowledge Center plugin helps you manage your knowledge articles from a single interface consisting of dashboards that provide metrics of articles and facilitate swift actions.

-   **[Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)**

    Use generative AI skills in your conversational experiences. Now Assist in Virtual Agent uses LLMs to create a natural-language, conversational experience that can improve the success of your self-service workflows.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

