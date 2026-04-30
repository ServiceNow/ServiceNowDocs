---
title: Agent experience for CSM release notes
description: The ServiceNow Agent experience for CSM provides customer service agents with the tools that they need to find, research, and resolve customer issues and questions. Agent experience for CSM was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-04-01"
reading_time_minutes: 7
---

# Agent experience for CSM release notes

The ServiceNow® Agent experience for CSM provides customer service agents with the tools that they need to find, research, and resolve customer issues and questions. Agent experience for CSM was enhanced and updated in the Yokohama release.

## Agent experience for CSM highlights for the Yokohama release

-   Alert agents about the status of current chats by using color-coded session tabs to indicate service level agreement \(SLA\) threshold timers, chat duration, and unread message counts.
-   Create form templates or modify existing templates with enhancements to the form template feature.
-   Integrate enhanced knowledge guidance on the Front-line case page and enable agents to attach and add links to knowledge articles in comments, work notes, or emails by using modeless dialogs.
-   Display native voice configurations in CSM Configurable Workspace with the Voice interaction record page that agents can use to handle phone calls.
-   Dedicate time after each call or chat for agents to finalize interaction details.

See [CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-workspaces-configure&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) for more information.

**Important:** The following applications are available in the ServiceNow Store:

-   CSM Configurable Workspace Bundle v5.0
-   Customer Central Bundle v1.0

For details, see the "Activation information" section of these release notes.

## New in the Agent experience for CSM release

-   **[Chat interaction session tabs](https://www.servicenow.com/docs/access?context=csm-workspace-chat-session-tabs&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use the following features to provide your agents with information about their current chats:

    -   Display informational messages in the session tabs that notify the agent of the current chat condition such as "Chat is in wrap-up" or "Chat has ended."
    -   Use background colors to distinguish between the active and inactive tabs. For inactive tabs, configure different colors to alert agents to the chat threshold timers.
    -   Use a counter to display the number of unread chat messages.
    -   Use a separator in the chat window between the older messages and the newer unread messages.
    -   Configure a minimum of one and up to a maximum of three chat SLA threshold timers that alert agents to unread messages in inactive chats. For each level, you can also select a time value and a unique color.
-   **[Voice interaction record page](https://www.servicenow.com/docs/access?context=csm-native-voice-record-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enable Contact Center as a Service \(CCaaS\) providers to display native voice integrations in CSM Configurable Workspace that agents can use to handle phone calls.

-   **[Interaction wrap-up for call and chat](https://www.servicenow.com/docs/access?context=interaction-wrapup-modeless-dialog&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Provide agents with enough dedicated time after each call or chat to finalize the interaction details and wrap up their work before starting a new conversation.

-   **[Customer history component](https://www.servicenow.com/docs/access?context=customer-central&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enable agents to view a customer's activities in the contextual side panel. Agents can search and filter the activities in the list and select a date range. For more information about the Customer history component, see [Next Experience Components documentation](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades).

-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


## Changed in this release

-   **[Form template enhancements](https://www.servicenow.com/docs/access?context=csm-workspace-form-templates&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use the following form template enhancements to create or edit templates as needed:

    -   The **Templates** tab in the configurable side panel displays larger template cards with the template name and an expanded description. Users can view different lists of templates, mark their favorites, and sort templates either alphabetically or by last used.
    -   The template form displays template fields in a clearly labeled form section and displays the line numbers and headings for each template line to improve readability
    -   The template tab header displays "Edit template" when a user opens a template in edit mode.
-   **[Front-line case page integration with knowledge guidance](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enable agents to attach and add links to knowledge articles in comments, work notes, or emails by using modeless dialogs.

-   **[Resurface special handling notes](https://www.servicenow.com/docs/access?context=c_OnScreenAlerts&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Display the special handling notes for a case at any time by selecting **Special handling notes** from the More actions menu on the case record action bar.

-   **[Customer Central application moved from family to store release](https://www.servicenow.com/docs/access?context=customer-central&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Starting with the Yokohama release, the Customer Central application \(com.sn\_csm\_customer\_central\) has moved to the ServiceNow Store. Any new enhancements to this application are delivered through the Customer Central store app.

-   **[Customer Activity Guided Setup now accessible from a new location](https://www.servicenow.com/docs/access?context=configure-customer-activity&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use the following updates in Guided Setup to enhance navigation and access customer history configurations:

    -   Access the Customer Activity Guided Setup from **All** &gt; **Customer Central** &gt; **Customer Activity** &gt; **Guided Setup**.
    -   View Activity Contexts, Activity Types, Activity Groups, and Activity Type Templates within Guided Setup. You can also access them in the menu by navigating to **All** &gt; **Customer Central** &gt; **Customer Activity** &gt; **Guided Setup**.
    -   Customer Activity has been renamed to Customer History, maintaining the same functionality.
    -   Access the Business Rule in the Activity Feed where it is now listed independently alongside Activity Types, Activity Groups, and Activity Type Templates for improved accessibility. Previously, it was nested under Activity Types.
-   **[Front-line case page lookup component](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US#section_dnl_3f4_s1c)**

    The Front-line case page includes the following enhancements:

    -   Includes the Consumer lookup component.
    -   Uses advanced search to look up contacts and consumers.
    -   Contact and consumer record cards can be collapsed to display more record space.
-   **[Action bar layout](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US#section_imv_qhs_mbc)**

    The following interaction record pages include an action bar with a single action layout:

    -   CSM Interaction record page
    -   CSM voice interaction record page
-   **[Comment and Work note modeless dialogs](https://www.servicenow.com/docs/access?context=csm-front-line-case-page-modeless-dialogs&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US#section_gzj_wlb_s2c)**

    Create and use form templates that add content to the **Additional comments** and **Work notes** fields on a case record. Automatically display a modeless dialog that includes the content from the form template and then post that content to the activity stream.

-   **[Front-line case page contextual side panel](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US#section_trg_ypr_m1c)**

    The Record Information tab in the contextual side panel includes the Overview and Active SLA cards. The contact card and timeline card have been removed to improve the page load time.

-   **[Recommended Actions AI search replaces Agent Assist](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US#section_trg_ypr_m1c)**

    Recommended Actions AI search replaces Agent Assist in the contextual side panel for the following record pages included with the CSM Configurable Workspace:

    -   CSM default record page
    -   Front-line case page
    -   CSM Interaction record page \(for type = Chat, Video, Walkup, Email\)
-   **[Customer History component features](https://www.servicenow.com/docs/access?context=customer-history-component-features&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use the following features to provide agents real-time updates and customer history details:

    -   Automatically refresh the Customer History component when account, contact, or consumer details change.
    -   Prompt agents to add missing account or contact details instead of leaving fields empty.
    -   Display an empty component until an agent links a contact using the lookup component, then show the contact's details.
    -   Enables agent to view updated customer information directly in Customer History on the Front-line Case page.

## Deprecations

Starting with the Yokohama release, Customer Service CTI Demo Data is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. ServiceNow Voice with Amazon Connect provide the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

CSM Configurable Workspace is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

Install CSM Configurable Workspace by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use the Customer Service Management application to provide the service and support that your external customers need.

-   **[Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use the ServiceNow® Now Assist for CSM application to summarize customer chat conversations on interactions, summarize case details, and generate case resolution notes.

-   **[Next Experience UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Next Experience UI Builder is a low-code web user interface builder that enables developers to build pages for workspace and portal web-based experiences. Use the base system and custom web components to build your pages.

-   **[Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents need to find, research, and resolve issues. CSM Configurable Workspace is a customer service-specific implementation that provides tier 1 agents with the tools that they need to respond to customers and to resolve cases.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

