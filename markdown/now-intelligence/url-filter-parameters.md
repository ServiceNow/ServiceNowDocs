---
title: URL filter parameters for dashboard filters
description: URL filter parameters enable users to encode filter selections directly in dashboard URLs, allowing bookmarkable, shareable dashboard states with automatically apply filters. The URL parameter is called unifiedFiltersParam and is appended as a path segment after the dashboard sys\_id.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/url-filter-parameters.html
release: australia
topic_type: concept
last_updated: "2026-06-15"
reading_time_minutes: 2
keywords: [URL parameters, dashboard filters, filter state, Platform Analytics]
breadcrumb: [Filters, Platform Analytics experience, Platform Analytics]
---

# URL filter parameters for dashboard filters

URL filter parameters enable users to encode filter selections directly in dashboard URLs, allowing bookmarkable, shareable dashboard states with automatically apply filters. The URL parameter is called **unifiedFiltersParam** and is appended as a path segment after the dashboard sys\_id.

## Key benefits

This functionality provides the following benefits:

-   Create shareable dashboard URLs with pre-applied filters that persist when recipients open the link.
-   Bookmark specific filtered dashboard views for quick return to saved analysis states.
-   Reduce time spent re-entering filter values for frequently-viewed dashboard configurations.
-   Enable filter state to be preserved across browser sessions via URL encoding.

## How it works

The following points describe how this capability works:

-   Users apply filters to a dashboard using the filter panel.
-   For each filter with selected values, it builds a key:values pair using the filterCustomId if configured, otherwise the filterId. Values are URI-encoded and joined by commas. All filter pairs are joined with semicolons into a single filter string. The filter string is appended to the dashboard URL as **/unifiedFiltersParam/&lt;filterString&gt;**.

    In the **Advanced options** section of the filter configuration, you can provide a Custom ID that replaces the filter's sys\_id in the dashboard URL.

-   In the **Share Dashboard** modal, users can select **Copy link with filter** to share the filter-encoded URL with colleagues. When opened, the dashboard loads with the same filters applied. The URL is copied to the clipboard.
-   Filter parameters are encoded in the query string using a standardized format supported by the Next Experience framework.
-   Clearing all filters resets the dashboard to its default state. The dashboard URL continues to show the originally applied filter values.

**Note:** Dashboard URLs with encoded filter parameters override both configured values and user preferences when selected to open the dashboard.

## Supported filter types

The following filter types can be encoded in the URL:

-   Text filters \(single-value and multi-value\)
-   Numeric range filters
-   Lookup filters \(reference fields\)
-   Boolean \(yes/no\) filters

## Limitations

URL filter parameters have the following known limitations:

-   URLs longer than 2000 characters are automatically shortened via TinyURL.
-   Special characters in filter values must be URL-encoded; the system handles this automatically

## Filter URL example with filter sys\_IDs

This sample URL contains three filter sys\_IDs followed by their values:`/now/platform-analytics-workspace/dashboards/params/edit/true/sys-id/459c953912b1746571a2ba9ce27c6381/unifiedFiltersParam/1jj9ciapngtpungufq4o:database,hardware,password_reset;1jj9cj50jmm9oeq5v978:true;1jj9ep15rqq5ug6djia8:2`

|Filter ID|Values|Description|
|---------|------|-----------|
|1jj9ciapngtpungufq4o|database, hardware, password\_reset|Multi-select filter with three values|
|1jj9cj50jmm9oeq5v978|true|Single-value Boolean filter|
|1jj9ep15rqq5ug6djia8|2|Single-value numeric filter|

## Filter URL example with custom filter IDs

This sample URL contains three custom filter IDs followed by their values:`/now/platform-analytics-workspace/dashboards/params/edit/true/sys-id/459c953912b1746571a2ba9ce27c6381/unifiedFiltersParam/incident-cat:database,hardware,password_reset;active:true;priority:1,3`

|Filter ID|Values|Description|
|---------|------|-----------|
|incident-cat|database, hardware, password\_reset|Multi-select filter with three values|
|active|true|Single-value Boolean filter|
|priority|1,3|Multi-select numeric filter with two values|

