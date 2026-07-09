---
title: Service Operations Workspace for ITSM release notes
description: The ServiceNow Service Operations Workspace application is a configurable workspace that provides a unified agent experience for multiple IT Service Management and IT Operations Management capabilities. Service Operations Workspace for IT Service Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 10
---

# Service Operations Workspace for ITSM release notes

The ServiceNow® Service Operations Workspace application is a configurable workspace that provides a unified agent experience for multiple IT Service Management and IT Operations Management capabilities. Service Operations Workspace for IT Service Management was enhanced and updated in the Yokohama release.

## Service Operations Workspace highlights for the Yokohama release

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

See [Service Operations Workspace for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/sow-landing-page.md) for more information.

**Important:** Service Operations Workspace is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Service Operations Workspace to Yokohama

Ensure that the following applications have compatible upgraded versions:

-   Service Operations Workspace ITSM Applications application \(sn\_sow\_itsm\_cont\)
-   Service Operations Workspace ITOM Applications application \(sn\_sow\_itom\_cont\)

For more information on compatible versions, see [Version compatibility between Service Operations Workspace for ITSM and Service Operations Workspace ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/sow-itsm-itom-version.md).

## New in the Yokohama release

-   **[User role for service desk agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/roles-in-sow.md)**

    Enable tier 1 service desk agents to quickly gather and verify information by granting the sn\_service\_desk\_agent role, which is accessible when the ITSM Roles plugin \(com.snc.itsm.roles\) is installed.

    The sn\_service\_desk\_agent role can be used starting with Service Operations Workspace version 6.1 with the Yokohama release.

-   **[Incident management configuration changes in the Service Operations Workspace Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/manage-admin-console-sow-itsm.md)**

    The Incident record of the Incident Management section in the Service Operations Workspace Admin Center has the following enhancements:

    -   Configure and use response templates to quickly respond to incidents.
    -   Configure additional properties to control incident features such as auto-closing incidents and copying or creating child incidents.
-   **[Reopen an incident in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/reopen-incident-sow.md)**

    Enable agents with incident write access, callers, or end user who opened the incident to reopen a resolved incident.

-   **[List page enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/work-incident-list-page-sow.md)**

    The Service Operations Workspace list page has the following enhancements:

    -   Ability to assign the incident record to yourself if you’re the logged-in user or to reassign it to another user or assignment group.
    -   An animated dot symbol that indicates whether a list has been customized.
-   **[Major incident management record page enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/communicating-with-stakeholders-sow.md)**

    Enhance incident and major incident-related communications including ad hoc communications and major incident playbooks in SOW by adding DEX Desktop Assistant as a channel.

-   **[Direct approvals in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/view-approvals-sow.md)**

    Service desk agent can approve records directly within the SOW without having to navigate to the Core UI. By approving records from the SOW, you can reduce response times, and ensure quick resolution of the tasks.

-   **[Automatically close an interaction in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/automatically-close-interaction-sow.md)**

    Interactions are now automatically closed when the associated incident is resolved, streamlining the workflow and ensuring consistent status updates.

-   **[Enhanced side panel features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/get-field-recommendations.md)**

    -   Access the Recommended Actions and AI Search features from the contextual side panel for request items and catalog tasks.
    -   Determine the order of the items in the contextual side panel.
    The Recommended Actions and AI Search features are now available in the contextual side panel for both request Items and catalog tasks.

-   **[Enable email redirection to SOW from SOW Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/manage-admin-console-sow-itsm.md)**

    Stay within the SOW and work on your tasks more efficiently by enabling email redirection. By enabling email redirection within the SOW Admin Center, you can simplify communication management, enabling the users to stay within the SOW and focus on their tasks without interruption.

-   **[Initiate a chat from Sidebar in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/initate-sidebar-chat-sow.md)**

    Use Slack as a primary mode of communication from the Sidebar so you can send direct messages to users without having to leave the SOW.

-   **[View the device health of user assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/work-on-interaction-sow.md)**

    DEX is integrated with SOW to monitor CIs or assets associated with SOW records such as incidents and interactions to determine the health of devices. You can view the device health information of the user's assets on the Record information side panel of the incident and interactions record page. This feature is available only if the DEX plugin \[sn\_dex\] is installed and DEX monitoring is enabled for the asset.

-   **[Using MRA Async for adding child incident, affected CIs, impacted services and assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/view-update-inc-overview-tab.md)**

    When adding a list containing more than 50 child incidents, affected CIs, impacted services or assets from the **Overview** tab or **Related records** tab of an incident or problem record, the Multiple Record Associator \(MRA\) component batch processes in async and helps adding them in background thereby increasing the overall performance of the system. This feature works only if the number of items to be added is more than 50 as the **async Threshold** configuration property is set to 50.

-   **[Viewing the device health of the user assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/work-on-interaction-sow.md)**

    View the device health information of the user's assets from the Assigned assets section on the Record information side panel of the incident and interactions record page. This helps in providing a quick resolution to the user. This feature is available only if the DEX plugin \[sn\_dex\] is installed and DEX monitoring is enabled for the asset.

-   **[Guided tours for SOW](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/play-guided-tour-sow.md)**

    Learn about Service Operations Workspace for ITSM through a sequence of interactive steps that guide you through a specific concept or process.

    The following guided tours are available:

    -   Create an incident task
    -   Overview of the Interaction record in SOW
-   **[Enhanced security model adoption in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/components-installed-investigate.md)**

    Help prevent unauthorized access to the tables of the following applications with Deny-Unless ACLs:

    -   Metrics and CI actions framework
    -   Remedial actions framework
    -   Agent client collector for investigation
    -   Microsoft Endpoint Configuration Manager for Investigation
    A Deny-Unless authentication ACL restricts access for a non-authenticated user, such as a public role user. Without access, the user can't perform any actions on the tables related to the above mentioned applications, including reading, writing, deleting, creating, or accessing the report view. This feature is available to both new \(zboot\) and upgrade instances.

-   **[Known error article for a problem](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/work-on-problem-sow.md)**

    Starting in version 7.1, share the workaround for a problem and deflect additional incidents by creating a known error article for the problem.

-   **[On-Call Scheduling configurations in Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/manage-admin-console-sow-itsm.md)**

    Starting in version 7.1, use the simplified navigation from Admin Center to manage configurations for On-Call Scheduling in Service Operations Workspace for ITSM. It improves the administrator's experience.

-   **[Configure Notify in SOW](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/configure-notify-sow.md)**

    Configure the provider preferences for Notify to manage the conference calls in Service Operations Workspace.

-   **[Create CAB meetings in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/cm-create-cab-meeting-sow.md)**

    Define and create Change Advisory Board \(CAB\) meetings, invite attendees and dynamically populate agenda items for each meeting in Service Operations Workspace.

    Run CAB meetings through CAB Workbench, available within Service Operations Workspace to review and authorize change requests. For more information, see [Conduct a CAB meeting in the CAB workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/cm-manage-cab-meeting-workbench-sow.md).


## Changed in this release

-   **[Incident record page changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/view-inc-record-info-contextual-sidepanel.md)**

    The Incident record page has the following changes:

    -   The caller card is placed first on the Record information side panel for tier 1 agents.
    -   The origin card itself is no longer clickable to reduce usability issues with the card and its clickable elements.
-   **[Reference field behavior changes in SOW](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/view-update-inc-overview-tab.md)**

    Selecting any reference field in SOW now displays only the recent selection values instead of automatic searching and displaying the results of the field values available in the system. This change increases the overall performance of the reference fields. By default, this change is enabled. To revert this change, set the **Reference search on click** \(**ref\_search\_on\_click**\) UX page property to set to `true`.

-   **[Viewing Assign to me option](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/users-sow-itsm.md)**

    Users with the incident\_read role can no longer view the **Assign to me** option for an incident record.

-   **Email component issues on SOW Incident**

    Email components are now accurately displayed for SOW Incident when the email is selected from the activity stream, stacked view, or email template is applied.

-   **Resetting filter conditions**

    Filter conditions are now reset when switched from one related list to another related list.

-   **Saving interaction record loads recent tasks**

    When a new interaction record is created and saved, the sidebar now loads record Information instead of recent Tasks.

-   **[Problem Management state transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/understanding-state-mgmt-transitions.md)**

    Sections that are configured to be expanded now automatically expand when you transition to a new state, without requiring a page reload.

-   **[GenAI email templates for communication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/compose-communication-mim-sow.md)**

    Use the GenAI capabilities for composing email with GenAI email templates in all major incident communications. The GenAI email templates are visible in a separate section when the email templates field is selected and the following conditions are met:

    -   Any GenAI variable is available in the email templates.
    -   Now Assist for ITSM is installed and activated.
    -   GenAI skills are enabled.
    -   User have the required roles to execute the GenAI skills.
-   **[Close resolved incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/close-resolved-incident-sow.md)**

    Close an incident in **Resolved** state using the itil\_admin user role.

-   **[Resize modals on the SRP and list pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/srp-service-operations-workspace.md)**

    Ensure flexibility and efficiency by enabling users to resize the modals on the SOW SRP and list pages. This helps in adjusting screen space allocation, enabling multi-tasking, and optimizing content visibility for different tasks and screen sizes. 


## Activation information

Service Operations Workspace for ITSM is active by default and its default version is 7.0 in Yokohama. When you upgrade from any previous release to Yokohama from the ServiceNow Store, Service Operations Workspace for ITSM 7.0 is automatically installed.

## Related ServiceNow applications and features

-   **[Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/c_ITILChangeManagement.md)**

    Control the life cycle of a change and implement the change with minimum disruption to IT services.

-   **[Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/c_IncidentManagement.md)**

    Enable users to identify IT issues and log incidents through the Incident Management system. Efficiently track, classify, and prioritize incidents to work effectively toward their resolution.

-   **[Interaction Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/interaction-management.md)**

    Respond to an incoming chat, phone, walk-up, or messaging interaction quickly by using an interaction that provides a centralized location for all communication channels.

-   **[Notify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/notify-landing-page.md)**

    Provide support for SMS and voice channels on the platform to communicate with your team and customers.

-   **[On-Call Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/c_OnCallScheduling.md)**

    Identify available on-call members of a support group who can be contacted to resolve an issue.

-   **[Password Reset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/password-reset-landing-page.md)**

    The ServiceNow® Password Reset application enforces strong and secure passwords by enabling end users to reset or change their passwords either by using the self-service process or by requesting the assistance of a service desk agent.

-   **[Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/predictive-intelligence.md)**

    Use machine-learning algorithms to provide dynamic and contextual recommendations for resolving an incident.

-   **[Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/c_ProblemManagement.md)**

    Identify the root cause of recurring incidents or a major incident to help prevent them from happening again.

-   **[Recommended Actions for ITSM in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/recommended-actions-for-itsm-in-service-operations-workspace.md)**

    Get field recommendations and guidance in the side panel for the incident form in Service Operations Workspace.

-   **[Request Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/c_RequestManagement.md)**

    Initiate a catalog request flow from a different IT Service Management flow, such as an incident flow, by using catalog requests.

-   **[Service Level Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/service-level-mgmt-landing-page.md)**

    Access incident service level agreement \(SLA\) information on the Service Operations Workspace for ITSM landing page and incident record page.

-   **[Service Operations Workspace for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/sow-landing-page-itom.md)**

    Configure your operator experience through a unified interface for multiple ServiceNow® IT Operations Management workflows.

-   **[Walk-up Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/walkup-experience-landing-page.md)**

    Manage walk-up interactions and queues effortlessly by using Service Operations Workspace for ITSM.


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/it-service-management-rn-landing.md)

