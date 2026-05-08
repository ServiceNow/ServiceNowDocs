---
title: Self-service and omnichannel engagement for CSM release notes
description: With self-service and omnichannel applications in the ServiceNow Customer Service Management \(CSM\) application, your customers can use chat on self-service portals, consumer messaging apps, email, or phone calls to connect with your organization. Self-service and omnichannel applications for CSM were enhanced and updated in the Australia.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 10
---

# Self-service and omnichannel engagement for CSM release notes

With self-service and omnichannel applications in the ServiceNow® Customer Service Management \(CSM\) application, your customers can use chat on self-service portals, consumer messaging apps, email, or phone calls to connect with your organization. Self-service and omnichannel applications for CSM were enhanced and updated in the Australia.

## Self-service and omnichannel applications for CSM highlights for the Australia release

-   Enhance B2C consumer support through ServiceNow AI Platform self-service capabilities with the Consumer Portal.
-   Embed components into external websites to provide users with access to the self-service capabilities on the ServiceNow AI Platform.
-   Reduce manual documentation and maintain consistency by using Now Assist to auto-generate wrap up codes and summaries from transcripts.
-   Enable agents to initiate outbound email interactions from contact or consumer records, with configurable automated reminders to end users, enabling proactive customer engagement and comprehensive email tracking. Improve reporting reliability and compliance with configurable wrap‑up codes for CCaaS and AWA‑routed email interactions.
-   Schedule, reschedule, and cancel native callbacks from Agent Workspace across all omnichannel interactions \(chat, voice, email, and messaging\) and cases without switching to external tools or applications.

See Omnichannel, Self-service for Customer Service Management, and Interaction Controls Component \(ICC\) for voice calls for more information.

**Important:** Self-service and omnichannel applications are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **Configure Web Embeddables**

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
-   **Use Interaction Controls Component \(ICC\) call controls with Amazon Connect**

    Manage Amazon Connect calls in the CSM Configurable Workspace voice Interaction record. The integration supports inbound and outbound call flows, presence management, and transfers without switching applications.

-   **Supervisor call monitoring**

    Monitor, coach, and join agent calls from the CSM Configurable Workspace without having to switch to the CCaaS desktop. All supervisor actions are automatically logged for auditing and reporting purpose.

-   **Agent help request for voice calls**

    Empower agents to request supervisor assistance during calls by selecting the **Help Request** button. Agents can specify reasons why they are calling for help to provide more context to the supervisor before the supervisor responds, and receive notifications when supervisors coach or join. All help request data is captured for reporting for data-driven coaching. Some other key features include the following:

    -   Configure phone directory to show or hide Agents, Queues, or External tabs based on CCaaS provider settings. Agents see tabs enabled by the CCaaS provider, preventing transfers to unsupported numbers.
    -   While handling a customer call, agents can now see accurate availability status for other agents, supporting informed transfer decisions. Agent availability status updates in the transfer list and phone directory in real-time during call transfers.
-   **Use AI to generate wrap up code and notes summary**

    Automatically suggest a wrap-up code and generate an interaction summary based on conversation transcripts by using Now Assist, which reduces manual documentation time and contributes to consistent record-keeping. Choose automatic or agent-initiated generation to fit your workflow.

-   **Using the Consumer Portal**

    Support your consumers through the Consumer Portal self-service capabilities such as knowledge articles, service catalogs, case management, Virtual Agent, and others. These capabilities help reduce maintenance effort through low-code configurations on pages with configurable widgets.

-   **Native callback features**

    Callback management enables agents to schedule callbacks on behalf of customers. The key features include:

    -   Enable agents to schedule callbacks from any interaction or case.
    -   Equip agents to reschedule or cancel callbacks from the callback record page with proper state tracking.
    -   Facilitate agents to view scheduled callbacks in the list view so they can open the individual callback record page.
    -   Enable agents to view and manage scheduled callbacks for the current interaction or case in the contextual side panel.
-   **Email interaction feature: Wrap up of email interactions**

    Note the following capabilities introduced for wrapping up email interactions:

    -   Introduction of wrap‑up modal for Advanced Work Assignment \(AWA\) and CCaaS‑routed email interactions with internal wrap‑up codes configurable by admins.
    -   Automatic closure of inactive interactions with system-assigned wrap-up codes in multiple scenarios:
        -   When agents create a case from an email interaction.
        -   When the wrap-up modal times out without agent submission.
        -   When customers don’t respond within the defined follow-up period.
-   **Email interaction feature: Outbound Interaction from agent-initiated email**

    The new capabilities for outbound interactions initiated by agents through email are:

    -   Initiate outbound email interactions from contact or consumer records by selecting email addresses or using the Compose Email UI option, opening a modeless email composer with the recipient's email address auto populated.
    -   Automatic creation of Work‑In‑Progress \(WIP\) outbound email interactions when agents initiate an email to a customer.
    -   Preserve email drafts when agents navigate away, and automatically close interactions that show no sent or received email activity and contain only unsent drafts within a rolling 30‑day period. Any agent activity on the draft resets the 30‑day window.
    -   Consolidate multiple agent‑initiated drafts into a single, unified interaction within service workflows, with ownership assigned to the sending agent. You can optionally configure the system to create separate interactions for each draft for the same contact.
    -   Configurable reminder windows for sending automated reminder emails when customers don’t respond.
    -   Customer response notifications on the ongoing tab and interaction linking in contact or consumer related lists for seamless conversation tracking.
-   **Email interaction feature: Transfer Email Interactions routed by CCaaS**

    Transfer CCaaS‑routed email interactions to another agent or queue, improving accurate handoff and workload distribution.


## UI changes

-   **Agent help request for voice calls**

    The following UI components have been added to the Global Call window in the agent CSM Configurable Workspace when making outbound calls from a keypad or phone directory:

    -   A **Help Request** button to seek supervisor assistance during an active call.
    -   A **Cancel Help Request** button to cancel a submitted help request at any time during the active call.
-   **Using the interaction and case page for callback request**

    The following UI components have been added on the interaction and case pages:

    -   A **Schedule callback** button on interaction and case pages to enable agents to schedule callbacks on behalf of customers.
    -   A **Reschedule** button on the callback task record page to enable agents to modify scheduled callback date and time on behalf of customers.
    -   A **Cancel** button on the callback record page to enable agents to cancel callbacks created on behalf of customers.
    -   A **Scheduled callbacks** tile in the contextual side panel to enable agents to view and manage upcoming callbacks while working on interactions or cases.
    Scheduled callbacks list view: A **Scheduled callbacks** list view has been added in Agent Workspace to enable agents to view all scheduled callbacks and open any callback to access its task record management.

-   **Using the email interaction page**

    The following UI components have been added on the Email Interaction page:

    -   A **Compose Email** UI option to contact and consumer records for initiating outbound email interactions from these records.
    -   Clickable email addresses to contact and consumer records to open the email composer with the recipient address automatically inserted.
    -   A **Transfer Email** option with list of available agents and queues has been added for CCaaS‑routed email interactions, enabling agents to transfer the interaction to the selected queues or agents.
    -   A unified wrap‑up dialog has been added to provide a single closure experience for email interactions routed through AWA or CCaaS.

## Changed in this release

-   **Customer Service Portal Base**

    Starting with the Australia release, the Customer Service Portal Base plugin \(com.snc.csm\_portal\_base\) has been migrated to the App Store as a standalone application. Future enhancements are delivered through the Customer Service Portal Base store app. This change improves packaging, versioning, and deployment flexibility for implementations that require portal framework, responsive design, case management, knowledge integration, and community features. The store app also includes email integration, translation support, attachment handling, and mobile enhancements.

-   **Subscriptions and Activity Feed Framework**

    Starting with the Australia release, the Subscriptions and Activity Feed Framework plugin \(com.snc.subscriptions\_activity\_feed\) has been migrated to the App Store as a standalone application. Future enhancements are delivered through the Subscriptions and Activity Feed Framework store app. This change improves packaging, versioning, and deployment flexibility for implementations that require subscription framework, activity tracking, notification preferences, or context management.

-   **Walk-Up for CSM**

    Starting with the Australia release, the Walk-up for CSM plugin \(com.snc.walkup\_for\_csm\) has been migrated to the App Store as a standalone application. Future enhancements are delivered through the Walk-up for CSM store app. This change improves packaging, versioning, and deployment flexibility for implementations that require subscription framework, activity tracking, notification preferences, or context management.


## Activation information

Install self-service and omnichannel applications, such as OpenFrame and Interaction Controls Component \(ICC\), by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Plugin information

-   **New plugins**

    The following plugins are new in the Australia release:

    -   Customer Service integration with Social Media Store \(sn\_cs\_social\_host\): The Customer Service integration with Social Media app enables agents to select Social as the communication channel and add a social profile to the Case form. Any communication with customers or consumers that takes place through social media is recorded on the Case form in the Social Logs related list. For more information, see Social media communication channel
    -   Web Components for Customers \(sn\_cx\_components\): The plugin adds Case create and Case view Web Embeddables components to your ServiceNow instance. You can clone and configure them, and embed on your third-party website. For more information, see Activate Web Embeddables.
    -   Web Embeddable Core \(sn\_embeddable\_core\): This plugin enables you to create, edit, clone, delete, and organize components into modules, groups, and instances. Each instance can be configured with a live preview. It also provides tools to manage CORS rules for secure integration. For more information, see Activate Web Embeddables.
    -   Web Components for Guest \(sn\_guest\_component\): This plugin enables guest user access to Knowledge article view and Catalog item Web Embeddables components on third-party websites. It allows unauthenticated users to view public knowledge articles and submit catalog items without logging in. You can configure access controls to determine which content is publicly accessible. For more information, see Activate Web Embeddables.
-   **Plugins planned for deprecation**

    These plugins are planned for deprecation in the C release. Beginning with the Australia release, these plugins will be migrated to store applications. Upgrade your instance to Australia release version and the store applications will be automatically installed:

    -   Openframe Integration App \(com.sn\_openframe\_integration\)
    -   Skill Determination \(com.snc.skill\_determination\)
    -   Advanced Work Assignment for CSM \(sn\_csm.awa\)
    -   Social Media Store \(sn\_cs\_social\_host\)

## Browser requirements

Starting with the Australia release, self-service and omnichannel application don't support Internet Explorer. For more information, see [Browser support](../../administer/navigation-and-ui/reference/browser-support.md).

## Related ServiceNow applications and features

-   **Field Service Management**

    The Field Service Management application helps you manage work orders and related tasks, resources, skills, assets, and locations. Assign work order tasks and dispatch agents to a customer location to perform field work.

-   **Knowledge Management**

    From the Customer Service Portal and Consumer Service Portal, enable your customers to search for shared information using the Knowledge Management application. Customer service agents can use knowledge content to help resolve cases.

-   **IT Service Management**

    The following IT Service Management applications can integrate with Customer Service Management: Incident Management, Problem Management, Change Management, and Request Management. With these integrations, you can create incident, problem, change, and request records from customer service cases. Customers can also submit requests from the Customer Service Portal.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

