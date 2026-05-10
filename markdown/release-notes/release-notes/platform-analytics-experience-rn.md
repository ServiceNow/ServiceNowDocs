---
title: Platform Analytics experience release notes
description: The ServiceNow Platform Analytics experience provides a single center for consuming the data from all Platform Analytics products. The Platform Analytics experience was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
---

# Platform Analytics experience release notes

The ServiceNow® Platform Analytics experience provides a single center for consuming the data from all Platform Analytics products. The Platform Analytics experience was enhanced and updated in the Australia release.

## Platform Analytics experience highlights for the Australia release

-   Embed dashboards and visualizations directly in workspaces to see relevant KPIs where they act.
-   Use a single, consistent visualization and filter model for table data, Performance Analytics indicators, Workflow Data Fabric, and UX analytics.
-   Author and adjust layouts within the dashboard, which enables business owners to make changes without heavy developer involvement.
-   Use performance enhancements, such as dashboard caching and UX improvements, to help shorten load times and improve day-to-day usability for high-traffic dashboards.

See [Platform Analytics experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/par-workspace.md) for more information.

## Important information for upgrading Platform Analytics experience to Australia

After upgrading, only admins can create Core UI analytics objects: reports, Performance Analytics widgets, responsive dashboards, and interactive filters. Other users can still view and edit Core UI objects but can create only Platform Analytics objects, such as data visualizations.

When upgrading, the published status on all Core UI reports changes to **false**, making them unpublished.

After upgrading, the Analytics Hub isn't available. Links to the Analytics Hub are redirected to KPI Details.

## New in the Australia release

-   **[New UI Builder templates for Dashboards and Data visualization libraries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/reuse-page-definitions.md)**

    Create Dashboard and Data Visualization library pages within your workspaces in UI Builder by using new page templates.

-   **[View usage information in the data visualization library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/dashboards-for-admin-users.md)**

    As an analytics manager, view usage statistics in the data visualization library. Those statistics include the number of reports, data visualizations that aren't used in any dashboards, and the number of data visualizations not viewed for more than six months.

-   **[Get recommendations to review problematic analytics resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/pa-library-recommendations.md)**

    As an analytics manager, view recommendations for which artifacts you should fix or delete in the Dashboard, Data Visualization, and Indicator libraries.

-   **[Executive dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/executive-dashboard-overview.md)**

    Use the new Executive Dashboards, which have been rebuilt using the Platform Analytics in-line dashboard capabilities.

-   **[View data snapshot indicators in data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/config-dv-sing-sc-ind-data.md)**

    Add indicators that are built from data snapshots sources to data visualizations.


## UI changes

-   **[Use simplified navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/using-the-next-experience-global-header.md)**

    When you are moved to Next Experience navigation:

    -   The Analytics Overview page and all library pages now contain their own Platform Analytics navigation tree.
    -   The navigation path **Self-Service** &gt; **Dashboards** redirects to **Platform Analytics** &gt; **Library** &gt; **Dashboards**.
    -   The navigation path **Reports** &gt; **View / Run** redirects to **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.
-   **[Sort library records by column values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/find-dashboard-library.md)**

    Select the header of any column in a library page to sort the library by that column.

-   **[New settings in Single Score data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-dv-sing-sc-ac.md)**

    Configure new color settings for Single Score data visualizations. You can also change the relative position of both the score and the title header.


## Changed in this release

-   **[Manage Platform Analytics in the improved Analytics Overview page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/analytics-center.md)**

    Quickly discover artifacts, access relevant information and key metrics, and take actions to manage the health of the library. The Analytics Overview page \(formerly Analytics Center\) acts as a one-stop shop and entry point for role-specific access to all important information related to Platform Analytics.

-   **[Platform Analytics experience is enabled by default for all users on upgrade to Australia](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/par-workspace.md)**

    Create content entirely within Platform Analytics.

-   **[Take role-based tours](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/guided-tours.md)**

    Role-based guided tours are added to the Platform Analytics Migration Center and the Dashboards and Data Visualizations library pages.

-   **[Filter dashboards by string field values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-select-filter-workspace.md)**

    Filter data by the contents of string-type fields with a single-select or multiple-select filter.

-   **[View the percentage each data segment contributes to the total](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-dv-donut-ac.md)**

    Enable the **Show % of total in tooltip** option to show the percentage each data point contributes to the total alongside absolute values in the tooltip. Applies to time series, bar, bubble, donut, geomap, and heatmap visualizations.

-   **[Explore native data snapshots indicators in KPI Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/kpi-details.md)**
    -   Employ intraday analysis with granularity based on work shifts.
    -   Customize score formatting options.
    -   Adjust breakdowns, calendar, and aggregation periods while exploring an indicator.
    -   Set up subscriptions for alerts on targets and thresholds directly from the targets and thresholds panels.
    -   Define hierarchical breakdowns with scores rolled up to parent elements.
-   **[Create hierarchical filters for Industrial Connected Workforce indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-hierarchical-filter.md)**

    Create multilevel filters with roll-up aggregation across nested organizational structures, which moves from site, to plan, to department, to functional location.

-   **[Download data visualizations as CSV or Excel files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/export-data-vis-from-dboard.md)**

    As a viewer, you now can download any data visualization, not only a List, as a CSV or XLS file.

-   **[Automatically set the aggregation period of data snapshots indicator trend lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/config-dv-time-series-ind-data.md)**

    Set the **Aggregation period** field in the **Trend by** settings to Auto so ****, the system automatically selects the aggregation period of data snapshot indicator trend lines based on the date range and business calendar.

-   **[Automatic aggregation of date-filtered data based on date range](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-date-filter-workspace.md)**

    Filter dashboards by business calendar and have the system infer the appropriate aggregation level at runtime. If you put a time series data visualization on a dashboard with a date filter, the aggregation of shown data adjusts automatically depending on the selected date range. This adjustment applies to both table and data snapshots indicator data.

-   **[Create custom data visualization filters with an improved condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/filter-dv-condition-builder.md)**

    When creating a data visualization for table data, you can create a custom filter when you specify the data source. The condition builder for the custom filter now has menus of fields, operators, values, and related tables.

-   **[Hide the Refresh action on data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-dv-sing-sc-ac.md)**

    In the Headers and Borders section of data visualizations, use the **Show refresh option** check box to hide the **Refresh** icon ![](../image/refresh-icon.jpg) in the Configuration settings of data visualizations. Data visualizations on cached dashboards never have the Refresh icon.

-   **[Migration Center enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/data-migration.md)**
    -   As an analytics manager, migrate any Core UI dashboard to Platform Analytics in the Dashboard library.
    -   Edit migrated content before activating it in the Platform Analytics experience.
    -   Activate content selectively.
    -   Total views of Core UI reports and other widgets are now migrated along with the Core UI content.
-   **[Dashboard element enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/edit-db-elements-in-ac.md)**

    Moving and resizing dashboard elements no longer opens the configuration panel.

-   **[Enhanced scheduled exports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/schedule-export-dboards-data-viz.md)**

    When scheduling the email of dashboards or data visualizations, limit recipients based on reference qualifiers.


## Deprecated features

Business users can no longer create or edit the following Core UI objects:

-   Reports

    Create new Core UI reports from sys\_reports.list with the report\_admin role.

-   Interactive filters

    Create new Core UI interactive filters from sys\_ui\_hp\_publisher.list with the report\_admin role.

-   Responsive dashboards

    Create new responsive dashboards from pa\_dashboards.list with the dashboard\_admin role.

-   PA widgets

    Create new Performance Analytics widgets from pa\_widgets.list with the pa\_admin role.


## Activation information

Platform Analytics experience is a ServiceNow AI Platform feature that is active by default.

## Related ServiceNow applications and features

-   **[Now Assist in Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/now-assist-platform-analytics.md)**

    Use AI-powered tools to enhance the value you get from Platform Analytics.

-   **[Performance Analytics \(Indicator data sources\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/pa-overview.md)**

    Create key performance indicators to optimize your business processes. Display these indicators in Platform Analytics.

-   **[Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/user-exp-analytics-landing.md)**

    Monitor how users interact with your ServiceNow Core UI, Next Experience, Portal, and Mobile applications.

-   **[Task Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/task-mining.md)**

    Collect and analyze workstation activities to understand how tasks are performed, identify inefficiencies, and make data-driven decisions.


**Parent Topic:**[Platform Analytics release notes](analytics-intel-report-rn-landing.md)

