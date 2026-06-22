---
title: Combined Agent experience for CSM release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Agent experience for CSM from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-agentexperienceforcsm-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Agent experience for CSM release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Agent experience for CSM from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Agent experience for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Agent experience for CSM to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Agent experience for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&family=xanadu&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Chat interaction session tabs](https://www.servicenow.com/docs/access?context=csm-workspace-chat-session-tabs&family=yokohama&ft:locale=en-US)**

Use the following features to provide your agents with information about their current chats:

    -   Display informational messages in the session tabs that notify the agent of the current chat condition such as "Chat is in wrap-up" or "Chat has ended."
    -   Use background colors to distinguish between the active and inactive tabs. For inactive tabs, configure different colors to alert agents to the chat threshold timers.
    -   Use a counter to display the number of unread chat messages.
    -   Use a separator in the chat window between the older messages and the newer unread messages.
    -   Configure a minimum of one and up to a maximum of three chat SLA threshold timers that alert agents to unread messages in inactive chats. For each level, you can also select a time value and a unique color.
-   **[Voice interaction record page](https://www.servicenow.com/docs/access?context=csm-native-voice-record-page&family=yokohama&ft:locale=en-US)**

Enable Contact Center as a Service \(CCaaS\) providers to display native voice integrations in CSM Configurable Workspace that agents can use to handle phone calls.

-   **[Interaction wrap-up for call and chat](https://www.servicenow.com/docs/access?context=interaction-wrapup-modeless-dialog&family=yokohama&ft:locale=en-US)**

Provide agents with enough dedicated time after each call or chat to finalize the interaction details and wrap up their work before starting a new conversation.

-   **[Customer history component](https://www.servicenow.com/docs/access?context=customer-central&family=yokohama&ft:locale=en-US)**

Enable agents to view a customer's activities in the contextual side panel. Agents can search and filter the activities in the list and select a date range. For more information about the Customer history component, see [Next Experience Components documentation](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades).

-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&family=yokohama&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Agent experience for CSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Email enhancements](https://www.servicenow.com/docs/access?context=csm-front-line-case-page-modeless-dialogs&family=xanadu&ft:locale=en-US)**

The Compose Email modeless dialog includes the following enhancements:

    -   A collapsible header that includes the **To**, **Cc**, **Bcc**, and **Subject** fields.
    -   Icons in the footer that enable you to discard the current email draft, apply a template, view a list of recent email drafts, and add attachments.
    -   Compose Email modeless dialog that you can open to see the last saved email draft.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Form template enhancements](https://www.servicenow.com/docs/access?context=csm-workspace-form-templates&family=yokohama&ft:locale=en-US)**

Use the following form template enhancements to create or edit templates as needed:

    -   The **Templates** tab in the configurable side panel displays larger template cards with the template name and an expanded description. Users can view different lists of templates, mark their favorites, and sort templates either alphabetically or by last used.
    -   The template form displays template fields in a clearly labeled form section and displays the line numbers and headings for each template line to improve readability
    -   The template tab header displays "Edit template" when a user opens a template in edit mode.
-   **[Front-line case page integration with knowledge guidance](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&family=yokohama&ft:locale=en-US)**

Enable agents to attach and add links to knowledge articles in comments, work notes, or emails by using modeless dialogs.

-   **[Resurface special handling notes](https://www.servicenow.com/docs/access?context=c_OnScreenAlerts&family=yokohama&ft:locale=en-US)**

Display the special handling notes for a case at any time by selecting **Special handling notes** from the More actions menu on the case record action bar.

-   **[Customer Central application moved from family to store release](https://www.servicenow.com/docs/access?context=customer-central&family=yokohama&ft:locale=en-US)**

Starting with the Yokohama release, the Customer Central application \(com.sn\_csm\_customer\_central\) has moved to the ServiceNow Store. Any new enhancements to this application are delivered through the Customer Central store app.

-   **[Customer Activity Guided Setup now accessible from a new location](https://www.servicenow.com/docs/access?context=configure-customer-activity&family=yokohama&ft:locale=en-US)**

Use the following updates in Guided Setup to enhance navigation and access customer history configurations:

    -   Access the Customer Activity Guided Setup from **All** &gt; **Customer Central** &gt; **Customer Activity** &gt; **Guided Setup**.
    -   View Activity Contexts, Activity Types, Activity Groups, and Activity Type Templates within Guided Setup. You can also access them in the menu by navigating to **All** &gt; **Customer Central** &gt; **Customer Activity** &gt; **Guided Setup**.
    -   Customer Activity has been renamed to Customer History, maintaining the same functionality.
    -   Access the Business Rule in the Activity Feed where it is now listed independently alongside Activity Types, Activity Groups, and Activity Type Templates for improved accessibility. Previously, it was nested under Activity Types.
-   **[Front-line case page lookup component](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&family=yokohama&ft:locale=en-US)**

The Front-line case page includes the following enhancements:

    -   Includes the Consumer lookup component.
    -   Uses advanced search to look up contacts and consumers.
    -   Contact and consumer record cards can be collapsed to display more record space.
-   **[Action bar layout](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&family=yokohama&ft:locale=en-US)**

The following interaction record pages include an action bar with a single action layout:

    -   CSM Interaction record page
    -   CSM voice interaction record page
-   **[Comment and Work note modeless dialogs](https://www.servicenow.com/docs/access?context=csm-front-line-case-page-modeless-dialogs&family=yokohama&ft:locale=en-US)**

Create and use form templates that add content to the **Additional comments** and **Work notes** fields on a case record. Automatically display a modeless dialog that includes the content from the form template and then post that content to the activity stream.

-   **[Front-line case page contextual side panel](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&family=yokohama&ft:locale=en-US)**

The Record Information tab in the contextual side panel includes the Overview and Active SLA cards. The contact card and timeline card have been removed to improve the page load time.

-   **[Recommended Actions AI search replaces Agent Assist](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&family=yokohama&ft:locale=en-US)**

Recommended Actions AI search replaces Agent Assist in the contextual side panel for the following record pages included with the CSM Configurable Workspace:

    -   CSM default record page
    -   Front-line case page
    -   CSM Interaction record page \(for type = Chat, Video, Walkup, Email\)
-   **[Customer History component features](https://www.servicenow.com/docs/access?context=customer-history-component-features&family=yokohama&ft:locale=en-US)**

Use the following features to provide agents real-time updates and customer history details:

    -   Automatically refresh the Customer History component when account, contact, or consumer details change.
    -   Prompt agents to add missing account or contact details instead of leaving fields empty.
    -   Display an empty component until an agent links a contact using the lookup component, then show the contact's details.
    -   Enables agent to view updated customer information directly in Customer History on the Front-line Case page.

</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Agent experience for CSM features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Agent experience for CSM features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Starting with the Xanadu release, CSM Agent Workspace is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. [CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-workspaces-configure&family=xanadu&ft:locale=en-US) provides the latest experience for this functionality.

</td></tr><tr><td>

Yokohama

</td><td>

Starting with the Yokohama release, Customer Service CTI Demo Data is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. ServiceNow Voice with Amazon Connect provide the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Agent experience for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install CSM Configurable Workspace by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

CSM Configurable Workspace is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&family=yokohama&ft:locale=en-US).

 Install CSM Configurable Workspace by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Agent experience for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Agent experience for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Agent experience for CSM, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The following templates were updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

-   [Case playbook: horizontal stages template](https://www.servicenow.com/docs/access?context=csm-playbook-templates&family=xanadu&ft:locale=en-US)
-   [Case playbook: vertical stages template](https://www.servicenow.com/docs/access?context=csm-playbook-templates&family=xanadu&ft:locale=en-US)

 This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=xanadu&ft:locale=en-US) for details.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Agent experience for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Agent experience for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Expand and collapse the header in the Compose Email modeless dialog to edit address fields or increase your working space in the email body.
-   Use icons to quickly access email tools such as applying a template or adding an attachment.
-   Open the Compose Email modeless dialog with the last saved email draft.

 See [CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-workspaces-configure&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Alert agents about the status of current chats by using color-coded session tabs to indicate service level agreement \(SLA\) threshold timers, chat duration, and unread message counts.
-   Create form templates or modify existing templates with enhancements to the form template feature.
-   Integrate enhanced knowledge guidance on the Front-line case page and enable agents to attach and add links to knowledge articles in comments, work notes, or emails by using modeless dialogs.
-   Display native voice configurations in CSM Configurable Workspace with the Voice interaction record page that agents can use to handle phone calls.
-   Dedicate time after each call or chat for agents to finalize interaction details.

 See [CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-workspaces-configure&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

