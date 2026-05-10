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

-   **[Merge duplicate articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-in-knowledge-management/merge-duplicate-articles.md)**

    Merge selected duplicate knowledge articles into a new consolidated article using Now Assist in Knowledge Management. The merge preserves references to source articles and helps maintain a clean, high‑quality knowledge base.


**Important:** Now Assist is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist to Australia

If you customized actions on the user interface or other items that are associated with Now Assist skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions might not work as expected.

If you run into issues when you're upgrading a Now Assist product, see the [Issues and mitigation for Now Assist \(generative AI\) Applications and Plugin updates \[KB1637452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) article in the Now Support Knowledge Base. Log in to view the article.

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform. These changes include a new read\_only\_option field with granular control levels, including strict\_read\_onlyand client\_script\_modifiable. The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen instance security while preserving flexibility. If you have custom client scripts that modify read‑only fields using `g_form.setValue()` or `g_form.clearValue()`, refer to the [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) article in the Now Support Knowledge Base to identify affected fields and adjust the settings.

The existing access control lists \(ACLs\) have been updated to replace the admin role with purpose-driven granular roles within scripts or security attributes. As part of this update, the `getRoles()` API is replaced with the `hasRole()` API for authorization purposes. Additionally, all references to the admin role in the code have been substituted with the granular roles for authorization use cases. For more information, see [https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html](https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html).

## New in the Australia release

-   **[Using Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/using-now-assist-admin_0.md)**

    Explore the archive option from navigation pane within Now Assist Admin and archive custom and copies of Now Assist skills.


-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you an AI native experience with three licensing tiers available:

    -   Foundation: AI agents and skills to deliver insights
    -   Advanced: AI agents and skills to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI agents and skills, and create your own
-   **[Merge duplicate articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-in-knowledge-management/merge-duplicate-articles.md)**

    Use Now Assist in Knowledge Management to merge selected duplicate knowledge articles into a single consolidated article, preserving references to the original sources and maintaining a high‑quality, well‑organized knowledge base.


## Changed in this release

-   **[Now Assist Conversational Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/conversational-help-skills.md)**

    The discovery of Conversational Help Skills from Now Assist panel is no longer configured as auto-enabled.


## Deprecated features

[Australia Patch 1](../quality/australia-patch-1.md)

-   Starting with [Australia Patch 1](../quality/australia-patch-1.md) release, Conversational Help Skills is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

## Activation information

-   **[Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills.md)**

    Now Assist features are available with activation of any Now Assist plugin from ServiceNow Store. The following plugins are available:

    -   
    -   [Now Assist for App Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-app-engine/add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise.md)
    -   [Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-landing-cmdb.md)
    -   [Now Assist for Collaborative Work Management \(CWM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-collaborative-work-management-cwm/now-assist-for-cwm-landing.md)
    -   
    -   [Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm.md)
    -   [Now Assist for Employee Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/now-assisit-employee-exp.md)
    -   [Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/now-assist-ea.md)
    -   [Now Assist for Operational Sustainability \(formerly ESG\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/now-assist-for-esg.md)
    -   [Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/now-assist-fsm.md)
    -   [Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/now-assist-for-financial-services-operations.md)
    -   [Now Assist for Hardware Asset Management \(HAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-hardware-asset-management/now-assist-ham.md)
    -   [Now Assist for Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-health-and-safety/now-assist-hs-landing.md)
    -   [Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd.md)
    -   [Now Assist for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/now-assist-for-irm.md)
    -   [Now Assist for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/now-assist-itom.md)
    -   [Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm.md)
    -   [Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-legal-service-delivery/now-assist-lsd-landing.md)
    -   [Operational Technology \(OT\) Manager Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/now-assist-for-otm-landing.md)
    -   [Now Assist for Operational Technology Service Management \(OTSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/now-assist-for-operational-technology-service-management.md)
    -   [Now Assist for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-order-management.md)
    -   [Now Assist for Public Sector Digital Services \(PSDS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/now-assist-for-psds.md)
    -   [Now Assist for Sales Force Automation \(SFA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-for-sales-and-order-management-som.md)
    -   [Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-security-incident-landing.md)
    -   [Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-software-asset-management-sam/now-assist-sam.md)
    -   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo.md)
    -   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo.md)
    -   [Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/now-assist-spm.md)
    -   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-spmc.md)
    -   [Now Assist for Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/now-assist-tprm.md)
    -   [Now Assist for Workplace Service Delivery \(WSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-wsd/now-assist-wsd-landing.md)
    -   [Now Assist for Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-vulnerability-response-vr/now-assist-for-vulnerability-response-landing.md)
    -   [Now Assist for Zero Copy Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/now-assist-for-zero-copy-connector-for-erp.md)

## Plugin information

-   **[Now Assist Conversational Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/conversational-help-skills.md)**

    The following plugin is planned for deprecation in a future release:

    Conversational Help Skills: Planned for deprecation in May 2026. Install the External Content Connectors Application Suite from the [ServiceNow store](https://store.servicenow.com/store/app/dd69bc781bd9a650396216db234bcb0b). For configuration guidance, see [External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/ext-cont-connectors-landing-page.md) .


## Additional requirements

The Next Experience UI Framework must be enabled before you can use the Now Assist panel.

## Browser requirements

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Internet Explorer.

## Localization information

Now Assist supports Dynamic Translation for Australia.

## Related ServiceNow applications and features

-   **[AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/overview-ais.md)**

    The ServiceNow® AI Search application provides a consumer-grade search engine for Service Portal, Now Mobile, and Virtual Agent. Intelligent query features help you quickly find the answers that you need.

-   **[Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/document-intelligence/document-intelligence-landing.md)**

    The ServiceNow®Document Intelligence \(DocIntel\) application is an AI solution that enables any organization to automate and accelerate the process of extracting data from documents. That data can easily be integrated into larger automation workflows to save time and resources.

-   **[Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation/dynamic-translation-overview.md)**

    The ServiceNow® Dynamic Translation application enables you to dynamically translate text entered in an application or chat window for a seamless localization experience.

-   **[Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generative-ai-controller/generative-ai-controller.md)**

    The ServiceNow® Generative AI Controller helps you integrate third-party LLMs with your workflows.

-   **[Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/knowledge-management.md)**

    The ServiceNow® Knowledge Management application enables the sharing of information in Knowledge Base. A Knowledge Base contains articles that provide users with information such as self-help, troubleshooting, and task resolution.

-   **[Knowledge Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-center.md)**

    The ServiceNow® Knowledge Center plugin helps you manage your knowledge articles from a single interface consisting of dashboards that provide metrics of articles and facilitate swift actions.

-   **[Now Assist in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/now-assist-in-va-landing.md)**

    Use generative AI skills in your conversational experiences. Now Assist in Virtual Agent uses LLMs to create a natural-language, conversational experience that can improve the success of your self-service workflows.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

