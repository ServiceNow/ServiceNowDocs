---
title: Configure dashboard data broker
description: Activate the Dashboard data broker preset and configure the data broker to potentially speed the loading of dashboards by prefetching some data.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Creating Platform Analytics pages, Platform Analytics experience, Platform Analytics]
---

# Configure dashboard data broker

Activate the Dashboard data broker preset and configure the data broker to potentially speed the loading of dashboards by prefetching some data.

## Before you begin

Role required: ui\_builder\_admin, admin

## About this task

The dashboard includes a Dashboard data broker preset. This data broker prefetches all the static JavaScript assets that are required by the visualizations that are rendered in the dashboard. This prefetch could speed the loading of visualizations that include many such assets.

This data broker prefetches data only on direct page loads. It does not apply on click-through page loads, such as when the dashboard is opened by selecting a URL link from another page. It also does not function when the dashboard is used as an embedded component.

## Procedure

1.  Open your workspace and either create a page from the Dashboards template or navigate to an existing page from that template.

2.  Open the Config tab in the configuration panel of the Dashboard component.

3.  Check whether the Dashboard data broker preset is activated.

    The preset is activated by default.

    ![Activating the Dashboard data binding preset](../image/dashboard-preset-data-binding.png)

4.  In the **Data and scripts** section of the page, open **Data resources** &gt; **Data controller 1**.

    You can rename the data resource if desired.

5.  Check whether the properties are correct:

    |Property|Value|
    |--------|-----|
    |experienceId|app &gt; appId|
    |dashboardSysId|props &gt; sysId|
    |filterId|props &gt; filter|

6.  Add default values for the optional page parameters.

    |Parameter|Value|
    |---------|-----|
    |sysId|null|
    |filter|1|

    ![Adding optional parameter values in the editor.](../image/dashboard-edit-optional-parms.png)

7.  In the configuration panel, check whether the following properties are correctly set:

    |Property|Value|
    |--------|-----|
    |Use data broker to fetch data|true|
    |Data broker response|dashboard &gt; data: \(\{"success":false\}\)|

    You can customize these values, but you probably do not have to.

8.  Save the page and open it in runtime.


**Parent Topic:**[Creating Platform Analytics pages in your own workspace](../../../use/performance-analytics/concept/adding-analytics-center-to-ws.md)

**Related topics**  


[Create a Platform Analytics workspace from App Engine Studio](../../../use/performance-analytics/concept/create-analytics-ws-aes.md)

[Add Platform Analytics pages to a configurable workspace](../../../use/performance-analytics/task/add-analytics-center-to-experience.md#)

[Add a dashboard to a Dashboards page](../../../use/performance-analytics/task/add-dashboard-to-workspace.md)

[Configure custom redirection from a dashboard component](../../../use/performance-analytics/task/config-custom-redirection-from-db.md)

[Pass global filters to the dashboard page template](../../../use/par-for-workspace/task/pass-global-filters-to-db.md)

