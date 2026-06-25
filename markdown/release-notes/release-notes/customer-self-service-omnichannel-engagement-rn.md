---
title: Self-service and omnichannel engagement for CSM release notes
description: With self-service and omnichannel applications in the ServiceNow Customer Service Management \(CSM\) application, your customers can use chat on self-service portals, consumer messaging apps, email, or phone calls to connect with your organization. Self-service and omnichannel applications for CSM were enhanced and updated in the Australia.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 14
---

# Self-service and omnichannel engagement for CSM release notes

With self-service and omnichannel applications in the ServiceNow® Customer Service Management \(CSM\) application, your customers can use chat on self-service portals, consumer messaging apps, email, or phone calls to connect with your organization. Self-service and omnichannel applications for CSM were enhanced and updated in the Australia.

## Self-service and omnichannel applications for CSM highlights for the Australia release

-   Set up SSO for the Amazon Connect CCaaS integration using a SAML-compatible identity provider. Agents can access the Contact Control Panel without separate credentials.
-   Enhance B2C consumer support through ServiceNow AI Platform self-service capabilities with the Consumer Portal.
-   Embed components into external websites to provide users with access to the self-service capabilities on the ServiceNow AI Platform.
-   Support agent efficiency by automatically linking email replies on closed interactions to open cases, generating AI summaries on demand, and enabling CCaaS or AWA-routed transfers.
-   Schedule, reschedule, and cancel native callbacks from Agent Workspace across all omnichannel interactions \(chat, voice, email, and messaging\) and cases without switching to external tools or applications.

See , [Self-service for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/self-service-options-csm-customers.md), and [Interaction Controls Component \(ICC\) for voice calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/contact-center-integration-with-icc.md) for more information.

**Important:** Self-service and omnichannel applications are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Configure Web Embeddables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/using-web-embeddables.md)**

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
-   **[Use Interaction Controls Component \(ICC\) call controls with Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/amazon-connect-for-voice-calls.md)**

    Manage Amazon Connect calls in the CSM Configurable Workspace voice Interaction record. The integration supports inbound and outbound call flows, presence management, and transfers without switching applications.

-   **[Supervisor call monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/supervisor-monitoring-for-voice.md)**

    Monitor, coach, and join agent calls from the CSM Configurable Workspace without having to switch to the CCaaS desktop. All supervisor actions are automatically logged for auditing and reporting purpose.

-   **[Agent help request for voice calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/agent-help-request-for-voice-calls.md)**

    Agents can request supervisor assistance during active calls using the **Help Request** button, specify a reason to give supervisors context before they respond, and receive notifications when supervisors coach or join. All help request data is captured for reporting to support data-driven coaching. Additional agent workflow enhancements include:

    -   Configure the phone directory to show or hide the Agents, Queues, or External tabs based on CCaaS provider settings, preventing transfers to unsupported numbers.
    -   During active calls, agents can view real-time availability status for other agents in the transfer list and phone directory, supporting more informed transfer decisions.
-   **[Use AI to generate wrap up code and notes summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ai-generated-wrap-up-codes-and-notes-summary.md)**

    Automatically suggest a wrap-up code and generate an interaction summary based on conversation transcripts by using Now Assist, which reduces manual documentation time and contributes to consistent record-keeping. Choose automatic or agent-initiated generation to fit your workflow.

-   **[Using the Consumer Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/use-consumer-portal.md)**

    Support your consumers through the Consumer Portal self-service capabilities such as knowledge articles, service catalogs, case management, Virtual Agent, and others. These capabilities help reduce maintenance effort through low-code configurations on pages with configurable widgets.

-   **[Native callback features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/contact-center-intergration-with-icc-callback.md)**

    Callback management enables agents to schedule callbacks on behalf of customers. The key features include:

    -   Enable agents to schedule callbacks from any interaction or case.
    -   Equip agents to reschedule or cancel callbacks from the callback record page with proper state tracking.
    -   Facilitate agents to view scheduled callbacks in the list view so they can open the individual callback record page.
    -   Enable agents to view and manage scheduled callbacks for the current interaction or case in the contextual side panel.
-   **[Email interaction feature: Wrap up of email interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/using-email-interaction-page.md)**

    Note the following capabilities introduced for wrapping up email interactions:

    -   Introduction of wrap‑up modal for Advanced Work Assignment \(AWA\) and CCaaS‑routed email interactions with internal wrap‑up codes configurable by admins.
    -   Automatic closure of inactive interactions with system-assigned wrap-up codes in multiple scenarios:
        -   When agents create a case from an email interaction.
        -   When the wrap-up modal times out without agent submission.
        -   When customers don’t respond within the defined follow-up period.
-   **[Email interaction feature: Outbound Interaction from agent-initiated email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/using-email-interaction-page.md)**

    The new capabilities for outbound interactions initiated by agents through email are:

    -   Initiate outbound email interactions from contact or consumer records by selecting email addresses or using the Compose Email UI option, opening a modeless email composer with the recipient's email address auto-populated.
    -   Automatic creation of Work‑In‑Progress \(WIP\) outbound email interactions when agents initiate an email to a customer.
    -   Preserve email drafts when agents navigate away, and automatically close interactions that show no sent or received email activity and contain only unsent drafts within a rolling 30‑day period. Any agent activity on the draft resets the 30‑day window.
    -   Consolidate multiple agent‑initiated drafts into a single, unified interaction within service workflows, with ownership assigned to the sending agent. You can optionally configure the system to create separate interactions for each draft for the same contact.
    -   Configurable reminder windows for sending automated reminder emails when customers don’t respond.
    -   Customer response notifications on the ongoing tab and interaction linking in contact or consumer related lists for seamless conversation tracking.
-   **[Email interaction feature: Transfer Email Interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/using-email-interaction-page.md)**

    Transfer CCaaS or AWA-routed email interactions to another queue or agent. When transferring to a queue, corresponding routing rules apply automatically. When transferring to a specific agent, the interaction is directly assigned.

-   **[Email interaction feature: Email reply routing and summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/using-email-interaction-page.md)**

    The new capabilities for smart email routing and summarization are:

    -   Receive customer email replies on the correct open case or interaction automatically, with ServiceNow Otto® selecting the best-matching case when multiple open cases exist.
    -   Get AI summaries automatically on transfer and on demand, reducing the need to read the full email thread.
    -   See summaries instantly on page refresh without re-running AI, and refresh with one click when new activity arrives on the interaction.
    **Note:** Check your entitlements to determine whether you have access to summarization and AI-based context matching.

-   **[Usage insights for call events enabled using Interaction Controls Component \(ICC\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/usage-insight-for-icc-enabled-call-events.md)**

    Monitor call events from ICC enabled agent sessions for the customer, in **Usage Insights** available under **Platform Analytics**. View, filter, and inspect event payloads for actions such as muting, recording, and coaching session initiation. To enable tracking, turn on the Analytics toggle in the agent's profile preferences and add the agent's **sys\_id** to the **sn\_openframe.logger.enabled.users** system property.

-   **[Amazon Connect SSO integration with ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/amazon-connect-sso-integration-with-servicenow.md)**

    Configure Single Sign-On \(SSO\) between ServiceNow and Amazon Connect by adding the identity provider SSO URL to the Amazon Connect instance configuration. When a Security Assertion Markup Language \(SAML\) compatible identity provider is configured, agents signed in to ServiceNow can access Amazon Connect in the Contact Control Panel \(CCP\) without separate credentials.

-   **[Call Wrap-Up](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/initiate-agent-wrap-up-during-active-call.md)**

    Initiate the wrap-up process before a call ends using the **Open Wrap-Up** button in the ICC enabled Active Call window. Agents can enter wrap-up codes and notes in real time, and minimize or expand the wrap-up modal as needed to maintain context during the call. Enable this feature for your CCaaS integration.

-   **[Implement the overflow menu for active calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/implement-overflow-menu-icc.md)**

    Access primary call controls, such as Recording, Hold, Mute, Transfer, and Help Request, directly on the active call interface. When controls exceed five or the available display width, additional CCaaS-defined actions are available through an overflow menu.


## UI changes

-   **[Interaction Controls Component \(ICC\) call features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/interaction-controls-component-icc-call-interaction-features.md)**

    The following UI components are available in the Active Call window, enabled via ICC in the CSM Configurable Workspace:

    -   A **Help Request** button to seek supervisor assistance during an active call.
    -   A **Cancel Help Request** or **End Help Request** button to cancel and end a submitted help request at any time during the active call.
    -   An overflow menu icon \(ellipsis\) to access secondary call control buttons when the number of controls exceeds five or when the available display width is exceeded.
-   **[Using the interaction and case page for callback request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-config-ws-pages-templates.md)**

    The following UI components have been added on the interaction and case pages:

    -   A **Schedule callback** button on interaction and case pages to enable agents to schedule callbacks on behalf of customers.
    -   A **Reschedule** button on the callback task record page to enable agents to modify scheduled callback date and time on behalf of customers.
    -   A **Cancel** button on the callback record page to enable agents to cancel callbacks created on behalf of customers.
    -   A **Scheduled callbacks** tile in the contextual side panel to enable agents to view and manage upcoming callbacks while working on interactions or cases.
    Scheduled callbacks list view: A **Scheduled callbacks** list view has been added in Agent Workspace to enable agents to view all scheduled callbacks and open any callback to access its task record management.

-   **[Using the email interaction page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/using-email-interaction-page.md)**

    The following UI components have been added on the Email Interaction page:

    -   A **Compose Email** UI option to contact and consumer records for initiating outbound email interactions from these records.
    -   Clickable email addresses to contact and consumer records to open the email composer with the recipient address automatically inserted.
    -   A **Transfer Email** option with list of available agents and queues has been added for AWA or CCaaS‑routed email interactions, enabling agents to transfer the interaction to the selected queues or agents.
    -   A unified wrap‑up dialog has been added to provide a single closure experience for email interactions routed through AWA or CCaaS.
    -   A **Summarize** button on the email interaction page to trigger an AI summary of the full conversation.
    -   A Refresh Summary icon on the summary card to manually re-trigger summarization at any point.
    -   Feedback icons and copy icon on the summary card to indicate whether the summary is helpful and to copy the summary text.
-   **[Call Wrap-Up](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/initiate-agent-wrap-up-during-active-call.md)**

    Manage wrap-up during active calls using new UI components in the Active Call window in the CSM Configurable Workspace:

    -   An **Open Wrap-Up** button to initiate the wrap-up process during an active call.
    -   **Minimize** and **Expand** controls on the wrap-up modal to manage screen space while remaining on the call.

## Changed in this release

-   **[Customer Service Portal Base](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-csm-service-portals.md)**

    Starting with the Australia release, the Customer Service Portal Base plugin \(com.snc.csm\_portal\_base\) has been migrated to the App Store as a standalone application. Future enhancements are delivered through the Customer Service Portal Base store app. This change improves packaging, versioning, and deployment flexibility for implementations that require portal framework, responsive design, case management, knowledge integration, and community features. The store app also includes email integration, translation support, attachment handling, and mobile enhancements.

-   **Subscriptions and Activity Feed Framework**

    Starting with the Australia release, the Subscriptions and Activity Feed Framework plugin \(com.snc.subscriptions\_activity\_feed\) has been migrated to the App Store as a standalone application. Future enhancements are delivered through the Subscriptions and Activity Feed Framework store app. This change improves packaging, versioning, and deployment flexibility for implementations that require subscription framework, activity tracking, notification preferences, or context management.

-   **[Walk-Up for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-walkup-experience.md)**

    Starting with the Australia release, the Walk-up for CSM plugin \(com.snc.walkup\_for\_csm\) has been migrated to the App Store as a standalone application. Future enhancements are delivered through the Walk-up for CSM store app. This change improves packaging, versioning, and deployment flexibility for implementations that require subscription framework, activity tracking, notification preferences, or context management.

-   ****

    Initiate a walk-up check-in directly from the Business Portal home page without navigating away from the landing experience.

-   ****

    Generate dynamic record view URLs with the Data List widget. Portal admins can configure the target record context, parent table, child table, or reference table and the portal builds the URL with the relevant parameters to render the correct record view at runtime.

-   ****

    Adds a Dynamic portal object instance option to the Portal Object widget \(turned off by default\). When turned on, the widget reads the extended table, record ID, and view from URL parameters and derives the card title, image field, summary view fields, and detail view from the view definition on the extended table without requiring static configuration in the widget instance.


## Activation information

Install self-service and omnichannel applications, such as OpenFrame and Interaction Controls Component \(ICC\), by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Check your entitlements to determine whether you have access to AI email summarization and AI-based context matching for multi-case linking. For details, see [Activate email interaction summarization for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-email-summarization-csm.md) and [Activate contextual email matching for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-contextual-email-matching-csm.md).

## Plugin information

-   **New plugins**

    The following plugins are new in the Australia release:

    -   Customer Service integration with Social Media Store \(sn\_cs\_social\_host\): The Customer Service integration with Social Media app enables agents to select Social as the communication channel and add a social profile to the Case form. Any communication with customers or consumers that takes place through social media is recorded on the Case form in the Social Logs related list. For more information, see [Social media communication channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/social-media-integration.md)
    -   Web Components for Customers \(sn\_cx\_components\): The plugin adds Case create and Case view Web Embeddables components to your ServiceNow instance. You can clone and configure them, and embed on your third-party website. For more information, see [Activate Web Embeddables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/act-web-embeddables.md).
    -   Web Embeddable Core \(sn\_embeddable\_core\): This plugin enables you to create, edit, clone, delete, and organize components into modules, groups, and instances. Each instance can be configured with a live preview. It also provides tools to manage CORS rules for secure integration. For more information, see [Activate Web Embeddables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/act-web-embeddables.md).
    -   Web Components for Guest \(sn\_guest\_component\): This plugin enables guest user access to Knowledge article view and Catalog item Web Embeddables components on third-party websites. It allows unauthenticated users to view public knowledge articles and submit catalog items without logging in. You can configure access controls to determine which content is publicly accessible. For more information, see [Activate Web Embeddables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/act-web-embeddables.md).
-   **Plugins planned for deprecation**

    These plugins are planned for deprecation in the C release. Beginning with the Australia release, these plugins will be migrated to store applications. Upgrade your instance to Australia release version and the store applications will be automatically installed:

    -   [Openframe Integration App](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_OpenFrameOverview.md) \(com.sn\_openframe\_integration\)
    -   [Skill Determination](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/quick-start-tests-csm.md) \(com.snc.skill\_determination\)
    -   [Advanced Work Assignment for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/awa-csm-overview.md) \(sn\_csm.awa\)
    -   [Social Media Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/social-media-integration.md) \(sn\_cs\_social\_host\)

## Browser requirements

Starting with the Australia release, self-service and omnichannel application don't support Internet Explorer. For more information, see [Browser support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/browser-support.md).

## Accessibility information

CSM Engagement Messenger now supports reflow, allowing content to be zoomed up to 400% in a browser without loss of content or functionality. Page layouts automatically transform into a vertical, stacked view at 400% zoom. This update benefits users with low vision and those working across varied devices and environments.

## Related ServiceNow applications and features

-   **[Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/fsm-application-landing-page.md)**

    The Field Service Management application helps you manage work orders and related tasks, resources, skills, assets, and locations. Assign work order tasks and dispatch agents to a customer location to perform field work.

-   **[Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management.md)**

    From the Customer Service Portal and Consumer Service Portal, enable your customers to search for shared information using the Knowledge Management application. Customer service agents can use knowledge content to help resolve cases.

-   **[IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md)**

    The following IT Service Management applications can integrate with Customer Service Management: [Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-integration-sm-incident.md), [Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-integration-sm-problem.md), [Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-integration-sm-change.md), and [Request Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-integration-sm-request.md). With these integrations, you can create incident, problem, change, and request records from customer service cases. Customers can also submit requests from the Customer Service Portal.


**Parent Topic:**[Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/customer-service-mgmt-rn-landing.md)

