---
title: Configure URL filter parameters on a dashboard
description: Enable URL filter parameters on your dashboard to support encoding of filter values in the dashboard URL..
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/config-url-filter-params.html
release: zurich
topic_type: task
last_updated: "2026-06-19"
reading_time_minutes: 1
keywords: [enable, configure, URL parameters, dashboard, Platform Analytics]
breadcrumb: [URL filter parameters for dashboard filters, Filters, Platform Analytics experience, Platform Analytics]
---

# Configure URL filter parameters on a dashboard

Enable URL filter parameters on your dashboard to support encoding of filter values in the dashboard URL..

## Before you begin

Role required: dashboard\_admin, or you must be the dashboard owner or have had editing rights shared with you.

## About this task

URL filter parameters allow dashboard users to create bookmarkable links that preserve their filter selections. This is useful for sharing specific data views with colleagues or maintaining quick access to frequently-used dashboard configurations.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards** and select the dashboard with the filter you want to configure.

2.  Select **Edit**.

3.  Select the filter you want to configure to open the filter's configuration panel.

4.  In the Advanced options section, specify a **Filter Custom Id**.

    The custom ID can indicate what the filter does and replaces the filter's sys\_id in the URL's filter parameter.

5.  Save the dashboard and select **Exit editing mode**.

    The URL filter parameter setting is now saved and will persist for all future dashboard loads.

6.  Apply filters to the dashboard to test the feature.

    Observe that the dashboard URL updates to include the filter parameter values. Open the sharing panel, copy the URL, and open it in a new tab to verify that the filters are applied automatically.


## Result

URL filter parameters are now configured on the dashboard. Users can apply filters and then bookmark or share the resulting URL with colleagues. When the URL is opened, the dashboard loads with all filters pre-applied.

