---
title: Combined Process Mining release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Process Mining from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-processmining-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Process Mining release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Process Mining from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Process Mining release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Process Mining to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Process Mining.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Process Mining evaluation version available](https://www.servicenow.com/docs/access?context=process-mining&family=xanadu&ft:locale=en-US)**

Try sample mining and limited features on the Incident table without an entitlement so you can decide whether the advanced features are beneficial to your organization.

-   **[Process Mining graph enhanced with perspectives](https://www.servicenow.com/docs/access?context=set-perspective&family=xanadu&ft:locale=en-US)**

Filter the Process Mining graph by the activity definitions you want to view at a particular time.

-   **[Understanding the root cause of inefficiency made easier](https://www.servicenow.com/docs/access?context=annotate-project&family=xanadu&ft:locale=en-US)**

Generate a summary of all work notes to see the history of the inefficiency rather than having to read each individual work note separately.

-   **[Configure finding definitions](https://www.servicenow.com/docs/access?context=configuring-finding-definitions&family=xanadu&ft:locale=en-US)**

Configure and view automated and rule-based finding definitions efficiently using a comprehensive guided setup.

-   **[Include additional use case analysis in a project automatically](https://www.servicenow.com/docs/access?context=adv-settings&family=xanadu&ft:locale=en-US)**

Set Approval analysis or SLA breach analysis automatically for applicable processes when creating a project so you don't need to make this selection manually.

-   **[Variation analysis introduced in Summary and Insights page](https://www.servicenow.com/docs/access?context=summary-insights-dashboard&family=xanadu&ft:locale=en-US)**

Analyze various routes the records in the process took based on parameters like mostly traversed, more steps, and so on. This information is accessible on the Summary and Insights page.

-   **[Customize the outline of the process mining graph dashboard](https://www.servicenow.com/docs/access?context=analyst-workbench-dashboard&family=xanadu&ft:locale=en-US)**

Customize the orientation of the outline of the process graph set for the current project workbench for nodes within the graph. For example, when using a vertically oriented widget, you might prefer the graph and star diagram to be displayed in a vertical layout rather than a horizontal one.

-   **[Inflow and outflow analysis: node star diagram](https://www.servicenow.com/docs/access?context=node-diagram&family=xanadu&ft:locale=en-US)**

View the records for any node or arc from the map dashboard.

-   **[Option to filter out incoming or outgoing arcs](https://www.servicenow.com/docs/access?context=analyst-workbench-dashboard&family=xanadu&ft:locale=en-US)**

View only incoming or only outgoing arcs to see the inflow/outflow of work for a particular process with respect to other related processes on the graph.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Now Assist based work notes analysis](https://www.servicenow.com/docs/access?context=worknotes-analysis&family=yokohama&ft:locale=en-US)**

Work notes analysis is now enhanced using Now Assist to understand the operational reasons behind activity transitions by examining the work notes and comments recorded around the time of these transitions.

-   **[Process configuration builder introduced](https://www.servicenow.com/docs/access?context=create-process-config&family=yokohama&ft:locale=en-US)**

Configure and view the process configurations efficiently by using the new comprehensive Process configuration builder. It is a guided setup to configure and view the process configurations.

-   **[Content pack importer introduced for process configurations](https://www.servicenow.com/docs/access?context=po-content-pack&family=yokohama&ft:locale=en-US)**

Import and customize the content pack process configuration templates to activate new features. Content pack process configuration templates are now read-only.

-   **[Process Mining evaluation project available for HR and CSM](https://www.servicenow.com/docs/access?context=evaluation-pm-inci-manag&family=yokohama&ft:locale=en-US)**

Ability to try out the sample mining and limited features available for HR and CSM without an entitlement. For the advanced features, you can purchase a license.

-   **[Access control \(ACL\) rules updated](https://www.servicenow.com/docs/access?context=access-control&family=yokohama&ft:locale=en-US)**

The ACL rules have been updated for broader visibility on the try-out version while also increasing the security.

    -   No Process Mining role is required to access a shared project and to generate Platform Analytics insights for some tables.
    -   Some breakdown filters or activity definitions are blocked for certain users based on the column access.
-   **[Process Mining performance improved](https://www.servicenow.com/docs/access?context=analyst-workbench-overview&family=yokohama&ft:locale=en-US)**

The following improvements boost Process Mining performance and lead to quicker insights:

    -   Introduced lazy loading of improvement opportunities and variants for faster workspace loading.
    -   Introduced applying a transition filter before mining to reduce scope of data and speed up the mining process.
    -   Improved Process Mining workbench load time.
-   **[Transition filters enhanced](https://www.servicenow.com/docs/access?context=node-to-node-conditions&family=yokohama&ft:locale=en-US)**

The enhanced transition filters now provide more flexibility and precision in filtering the process map by providing the following:

    -   Ability to use `OR` clause on steps to create a more complex and nuanced criteria for process transitions.
    -   Include predicates like "is empty" and "is not empty" allowing for more refined control over the conditions under which transitions occur, ensuring that workflows are both comprehensive and adaptable to a variety of scenarios.
    -   Ability to select more than one value with a single click that contains a specific text.
-   **[Enhanced the Process Mining engine](https://www.servicenow.com/docs/access?context=set-activity-def&family=yokohama&ft:locale=en-US)**

Key updates include:

    -   Defining integer fields as activity definitions.
    -   Grouping journal fields to identify how quickly an agent reacted to an assigned case.
    -   Defining the order of simultaneous activities on the graph.
-   **[Addition﻿al breakdown capacity for Process Mining on external data](https://www.servicenow.com/docs/access?context=external-dataset&family=yokohama&ft:locale=en-US)**

Ability to import a maximum of 10 breakdown fields enabling to segment and analyze specific subsets of the external process data using Process Mining.

-   **[API for accessing Process Mining data](https://www.servicenow.com/docs/access?context=define-workflow-model&family=yokohama&ft:locale=en-US)**

Create, mine, and access Process Mining data via an API \(ProcessMiningIntegrationAPI\). For more information, see the API documentation.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Process Mining features.

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

</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Process Mining features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Process Mining features or functionality were deprecated.

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Process Mining.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Process Mining is available with activation of the sn\_po plugin.

</td></tr><tr><td>

Yokohama

</td><td>

Process Mining is available with activation of the sn\_po plugin. For details, see [Activating Process Optimization](https://www.servicenow.com/docs/access?context=activating-process-mining&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Process Mining we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Process Mining we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Process Mining, such as specific requirements or compliance levels.

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

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Process Mining we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Process Mining we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Process Mining evaluation version available
-   Process Mining graph enhanced with perspectives
-   Finding Builder introduced
-   Additional use case analysis included in a project automatically
-   **Show records** action available on Process Mining graph dashboard \(Star diagram\)

 See [Process Optimization](https://www.servicenow.com/docs/access?context=process-mining&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Now Assist based work notes analysis
-   Process configuration builder introduced
-   Content pack importer introduced for process configurations
-   Process Mining evaluation project available for HR and CSM
-   Access control \(ACL\) rules updated

 See [Process Optimization](https://www.servicenow.com/docs/access?context=process-mining&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

