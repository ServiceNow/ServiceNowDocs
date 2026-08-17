---
title: Combined ServiceNow Otto for Configuration Management Database \(CMDB\) release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for ServiceNow Otto for Configuration Management Database \(CMDB\) from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-servicenowottoforconfigurationmanagementdatabasecmdb-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Otto for Configuration Management Database \(CMDB\) release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for ServiceNow Otto for Configuration Management Database \(CMDB\) from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Otto for Configuration Management Database \(CMDB\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Otto for Configuration Management Database \(CMDB\) to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

To enable Now Assist to provide detailed descriptions of CIs and classes, you must activate the 'External Content Connectors' plugin, install the ‘ServiceNow Product Documentation’ connector, and then crawl the product documentation. For configuration instructions, see [Configure the CI form contextual help skill](https://www.servicenow.com/docs/access?context=na-cmdb-skill-form-sense-config&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for ServiceNow Otto for Configuration Management Database \(CMDB\).

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

-   **[Analyzing the impact of a change or incident](https://www.servicenow.com/docs/access?context=na-cmdb-awf-impact-analysis-using&family=australia&ft:locale=en-US)**

The Assess CMDB Impact agentic workflow identifies the upstream services and CIs that are likely to be affected by an incident or by a proposed change. The workflow reasons about propagation likelihood based on CMDB dependency topology and the nature of the change. The workflow returns a structured list with impact levels and the reasoning.

-   **[Determine which SGC to use](https://www.servicenow.com/docs/access?context=na-cmdb-awf-suggest-sgc-mappings&family=australia&ft:locale=en-US)**

Sometimes you're not sure which integration to use to capture CI data. When you provide Now Assist with the name of a particular CI class, it can recommend the data sources or Service Graph Connectors and ingestion sources that can best populate CMDB data.

-   **[Business application candidate agent](https://www.servicenow.com/docs/access?context=na-cmdb-agent-biz-app-candidate-c&family=australia&ft:locale=en-US)**

The Business application candidate agent discovers and suggests business applications to associate with existing application services in the CMDB, reducing manual mapping effort and improving data governance. The agent uses AI clustering and feedback loops to propose business application candidates for your review.


-   ****

-   **[Summarize CMDB readiness](https://www.servicenow.com/docs/access?context=na-cmdb-skill-summ-rdy&family=australia&ft:locale=en-US)**

View an AI-generated summary of the CMDB success advisor for Hardware Asset Management \(HAM\) dashboard data. The summary highlights the key findings on CMDB data accuracy, completeness, and health, and suggests remediation actions to address the findings.

-   **[View CI details on CI forms](https://www.servicenow.com/docs/access?context=na-cmdb-skill-ci-form-help&family=australia&ft:locale=en-US)**

The skill answers your questions on CI classes and attributes to help you work in CI forms, dashboards, home pages, and other views on the workspace. You can submit similar queries on the Explore CI view.

-   **[CMDB searches can include relationships](https://www.servicenow.com/docs/access?context=na-cmdb-awf-search&family=australia&ft:locale=en-US)**

Search queries can depend on relationships between CIs and can span multiple tables. For example, you might ask: "Search for servers that depend on databases - only Linux servers running Redhat".

-   **[Search the Service Graph database](https://www.servicenow.com/docs/access?context=na-cmdb-skill-search-result-classfy&family=australia&ft:locale=en-US)**

ServiceNow Otto for CMDB analyzes your search criteria, identifies implicit filters, determines the optimum search method \(keyword search or query generation\), queries Service Graph data, and then displays the results. You then have the option to refine the search using natural language in the Now Assist panel.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ServiceNow Otto for Configuration Management Database \(CMDB\) features.

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

-   **Now Assist &gt; ServiceNow Otto announcement**




-   **[Get advice on CMDB governance](https://www.servicenow.com/docs/access?context=na-cmdb-awf-cmdb-governance&family=australia&ft:locale=en-US)**

Correction to the required role for the Provide advice on CMDB governance agentic workflow. The admin or system\_scheduler\_admin role is required.


-   **[New role required for the Create configuration item agentic workflow](https://www.servicenow.com/docs/access?context=na-cmdb-awf-ci-creator&family=australia&ft:locale=en-US)**

The sn\_cmdb\_admin role is now required to use the 'Create configuration item' agentic workflow \(was sn\_cmdb\_editor\).

-   **Skills now also require the now\_assist\_panel\_user role**

AI skills that execute in the Now Assist panel now require both the cmdb\_dedup\_admin and now\_assist\_panel\_user roles.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ServiceNow Otto for Configuration Management Database \(CMDB\) features or functionality were removed.

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

Between your current release family and Australia, some ServiceNow Otto for Configuration Management Database \(CMDB\) features or functionality were deprecated.

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

Review information on how to activate ServiceNow Otto for Configuration Management Database \(CMDB\).

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

Install ServiceNow Otto for CMDB by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Otto for Configuration Management Database \(CMDB\) we have noted them here.

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

If any specific browser requirements were introduced or changed for ServiceNow Otto for Configuration Management Database \(CMDB\) we have noted them here.

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

Review details on accessibility information for ServiceNow Otto for Configuration Management Database \(CMDB\), such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for ServiceNow Otto for Configuration Management Database \(CMDB\) we have noted them here.

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

If there are specific highlight considerations for ServiceNow Otto for Configuration Management Database \(CMDB\) we have noted them here.

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

[Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US) The ServiceNow AI Platform now brings you an AI native experience with three licensing tiers available.

 -   Get an AI-generated summary of the CMDB success advisor for HAM dashboard, with key findings on CMDB data accuracy, completeness, and health and the suggested remediation actions.
-   Compare your current manual \(static\) IRE processes with AI-powered Dynamic IRE.

-   Automate the actions that a user would typically make for de-duplication tasks using the de-duplication task resolution assistant skill.
-   Search the Service Graph database using natural language.
-   Dive deeply into CI and class information while working in CI forms, dashboards, home pages, and other views on the workspace.

 See [ServiceNow Otto for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

