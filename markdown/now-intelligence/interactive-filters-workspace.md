---
title: Filters in Platform Analytics
description: Filter lists and data visualizations on an inline or technical dashboard. Filter by possible data value or text, by whether the value is true or false, or by date.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Platform Analytics experience, Platform Analytics]
---

# Filters in Platform Analytics

Filter lists and data visualizations on an inline or technical dashboard. Filter by possible data value or text, by whether the value is true or false, or by date.

To find Filters in Platform Analytics, navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Filters**. You can also navigate to this library from other Platform Analytics library pages. Access to the filter library requires the analytics\_filter\_admin role or higher. For more information on user roles in Filters, see [Filter roles](../reference/platform-analytics-roles.md#table_tm2_v15_32c).

![Platform Analytics Filters library](../image/pa-filters-lib.png "Filter library")

Add an interactive filter to a Platform Analytics dashboard 

This video illustrates how to create a filter, in this case a multi-select filter for table data.

Technical dashboards are populated in the UI Builder and are more flexible but require considerably more expertise. For example, on a technical dashboard, you have to create custom event handlers for filters to apply to lists or data visualizations.

**Note:** When you enable Usage Insights filters within Platform Analytics dashboards, they operate as global filters. This means they impact all visualizations across the entire dashboard, not just a single visualization.

**Note:** The default maximum number of custom filters you can save for the Usage Insights application is 500. You can modify the number of custom filters in the **uxa.query\_builder.max\_num\_of\_user\_filter** property.

When you edit Core UI filters dashboards migrated in compatibility mode, you do so in the Core UI tools. For more information, see [Reporting, dashboards, and Performance Analytics in the Core UI](../../reporting/concept/classic-vis-overview.md).

## Filters on inline dashboards

For inline dashboards, you can create a filter directly on the dashboard through the inline editor, or add a filter from the filter library. In either case, you can add filters to a specific tab or have them apply to the entire dashboard. To take these actions, you only need the right to edit the dashboard.

If you have the analytics\_filter\_admin role, you can also create a filter for the library through the Filter Designer or copy an existing filter to the library.

The filter applies to those data visualizations and list components that contain a target of the filter.

In a filter group, you configure several filters and apply or clear them with one action, making one database call. A filter group may therefore be more efficient than multiple separate filters.

When you create a filter, you first specify the filter type. All further configuration options depend on the selected type.

**Important:** When using this documentation, first select a topic for creating a filter. After you create a filter and select the filter type, follow the configuration topic for that filter type.

## Retaining filter values

Filter values are not retained when someone edits the filter configuration. On editing, the filter reverts to its default values for all users on their next login or page refresh. On technical dashboards and pages created in UI Builder, filters don't retain values across user sessions or refreshes. For an exception, see [Add a dashboard to a Dashboards page](../../performance-analytics/task/add-dashboard-to-workspace.md).

When you export a dashboard to Microsoft PowerPoint, filter values are applied automatically. When you export a dashboard to PDF, you can choose whether to retain filter values. Filter values are not retained when you export a technical dashboard. For more information, see [Export a Platform Analytics dashboard](../../dashboards/task/export-pae-dashboard-ppt.md).

## Domain filters

You can filter visualizations by domain on domain-separated instances. Domain filtering uses a different component. For more information, see [Create a domain filter](../task/create-domain-filter.md#).

