---
title: Platform Analytics experience release notes
description: The ServiceNow Platform Analytics experience provides a single center for consuming the data from all Platform Analytics products. The Platform Analytics experience was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Platform Analytics experience release notes

The ServiceNow® Platform Analytics experience provides a single center for consuming the data from all Platform Analytics products. The Platform Analytics experience was enhanced and updated in the Zurich release.

## Platform Analytics experience highlights for the Zurich release

-   Collaborate on data-informed decisions through an AI-assisted, interactive explorer that serves as a centralized workspace, where you can create and share data visualizations on the fly.
-   Manage Performance Analytics indicators more conveniently, with access to editing, creation, and migration from within the Platform Analytics experience.

See [Platform Analytics experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/par-workspace.md) for more information.

## Important information for upgrading Platform Analytics experience to Zurich

On upgrade, any homepages on your instance that have been opened are migrated to Core UI dashboards, which are visible in the dashboard library. For more information, see [Homepage deprecation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/homepage-deprecation-help-tool.md).

Simple lists are all converted to the new List element on upgrade.

## New in the Zurich release

-   **[View, share, and export table records in the List component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/create-dv-analytics-list.md)**

    Take advantage of the improved list capabilities of the List element, which replaces List - Simple. The List supports pagination, export from dashboards, export to comma-separated values, and alternative group by. It also provides a consistent configuration experience with other data visualizations.

-   **[Create indicators and migrate to data snapshots in the indicator library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/your-kpis.md)**
    -   Manage indicators from the indicator library, including links to create and edit indicators.
    -   Activate data snapshots conveniently, opening up the possibilities of applying multiple levels of breakdown to your indicators. See statistics on recent views and updates in tiles.
    -   If data snapshots are activated for the instance, see how many indicators are eligible and have already had data snapshots enabled.
    -   Show columns for any field on indicator records, as well as usage information.
-   **[Drill down to application overviews for Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/visualization-drilldown-in-config-ws.md)**

    Navigate to individual application overviews for Usage Insights from data visualizations. The **Go to data view** chart interaction is now supported for Usage Insights data and takes the viewer to these overview pages by default.

-   **[Filter data in Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/filter-user-list.md)**

    Filter Usage Insights data on default and custom Usage Insights properties.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Consistent header and border configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/add-elements-to-a-dashboard.md)**

    Dashboard components now have header and border configuration options that are consistent with data visualizations and each other.

    Component icons have consistent coloring for improved contrast and accessibility and are consolidated in the same corner.


## Changed in this release

-   **[Select whether to drill down to Platform Analytics or Core UI lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/visualization-drilldown-in-config-ws.md)**

    Decide whether data view chart interactions for data visualizations on an instance drill down to Platform Analytics or Core UI record lists. This choice applies only on the Platform Analytics experience.

-   **[View usage information in the dashboards library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/dashboards-for-admin-users.md)**

    For analytics managers, the dashboard library now contains usage statistics, such as the number of dashboards not viewed in one year and the number of dashboards deactivated for more than three months.

-   **[Export data visualizations from dashboards to PNG and JPEG](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/export-data-vis-from-dboard.md)**

    Export individual data visualizations as a viewer to a graphic file.

-   **[Platform Analytics experience is supported even when Next Experience UI is disabled](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/data-migration-perform.md)**

    You can migrate to Platform Analytics even if Next Experience isn’t enabled. Core UI dashboards are embedded in iframes.

-   **[Migration Center changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/data-migration.md)**
    -   Dashboard owners can perform partial migration on their own dashboards.
    -   Geomap migration supported.
    -   Interactive filter check box option.
    -   Export to CSV from lists is supported.
-   **[Data visualizations and filters support Workflow Data Fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/workflow-data-fabric.md)**

    Perform data analysis on external data fabric sources.


## Activation information

Platform Analytics experience is a ServiceNow AI Platform feature that is active by default.

## Related ServiceNow applications and features

-   **[Now Assist in Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/now-assist-platform-analytics.md)**

    Several Now Assist Generative AI tools are available for generating and working with Platform Analytics objects through iterative questions and answers.

-   **[Performance Analytics \(Indicator data sources\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/pa-overview.md)**

    Performance Analytics is an in-platform process optimization solution, providing the indicator data sources that the Platform Analytics experience exposes graphically. It enables  organizations to set, track, and analyze progress toward goals. Performance Analytics was enhanced  and updated in the Zurich release.

-   **[User Experience Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/user-exp-analytics-landing.md)**

    This application provides dashboard views for monitoring usage analytics of your Next Experience web applications as well as Virtual Agent, ServiceNow mobile, and Service Portal applications. Usage Insights provides a data source which data visualizations can display.

-   **[Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/process-mining.md)**

    Process Mining helps analysts and process owners quickly analyze and optimize their business processes. Use Process Mining with Platform Analytics insights to optimize your indicator data sources.


**Parent Topic:**[Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/analytics-intel-report-rn-landing.md)

