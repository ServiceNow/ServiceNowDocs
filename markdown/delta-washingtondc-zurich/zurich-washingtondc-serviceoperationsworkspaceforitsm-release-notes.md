---
title: Combined Service Operations Workspace for ITSM release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Service Operations Workspace for ITSM from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-serviceoperationsworkspaceforitsm-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 37
breadcrumb: [Products combined by family]
---

# Combined Service Operations Workspace for ITSM release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Service Operations Workspace for ITSM from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Service Operations Workspace for ITSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Service Operations Workspace for ITSM to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

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

</td></tr><tr><td>

Yokohama

</td><td>

Ensure that the following applications have compatible upgraded versions:

-   Service Operations Workspace ITSM Applications application \(sn\_sow\_itsm\_cont\)
-   Service Operations Workspace ITOM Applications application \(sn\_sow\_itom\_cont\)

 For more information on compatible versions, see [Version compatibility between Service Operations Workspace for ITSM and Service Operations Workspace ITOM](https://servicenow-staging.fluidtopics.net/access?context=sow-itsm-itom-version&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Ensure that the following applications have compatible upgraded versions:

-   Service Operations Workspace ITSM Applications application \(sn\_sow\_itsm\_cont\)
-   Service Operations Workspace ITOM Applications application \(sn\_sow\_itom\_cont\)

 For more information on compatible versions, see [Version compatibility between Service Operations Workspace for ITSM and Service Operations Workspace ITOM](https://servicenow-staging.fluidtopics.net/access?context=sow-itsm-itom-version&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Service Operations Workspace for ITSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Admin Center changes](https://servicenow-staging.fluidtopics.net/access?context=manage-admin-console-sow-itsm&family=xanadu&ft:locale=en-US)**
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
-   **[Granular roles](https://servicenow-staging.fluidtopics.net/access?context=roles-in-sow&family=xanadu&ft:locale=en-US)**

Configure the user access for various record pages in Service Operations Workspace for ITSM by using the following granular roles, and the user’s access to these record pages is based on the role assigned.

    -   Incident: sn\_incident\_read and sn\_incident\_write
    -   Request: sn\_request\_read, sn\_request\_write
    -   Problem: sn\_problem\_read, sn\_problem\_write
    -   Change: sn\_change\_read and sn\_change\_write
Because these granular roles inherit the sn\_sow.sow\_home and sn\_sow.sow\_list roles, the users with the granular roles can access the Service Operations Workspace for ITSM home and list pages.

**Note:** When upgrading to Xanadu, the email\_composer user role is added to the users along with the respective granular roles. The time to add the role depends on the number of users having the granular roles for write function and impacts the overall instance upgrade time. Adding the email\_composer user role ensures that the granular write users have access to the email templates in SOW.

-   **[Interaction record page enhancements](https://servicenow-staging.fluidtopics.net/access?context=create-interactions&family=xanadu&ft:locale=en-US)**

View the requester's details, their assets, recent interactions, and related links from the Opened for card. This centralized access point provides an agent with a comprehensive overview to efficiently manage the requester's information.

To streamline the workflow and maintain focus on interactions, a modal-based interface for record association is implemented for the interaction record in Service Operations Workspace. This interface simplifies the workflow by automatically suggesting tables that are frequently associated with Interactions, including the change, incident, knowledge, problem, and request. This enhancement is designed to streamline operations and enhance user efficiency.

Starting in version 6.1, view all available metrics of the requester’s assets that are collected through the Digital End-User Experience \(DEX\) architecture from the interaction record.

-   **[Incident record page enhancements](https://servicenow-staging.fluidtopics.net/access?context=view-update-inc-overview-tab&family=xanadu&ft:locale=en-US)**

The incident record page has the following enhancements:

    -   View the Configuration Item \(CI\) dependency for the following reference fields:
        -   Configuration item
        -   Service
        -   Service Offering
    -   View the VIP field decorator for a caller field in the **Details** tab and in the **Record information** tab of the contextual side panel for VIP users.
    -   Search and filter the configuration items \(CI\) that are based on the configuration class when you add the affected CIs to an incident record.
    -   When an agent reports a knowledge gap from an incident record, the success message that contains the created knowledge feedback task record link is displayed. You can select the link to open the knowledge feedback task record on a separate tab to provide the information and create an article for the knowledge gap.
    -   For issues related to Password Reset, you can now select **Password Reset** as the incident category. After this category is set and the incident record is saved, you can resolve the incident by using the Reset password UI action. For more information on Password Reset, see [Password Reset in SOW](https://servicenow-staging.fluidtopics.net/access?context=exploring-password-reset-sow&family=xanadu&ft:locale=en-US).
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
-   **[Announcements for a major incident](https://servicenow-staging.fluidtopics.net/access?context=create-announcements-major-inc&family=xanadu&ft:locale=en-US)**

Keep your users informed about an ongoing major incident by broadcasting communication messages about it. Create and configure announcements from the **Communicate** tab of the major incident record. Announcements can appear in an announcement banner or an announcement widget that users can view on their IT service portal.

-   **[Major incident record enhancements](https://servicenow-staging.fluidtopics.net/access?context=review-update-pir-mim-sow&family=xanadu&ft:locale=en-US)**

Starting in version 6.1, you can do the following:

    -   View the information on the **Post incident report** tab using the incident management granular roles such as sn\_incident\_read and sn\_incident\_write.
    -   Flag events on the activity stream of a major incident to include them in the post incident report events timeline.
    -   Access the Collaborate side panel tab and its features from the incident communication task \(ICT\) record associated with the major incident record.
    -   Select or change the SMS templates for the major incident SMS communication to the required end users with the following roles:
        -   major\_incident\_manager
        -   sn\_incident\_write user who has the required communication related roles
        -   ITIL user to whom the major incident is assigned
-   **[Automatic closure of an interaction from an incident](https://servicenow-staging.fluidtopics.net/access?context=view-update-inc-overview-tab&family=xanadu&ft:locale=en-US)**

Starting in version 6.1, when an incident record created from an interaction record is resolved, the interaction record is automatically set to **Wrap up** or **Closed complete** state. You must set the **Auto close the origin interaction** \(**sn\_sow\_inc.autoclose\_origin.interaction**\) system property to `true` and the **Close interaction from incident** business rule must be `Active`.

-   **[SOW list page enhancements](https://servicenow-staging.fluidtopics.net/access?context=incident-list-page&family=xanadu&ft:locale=en-US)**

Starting in version 6.1, you can do the following:

    -   View the user who updated the incident record using the **Updated** column on the SOW incident list page.
    -   Copy the sys ID or the URL of a record from the SOW list page to share with other agents, enabling quicker resolution of the issue.
    -   Configure the **fuzzyCount** property to display the number of records on the list page.
-   **[Collaboration in Problem Management](https://servicenow-staging.fluidtopics.net/access?context=problem-sow&family=xanadu&ft:locale=en-US)**

Starting in version 6.1, you can chat or make calls to communicate with stakeholders using the [**Collaborate** option in the contextual side panel](https://servicenow-staging.fluidtopics.net/access?context=collaboration-sow&family=xanadu&ft:locale=en-US) of problem and problem task records.

-   **[Change Management enhancements](https://servicenow-staging.fluidtopics.net/access?context=change-sow&family=xanadu&ft:locale=en-US)**

Starting in 6.1, you can do the following:

    -   Find your change model or template when raising new changes by using the enhanced filtering and search capabilities for the Standard Change Catalog.
    -   Manage the Standard Change life cycle.
    -   Propose, modify, and retire Standard Change templates.
    -   Propose mass configuration item \(CI\) updates.
    -   Propose changes to single CIs.
    -   Automate the update and audit trail of CIs, with mass updates and change proposals recording the attributes being changed and \(optionally\) updating the CMDB automatically.
-   **[Quick start tests for Incident Management in Service Operations Workspace for ITSM](https://servicenow-staging.fluidtopics.net/access?context=quick-start-tests-im-sow&family=xanadu&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Incident Management features work as expected. If you customized Incident Management, copy quick start tests and configure them for your customizations. The following quick start tests are added for Incident Management in Service Operations Workspace for ITSM:

    -   Create problem from incident: Enables you to test the problem creation from an incident by using the Create problem UI option.
    -   Verify Assign to me button functionality: Enables you to test the incident assignment by using the Assign to me UI option.
-   **[Password Reset in Service Operations Workspace for ITSM](https://servicenow-staging.fluidtopics.net/access?context=exploring-password-reset-sow&family=xanadu&ft:locale=en-US)**

Assist users to quickly access their accounts by enabling them to reset the user password.

-   **[Exploring Recommended Actions for ITSM in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=exploring-recommended-actions-for-itsm-in-service-operations-workspace&family=xanadu&ft:locale=en-US)**

Manually search for AI-powered recommendations that assist in swiftly addressing issues. AI-enhanced search results are available for these record types: incident, incident task, problem, problem task, change request, change request task, interaction, and request.

-   **[__Overview__ tab for problem records](https://servicenow-staging.fluidtopics.net/access?context=problem-sow&family=xanadu&ft:locale=en-US)**

Configure how and what information is displayed in the sections of the dynamic **Overview** tab for each problem state.

-   **[Manage life cycle of problem tasks](https://servicenow-staging.fluidtopics.net/access?context=work-on-problem-task-sow&family=xanadu&ft:locale=en-US)**

Provide additional flexibility for problem task analysts, including the ability to reassess problem tasks from the Work in Progress state.

-   **[Initial support for problem models](https://servicenow-staging.fluidtopics.net/access?context=problem-mgmt-models-sow&family=xanadu&ft:locale=en-US)**

Introduction of Problem Management models, one default problem model \(General\) and two default problem task models \(Root cause analysis and General\).

The default models are equivalent to the base life cycle in the Xanadu release. This initial support enables you to create custom models to tailor additional scenarios for specific use cases.

**Note:**

If you’re using Service Operations Workspace 5.x and you enable Problem Management models, you manage problems and problem tasks in the classic UI16 experience, rather than in Service Operations Workspace.

Service Operations Workspace 6.x is based on the Xanadu release and it supports Problem Management models.

-   **[Shortcuts for creating fix tasks from a problem](https://servicenow-staging.fluidtopics.net/access?context=problem-sow&family=xanadu&ft:locale=en-US)**

Use the following shortcuts from the **Overview** tab of a problem:

    -   **Create defect** \(part of Agile Development 2.0\)
    -   **Create enhancement** \(part of Agile Development 2.0\)
    -   **Create improvement initiative** \(part of Continual Improvement Management\)
-   **[Guided tours](https://servicenow-staging.fluidtopics.net/access?context=explore-sow&family=xanadu&ft:locale=en-US)**

Learn about Service Operations Workspace for ITSM through a sequence of interactive steps that guide you through a specific concept or process.

Starting in version 6.1, the following guided tours are available:

    -   Overview of the PAR dashboard
    -   Overview of the various tabs and actions of an incident record page.
    -   Generate and download a post incident report for sharing it with all the stakeholders.
    -   Overview of the various tabs and actions of a problem record page.
    -   Get tailored recommendations for problems
    -   Get tailored recommendations for interactions
    -   Get tailored recommendations for requests
-   **[Add approvers to approve a request](https://servicenow-staging.fluidtopics.net/access?context=add-approvers-request-sow&family=xanadu&ft:locale=en-US)**

Starting in version 6.1, to expedite the process and effectively meet the user's request, you can add one or more approvers to the request or to a specific request item. This helps to streamline the approval workflow and ensure that the user's needs are fulfilled quickly and efficiently.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[User role for service desk agents](https://servicenow-staging.fluidtopics.net/access?context=roles-in-sow&family=yokohama&ft:locale=en-US)**

Enable tier 1 service desk agents to quickly gather and verify information by granting the sn\_service\_desk\_agent role, which is accessible when the ITSM Roles plugin \(com.snc.itsm.roles\) is installed.

The sn\_service\_desk\_agent role can be used starting with Service Operations Workspace version 6.1 with the Yokohama release.

-   **[Incident management configuration changes in the Service Operations Workspace Admin Center](https://servicenow-staging.fluidtopics.net/access?context=manage-admin-console-sow-itsm&family=yokohama&ft:locale=en-US)**

The Incident record of the Incident Management section in the Service Operations Workspace Admin Center has the following enhancements:

    -   Configure and use response templates to quickly respond to incidents.
    -   Configure additional properties to control incident features such as auto-closing incidents and copying or creating child incidents.
-   **[Reopen an incident in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=reopen-incident-sow&family=yokohama&ft:locale=en-US)**

Enable agents with incident write access, callers, or end user who opened the incident to reopen a resolved incident.

-   **[List page enhancements](https://servicenow-staging.fluidtopics.net/access?context=work-incident-list-page-sow&family=yokohama&ft:locale=en-US)**

The Service Operations Workspace list page has the following enhancements:

    -   Ability to assign the incident record to yourself if you’re the logged-in user or to reassign it to another user or assignment group.
    -   An animated dot symbol that indicates whether a list has been customized.
-   **[Major incident management record page enhancements](https://servicenow-staging.fluidtopics.net/access?context=communicating-with-stakeholders-sow&family=yokohama&ft:locale=en-US)**

Enhance incident and major incident-related communications including ad hoc communications and major incident playbooks in SOW by adding DEX Desktop Assistant as a channel.

-   **[Direct approvals in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=view-approvals-sow&family=yokohama&ft:locale=en-US)**

Service desk agent can approve records directly within the SOW without having to navigate to the Core UI. By approving records from the SOW, you can reduce response times, and ensure quick resolution of the tasks.

-   **[Automatically close an interaction in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=automatically-close-interaction-sow&family=yokohama&ft:locale=en-US)**

Interactions are now automatically closed when the associated incident is resolved, streamlining the workflow and ensuring consistent status updates.

-   **[Enhanced side panel features](https://servicenow-staging.fluidtopics.net/access?context=get-field-recommendations&family=yokohama&ft:locale=en-US)**

    -   Access the Recommended Actions and AI Search features from the contextual side panel for request items and catalog tasks.
    -   Determine the order of the items in the contextual side panel.
The Recommended Actions and AI Search features are now available in the contextual side panel for both request Items and catalog tasks.

-   **[Enable email redirection to SOW from SOW Admin Center](https://servicenow-staging.fluidtopics.net/access?context=manage-admin-console-sow-itsm&family=yokohama&ft:locale=en-US)**

Stay within the SOW and work on your tasks more efficiently by enabling email redirection. By enabling email redirection within the SOW Admin Center, you can simplify communication management, enabling the users to stay within the SOW and focus on their tasks without interruption.

-   **[Initiate a chat from Sidebar in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=initate-sidebar-chat-sow&family=yokohama&ft:locale=en-US)**

Use Slack as a primary mode of communication from the Sidebar so you can send direct messages to users without having to leave the SOW.

-   **[View the device health of user assets](https://servicenow-staging.fluidtopics.net/access?context=work-on-interaction-sow&family=yokohama&ft:locale=en-US)**

DEX is integrated with SOW to monitor CIs or assets associated with SOW records such as incidents and interactions to determine the health of devices. You can view the device health information of the user's assets on the Record information side panel of the incident and interactions record page. This feature is available only if the DEX plugin \[sn\_dex\] is installed and DEX monitoring is enabled for the asset.

-   **[Using MRA Async for adding child incident, affected CIs, impacted services and assets](https://servicenow-staging.fluidtopics.net/access?context=view-update-inc-overview-tab&family=yokohama&ft:locale=en-US)**

When adding a list containing more than 50 child incidents, affected CIs, impacted services or assets from the **Overview** tab or **Related records** tab of an incident or problem record, the Multiple Record Associator \(MRA\) component batch processes in async and helps adding them in background thereby increasing the overall performance of the system. This feature works only if the number of items to be added is more than 50 as the **async Threshold** configuration property is set to 50.

-   **[Viewing the device health of the user assets](https://servicenow-staging.fluidtopics.net/access?context=work-on-interaction-sow&family=yokohama&ft:locale=en-US)**

View the device health information of the user's assets from the Assigned assets section on the Record information side panel of the incident and interactions record page. This helps in providing a quick resolution to the user. This feature is available only if the DEX plugin \[sn\_dex\] is installed and DEX monitoring is enabled for the asset.

-   **[Guided tours for SOW](https://servicenow-staging.fluidtopics.net/access?context=play-guided-tour-sow&family=yokohama&ft:locale=en-US)**

Learn about Service Operations Workspace for ITSM through a sequence of interactive steps that guide you through a specific concept or process.

The following guided tours are available:

    -   Create an incident task
    -   Overview of the Interaction record in SOW
-   **[Enhanced security model adoption in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=components-installed-investigate&family=yokohama&ft:locale=en-US)**

Help prevent unauthorized access to the tables of the following applications with Deny-Unless ACLs:

    -   Metrics and CI actions framework
    -   Remedial actions framework
    -   Agent client collector for investigation
    -   Microsoft Endpoint Configuration Manager for Investigation
A Deny-Unless authentication ACL restricts access for a non-authenticated user, such as a public role user. Without access, the user can't perform any actions on the tables related to the above mentioned applications, including reading, writing, deleting, creating, or accessing the report view. This feature is available to both new \(zboot\) and upgrade instances.

-   **[Known error article for a problem](https://servicenow-staging.fluidtopics.net/access?context=work-on-problem-sow&family=yokohama&ft:locale=en-US)**

Starting in version 7.1, share the workaround for a problem and deflect additional incidents by creating a known error article for the problem.

-   **[On-Call Scheduling configurations in Admin Center](https://servicenow-staging.fluidtopics.net/access?context=manage-admin-console-sow-itsm&family=yokohama&ft:locale=en-US)**

Starting in version 7.1, use the simplified navigation from Admin Center to manage configurations for On-Call Scheduling in Service Operations Workspace for ITSM. It improves the administrator's experience.

-   **[Configure Notify in SOW](https://servicenow-staging.fluidtopics.net/access?context=configure-notify-sow&family=yokohama&ft:locale=en-US)**

Configure the provider preferences for Notify to manage the conference calls in Service Operations Workspace.

-   **[Create CAB meetings in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=cm-create-cab-meeting-sow&family=yokohama&ft:locale=en-US)**

Define and create Change Advisory Board \(CAB\) meetings, invite attendees and dynamically populate agenda items for each meeting in Service Operations Workspace.

Run CAB meetings through CAB Workbench, available within Service Operations Workspace to review and authorize change requests. For more information, see [Conduct a CAB meeting in the CAB workbench](https://servicenow-staging.fluidtopics.net/access?context=cm-manage-cab-meeting-workbench-sow&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **[Configuring Notify in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=configure-notify-sow&family=zurich&ft:locale=en-US)**

Configure Notify with Microsoft Teams SOW in Admin Center using the guided setup.

-   **[Visual indicators for unread messages](https://servicenow-staging.fluidtopics.net/access?context=sow-itsm-workspace-chat-session-tabs-configure&family=zurich&ft:locale=en-US)**

To help agents maintain the Service Level Agreement \(SLA\) for chats, visual indicators are available on chat session tabs in the SOW. These indicators include color codes, where tabs with unread messages are highlighted in different colors. Inactive tabs display a purple background color to indicate that a message has been received. Tab colors shift to yellow and then to red to highlight critical wait times. These enhancements aim to improve customer service by ensuring quick response time, increase productivity by helping agents manage multiple chats more effectively, and reduce stress by providing clear visual cues, ultimately leading to better SLA compliance and higher service quality.

-   **[Resize modal in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=view-update-inc-overview-tab&family=zurich&ft:locale=en-US)**

Optimize your viewing experience by resizing the following modals in SOW:

    -   Copy incident
    -   Report knowledge gap
    -   Reopen incident
-   **[Add similar incidents to major incident record](https://servicenow-staging.fluidtopics.net/access?context=managing-major-incident-sow&family=zurich&ft:locale=en-US)**

Find multiple similar incidents and add them as child incidents to a major incident or major incident candidate record from the child incident related list in the **Related records** tab of the major incident record. Similar incidents are retrieved based on the similarity solution definition that can be configured to train on various fields such as **Short description** and **Description**. Adding the similar incidents as child incidents to the major incident record ensures avoiding the creation of multiple major incident records for the same issue.

-   **[On-Call Scheduling enhancements in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=work-on-escalation-trigger-rules-and-policies-in-sow&family=zurich&ft:locale=en-US)**

On-call scheduling in SOW has the following enhancements:

    -   The On-call trigger rule page is enhanced to support and select subflows.
    -   The On-call trigger rule page is enhanced for supporting re-triggering escalations on configured fields such as Priority. Re-triggering is enabled whenever the value in the configured field changes.
    -   Configure custom providers as channels for on-call escalation notifications.
    -   Send the on-call escalations notifications to all stakeholders when any of the record fields configured using the on-call trigger rules are modified.
-   **[Auto-dismiss the alerts and notification in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=configure-alerts-auto-dismiss-sow&family=zurich&ft:locale=en-US)**

Configure the alerts and notifications in SOW to automatically dismiss within the specified time. Auto-dismissal of the alert notification reduces the user effort in manually dismissing the notification. By default, the base system has the following settings:

    -   Auto-dismiss is turned on for alert notification of type info, positive \(success\) and low and has the timeout value of three seconds.
    -   Auto-dismiss is turned off for alert notification of type critical, high, moderate, and warning.
    -   The time label is turned off and only a visual time indicator is displayed.
    -   The alert notification content is expanded.
-   **[DEX and SO view in the investigate tab](https://servicenow-staging.fluidtopics.net/access?context=dex-so-metric-views-investigate-tab&family=zurich&ft:locale=en-US)**

Based on the Configuration Item \(CI\) selected in the **Investigate** tab and the rules defined in the **Investigate CI Experience Rules** \(**sn\_sow\_investigate\_ci\_ux\_rule**\) table, the Investigate tab displays the CI metrics in the UI experience dashboard view for the different CI classes:

    -   DEX view - Displayed for the cmdb\_ci\_computer CI class.
    -   SO view - Displayed for the cmdb\_ci\_service class.
You can select both the affected CIs including service and service offering and caller CIs.

-   **[SOW record page enhancements](https://servicenow-staging.fluidtopics.net/access?context=view-update-inc-overview-tab&family=zurich&ft:locale=en-US)**

The SOW record page has the following enhancements:

    -   Add a clickable URL to the Summary section on the **Overview** tab of an incident record, enhancing navigation and reference capabilities. The Overview page supports URL type of field in read-only mode.
    -   Perform various DEX actions on a CI using actions from the Action library in the contextual side panel of the SOW record page.
    -   Manage user actions on the reference fields of a SOW record page with the following glide list actions:
        -   Add me - Add the logged in user to the field.
        -   Remove me - Remove the logged in user from the field.
        -   Add multiple users - Add multiple users to the field.
        -   Add multiple records - Add multiple records to the field.
-   **[View recent tasks in a knowledge article record](https://servicenow-staging.fluidtopics.net/access?context=work-knowledge-article&family=zurich&ft:locale=en-US)**

Configure the **Display recent task for knowledge article** \(**glide.knowman.recent\_task.display**\) system property to view the recent task records to which the knowledge article is recently attached. You can select the task record link to open the task record in a new tab with the workspace view.

-   **[Introduction of Granular Admin roles in SOW](https://servicenow-staging.fluidtopics.net/access?context=roles-in-sow&family=zurich&ft:locale=en-US)**

The following granular admin roles are introduced in SOW:

    -   sn\_sow\_admin.sn\_sow\_admin: Provides access to SOW Admin Center page for SOW configurations. Admins can use the role to configure SOW features and maintain organizational policies.
    -   sn\_sow\_inc\_sn\_incident\_sow\_admin: Provides access to SOW Admin Center pages for configurations related to Incident Management features.
    -   sn\_sow\_mim.sn\_mim\_sow\_admin: Provides access to the SOW Admin Center pages for configurations related to Major Incident Management \(MIM\) features.
    -   sn\_sow\_on\_call.sn\_on\_call\_sow\_admin: Provides access to the SOW Admin Center pages for On-Call Scheduling configurations.
    -   sn\_sow\_problem.sn\_problem\_sow\_admin: Provides access to the SOW Admin Center pages for Problem Management configurations.
-   **[View conflicts in the change request form](https://servicenow-staging.fluidtopics.net/access?context=create-change-sow&family=zurich&ft:locale=en-US)**

The improved schedule and conflicts section added in the change request form displays the scheduling conflicts for a change request. If a scheduling conflict exists, conflict detection also provides details of any related blackout or maintenance schedules and other active change requests to determine the scheduling conflict. You can use the resulting information to review and modify the change request details to eliminate conflicts. You can also manually check and manage conflicts.

For more information on conflict detection, see [Conflict detection](https://servicenow-staging.fluidtopics.net/access?context=c_ConflictDetection&family=zurich&ft:locale=en-US).

-   **[Monthly roster rotation for an on-call schedule](https://servicenow-staging.fluidtopics.net/access?context=create-a-schedule-in-sow&family=zurich&ft:locale=en-US)**

Specify how the roster rotation should happen monthly for an on-call schedule. This option is available only for the 2024 schedule engine.

-   **[Interaction wrap up with modeless dialog](https://servicenow-staging.fluidtopics.net/access?context=interaction-wrap-up-sow&family=zurich&ft:locale=en-US)**

Provide agents with dedicated time after each call or chat to finalize the interaction details and wrap up their work before starting a new conversation.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Service Operations Workspace for ITSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Landing page configurations from Admin Center](https://servicenow-staging.fluidtopics.net/access?context=manage-admin-console-sow-itsm&family=xanadu&ft:locale=en-US)**

All landing page configurations such as the landing page redirection, donut configurations, and so on are grouped under the **Landing Page Configurations** section of the **Configurations** tab.

-   **[Reordering of modules on the left navigation pane](https://servicenow-staging.fluidtopics.net/access?context=reorder-left-navigation-pane-modules&family=xanadu&ft:locale=en-US)**

The left navigation pane modules, such as Inbox and Lists, are reordered for improved access to these modules.

-   **[Role to create a request from interaction and incident records](https://servicenow-staging.fluidtopics.net/access?context=create-catalog-request-sow&family=xanadu&ft:locale=en-US)**

A user should now have either the itil role or sn\_request\_write role to create a request from interaction and incident records. Before Xanadu, users needed the interaction\_agent role to create the request.

-   **[DevOps data in change request](https://servicenow-staging.fluidtopics.net/access?context=create-change-sow&family=xanadu&ft:locale=en-US)**
    -   View, add, and edit DevOps data in a manually created change request in Service Operations Workspace for ITSM for a unified change request experience in the DevOps Change Workspace and Service Operations Workspace for ITSM.
    -   Starting in version 6.1, view, add, and edit work items data in a manually created DevOps change request in Service Operations Workspace for ITSM.
-   **[Creating change requests from problem records](https://servicenow-staging.fluidtopics.net/access?context=work-on-problem-sow&family=xanadu&ft:locale=en-US)**

You can create additional change requests, because the action is no longer hidden after it has been used once.

-   **[Inline editing in the __Problem Tasks__ tab](https://servicenow-staging.fluidtopics.net/access?context=lists-inline-edit&family=xanadu&ft:locale=en-US)**

Change a field in the problem tasks list instead of opening the record and changing it on the form.

-   **[Sidebar enhancements for incidents](https://servicenow-staging.fluidtopics.net/access?context=using-sidebar&family=xanadu&ft:locale=en-US)**

The sidebar will now display recommendations for users who can assist agents in resolving incidents or tasks. A standard set of recommendations are provided to enhance the support workflow.

ITSM Pro provides the customized recommendations using an AI-based algorithm, ensuring that the most appropriate users are suggested to assist with the task.

The group addition feature offers the ability to add entire groups to a conversation. By default, all members of a group will be included in the conversation. For groups with designated on-call members, only those members are added to the conversation, enabling for more focused and efficient communication.

-   **[Reflow for Configurable Workspace](https://servicenow-staging.fluidtopics.net/access?context=auto-reflow&family=xanadu&ft:locale=en-US)**

Service Operations Workspace for ITSM configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For more information, see the Accessibility information section that follows.

-   **[Email notification redirection behavior in Problem Management](https://servicenow-staging.fluidtopics.net/access?context=configure-notifcations-sow-itsm&family=xanadu&ft:locale=en-US)**

When users select the problem record link in their email notifications, they can be redirected to the problem record in Service Operations Workspace instead of the classic UI16 experience. The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.

-   **[Work notes in Compose section](https://servicenow-staging.fluidtopics.net/access?context=view-update-inc-overview-tab&family=xanadu&ft:locale=en-US)**

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


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Incident record page changes](https://servicenow-staging.fluidtopics.net/access?context=view-inc-record-info-contextual-sidepanel&family=yokohama&ft:locale=en-US)**

The Incident record page has the following changes:

    -   The caller card is placed first on the Record information side panel for tier 1 agents.
    -   The origin card itself is no longer clickable to reduce usability issues with the card and its clickable elements.
-   **[Reference field behavior changes in SOW](https://servicenow-staging.fluidtopics.net/access?context=view-update-inc-overview-tab&family=yokohama&ft:locale=en-US)**

Selecting any reference field in SOW now displays only the recent selection values instead of automatic searching and displaying the results of the field values available in the system. This change increases the overall performance of the reference fields. By default, this change is enabled. To revert this change, set the **Reference search on click** \(**ref\_search\_on\_click**\) UX page property to set to `true`.

-   **[Viewing Assign to me option](https://servicenow-staging.fluidtopics.net/access?context=users-sow-itsm&family=yokohama&ft:locale=en-US)**

Users with the incident\_read role can no longer view the **Assign to me** option for an incident record.

-   **Email component issues on SOW Incident**

Email components are now accurately displayed for SOW Incident when the email is selected from the activity stream, stacked view, or email template is applied.

-   **Resetting filter conditions**

Filter conditions are now reset when switched from one related list to another related list.

-   **Saving interaction record loads recent tasks**

When a new interaction record is created and saved, the sidebar now loads record Information instead of recent Tasks.

-   **[Problem Management state transitions](https://servicenow-staging.fluidtopics.net/access?context=understanding-state-mgmt-transitions&family=yokohama&ft:locale=en-US)**

Sections that are configured to be expanded now automatically expand when you transition to a new state, without requiring a page reload.

-   **[GenAI email templates for communication](https://servicenow-staging.fluidtopics.net/access?context=compose-communication-mim-sow&family=yokohama&ft:locale=en-US)**

Use the GenAI capabilities for composing email with GenAI email templates in all major incident communications. The GenAI email templates are visible in a separate section when the email templates field is selected and the following conditions are met:

    -   Any GenAI variable is available in the email templates.
    -   Now Assist for ITSM is installed and activated.
    -   GenAI skills are enabled.
    -   User have the required roles to execute the GenAI skills.
-   **[Close resolved incident](https://servicenow-staging.fluidtopics.net/access?context=close-resolved-incident-sow&family=yokohama&ft:locale=en-US)**

Close an incident in **Resolved** state using the itil\_admin user role.

-   **[Resize modals on the SRP and list pages](https://servicenow-staging.fluidtopics.net/access?context=srp-service-operations-workspace&family=yokohama&ft:locale=en-US)**

Ensure flexibility and efficiency by enabling users to resize the modals on the SOW SRP and list pages. This helps in adjusting screen space allocation, enabling multi-tasking, and optimizing content visibility for different tasks and screen sizes. 


</td></tr><tr><td>

Zurich

</td><td>

-   **[Configure help and order of the remedial action parameters](https://servicenow-staging.fluidtopics.net/access?context=components-installed-with-remediation-fw&family=zurich&ft:locale=en-US)**

Configure the **Help** and **Order** fields for the remedial action parameters on the Remedial action parameter \[sn\_reacf\_remedial\_action\_parameter\] table if you have the Remedial action admin\[sn\_reacf.sn\_remedial\_action\_admin\] user role.

-   **[List page enhancements in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=work-incident-list-page-sow&family=zurich&ft:locale=en-US)**

The list page in SOW has the following enhancements:

    -   The related lists in the **Related records** tab of the SOW record pages, including those within the record pages as well such as Recent Incidents or Assigned Assets, are updated with the record list bundle. This update provides them with the same appearance, functionality, and user experience as the SOW list page.
    -   The related lists in the **Related records** tab of the SOW record pages, including the Multi Record Associator \(MRA\) list, as well as the related lists within the record pages such as Recent Incidents or Assigned Assets, now support the fuzzy count UX page property. You can configure a default value that is applicable to the list for all tables or a value for a specific table such as incident thereby improving the list page performance.
-   **[Dependency view changes for reference fields](https://servicenow-staging.fluidtopics.net/access?context=view-update-inc-overview-tab&family=zurich&ft:locale=en-US)**

Selecting the dependency view for the following fields in the incident, problem, change, and request records, opens a unified CMDB map in a new tab within the workspace view instead of a new browser tab:

    -   Configuration item
    -   Service
    -   Service offering
-   **[Propose a standard change template](https://servicenow-staging.fluidtopics.net/access?context=propose-standard-change-sow&family=zurich&ft:locale=en-US)**

As a user with the itil role, you can create a standard change template proposal from any change record in SOW.

-   **[Service Operations Workspace access for an on-call shift administrator](https://servicenow-staging.fluidtopics.net/access?context=roles-in-sow&family=zurich&ft:locale=en-US)**

Starting in version 8.2, a user with the rota\_admin role can access Teams, Schedules, and Home pages in SOW.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Service Operations Workspace for ITSM features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Service Operations Workspace for ITSM features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Service Operations Workspace for ITSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

Service Operations Workspace for ITSM is active by default and its default version is 5.0 in Xanadu. When you upgrade from any previous release to Xanadu from ServiceNow Store, Service Operations Workspace for ITSM 5.0 is automatically installed.

</td></tr><tr><td>

Yokohama

</td><td>

Service Operations Workspace for ITSM is active by default and its default version is 7.0 in Yokohama. When you upgrade from any previous release to Yokohama from the ServiceNow Store, Service Operations Workspace for ITSM 7.0 is automatically installed.

</td></tr><tr><td>

Zurich

</td><td>

Service Operations Workspace for ITSM is active by default and its default version is 8.0 in Zurich. When you upgrade from any previous release to Zurich from the ServiceNow Store, Service Operations Workspace for ITSM 8.0 is automatically installed.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Service Operations Workspace for ITSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Service Operations Workspace for ITSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Service Operations Workspace for ITSM, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://servicenow-staging.fluidtopics.net/access?context=auto-reflow&family=xanadu&ft:locale=en-US) for details.

-   **Resize text**

Starting in version 6.1, text size can be increased to 400% through your browser settings without loss of content or functionality for Incident Management and Password Reset in SOW.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Reflow**

The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [\[Placeholder link text to key bundle-platux.auto-reflow\]](https://servicenow-staging.fluidtopics.net/access?context=auto-reflow&family=zurich&ft:locale=en-US) for details.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Service Operations Workspace for ITSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Service Operations Workspace for ITSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

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

 See [Service Operations Workspace for ITSM](https://servicenow-staging.fluidtopics.net/access?context=sow-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Streamline task management and reduce response times by approving the request, request item, catalog task, change request, and standard change proposal records directly from Service Operations Workspace \(SOW\).
-   Quickly find details helpful in resolving issues by using Recommended Actions and AI Search for request items and catalog items.
-   Enable agents with incident write access, callers, and end users who opened the incident to reopen a resolved incident from the incident record page in Service Operations Workspace.
-   Configure response templates and incident management properties from the Service Operations Workspace Admin Center.
-   Configure and use DEX Desktop Assistant as a channel in all incident and major incident-related communications.
-   Starting in version 7.1, you can do the following:
    -   Restrict unauthorized access to Incident Management in Service Operations Workspace using deny ACLs.
    -   Compose email using GenAI email templates for all major incident communications.
    -   Close a resolved incident with itil\_admin user role.
    -   Share the workaround for a problem and deflect additional incidents.
    -   Configure the On-Call Scheduling features from Service Operations Workspace Admin Center.
    -   Use visual indicators like colors and icons on chat session tabs to notify agents about unread messages to maintain the SLA for the chats in Service Operations Workspace.
    -   Configure the provider for Notify in SOW.
    -   Agents can see a transcript of voice calls while interacting with customers in Service Operations Workspace.
    -   Create Change Advisory Board \(CAB\) meetings and run them through CAB Workbench in Service Operations Workspace.

 See [Service Operations Workspace for ITSM](https://servicenow-staging.fluidtopics.net/access?context=sow-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Propose a standard change template from a change record in Service Operations Workspace \(SOW\).
-   Experience enhanced meeting and pagination controls in the Change Advisory board \(CAB\) workbench.
-   Configure the Microsoft Teams integration with Notify in SOW Admin Center.
-   Use visual indicators like colors and icons on chat session tabs to notify agents about unread messages to maintain the Service Level Agreement \(SLA\) for the chats in SOW.
-   Optimize your viewing experience by resizing the modals in SOW.
-   Find similar incidents and add them as child incidents to a major incident record.
-   Support subflows in the On-Call trigger rule configurations.
-   Configure the alerts and notifications in SOW to automatically dismiss within the specified time.
-   View the dependency map for reference fields in a separate tab within the workspace.
-   Starting in version 8.2, you can do the following:
    -   Analyze the metrics for configuration items \(CIs\) in the Digital End-User Experience \(DEX\) and Service Observability \(SO\) UI dashboard view on the Investigate tab of an incident record.
    -   Access and configure SOW from the Admin Center using granular feature admin roles.
    -   View the recent task records to which the knowledge article is attached.
    -   Manage user actions on the reference fields with the glide list action.
    -   Perform DEX actions on a Configuration Item \(CI\) using the Action library from the contextual panel of the record page.
    -   View the details of conflicts detected, and manually run conflict detection in the change request form.
    -   Configure monthly roster rotation for an on-call schedule.
    -   As an on-call shift administrator with the rota\_admin role, access Teams, Schedules, and Home pages in SOW.

 See [Service Operations Workspace for ITSM](https://servicenow-staging.fluidtopics.net/access?context=sow-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

