---
title: Combined Process Mining release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Process Mining from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-processmining-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Process Mining release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Process Mining from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Process Mining release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Process Mining to Zurich

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

Between your current release family and Zurich, new features were introduced for Process Mining.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Process Mining evaluation version available](https://servicenow-staging.fluidtopics.net/access?context=process-mining&family=xanadu&ft:locale=en-US)**

Try sample mining and limited features on the Incident table without an entitlement so you can decide whether the advanced features are beneficial to your organization.

-   **[Process Mining graph enhanced with perspectives](https://servicenow-staging.fluidtopics.net/access?context=set-perspective&family=xanadu&ft:locale=en-US)**

Filter the Process Mining graph by the activity definitions you want to view at a particular time.

-   **[Understanding the root cause of inefficiency made easier](https://servicenow-staging.fluidtopics.net/access?context=annotate-project&family=xanadu&ft:locale=en-US)**

Generate a summary of all work notes to see the history of the inefficiency rather than having to read each individual work note separately.

-   **[Configure finding definitions](https://servicenow-staging.fluidtopics.net/access?context=configuring-finding-definitions&family=xanadu&ft:locale=en-US)**

Configure and view automated and rule-based finding definitions efficiently using a comprehensive guided setup.

-   **[Include additional use case analysis in a project automatically](https://servicenow-staging.fluidtopics.net/access?context=adv-settings&family=xanadu&ft:locale=en-US)**

Set Approval analysis or SLA breach analysis automatically for applicable processes when creating a project so you don't need to make this selection manually.

-   **[Variation analysis introduced in Summary and Insights page](https://servicenow-staging.fluidtopics.net/access?context=summary-insights-dashboard&family=xanadu&ft:locale=en-US)**

Analyze various routes the records in the process took based on parameters like mostly traversed, more steps, and so on. This information is accessible on the Summary and Insights page.

-   **[Customize the outline of the process mining graph dashboard](https://servicenow-staging.fluidtopics.net/access?context=analyst-workbench-dashboard&family=xanadu&ft:locale=en-US)**

Customize the orientation of the outline of the process graph set for the current project workbench for nodes within the graph. For example, when using a vertically oriented widget, you might prefer the graph and star diagram to be displayed in a vertical layout rather than a horizontal one.

-   **[Inflow and outflow analysis: node star diagram](https://servicenow-staging.fluidtopics.net/access?context=node-diagram&family=xanadu&ft:locale=en-US)**

View the records for any node or arc from the map dashboard.

-   **[Option to filter out incoming or outgoing arcs](https://servicenow-staging.fluidtopics.net/access?context=analyst-workbench-dashboard&family=xanadu&ft:locale=en-US)**

View only incoming or only outgoing arcs to see the inflow/outflow of work for a particular process with respect to other related processes on the graph.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Now Assist based work notes analysis](https://servicenow-staging.fluidtopics.net/access?context=worknotes-analysis&family=yokohama&ft:locale=en-US)**

Work notes analysis is now enhanced using Now Assist to understand the operational reasons behind activity transitions by examining the work notes and comments recorded around the time of these transitions.

-   **[Process configuration builder introduced](https://servicenow-staging.fluidtopics.net/access?context=create-process-config&family=yokohama&ft:locale=en-US)**

Configure and view the process configurations efficiently by using the new comprehensive Process configuration builder. It is a guided setup to configure and view the process configurations.

-   **[Content pack importer introduced for process configurations](https://servicenow-staging.fluidtopics.net/access?context=po-content-pack&family=yokohama&ft:locale=en-US)**

Import and customize the content pack process configuration templates to activate new features. Content pack process configuration templates are now read-only.

-   **[Process Mining evaluation project available for HR and CSM](https://servicenow-staging.fluidtopics.net/access?context=evaluation-pm-inci-manag&family=yokohama&ft:locale=en-US)**

Ability to try out the sample mining and limited features available for HR and CSM without an entitlement. For the advanced features, you can purchase a license.

-   **[Access control \(ACL\) rules updated](https://servicenow-staging.fluidtopics.net/access?context=access-control&family=yokohama&ft:locale=en-US)**

The ACL rules have been updated for broader visibility on the try-out version while also increasing the security.

    -   No Process Mining role is required to access a shared project and to generate Platform Analytics insights for some tables.
    -   Some breakdown filters or activity definitions are blocked for certain users based on the column access.
-   **[Process Mining performance improved](https://servicenow-staging.fluidtopics.net/access?context=analyst-workbench-overview&family=yokohama&ft:locale=en-US)**

The following improvements boost Process Mining performance and lead to quicker insights:

    -   Introduced lazy loading of improvement opportunities and variants for faster workspace loading.
    -   Introduced applying a transition filter before mining to reduce scope of data and speed up the mining process.
    -   Improved Process Mining workbench load time.
-   **[Transition filters enhanced](https://servicenow-staging.fluidtopics.net/access?context=node-to-node-conditions&family=yokohama&ft:locale=en-US)**

The enhanced transition filters now provide more flexibility and precision in filtering the process map by providing the following:

    -   Ability to use `OR` clause on steps to create a more complex and nuanced criteria for process transitions.
    -   Include predicates like "is empty" and "is not empty" allowing for more refined control over the conditions under which transitions occur, ensuring that workflows are both comprehensive and adaptable to a variety of scenarios.
    -   Ability to select more than one value with a single click that contains a specific text.
-   **[Enhanced the Process Mining engine](https://servicenow-staging.fluidtopics.net/access?context=set-activity-def&family=yokohama&ft:locale=en-US)**

Key updates include:

    -   Defining integer fields as activity definitions.
    -   Grouping journal fields to identify how quickly an agent reacted to an assigned case.
    -   Defining the order of simultaneous activities on the graph.
-   **[Addition﻿al breakdown capacity for Process Mining on external data](https://servicenow-staging.fluidtopics.net/access?context=external-dataset&family=yokohama&ft:locale=en-US)**

Ability to import a maximum of 10 breakdown fields enabling to segment and analyze specific subsets of the external process data using Process Mining.

-   **[API for accessing Process Mining data](https://servicenow-staging.fluidtopics.net/access?context=define-workflow-model&family=yokohama&ft:locale=en-US)**

Create, mine, and access Process Mining data via an API \(ProcessMiningIntegrationAPI\). For more information, see the API documentation.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Opportunity details page](https://servicenow-staging.fluidtopics.net/access?context=opportunity-details&family=zurich&ft:locale=en-US)**

Generate highlights to surface key drivers behind process patterns that accelerate decision-making and prioritization of process changes on the Opportunity details page. This page provides the detailed context of every improvement opportunity. It uses Now Assist to help generate highlights.

-   **[Idle time analysis](https://servicenow-staging.fluidtopics.net/access?context=idle-time-analysis&family=zurich&ft:locale=en-US)**

Analyze where cases are waiting to be assigned to agents by tracking and analyzing the time during which the case is assigned to a team but not yet to an agent. Idle time analysis helps identify inefficiencies, such as delays in task assignment or workflow bottlenecks, and helps improve coordination and reduce waiting time within processes. Idle time analysis must be configured in the process configuration.

-   **[Touchpoint analysis](https://servicenow-staging.fluidtopics.net/access?context=touchpoint-analysis&family=zurich&ft:locale=en-US)**

Identify where and how human involvement occurs in a process by using touchpoint analysis. Analyzing the fields that involves human involvement helps you improve your processes, enhancing performance and reducing operational costs. Touchpoint analysis enables you to analyze the workload of transitions and cases. Touchpoint analysis must be configured in the process configuration.

-   **[Enhanced data security](https://servicenow-staging.fluidtopics.net/access?context=set-objectives&family=zurich&ft:locale=en-US)**

Mark a project as restricted to help protect sensitive data and avoid security breaches. Restricted project data is available only to the owner and the users with whom the project is shared.

-   **[Share a Process Optimization project](https://servicenow-staging.fluidtopics.net/access?context=share-project&family=zurich&ft:locale=en-US)**

Share projects through a link that remains unchanged even when the project is updated and remined.

-   **[Creation of automation requests and CIMs simplified](https://servicenow-staging.fluidtopics.net/access?context=submit-automation-idea&family=zurich&ft:locale=en-US)**

When creating an automation or Continual Improvement Management \(CIM\) request from Process Mining, mandatory fields are pre-populated, reducing friction and accelerating time-to-action.

-   **[Process Mining integrated with ServiceNow playbook](https://servicenow-staging.fluidtopics.net/access?context=analyst-workbench-dashboard&family=zurich&ft:locale=en-US)**

Process Mining has been integrated with ServiceNow playbook. After analyzing and identifying a process for improvement, export the process to playbook and add subflows or triggers to analyze and refine the flow.

Use the Playbooks icon on the Process Mining Analyst Workbench to export up to 5 routes of a project to ServiceNow playbook. This feature is enabled by Now Assist.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Process Mining features.

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
</table>## Removed

Between your current release family and Zurich, some Process Mining features or functionality were removed.

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

Between your current release family and Zurich, some Process Mining features or functionality were deprecated.

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

Process Mining is available with activation of the sn\_po plugin. For details, see [Activating Process Optimization](https://servicenow-staging.fluidtopics.net/access?context=activating-process-mining&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Process Mining is available by default. For details, see [Activating Process Optimization](https://servicenow-staging.fluidtopics.net/access?context=activating-process-mining&family=zurich&ft:locale=en-US).

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

</td></tr><tr><td>

Zurich

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

</td></tr><tr><td>

Zurich

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

</td></tr><tr><td>

Zurich

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

</td></tr><tr><td>

Zurich

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

 See [Process Optimization](https://servicenow-staging.fluidtopics.net/access?context=process-mining&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Now Assist based work notes analysis
-   Process configuration builder introduced
-   Content pack importer introduced for process configurations
-   Process Mining evaluation project available for HR and CSM
-   Access control \(ACL\) rules updated

 See [Process Optimization](https://servicenow-staging.fluidtopics.net/access?context=process-mining&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Generate highlights of the improvement opportunities in the Opportunity details page.
-   Identify inefficiencies by focusing on the delays in task assignment by using idle time analysis.
-   Analyze the workload of transitions and cases by using touchpoint analysis.
-   Enhance data security by marking projects as restricted.
-   Process Mining is integrated with ServiceNow playbook.

 See [Process Optimization](https://servicenow-staging.fluidtopics.net/access?context=process-mining&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

