---
title: Filters in Platform Analytics
description: Filter lists and data visualizations on an inline or technical dashboard. Filter by possible data value, by whether the value is true or false, or by date.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-08-25"
reading_time_minutes: 4
breadcrumb: [Platform Analytics]
---

# Filters in Platform Analytics

Filter lists and data visualizations on an inline or technical dashboard. Filter by possible data value, by whether the value is true or false, or by date.

Add an interactive filter to a Platform Analytics dashboard 

The preceding video illustrates how to create a filter, in this case a multi-select filter for table data.

You can create a filter for either an inline dashboard or a technical dashboard. Inline dashboards are those dashboards created and populated in the inline dashboard editor. Technical dashboards are populated in the UI Builder and are more flexible but require considerably more expertise. For example, on a technical dashboard, you have to create custom event handlers for filters to apply to lists or data visualizations.

## Filters on inline dashboards

For inline dashboards, you can either create a filter directly on the dashboard through the inline editor, or you can add a filter to the dashboard from the filter library. In either case, you can add filters to a specific tab or have them apply to the entire dashboard. To take these actions, you only need the right to edit the dashboard.

If you have the analytics\_filter\_admin role, you can also create a filter for the library through the Filter Designer or copy an existing filter to the library.

The filter applies to those data visualizations and list components that contain a target of the filter.

If you want to put multiple filters on your dashboard, consider adding a filter group. In a filter group, you configure several filters and apply or clear them with one action, making only one call to the database. A filter group may therefore be more efficient than multiple separate filters.

When you create a filter, you first specify the filter type. All further configuration options depend on the selected type.

**Important:** When using this documentation, first select a topic for creating a filter. After you create a filter and select the filter type, follow the appropriate topic for configuring a filter of that type.

## Retaining filter values

On inline dashboards, filters retain their values across logins or page refreshes. However, these values are no longer retained when someone edits the filter configuration. Afterward, the filter reverts to its default values for all users on their next login or page refresh. On technical dashboards and pages created in UI Builder, filters do not retain values across logins or refreshes. For an exception, see [Add a dashboard to a Dashboards page](../../performance-analytics/task/add-dashboard-to-workspace.md).

## Domain filters

You can filter visualizations by domain on domain-separated instances. Domain filtering uses a different component. For more information, see [Create a domain filter](../task/create-domain-filter.md#).

-   **[Create or add a filter on an inline dashboard](../task/select-workspace-filter-type.md)**  
Create a filter or select one from the filter library. When creating a filter, name it, and choose whether to create a single select, multiple select, date, or true/false filter.
-   **[Create a filter in the Filter Designer](../task/add-filter-library.md)**  
Create a Platform Analytics filter in the Filter Designer and add it to the library for reuse.
-   **[Create a filter on a technical dashboard in UI Builder](../task/add-filter-tech-dashboard.md)**  
To filter data visualizations and simple lists in a technical dashboard, add a filter component in UI Builder and configure event handlers.
-   **[Make a data visualization act as a filter](../task/make-dv-act-as-filter.md)**  
You can set a data visualization to act as a filter on a dashboard that contains it. Only table or indicator data can be so filtered.
-   **[Configure a Single/Multiple select or cascading filter](../task/create-select-filter-workspace.md)**  
Let users filter a dashboard tab on one or more values from a set of choices, such as incident priority. You can have a single or multiple select filter follow another filter in a cascade.
-   **[Configure a True/False filter](../task/create-boolean-filter-workspace.md)**  
Let users filter on true/false fields and breakdown elements. For example, you can enable users to choose only the incidents where the **Active** field is set to **true**.
-   **[Configure a Date filter in the inline editor](../task/create-date-filter-workspace.md)**  
Let users select predefined periods or specify custom start and end dates for the data on a dashboard tab.
-   **[Create a domain filter](../task/create-domain-filter.md#)**  
Create a domain filter so that you can filter data visualizations on domains in a domain-separated instance. Domain filters enable the user to see data associated with one or more domains.
-   **[Edit a Platform Analytics filter on a dashboard](../task/edit-filters-configurable-workspaces.md)**  
When you highlight a filter on a dashboard that you have put into edit mode, you have several editing options depending on whether the filter is local to the dashboard or saved in the library.
-   **[Troubleshoot breakdown filters](../task/troubleshoot-breakdown-filters.md)**  
In Platform Analytics experience, it's not possible to do extend the functionality of a migrated breakdown filter that doesn't have an associated indicator.

**Parent Topic:**[Platform Analytics](../../performance-analytics/concept/c_performanceAnalyticsAndReporting.md)

