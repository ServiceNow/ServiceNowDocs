---
title: Platform Analytics experience release notes
description: The ServiceNow Platform Analytics experience provides a single center for consuming the data from all Platform Analytics products. The Platform Analytics experience was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Platform Analytics experience release notes

The ServiceNow® Platform Analytics experience provides a single center for consuming the data from all Platform Analytics products. The Platform Analytics experience was enhanced and updated in the Zurich release.

## Platform Analytics experience highlights for the Zurich release

-   Collaborate on data-informed decisions through an AI-assisted, interactive explorer that serves as a centralized workspace, where you can create and share data visualizations on the fly.
-   Manage Performance Analytics indicators more conveniently, with access to editing, creation, and migration from within the Platform Analytics experience.

See [Platform Analytics experience](https://www.servicenow.com/docs/access?context=par-workspace&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) for more information.

## Important information for upgrading Platform Analytics experience to Zurich

On upgrade, any homepages on your instance that have been opened are migrated to Core UI dashboards, which are visible in the dashboard library. For more information, see [Homepage deprecation](https://www.servicenow.com/docs/access?context=homepage-deprecation-help-tool&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

Simple lists are all converted to the new List element on upgrade.

## New in the Zurich release

-   **[View, share, and export table records in the List component](https://www.servicenow.com/docs/access?context=create-dv-analytics-list&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Take advantage of the improved list capabilities of the List element, which replaces List - Simple. The List supports pagination, export from dashboards, export to comma-separated values, and alternative group by. It also provides a consistent configuration experience with other data visualizations.

-   **[Create indicators and migrate to data snapshots in the indicator library](https://www.servicenow.com/docs/access?context=your-kpis&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**
    -   Manage indicators from the indicator library, including links to create and edit indicators.
    -   Activate data snapshots conveniently, opening up the possibilities of applying multiple levels of breakdown to your indicators. See statistics on recent views and updates in tiles.
    -   If data snapshots are activated for the instance, see how many indicators are eligible and have already had data snapshots enabled.
    -   Show columns for any field on indicator records, as well as usage information.
-   **[Drill down to application overviews for User Experience Analytics](https://www.servicenow.com/docs/access?context=visualization-drilldown-in-config-ws&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Navigate to individual application overviews for User Experience Analytics from data visualizations. The **Go to data view** chart interaction is now supported for User Experience Analytics data and takes the viewer to these overview pages by default.

-   **[Filter data in User Experience Analytics](https://www.servicenow.com/docs/access?context=filter-user-list&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Filter User Experience Analytics data on default and custom User Experience Analytics properties.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Consistent header and border configuration](https://www.servicenow.com/docs/access?context=add-elements-to-a-dashboard&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Dashboard components now have header and border configuration options that are consistent with data visualizations and each other.

    Component icons have consistent coloring for improved contrast and accessibility and are consolidated in the same corner.


## Changed in this release

-   **[Select whether to drill down to Platform Analytics or Core UI lists](https://www.servicenow.com/docs/access?context=visualization-drilldown-in-config-ws&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Decide whether data view chart interactions for data visualizations on an instance drill down to Platform Analytics or Core UI record lists. This choice applies only on the Platform Analytics experience.

-   **[View usage information in the dashboards library](https://www.servicenow.com/docs/access?context=dashboards-for-admin-users&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    For analytics managers, the dashboard library now contains usage statistics, such as the number of dashboards not viewed in one year and the number of dashboards deactivated for more than three months.

-   **[Export data visualizations from dashboards to PNG and JPEG](https://www.servicenow.com/docs/access?context=export-data-vis-from-dboard&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Export individual data visualizations as a viewer to a graphic file.

-   **[Platform Analytics experience is supported even when Next Experience UI is disabled](https://www.servicenow.com/docs/access?context=data-migration-perform&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    You can migrate to Platform Analytics even if Next Experience isn’t enabled. Core UI dashboards are embedded in iframes.

-   **[Migration Center changes](https://www.servicenow.com/docs/access?context=data-migration&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**
    -   Dashboard owners can perform partial migration on their own dashboards.
    -   Geomap migration supported.
    -   Interactive filter check box option.
    -   Export to CSV from lists is supported.
-   **[Data visualizations and filters support Workflow Data Fabric tables](https://www.servicenow.com/docs/access?context=workflow-data-fabric&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Perform data analysis on external data fabric sources.


## Activation information

Platform Analytics experience is a ServiceNow AI Platform feature that is active by default.

## Related ServiceNow applications and features

-   **[Now Assist in Platform Analytics](https://www.servicenow.com/docs/access?context=now-assist-platform-analytics&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Several Now Assist Generative AI tools are available for generating and working with Platform Analytics objects through iterative questions and answers.

-   **[Performance Analytics \(Indicator data sources\)](https://www.servicenow.com/docs/access?context=pa-overview&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Performance Analytics is an in-platform process optimization solution, providing the indicator data sources that the Platform Analytics experience exposes graphically. It enables  organizations to set, track, and analyze progress toward goals. Performance Analytics was enhanced  and updated in the Zurich release.

-   **[User Experience Analytics](https://www.servicenow.com/docs/access?context=user-exp-analytics-landing&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    This application provides dashboard views for monitoring usage analytics of your Next Experience web applications as well as Virtual Agent, ServiceNow mobile, and Service Portal applications. User Experience Analytics provides a data source which data visualizations can display.

-   **[Process Mining](https://www.servicenow.com/docs/access?context=process-mining&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Process Mining helps analysts and process owners quickly analyze and optimize their business processes. Use Process Mining with Platform Analytics insights to optimize your indicator data sources.


**Parent Topic:**[Platform Analytics release notes](analytics-intel-report-rn-landing.md)

