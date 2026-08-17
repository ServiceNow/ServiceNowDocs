---
title: ServiceNow Otto for Configuration Management Database \(CMDB\) release notes
description: The ServiceNow ServiceNow Otto for Configuration Management Database \(CMDB\) application helps to improve the quality of CMDB data, search the CMDB quickly, find and remedy issues with Service Graph Connector import sets, and more. ServiceNow Otto for CMDB was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-07-30"
reading_time_minutes: 5
---

# ServiceNow Otto for Configuration Management Database \(CMDB\) release notes

The ServiceNow® ServiceNow Otto for Configuration Management Database \(CMDB\) application helps to improve the quality of CMDB data, search the CMDB quickly, find and remedy issues with Service Graph Connector import sets, and more. ServiceNow Otto for CMDB was enhanced and updated in the Australia release.

## Now Assist &gt; ServiceNow Otto announcement

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

## ServiceNow Otto for CMDB highlights for the Australia release

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md) The ServiceNow AI Platform now brings you an AI native experience with three licensing tiers available.

-   Get an AI-generated summary of the CMDB success advisor for HAM dashboard, with key findings on CMDB data accuracy, completeness, and health and the suggested remediation actions.
-   Compare your current manual \(static\) IRE processes with AI-powered Dynamic IRE.

-   Automate the actions that a user would typically make for de-duplication tasks using the de-duplication task resolution assistant skill.
-   Search the Service Graph database using natural language.
-   Dive deeply into CI and class information while working in CI forms, dashboards, home pages, and other views on the workspace.

See [ServiceNow Otto for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-landing-cmdb.md) for more information.

**Important:** ServiceNow Otto for CMDB is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading ServiceNow Otto for CMDB to Australia

To enable Now Assist to provide detailed descriptions of CIs and classes, you must activate the 'External Content Connectors' plugin, install the ‘ServiceNow Product Documentation’ connector, and then crawl the product documentation. For configuration instructions, see [Configure the CI form contextual help skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/na-cmdb-skill-form-sense-config.md).

## New in the Australia release

-   **[Analyzing the impact of a change or incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/na-cmdb-awf-impact-analysis-using.md)**

    The Assess CMDB Impact agentic workflow identifies the upstream services and CIs that are likely to be affected by an incident or by a proposed change. The workflow reasons about propagation likelihood based on CMDB dependency topology and the nature of the change. The workflow returns a structured list with impact levels and the reasoning.

-   **[Recommend service graph connector agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/na-cmdb-awf-suggest-sgc-mappings.md)**

    Sometimes you're not sure which integration to use to capture CI data. When you provide Now Assist with the name of a particular CI class, it can recommend the data sources or Service Graph Connectors and ingestion sources that can best populate CMDB data.

-   **[Business application candidate agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/na-cmdb-agent-biz-app-candidate-c.md)**

    The Business application candidate agent discovers and suggests business applications to associate with existing application services in the CMDB, reducing manual mapping effort and improving data governance. The agent uses AI clustering and feedback loops to propose business application candidates for your review.


-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Summarize CMDB readiness with the ServiceNow Otto skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/na-cmdb-skill-summ-rdy.md)**

    View an AI-generated summary of the CMDB success advisor for Hardware Asset Management \(HAM\) dashboard data. The summary highlights the key findings on CMDB data accuracy, completeness, and health, and suggests remediation actions to address the findings.

-   **[View CI attribute descriptions on CI forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/na-cmdb-skill-ci-form-help.md)**

    The skill answers your questions on CI classes and attributes to help you work in CI forms, dashboards, home pages, and other views on the workspace. You can submit similar queries on the Explore CI view.

-   **[CMDB searches can include relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/na-cmdb-awf-search.md)**

    Search queries can depend on relationships between CIs and can span multiple tables. For example, you might ask: "Search for servers that depend on databases - only Linux servers running Redhat".

-   **[Search the Service Graph database using natural language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/na-cmdb-skill-search-result-classfy.md)**

    ServiceNow Otto for CMDB analyzes your search criteria, identifies implicit filters, determines the optimum search method \(keyword search or query generation\), queries Service Graph data, and then displays the results. You then have the option to refine the search using natural language in the Now Assist panel.


## Changed in this release

-   **Now Assist &gt; ServiceNow Otto announcement**

    Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


-   **[Get advice on CMDB governance from ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/na-cmdb-awf-cmdb-governance.md)**

    Correction to the required role for the Provide advice on CMDB governance agentic workflow. The admin or system\_scheduler\_admin role is required.


-   **[New role required for the Create configuration item agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/na-cmdb-awf-ci-creator.md)**

    The sn\_cmdb\_admin role is now required to use the 'Create configuration item' agentic workflow \(was sn\_cmdb\_editor\).

-   **Skills now also require the now\_assist\_panel\_user role**

    AI skills that execute in the Now Assist panel now require both the cmdb\_dedup\_admin and now\_assist\_panel\_user roles.


## Activation information

Install ServiceNow Otto for CMDB by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-rn-landing.md)

