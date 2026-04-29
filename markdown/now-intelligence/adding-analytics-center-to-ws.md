---
title: Creating Platform Analytics pages in your own workspace
description: You can either create a new workspace with preconfigured Platform Analytics pages in App Engine Studio, or add Platform Analytics pages to your own workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Platform Analytics experience, Platform Analytics]
---

# Creating Platform Analytics pages in your own workspace

You can either create a new workspace with preconfigured Platform Analytics pages in App Engine Studio, or add Platform Analytics pages to your own workspace.

Choose from the following ways to add Platform Analytics to your workspace. These approaches differ in the degree of customization they provide:

-   Add an entire pre-built workspace from App Engine Studio.
-   Use the page templates that are provided in the UI Builder. You can re-create all of Platform Analytics experience, or you can add only selected parts.

-   **[Create a Platform Analytics workspace from App Engine Studio](create-analytics-ws-aes.md)**  
The App Engine Studio includes a prebuilt workspace that you can add to an application. This workspace includes an Analytics Center page, along with the pages that the Analytics Center links to.
-   **[Add Platform Analytics pages to a configurable workspace](../task/add-analytics-center-to-experience.md#)**  
Add an Analytics Overview and its related pages to your own workspace/experience through page templates.
-   **[Add a dashboard to a Dashboards page](../task/add-dashboard-to-workspace.md)**  
You can add either a technical dashboard or one made in the inline editor to a page you built from the Dashboards page template. Configure the dashboard component on that page.
-   **[Configure custom redirection from a dashboard component](../task/config-custom-redirection-from-db.md)**  
If you have created a page in your workspace from the Dashboard page template, you can customize the on-click redirection from the dashboard component on that page. The inline dashboard that this component displays will follow the custom redirection.
-   **[Dashboard URL parameter delegation](../../../build/component-uib-setup/concept/dashboard-url-parameter-delegation.md#)**  
The Delegate URL params property enables UIB pages containing dashboard components to control how URL parameter updates are handled. Doing so enables custom navigation logic for embedded or workspace scenarios.
-   **[Pass global filters to the dashboard page template](../../par-for-workspace/task/pass-global-filters-to-db.md)**  
Global filters are sent to the dashboard to serve as filters for the visualizations within the dashboard. These filters are merged with existing filters in the dashboard.
-   **[Configure dashboard data broker](../../../build/component-uib-setup/task/configure-dashboard-data-broker.md)**  
Activate the Dashboard data broker preset and configure the data broker to potentially speed the loading of dashboards by prefetching some data.

**Parent Topic:**[Platform Analytics experience](../../par-for-workspace/concept/par-workspace.md)

