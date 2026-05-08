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

-   **Merge duplicate articles**

    Merge selected duplicate knowledge articles into a new consolidated article using Now Assist in Knowledge Management. The merge preserves references to source articles and helps maintain a clean, high‑quality knowledge base.


**Important:** Now Assist is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist to Australia

If you customized actions on the user interface or other items that are associated with Now Assist skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions might not work as expected.

If you run into issues when you're upgrading a Now Assist product, see the [Issues and mitigation for Now Assist \(generative AI\) Applications and Plugin updates \[KB1637452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) article in the Now Support Knowledge Base. Log in to view the article.

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform. These changes include a new read\_only\_option field with granular control levels, including strict\_read\_onlyand client\_script\_modifiable. The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen instance security while preserving flexibility. If you have custom client scripts that modify read‑only fields using `g_form.setValue()` or `g_form.clearValue()`, refer to the [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) article in the Now Support Knowledge Base to identify affected fields and adjust the settings.

The existing access control lists \(ACLs\) have been updated to replace the admin role with purpose-driven granular roles within scripts or security attributes. As part of this update, the `getRoles()` API is replaced with the `hasRole()` API for authorization purposes. Additionally, all references to the admin role in the code have been substituted with the granular roles for authorization use cases. For more information, see [https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html](https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html).

## New in the Australia release

-   **Using Now Assist Admin**

    Explore the archive option from navigation pane within Now Assist Admin and archive custom and copies of Now Assist skills.


-   **ServiceNow product tiers**

    The ServiceNow AI Platform now brings you an AI native experience with three licensing tiers available:

    -   Foundation: AI agents and skills to deliver insights
    -   Advanced: AI agents and skills to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI agents and skills, and create your own
-   **Merge duplicate articles**

    Use Now Assist in Knowledge Management to merge selected duplicate knowledge articles into a single consolidated article, preserving references to the original sources and maintaining a high‑quality, well‑organized knowledge base.


## Changed in this release

-   **Now Assist Conversational Help**

    The discovery of Conversational Help Skills from Now Assist panel is no longer configured as auto-enabled.


## Deprecated features

[Australia Patch 1](../quality/australia-patch-1.md)

-   Starting with [Australia Patch 1](../quality/australia-patch-1.md) release, Conversational Help Skills is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

## Activation information

-   **Now Assist skills**

    Now Assist features are available with activation of any Now Assist plugin from ServiceNow Store. The following plugins are available:

    -   Now Assist for Accounts Payable Operations \(APO\)
    -   Now Assist for App Engine
    -   Now Assist for Configuration Management Database \(CMDB\)
    -   Now Assist for Collaborative Work Management \(CWM\)
    -   
    -   Now Assist for Customer Service Management \(CSM\)
    -   Now Assist for Employee Experience
    -   Now Assist for Enterprise Architecture \(EA\)
    -   Now Assist for Operational Sustainability \(formerly ESG\)
    -   Now Assist for Field Service Management \(FSM\)
    -   Now Assist for Financial Services Operations \(FSO\)
    -   Now Assist for Hardware Asset Management \(HAM\)
    -   Now Assist for Health and Safety
    -   Now Assist for HR Service Delivery \(HRSD\)
    -   Now Assist for Integrated Risk Management \(IRM\)
    -   Now Assist for ITOM
    -   Now Assist for IT Service Management \(ITSM\)
    -   Now Assist for Legal Service Delivery \(LSD\)
    -   Operational Technology \(OT\) Manager Foundation
    -   Now Assist for Operational Technology Service Management \(OTSM\)
    -   Now Assist for Order Management
    -   Now Assist for Public Sector Digital Services \(PSDS\)
    -   Now Assist for Sales Force Automation \(SFA\)
    -   Now Assist for Security Incident Response
    -   Now Assist for Software Asset Management \(SAM\)
    -   Now Assist for Supplier Lifecycle Operations \(SLO\)
    -   Now Assist for Sourcing and Procurement Operations \(SPO\)
    -   Now Assist for Strategic Portfolio Management \(SPM\)
    -   Now Assist for Telecommunications, Media and Technology \(TMT\)
    -   Now Assist for Third-party Risk Management \(TPRM\)
    -   Now Assist for Workplace Service Delivery \(WSD\)
    -   Now Assist for Vulnerability Response
    -   Now Assist for Zero Copy Connector

## Plugin information

-   **Now Assist Conversational Help**

    The following plugin is planned for deprecation in a future release:

    Conversational Help Skills: Planned for deprecation in May 2026. Install the External Content Connectors Application Suite from the [ServiceNow store](https://store.servicenow.com/store/app/dd69bc781bd9a650396216db234bcb0b). For configuration guidance, see External Content Connectors .


## Additional requirements

The Next Experience UI Framework must be enabled before you can use the Now Assist panel.

## Browser requirements

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Internet Explorer.

## Localization information

Now Assist supports Dynamic Translation for Australia.

## Related ServiceNow applications and features

-   **AI Search**

    The ServiceNow® AI Search application provides a consumer-grade search engine for Service Portal, Now Mobile, and Virtual Agent. Intelligent query features help you quickly find the answers that you need.

-   **Document Intelligence**

    The ServiceNow®Document Intelligence \(DocIntel\) application is an AI solution that enables any organization to automate and accelerate the process of extracting data from documents. That data can easily be integrated into larger automation workflows to save time and resources.

-   **Dynamic Translation**

    The ServiceNow® Dynamic Translation application enables you to dynamically translate text entered in an application or chat window for a seamless localization experience.

-   **Generative AI Controller**

    The ServiceNow® Generative AI Controller helps you integrate third-party LLMs with your workflows.

-   **Knowledge Management**

    The ServiceNow® Knowledge Management application enables the sharing of information in Knowledge Base. A Knowledge Base contains articles that provide users with information such as self-help, troubleshooting, and task resolution.

-   **Knowledge Center**

    The ServiceNow® Knowledge Center plugin helps you manage your knowledge articles from a single interface consisting of dashboards that provide metrics of articles and facilitate swift actions.

-   **Now Assist in Virtual Agent**

    Use generative AI skills in your conversational experiences. Now Assist in Virtual Agent uses LLMs to create a natural-language, conversational experience that can improve the success of your self-service workflows.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

