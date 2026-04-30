---
title: Service Operations Workspace for ITSM release notes
description: The ServiceNow Service Operations Workspace application is a configurable workspace that provides a unified experience for multiple IT Service Management and IT Operations Management capabilities. You can configure your agent experience by using the interface of Service Operations Workspace for ITSM. Service Operations Workspace for IT Service Management was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 20
---

# Service Operations Workspace for ITSM release notes

The ServiceNow® Service Operations Workspace application is a configurable workspace that provides a unified experience for multiple IT Service Management and IT Operations Management capabilities. You can configure your agent experience by using the interface of Service Operations Workspace for ITSM. Service Operations Workspace for IT Service Management was enhanced and updated in the Xanadu release.

## Service Operations Workspace for ITSM highlights for the Xanadu release

-   Use the simplified navigation from Admin Center to manage configurations for incidents, problems, change requests, and the contextual side panel in the record pages in Service Operations Workspace for ITSM. It improves the administrator's experience.
-   Migrate your ITSM Agent Workspace features to Service Operations Workspace for ITSM with an on-screen utility.
-   Configure the user access for various record pages in Service Operations Workspace for ITSM by using granular roles.
-   View the Configuration Item \(CI\) dependency map for reference fields in an incident record.
-   View the VIP field decorator on a caller field in an incident record for VIP users.
-   Test the features and workflows for Incident Management in Service Operations Workspace for ITSM with quick start tests.
-   Broadcast communication messages as announcements in Major Incident Management.
-   Resolve the password reset related incidents by using the **Password reset** UI action on an incident record.
-   Identify an interaction record for its precise processing by specifying the values for its **Opened for** and **Short description** fields.
-   Enable a service desk agent to reset a user password in Service Operations Workspace for ITSM.
-   Get AI-powered search results for these record types: incident, incident task, problem, problem task, change request, change request task, interaction, and request. These AI-powered search results help you to quickly find the solutions you need.
-   Manage the life cycle of a problem by using the configurable and dynamic **Overview** tab.
-   Use Guided Tours to learn about a concept or process within Service Operations Workspace for ITSM.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.
-   Starting in version 6.1 you can do the following:
    -   Configure the Interaction Management features from the SOW admin center.
    -   Provide users with current resources for learning about SOW admin configuration.
    -   View the requester’s device details from the record information card to quickly resolve hardware-related issues.
    -   Add one or more approvers to the request or a request item to speed up the process and fulfill the user's request more efficiently.
    -   Improve the system performance by configuring the count of number of incident records in the incident list page.
    -   Copy the sys ID or the URL of a record from the SOW list page to share with other agents, enabling quicker resolution of the issue.
    -   Chat or make calls to communicate with stakeholders using the **Collaborate** option in the contextual sidebar of problem and problem task records.
    -   Configure the automatic closure of interaction record from an incident record.
    -   Flag the events on the activity stream of a major incident to add the events to the post incident report events timeline.
    -   View the post incident report information on the **Post incident report** tab with the Incident management granular roles.
    -   Add related interaction records to an incident record.
    -   Define, customize, and apply tags to the activities in the activity streams of an incident record.
    -   Experience a clean UI with collapsible activity stream tiles.
    -   Resolve incident or support issues faster and more efficiently with response templates.
    -   Get similarity-based problems and change requests as recommendations by recognizing the similar patterns between the fields of the incident table and the problem or change request table.
    -   Manage the Standard Change life cycle.
    -   Explore and filter the Standard Change Catalog.
    -   Propose mass configuration item updates in Change Management.

See [Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=sow-landing-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) for more information.

**Important:** Service Operations Workspace for ITSM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Service Operations Workspace to Xanadu

Ensure that the following applications have compatible upgraded versions:

-   Service Operations Workspace ITSM Applications application \(sn\_sow\_itsm\_cont\)
-   Service Operations Workspace ITOM Applications application \(sn\_sow\_itom\_cont\)

|Service Operations Workspace for ITSM \(sn\_sow\_itsm\_cont\)|Service Operations Workspace for ITOM \(sn\_sow\_itom\_cont\)|
|-------------------------------------------------------------|-------------------------------------------------------------|
|1.1.x|21.0.y|
|1.2.x|21.1.y|
|1.3.x|21.2.y, 21.5.y, and 21.6.y|
|2.0.x|22.0.y|
|2.1.x|22.1.y and 22.y.y|
|3.1.x|23.y.y|
|4.x.x|24.y.y|
|5.0.x|24.2.y|
|5.1.0|25.2.0|
|6.1.1|26.0.12|

## New in the Xanadu release

-   **[Admin Center changes](https://www.servicenow.com/docs/access?context=manage-admin-console-sow-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**
    -   Migrate your ITSM Agent Workspace features to Service Operations Workspace by using the on-screen utility without having to rebuild these features. This migration includes customizations done on ITSM Agent Workspace for various forms, UI actions, and lists.
    -   Configure the availability and order of the contextual side panel tabs in record pages.
    -   Configure modern Change Management features from the Service Operations Workspace Admin Center to increase change efficiency, accelerate change approvals, drive data-driven risk analysis, and leverage DevOps data for change automation.
    -   Configure the visibility settings of the **Overview** tab for each problem record state.
    -   Configure the visibility settings of the **Overview** tab in the incident record page for tier 1 agents from the Incident record section of Incident Management in Admin Center.
    -   Configure Service Desk assisted Password Reset to accomplish the following tasks:
        -   Assign the password reset service desk role to the user.
        -   Create a credential store record to configure access to your credential store server while a user is changing or resetting a password.
        -   Configure the verification methods for the service desk process.
        -   Configure the password policies.
    -   Starting in version 6.1, you can do the following actions from the SOW Admin Center:
        -   Configure Interaction Management in SOW.
        -   Browse through a collection of SOW learning resources to help users understand more about SOW configuration.
-   **[Granular roles](https://www.servicenow.com/docs/access?context=roles-in-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Configure the user access for various record pages in Service Operations Workspace for ITSM by using the following granular roles, and the user’s access to these record pages is based on the role assigned.

    -   Incident: sn\_incident\_read and sn\_incident\_write
    -   Request: sn\_request\_read, sn\_request\_write
    -   Problem: sn\_problem\_read, sn\_problem\_write
    -   Change: sn\_change\_read and sn\_change\_write
    Because these granular roles inherit the sn\_sow.sow\_home and sn\_sow.sow\_list roles, the users with the granular roles can access the Service Operations Workspace for ITSM home and list pages.

    **Note:** When upgrading to Xanadu, the email\_composer user role is added to the users along with the respective granular roles. The time to add the role depends on the number of users having the granular roles for write function and impacts the overall instance upgrade time. Adding the email\_composer user role ensures that the granular write users have access to the email templates in SOW.

-   **[Interaction record page enhancements](https://www.servicenow.com/docs/access?context=create-interactions&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    View the requester's details, their assets, recent interactions, and related links from the Opened for card. This centralized access point provides an agent with a comprehensive overview to efficiently manage the requester's information.

    To streamline the workflow and maintain focus on interactions, a modal-based interface for record association is implemented for the interaction record in Service Operations Workspace. This interface simplifies the workflow by automatically suggesting tables that are frequently associated with Interactions, including the change, incident, knowledge, problem, and request. This enhancement is designed to streamline operations and enhance user efficiency.

    Starting in version 6.1, view all available metrics of the requester’s assets that are collected through the Digital End-User Experience \(DEX\) architecture from the interaction record.

-   **[Incident record page enhancements](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    The incident record page has the following enhancements:

    -   View the Configuration Item \(CI\) dependency for the following reference fields:
        -   Configuration item
        -   Service
        -   Service Offering
    -   View the VIP field decorator for a caller field in the **Details** tab and in the **Record information** tab of the contextual side panel for VIP users.
    -   Search and filter the configuration items \(CI\) that are based on the configuration class when you add the affected CIs to an incident record.
    -   When an agent reports a knowledge gap from an incident record, the success message that contains the created knowledge feedback task record link is displayed. You can select the link to open the knowledge feedback task record on a separate tab to provide the information and create an article for the knowledge gap.
    -   For issues related to Password Reset, you can now select **Password Reset** as the incident category. After this category is set and the incident record is saved, you can resolve the incident by using the Reset password UI action. For more information on Password Reset, see [Password Reset in SOW](https://www.servicenow.com/docs/access?context=exploring-password-reset-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).
    -   Starting in version 6.1, the incident record has the following enhancements:
        -   The activity stream displays the activity information in tiles that are collapsible. By default, the first activity tile, either a work note or comment, is expanded and the consecutive tiles are collapsed. This ensures a clean UI and enables you to expand and view the activity information when required. It ensures a clean UI and enables you to view the activity information when required. To enable this feature, set the **Enable the expandable activity stream tiles** \(**enableExpandableActivityStreamTiles**\) UX page property to `true`.
        -   An internal tag is added to the work notes.
        -   You can define, customize, and apply tags to the activity streams. These tags help you filter the activity based on the tags. You can use the **Activity stream property** \(**activitystreamprops**\) property to define and customize your tags.
        -   Add related interaction records to an incident from the Interactions related list of the **Related records** tab.
        -   Resolve cases or support issues faster and more efficiently with response templates. Access the response templates \(formerly known as templated snippets\) from the contextual side panel of an incident record to quickly copy the reusable messages and provide quick and consistent messages to users, or to display standard chat response messages to the requesters in chat.
        -   Use the **Opened By** field in the Origin card of the Record information side panel tab of an incident to view the user who created the incident's origin record.
        -   Use the **Type** field in the Origin card of the Record information side panel tab of an incident to view the channel type of the incident's origin record. For example, if the origin is an interaction record, the type can be Chat.
        -   If an incident is created from an interaction record, you have the following options:
            -   View chat transcript: View the chat history with the caller of the interaction record. This option is available only if the interaction record is of the Chat type and is in Closed complete or Closed Abandoned state.
            -   View work notes: View the work notes history of the interaction record.
-   **[Announcements for a major incident](https://www.servicenow.com/docs/access?context=create-announcements-major-inc&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Keep your users informed about an ongoing major incident by broadcasting communication messages about it. Create and configure announcements from the **Communicate** tab of the major incident record. Announcements can appear in an announcement banner or an announcement widget that users can view on their IT service portal.

-   **[Major incident record enhancements](https://www.servicenow.com/docs/access?context=review-update-pir-mim-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Starting in version 6.1, you can do the following:

    -   View the information on the **Post incident report** tab using the incident management granular roles such as sn\_incident\_read and sn\_incident\_write.
    -   Flag events on the activity stream of a major incident to include them in the post incident report events timeline.
    -   Access the Collaborate side panel tab and its features from the incident communication task \(ICT\) record associated with the major incident record.
    -   Select or change the SMS templates for the major incident SMS communication to the required end users with the following roles:
        -   major\_incident\_manager
        -   sn\_incident\_write user who has the required communication related roles
        -   ITIL user to whom the major incident is assigned
-   **[Automatic closure of an interaction from an incident](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Starting in version 6.1, when an incident record created from an interaction record is resolved, the interaction record is automatically set to **Wrap up** or **Closed complete** state. You must set the **Auto close the origin interaction** \(**sn\_sow\_inc.autoclose\_origin.interaction**\) system property to `true` and the **Close interaction from incident** business rule must be `Active`.

-   **[SOW list page enhancements](https://www.servicenow.com/docs/access?context=incident-list-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Starting in version 6.1, you can do the following:

    -   View the user who updated the incident record using the **Updated** column on the SOW incident list page.
    -   Copy the sys ID or the URL of a record from the SOW list page to share with other agents, enabling quicker resolution of the issue.
    -   Configure the **fuzzyCount** property to display the number of records on the list page.
-   **[Collaboration in Problem Management](https://www.servicenow.com/docs/access?context=problem-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Starting in version 6.1, you can chat or make calls to communicate with stakeholders using the [**Collaborate** option in the contextual side panel](https://www.servicenow.com/docs/access?context=collaboration-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) of problem and problem task records.

-   **[Change Management enhancements](https://www.servicenow.com/docs/access?context=change-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Starting in 6.1, you can do the following:

    -   Find your change model or template when raising new changes by using the enhanced filtering and search capabilities for the Standard Change Catalog.
    -   Manage the Standard Change life cycle.
    -   Propose, modify, and retire Standard Change templates.
    -   Propose mass configuration item \(CI\) updates.
    -   Propose changes to single CIs.
    -   Automate the update and audit trail of CIs, with mass updates and change proposals recording the attributes being changed and \(optionally\) updating the CMDB automatically.
-   **[Quick start tests for Incident Management in Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=quick-start-tests-im-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Incident Management features work as expected. If you customized Incident Management, copy quick start tests and configure them for your customizations. The following quick start tests are added for Incident Management in Service Operations Workspace for ITSM:

    -   Create problem from incident: Enables you to test the problem creation from an incident by using the Create problem UI option.
    -   Verify Assign to me button functionality: Enables you to test the incident assignment by using the Assign to me UI option.
-   **[Password Reset in Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=exploring-password-reset-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Assist users to quickly access their accounts by enabling them to reset the user password.

-   **[Exploring Recommended Actions for ITSM in Service Operations Workspace](https://www.servicenow.com/docs/access?context=exploring-recommended-actions-for-itsm-in-service-operations-workspace&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Manually search for AI-powered recommendations that assist in swiftly addressing issues. AI-enhanced search results are available for these record types: incident, incident task, problem, problem task, change request, change request task, interaction, and request.

-   **[__Overview__ tab for problem records](https://www.servicenow.com/docs/access?context=problem-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Configure how and what information is displayed in the sections of the dynamic **Overview** tab for each problem state.

-   **[Manage life cycle of problem tasks](https://www.servicenow.com/docs/access?context=work-on-problem-task-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Provide additional flexibility for problem task analysts, including the ability to reassess problem tasks from the Work in Progress state.

-   **[Initial support for problem models](https://www.servicenow.com/docs/access?context=problem-mgmt-models-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Introduction of Problem Management models, one default problem model \(General\) and two default problem task models \(Root cause analysis and General\).

    The default models are equivalent to the base life cycle in the Xanadu release. This initial support enables you to create custom models to tailor additional scenarios for specific use cases.

    **Note:**

    If you’re using Service Operations Workspace 5.x and you enable Problem Management models, you manage problems and problem tasks in the classic UI16 experience, rather than in Service Operations Workspace.

    Service Operations Workspace 6.x is based on the Xanadu release and it supports Problem Management models.

-   **[Shortcuts for creating fix tasks from a problem](https://www.servicenow.com/docs/access?context=problem-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Use the following shortcuts from the **Overview** tab of a problem:

    -   **Create defect** \(part of Agile Development 2.0\)
    -   **Create enhancement** \(part of Agile Development 2.0\)
    -   **Create improvement initiative** \(part of Continual Improvement Management\)
-   **[Guided tours](https://www.servicenow.com/docs/access?context=explore-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Learn about Service Operations Workspace for ITSM through a sequence of interactive steps that guide you through a specific concept or process.

    Starting in version 6.1, the following guided tours are available:

    -   Overview of the PAR dashboard
    -   Overview of the various tabs and actions of an incident record page.
    -   Generate and download a post incident report for sharing it with all the stakeholders.
    -   Overview of the various tabs and actions of a problem record page.
    -   Get tailored recommendations for problems
    -   Get tailored recommendations for interactions
    -   Get tailored recommendations for requests
-   **[Add approvers to approve a request](https://www.servicenow.com/docs/access?context=add-approvers-request-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Starting in version 6.1, to expedite the process and effectively meet the user's request, you can add one or more approvers to the request or to a specific request item. This helps to streamline the approval workflow and ensure that the user's needs are fulfilled quickly and efficiently.


## Changed in this release

-   **[Landing page configurations from Admin Center](https://www.servicenow.com/docs/access?context=manage-admin-console-sow-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    All landing page configurations such as the landing page redirection, donut configurations, and so on are grouped under the **Landing Page Configurations** section of the **Configurations** tab.

-   **[Reordering of modules on the left navigation pane](https://www.servicenow.com/docs/access?context=reorder-left-navigation-pane-modules&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    The left navigation pane modules, such as Inbox and Lists, are reordered for improved access to these modules.

-   **[Role to create a request from interaction and incident records](https://www.servicenow.com/docs/access?context=create-catalog-request-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    A user should now have either the itil role or sn\_request\_write role to create a request from interaction and incident records. Before Xanadu, users needed the interaction\_agent role to create the request.

-   **[DevOps data in change request](https://www.servicenow.com/docs/access?context=create-change-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**
    -   View, add, and edit DevOps data in a manually created change request in Service Operations Workspace for ITSM for a unified change request experience in the DevOps Change Workspace and Service Operations Workspace for ITSM.
    -   Starting in version 6.1, view, add, and edit work items data in a manually created DevOps change request in Service Operations Workspace for ITSM.
-   **[Creating change requests from problem records](https://www.servicenow.com/docs/access?context=work-on-problem-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    You can create additional change requests, because the action is no longer hidden after it has been used once.

-   **[Inline editing in the __Problem Tasks__ tab](https://www.servicenow.com/docs/access?context=lists-inline-edit&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Change a field in the problem tasks list instead of opening the record and changing it on the form.

-   **[Sidebar enhancements for incidents](https://www.servicenow.com/docs/access?context=using-sidebar&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    The sidebar will now display recommendations for users who can assist agents in resolving incidents or tasks. A standard set of recommendations are provided to enhance the support workflow.

    ITSM Pro provides the customized recommendations using an AI-based algorithm, ensuring that the most appropriate users are suggested to assist with the task.

    The group addition feature offers the ability to add entire groups to a conversation. By default, all members of a group will be included in the conversation. For groups with designated on-call members, only those members are added to the conversation, enabling for more focused and efficient communication.

-   **[Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Service Operations Workspace for ITSM configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For more information, see the Accessibility information section that follows.

-   **[Email notification redirection behavior in Problem Management](https://www.servicenow.com/docs/access?context=configure-notifcations-sow-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    When users select the problem record link in their email notifications, they can be redirected to the problem record in Service Operations Workspace instead of the classic UI16 experience. The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.

-   **[Work notes in Compose section](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Starting in version 6.1, the Work notes \(Private\) is displayed as default in the **Compose** section instead of the **Comments \(Customer visible\)** section for incident records.

-   **View the Close icon**

    Starting in version 6.1, the “X” symbol of the Close icon is clearly visible on the SOW landing page.

-   **Complementary landmark for screen reader support**

    Starting in version 6.1, the complementary landmark is available on the SOW landing page for the screen reader support.

-   **View the Problem and Change record information with incident granular roles**

    Starting in version 6.1, when a user with incident granular roles \(sn\_incident\_read and sn\_incident\_write\) selects the preview info icon on the problem and change records from the related records section of the **Details** tab on an incident record, a pop up displays a message that they don’t have the permission to view the record.

-   **View impacted location for proposed major incident candidate**

    Starting in version 6.1, you can view the impact locations for a proposed major incident candidate along with promoted major incident.

-   **Expansion of the compose section with activity stream**

    Starting in version 6.1, when a file containing a lengthy name is attached to an incident record, and the activity stream is expanded to view the file name, the compose section also expands on the same level as the activity stream.

-   **Copy URL action for Incident list page**

    Starting in version 6.1, you can copy and share the incident record on the Incident list page with the required stakeholders.

-   **Arrow orientation in record information panel**

    Starting in version 6.1, the arrows next to the links in the Opened for card in the record information panel now point in the right direction, including for right-to-left languages.

-   **Access to form header links**

    Starting in version 6.1, you can now select the form header links irrespective of the size of the browser.


## Activation information

Service Operations Workspace for ITSM is active by default and its default version is 5.0 in Xanadu. When you upgrade from any previous release to Xanadu from ServiceNow Store, Service Operations Workspace for ITSM 5.0 is automatically installed.

## Accessibility information

-   **Accessibility improvements**

    Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

    The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

    This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for details.

-   **Resize text**

    Starting in version 6.1, text size can be increased to 400% through your browser settings without loss of content or functionality for Incident Management and Password Reset in SOW.


## Related ServiceNow applications and features

-   **[Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-overview&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Automatically assign interactions to your agents based on their availability.

-   **[Change Management](https://www.servicenow.com/docs/access?context=c_ITILChangeManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Control the life cycle of a change and implement the change with minimum disruption to IT services.

-   **[Incident Management](https://www.servicenow.com/docs/access?context=c_IncidentManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Enable users to identify IT issues and log incidents through the Incident Management system. Efficiently track, classify, and prioritize incidents to work effectively toward their resolution.

-   **[Interaction Management](https://www.servicenow.com/docs/access?context=interaction-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Respond to an incoming chat, phone, walk-up, or messaging interaction quickly by using an interaction that provides a centralized location for all communication channels.

-   **[Knowledge Management](https://www.servicenow.com/docs/access?context=knowledge-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Provide an agent with knowledge articles that include information such as self-help, troubleshooting, and task resolution.

-   **[Notify](https://www.servicenow.com/docs/access?context=notify-landing-page&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Provide support for SMS and voice channels on the platform to communicate with your team and customers.

-   **[Now Assist for ITSM](../analytics-intelligence-reporting/now-assist-rn.md)**

    Use the ServiceNow® Now Assist for ITSM application to summarize your incident information, generate resolution notes, and generate the chat information for an interaction. You can enable your agents to understand the chat and incident context and to propose quicker resolutions.

-   **[On-Call Scheduling](https://www.servicenow.com/docs/access?context=c_OnCallScheduling&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Identify available on-call members of a support group who can be contacted to resolve an issue.

-   **[Password Reset](https://www.servicenow.com/docs/access?context=password-reset-landing-page&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    The ServiceNow® Password Reset application enforces strong and secure passwords by enabling end users to reset or change their passwords either by using the self-service process or by requesting the assistance of a service desk agent.

-   **[Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use machine-learning algorithms to provide dynamic and contextual recommendations for resolving an incident.

-   **[Problem Management](https://www.servicenow.com/docs/access?context=c_ProblemManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Identify the root cause of recurring incidents or a major incident to help prevent them from happening again.

-   **[Recommended Actions for ITSM in Service Operations Workspace](https://www.servicenow.com/docs/access?context=recommended-actions-for-itsm-in-service-operations-workspace&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Get field recommendations and guidance in the side panel for the incident form in the Service Operations Workspace.

-   **[Request Management](https://www.servicenow.com/docs/access?context=c_RequestManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Initiate a catalog request flow from a different IT Service Management flow, such as an incident flow, by using catalog requests.

-   **[Service Level Management](https://www.servicenow.com/docs/access?context=service-level-mgmt-landing-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Access incident service level agreement \(SLA\) information on the Service Operations Workspace for ITSM landing page and incident record page.

-   **[ServiceNow for Microsoft Teams](https://www.servicenow.com/docs/access?context=c_ServiceNowForMSTeams&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    Enable users to collaborate through the connected experience provided by Service Operations Workspace for ITSM.

-   **[Service Operations Workspace for ITOM](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Configure your operator experience through a unified interface for multiple ServiceNow® IT Operations Management workflows.

-   **[Task Intelligence for ITSM](https://www.servicenow.com/docs/access?context=c-itsm-task-intelligence&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Use machine learning to set up, deploy, and track solution-based models to achieve important business outcomes.

-   **[Universal Request](https://www.servicenow.com/docs/access?context=ur-landing-limitedaccess&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    ServiceNow® Universal Request empowers customers in their journey toward Enterprise Service Management \(ESM\) or Global Business Services \(GBS\) by enabling agents to resolve cases seamlessly across the enterprise to provide a better employee experience.

-   **[Walk-up Experience](https://www.servicenow.com/docs/access?context=walkup-experience-landing-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Manage walk-up interactions and queues effortlessly by using Service Operations Workspace for ITSM.

-   **[Workforce Optimization for ITSM](https://www.servicenow.com/docs/access?context=workforce-optimization-itsm-landing-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Manage agent schedules by using Workforce Optimization for ITSM Scheduling. Use ServiceNow® Coaching to review and complete assigned trainings.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

