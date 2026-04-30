---
title: Technical dashboards
description: If you need more advanced or customized features in a dashboard than you can get through the inline editor, you can create a UI Builder page that is exposed as a dashboard. Such pages are called technical dashboards.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Dashboards, Platform Analytics experience, Platform Analytics]
---

# Technical dashboards

If you need more advanced or customized features in a dashboard than you can get through the inline editor, you can create a UI Builder page that is exposed as a dashboard. Such pages are called technical dashboards.

## Technical dashboard overview

You create a technical dashboard in the dashboard editor. However, you cannot edit the dashboard contents in the inline editor. Instead of an **Edit** button, you have an **Open in UI Builder** button. In UI Builder, you can populate the dashboard will the full range of UI Builder containers and components. You have some additional options, such as being able to use manual data sources or local data broker instances. You also are required to configure more technical details yourself, such as event handlers for filters and drilling down in data visualizations.

Only someone with the ui\_builder\_admin role can create a technical dashboard, edit its contents, or configure its UI Builder page options.

You can open a technical dashboard in the dashboard editor from the dashboard library, as you would for any dashboard. In the editor, you can share the dashboard, create a printable version, or edit its [dashboard details](../../dashboards/task/config-db-in-ac.md). You can also expose technical dashboards in multiple workspaces as described in [Add a dashboard to a Dashboards page](../task/add-dashboard-to-workspace.md).

Technical dashboards are kept in a dedicated UI Experience named Advanced Dashboards. However, it is better to open technical dashboards in the dashboard editor and use the **Open in UI Builder** button than to open them directly in UI Builder through the Advanced Dashboards experience.

**Warning:**

Do not try to create a technical dashboard directly in the Advanced Dashboards experience. The UI Builder page you create will not appear in the dashboards library and will be missing other preconfigurations.

## Other technical dashboard topics

-   **[Technical dashboards compared to inline dashboards](../reference/technical-vs-in-line-dashboards.md)**  
The inline editor produces dashboard components with events and page properties preconfigured. The technical editor allows for a full range of UIB components but requires more back-end configuration.
-   **[Create a technical dashboard in UI Builder](../../dashboards/task/create-tech-db-in-ac.md)**  
Follow the Technical Editor option to create a dashboard using UI Builder. In UI Builder, you can use a wider range of features than the inline editor, including scripting and data binding.
-   **[Add a drilldown event to a data visualization on a technical dashboard](../../dashboards/task/add-custom-drilldown-event.md)**  
Technical dashboards do not support preconfigured destinations for drilling down from a data visualization. If you want a viewer to open a more detailed view of the data when they interact with a visualization, configure a custom drilldown event.
-   **[Add a drilldown event to a saved data visualization on a technical dashboard](../../dashboards/task/add-custom-drilldown-event-saved-dv.md)**  
Technical dashboards do not support preconfigured destinations for drilling down from a data visualization. If you want a viewer to open a more detailed view of the data when they interact with a visualization, configure a custom drilldown event.
-   **[Configure an event handler for a Filter component](../../dashboards/task/configure-event-handler-filter-lists-data-vis.md)**  
On a technical dashboard, configure a special client script-based event handler for a Filter component so it can be followed by any Lists or Data Visualizations. It is not necessary to configure an event handler for filters on inline dashboards.
-   **[Use a local data instance with a data visualization](../../dashboards/task/dv-local-data-instance.md)**  
For finer grained control of the data source than you have with preconfigured data sources, create a local data instance. Then bind the local data instance to the **dataPassthrough** property of the data visualization.

**Parent Topic:**[Dashboards in Platform Analytics](../../par-for-workspace/concept/analytics-center-dashboards.md)

**Related topics**  


[Exploring Platform Analytics dashboards](../../dashboards/reference/ac-elements.md)

[Common dashboard tasks in the in-line editor](../../dashboards/concept/common-dashboard-tasks.md)

[Configuring dashboards](../../dashboards/concept/configuring-dashboards.md)

[Executive dashboard overview](../../dashboards/executive-dashboards/executive-dashboard-overview.md)

[Proactive analytics insights on dashboards](../../par-for-workspace/concept/proactive-analytics.md)

[Dashboard reference](../../par-for-workspace/concept/dashboard-reference-page.md)

