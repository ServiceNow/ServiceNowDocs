---
title: Combined ServiceNow Otto for Configuration Management Database \(CMDB\) release notes for upgrades from Yokohama to Brazil
description: Consolidated page of all release notes for ServiceNow Otto for Configuration Management Database \(CMDB\) from Yokohama to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-brazil/brazil-yokohama-servicenowottoforconfigurationmanagementdatabasecmdb-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 15
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Otto for Configuration Management Database \(CMDB\) release notes for upgrades from Yokohama to Brazil

Consolidated page of all release notes for ServiceNow Otto for Configuration Management Database \(CMDB\) from Yokohama to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Otto for Configuration Management Database \(CMDB\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Otto for Configuration Management Database \(CMDB\) to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Upgrade information**

To enable Now Assist to provide detailed descriptions of CIs and classes, you must activate the 'External Content Connectors' plugin, install the ‘ServiceNow Product Documentation’ connector, and then crawl the product documentation. For configuration instructions, see [Configure the CI form contextual help skill](https://www.servicenow.com/docs/access?context=na-cmdb-skill-form-sense-config&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for ServiceNow Otto for Configuration Management Database \(CMDB\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Preview deduplication template results](https://www.servicenow.com/docs/access?context=now-assist-cmdb-mng-dupe-cis-skill&family=yokohama&ft:locale=en-US)**

While you're working in the manage duplicate CIs skill, select **Review existing templates** to help you to decide which deduplication template to apply. Now Assist generates a summary of the results of applying a template without actually running the remediation process. You can preview the results for any existing template. When you see the desired result in a preview, you can specify that template and proceed with the deduplication process.


</td></tr><tr><td>

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

-   **[\[Placeholder link text to key bundle-platcap.na-cmdb-agent-biz-app-candidate-c\]](https://www.servicenow.com/docs/access?context=na-cmdb-agent-biz-app-candidate-c&family=australia&ft:locale=en-US)**

The Business application candidate agent discovers and suggests business applications to associate with existing application services in the CMDB, reducing manual mapping effort and improving data governance. The agent uses AI clustering and feedback loops to propose business application candidates for your review.


 -   **[Summarize CMDB readiness](https://www.servicenow.com/docs/access?context=na-cmdb-skill-summ-rdy&family=australia&ft:locale=en-US)**

View an AI-generated summary of the CMDB success advisor for Hardware Asset Management \(HAM\) dashboard data. The summary highlights the key findings on CMDB data accuracy, completeness, and health, and suggests remediation actions to address the findings.


 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


 -   **[Search the Service Graph database](https://www.servicenow.com/docs/access?context=na-cmdb-skill-search-result-classfy&family=australia&ft:locale=en-US)**

ServiceNow Otto for CMDB analyzes your search criteria, identifies implicit filters, determines the optimum search method \(keyword search or query generation\), queries Service Graph data, and then displays the results. You then have the option to refine the search using natural language in the Now Assist panel.


 -   **[View CI details on CI forms](https://www.servicenow.com/docs/access?context=na-cmdb-skill-ci-form-help&family=australia&ft:locale=en-US)**

The skill answers your questions on CI classes and attributes to help you work in CI forms, dashboards, home pages, and other views on the workspace. You can submit similar queries on the Explore CI view.

-   **[CMDB searches can include relationships](https://www.servicenow.com/docs/access?context=na-cmdb-awf-search&family=australia&ft:locale=en-US)**

Search queries can depend on relationships between CIs and can span multiple tables. For example, you might ask: "Search for servers that depend on databases - only Linux servers running Redhat".


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing ServiceNow Otto for Configuration Management Database \(CMDB\) features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&family=yokohama&ft:locale=en-US)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Now Assist &gt; ServiceNow Otto announcement](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&family=zurich&ft:locale=en-US)**

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


 -   **[Analyzing the impact of a change or incident](https://www.servicenow.com/docs/access?context=na-cmdb-awf-impact-analysis-using&family=zurich&ft:locale=en-US)**

The Assess CMDB Impact agentic workflow identifies the upstream services and CIs that are likely to be affected by an incident or by a proposed change. The workflow reasons about propagation likelihood based on CMDB dependency topology and the nature of the change. The workflow returns a structured list with impact levels and the reasoning.

-   **[Determine which SGC to use](https://www.servicenow.com/docs/access?context=na-cmdb-awf-suggest-sgc-mappings&family=zurich&ft:locale=en-US)**

Sometimes you're not sure which integration to use to capture CI data. When you provide Now Assist with the name of a particular CI class, it can recommend the data sources or Service Graph Connectors and ingestion sources that can best populate CMDB data.

-   **[\[Placeholder link text to key bundle-platcap.na-cmdb-agent-biz-app-candidate-c\]](https://www.servicenow.com/docs/access?context=na-cmdb-agent-biz-app-candidate-c&family=zurich&ft:locale=en-US)**

The Business application candidate agent discovers and suggests business applications to associate with existing application services in the CMDB, reducing manual mapping effort and improving data governance. The agent uses AI clustering and feedback loops to propose business application candidates for your review.


 -   **[View CI details on CI forms](https://www.servicenow.com/docs/access?context=na-cmdb-skill-ci-form-help&family=zurich&ft:locale=en-US)**

The skill answers your questions on CI classes and attributes to help you work in CI forms, dashboards, home pages, and other views on the workspace. You can submit similar queries on the Explore CI view.

-   **[CMDB searches can include relationships](https://www.servicenow.com/docs/access?context=na-cmdb-awf-search&family=zurich&ft:locale=en-US)**

Search queries can depend on relationships between CIs and can span multiple tables. For example, you might ask: "Search for servers that depend on databases - only Linux servers running Redhat".


 -   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**

Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


 -   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&family=zurich&ft:locale=en-US)**

Agentic workflows and AI agents included with your applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. See the documentation for the agentic workflow or AI agent for the specific roles you must add.

-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=zurich&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[New role required for the Create configuration item agentic workflow](https://www.servicenow.com/docs/access?context=na-cmdb-awf-ci-creator&family=zurich&ft:locale=en-US)**

The sn\_cmdb\_admin role is now required to use the Create configuration item agentic workflow \(was sn\_cmdb\_editor\).

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

-   **Now Assist &gt; ServiceNow Otto announcement**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


 -   **[Get advice on CMDB governance](https://www.servicenow.com/docs/access?context=na-cmdb-awf-cmdb-governance&family=australia&ft:locale=en-US)**

Correction to the required role for the Provide advice on CMDB governance agentic workflow. The admin or system\_scheduler\_admin role is required.


 -   **[New role required for the Create configuration item agentic workflow](https://www.servicenow.com/docs/access?context=na-cmdb-awf-ci-creator&family=australia&ft:locale=en-US)**

The sn\_cmdb\_admin role is now required to use the 'Create configuration item' agentic workflow \(was sn\_cmdb\_editor\).

-   **Skills now also require the now\_assist\_panel\_user role**

AI skills that execute in the Now Assist panel now require both the cmdb\_dedup\_admin and now\_assist\_panel\_user roles.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some ServiceNow Otto for Configuration Management Database \(CMDB\) features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some ServiceNow Otto for Configuration Management Database \(CMDB\) features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Yokohama

</td><td>

-   **Activation information**

Install ServiceNow Otto for CMDB by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


**Important:** ServiceNow Otto for CMDB is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install ServiceNow Otto for CMDB by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** ServiceNow Otto for CMDB is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Otto for Configuration Management Database \(CMDB\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Yokohama

</td><td>

[Yokohama Patch 11](https://www.servicenow.com/docs/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

 Previous Patch releases

-   Select **Summarize** on a CI form, in the workspace, or from any list to view a concise summary of key CI data directly on the form: discovery and class details, associated business services, security vulnerabilities, and related records like incidents, alerts, problems, and change requests.
-   The 'Manage duplicate CIs' skill identifies duplicate CIs, populates remediation tasks, and then assigns the tasks to the appropriate group. You follow step-by-step guidance and can preview remediation results before selecting a template. The updated CI correctness scores enable the CMDB Health Dashboard to display accurate information.

 See [ServiceNow Otto for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-yokohama-brazil/rn-combined-intro.md)

