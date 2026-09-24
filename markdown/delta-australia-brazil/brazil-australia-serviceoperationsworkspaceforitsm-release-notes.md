---
title: Combined Service Operations Workspace for ITSM release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Service Operations Workspace for ITSM from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-serviceoperationsworkspaceforitsm-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Service Operations Workspace for ITSM release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Service Operations Workspace for ITSM from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Service Operations Workspace for ITSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Service Operations Workspace for ITSM to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Service Operations Workspace for ITSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Review AI incident summary and suggestions in the incident record](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&family=australia&ft:locale=en-US)**

Investigate and resolve incidents efficiently by reviewing the AI-generated incident summary and suggested resolution plan in the AI summary and suggestions card on the **Overview** tab of an incident record. If the **Overview** tab is hidden for L1 service desk agents, the card appears on the **Details** tab.


 -   **[UI16 links to SOW redirection behavior](https://www.servicenow.com/docs/access?context=manage-admin-console-sow-itsm&family=australia&ft:locale=en-US)**

Redirect UI16 module links such as forms and lists to the equivalent SOW experience. The UI16 module link redirection behavior is supported for all the applications in SOW when the system property **sn\_sow\_itsm\_admin.experience\_redirection\_enabled.sow** is set to `true`.

For new instances, this redirection configuration is automatically available in the base system. For upgrade instances, administrators can configure the redirection behavior from the SOW Admin Center. You can enable this feature for the UI16 links and user groups or specifically for a custom table. You can also enable this feature for specific user groups or all user groups within the custom table or applications in SOW.

-   **[Mapping granular admin roles with SOW granular roles](https://www.servicenow.com/docs/access?context=roles-in-sow&family=australia&ft:locale=en-US)**

Using granular admin roles, provide full administrative access to the configuration and property pages for the applications in SOW without requiring the administrator \(admin\) role. These granular admin roles are mapped with ACLs and contain the corresponding existing SOW granular roles.

-   **[UX property to hide contextual side panel](https://www.servicenow.com/docs/access?context=manage-admin-console-sow-itsm&family=australia&ft:locale=en-US)**

Use the Hide contextual side panel for specific table and tab combination option from the SOW Properties section in the SOW Admin Center to configure the hide **ContextualSidebar** UX page property. This property enables you to define the table with tab combination for which the default primary contextual side panel must be hidden, prioritizing the embedded contextual side panel within the tab instead.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Auto install SOW](https://www.servicenow.com/docs/access?context=getting-started-sow&family=brazil&ft:locale=en-US)**

A scheduled job is now available that executes a batch installation on a new instance to automatically install applications such as Service Operations Workspace for ITSM Advanced Applications only if the you have the necessary entitlements for the application. This is applicable only on newly provisioned zboot instance.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Service Operations Workspace for ITSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Generate, update and publish PIR](https://www.servicenow.com/docs/access?context=review-update-pir-mim-sow&family=australia&ft:locale=en-US)**

Perform the following actions on the PIR if you have the incident\_write role and added as co-contributor to the PIR:

    -   Update the state or publish the PIR.
    -   Refresh the Incident Summary data on the PIR.
    -   Create PIR custom event.
    -   Search, add, edit and save co-contributors \(Users\) for PIR.

 -   **[Configure reference field auto-load behavior from SOW Admin Center](https://www.servicenow.com/docs/access?context=admin-center-sow&family=australia&ft:locale=en-US)**

Use the Reference field auto-load behavior option from the SOW Properties section of the SOW Admin Center to configure the **Reference search on click** \(**ref\_search\_on\_click**\) UX page property. The option enables you to configure the automatic searching of field value results displayed for reference fields such as Configuration item, Service offering, and Service.

-   **[Recent list links in SOW record](https://www.servicenow.com/docs/access?context=view-inc-record-info-contextual-sidepanel&family=australia&ft:locale=en-US)**

Select the Recent incidents, Recent interaction, or Recent tasks links from the Record information side panel of a SOW record displays the 10 most recent records irrespective of their timeline instead of showing the records from last seven days. You can select the **View All** option to view additional records as well.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Default Attached knowledge related list](https://www.servicenow.com/docs/access?context=incident-sow&family=brazil&ft:locale=en-US)**

The attached knowledge related list now appears in the Related records tab by default, if any Knowledge article attached to the incident record.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Service Operations Workspace for ITSM features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Service Operations Workspace for ITSM features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

-   **Activation information**

Service Operations Workspace for ITSM is active by default and its default version is `9.0` in Australia. When you upgrade from any previous release to Australia from the ServiceNow Store, Service Operations Workspace for ITSM `9.0` is automatically installed.


**Important:** Service Operations Workspace is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Service Operations Workspace for ITSM is active by default and its default version is 9.5 in Brazil. When you upgrade from any previous release to Brazil from the ServiceNow Store, Service Operations Workspace for ITSM 9.5 is automatically installed.


**Note:** Service Operations Workspace is available in the ServiceNow Store. For details, see the following activation information.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Service Operations Workspace for ITSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Accessibility information**
    -   Accessibility improvements were made to the Major Incident Management in Service Operations Workspace for ITSM in UI List component, record pages and Major Incident workbench tabs, including keyboard navigation and screen reader support. These updates benefit users who rely on screen readers or other Assistive Technology \(AT\), keyboard-only users, and users with low vision.
    -   Reflow support for Major Incident Management in Service Operations Workspace for ITSM: Content can be zoomed up to 400% through your browser settings, with page layouts automatically transforming into a vertical, stacked view without loss of content or functionality. This enhancement helps users with low vision or who have trouble seeing web content due to monitor size, device type, poor lighting, or other situations.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Service Operations Workspace for ITSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

-   Redirect UI16 module navigation links to the equivalent SOW experience.
-   Access SOW configuration and property pages of various SOW applications using granular admin roles.
-   Improve the focus on relevant contextual information by hiding the contextual side panel for a specific table and tab combination.
-   Configure reference field auto-load behavior from the SOW Admin Center.
-   Enable service desk agents to create, manage, and track checklists for Request and RITM records directly within the workspace to confirm that all steps are completed.
-   Starting in version 9.2, you can do the following:
    -   Perform various actions on the post incident report \(PIR\) if you have the incident\_write role and added as co-contributor to the PIR.
    -   Investigate and resolve incidents by using the AI incident summary and resolution plan suggestion in the **Overview** tab of an incident record.

 See [Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=sow-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Service Operations Workspace provides a unified interface for IT service agents to manage incidents, changes, requests and approvals. It supports configurable dashboards, list views, and record pages for ITSM and ITOM workflows.
-   You can effectively manage the lifecycle of incidents, requests in Service Operations Workspace. All of these workflows leverage the power of capabilities such collaborations and AI based recommendations.

 See [Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=sow-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

