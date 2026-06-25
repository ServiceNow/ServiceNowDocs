---
title: Now Assist release notes
description: The ServiceNow Now Assist experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. Now Assist was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
---

# Now Assist release notes

The ServiceNow® Now Assist experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. Now Assist was enhanced and updated in the Australia release.

## Now Assist highlights for the Australia release

[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

-   Now Assist Guardian is enabled by default and detects prompt injection attempts and offensive content without manual activation.
-   Configure prompt injection detection separately for each Now Assist skill.
-   Create knowledge articles from Now Assist using files stored in Box.
-   Improve the clarity and accessibility of your articles with the AI-powered prompt Reading Ease scan.

-   **[Merge duplicate articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/merge-duplicate-articles.md)**

    Merge selected duplicate knowledge articles into a new consolidated article using Now Assist in Knowledge Management. The merge preserves references to source articles and helps maintain a clean, high‑quality knowledge base.


**Important:** Now Assist is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist to Australia

If you customized actions on the user interface or other items that are associated with Now Assist skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions might not work as expected.

If you run into issues when you're upgrading a Now Assist product, see the [Issues and mitigation for Now Assist \(generative AI\) Applications and Plugin updates \[KB1637452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) article in the Now Support Knowledge Base. Log in to view the article.

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform. These changes include a new read\_only\_option field with granular control levels, including strict\_read\_only and client\_script\_modifiable. The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen instance security while preserving flexibility. If you have custom client scripts that modify read‑only fields using `g_form.setValue()` or `g_form.clearValue()`, refer to the [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) article in the Now Support Knowledge Base to identify affected fields and adjust the settings.

The existing access control lists \(ACLs\) have been updated to replace the admin role with purpose-driven granular roles within scripts or security attributes. As part of this update, the `getRoles()` API is replaced with the `hasRole()` API for authorization purposes. Additionally, all references to the admin role in the code have been substituted with the granular roles for authorization use cases. For more information, see [Granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/granular-admin-roles.md).

## New in the Australia release

-   **[Create knowledge articles using Now Assist and Box](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-create-article-with-Box.md)**

    The Knowledge Center now integrates with Box. This integration enables authors to use stored files as a source for generating knowledge articles with Now Assist.


-   **[Now Assist Guardian enabled by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/now-assist-guardian.md)**

    Detect and log prompt injection attempts across all generative AI applications and features, and offensive content in supported Now Assist skills, by default. You can configure Now Assist Guardian to block AI-generated responses when an attempt is detected.

-   **[Using Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/using-now-assist-admin_0.md)**

    Explore additional user interface tabs of a Now Assist skill within a selected workflow. Access the usage and analytics of that skill. You can also view and manage the security and governance details of the selected skills.

-   **[Create knowledge articles using Now Assist and Box](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-create-article-with-Box.md)**

    Knowledge Center integrates with **Box**, enabling authors to use stored files as a source for generating knowledge articles with Now Assist.

-   **[Article Optimization with Reading Ease scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-reading-ease-scan.md)**

    The AI-based **Reading Ease** scan, integrated into the article optimization feature of Knowledge Center, scans articles for readability, provides actionable recommendations, and supports ongoing article improvement.

-   **[Configure prompt injection detection for Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/configure-prompt-injection-attack-protection.md)**

    Set the prompt injection detection action and severity level for Now Assist skills. Prompt injection detection is enabled by default for all Now Assist skills, except Platform skills and custom skills. When a skill has its own setting, Now Assist Guardian automatically applies the more protective of the two settings, the skill-level setting or the instance-level setting.

-   **[Visual Q&amp;A in Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-qa-genius-result.md)**

    Upload screenshots, error images, or documents in the Now Assist panel and get AI-generated answers about content without leaving your current context.

-   **[Catalog experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-premium.md)**

    Navigate away from a catalog form mid-completion and a modal appears asking whether you want to stay or leave, preventing accidental loss of your work. After you submit a catalog item, you can select View Details to open the submitted record.

-   **[Enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-premium.md)**

    Switch between multiple interactive views — such as knowledge articles, catalogs, and org charts — within a single conversation using a new dropdown in the Now Assist panel. When more than six promoted topics are available, you can select a category on the topic menu to see all of them at once.

-   **[Image and document upload](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-premium.md)**

    Upload images and screenshots directly into the Now Assist panel as part of your conversation and the Now Assist interprets the visual content to answer your questions or generate summaries.

-   **[Maintain and display the right context](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-premium.md)**

    Open the Now Assist panel while working on an incident record and you automatically see the most recent conversation tied to that incident. You can continue chatting about the incident or switch to unrelated topics in the same session, keeping your work in context without losing your place.


-   **[Using Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/using-now-assist-admin_0.md)**

    Explore the archive option from navigation pane within Now Assist Admin and archive custom and copies of Now Assist skills.


-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you an AI native experience with three licensing tiers available:

    -   Foundation: AI agents and skills to deliver insights
    -   Advanced: AI agents and skills to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI agents and skills, and create your own
-   **[Merge duplicate articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/merge-duplicate-articles.md)**

    Use Now Assist in Knowledge Management to merge selected duplicate knowledge articles into a single consolidated article, preserving references to the original sources and maintaining a high‑quality, well‑organized knowledge base.


## Changed in this release

-   **[Now Assist Conversational Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/conversational-help-skills.md)**

    The discovery of Conversational Help Skills from the Now Assist panel is no longer configured as auto-enabled.


## Deprecated features

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   Starting with the [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md) release, Conversational Help Skills is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

-   **[Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills.md)**

    Now Assist features are available with activation of any Now Assist plugin from ServiceNow Store. The following plugins are available:

    -   [Now Assist for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-apo.md)
    -   
    -   [Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-landing-cmdb.md)
    -   [Now Assist for Collaborative Work Management \(CWM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-cwm-landing.md)
    -   
    -   [Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-csm.md)
    -   [Now Assist for Employee Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assisit-employee-exp.md)
    -   [Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/now-assist-ea.md)
    -   [Now Assist for Operational Sustainability \(formerly ESG\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/now-assist-for-esg.md)
    -   [Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-fsm.md)
    -   [Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations.md)
    -   [Now Assist for Hardware Asset Management \(HAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-ham.md)
    -   [Now Assist for Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-hs-landing.md)
    -   [Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-hrsd.md)
    -   [Now Assist for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/now-assist-for-irm.md)
    -   [Now Assist for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-itom.md)
    -   [Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-itsm.md)
    -   [Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-lsd-landing.md)
    -   [Operational Technology \(OT\) Manager Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/now-assist-for-otm-landing.md)
    -   [Now Assist for Operational Technology Service Management \(OTSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/now-assist-for-operational-technology-service-management.md)
    -   [Now Assist for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-order-management.md)
    -   [Now Assist for Public Sector Digital Services \(PSDS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/now-assist-for-psds.md)
    -   [Now Assist for Sales Force Automation \(SFA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-for-sales-and-order-management-som.md)
    -   [Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-security-incident-landing.md)
    -   [Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-sam.md)
    -   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-slo.md)
    -   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/now-assist-spo.md)
    -   [Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-spm.md)
    -   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-spmc.md)
    -   [Now Assist for Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/now-assist-tprm.md)
    -   [Now Assist for Workplace Service Delivery \(WSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-wsd-landing.md)
    -   [Now Assist for Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-vulnerability-response-landing.md)
    -   [Now Assist for Zero Copy Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/now-assist-for-zero-copy-connector-for-erp.md)

## Plugin information

-   **[Now Assist Conversational Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/conversational-help-skills.md)**

    The following plugin is planned for deprecation in a future release:

    Conversational Help Skills: Planned for deprecation in May 2026. Install the External Content Connectors Application Suite from the [ServiceNow store](https://store.servicenow.com/store/app/dd69bc781bd9a650396216db234bcb0b). For configuration guidance, see [External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ext-cont-connectors-landing-page.md).


## Additional requirements

The Next Experience UI Framework must be enabled before you can use the Now Assist panel.

## Browser requirements

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Internet Explorer.

## Localization information

Now Assist supports Dynamic Translation for Australia.

## Related ServiceNow applications and features

-   **[AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/overview-ais.md)**

    The ServiceNow® AI Search application provides a consumer-grade search engine for Service Portal, Now Mobile, and Virtual Agent. Intelligent query features help you quickly find the answers that you need.

-   **[Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/document-intelligence-landing.md)**

    The ServiceNow®Document Intelligence \(DocIntel\) application is an AI solution that enables any organization to automate and accelerate the process of extracting data from documents. That data can easily be integrated into larger automation workflows to save time and resources.

-   **[Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation-overview.md)**

    The ServiceNow® Dynamic Translation application enables you to dynamically translate text entered in an application or chat window for a seamless localization experience.

-   **[Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generative-ai-controller.md)**

    The ServiceNow® Generative AI Controller helps you integrate third-party LLMs with your workflows.

-   **[Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management.md)**

    The ServiceNow® Knowledge Management application enables the sharing of information in Knowledge Base. A Knowledge Base contains articles that provide users with information such as self-help, troubleshooting, and task resolution.

-   **[Knowledge Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-center.md)**

    The ServiceNow® Knowledge Center plugin helps you manage your knowledge articles from a single interface consisting of dashboards that provide metrics of articles and facilitate swift actions.

-   **[Now Assist in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-va-landing.md)**

    Use generative AI skills in your conversational experiences. Now Assist in Virtual Agent uses LLMs to create a natural-language, conversational experience that can improve the success of your self-service workflows.


**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-rn-landing.md)

