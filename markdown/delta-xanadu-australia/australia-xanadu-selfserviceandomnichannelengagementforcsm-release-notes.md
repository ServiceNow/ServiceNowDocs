---
title: Combined Self-service and omnichannel engagement for CSM release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Self-service and omnichannel engagement for CSM from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-selfserviceandomnichannelengagementforcsm-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 21
breadcrumb: [Products combined by family]
---

# Combined Self-service and omnichannel engagement for CSM release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Self-service and omnichannel engagement for CSM from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Self-service and omnichannel engagement for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Self-service and omnichannel engagement for CSM to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Self-service and omnichannel engagement for CSM.

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

-   **[Business Portal](https://www.servicenow.com/docs/access?context=configure-business-portal&family=yokohama&ft:locale=en-US)**

Support your customers through the Business Portal self-service capabilities, such as knowledge articles, service catalogs, case management, Virtual Agent, and others. Help reduce maintenance effort through low-code configurations on pages with configurable widgets.

-   **[Email as an Interaction](https://www.servicenow.com/docs/access?context=email-channel&family=yokohama&ft:locale=en-US)**

Enhance case management with the Email as an Interaction feature.

    -   Transform emails into interactions, enabling customer communication to be tracked in a central location and help avoid unnecessary case creation.
    -   Manage straightforward customer inquiries via email, create cases for more complex issues, or link emails to existing cases.
    -   Notify agents on email responses received from customers.
-   **[Contact Center Integration Core](https://www.servicenow.com/docs/access?context=contactcenter-integration&family=yokohama&ft:locale=en-US)**

As an admin, import data automatically from a third-party contact center as a service \(CCaaS\) application to facilitate external routing and third-party telephony integration in their ServiceNow® instance.

**Note:** The Contact Center Integration Core is a framework that includes voice call features, which doesn't work unless CCaaS implements it.

    -   Import records such as queues, skills, and wrap-up codes from a third party into your ServiceNow instance.
    -   Maintain data consistency between your ServiceNow instance and third-party systems. Verify that chats and cases are routed to the correct agent and that the correct wrap-up codes are available when dispositioning an interaction.
-   **[Interaction Controls Component \(ICC\)](https://www.servicenow.com/docs/access?context=contact-center-integration-with-icc&family=yokohama&ft:locale=en-US)**

As an agent, manage calls, such as muting, holding, and transferring, directly within the Configurable Workspace. As a part of the new Voice interaction page experience, the ICC framework helps improve workflow efficiency and promotes a consistent agent experience across all channels.

**Note:** ICC must be integrated with your specific Contact Center as a Service \(CCaaS\) plugin to establish the telephony connection.

Connect customers with field agents or third-party support teams in the embedded call interface. Choose between the following transfer options:

    -   Consult transfer: Share the call context with the external contact before transferring the customer.
    -   Blind transfer: Immediately transfer the call to the external contact.
-   **[OpenFrame Integration to Interaction Controls Component \(ICC\)](https://www.servicenow.com/docs/access?context=interaction-controls-component&family=yokohama&ft:locale=en-US)**

ICC is a new component for a native call controls interface embedded in Agent Workspace. With the ICC component, you can do the following:

    -   Create the state context in OpenFrame to read the state of idle and active call state, and the state of the transfer.
    -   Provide iframe sandbox parameters to allow iframe access to security features and to enable additional iframe restrictions.
    -   Create an extension point implementation to create and get phone log segments.
-   **[Integrating Conversational SMS with AWS End User Messaging](https://www.servicenow.com/docs/access?context=conversational-sms-integration-amazon&family=yokohama&ft:locale=en-US)**

Integrate the ServiceNow SMS channel with AWS end-user messaging to engage in conversations with Now Virtual Agent and live agents to address and resolve any customer queries or issues.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Amazon Connect for voice calls via ICC](https://www.servicenow.com/docs/access?context=amazon-connect-for-voice-calls&family=zurich&ft:locale=en-US)**

Manage Amazon Connect calls directly in the CSM Configurable Workspace voice Interaction record page. This integration supports inbound and outbound call flows, presence management, and call transfers without switching applications.

-   **[Selecting queues for outbound calls](https://www.servicenow.com/docs/access?context=select-queues-for-outbound-calls&family=zurich&ft:locale=en-US)**

Enable agents to designate a specific queue for their outbound calls directly from the keypad or the phone directory in the Global Call window to improve routing and reporting. This provides a streamlined search interface that enables agents to find and select a single queue that can be applied across all outbound dialing methods.

-   **[Integrating WhatsApp with Customer Service Management using the WhatsApp Cloud API](https://www.servicenow.com/docs/access?context=messg-integrating-whatsapp-with-csm-whatsapp-cloud&family=zurich&ft:locale=en-US)**

Connect directly to WhatsApp Cloud API for more reliable, feature-rich customer support without third-party dependencies. The key capabilities include the following:

    -   Send and receive text messages for direct customer communication.
    -   Exchange images, videos, audio files, and documents for clearer, more contextual conversations.
    -   Simplify customer input with list pickers and location sharing.
    -   View typing indicators for more natural conversational flow.
    -   Automatically capture and record customer opt-in and opt-out messages to ensure compliance with WhatsApp's messaging policies.
-   **[Defining CCaaS callbacks](https://www.servicenow.com/docs/access?context=interaction-controls-component-icc-callback-integration-features&family=zurich&ft:locale=en-US)**
    -   Offer callers a callback option that lets them retain their position in the queue and receive a call when an agent is available. Alternatively, callers can choose a specific date and time for the callback, also known as scheduled callback.
    -   As an agent, view callback requests in the order that they're received.
-   **[CCaaS callback features](https://www.servicenow.com/docs/access?context=contact-center-intergration-with-icc-callback&family=zurich&ft:locale=en-US)**

As an agent, address callback requests from the CSM Configurable Workspace. Initiate callbacks and manage active calls with the Callback context card and Callback Actions component on the voice interaction page.

On the Callback actions component, you can use the **Call number** option to initiate a call; alternatively, the call can be initiated automatically at the end of the preview timer when enabled. After the call has ended, the **Close callback** option closes the callback interaction and changes the status to Closed complete. Agents can also retry the callback as needed.

Monitor the callback life cycle and capture the preview time that measures the time between when an agent accepts the callback request and the agent dials out the customer.

-   **[Global call list](https://www.servicenow.com/docs/access?context=ccaas-global-call-list&family=zurich&ft:locale=en-US)**

Switch between workspaces using the global call list. As a CSM agent, you can accept calls and open interaction records in supported, unsupported, or default workspaces.

-   **[Phone directory](https://www.servicenow.com/docs/access?context=ccaas-phone-directory&family=zurich&ft:locale=en-US)**

Access the embedded phone directory in your CSM Configurable Workspace via Interaction Controls Component \(ICC\) to make outbound calls to external and internal contacts.

-   **[Call resiliency](https://www.servicenow.com/docs/access?context=ccaas-call-resiliency&family=zurich&ft:locale=en-US)**

Route phone calls to the CSM Configurable Workspace without creating an interaction record, helping agents handle calls even during connectivity issues.

-   **[Voice Controls Simulator tool](https://www.servicenow.com/docs/access?context=voice-control-simulator-tool&family=zurich&ft:locale=en-US)**

Test and validate voice call UI flows in the CSM Configurable Workspace to ensure CCaaS partners have clear insights into their supported voice control capabilities.

-   **[Monitoring calls](https://www.servicenow.com/docs/access?context=call-monitoring&family=zurich&ft:locale=en-US)**

Enable supervisors to monitor, coach, and barge-in on calls in real time by integrating ServiceNow's native voice call feature within an active call interface.


</td></tr><tr><td>

Australia

</td><td>

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

Manage Amazon Connect calls in the CSM Configurable Workspace voice Interaction record. The integration supports inbound and outbound call flows, presence management, and transfers without switching applications.

-   **[Supervisor call monitoring](https://www.servicenow.com/docs/access?context=supervisor-monitoring-for-voice&family=australia&ft:locale=en-US)**

Monitor, coach, and join agent calls from the CSM Configurable Workspace without having to switch to the CCaaS desktop. All supervisor actions are automatically logged for auditing and reporting purpose.

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

    -   Initiate outbound email interactions from contact or consumer records by selecting email addresses or using the Compose Email UI option, opening a modeless email composer with the recipient's email address auto-populated.
    -   Automatic creation of Work‑In‑Progress \(WIP\) outbound email interactions when agents initiate an email to a customer.
    -   Preserve email drafts when agents navigate away, and automatically close interactions that show no sent or received email activity and contain only unsent drafts within a rolling 30‑day period. Any agent activity on the draft resets the 30‑day window.
    -   Consolidate multiple agent‑initiated drafts into a single, unified interaction within service workflows, with ownership assigned to the sending agent. You can optionally configure the system to create separate interactions for each draft for the same contact.
    -   Configurable reminder windows for sending automated reminder emails when customers don’t respond.
    -   Customer response notifications on the ongoing tab and interaction linking in contact or consumer related lists for seamless conversation tracking.
-   **[Email interaction feature: Transfer Email Interactions](https://www.servicenow.com/docs/access?context=using-email-interaction-page&family=australia&ft:locale=en-US)**

Transfer CCaaS or AWA-routed email interactions to another queue or agent. When transferring to a queue, corresponding routing rules apply automatically. When transferring to a specific agent, the interaction is directly assigned.

-   **[Email interaction feature: Email reply routing and summarization](https://www.servicenow.com/docs/access?context=using-email-interaction-page&family=australia&ft:locale=en-US)**

The new capabilities for smart email routing and summarization are:

    -   Receive customer email replies on the correct open case or interaction automatically, with ServiceNow Otto® selecting the best-matching case when multiple open cases exist.
    -   Get AI summaries automatically on transfer and on demand, reducing the need to read the full email thread.
    -   See summaries instantly on page refresh without re-running AI, and refresh with one click when new activity arrives on the interaction.
**Note:** Check your entitlements to determine whether you have access to summarization and AI-based context matching.

-   **[Usage insights for call events enabled using Interaction Controls Component \(ICC\)](https://www.servicenow.com/docs/access?context=usage-insight-for-icc-enabled-call-events&family=australia&ft:locale=en-US)**

Monitor call events from ICC enabled agent sessions for the customer, in **Usage Insights** available under **Platform Analytics**. View, filter, and inspect event payloads for actions such as muting, recording, and coaching session initiation. To enable tracking, turn on the Analytics toggle in the agent's profile preferences and add the agent's **sys\_id** to the **sn\_openframe.logger.enabled.users** system property.

-   **[Amazon Connect SSO integration with ServiceNow](https://www.servicenow.com/docs/access?context=amazon-connect-sso-integration-with-servicenow&family=australia&ft:locale=en-US)**

Configure Single Sign-On \(SSO\) between ServiceNow and Amazon Connect by adding the identity provider SSO URL to the Amazon Connect instance configuration. When a Security Assertion Markup Language \(SAML\) compatible identity provider is configured, agents signed in to ServiceNow can access Amazon Connect in the Contact Control Panel \(CCP\) without separate credentials.

-   **[Call Wrap-Up](https://www.servicenow.com/docs/access?context=initiate-agent-wrap-up-during-active-call&family=australia&ft:locale=en-US)**

Initiate the wrap-up process before a call ends using the **Open Wrap-Up** button in the ICC enabled Active Call window. Agents can enter wrap-up codes and notes in real time, and minimize or expand the wrap-up modal as needed to maintain context during the call. Enable this feature for your CCaaS integration.

-   **[Implement the overflow menu for active calls](https://www.servicenow.com/docs/access?context=implement-overflow-menu-icc&family=australia&ft:locale=en-US)**

Access primary call controls, such as Recording, Hold, Mute, Transfer, and Help Request, directly on the active call interface. When controls exceed five or the available display width, additional CCaaS-defined actions are available through an overflow menu.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Self-service and omnichannel engagement for CSM features.

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

-   **[Using the email interaction page](https://www.servicenow.com/docs/access?context=using-email-interaction-page&family=yokohama&ft:locale=en-US)**

Manage and view customer-related information and past conversations while interacting with customers via email.

-   **[Using the Now Assist in Virtual Agent enhanced chat in self-service portals](https://www.servicenow.com/docs/access?context=nass-portal&family=yokohama&ft:locale=en-US)**

Receive comprehensive and detailed answers with intelligent search and conversational experiences using Now Assist in Virtual Agent. The search results are synthesized from Knowledge Base articles, Virtual Agent articles, and catalog items with links to the sources. The agent retains conversation context across multi-turn questions, promoting continuity and relevance in responses.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Using the email interaction page](https://www.servicenow.com/docs/access?context=using-email-interaction-page&family=zurich&ft:locale=en-US)**

View annotations for the most recent activity along with a compact email header that includes the subject, sender, and receiver details in the activity stream. Focus on new or unread email messages rather than the entire email conversation.

View or edit the interaction record while drafting an email in a modeless dialog, keeping all relevant information accessible.

-   **[Using Agent Chat](https://www.servicenow.com/docs/access?context=ci-agent-chat-using&family=zurich&ft:locale=en-US)**

Leave a chat without ending it for other agents, enabling you to complete your task and exit the chat.

Confirm before closing a chat tab to avoid unintentionally leaving the chat.

Enable multiple agents to add wrap-up codes and comments for a single chat.

-   **[Import queues](https://www.servicenow.com/docs/access?context=import-queues&family=zurich&ft:locale=en-US)**

Review and update queues imported from a contact center in a post-import page. The post-import page for a queue mirrors the existing post-import pages for skills and wrap-up codes, providing a consistent user experience.

-   **[ICC call control features](https://www.servicenow.com/docs/access?context=interaction-controls-component-icc-call-interaction-features&family=zurich&ft:locale=en-US)**

Notify agents when a supervisor is coaching or has joined an active call while monitoring agents directly through the CCaaS system.

-   **[CCaaS callback features](https://www.servicenow.com/docs/access?context=contact-center-intergration-with-icc-callback&family=zurich&ft:locale=en-US)**

Callback management has been improved to make handling requests easier for agents. The key changes include:

    -   Equip agents to transfer the callback requests before dialing the call, enhancing flexibility in managing customer interactions.
    -   Enable scheduled callbacks, which help customers to choose a preferred callback time in addition to the existing ASAP option.
    -   Facilitate agents to view the list of queues and other agents for easier callback transfers and efficient customer management.
    -   Capture callback reasons more effectively with the expanded Reason for Call field, which includes additional choice values.
-   **[Unified routing of email interactions via CCaaS](https://www.servicenow.com/docs/access?context=using-email-interaction-customer-service-management&family=zurich&ft:locale=en-US)**

Email interaction handling has been enhanced to improve efficiency and responsiveness in managing customer communications. The key changes include:

    -   Support external routing of email interactions.
    -   Enable agents to put email interactions on hold while waiting for customer responses.
    -   Notify CCaaS when an interaction is put on hold so that CCaaS can free up the agent's capacity for handling other interactions.
    -   Send automatic email reminders to customers for interactions that are on hold for a configurable period.
    -   Reroute email interactions to available agents when the originally assigned agent is unavailable.
    -   Prevent creating outbound email interactions when emails are sent on top of cases.
-   **[Import queues](https://www.servicenow.com/docs/access?context=import-queues&family=zurich&ft:locale=en-US)**

Use bulk action to assign service channels to multiple queues simultaneously during queue-import, simplifying queue management for CCaaS integrations.

-   **[Portal Data List widget](https://www.servicenow.com/docs/access?context=portal-data-list-widget&family=zurich&ft:locale=en-US)**

The Data List widget now offers more configuration flexibility and supports dynamic, context‑aware view selection. Key enhancements include:

    -   Role‑Based and Guest Views: Use the new role\_based\_views and guest\_view options to define different views for different user roles and for unauthenticated users removing the dependency on a single static view.
    -   Automatic URL Parameter Passing: Pass URL parameters automatically into scripts invoked from Data List instance options enabling admins to build richer, multi‑parameter conditions without extra setup.
    -   Script‑Based View Selection: Use the Data List Condition Script option to choose a view dynamically. Scripts can evaluate URL parameters and other context to determine the most appropriate view at runtime.
    -   Configurable Default Sorting: Define initial sorting behavior using the new sort\_by and sort\_order options letting the users see a meaningful default order when the list loads.

</td></tr><tr><td>

Australia

</td><td>

-   **[Customer Service Portal Base](https://www.servicenow.com/docs/access?context=configure-csm-service-portals&family=australia&ft:locale=en-US)**

Starting with the Australia release, the Customer Service Portal Base plugin \(com.snc.csm\_portal\_base\) has been migrated to the App Store as a standalone application. Future enhancements are delivered through the Customer Service Portal Base store app. This change improves packaging, versioning, and deployment flexibility for implementations that require portal framework, responsive design, case management, knowledge integration, and community features. The store app also includes email integration, translation support, attachment handling, and mobile enhancements.

-   **[Subscriptions and Activity Feed Framework](https://www.servicenow.com/docs/access?context=actsub-api&family=australia&ft:locale=en-US)**

Starting with the Australia release, the Subscriptions and Activity Feed Framework plugin \(com.snc.subscriptions\_activity\_feed\) has been migrated to the App Store as a standalone application. Future enhancements are delivered through the Subscriptions and Activity Feed Framework store app. This change improves packaging, versioning, and deployment flexibility for implementations that require subscription framework, activity tracking, notification preferences, or context management.

-   **[Walk-Up for CSM](https://www.servicenow.com/docs/access?context=csm-walkup-experience&family=australia&ft:locale=en-US)**

Starting with the Australia release, the Walk-up for CSM plugin \(com.snc.walkup\_for\_csm\) has been migrated to the App Store as a standalone application. Future enhancements are delivered through the Walk-up for CSM store app. This change improves packaging, versioning, and deployment flexibility for implementations that require subscription framework, activity tracking, notification preferences, or context management.

-   **[\[Placeholder link text to key walkup-checkin-businessportal\]](https://www.servicenow.com/docs/access?context=walkup-checkin-businessportal&family=australia&ft:locale=en-US)**

Initiate a walk-up check-in directly from the Business Portal home page without navigating away from the landing experience.

-   **[\[Placeholder link text to key portal-datalist-widget-data-json\]](https://www.servicenow.com/docs/access?context=portal-datalist-widget-data-json&family=australia&ft:locale=en-US)**

Generate dynamic record view URLs with the Data List widget. Portal admins can configure the target record context, parent table, child table, or reference table and the portal builds the URL with the relevant parameters to render the correct record view at runtime.

-   **[\[Placeholder link text to key port-object-inst-options\]](https://www.servicenow.com/docs/access?context=port-object-inst-options&family=australia&ft:locale=en-US)**

Adds a Dynamic portal object instance option to the Portal Object widget \(turned off by default\). When turned on, the widget reads the extended table, record ID, and view from URL parameters and derives the card title, image field, summary view fields, and detail view from the view definition on the extended table without requiring static configuration in the widget instance.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Self-service and omnichannel engagement for CSM features or functionality were removed.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Self-service and omnichannel engagement for CSM features or functionality were deprecated.

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

</td></tr><tr><td>

Zurich

</td><td>

Starting with the Zurich release, Customer Service CTI Demo Data Plugin and CTI Softphone Plugin are no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base, [Components installed with Customer Service CTI Demo Data](https://www.servicenow.com/docs/access?context=r_InstalledWithCustServCTIDemoData&family=zurich&ft:locale=en-US), and [Components installed with CTI Softphone](https://www.servicenow.com/docs/access?context=r_InstalledWithCCTISoftphone&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Self-service and omnichannel engagement for CSM.

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

Install the Engagement Messenger, Playbook for Portals, and Omnichannel applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install self-service and omnichannel applications, such as OpenFrame and Interaction Controls Component \(ICC\), by requesting them from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install self-service and omnichannel applications, such as OpenFrame and Interaction Controls Component \(ICC\), by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

 Check your entitlements to determine whether you have access to AI email summarization and AI-based context matching for multi-case linking. For details, see [Activate email interaction summarization](https://www.servicenow.com/docs/access?context=activate-email-summarization-csm&family=australia&ft:locale=en-US) and [Activate contextual email matching](https://www.servicenow.com/docs/access?context=activate-contextual-email-matching-csm&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Self-service and omnichannel engagement for CSM we have noted them here.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Self-service and omnichannel engagement for CSM we have noted them here.

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

Internet Explorer isn't supported.

</td></tr><tr><td>

Zurich

</td><td>

Internet Explorer isn't supported. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Starting with the Australia release, self-service and omnichannel application don't support Internet Explorer. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Self-service and omnichannel engagement for CSM, such as specific requirements or compliance levels.

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

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

</td><td>

CSM Engagement Messenger now supports reflow, allowing content to be zoomed up to 400% in a browser without loss of content or functionality. Page layouts automatically transform into a vertical, stacked view at 400% zoom. This update benefits users with low vision and those working across varied devices and environments.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Self-service and omnichannel engagement for CSM we have noted them here.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   Integrate with contact centers using Contact Center Integration Core to import data from a third party contact center as a service \(CCaaS\) application.
-   Better integrate with contact centers by adding call controls to Agent Workspace with Interaction Controls Component \(ICC\).
-   Enhance B2B customer support through ServiceNow® self-service capabilities with the new Business Portal.
-   Provide a consistent experience for agents handling omnichannel interactions through email interactions, which preserve the context for agents by associating the email conversation between the agent and the customer.
-   Improve contact center efficiency by helping avoid the creation of duplicate cases through the use of the Email as an Interaction feature.

 See [Omnichannels for communicating with customers](https://www.servicenow.com/docs/access?context=omnichannels-communicating-customers&family=yokohama&ft:locale=en-US), [Self-service for Customer Service Management](https://www.servicenow.com/docs/access?context=self-service-options-csm-customers&family=yokohama&ft:locale=en-US), and [Playbooks for Portals](https://www.servicenow.com/docs/access?context=playbooks-for-portals&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Integrate Amazon Connect with Interaction Controls Component \(ICC\) voice call features to allow agents manage phone interactions directly within their Workspace.
-   Allows agents to select a queue when making outbound calls to improve routing, reporting, and compliance.
-   Integrate WhatsApp Cloud API with CSM to enable rich media messaging, interactive controls, Virtual Agent automation, and Agent Workspace support without third-party dependencies.
-   Enable external routing of email interactions to reduce administrative effort.
-   Improve agent callback transfers for smoother handovers and support customers to request scheduled callbacks.

 See [Omnichannels for communicating with customers](https://www.servicenow.com/docs/access?context=omnichannels-communicating-customers&family=zurich&ft:locale=en-US) and [ICC for voice calls](https://www.servicenow.com/docs/access?context=contact-center-integration-with-icc&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Set up SSO for the Amazon Connect CCaaS integration using a SAML-compatible identity provider. Agents can access the Contact Control Panel without separate credentials.
-   Enhance B2C consumer support through ServiceNow AI Platform self-service capabilities with the Consumer Portal.
-   Embed components into external websites to provide users with access to the self-service capabilities on the ServiceNow AI Platform.
-   Support agent efficiency by automatically linking email replies on closed interactions to open cases, generating AI summaries on demand, and enabling CCaaS or AWA-routed transfers.
-   Schedule, reschedule, and cancel native callbacks from Agent Workspace across all omnichannel interactions \(chat, voice, email, and messaging\) and cases without switching to external tools or applications.

 See [\[Placeholder link text to key bundle-csm.omnichannels-communicating-customers\]](https://www.servicenow.com/docs/access?context=omnichannels-communicating-customers&family=australia&ft:locale=en-US), [Self-service](https://www.servicenow.com/docs/access?context=self-service-options-csm-customers&family=australia&ft:locale=en-US), and [ICC for voice calls](https://www.servicenow.com/docs/access?context=contact-center-integration-with-icc&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

