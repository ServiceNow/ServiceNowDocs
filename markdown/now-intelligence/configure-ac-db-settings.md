---
title: Configure Platform Analytics dashboard settings
description: You can set refresh interval details and background colors, enable data caching to speed page refreshes, and choose which Insights cards to show.Dashboard content isn’t refreshed every time a user navigates between tabs. You can configure the number of minutes that dashboard tab content is cached before it's refreshed.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-03-21"
reading_time_minutes: 3
keywords: [How to schedule dashboard refresh interval, How to change dashboard background colors, Where to set up dashboard insights]
breadcrumb: [Dashboards in Platform Analytics, Platform Analytics experience, Platform Analytics]
---

# Configure Platform Analytics dashboard settings

You can set refresh interval details and background colors, enable data caching to speed page refreshes, and choose which Insights cards to show.

## Before you begin

Role required: dashboard\_admin for all dashboards, or any role for dashboards that you own or ones that you have been given the right to edit. See [Platform Analytics dashboard roles](../../par-for-workspace/concept/pa-dashboard-roles.md) for more information about viewing and editing rights on dashboards.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  In the **Dashboards** library, choose the dashboard you want to configure.

3.  Select **Edit** to enter editing mode.

4.  Select the settings button \(![Settings icon](../image/icon-cogwheel-ac.png)\) to open the **Settings** panel.

    ![Dashboard settings panel.](../../par-for-workspace/image/dashboard-settings.png)

5.  Change any of the following settings.

    -   Edit the **Refresh** options.

        Users with the dashboard\_admin role can configure automatic refreshes of the dashboard.

        -   Select **Show refresh information** to display the last time the dashboard was refreshed under the dashboard title. This information updates when the dashboard is automatically refreshed and when a user selects the refresh button \(![Refresh icon](../image/icon-db-refresh.png)\).
        -   Select **Scheduled repetition** to specify in minutes or hours how often the dashboard is reloaded. Applies only while the dashboard is open.

            **Note:**

            Do not confuse this setting with the **Refresh after being away for X minutes** option on data visualizations. This latter option takes effect when you navigate away from a dashboard containing the data visualization to another page in the same workspace or experience. If you navigate back to the dashboard after the specified number of minutes, the data visualization automatically refreshes.

        -   Select **Enable data cache** to shorten the load time on page refreshes for data visualizations based on table or indicator data. Data caching also applies to indicator scorecards. The dashboard uses the cached data instead of querying the database when the page is refreshed.

            **Note:**

            -   Enabling **Scheduled repetition** disables data caching and vice versa.
            -   Enabling **Real time update** or **Refresh after being away for X min** on a data visualization overrides caching for that visualization. If this option is subsequently disabled, the currently cached value is shown, if it hasn't expired.
            Data caches have an expiration time. When the page is refreshed and the cached data has expired, fresh data is queried and cached. When data caching is enabled, you can set the length of time for cached data to be valid in **Cached expiration time**. Options are 1, 2, 4, 8, 12, or 24 hours.

            You can manually refresh the cached data for either the whole dashboard or a data visualization by refreshing either the dashboard or the visualization, respectively.

    -   In the **Presentation** section, edit the background color of one or more tabs on the dashboard.

        Select a color from a list of preconfigured colors, or use the color palette to specify a color.

    -   Choose whether and which analytics to show in the **Insights** section.

        When you select **Show insights panel**, an **Insights** button is added to the dashboard. When a viewer presses this button, insights cards corresponding to the selected analytics options are shown. For more information, see [Proactive analytics insights on dashboards](../../par-for-workspace/concept/proactive-analytics.md).


## Configure Platform Analytics dashboard tab cache timeout

Dashboard content isn’t refreshed every time a user navigates between tabs. You can configure the number of minutes that dashboard tab content is cached before it's refreshed.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to `sys_properties.list`.

2.  Open the property **next\_experience.dashboard.tab.timeout**.

    This property is enabled by default.

3.  Edit the value.

    The default number of minutes after which tab content is refreshed is 20.

4.  Select `Update`.


