---
title: Technical dashboards compared to inline dashboards
description: The inline editor produces dashboard components with events and page properties preconfigured. The technical editor allows for a full range of UIB components but requires more back-end configuration.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [filter, Platform Analytics, data visualization]
breadcrumb: [Technical dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Technical dashboards compared to inline dashboards

The inline editor produces dashboard components with events and page properties preconfigured. The technical editor allows for a full range of UIB components but requires more back-end configuration.

<table id="table_d5z_rms_31c"><thead><tr><th>

Dashboard created inline

</th><th>

Technical dashboard

</th></tr></thead><tbody><tr><td>

Can be created with any role.

</td><td>

Can only be created with the ui\_builder\_admin role.

</td></tr><tr><td>

Can contain the following:-   Data visualizations
-   Filters
-   Headings
-   Images
-   Simple lists
-   Rich text

</td><td>

Can contain any component that is supported in UI Builder, including all components available for a dashboard created inline.

</td></tr><tr><td>

Can be duplicated.

</td><td>

Cannot be duplicated.

</td></tr><tr><td>

Can be exported.

</td><td>

Cannot be exported.

</td></tr><tr><td>

Data visualizations and filters support only predefined data sources.

</td><td>

Manual JSON data sources and local data instances are supported. \(True for UI Builder pages in general.\)

</td></tr><tr><td>

No event configuration for drilldowns. Default and preconfigured drilldowns are available as Chart interactions.

</td><td>

If you want viewers to drill down from a visualization, you have to configure a drilldown event on that visualization. You may need to configure other events. Chart interactions are not available.

</td></tr><tr><td>

Filter events are preconfigured to affect the relevant elements on the dashboard.

</td><td>

Filter event handlers must be configured manually.

</td></tr><tr><td>

If the viewer selects filter values and leaves the dashboard, those values are preselected for that viewer when they reopen the dashboard.

</td><td>

Filter values do not persist between user sessions.

</td></tr><tr><td>

Can be shared with or without editing rights depending on the roles of the sharer and what rights have been shared with them.

</td><td>

Same as dashboards created inline.

</td></tr><tr><td>

Can specify dashboard details, including exposing the dashboard in other experiences or configurable workspaces. The rights to edit dashboard details are limited to dashboard admins and the dashboard owner.

</td><td>

Same as dashboards created inline.

</td></tr></tbody>
</table>**Parent Topic:**[Technical dashboards](../concept/technical-dashboards.md)

**Related topics**  


[Create a filter on a technical dashboard in UI Builder](../../par-for-workspace/task/add-filter-tech-dashboard.md)

[Chart interactions in a data visualization](../../par-for-workspace/concept/dv-chart-interactions.md)

