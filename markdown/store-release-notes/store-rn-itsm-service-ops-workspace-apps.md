---
title: Service Operations Workspace ITSM Applications release notes
description: Version history for the Service Operations Workspace ITSM Applications on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-service-ops-workspace-apps.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 19
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# Service Operations Workspace ITSM Applications release notes

Version history for the Service Operations Workspace ITSM Applications on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 9.2.0 - June 2026**
    -   Changes:
        -   Updated plugin dependencies to ensure compatibility with the ServiceNow Australia and later releases.
        -   Minor defect fixes.
-   **Version 8.7.0 - June 2026**

    Changed: Updated plugin dependencies to ensure compatibility with the ServiceNow Zurich release.

-   **Version 9.1.1 - April 2026**
    -   Changed:
        -   Here is the text that goes in the SOW Apps listing page:Starting with the Australia release, SOW applications are reorganized as per the following application packages:
            -   SOW ITSM Applications \(Incident, Request\)
            -   SOW ITSM Advanced Applications \(Change, Problem, Major Incident Management \(MIM\), On-Call Scheduling, Walk-up Experience\)
        -   For existing customers:
            -   Family release upgrade: All applications will be automatically upgraded to the default version available in the Australia family release.
            -   Store version upgrade: Customers installing SOW 9.1 from the ServiceNow Store must install both application packages listed above.
-   **Version 8.6.0 - April 2026**
    -   New
        -   Agents can now add comments for catalog task records out-of-the-box
        -   Agents can now view an AI-generated summary of a request record \(requires Now Assist for ITSM\)
-   **Version 9.0.4 - March 2026**
    -   Incident Management for Service Operations Workspace
        -   New: Admins can redirect fulfiller users or user groups from Classic \(UI16\) module menus to the SOW equivalent experience.
    -   Problem Management for Service Operations Workspace
        -   New: Administrators can redirect fulfiller users or user groups from classic \(UI16\) module menus to the SOW equivalent experience.
    -   Change Management for Service Operations Workspace
        -   New:
            -   Administrators can redirect fulfiller users or user groups from classic \(UI16\) module menus to the SOW equivalent experience.
            -   Change Create - new landing page.
        -   Changed: Redirect from old create change landing page to new create change landing page.
-   **Version 8.4.0 - January 2026**

    New: Agents can review AI agent activity that has taken place on an incident record \(requires ITSM Pro+ subscription\).

-   **Version 8.2.4 - December 2025**
    -   Incident Management for Service Operations Workspace:
        -   New:
            -   Admins can delegate administration of Incident Management for SOW to another user/group with granular role support.
            -   Agents can instantly view service KPIs and device health within incident records, accelerating investigations and boosting productivity. \(requires DEX or ITOM Service Observability\)
            -   Agents can instantly see which KB articles resolved recent incidents, helping validate content impact and speed up investigations.
            -   Fulfillers will be able to View Transcripts and recording of completed calls in ServiceNow records for MS Teams
            -   On-call scheduling can rotate members on monthly schedule along with Daily and weekly
            -   With the new MS Teams Events API, meetings can be viewed and updated from MS Teams
        -   Fixed: Agents can now leverage out-of-the-box response templates on the incident form as the Form channel, which is required to view/select the response template in the side panel, was added to the templates.
    -   Interaction Management for Service Operations Workspace
        -   New:
            -   Admins can delegate administration of Interaction Management for SOW to another user/group with granular role support.
            -   Agents can use new modeless wrap up experience for Phone type interactions
        -   Changed: Agent chat performance has improved through the elimination of unnecessary backend calls.
    -   Problem Management for Service Operations Workspace
        -   New: Admins can delegate administration of Problem Management for SOW to another user/group with granular role support.
-   **Version 7.1.6 - December 2025**

    Changed: Fixed the issue with private sidebar discussion in the collaboration side panel. The private sidebar discussion will be hidden from unintended users.

-   **Version 8.1.0 - September 2025**

    New: Added Collaboration as a UIB component and enabled it in the component panel for use on any UIB page for call and chat features.

-   **Version 7.1.4 - September 2025**

    Fixed: Shift end is showing incorrectly on the Provide coverage modal when opened from shift or user span on the On-Call schedule calendar.

-   **Version 8.0.3 - August 2025**
    -   Incident Management for Service Operations Workspace:
        -   New:
            -   Admins can configure fuzzy counts for multi-record associator modal lists
            -   Admins can reference the SOW Incident record page view across other configurable workspaces \(e.g., CSM/FSM Workspace\)
            -   Agents can leverage Learning Enhanced Automation Playbooks within an incident \(ITOM Pro+ required\)
        -   Changed:
            -   Agents can leverage CMDB's Unified Map experience for viewing CI details and where it sits in their enterprise's digital estate
    -   Interaction Management for Service Operations Workspace
        -   New:
            -   Admins can enable/disable hiding the inbox upon work item acceptance from SOW Admin Center
            -   Admins can configure the information session tab settings for chat interactions in SOW Admin Center
    -   Major Incident Management for Service Operations Workspace
        -   New:
            -   Major Incident Managers and Responders can find and link similar incidents to the one they are actively working to identify the blast radius of the incident sooner
    -   Problem Management for Service Operations Workspace
        -   Changed:
            -   Selecting the dependency map view for the following fields opens a unified CMDB map in a new tab within the workspace view instead of a new browser tab:
                -   Configuration item
                -   Service
                -   Service offering
    -   Request Management for Service Operations Workspace
        -   New:
            -   Agents can view quick details about who is working on a catalog task record so that they can reach out to the assignee for any follow-ups
-   **Version 7.1.3 - August 2025**
    -   Fixed:
        -   Change Requests are not documented when created from Incident in SOW. Fixing this issue by linking the Change \(CHG\) number to the Incident in the RFC field.
        -   Fixing the issue to enable 'Copy Change' while the mandatory fields are not populated.
        -   When clicking on 'Go to CAB Meeting' on SOW Change sidebar, this navigates to UI16 CAB and not SOW CAB if installed.
        -   When creating a Change from a Problem record in SOW users should now be directed to the Create new Change page
        -   Method failing on table name exception is fixed.
        -   On the Change Overview page's summary section now supports dot walked fields in read only mode.
        -   In the CAB Meeting page the Restore or Make next agenda item buttons should no longer overlap the Agenda item description text.
        -   The Create new Change page should now always display cards for Models regardless of the Standard Change plugin being installed.
        -   Latest versions of team governance files are being moved to SRM scope so removed the old versions from admin experience scope.
        -   Fix the issue to enable button which was not visible on SOW workspace for Walk-up location kiosk records, for the 'Default view' in the UI action.
        -   Right colors are shown on the interaction tab as configured on the session tabs
-   **Version 6.1.7 - June 2025**
    -   New:
        -   Added support for GenAI features -
            -   Support email content generation for major incident with email templates using NowAssist.
            -   Make informed decisions on incidents by considering the requester's sentiments, sentiment trend and the reasoning behind them.
    -   Fixed:
        -   Visibility of email templates for recurring communications after composing once in the Communicate tab for major incidents in SOW.
        -   Visibility of email templates when the defined conditions are not met.
        -   Major Incident Process playbook executes even when proposed major incident is rejected.​
        -   Playbook isn't completed when Mark complete action is used in the PIR step.
        -   Playbook isn't cancelled when incident is cancelled.
-   **Version 7.1.0 - May 2025**
    -   Service Operations Workspace ITSM Admin Center
        -   New:
            -   Guided Setup for On-call configuration
            -   Ability to auto-discover service desk groups to assign role
            -   Support for configuring fuzzy count for list views
    -   Problem Management for Service Operations Workspace
        -   New:
            -   Ability to create known error article recommendation for a high impact problem On Call Scheduling for Service Operations Workspace
            -   Guided setup for on-call admin configurations Notify UI Components for Configurable Workspaces
    -   Guided setup for Notify admin configurations Meeting Watcher - UI Builder Data Resource
        -   New: Data Resource for UI Builder supporting the operations of Change Advisory Board \(CAB\) for Service Operations Workspace Meeting CAB
            -   Create and manage Change Advisory Board \(CAB\) meetings in SOW
            -   Run CAB meetings through CAB Workbench in SOW to review and authorize change requests
            -   Discuss agenda items through CAB workbench before and during the CAB meeting
    -   Incident Management for Service Operations Workspace
        -   New: Users with itil\_admin role can close resolved incidents
        -   Changed:
            -   Agents are alerted when an incident is reopened that contains child incidents. They are notified of child incidents being reopened as a part of a parent incident being reopened.
            -   Remedial action playbooks is updated to use Flow Engine v2
    -   Interaction Management for Service Operations Workspace
        -   New:
            -   Agents can be notified when end users post an update to a non-focused chat tab. They can further prioritize responding to waiting end users with tabs changing colors as they cross certain thresholds.
            -   Agents can leverage a unified, in-record interface for phone/call-based interactions
            -   Agents can focus on an accepted interaction with the inbox panel auto-hiding upon accept
-   **Version 6.1.5 - March 2025**

    No changes.

-   **Version 7.0.0 - February 2025**
    -   New:
        -   Improvements to incident and interaction management to improve agent productivity and streamline resolution.
        -   Improvements to problem management
        -   Support for My Approvals for change/request approvals, \(similar to UI16\) in SOW
        -   Improvements to SOW Admin Center
        -   Support for DEX as a communications channel in Major Incident Management
        -   Improvements to Mobile Agent
        -   Support for Slack in Sidebar
        -   Improvements to CAB workbench approvals for change management
        -   Improvements to enable NowAssist for change management
-   **Version 6.1.3 - January 2025**
    -   Fixed:
        -   Major Incident Management
            -   Communication tab fails to load data.
            -   Major incident proposal results in other jobs in event queue use proposing user for audit entries.
        -   Interaction.
            -   In SOW 6.0 and 6.1 versions, the short description and opened for fields are marked as mandatory for the interaction record. This version corrects the issue, ensuring that these fields are mandatory only in the Service Operations Workspace. The previous defect was causing problems when using the Interaction feature in HR or CSM applications.
            -   When associating records to Interactions via the Associate Record modal, records that were already linked to the Interaction were still available for selection. This defect has been fixed, and now those records are no longer selectable.
        -   Change Request Management
            -   The "View Activity" button on the Change Request Overview tab has been fixed. It will now correctly hide and show the Activity Stream.
-   **Version 5.1.1 - December 2024**
    -   Fixed:
        -   Incorrect shift times on the calendar
        -   Incorrect start and end time for conflict and coverage cards on Required Actions side panel tab
        -   Incorrect start and end time for absence cards on My Requests side panel tab
        -   Calendar doesn't load when the group manager approves absence requested for the days post DST
-   **Version 6.1.0 - November 2024**
    -   New:
        -   Configure the Interaction Management features from SOW admin center.
        -   Provide users with current resources for learning about SOW admin configuration.
        -   View the requester's device details from the record information card to quickly resolve hardware-related issues.
        -   Add one or more approvers to the request or a request item to speed up the process and fulfil the user's request more efficiently.
        -   Improve the system performance by configuring the count of number of incident records in the incident list page.
        -   Copy the sys ID or the URL of the incident from the incident list page to share with other agents, enabling quicker resolution of the issue.
        -   Chat or make calls to communicate with stakeholders using the Collaborate option in the contextual side panel of problem and problem task records.
        -   Configure the automatic closure of interaction record from an incident record.
        -   Flag the events on the activity stream of a major incident to add the events to the post incident report events timeline.
        -   View the post incident report information on the Post incident report tab with the Incident management granular roles.
        -   Add multiple related interaction records to an incident record.
        -   Define, customize, and apply tags to the activities in the activity streams of an incident record.
        -   Experience a clean UI with collapsible activity stream tiles.
        -   Resolve incident or support issues faster and more efficiently with response templates.
        -   Get similarity-based problems and change requests as recommendations by recognizing the similar patterns between the fields of the incident table and the problem or change request table.
        -   Manage the Standard Change life cycle. Create, propose, edit and retire standard change templates from Service Operations Workspace.
        -   Explore and filter the Change Catalog. Find your change model or template with ease when raising new changes, by using improved filtering and search for the Change Catalogue in Service Operations Workspace.
        -   Propose mass configuration item updates in Change Management. Automate the update and audit trail of CIs from within the change record in Service Operations Workspace. Mass update and change proposals record the attributes being changed and \(optionally\) update the CMDB automatically when the change is complete.
-   **Version 5.1.0 - August 2024**
    -   New: Service Reliability Management - Improvement for Teams and Service enablement for Service Reliability Management
    -   Fixed:
        -   Service Reliability Management - Performance issue in activating Teams and Services for Service Reliability Management.
        -   Major Incident Management: Sidebar channels in Major Incident Management which should be added per Communication Plan Definition was not added.
        -   On-Call: On-Call: Escalation designer in Service Operations Workspace sometimes would not add audience.
        -   Change Management
            -   Change Overview pane does not display any card information when the Planning overview card is selected.
            -   CI / Service / Service offering pop up does not load on SOW Change Management.
        -   Problem Management: Problem Tasks created with a type \(when models is enabled\) should not change the Model field if it is not empty.
-   **Version 4.2.2 - June 2024**

    No changes. Updated for dependency update.

-   **Version 5.0.0 - May 2024**
    -   New:
        -   Manage the entire major incident lifecycle with Major Incident Management in Service Operations Workspaces in the following ways:
            -   Propose, promote, create, and manage major incidents.
            -   Identify and create a major incident automatically based on major incident trigger rules.
            -   Communicate with business stakeholders and end users by sending status updates and notifications to inform about the impact and progress of the major incident.
            -   Collaborate with the business stakeholders to discuss the issues and help with resolving the major incident.
            -   Resolve major incident.
        -   Configure Major Incident Management using Admin Center in Service Operations Workspace. Admin Center enables you to install Major Incident Management and then configure the following features:
            -   Major incident trigger rules to automatically create, propose, or promote major incidents.
            -   Assign playbooks to manage major incident process.
            -   Assign Major Incident Manager role to users for managing major incidents.
            -   Email notifications that are sent to the stakeholders and end users.
            -   Communication such as email and SMS messages sent to the stakeholders and end users.
            -   Communication plans definitions, tasks, collaboration tasks and channels for an easy and effective communication with stakeholders and end users.
            -   Timeline configuration for generating post incident report.
        -   Visualize the entire major incident process in a task-oriented view with Major incident Playbooks in Major Incident Management. They leverage communication, collaboration, and core major incident process capabilities. This helps in quickly identifying key areas that require attention, and managing and resolving major incidents faster. The following two playbooks are available in the base system:
            -   MI playbook
            -   Advanced MI playbook
        -   Review the post incident report for a major incident to evaluate the incident response process and identify the process gaps for improvements. Reviewing the report helps you analyze the incident and understand what can be done to avoid a similar incident or issue in the future. Post incident report is created automatically after a major incident is resolved. Use the Post incident reporttab on a major incident record to generate, edit, review and publish the report in PDF.
        -   Incident management enhancements:
            -   Copy the page URL to clipboard for quickly sharing the link with other agents or stakeholders.
            -   Preview the records of the reference key fields on the same page. If you want, you can also open the record on a separate tab.
            -   Update the incident information on the Summary and Impact summary section of the Overview tab.
            -   Preview the caller information from the caller card on the Record information side panel.
            -   View the assets, recent interaction, and incident information specific to the caller.
            -   The incident information on the header of the incident record page is now moved to the Summary section to increase the workspace view area.
            -   Preview the record information from the respective lists on the landing page. Users can preview and update the record information in the workspace view. This feature is applicable for the following records:
                -   Interaction
                -   Incident
                -   Problem
                -   Change
                -   Request
        -   Problem management enhancements:
            -   Problem coordinators can manage problems and problem tasks through their lifecycle on Service Operations Workspace
        -   Admin Center enhancements:
            -   Added support for installing Major Incident Management in Service Operations Workspace.
            -   Added differentiated landing page configurations for tier 1 and tier 2 personas for:
                -   Donut configurations
                -   Announcements
                -   Upcoming section
                -   Quick links
                -   Getting started section
            -   Added support for collapsing the donut card lists by default on the landing page.
    -   Fixed:
        -   Change Management:
            -   Various improvements to field labels for accessibility.
            -   Screen readers should only factor headings for the toggle of the Scope and Impact section on Overview page.
            -   New button on custom lists created via My Lists for Change Request does not work.
            -   Users need to reload the page to see Refresh Impacted Services button on saving a new change request
            -   Users are unable to view accessible change model cards on the Change Model landing page.
            -   Change Schedule page fails to load when a custom abort Business Rule executes on submission of the Planned Start and End Date fields.
            -   The activity section on change overview page cannot be hidden once it is collapsed.
            -   Counts on the cards in the Scope and Impact Overview section do not reflect the counts in the corresponding lists of records.
            -   Change Models landing page is blank for users that have insufficient roles.
            -   Secondary Risk Actions not being translated correctly.
        -   Incident Management:
            -   Minor defect fixes
-   **Version 4.2.0 - February 2024**
    -   New:
        -   Updates to on-call capabilities: Ability to use the schedules menu to access the On-Call Scheduling application from the home page. Agents can use schedules to view their schedules, request absence and set their notification preference. Group Manager can use schedules to manage schedules and requests, set escalation trigger rules and policies, and create delivery channels for notification preferences
        -   Updates to Site Reliability Management capabilities: Introduced updated access controls and global team access changes for SRM
    -   Changed: Minor updates and fixes
-   **Version 4.1.0 - November 2023**

    Updated support for the Now Assist for ITSM application.

-   **Version 4.0.0 - November 2023**

    Simplify the upgrade experience using the standard record page for various record forms.

-   **Version 3.1.0 - September 2023**
    -   New: Now Assist Summary component for Incident Overview
    -   Changed: Incident Resolve modal changes
    -   Fixed
        -   Fixed interaction performance issue of slow load of an interaction record.
        -   Fixed issue with starting a conference call when the participant number is very large
-   **Version 3.0.0 - August 2023**
    -   New:
        -   Collaboration Services for Service Operations Workspace:
            -   Initiate and manage conference calls for Zoom, MS Teams, and Webex.
            -   Initiate and manage telephony calls with Twilio.
            -   Initiate and manage chats using Sidebar.
            -   Send SMS messages directly from the workspace.
        -   Recommended Actions for ITSM - Advanced:
            -   Added support to display Recommended Actions.
            -   Display contextual and actionable recommendations through a side panel for incidents. Additionally, recommendations can also be shown at the field level.
            -   Users can configure the rules for both field-level and contextual recommendations.
        -   Service Operations Workspace ITSM Admin Experience:
            -   Provides a simple UI to configure the content and information that is surfaced to the agents on record pages. It also surfaces additional application capabilities that can be enabled to update your agent workspaces.
    -   Changed:
        -   Incident Management:
            -   Updated the Incident Overview page.
            -   Added new Recommended Actions for Incidents.
        -   Remedial Actions Framework:
            -   Added controls to restrict duplicate remedial action request execution within a time window.
            -   Allow cancellation of a remedial action.
    -   Fixed:
        -   Fixed inline editing issue with related record lists.
        -   Functional and performance fixes on an interaction record.
        -   Other minor bug fixes.
-   **Version 2.1.1 - June 2023**
    -   Fixed:
        -   A performance issue on Service Operations Workspace landing page when there are multiple on-call groups on the instance
        -   A technical error for installation warnings from Change Management for Service Operations Workspace
-   **Version 2.1.0 - May 2023**

    New:

    -   Added support for CTI in contact card.
    -   Added table-based configuration options so that change teams can easily align the Overview Pages to their process requirements. This new configuration option provides a greatly simplified approach to ensuring that the right information is rendered to knowledge workers when navigating the change via the Overview Pages.
    -   Investigation Framework:
        -   Remedial Actions Framework - New capability added to support remediations.
        -   Execute remedial actions directly on CI.
        -   Support for automatically fetching msinfo32 and dsregcmd data for Windows devices and servers.
        -   Introduced a new status 'Cancelled' for on-call escalations.
-   **Version 2.0.1 - March 2023**

    Fixed - Minor fixes.

-   **Version 2.0.0 - February 2023**
    -   New:
        -   Incident Investigation:
            -   An adapter to support Microsoft Endpoint Configuration Manager for incident investigation.&gt;
            -   Visibility for when metrics cross pre-set warning and critical threshold levels
            -   Additional system information metrics for Agent Client Collector \(ACC\) adapter&gt;
    -   Change Management: Navigate the change lifecycle with dynamic overview pages and a scheduling experience in Service Operations Workspace.
    -   Experts on-call: Track on-call escalations in real-time.
    -   Changed: Interaction Management - Reach out to the requester using the contact details on the Requester card.
    -   Fixed: Fixed inline editing issue with related record lists.
-   **Version 1.3.3 - January 2023**

    Minor fixes.

-   **Version 1.3.1 - November 2022**
    -   New:
        -   Enabled AI Search as the search engine for global search in Service Operations Workspace.
        -   Added Complete and Abandon UI actions on the interaction record.
        -   Added Agent Assist on the interaction record for searching KB articles.
        -   Enabled MS Teams collaboration on the interaction record.
    -   Changed: Experts on-call are displayed based on all configuration items and services associated with the incident.
    -   Fixed:
        -   Active records in the Requestor Information panel display in various languages.
        -   Agent Assist does not show when creating a new record.
        -   Creating a pre-approved change returns an error.
        -   The New button does not redirect to a change request form when a user has admin access.
        -   The Edit button for quick links on the homepage disappears if favorites are pinned.
-   **Version 1.2.1 - August 2022**
    -   New:
        -   Prioritize work for tier-2 agents by seeing an overview of assignments, outages, and service announcements.
        -   Investigate any affected CIs associated with an incident using the Investigate tab. This tab displays statistical information of the associated affected CIs and helps you analyze and resolve incidents.
        -   View the availability of a user on MS Teams before reaching out to the user via chat
        -   Reduce the interaction request queue in an agents inbox by enabling automatic assignment of interactions using Advanced Work Assignment \(AWA\) assignment rules.
-   **Version 1.1.1 - June 2022**
    -   New:
        -   Added onboarding experience for users logging into Service Operations Workspace. It provides instructions to orient users to key tasks in the workspace.
        -   Introduced a Guided setup, Service Operations Workspace for ITSM, to help with the initial configuration of the workspace.
    -   Changed:
        -   Made UI changes to ensure a consistent visual experience.
        -   If the incident is not assigned to anyone and the logged-in user belongs to the current assignment group, replaced the Assign action with the Assigned to me action for the Record information section in the contextual side panel.
    -   Fixed:
        -   Landing page: If KPIs are not set up or there is no data available for the agent, performance-related message on the landing page header is hidden.
        -   Incident Management: The Assign to me list action is hidden for incidents that are already assigned to the logged-in user.
        -   Problem Management: The New button works on the problem task list when a user adds it to sys\_ux\_list.
        -   Change Management:
            -   Added the Incidents caused by change related list on the Change form.
            -   Added a header entry to define the short description as the primary field for change tasks.
        -   Walk-up Experience: Added the Consume UI action on Stockroom Consumable.
        -   Workspace: Fixed console errors for the sn-contact-card component and agent chat.
-   **Version 1.0.1 - March 2022**

    Service Operations Workspace ITSM Applications enable you to streamline IT Service Management workflows and processes for modern operations. You can effectively manage the lifecycle of incidents, requests, and walk-up appointments in the Service Operations Workspace.


