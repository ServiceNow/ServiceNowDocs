---
title: Combined Problem Management release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Problem Management from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-problemmanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 4
breadcrumb: [Products combined by family]
---

# Combined Problem Management release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Problem Management from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Problem Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Problem Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Between your current release family and Zurich, new features were introduced for Problem Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Initial support for Problem Management models](https://servicenow-staging.fluidtopics.net/access?context=problem-mgmt-models&family=xanadu&ft:locale=en-US)**

Introduction of Problem Management models, beginning with one default problem model \(General\) and two default problem task models \(Root cause analysis and General\).

The default models are equivalent to the base life cycle in the Washington DC release. This initial support allows for the creation of custom models to tailor additional scenarios for specific use cases.

**Note:**

If you are using Service Operations Workspace 5.x and you enable Problem Management models, you will manage problems and problem tasks in the classic UI16 experience, rather than in Service Operations Workspace.

Service Operations Workspace 6.x is based on the Xanadu release and it supports Problem Management models.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[User role for service desk agents](https://servicenow-staging.fluidtopics.net/access?context=prob-roles-instld-itsm-roles&family=yokohama&ft:locale=en-US)**

With the sn\_service\_desk\_agent user role, increase operational efficiency by streamlining the process of asking about, gathering, and verifying information, as well as delivering quick resolutions. This role is designed for tier 1 service desk agents and is accessible when the ITSM Roles plugin \(com.snc.itsm.roles\) installed.

The sn\_service\_desk\_agent role includes the following roles:

    -   sn\_incident\_write
    -   sn\_problem\_write
    -   sn\_change\_write
    -   sn\_request\_write
    -   tracked\_file\_reader
Additionally, with the installation of the **ITSM Gen AI** \(**com.sn.itsm.gen.ai**\) plugin, the knowledge\_user and now\_assist\_panel\_user roles are integrated within the sn\_service\_desk\_agent role.

The sn\_service\_desk\_agent user role can be used starting with Service Operations Workspace version 6.1.

-   **[Problem Models for Streamlined Problem Management](https://servicenow-staging.fluidtopics.net/access?context=problem-mgmt-models&family=yokohama&ft:locale=en-US)**

Problem Management models are used to simplify management of problems and problem tasks. These models provide an efficient way to configure state transitions and define conditions to move from one state to another.

This functionality is enabled out of the base system for new or zBoot customers.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Problem Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Re-assess a Problem Task from the Work in Progress state](https://servicenow-staging.fluidtopics.net/access?context=assess-a-problem-task&family=xanadu&ft:locale=en-US)**

Additional flexibility for the workflow of a problem task analyst.

-   **[Email notification redirection behavior](https://servicenow-staging.fluidtopics.net/access?context=configure-notifcations-sow-itsm&family=xanadu&ft:locale=en-US)**

When users select the problem record link in their email notifications, they can be redirected to the problem record in Service Operations Workspace instead of the classic UI16 experience. The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.

-   **[Known error articles available by default](https://servicenow-staging.fluidtopics.net/access?context=create-known-error-from-problem&family=xanadu&ft:locale=en-US)**

Problem Knowledge Integration is activated by default for new customers.

-   **[Problem Management Migration Utility](https://servicenow-staging.fluidtopics.net/access?context=migration-utility&family=xanadu&ft:locale=en-US)**

The Xanadu base problem files list is updated so the Problem Management Migration Utility can detect customizations.


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

Between your current release family and Zurich, some Problem Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Between your current release family and Zurich, some Problem Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Review information on how to activate Problem Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

[Problem Management](https://servicenow-staging.fluidtopics.net/access?context=c_ProblemManagement&family=xanadu&ft:locale=en-US) is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Yokohama

</td><td>

Problem Management is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Problem Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

If any specific browser requirements were introduced or changed for Problem Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Review details on accessibility information for Problem Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

If there are specific localization considerations for Problem Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

If there are specific highlight considerations for Problem Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Introduction of Problem Management models to provide support for additional problem and problem task scenarios
-   Known error articles are enabled by default for new customers
-   Configure email notifications to redirect to Service Operations Workspace instead of the classic UI16 experience
-   Re-assess a problem task from Work In Progress

 See [Problem Management](https://servicenow-staging.fluidtopics.net/access?context=c_ProblemManagement&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Increase operational efficiency of tier 1 service desk agents with the dedicated sn\_service\_desk\_agent role.
-   Simplify the management of problems and problem tasks using Problem Management models.

 See [Problem Management](https://servicenow-staging.fluidtopics.net/access?context=c_ProblemManagement&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

