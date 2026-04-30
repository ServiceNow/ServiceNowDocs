---
title: Create a dashboard
description: Create a dashboard that serves as a home page to assess the health of your instances at a glance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Instance Observer user configurable dashboard, Overview of Instance Observer, Platform Health, Using Impact, Impact]
---

# Create a dashboard

Create a dashboard that serves as a home page to assess the health of your instances at a glance.

## Before you begin

Role required: IO provisioned user

## Procedure

1.  Navigate to **Impact** &gt; **Platform Health** &gt; **Monitor** &gt; **Instance Observer** &gt; **Dashboard** &gt; **+Create new dashboard**.

2.  On the form, fill in the fields.

<table id="table_lgj_1lf_w2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Required unique name for the dashboard.

</td></tr><tr><td>

Description

</td><td>

Enter a description for the dashboard, keeping in mind this may be a shared dashboard.

</td></tr><tr><td>

Instance

</td><td>

Required to select production and non-production instances to be included on the dashboard.

</td></tr><tr><td>

Publish settings

</td><td>

Required field:-   Private: Only visible to you
-   Public: Visible to all users in your organization


</td></tr><tr><td>

Preferences

</td><td>

Select as the default dashboard to make this dashboard as the new homepage when launching Instance Observer. Default preferences are at the user level only.

</td></tr></tbody>
</table>3.  Select **Create**.

4.  Select **Add Widget**.

    -   Custom: Select custom to add your choice of metric, widgets, and aggregation. Note: Categories are equivalent to the pages available in the [Performance](instance-observer-performance.md) section.
    -   Out of the box: Choose from pre-defined widgets available on the base system dashboard to display. Depending on the selected category, the widget varies. These widgets are available for all instances of the account irrespective of the instances selected for the customized dashboard.
    Three widget types are supported:

    -   Table Data: Data added in tabular form
    -   Time Series: Data for the selected time period displayed in line charts
    -   KPIs: Key Performance Indicators for all important metrics with your choice of aggregation
5.  Select the **Category** for the widget.

6.  Add additional widgets to the custom dashboard.

7.  Select the gear icon on a widget to Edit or Delete a widget.

    A delete confirmation will display before removing the widget.

8.  Exit the Edit Dashboard mode to view the dashboard.

    Users can perform additional actions for dashboards:

    -   Select the time period and refresh frequency for the dashboards.
    -   Share a public dashboard’s link with other users in their organization.
    -   Zoom the dashboard on their monitor where in the dashboard will be refreshed automatically in the background
    -   From the gear icon on the dashboard users can perform the following actions:
        -   Settings: Change name, description, instances, share settings, and set the dashboard as default if needed.
        -   Clone: Clone a custom dashboard to use as a baseline for a new dashboard.
        -   Delete: Delete a dashboard, if required. Deleted dashboards will move under the Manage dashboard section and will be available for restoration for 7 days. When a customized dashboard that was set as default is deleted, the out-of-the-box dashboard will automatically become your default dashboard.
        -   Manage Dashboard: Lists all dashboards created by the logged in user, shared with the user, and deleted dashboards.
    For more information, see [Performance insights in user-configurable dashboard](io-performance-insights.md).


