---
title: Combined Service Operations Workspace for ITSM release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Service Operations Workspace for ITSM from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-serviceoperationsworkspaceforitsm-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 14
breadcrumb: [Products combined by family]
---

# Combined Service Operations Workspace for ITSM release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Service Operations Workspace for ITSM from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Service Operations Workspace for ITSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Service Operations Workspace for ITSM to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Ensure that the following applications have compatible upgraded versions:

-   Service Operations Workspace ITSM Applications application \(sn\_sow\_itsm\_cont\)
-   Service Operations Workspace ITOM Applications application \(sn\_sow\_itom\_cont\)

 For more information on compatible versions, see [Version compatibility between Service Operations Workspace for ITSM and Service Operations Workspace ITOM](https://www.servicenow.com/docs/access?context=sow-itsm-itom-version&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Service Operations Workspace for ITSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Configuring Notify in Service Operations Workspace](https://www.servicenow.com/docs/access?context=configure-notify-sow&family=zurich&ft:locale=en-US)**

Configure Notify with Microsoft Teams SOW in Admin Center using the guided setup.

-   **[Visual indicators for unread messages](https://www.servicenow.com/docs/access?context=sow-itsm-workspace-chat-session-tabs-configure&family=zurich&ft:locale=en-US)**

To help agents maintain the Service Level Agreement \(SLA\) for chats, visual indicators are available on chat session tabs in the SOW. These indicators include color codes, where tabs with unread messages are highlighted in different colors. Inactive tabs display a purple background color to indicate that a message has been received. Tab colors shift to yellow and then to red to highlight critical wait times. These enhancements aim to improve customer service by ensuring quick response time, increase productivity by helping agents manage multiple chats more effectively, and reduce stress by providing clear visual cues, ultimately leading to better SLA compliance and higher service quality.

-   **[Resize modal in Service Operations Workspace](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&family=zurich&ft:locale=en-US)**

Optimize your viewing experience by resizing the following modals in SOW:

    -   Copy incident
    -   Report knowledge gap
    -   Reopen incident
-   **[Add similar incidents to major incident record](https://www.servicenow.com/docs/access?context=managing-major-incident-sow&family=zurich&ft:locale=en-US)**

Find multiple similar incidents and add them as child incidents to a major incident or major incident candidate record from the child incident related list in the **Related records** tab of the major incident record. Similar incidents are retrieved based on the similarity solution definition that can be configured to train on various fields such as **Short description** and **Description**. Adding the similar incidents as child incidents to the major incident record ensures avoiding the creation of multiple major incident records for the same issue.

-   **[On-Call Scheduling enhancements in Service Operations Workspace](https://www.servicenow.com/docs/access?context=work-on-escalation-trigger-rules-and-policies-in-sow&family=zurich&ft:locale=en-US)**

On-call scheduling in SOW has the following enhancements:

    -   The On-call trigger rule page is enhanced to support and select subflows.
    -   The On-call trigger rule page is enhanced for supporting re-triggering escalations on configured fields such as Priority. Re-triggering is enabled whenever the value in the configured field changes.
    -   Configure custom providers as channels for on-call escalation notifications.
    -   Send the on-call escalations notifications to all stakeholders when any of the record fields configured using the on-call trigger rules are modified.
-   **[Auto-dismiss the alerts and notification in Service Operations Workspace](https://www.servicenow.com/docs/access?context=configure-alerts-auto-dismiss-sow&family=zurich&ft:locale=en-US)**

Configure the alerts and notifications in SOW to automatically dismiss within the specified time. Auto-dismissal of the alert notification reduces the user effort in manually dismissing the notification. By default, the base system has the following settings:

    -   Auto-dismiss is turned on for alert notification of type info, positive \(success\) and low and has the timeout value of three seconds.
    -   Auto-dismiss is turned off for alert notification of type critical, high, moderate, and warning.
    -   The time label is turned off and only a visual time indicator is displayed.
    -   The alert notification content is expanded.
-   **[DEX and SO view in the investigate tab](https://www.servicenow.com/docs/access?context=dex-so-metric-views-investigate-tab&family=zurich&ft:locale=en-US)**

Based on the Configuration Item \(CI\) selected in the **Investigate** tab and the rules defined in the **Investigate CI Experience Rules** \(**sn\_sow\_investigate\_ci\_ux\_rule**\) table, the Investigate tab displays the CI metrics in the UI experience dashboard view for the different CI classes:

    -   DEX view - Displayed for the cmdb\_ci\_computer CI class.
    -   SO view - Displayed for the cmdb\_ci\_service class.
You can select both the affected CIs including service and service offering and caller CIs.

-   **[SOW record page enhancements](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&family=zurich&ft:locale=en-US)**

The SOW record page has the following enhancements:

    -   Add a clickable URL to the Summary section on the **Overview** tab of an incident record, enhancing navigation and reference capabilities. The Overview page supports URL type of field in read-only mode.
    -   Perform various DEX actions on a CI using actions from the Action library in the contextual side panel of the SOW record page.
    -   Manage user actions on the reference fields of a SOW record page with the following glide list actions:
        -   Add me - Add the logged in user to the field.
        -   Remove me - Remove the logged in user from the field.
        -   Add multiple users - Add multiple users to the field.
        -   Add multiple records - Add multiple records to the field.
-   **[View recent tasks in a knowledge article record](https://www.servicenow.com/docs/access?context=work-knowledge-article&family=zurich&ft:locale=en-US)**

Configure the **Display recent task for knowledge article** \(**glide.knowman.recent\_task.display**\) system property to view the recent task records to which the knowledge article is recently attached. You can select the task record link to open the task record in a new tab with the workspace view.

-   **[Introduction of Granular Admin roles in SOW](https://www.servicenow.com/docs/access?context=roles-in-sow&family=zurich&ft:locale=en-US)**

The following granular admin roles are introduced in SOW:

    -   sn\_sow\_admin.sn\_sow\_admin: Provides access to SOW Admin Center page for SOW configurations. Admins can use the role to configure SOW features and maintain organizational policies.
    -   sn\_sow\_inc\_sn\_incident\_sow\_admin: Provides access to SOW Admin Center pages for configurations related to Incident Management features.
    -   sn\_sow\_mim.sn\_mim\_sow\_admin: Provides access to the SOW Admin Center pages for configurations related to Major Incident Management \(MIM\) features.
    -   sn\_sow\_on\_call.sn\_on\_call\_sow\_admin: Provides access to the SOW Admin Center pages for On-Call Scheduling configurations.
    -   sn\_sow\_problem.sn\_problem\_sow\_admin: Provides access to the SOW Admin Center pages for Problem Management configurations.
-   **[View conflicts in the change request form](https://www.servicenow.com/docs/access?context=create-change-sow&family=zurich&ft:locale=en-US)**

The improved schedule and conflicts section added in the change request form displays the scheduling conflicts for a change request. If a scheduling conflict exists, conflict detection also provides details of any related blackout or maintenance schedules and other active change requests to determine the scheduling conflict. You can use the resulting information to review and modify the change request details to eliminate conflicts. You can also manually check and manage conflicts.

For more information on conflict detection, see [Conflict detection](https://www.servicenow.com/docs/access?context=c_ConflictDetection&family=zurich&ft:locale=en-US).

-   **[Interaction wrap up with modeless dialog](https://www.servicenow.com/docs/access?context=interaction-wrap-up-sow&family=zurich&ft:locale=en-US)**

Provide agents with dedicated time after each call or chat to finalize the interaction details and wrap up their work before starting a new conversation.


</td></tr><tr><td>

Australia

</td><td>

-   **[UI16 links to SOW redirection behavior](https://www.servicenow.com/docs/access?context=manage-admin-console-sow-itsm&family=australia&ft:locale=en-US)**

Improve the fulfiller experience by redirecting UI16 module links such as forms and lists to the equivalent SOW experience. The UI16 module link redirection behavior is supported for all the applications in SOW when the system property **sn\_sow\_itsm\_admin.experience\_redirection\_enabled.sow** is set to `true`.

For new instances, this redirection configuration is automatically available in the base system. For upgrade instances, administrators can configure the redirection behavior from the SOW Admin Center. You can enable this feature for the UI16 links and user groups or specifically for a custom table. You can also enable this feature for specific user groups or all user groups within the custom table or applications in SOW.

-   **[Mapping granular admin roles with SOW granular roles](https://www.servicenow.com/docs/access?context=roles-in-sow&family=australia&ft:locale=en-US)**

Using granular admin roles, provide full administrative access to the configuration and property pages for the applications in SOW without requiring the administrator \(admin\) role. These granular admin roles are mapped with ACLs and contain the corresponding existing SOW granular roles.

-   **[UX property to hide contextual side panel](https://www.servicenow.com/docs/access?context=manage-admin-console-sow-itsm&family=australia&ft:locale=en-US)**

Use the Hide contextual side panel for specific table and tab combination option from the SOW Properties section in the SOW Admin Center to configure the hide **ContextualSidebar** UX page property. This property enables you to define the table with tab combination for which the default primary contextual side panel must be hidden, prioritizing the embedded contextual side panel within the tab instead.

-   **[Review AI incident summary and suggestions in the incident record](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&family=australia&ft:locale=en-US)**

Investigate and resolve incidents efficiently by reviewing the AI-generated incident summary and suggested resolution plan in the AI summary and suggestions card on the **Overview** tab of an incident record. If the **Overview** tab is hidden for L1 service desk agents, the card appears on the **Details** tab.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Service Operations Workspace for ITSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Configure help and order of the remedial action parameters](https://www.servicenow.com/docs/access?context=components-installed-with-remediation-fw&family=zurich&ft:locale=en-US)**

Configure the **Help** and **Order** fields for the remedial action parameters on the Remedial action parameter \[sn\_reacf\_remedial\_action\_parameter\] table if you have the Remedial action admin\[sn\_reacf.sn\_remedial\_action\_admin\] user role.

-   **[List page enhancements in Service Operations Workspace](https://www.servicenow.com/docs/access?context=work-incident-list-page-sow&family=zurich&ft:locale=en-US)**

The list page in SOW has the following enhancements:

    -   The related lists in the **Related records** tab of the SOW record pages, including those within the record pages as well such as Recent Incidents or Assigned Assets, are updated with the record list bundle. This update provides them with the same appearance, functionality, and user experience as the SOW list page.
    -   The related lists in the **Related records** tab of the SOW record pages, including the Multi Record Associator \(MRA\) list, as well as the related lists within the record pages such as Recent Incidents or Assigned Assets, now support the fuzzy count UX page property. You can configure a default value that is applicable to the list for all tables or a value for a specific table such as incident thereby improving the list page performance.
-   **[Dependency view changes for reference fields](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&family=zurich&ft:locale=en-US)**

Selecting the dependency view for the following fields in the incident, problem, change, and request records, opens a unified CMDB map in a new tab within the workspace view instead of a new browser tab:

    -   Configuration item
    -   Service
    -   Service offering
-   **[Propose a standard change template](https://www.servicenow.com/docs/access?context=propose-standard-change-sow&family=zurich&ft:locale=en-US)**

As a user with the itil role, you can create a standard change template proposal from any change record in SOW.

-   **[Service Operations Workspace access for an on-call shift administrator](https://www.servicenow.com/docs/access?context=roles-in-sow&family=zurich&ft:locale=en-US)**

Starting in version 8.2, a user with the rota\_admin role can access Teams, Schedules, and Home pages in SOW.


</td></tr><tr><td>

Australia

</td><td>

-   **[Configure reference field auto-load behavior from SOW Admin Center](https://www.servicenow.com/docs/access?context=admin-center-sow&family=australia&ft:locale=en-US)**

Use the Reference field auto-load behavior option from the SOW Properties section of the SOW Admin Center to configure the **Reference search on click ** \(**ref\_search\_on\_click**\) UX page property. The option enables you to configure the automatic searching of field value results displayed for reference fields such as Configuration item, Service offering, and Service.

-   **[Recent list links in SOW record](https://www.servicenow.com/docs/access?context=view-inc-record-info-contextual-sidepanel&family=australia&ft:locale=en-US)**

Selecting the Recent incidents, Recent interaction, or Recent tasks links from the Record information side panel of a SOW record displays the 10 most recent records irrespective of their timeline instead of showing the records from last seven days. You can select the **View All** option to view additional records as well.

-   **[Generate, update and publish PIR](https://www.servicenow.com/docs/access?context=review-update-pir-mim-sow&family=australia&ft:locale=en-US)**

Perform the following actions on the PIR if you have the incident\_write role and added as co-contributor to the PIR:

    -   Update the state or publish the PIR.
    -   Refresh the Incident Summary data on the PIR.
    -   Create PIR custom event.
    -   Search, add, edit and save co-contributors \(Users\) for PIR.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Service Operations Workspace for ITSM features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Service Operations Workspace for ITSM features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

Service Operations Workspace for ITSM is active by default and its default version is 8.0 in Zurich. When you upgrade from any previous release to Zurich from the ServiceNow Store, Service Operations Workspace for ITSM 8.0 is automatically installed.

</td></tr><tr><td>

Australia

</td><td>

Service Operations Workspace for ITSM is active by default and its default version is 9.0 in Australia. When you upgrade from any previous release to Australia from the ServiceNow Store, Service Operations Workspace for ITSM 9.0 is automatically installed.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Service Operations Workspace for ITSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

-   **Reflow**

The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [\[Placeholder link text to key bundle-platux.auto-reflow\]](https://www.servicenow.com/docs/access?context=auto-reflow&family=zurich&ft:locale=en-US) for details.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Service Operations Workspace for ITSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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
    -   As an on-call shift administrator with the rota\_admin role, access Teams, Schedules, and Home pages in SOW.

 See [Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=sow-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Redirect UI16 module navigation links to the equivalent SOW experience.
-   Access SOW configuration and property pages of various SOW applications using granular admin roles.
-   Improve the focus on relevant contextual information by hiding the contextual side panel for a specific table and tab combination.
-   Configure reference field auto-load behavior from the SOW Admin Center.
-   Enable service desk agents to easily create, manage, and track checklists for Request and RITM records directly within the workspace to confirm that all steps are completed.
-   Starting in version 9.2, you can do the following:
    -   Perform various actions on the post incident report \(PIR\) if you have the incident\_write role and added as co-contributor to the PIR.
    -   Reduce the effort to investigate and resolve incidents using the AI incident summary and resolution plan suggestion in the **Overview** tab of an incident record.

 See [Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=sow-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

