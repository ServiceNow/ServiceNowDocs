---
title: Configure dashboard data broker
description: Activate the Dashboard data broker preset and configure the data broker to potentially speed the loading of dashboards by prefetching some data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/configure-dashboard-data-broker.html
release: australia
topic_type: task
last_updated: "2026-03-12"
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

    \[Omitted image "dashboard-preset-data-binding.png"\] Alt text: Activating the Dashboard data binding preset

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

    \[Omitted image "dashboard-edit-optional-parms.png"\] Alt text: Adding optional parameter values in the editor.

7.  In the configuration panel, check whether the following properties are correctly set:

    |Property|Value|
    |--------|-----|
    |Use data broker to fetch data|true|
    |Data broker response|dashboard &gt; data: \(\{"success":false\}\)|

    You can customize these values, but you probably do not have to.

8.  Save the page and open it in runtime.


**Parent Topic:**[Creating Platform Analytics pages in your own workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/adding-analytics-center-to-ws.md)

**Related topics**  


[Create a Platform Analytics workspace from App Engine Studio]()

[Add Platform Analytics pages to a configurable workspace]()

[Add a dashboard to a Dashboards page]()

[Configure custom redirection from a dashboard component]()

[Dashboard URL parameter delegation]()

[Pass global filters to the dashboard page template]()

