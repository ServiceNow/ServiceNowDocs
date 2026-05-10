---
title: Now Assist for Configuration Management Database \(CMDB\) release notes
description: The ServiceNow Now Assist for Configuration Management Database \(CMDB\) application helps to improve the quality of CMDB data, search the CMDB quickly, find and remedy issues with Service Graph Connector import sets, and more. Now Assist for CMDB was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Now Assist for Configuration Management Database \(CMDB\) release notes

The ServiceNow® Now Assist for Configuration Management Database \(CMDB\) application helps to improve the quality of CMDB data, search the CMDB quickly, find and remedy issues with Service Graph Connector import sets, and more. Now Assist for CMDB was enhanced and updated in the Australia release.

## Now Assist for CMDB highlights for the Australia release

[Australia Patch 1](../quality/australia-patch-1.md) The ServiceNow AI Platform now brings you an AI native experience with three licensing tiers available.

-   Compare your current manual \(static\) IRE processes with AI-powered Dynamic IRE.

-   Automate the actions that a user would typically make for de-duplication tasks using the de-duplication task resolution assistant skill.
-   Search the Service Graph database using natural language.
-   Dive deeply into CI and class information while working in CI forms, dashboards, home pages, and other views on the workspace.
-   Search the Service Graph database using natural language

See [Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-landing-cmdb.md) for more information.

**Important:** Now Assist for CMDB is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist for CMDB to Australia

To enable Now Assist to provide detailed descriptions of CIs and classes, you must activate the 'External Content Connectors' plugin, install the ‘ServiceNow Product Documentation’ connector, and then crawl the product documentation. For configuration instructions, see [Configure the CI form contextual help skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-form-sense-config.md).

## New in the Australia release

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[View CI attribute descriptions on CI forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-ci-form-help.md)**

    The skill answers your questions on CI classes and attributes to help you work in CI forms, dashboards, home pages, and other views on the workspace. You can submit similar queries on the Explore CI view.

-   **[CMDB searches can include relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-search.md)**

    Search queries can depend on relationships between CIs and can span multiple tables. For example, you might ask: "Search for servers that depend on databases - only Linux servers running Redhat".

-   **[Search the Service Graph database using natural language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-search-result-classfy.md)**

    Now Assist for CMDB analyzes your search criteria, identifies implicit filters, determines the optimum search method \(keyword search or query generation\), queries Service Graph data, and then displays the results. You then have the option to refine the search using natural language in the Now Assist panel.


## Changed in this release

-   **[New role required for the Create configuration item agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-ci-creator.md)**

    The sn\_cmdb\_admin role is now required to use the 'Create configuration item' agentic workflow \(was sn\_cmdb\_editor\).

-   **Skills now also require the now\_assist\_panel\_user role**

    AI skills that execute in the Now Assist panel now require both the cmdb\_dedup\_admin and now\_assist\_panel\_user roles.


## Activation information

Install Now Assist for CMDB by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

