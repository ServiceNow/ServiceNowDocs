---
title: ServiceNow Otto for Platform Analytics Release Notes
description: ServiceNow Otto for Platform Analytics consists of several skills and applications that let you generate and work with Platform Analytics objects through generative AI. These skills let you analyze your business data through conversational interactions, without a technical knowledge of Platform Analytics.Query information that is available in formula indicators, not only in automated indicators and tables.Support returns for ACL Assessments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/otto-for-platform-analytics-rn-static.html
release: australia
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Platform Analytics release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# ServiceNow Otto for Platform Analytics Release Notes

ServiceNow Otto® for Platform Analytics consists of several skills and applications that let you generate and work with Platform Analytics objects through generative AI. These skills let you analyze your business data through conversational interactions, without a technical knowledge of Platform Analytics.

## About ServiceNow Otto for Platform Analytics

-   Generate and export Platform Analytics artifacts from conversational interactions in the ServiceNow Otto® panel.
-   Benefit from a single, smooth experience in asking questions across all ServiceNow Otto® for Platform Analytics skills, and other applications that incorporate Platform Analytics and AI, through a shared backend.

See [ServiceNow Otto for Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/now-assist-platform-analytics.md) for more information.

## Activation and other requirements

-   **Activation information**

    AI Data Explorer is available from the ServiceNow Store.

    Query Generation, Analytics Generation, and the dashboard and data visualization export skill are installed with Generative AI Controller, which is included as a dependency of all ServiceNow Otto applications.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

    After installation, activate the relevant skills. For more information, see the relevant Configure topics under [ServiceNow Otto for Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/now-assist-platform-analytics.md).


**Parent Topic:**[Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/analytics-intel-report-rn-landing.md)

## October 2026 AI Data Explorer release notes

Query information that is available in formula indicators, not only in automated indicators and tables.

### What's changed

-   **[Query formula indicator scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/indicator-vs-table-data-source-selection.md)**

    In AI Data Explorer, your queries can now reference information from indicator formulas, such as "What percentage of open incidents are Priority 1?"

-   **[Improved overview pages for skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/activate-aide-explorer.md)**

    When you view details from the tile of an AI skill in AI Admin Hub, you now get more information:

    -   A more detailed description of the skill
    -   Key benefits of the skill
    -   Required and recommended skills to go with the skill

## Brazil Patch 2 Platform Analytics release notes

Support returns for ACL Assessments.

### What's changed

-   **[ACL Assessment for Data Visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/report-view-acl-dashboard.md)**

    The ACL Assessment for Reports that was removed in Australia Patch 4 is back with support for Platform Analytics data visualizations. It also scans data source conditions for restricted fields.


### Plugin information

-   **Renamed or changed plugins**

    ACL Assessment for Data Visualizations \(sn\_report\_acl\): Scans data visualizations and Core UI reports for attempts to view content that were blocked by report\_view or read ACL rules.


