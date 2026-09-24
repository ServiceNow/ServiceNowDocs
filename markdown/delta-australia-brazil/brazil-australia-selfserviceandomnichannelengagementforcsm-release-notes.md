---
title: Combined Self-service and omnichannel engagement for CSM release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Self-service and omnichannel engagement for CSM from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-selfserviceandomnichannelengagementforcsm-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 16
breadcrumb: [Products combined by family]
---

# Combined Self-service and omnichannel engagement for CSM release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Self-service and omnichannel engagement for CSM from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Self-service and omnichannel engagement for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Self-service and omnichannel engagement for CSM to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Upgrade information**

Introduced dynamic resizing to the Active Call Interaction Control toolbar. Buttons adapt to container width at runtime while keyboard navigation and focus order remain consistent.


</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Self-service and omnichannel engagement for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Voice call widget](https://www.servicenow.com/docs/access?context=portal-phone-widget&family=australia&ft:locale=en-US)**

Customers can now make voice calls directly from portal pages or the Engagement Messenger. Call context stays intact as customers navigate between pages. These calls connect to AI Voice Agents to deliver conversational voice experiences without relying on contact center platforms.

-   **[Integrate ServiceNow Voice with Amazon Connect](https://www.servicenow.com/docs/access?context=integrate-ccc-amazonconnect&family=australia&ft:locale=en-US)**

Use ServiceNow AI Voice Agents to build conversational voice experiences by routing calls from Amazon Connect, Five9, or NICE contact center channels to deliver natural, conversational customer interactions.


 -   **[Email interaction feature: Email reply routing and summarization](https://www.servicenow.com/docs/access?context=using-email-interaction-page&family=australia&ft:locale=en-US)**

The new capabilities for smart email routing and summarization are:

    -   Receive customer email replies on the correct open case or interaction automatically, with ServiceNow Otto® selecting the best-matching case when multiple open cases exist.
    -   Get AI summaries automatically on transfer and on demand, reducing the need to read the full email thread.
    -   See summaries instantly on page refresh without re-running AI, and refresh with one click when new activity arrives on the interaction.
**Note:** Check your entitlements to determine whether you have access to summarization and AI-based context matching.

-   **[Usage insights for ICC call events](https://www.servicenow.com/docs/access?context=usage-insight-for-icc-enabled-call-events&family=australia&ft:locale=en-US)**

Monitor call events from ICC enabled agent sessions for the customer, in **Usage Insights** available under **Platform Analytics**. View, filter, and inspect event payloads for actions such as muting, recording, and coaching session initiation. To enable tracking, turn on the Analytics toggle in the agent's profile preferences and add the agent's **sys\_id** to the **sn\_openframe.logger.enabled.users** system property.

-   **[Amazon Connect SSO integration with ServiceNow](https://www.servicenow.com/docs/access?context=amazon-connect-sso-integration-with-servicenow&family=australia&ft:locale=en-US)**

Configure Single Sign-On \(SSO\) between ServiceNow and Amazon Connect by adding the identity provider SSO URL to the Amazon Connect instance configuration. When a Security Assertion Markup Language \(SAML\) compatible identity provider is configured, agents signed in to ServiceNow can access Amazon Connect in the Contact Control Panel \(CCP\). Separate credentials are not required.

-   **[Call Wrap-Up](https://www.servicenow.com/docs/access?context=initiate-agent-wrap-up-during-active-call&family=australia&ft:locale=en-US)**

Initiate the wrap-up process before a call ends using the **Open Wrap-Up** button in the ICC enabled Active Call window. Agents can enter wrap-up codes and notes in real-time, and minimize or expand the wrap-up modal as needed to maintain context during the call. Enable this feature for your CCaaS integration.

-   **[Implement the overflow menu for active calls](https://www.servicenow.com/docs/access?context=implement-overflow-menu-icc&family=australia&ft:locale=en-US)**

Access primary call controls, such as Recording, Hold, Mute, Transfer, and Help Request, directly on the active call interface. When controls exceed five or the available display width, additional CCaaS-defined actions are available through an overflow menu.


 -   **[Web Embeddables](https://www.servicenow.com/docs/access?context=using-web-embeddables&family=australia&ft:locale=en-US)**

Embed ServiceNow components into any third-party website or web application to extend the ServiceNow AI Platform capabilities. You can use a library of default configurable components or create custom components.

You can configure and embed the following ServiceNow components on the third-party websites:

    -   Case list: Displays a comprehensive list of cases along with their key details.
    -   Case view: Shows a detailed view of case and case-related activities. You can display relevant playbooks when created for the case record.
    -   Case create: Displays a form to create a case to address issues related to products and services.
    -   Catalog item: Request Service Catalog items or services.
    -   Knowledge article view: Displays knowledge articles along with key details like title, content, author, view count, read time, and more. You can also rate the article and switch the display language.
    -   Data visualization: Shows a graphical representation of information from any ServiceNow AI Platform table using visual elements such as single score, pie, donut, and semi donut charts.
    -   Playbook intake: Enable your users to submit cases using the Playbook guided experience. Systematically capture case details and display stages, and activities involved in resolving the case.
    -   Catalog browse: Browse and search Service Catalog items from different catalogs and categories within a third-party website.
    -   Object list: Display records from different tables with their related actions in a list format.
-   **[Amazon Connect for voice calls via ICC](https://www.servicenow.com/docs/access?context=amazon-connect-for-voice-calls&family=australia&ft:locale=en-US)**

Manage Amazon Connect calls in the CRM Workspace voice Interaction record. The integration supports inbound and outbound call flows, presence management, and transfers without switching applications.

-   **[Supervisor call monitoring](https://www.servicenow.com/docs/access?context=supervisor-monitoring-for-voice&family=australia&ft:locale=en-US)**

Monitor, coach, and join agent calls from the CRM Workspace without having to switch to the CCaaS desktop. All supervisor actions are automatically logged for auditing and reporting purpose.

-   **[Agent help request for voice calls](https://www.servicenow.com/docs/access?context=agent-help-request-for-voice-calls&family=australia&ft:locale=en-US)**

Agents can request supervisor assistance during active calls using the **Help Request** button, specify a reason to give supervisors context before they respond, and receive notifications when supervisors coach or join. All help request data is captured for reporting to support data-driven coaching. Additional agent workflow enhancements include:

    -   Configure the phone directory to show or hide the Agents, Queues, or External tabs based on CCaaS provider settings, preventing transfers to unsupported numbers.
    -   During active calls, agents can view real-time availability status for other agents in the transfer list and phone directory, supporting more informed transfer decisions.
-   **[Use AI to generate wrap up code and notes summary](https://www.servicenow.com/docs/access?context=ai-generated-wrap-up-codes-and-notes-summary&family=australia&ft:locale=en-US)**

Automatically suggest a wrap-up code and generate an interaction summary based on conversation transcripts by using Now Assist, which reduces manual documentation time and contributes to consistent record-keeping. Choose automatic or agent-initiated generation to fit your workflow.

-   **[Use Consumer Portal](https://www.servicenow.com/docs/access?context=use-consumer-portal&family=australia&ft:locale=en-US)**

Support your consumers through the Consumer Portal self-service capabilities such as knowledge articles, service catalogs, case management, Virtual Agent, and others. These capabilities help reduce maintenance effort through low-code configurations on pages with configurable widgets.

-   **[Native callback features](https://www.servicenow.com/docs/access?context=contact-center-intergration-with-icc-callback&family=australia&ft:locale=en-US)**

Callback management enables agents to schedule callbacks on behalf of customers. The key features include:

    -   Enable agents to schedule callbacks from any interaction or case.
    -   Equip agents to reschedule or cancel callbacks from the callback record page with proper state tracking.
    -   Facilitate agents to view scheduled callbacks in the list view so they can open the individual callback record page.
    -   Enable agents to view and manage scheduled callbacks for the current interaction or case in the contextual side panel.
-   **[Email interaction feature: Wrap up of email interactions](https://www.servicenow.com/docs/access?context=using-email-interaction-page&family=australia&ft:locale=en-US)**

Note the following capabilities introduced for wrapping up email interactions:

    -   Introduction of wrap‑up modal for Advanced Work Assignment \(AWA\) and CCaaS‑routed email interactions with internal wrap‑up codes configurable by admins.
    -   Automatic closure of inactive interactions with system-assigned wrap-up codes in multiple scenarios:
        -   When agents create a case from an email interaction.
        -   When the wrap-up modal times out without agent submission.
        -   When customers don’t respond within the defined follow-up period.
-   **[Email interaction feature: Outbound Interaction from agent-initiated email](https://www.servicenow.com/docs/access?context=using-email-interaction-page&family=australia&ft:locale=en-US)**

The new capabilities for outbound interactions initiated by agents through email are:

    -   Initiate outbound email interactions from contact or consumer records by selecting email addresses or using the Compose Email UI option. This opens a modeless email composer with the recipient's email address auto-populated.
    -   Automatic creation of Work‑In‑Progress \(WIP\) outbound email interactions when agents initiate an email to a customer.
    -   Preserve email drafts when agents navigate away. The system automatically closes interactions that show no sent or received email activity and contain only unsent drafts within a rolling 30‑day period. Any agent activity on the draft resets the 30‑day window.
    -   Consolidate multiple agent‑initiated drafts into a single, unified interaction within service workflows, with ownership assigned to the sending agent. You can optionally configure the system to create separate interactions for each draft for the same contact.
    -   Configurable reminder windows for sending automated reminder emails when customers don’t respond.
    -   Customer response notifications on the ongoing tab and interaction linking in contact or consumer related lists for seamless conversation tracking.
-   **[Email interaction feature: Transfer Email Interactions](https://www.servicenow.com/docs/access?context=using-email-interaction-page&family=australia&ft:locale=en-US)**

Transfer CCaaS or AWA-routed email interactions to another queue or agent. When transferring to a queue, corresponding routing rules apply automatically. When transferring to a specific agent, the interaction is directly assigned.


</td></tr><tr><td>

Brazil

</td><td>

-   **[View work orders](https://www.servicenow.com/docs/access?context=workorders-consumerportal&family=brazil&ft:locale=en-US)**

View and track work orders directly in the Consumer Portal \(B2C\) using the new Work Orders page.

-   **[Voice call widget](https://www.servicenow.com/docs/access?context=portal-phone-widget&family=brazil&ft:locale=en-US)**

Customers can now make voice calls directly from portal pages or the Engagement Messenger. Call context stays intact as customers navigate between pages. These calls connect to AI Voice Agents to deliver conversational voice experiences without relying on contact center platforms.

-   **[Integrate ServiceNow Voice with Amazon Connect](https://www.servicenow.com/docs/access?context=integrate-ccc-amazonconnect&family=brazil&ft:locale=en-US)**

Use ServiceNow AI Voice Agents to build conversational voice experiences by routing calls from Amazon Connect, Five9, or NICE contact center channels to deliver natural, conversational customer interactions.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Self-service and omnichannel engagement for CSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Integrating WhatsApp with Customer Service Management using the WhatsApp Cloud API](https://www.servicenow.com/docs/access?context=messg-integrating-whatsapp-with-csm-whatsapp-cloud&family=australia&ft:locale=en-US)**

The conversation thread includes an inline audio player for received audio messages, with play, pause, and seek controls.


 -   **[Integrating WhatsApp with Customer Service Management using the WhatsApp Cloud API](https://www.servicenow.com/docs/access?context=messg-integrating-whatsapp-with-csm-whatsapp-cloud&family=australia&ft:locale=en-US)**

WhatsApp direct integration gives agents richer conversational tools and gives customers more ways to reach for support. The key updates include:

    -   Access synthesized responses generated from Now Assist Virtual Agent \(NAVA\) in WhatsApp direct conversations.
    -   Play audio messages directly in the agent chat interface.

 -   **[Call Wrap-Up](https://www.servicenow.com/docs/access?context=initiate-agent-wrap-up-during-active-call&family=australia&ft:locale=en-US)**

Manage wrap-up during active calls using new UI components in the Active Call window in the CRM Workspace:

    -   An **Open Wrap-Up** button to initiate the wrap-up process during an active call.
    -   **Minimize** and **Expand** controls on the wrap-up modal to manage screen space while remaining on the call.

 -   **[Walk-up Check-in](https://www.servicenow.com/docs/access?context=walkup-checkin-businessportal&family=australia&ft:locale=en-US)**

Initiate a walk-up check-in directly from the Business Portal home page without navigating away from the landing experience.

-   **[Portal Data List widget JSON parameters](https://www.servicenow.com/docs/access?context=portal-datalist-widget-data-json&family=australia&ft:locale=en-US)**

Generate dynamic record view URLs with the Data List widget. Portal admins can configure the target record context, parent table, child table, or reference table. The portal builds the URL with the relevant parameters to render the correct record view at runtime.

-   **[Portal Object widget instance options form](https://www.servicenow.com/docs/access?context=port-object-inst-options&family=australia&ft:locale=en-US)**

Adds a Dynamic portal object instance option to the Portal Object widget \(turned off by default\). When turned on, the widget reads the extended table, record ID, and view from URL parameters. The widget derives the card title, image field, summary view fields, and detail view from the view definition on the extended table. This eliminates the need for static configuration in the widget instance.


 -   **[ICC voice call features](https://www.servicenow.com/docs/access?context=interaction-controls-component-icc-call-interaction-features&family=australia&ft:locale=en-US)**

The following UI components are available in the Active Call window, enabled via ICC in the CRM Workspace:

    -   A **Help Request** button to seek supervisor assistance during an active call.
    -   A **Cancel Help Request** or **End Help Request** button to cancel and end a submitted help request at any time during the active call.
    -   An overflow menu icon \(ellipsis\) to access secondary call control buttons when the number of controls exceeds five or when the available display width is exceeded.
-   **[Using the interaction and case page for callback request](https://www.servicenow.com/docs/access?context=csm-config-ws-pages-templates&family=australia&ft:locale=en-US)**

The following UI components have been added on the interaction and case pages:

    -   A **Schedule callback** button on interaction and case pages to enable agents to schedule callbacks on behalf of customers.
    -   A **Reschedule** button on the callback task record page to enable agents to modify scheduled callback date and time on behalf of customers.
    -   A **Cancel** button on the callback record page to enable agents to cancel callbacks created on behalf of customers.
    -   A **Scheduled callbacks** tile in the contextual side panel to enable agents to view and manage upcoming callbacks while working on interactions or cases.
Scheduled callbacks list view: A **Scheduled callbacks** list view has been added in Agent Workspace to enable agents to view all scheduled callbacks and open any callback to access its task record management.

-   **[Using the email interaction page](https://www.servicenow.com/docs/access?context=using-email-interaction-page&family=australia&ft:locale=en-US)**

The following UI components have been added on the Email Interaction page:

    -   A **Compose Email** UI option to contact and consumer records for initiating outbound email interactions from these records.
    -   Clickable email addresses to contact and consumer records to open the email composer with the recipient address automatically inserted.
    -   A **Transfer Email** option with list of available agents and queues has been added for AWA or CCaaS‑routed email interactions. Agents can transfer the interaction to the selected queues or agents.
    -   A unified wrap‑up dialog has been added to provide a single closure experience for email interactions routed through AWA or CCaaS.
    -   A **Summarize** button on the email interaction page to trigger an AI summary of the full conversation.
    -   A Refresh Summary icon on the summary card to manually re-trigger summarization at any point.
    -   Feedback icons and copy icon on the summary card to indicate whether the summary is helpful and to copy the summary text.

 -   **[Customer Service Portal Base](https://www.servicenow.com/docs/access?context=configure-csm-service-portals&family=australia&ft:locale=en-US)**

Starting with the Australia release, the Customer Service Portal Base plugin \(com.snc.csm\_portal\_base\) has been migrated to the App Store as a standalone application. Future enhancements are delivered through the Customer Service Portal Base store app. This change improves packaging, versioning, and deployment flexibility for implementations that require portal framework, responsive design, case management, knowledge integration, and community features. The store app also includes email integration, translation support, attachment handling, and mobile enhancements.

-   **[Subscriptions and Activity Feed Framework](https://www.servicenow.com/docs/access?context=actsub-api&family=australia&ft:locale=en-US)**

Starting with the Australia release, the Subscriptions and Activity Feed Framework plugin \(com.snc.subscriptions\_activity\_feed\) has been migrated to the App Store as a standalone application. Future enhancements are delivered through the Subscriptions and Activity Feed Framework store app. This change improves packaging, versioning, and deployment flexibility for implementations that require subscription framework, activity tracking, notification preferences, or context management.

-   **[Walk-Up for CSM](https://www.servicenow.com/docs/access?context=csm-walkup-experience&family=australia&ft:locale=en-US)**

Starting with the Australia release, the Walk-up for CSM plugin \(com.snc.walkup\_for\_csm\) has been migrated to the App Store as a standalone application. Future enhancements are delivered through the Walk-up for CSM store app. This change improves packaging, versioning, and deployment flexibility for implementations that require subscription framework, activity tracking, notification preferences, or context management.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Usage calculation of self-service experiences](https://www.servicenow.com/docs/access?context=csm-portal-user-sessions-timeouts_2&family=brazil&ft:locale=en-US)**

Get more accurate portal usage data with an updated analytics definition that eliminates double-counting of guest user sessions.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Self-service and omnichannel engagement for CSM features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Self-service and omnichannel engagement for CSM features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Communities**

Communities is no longer deployed, enhanced, or supported. The Communities plugins are set to planned deprecation status, which prevents new customer installations. Existing customers who have Communities installed can continue to use it, but new activations are no longer available. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate Self-service and omnichannel engagement for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Install self-service and omnichannel applications, such as OpenFrame and Interaction Controls Component \(ICC\), by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

Check your entitlements to determine whether you have access to AI email summarization and AI-based context matching for multi-case linking. For details, see [Activate email interaction summarization](https://www.servicenow.com/docs/access?context=activate-email-summarization-csm&family=australia&ft:locale=en-US) and [Activate contextual email matching](https://www.servicenow.com/docs/access?context=activate-contextual-email-matching-csm&family=australia&ft:locale=en-US).


**Important:** Self-service and omnichannel applications are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install self-service and omnichannel applications, such as OpenFrame and Interaction Controls Component \(ICC\), by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Self-service and omnichannel engagement for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Additional requirements**

Microphone permission is required for WebRTC calls on mobile devices.


</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Self-service and omnichannel engagement for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Browser requirements**

Starting with the Australia release, self-service and omnichannel application don't support Internet Explorer. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

-   **Browser requirements**

The WebRTC voice call widget is not supported on mobile browsers.


</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Self-service and omnichannel engagement for CSM, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Accessibility information**

CSM Engagement Messenger now supports reflow, allowing content to be zoomed up to 400% in a browser without loss of content or functionality. Page layouts automatically transform into a vertical, stacked view at 400% zoom. This update benefits users with low vision and those working across varied devices and environments.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Self-service and omnichannel engagement for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Self-service and omnichannel engagement for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   Set up SSO for the Amazon Connect CCaaS integration using a SAML-compatible identity provider. Agents can access the Contact Control Panel without separate credentials.
-   Enhance B2C consumer support through ServiceNow AI Platform self-service capabilities with the Consumer Portal.
-   Embed components into external websites to provide users with access to the self-service capabilities on the ServiceNow AI Platform.
-   Support agent efficiency by automatically linking email replies on closed interactions to open cases, generating AI summaries on demand, and enabling CCaaS or AWA-routed transfers.
-   Schedule, reschedule, and cancel native callbacks from Agent Workspace across all omnichannel interactions \(chat, voice, email, and messaging\) and cases without switching to external tools or applications.

 See [\[Placeholder link text to key bundle-csm.omnichannels-communicating-customers\]](https://www.servicenow.com/docs/access?context=omnichannels-communicating-customers&family=australia&ft:locale=en-US), [Self-service](https://www.servicenow.com/docs/access?context=self-service-options-csm-customers&family=australia&ft:locale=en-US), and [ICC for voice calls](https://www.servicenow.com/docs/access?context=contact-center-integration-with-icc&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Handle inbound calls intelligently by configuring AI Voice Agents with ServiceNow Voice and Amazon Connect.
-   Initiate WebRTC voice calls from portal pages or engagement messenger with a widget that maintains call state and context across page navigation.

 See [Self-service](https://www.servicenow.com/docs/access?context=self-service-options-csm-customers&family=brazil&ft:locale=en-US), and [Omnichannel](https://www.servicenow.com/docs/access?context=omnichannel&family=brazil&ft:locale=en-US) for more information.

**Note:** Self-service and omnichannel applications are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

