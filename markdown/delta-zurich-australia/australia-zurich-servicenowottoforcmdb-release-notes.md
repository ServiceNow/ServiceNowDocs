---
title: Combined ServiceNow Otto for CMDB release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for ServiceNow Otto for CMDB from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-servicenowottoforcmdb-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Otto for CMDB release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for ServiceNow Otto for CMDB from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Otto for CMDB release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Otto for CMDB to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

The installation \(activation\) process has changed for the ServiceNow Otto for CMDB v2.1 plugin. See [Configure](https://www.servicenow.com/docs/access?context=now-assist-cmdb-configuring&family=zurich&ft:locale=en-US) for the new instructions.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for ServiceNow Otto for CMDB.

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
</table>## Changes

Between your current release family and Australia, some changes were made to existing ServiceNow Otto for CMDB features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Now Assist &gt; ServiceNow Otto announcement](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&family=zurich&ft:locale=en-US)**

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


-   **[Analyzing the impact of a change or incident](https://www.servicenow.com/docs/access?context=na-cmdb-awf-impact-analysis-using&family=zurich&ft:locale=en-US)**

The Assess CMDB Impact agentic workflow identifies the upstream services and CIs that are likely to be affected by an incident or by a proposed change. The workflow reasons about propagation likelihood based on CMDB dependency topology and the nature of the change. The workflow returns a structured list with impact levels and the reasoning.

-   **[Determine which SGC to use](https://www.servicenow.com/docs/access?context=na-cmdb-awf-suggest-sgc-mappings&family=zurich&ft:locale=en-US)**

Sometimes you're not sure which integration to use to capture CI data. When you provide Now Assist with the name of a particular CI class, it can recommend the data sources or Service Graph Connectors and ingestion sources that can best populate CMDB data.

-   **[Business application candidate agent](https://www.servicenow.com/docs/access?context=na-cmdb-agent-biz-app-candidate-c&family=zurich&ft:locale=en-US)**

The Business application candidate agent discovers and suggests business applications to associate with existing application services in the CMDB, reducing manual mapping effort and improving data governance. The agent uses AI clustering and feedback loops to propose business application candidates for your review.


-   **[View CI details on CI forms](https://www.servicenow.com/docs/access?context=na-cmdb-skill-ci-form-help&family=zurich&ft:locale=en-US)**

The skill answers your questions on CI classes and attributes to help you work in CI forms, dashboards, home pages, and other views on the workspace. You can submit similar queries on the Explore CI view.

-   **[CMDB searches can include relationships](https://www.servicenow.com/docs/access?context=na-cmdb-awf-search&family=zurich&ft:locale=en-US)**

Search queries can depend on relationships between CIs and can span multiple tables. For example, you might ask: "Search for servers that depend on databases - only Linux servers running Redhat".


-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**

Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=zurich&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[New role required for the Create configuration item agentic workflow](https://www.servicenow.com/docs/access?context=na-cmdb-awf-ci-creator&family=zurich&ft:locale=en-US)**

The sn\_cmdb\_admin role is now required to use the Create configuration item agentic workflow \(was sn\_cmdb\_editor\).

-   ****
-   **[Create a CI](https://www.servicenow.com/docs/access?context=na-cmdb-awf-ci-creator&family=zurich&ft:locale=en-US)**

Verbal interaction with this feature has improved. Occasionally, you might need to create a CI manually. To help you, the CI creator agentic workflow accepts your natural language request and verifies that it understands which class the new CI should belong to. The workflow then checks Identification and Reconciliation engine \(IRE\) rules to determine the required attributes for the CI and requests that information. After you provide sufficient data, the workflow helps to ensure that the proposed CI includes the attributes that you requested, complies with IRE rules, and is not a duplicate. The workflow then creates the CI.

-   **[Advice on CMDB governance](https://www.servicenow.com/docs/access?context=na-cmdb-awf-governance&family=zurich&ft:locale=en-US)**

To help users understand the value of each step in the process, responses now include richer context. The CMDB Governance agentic workflow supports administrators and service owners by improving CMDB data governance. Before starting in on each governance task, the workflow presents the reasons for the task to help you better understand the importance and benefits of the activity. The objective is to ensure that CMDB data is accurate and complete so that users can trust the data.

-   **[Search the CMDB](https://www.servicenow.com/docs/access?context=na-cmdb-awf-search&family=zurich&ft:locale=en-US)**

Verbal interaction with this feature has improved. Users can now select the CI inline when multiple CIs are returned as matches. A summary of the CI now appears in the conversation. The CMDB search agentic workflow enables you to search for CIs by specifying any of several attributes of the CI of interest. The workflow accepts your natural language request, verifies your search goal, and then generates a keyword search, a single-table search with dot walks, or a multi-table search, depending on the information that you provided. The workflow can infer CI relationship data to generate an appropriate query.

-   **[Summarize CI data](https://www.servicenow.com/docs/access?context=na-cmdb-agent-ci-summarizer&family=zurich&ft:locale=en-US)**

Verbal interaction with this feature has improved. You can now view a concise summary of the key CI data by selecting the CI on a CI form, in a workspace page, or on any list view. The summary can include discovery data, ownership, and key related items such as open incidents, alerts, problems, upcoming change requests, and security vulnerabilities. Additionally, the summary lists the service instances that the CI is part of.

-   **[\[Placeholder link text to key now-assist-cmdb-mng-dupe-cis-skill\]](https://www.servicenow.com/docs/access?context=now-assist-cmdb-mng-dupe-cis-skill&family=zurich&ft:locale=en-US)**

Resolve de-duplication tasks with support from the Now Assist Manage duplicate CIs skill. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template.

-   **[Diagnose failed SGC import sets](https://www.servicenow.com/docs/access?context=now-assist-sgc-diagnose&family=zurich&ft:locale=en-US)**

Verbal interaction with this feature has improved. You can now diagnose a failed import set that is associated with a Service Graph Connector to get a summary of the errors and recommendations for resolving the issues.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ServiceNow Otto for CMDB features or functionality were removed.

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

Between your current release family and Australia, some ServiceNow Otto for CMDB features or functionality were deprecated.

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

Review information on how to activate ServiceNow Otto for CMDB.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

ServiceNow Otto for CMDB is a ServiceNow AI Platform feature that is available with activation of plugins that you get from the ServiceNow Store. For details, see [Configure](https://www.servicenow.com/docs/access?context=now-assist-cmdb-configuring&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Otto for CMDB we have noted them here.

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

If any specific browser requirements were introduced or changed for ServiceNow Otto for CMDB we have noted them here.

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

Review details on accessibility information for ServiceNow Otto for CMDB, such as specific requirements or compliance levels.

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

If there are specific localization considerations for ServiceNow Otto for CMDB we have noted them here.

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

If there are specific highlight considerations for ServiceNow Otto for CMDB we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

[Zurich Patch 11](https://www.servicenow.com/docs/access?context=zurich-patch-11&family=zurich&ft:locale=en-US)

-   AI identifies the upstream services and CIs that are likely to be affected by an incident or by a proposed change.
-   AI recommends the data sources or Service Graph Connectors and ingestion sources that can best populate CMDB data.
-   AI discovers and suggests business applications to associate with existing application services in the CMDB, reducing manual mapping effort and improving data governance.

 [Zurich Patch 7](https://www.servicenow.com/docs/access?context=zurich-patch-7&family=zurich&ft:locale=en-US)

-   Get AI-powered answers your questions on CI classes and attributes to help you work in CI forms, dashboards, home pages, and other views on the workspace.
-   Search queries can now span multiple tables and relationships between CIs.

 [Zurich Patch 5](https://www.servicenow.com/docs/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement

 [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Some Now Assist skills and agentic workflows are now turned on by default.
-   Agentic workflows and AI agents included with Now Assist applications now require additional security configuration.
-   Reduce the debugging time and effort when you resolve issues with Service Graph Connector import sets.
-   Find and resolve de-duplication tasks.
-   Speed the process of manually creating CIs.
-   Methodically work through the process of improving CMDB data governance.
-   Search for CIs by specifying any of several attributes of the CI of interest.
-   View a concise summary of the key CI data on a CI form in a workspace page or on any list view.

 [Zurich Patch 3](https://www.servicenow.com/docs/access?context=zurich-patch-3&family=zurich&ft:locale=en-US)

 [Zurich Patch 2](https://www.servicenow.com/docs/access?context=zurich-patch-2&family=zurich&ft:locale=en-US)

 [Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

 See [ServiceNow Otto for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

