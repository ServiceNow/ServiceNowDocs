---
title: Platform Analytics experience release notes
description: The Platform Analytics experience application enables you to distribute and consume Platform Analytics through data visualizations and dashboards with optional filters. Explore KPIs and receive insights into significant events in the data.External pages and UI Builder pages can now pass filter parameters via URL to pre-apply filters on Platform Analytics inline dashboards and visualizations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/platform-analytics-experience-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-28"
reading_time_minutes: 5
breadcrumb: [Platform Analytics release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Platform Analytics experience release notes

The Platform Analytics experience application enables you to distribute and consume Platform Analytics through data visualizations and dashboards with optional filters. Explore KPIs and receive insights into significant events in the data.

## About Platform Analytics experience

-   Create dashboards to visually share your data with stakeholders in your organization.
-   Create, update, and share visualizations based on indicators, tables or other data to share with others.
-   Filter lists and visualizations on dashboards based on values, date, or true/false.
-   Delve into the information behind your Key Performance Indicators \(KPIs\) and learn when processes behave in unexpected ways.

See [Platform Analytics experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/par-workspace.md) for more information.

## Activation and other requirements

-   **Activation information**

    Platform Analytics experience is enabled by default on upgrade to Brazil.

-   **Upgrade information**

    Core UI dashboards and reports are visible from the Platform Analytics Dashboard and Data visualization libraries.


**Parent Topic:**[Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/analytics-intel-report-rn-landing.md)

## Platform Analytics experience Bundle — v9.0

External pages and UI Builder pages can now pass filter parameters via URL to pre-apply filters on Platform Analytics inline dashboards and visualizations.

### What's new

-   **[Explore mode for read-only users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/editing-dv-in-line-db.md)**

    Read-only users can temporarily reconfigure a visualization in-session — on inline dashboards or in the Visualization Designer — without saving changes. When Explore mode is active, an informational alert indicates that changes aren't persisted, and the Save action is not available. This enables dashboard consumers to explore data on their own terms without requiring edit access.

-   **[Share dashboard with all internal users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/share-db-in-ac.md)**

    Administrators can share a Platform Analytics dashboard with all authenticated users by assigning it to the `dashboard_user` role, which ships with the base system. Any user who holds at least one role automatically receives read access to dashboards shared this way. The role name used as the sentinel is configurable via the system property `com.glide.par_dashboards.security.all_users_role`. This replaces the need to manage individual user, group, or role assignments for organization-wide dashboards.


### What's changed

-   **[URL filter parameters for inline dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/url-filter-parameters.md)**

    External pages and UI Builder pages can now pass filter values to Platform Analytics inline dashboards and the Visualization Designer using URL parameters. The feature introduces a standard mechanism that accepts filter payloads in `encodedQuery` format, validates and maps them to filter state, and applies them when the dashboard or visualization loads. Supported filter types include choice and Boolean. Deep links and drill-down workflows that previously relied on Classic or Core UI URL-based filtering are now supported in Platform Analytics experiences.

    Copying a dashboard link now includes active filter state in the URL using the format `/unified-filters-param/filterId:value1,value2`, removing the back-end dependency on the `par_dashboard` filter record.

-   **[Updated creation flow for dashboards and data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/common-dashboard-tasks.md)**

    The creation flow for Platform Analytics dashboards and data visualizations now clearly surfaces Next Experience as the recommended path. Core UI creation remains available for users who need it. The updated flow applies when the system properties `com.snc.par.coreui.dashboard_create.enabled` and `com.snc.par.coreui.report_create.enabled` are set to `true`. Instances where migration is complete and Core UI creation is inactive aren't affected. A new informational modal for data visualization creation has been added. The create flow now routes Core UI dashboard creation to the `pa_dashboard` record form and Core UI report creation to the Report Designer.

-   **[Configurable list view for drilldowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/dv-chart-interactions.md)**

    Dashboard and report designers can now select which list view opens when users drill down to data using the **Go to Data View** chart interaction. The configuration option is available in the **Chart Interaction** section of the Visualization and Dashboard Designers. Designers can specify a view from the `sys_ui_view_list` table, providing flexibility to target different views for different roles or use cases. Tooltip text in the visualization now dynamically reflects the configured destination — showing the data source name for **Go to Data View** interactions and the page name for **Go to URL** interactions. The **Go to URL** interaction now redirects in the same browser tab.

-   **[Export quality improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/export-pae-db-restrict.md)**
    -   A system property enables or disables the export button globally. A second property accepts a comma-separated list of roles permitted to export when the first property is enabled. When the roles list is empty, export is available to all users. This applies to on-demand export at both the dashboard and data visualization level, including client-side export.
    -   The export modal now includes a documentation link for supported and unsupported components. It also provides options to enable or disable sending exports via email and displays improved error messages after export failures. UI controls in export modals have been updated from toggles to check boxes.
    -   PDF exports now correctly apply the selected orientation \(landscape or portrait\) for list-type visualizations. Previously the orientation setting was recognized in the UI but exports always rendered in portrait.
    -   Users can select specific dashboard tabs to include when exporting to PDF, consistent with existing PPT export tab selection. Dashboards with applied filters respect the filter state in PDF exports.
    -   Scheduled export now supports additional file types and page format options that were previously available in Core UI but missing from the scheduled export UI. Day-of-week scheduling options \(Monday to Friday\) are now available. Core UI reports are hidden from the scheduled export library page.
-   **[Dashboard PDF export improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/export-pae-dashboard-ppt.md)**

    Platform Analytics dashboard PDF and PowerPoint export includes the following improvements:

    -   You can now select which dashboard tabs to include when exporting to PDF, consistent with the existing tab selection available for PPT export.
    -   When exporting a dashboard to PDF, you can choose whether to apply or exclude the active dashboard filters in the exported output.
    -   Visualizations in exported PDF and PPT files now follow the layout order displayed on the dashboard, with the top layout rendered first and widgets ordered left to right.
    -   Filters, images, and headings are now included in dashboard PDF exports. Previously these components were excluded because `par_metadata` records were not present for them.
    -   When a dashboard contains only unsupported components, the export now returns a meaningful error message rather than an empty PDF.
    -   Dashboards containing only list visualizations no longer trigger an unnecessary export server call.
-   **[Library page bookmark icon theme alignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/bookmark-dashboard-ac.md)**

    The bookmark icon in the Dashboard library page and the Data Visualization library page now renders in the applied theme color, consistent with the Indicators library page. Previously the bookmark icon displayed in blue regardless of the active theme.


