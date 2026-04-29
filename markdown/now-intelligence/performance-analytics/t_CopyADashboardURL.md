---
title: Copy a responsive dashboard URL
description: It is not possible to copy a dashboard URL from the browser. You can, however, create a URL that opens the current view of the dashboard, including tabs and breakdown elements. When the link is followed, the ServiceNow platform frame around the dashboard is not included.You can link to a Performance Analytics dashboard from your instance. Several URL parameters enable you to specify aspects of the dashboard when the link is followed.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with responsive dashboards, Create and use dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Copy a responsive dashboard URL

It is not possible to copy a dashboard URL from the browser. You can, however, create a URL that opens the current view of the dashboard, including tabs and [breakdown elements](../concept/performance-analytics-glossary.md#). When the link is followed, the ServiceNow platform frame around the dashboard is not included.

## Before you begin

Role required: You must be able to access the dashboard.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards** or **All** &gt; **Performance Analytics** &gt; **Dashboards**.

2.  Select the responsive dashboard with the URL that you want to copy.

3.  Select a tab, breakdown, and breakdown element.

4.  From the context menu ![context menu icon](../image/ContextMenu.png) select **Copy Dashboard URL**.


## Result

The dashboard URL is copied to your clipboard. Some browsers prompt you to copy the URL to your clipboard.

## What to do next

Share the URL with other users.

## Dashboard URL format

You can link to a Performance Analytics dashboard from your instance. Several URL parameters enable you to specify aspects of the dashboard when the link is followed.

All dashboard URLs follow this format:

```
https://<instance>.service-now.com/$dashboards.do?
```

.

**Note:** Because dashboards are not limited to users of Performance Analytics,

```
$dashboards.do
```

replaces

```
$pa_dashboard
```

, although both strings work in dashboard URLs.

This base URL is followed by several optional URL query parameters.

<table id="table_is3_f4t_hs"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_dashboard=&lt;sys\_id&gt;

</td><td>

The sys\_id of the dashboard to show.

</td></tr><tr><td>

sysparm\_tab=&lt;sys\_id&gt;

</td><td>

The sys\_id of the dashboard tab to show. If you do not specify a tab, the leftmost tab is displayed. This parameter applies only if **sysparm\_dashboard** exists.

</td></tr><tr><td>

sysparm\_breakdown\_source=&lt;sys\_id&gt;

</td><td>

The sys\_id of the dashboard breakdown to show.

</td></tr><tr><td>

sysparm\_element=&lt;value&gt;

</td><td>

The sys\_id or value of the [breakdown element](../concept/performance-analytics-glossary.md#) to show. This parameter applies only if **sysparm\_breakdown\_source** also exists. Values are case-sensitive.

</td></tr><tr><td>

sysparm\_element\_value=&lt;value&gt;

</td><td>

The selected element value. This value may be the sys\_id of a referenced record, or the database value for a choice list choice. Database values are case-sensitive. This parameter applies only if **sysparm\_element** and **syspartm\_breakdown\_source**also exist.

</td></tr><tr><td>

sysparm\_header=&lt;value&gt;

</td><td>

Controls if the dashboard header appears. Possible values are:-   Visible — The full header is visible.
-   Hidden — The full header is hidden.
-   Embedded — The header is visible but only the options **Refresh**, **Reset filters**, and **Export to PDF** are visible.

</td></tr><tr><td>

sysparm\_breakdown=&lt;value&gt;

</td><td>

Controls if the dashboard breakdown appears. Possible values are:-   Visible — The full breakdown is visible, including both source and element.
-   Hidden — The full breakdown is hidden.
-   Embedded — Only the breakdown element is visible.
-   Readonly — The breakdown is visible but the user cannot change how the filter is configured.

</td></tr></tbody>
</table>