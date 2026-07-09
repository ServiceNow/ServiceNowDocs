---
title: Agent experience for CSM release notes
description: The ServiceNow Agent experience for CSM provides customer service agents with the tools that they need to find, research, and resolve customer issues and questions. Agent experience for CSM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 8
---

# Agent experience for CSM release notes

The ServiceNow® Agent experience for CSM provides customer service agents with the tools that they need to find, research, and resolve customer issues and questions. Agent experience for CSM was enhanced and updated in the Zurich release.

## Agent experience highlights for the Zurich release

-   Provide front-line agents with an updated chat interaction user experience that puts the chat component front and center.
-   Use the callback component to return customer calls and create interaction records at the time of the callback.
-   Provide agents with visibility to all previous customer activity and the ability to filter and search to find specific activities.
-   Initiate a comment, work note, or email in the activity stream in CSM Configurable Workspace and then open the text in a modeless dialog.

See [CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-workspaces-configure.md) for more information.

## New in the Agent experience for CSM release

-   **[CSM centered chat interaction record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-centered-chat-interaction-page.md)**

    Includes a chat component in the center of the record page that provides front-line chat agents with a modernized interaction page layout.

-   **[Callback component on the CSM voice interaction record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-native-voice-record-page.md#section_vtg_dzk_vfc)**

    Provides agents with the ability to return customer calls and to create interaction records at the time of callback.

-   **[Task SLA cards component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-record-page-sla-card-component.md)**

    Use the Task SLA cards component as a standalone component on the Front-line case page. Visual updates to the Task SLA cards component enable agents to see where they are in the lifecycle of multiple task SLAs at a glance.

-   **[Task activity timeline preset and controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-record-page-timeline-component.md)**

    Use the Task activity timeline preset and controller to add the Timeline component as a standalone component on task record pages such as case or incident.

-   **[Notifications for agent mentions in records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/notifications-for-agent-mentions-in-records.md)**

    Receive workspace notifications when agents are mentioned using @ in comments or work notes. Notifications include record details and a direct link for quick access.

-   **[Quick start tests for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/quick-start-tests-csm.md)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Thin compose modeless dialogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-front-line-case-page-modeless-dialogs.md#section_nws_1rs_rfc)**

    Enable agents to initiate a comment, work note, or email in the activity stream and then open the text in a modeless dialog. This feature is available on the following record pages:

    -   Front-line case page
    -   CSM default record page
    -   CSM Interaction record page
    -   CSM voice interaction record page
    -   CSM centered chat interaction record page
    -   Email interaction record page
-   **Activity Stream enhancements**
    -   Activity Stream layout now automatically adjusts to your device \(laptop, tablet, or mobile\). Hidden content is indicated by \(...\) for better readability.
-   **[Lookup component on CSM Configurable Workspace record pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-record-page-lookup-component.md)**

    Use the Lookup component to look up and link a contact and then verify the contact. The Lookup component replaces the Lookup and Verify component on the CSM Configurable Workspace record pages.

-   **Hide inbox after item selection**

    The Inbox panel collapses after selecting an inbox item, enabling agents to see more of the screen and focus on the interaction.

-   **Multi-form controller support**

    Supports having two forms on a record page.

-   **Real-time notification count updates**

    Updated the bell icon behavior so the notification count accurately reflects the number of unique, unread notifications in real time, eliminating duplicate increments.

-   **[Customer History enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/customer-history-component-features.md)**

    Use the following enhancements to control grouping, appearance, and refresh behavior in customer history:

    -   Enable time grouping by month or quarter: A new property enables selection of time grouping as monthly or quarterly \(Q1-Q4\) in date filters.
    -   Customize feed appearance: Admins can configure feed icons along with their background colors using a property that offers predefined color options.
    -   Display activities by updated date: A new property enables feeds to surface activities based on the last updated timestamp in Customer History.
    -   Dynamic refresh updates: Customer History feeds now refresh automatically, but only for records in the Customer History activities table and within the current context \(for example, Contact\). Other tables and parent records are not included.
    -   Introduced a new search icon that lets agents show or hide the search bar with a click.
-   **[Improve discoverability of Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-front-line-case-page.md)**

    Use the following updates to improve the visibility of Recommended Actions across key CSM pages:

    -   Set Recommended Actions as the default first tab in the contextual side panel to provide agents with instant access to recommendations without switching tabs. This change applies to the following pages:
        -   Front-line case page
        -   CSM default record page
        -   CSM Interaction record page
        -   Email interaction record page
        -   CSM voice interaction record page
        -   CSM centered chat interaction record page
    -   Load Recommended Actions asynchronously to keep the UI responsive while recommendations load.
    -   Enable agents to send relevant KB articles through SMS during voice interactions and messaging-type interactions.
-   **[Default recommendations for Pro customers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-front-line-case-page.md)**

    Recommendations are now delivered by default for Pro customers when either the Task Intelligence for CSM or the Now Assist for CSM plugin is installed. Agents can view contextual recommendations under the **Suggested Actions** tab, such as similar cases and open incidents, when the case meets the predefined criteria. Agents can link or copy resolutions directly into the current case.

-   **[Resurface special handling notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/c_OnScreenAlerts.md)**

    Display the special handling notes at any time by selecting  Special handling notes  from the More actions menu on the case record action bar. This action is now available on records from the following tables:

    -   Account
    -   Asset
    -   Contact
    -   Incident
    -   Product Model
    -   Work Order Task
    This applies only to records where special handling notes are configured.

-   **[Information session tab enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-workspace-chat-session-tabs-configure.md)**

    Use the following changes to enforce permissions and improve usability of the **Session** tab:

    -   Restrict access to unauthorized users with error messages and validate role-based permissions.
    -   Auto-save admin updates to timer and color changes in real time.
    -   Display workspace settings only after the Session tab is enabled.
-   **[Configure Alert Dismissal settings at experience and alert level](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/auto-dismiss-alerts-in-csm-configurable-workspace.md)**

    Use the following settings to control alert dismissal:

    -   Set alerts to auto-dismiss or require manual dismissal.
    -   Configure alert behavior globally or according to alert.
    -   Reduce alert overload while supporting accessibility standards, which helps agents focus on critical alerts.
-   **[ServiceNow Link Manager is available on the Google Chrome, Microsoft Edge, and Mozilla Firefox plugin store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-workspace-snow-link-manager.md)**

    Streamline tab management and reduce browser clutter with ServiceNow Link Manager:

    -   Automatically consolidates new ServiceNow related tabs into an existing open ServiceNow tab.
    -   Provides cross-platform support.
    -   Enables agents to share record links, such as cases, through platforms like Gmail, Microsoft Teams, Microsoft Outlook, and other web tools integrated with ServiceNow. These links open using ServiceNow Link Manager, ensuring the record loads in the correct workspace and context.
    -   Provides a user-friendly interface that is easy to enable and turn off directly from the extension settings in the respective browser.
-   **[Follow records to receive notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-default-record-page.md#section_follow_action)**

    Select the **Follow** action to receive notifications when comments or work notes are added to a record. The Follow action is available in the More actions menu on the [Front-line case page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-front-line-case-page.md) and the [CSM default record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-default-record-page.md).

-   **Information icon**

    Select the information icon on a reference field to display additional information about the record in a pop-up window. Starting with CSM Configurable Workspace Bundle version 5.0, the information displays in a pop-up window with an option to open in a separate tab instead of opening directly in a separate tab. This change applies to the following record pages:

    -   CSM Front-line case page
    -   CSM default record page
    -   CSM Interaction record page
    Users can use Cmd+click \(Mac\) or Ctrl+click \(Windows\) when selecting the information icon to use the previous behavior.


## Deprecations

Starting with the Yokohama release, Customer Service CTI Demo Data is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. ServiceNow Voice with Amazon Connect provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

CSM Configurable Workspace is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/t_ActivateCustomerService.md).

Install CSM Configurable Workspace by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/browser-support.md).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/c_CustomerServiceManagement.md)**

    Use the Customer Service Management application to provide the service and support that your external customers need.

-   **[Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/now-assist-csm.md)**

    Use the ServiceNow® Now Assist for CSM application to summarize customer chat conversations on interactions, summarize case details, and generate case resolution notes.

-   **[Next Experience UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/ui-builder-overview.md)**

    Next Experience UI Builder is a low-code web user interface builder that enables developers to build pages for workspace and portal web-based experiences. Use the base system and custom web components to build your pages.

-   **[Workspace UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/workspace-landing-page.md)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents need to find, research, and resolve issues. CSM Configurable Workspace is a customer service-specific implementation that provides tier 1 agents with the tools that they need to respond to customers and to resolve cases.


**Parent Topic:**[Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/customer-service-mgmt-rn-landing.md)

