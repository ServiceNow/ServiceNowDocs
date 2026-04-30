---
title: Service Operations Workspace for ITSM release notes
description: The ServiceNow Service Operations Workspace application is a configurable workspace that provides a unified agent experience for multiple IT Service Management and IT Operations Management capabilities. Service Operations Workspace for IT Service Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
---

# Service Operations Workspace for ITSM release notes

The ServiceNow® Service Operations Workspace application is a configurable workspace that provides a unified agent experience for multiple IT Service Management and IT Operations Management capabilities. Service Operations Workspace for IT Service Management was enhanced and updated in the Zurich release.

## Service Operations Workspace highlights for the Zurich release

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
    -   As an on-call shift administrator with the rota\_admin role, access Teams, Schedules, and Home pages in SOW.

See [Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=sow-landing-page&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

**Important:** Service Operations Workspace is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Service Operations Workspace to Zurich

Ensure that the following applications have compatible upgraded versions:

-   Service Operations Workspace ITSM Applications application \(sn\_sow\_itsm\_cont\)
-   Service Operations Workspace ITOM Applications application \(sn\_sow\_itom\_cont\)

For more information on compatible versions, see [Version compatibility between Service Operations Workspace for ITSM and Service Operations Workspace ITOM](https://www.servicenow.com/docs/access?context=sow-itsm-itom-version&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

## New in the Zurich release

-   **[Configuring Notify in Service Operations Workspace](https://www.servicenow.com/docs/access?context=configure-notify-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Configure Notify with Microsoft Teams SOW in Admin Center using the guided setup.

-   **[Visual indicators for unread messages](https://www.servicenow.com/docs/access?context=sow-itsm-workspace-chat-session-tabs-configure&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    To help agents maintain the Service Level Agreement \(SLA\) for chats, visual indicators are available on chat session tabs in the SOW. These indicators include color codes, where tabs with unread messages are highlighted in different colors. Inactive tabs display a purple background color to indicate that a message has been received. Tab colors shift to yellow and then to red to highlight critical wait times. These enhancements aim to improve customer service by ensuring quick response time, increase productivity by helping agents manage multiple chats more effectively, and reduce stress by providing clear visual cues, ultimately leading to better SLA compliance and higher service quality.

-   **[Resize modal in Service Operations Workspace](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Optimize your viewing experience by resizing the following modals in SOW:

    -   Copy incident
    -   Report knowledge gap
    -   Reopen incident
-   **[Add similar incidents to major incident record](https://www.servicenow.com/docs/access?context=managing-major-incident-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Find multiple similar incidents and add them as child incidents to a major incident or major incident candidate record from the child incident related list in the **Related records** tab of the major incident record. Similar incidents are retrieved based on the similarity solution definition that can be configured to train on various fields such as **Short description** and **Description**. Adding the similar incidents as child incidents to the major incident record ensures avoiding the creation of multiple major incident records for the same issue.

-   **[On-Call Scheduling enhancements in Service Operations Workspace](https://www.servicenow.com/docs/access?context=work-on-escalation-trigger-rules-and-policies-in-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    On-call scheduling in SOW has the following enhancements:

    -   The On-call trigger rule page is enhanced to support and select subflows.
    -   The On-call trigger rule page is enhanced for supporting re-triggering escalations on configured fields such as Priority. Re-triggering is enabled whenever the value in the configured field changes.
    -   Configure custom providers as channels for on-call escalation notifications.
    -   Send the on-call escalations notifications to all stakeholders when any of the record fields configured using the on-call trigger rules are modified.
-   **[Auto-dismiss the alerts and notification in Service Operations Workspace](https://www.servicenow.com/docs/access?context=configure-alerts-auto-dismiss-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Configure the alerts and notifications in SOW to automatically dismiss within the specified time. Auto-dismissal of the alert notification reduces the user effort in manually dismissing the notification. By default, the base system has the following settings:

    -   Auto-dismiss is turned on for alert notification of type info, positive \(success\) and low and has the timeout value of three seconds.
    -   Auto-dismiss is turned off for alert notification of type critical, high, moderate, and warning.
    -   The time label is turned off and only a visual time indicator is displayed.
    -   The alert notification content is expanded.
-   **[DEX and SO view in the investigate tab](https://www.servicenow.com/docs/access?context=dex-so-metric-views-investigate-tab&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Based on the Configuration Item \(CI\) selected in the **Investigate** tab and the rules defined in the **Investigate CI Experience Rules** \(**sn\_sow\_investigate\_ci\_ux\_rule**\) table, the Investigate tab displays the CI metrics in the UI experience dashboard view for the different CI classes:

    -   DEX view - Displayed for the cmdb\_ci\_computer CI class.
    -   SO view - Displayed for the cmdb\_ci\_service class.
    You can select both the affected CIs including service and service offering and caller CIs.

-   **[SOW record page enhancements](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    The SOW record page has the following enhancements:

    -   Add a clickable URL to the Summary section on the **Overview** tab of an incident record, enhancing navigation and reference capabilities. The Overview page supports URL type of field in read-only mode.
    -   Perform various DEX actions on a CI using actions from the Action library in the contextual side panel of the SOW record page.
    -   Manage user actions on the reference fields of a SOW record page with the following glide list actions:
        -   Add me - Add the logged in user to the field.
        -   Remove me - Remove the logged in user from the field.
        -   Add multiple users - Add multiple users to the field.
        -   Add multiple records - Add multiple records to the field.
-   **[View recent tasks in a knowledge article record](https://www.servicenow.com/docs/access?context=work-knowledge-article&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Configure the **Display recent task for knowledge article** \(**glide.knowman.recent\_task.display**\) system property to view the recent task records to which the knowledge article is recently attached. You can select the task record link to open the task record in a new tab with the workspace view.

-   **[Introduction of Granular Admin roles in SOW](https://www.servicenow.com/docs/access?context=roles-in-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    The following granular admin roles are introduced in SOW:

    -   sn\_sow\_admin.sn\_sow\_admin: Provides access to SOW Admin Center page for SOW configurations. Admins can use the role to configure SOW features and maintain organizational policies.
    -   sn\_sow\_inc\_sn\_incident\_sow\_admin: Provides access to SOW Admin Center pages for configurations related to Incident Management features.
    -   sn\_sow\_mim.sn\_mim\_sow\_admin: Provides access to the SOW Admin Center pages for configurations related to Major Incident Management \(MIM\) features.
    -   sn\_sow\_on\_call.sn\_on\_call\_sow\_admin: Provides access to the SOW Admin Center pages for On-Call Scheduling configurations.
    -   sn\_sow\_problem.sn\_problem\_sow\_admin: Provides access to the SOW Admin Center pages for Problem Management configurations.
-   **[View conflicts in the change request form](https://www.servicenow.com/docs/access?context=create-change-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    The improved schedule and conflicts section added in the change request form displays the scheduling conflicts for a change request. If a scheduling conflict exists, conflict detection also provides details of any related blackout or maintenance schedules and other active change requests to determine the scheduling conflict. You can use the resulting information to review and modify the change request details to eliminate conflicts. You can also manually check and manage conflicts.

    For more information on conflict detection, see [Conflict detection](https://www.servicenow.com/docs/access?context=c_ConflictDetection&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

-   **[Interaction wrap up with modeless dialog in Service Operations Workspace](https://www.servicenow.com/docs/access?context=interaction-wrap-up-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Provide agents with dedicated time after each call or chat to finalize the interaction details and wrap up their work before starting a new conversation.


## UI changes

-   **[CAB workbench enhancements](https://www.servicenow.com/docs/access?context=cm-manage-cab-meeting-workbench-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**
    -   Configuration provided for risk-highlighted value is displayed in the agenda item card and CAB meeting details.
    -   Visual feedback is provided when agenda items are restored.

## Changed in this release

-   **[Configure help and order of the remedial action parameters](https://www.servicenow.com/docs/access?context=components-installed-with-remediation-fw&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Configure the **Help** and **Order** fields for the remedial action parameters on the Remedial action parameter \[sn\_reacf\_remedial\_action\_parameter\] table if you have the Remedial action admin\[sn\_reacf.sn\_remedial\_action\_admin\] user role.

-   **[List page enhancements in Service Operations Workspace](https://www.servicenow.com/docs/access?context=work-incident-list-page-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    The list page in SOW has the following enhancements:

    -   The related lists in the **Related records** tab of the SOW record pages, including those within the record pages as well such as Recent Incidents or Assigned Assets, are updated with the record list bundle. This update provides them with the same appearance, functionality, and user experience as the SOW list page.
    -   The related lists in the **Related records** tab of the SOW record pages, including the Multi Record Associator \(MRA\) list, as well as the related lists within the record pages such as Recent Incidents or Assigned Assets, now support the fuzzy count UX page property. You can configure a default value that is applicable to the list for all tables or a value for a specific table such as incident thereby improving the list page performance.
-   **[Dependency view changes for reference fields](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Selecting the dependency view for the following fields in the incident, problem, change, and request records, opens a unified CMDB map in a new tab within the workspace view instead of a new browser tab:

    -   Configuration item
    -   Service
    -   Service offering
-   **[Propose a standard change template](https://www.servicenow.com/docs/access?context=propose-standard-change-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    As a user with the itil role, you can create a standard change template proposal from any change record in SOW.

-   **[Service Operations Workspace access for an on-call shift administrator](https://www.servicenow.com/docs/access?context=roles-in-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Starting in version 8.2, a user with the rota\_admin role can access Teams, Schedules, and Home pages in SOW.


## Activation information

Service Operations Workspace for ITSM is active by default and its default version is 8.0 in Zurich. When you upgrade from any previous release to Zurich from the ServiceNow Store, Service Operations Workspace for ITSM 8.0 is automatically installed.

## Accessibility information

-   **Reflow**

    The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

    This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See  for details.


## Related ServiceNow applications and features

-   **[Change Management](https://www.servicenow.com/docs/access?context=c_ITILChangeManagement&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Control the life cycle of a change and implement the change with minimum disruption to IT services.

-   **[Incident Management](https://www.servicenow.com/docs/access?context=c_IncidentManagement&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Enable users to identify IT issues and log incidents through the Incident Management system. Efficiently track, classify, and prioritize incidents to work effectively toward their resolution.

-   **[Interaction Management](https://www.servicenow.com/docs/access?context=interaction-management&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Respond to an incoming chat, phone, walk-up, or messaging interaction quickly by using an interaction that provides a centralized location for all communication channels.

-   **[Notify](https://www.servicenow.com/docs/access?context=notify-landing-page&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Provide support for SMS and voice channels on the platform to communicate with your team and customers.

-   **[On-Call Scheduling](https://www.servicenow.com/docs/access?context=c_OnCallScheduling&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Identify available on-call members of a support group who can be contacted to resolve an issue.

-   **[Password Reset](https://www.servicenow.com/docs/access?context=password-reset-landing-page&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    The ServiceNow® Password Reset application enforces strong and secure passwords by enabling end users to reset or change their passwords either by using the self-service process or by requesting the assistance of a service desk agent.

-   **[Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use machine-learning algorithms to provide dynamic and contextual recommendations for resolving an incident.

-   **[Problem Management](https://www.servicenow.com/docs/access?context=c_ProblemManagement&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Identify the root cause of recurring incidents or a major incident to help prevent them from happening again.

-   **[Recommended Actions for ITSM in Service Operations Workspace](https://www.servicenow.com/docs/access?context=recommended-actions-for-itsm-in-service-operations-workspace&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Get field recommendations and guidance in the side panel for the incident form in Service Operations Workspace.

-   **[Request Management](https://www.servicenow.com/docs/access?context=c_RequestManagement&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Initiate a catalog request flow from a different IT Service Management flow, such as an incident flow, by using catalog requests.

-   **[Service Level Management](https://www.servicenow.com/docs/access?context=service-level-mgmt-landing-page&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Access incident service level agreement \(SLA\) information on the Service Operations Workspace for ITSM landing page and incident record page.

-   **[Service Operations Workspace for ITOM](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Configure your operator experience through a unified interface for multiple ServiceNow® IT Operations Management workflows.

-   **[Walk-up Experience](https://www.servicenow.com/docs/access?context=walkup-experience-landing-page&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Manage walk-up interactions and queues effortlessly by using Service Operations Workspace for ITSM.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

