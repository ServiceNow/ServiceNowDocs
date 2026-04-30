---
title: Filters in Platform Analytics
description: Filter lists and data visualizations on an inline or technical dashboard. Filter by possible data value, by whether the value is true or false, or by date.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-08-25"
reading_time_minutes: 3
breadcrumb: [Platform Analytics experience, Platform Analytics]
---

# Filters in Platform Analytics

Filter lists and data visualizations on an inline or technical dashboard. Filter by possible data value, by whether the value is true or false, or by date.

Add an interactive filter to a Platform Analytics dashboard 

The preceding video illustrates how to create a filter, in this case a multi-select filter for table data.

You can create a filter for either an inline dashboard or a technical dashboard. Inline dashboards are those dashboards created and populated in the inline dashboard editor. Technical dashboards are populated in the UI Builder and are more flexible but require considerably more expertise. For example, on a technical dashboard, you have to create custom event handlers for filters to apply to lists or data visualizations.

**Note:** When you enable User Experience Analytics filters within Platform Analytics dashboards, they operate as global filters. This means their effect is comprehensive, impacting all visualizations across the entire dashboard, not just a single visualization.

**Note:** The default maximum number of custom filters you can save for user experience analytics application is 500. You can modify the number of custom filters in theuxa.query\_builder.max\_num\_of\_user\_filter property.

When you edit Core UI filters dashboards migrated in compatibility mode, you do so in the Core UI tools. For more information, see [Reporting, dashboards, and Performance Analytics in the Core UI](../../reporting/concept/classic-vis-overview.md).

## Filters on inline dashboards

For inline dashboards, you can either create a filter directly on the dashboard through the inline editor, or you can add a filter to the dashboard from the filter library. In either case, you can add filters to a specific tab or have them apply to the entire dashboard. To take these actions, you only need the right to edit the dashboard.

If you have the analytics\_filter\_admin role, you can also create a filter for the library through the Filter Designer or copy an existing filter to the library.

The filter applies to those data visualizations and list components that contain a target of the filter.

If you want to put multiple filters on your dashboard, consider adding a filter group. In a filter group, you configure several filters and apply or clear them with one action, making only one call to the database. A filter group may therefore be more efficient than multiple separate filters.

When you create a filter, you first specify the filter type. All further configuration options depend on the selected type.

**Important:** When using this documentation, first select a topic for creating a filter. After you create a filter and select the filter type, follow the appropriate topic for configuring a filter of that type.

## Retaining filter values

On inline dashboards, filters retain their values across logins or page refreshes. However, these values are no longer retained when someone edits the filter configuration. Afterward, the filter reverts to its default values for all users on their next login or page refresh. On technical dashboards and pages created in UI Builder, filters do not retain values across logins or refreshes. For an exception, see [Add a dashboard to a Dashboards page](../../performance-analytics/task/add-dashboard-to-workspace.md).

Filter values can also be retained when you export an inline dashboard. When you export a dashboard to Microsoft PowerPoint, filter values are applied automatically. When you export a dashboard to PDF, you have the option whether or not to retain filter values. Filter values are not retained when you export a technical dashboard. For more information, see [Export a Platform Analytics dashboard](../../dashboards/task/export-pae-dashboard-ppt.md).

## Domain filters

You can filter visualizations by domain on domain-separated instances. Domain filtering uses a different component. For more information, see [Create a domain filter](../task/create-domain-filter.md#).

