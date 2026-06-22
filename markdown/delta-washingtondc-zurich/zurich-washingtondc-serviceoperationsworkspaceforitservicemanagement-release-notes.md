---
title: Combined Service Operations Workspace for IT Service Management release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Service Operations Workspace for IT Service Management from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-serviceoperationsworkspaceforitservicemanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Service Operations Workspace for IT Service Management release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Service Operations Workspace for IT Service Management from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Service Operations Workspace for IT Service Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Service Operations Workspace for IT Service Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Ensure that the following applications have compatible upgraded versions:

-   Service Operations Workspace ITSM Applications application \(sn\_sow\_itsm\_cont\)
-   Service Operations Workspace ITOM Applications application \(sn\_sow\_itom\_cont\)

 |SOW-ITSM \(sn\_sow\_itsm\_cont\)|SOW-ITOM \(sn\_sow\_itom\_cont\)|
|--------------------------------|--------------------------------|
|1.1.x|21.0.y|
|1.2.x|21.1.y|
|1.3.x|21.2.y, 21.5.y, and 21.6.y|
|2.0.x|22.0.y|
|2.1.x|22.1.y and 22.y.y|
|3.1.x|23.y.y|
|4.x.x|24.y.y|

 In the table, x is the subversion of the Service Operations Workspace ITSM Applications application \(sn\_sow\_itsm\_cont\) and y is the subversion of the Service Operations Workspace ITOM Applications application \(sn\_sow\_itom\_cont\).

 After the 3.0 upgrade, the Recommendation Framework feature is no longer available. Instead, only the standard version of the Recommended Actions for ITSM feature is available.

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
</table>## New features

Between your current release family and Zurich, new features were introduced for Service Operations Workspace for IT Service Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Using Universal Request in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=using-ur-sow&family=washingtondc&ft:locale=en-US)**

Use the ServiceNow® Universal Request application to create requests and connect with other departments and services to assist with request resolution. You can map the various departmental ticket states and activity streams into a unified and simplified experience for your employees and agents.

-   **[On-Call Scheduling in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=on-call-scheduling-in-sow&family=washingtondc&ft:locale=en-US)**

Use the Schedules menu to access the ServiceNow® On-Call Scheduling application from the home page. Agents can use the Schedules menu to view their schedules, request absence and set their notification preference. A Group Manager can use the schedules icon to manage schedules and requests, set escalation trigger rules and policies, and create delivery channels for notification preferences.

Use the teams icon to access the teams record. Agents can use the Teams menu to view their team's on-call schedules and a Group Manager can set escalation trigger rules, escalation policies, and team preferences.

Starting in version 5.0, you can select a preferred shift from the Share calendar drop-down list and subscribe to the calendar. This option is available for Agents and Shift managers who are part of the respective group.

-   **[Landing page configurations using Admin Center](https://servicenow-staging.fluidtopics.net/access?context=manage-admin-console-sow-itsm&family=washingtondc&ft:locale=en-US)**

Starting in version 5.0, you can configure the following options for the landing page:

    -   Display or hide various sections.
    -   On the landing page, collapse the list view for donuts cards by default, which reduces the page load time, and expand the list view by selecting any donut card.
-   **[Quick access to the record information](https://servicenow-staging.fluidtopics.net/access?context=sow-ui-landing-page&family=washingtondc&ft:locale=en-US)**

Starting in version 5.0, get quick access to the record information.

    -   From the list view that opens by selecting a donut area on the landing page, access the record information for the following records:

        -   Incident
        -   Problem
        -   Interaction
        -   Change
        -   Request
**Note:** You can preview and update the record information in the workspace view.

    -   From any record page, copy the record page URL to easily access the record and share it with other agents and other stakeholders if required.
-   **[Problem Management in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=problem-sow&family=washingtondc&ft:locale=en-US)**

Starting in version 5.0, problem coordinators can:

    -   Manage problems and problem tasks through their life cycle.
    -   Share problem workarounds or fixes with related incidents.
    -   Create known error articles to help deflect incidents.
**Note:**

    -   If you aren't using the base problem life cycle, you must continue to use the classic experience to manage problems or problem tasks through their life cycle.
    -   The base problem life cycle is included with the Problem Management  Best Practice - Madrid - State Model \(com.snc.best\_practice.problem.madrid.state\_model\) plugin. Use the Problem Management Migration Utility [store application](https://store.servicenow.com/sn_appstore_store.do#!/store/application/d03b7539dbbb3300f21e7ffdbf9619a8) to enable this plugin and migrate your records to the base problem life cycle.
    -   Known error articles are enabled by the Problem Management Best Practice - Madrid - Knowledge Integration \(com.snc.best\_practice.problem.madrid.knowledge\) plugin.
-   **[Incident record page enhancements in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=view-update-inc-overview-tab&family=washingtondc&ft:locale=en-US)**

Starting in version 5.0, the incident record page has enhancements that maintain parity and bring the features from the classic UI16 to the workspace view. These enhancements reduce the efforts of agents to increase their productivity. With the enhancements, agents can:

    -   Copy the page URL to the clipboard to quickly share the link to other agents or stakeholders.
    -   Preview the records of the reference key fields on the same page, or open the record in a separate tab.
    -   Update the incident information in the Summary section and Impact summary section of the **Overview** tab.
    -   Preview caller information from the caller card on the Record information side panel.
    -   View the assets, recent interaction, and incident information that are specific to the caller.
    -   The incident information such as priority, state, configuration item and opened, is moved from the header of the incident record page to the Summary section of the **Overview** tab to increase the workspace view area.
-   **[Major incident management in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=mim-in-sow&family=washingtondc&ft:locale=en-US)**

Starting in version 5.0, Major Incident Management in Service Operations Workspace enables you to manage the entire major incident life cycle in the following ways:

    -   Propose, promote, create, and manage major incidents.
    -   View the number of impacted callers and their locations on the world map.
    -   Identify and create a major incident automatically based on major incident trigger rules.
    -   Communicate with the business stakeholders and end users by sending status updates and notifications to inform them about the impact and progress of the major incident.
    -   Collaborate with the business stakeholders to discuss the issues and help with resolving the major incident.
    -   Resolve major incidents.
-   **[Major incident configurations in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=setup-mim-sow&family=washingtondc&ft:locale=en-US)**

Starting in version 5.0, configure Major Incident Management using Admin Center in Service Operations Workspace. Admin Center enables you to install Major Incident Management and then accomplish the following:

    -   Configure major incident trigger rules to create, propose, or promote major incidents automatically.
    -   Assign playbooks to manage major incident process.
    -   Assign a Major Incident Manager role to users for managing major incidents.
    -   Configure email notifications that are sent to the stakeholders and end users.
    -   Configure the communications, such as email and SMS messages, sent to the stakeholders and end users.
    -   Configure communication plan definitions, tasks, collaboration tasks, and channels for effective communication with stakeholders and end users.
    -   Configure timelines for generating post incident reports.
-   **[Playbook integration with major incident management](https://servicenow-staging.fluidtopics.net/access?context=managing-mi-playbook-sow&family=washingtondc&ft:locale=en-US)**

Starting in version 5.0, major incident playbooks in Major Incident Management provide a way to visualize the entire major incident process in a task-oriented view. The major incident playbooks leverage communication, collaboration, and core major incident process capabilities. These capabilities help to quickly identify key areas that require attention, as well as manage and resolve major incidents. The following two playbooks are available in the base system:

    -   MI playbook
    -   Advanced MI playbook
-   **[Review and publish post incident report in Major Incident Management](https://servicenow-staging.fluidtopics.net/access?context=review-update-pir-mim-sow&family=washingtondc&ft:locale=en-US)**

Starting in version 5.0, review the post incident report for a major incident to evaluate the incident response process and identify the process gaps for improvements. Reviewing the report helps you analyze the incident and to understand what can be done to avoid a similar incident or issue in the future. A post incident report is created automatically after a major incident is resolved. Use the Post incident report tab on a major incident record to generate, edit, review, and publish the report in PDF.


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
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Service Operations Workspace for IT Service Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Landing page changes](https://servicenow-staging.fluidtopics.net/access?context=sow-ui-landing-page&family=washingtondc&ft:locale=en-US)**

Starting in version 5.0, the following changes are applicable:

    -   To view all records associated with a donut card, you should now select the center of the donut area.
    -   To view the recently visited pages in Service Operations Workspace, you should now select the **History** menu.

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
</table>## Removed

Between your current release family and Zurich, some Service Operations Workspace for IT Service Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Starting in version 5.0, the following options are removed from the landing page:

-   Second-level cards that were displayed upon selecting a first-level donut card
-   **View all** button for donut cards
-   **Recently Viewed** section

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

Between your current release family and Zurich, some Service Operations Workspace for IT Service Management features or functionality were deprecated.

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

Review information on how to activate Service Operations Workspace for IT Service Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Service Operations Workspace for ITSM is active by default and its default version is 2.1 in Washington DC. When you upgrade from any previous release to Washington DC from ServiceNow Store, Service Operations Workspace for ITSM 2.1 is automatically installed.

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
</table>## Additional requirements

If any additional requirements were introduced or changed for Service Operations Workspace for IT Service Management we have noted them here.

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

If any specific browser requirements were introduced or changed for Service Operations Workspace for IT Service Management we have noted them here.

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

Review details on accessibility information for Service Operations Workspace for IT Service Management, such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for Service Operations Workspace for IT Service Management we have noted them here.

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

If there are specific highlight considerations for Service Operations Workspace for IT Service Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   As an admin with the SOW admin user role \(sn\_sow\_itsm\_admin.sow\_admin\_user\), you can view ServiceNow® Admin Center for access to ServiceNow® Incident Management configurations. For more information about the roles in the Admin Center, see [Admin Center in Service Operations Workspace for ITSM](https://servicenow-staging.fluidtopics.net/access?context=admin-center-sow&family=washingtondc&ft:locale=en-US).
-   Enable agents to effectively resolve a case or request through cross-departmental interactions rather than working in silos using Universal Request.
-   View multiple field recommendations in a drop-down list by selecting fields in the incident form.
-   Access your schedules from the schedules icon on the navigation menu to view and manage On-call schedules.
-   Access your teams from the teams icon on the navigation menu to view and manage your teams.
-   Starting in version 5.0, you can do the following:
    -   Configure the visibility of various sections of the landing page.
    -   Configure if the list view should be collapsed by default for donut cards on the landing page.
    -   Preview and update record information from the respective lists on the landing page.
    -   Copy the record page URL to easily access the record.
    -   Increase the productivity of the agents with various incident record page enhancements.
    -   Resolve critical issues with high business impact using Major Incident Management.
    -   Configure the required major incident features using Admin Center.
    -   Easily manage major incidents with major incident playbooks.
    -   Review the post incident report to identify major incident process gaps and analyze the incident that helps to avoid the issue in the future.
    -   Manage problems and problem tasks through their life cycle.
    -   Subscribe to an individual shift with the Share calendar drop-down list.

 See [Service Operations Workspace for ITSM](https://servicenow-staging.fluidtopics.net/access?context=sow-landing-page&family=washingtondc&ft:locale=en-US) for more information.

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

