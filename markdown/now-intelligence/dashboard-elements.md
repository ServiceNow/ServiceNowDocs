---
title: Dashboard elements
description: Elements refer to the visual objects you can place on a dashboard, including filters.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Dashboard elements

Elements refer to the visual objects you can place on a dashboard, including filters.

Dashboards contain a combination of visual elements or funnels to show data. Available elements include Data visualization, Divider, Filter, Filter Group, Heading, Image, List, Process Mining - Map, Rich Text, Workbench, and Usage Insights funnel.

![Untitled dashboard with the Add new element menu expanded to show elements you can add to the dashboard](../../../administer/user-exp-analytics/image/uxa-view-funnnel-pa.png)

-   **[Data visualization](../../performance-analytics/concept/analytics-center-data-visualizations.md)**

    Data visualizations enable you to present a visual representation of current instance data or temporary data that you’ve imported. Data visualizations include visualizations that you create in the dashboard designer and data visualizations from the library.

    **Important:** You cannot place reports or Performance Analytics widgets on a Platform Analytics dashboard. You must create data visualizations instead.

-   **[Filter](../../par-for-workspace/concept/interactive-filters-workspace.md)**

    Filters enable users to filter the visualizations on a dashboard based on specified criteria. You can put filters either on the individual tabs or above the tabs so that the filter applies to elements every tab. Filters include both data filters and domain filters. You can create filters in the dashboard designer or select them from the library.

-   **[Filter group](../../par-for-workspace/task/create-filter-group.md)**

    A set of filters that you can apply simultaneously. Use when you have multiple filters that can apply to multiple visualizations.

-   **[Heading](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/now-components/now-heading/usage)**

    Headings provide a place for text at the top of a dashboard or section of a dashboard. Formatting for headings is limited to six heading levels.

    You can align headers from the start, end, or center of the allotted space. Select **Justify** to align the text across the entire allotted space.

-   **[Image](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/now-components/now-image/uib-config)**

    Image elements hold static or animated images on the dashboard.

-   **[Process Mining - Map](../../par-for-workspace/task/configure-po-map.md)**

    Map the different states that are part of your process and the transitions between those states. See which states the objects of the process are in and the speed with which they change state. Requires an existing Process Mining project.

-   **[List](../../reporting/task/create-dv-analytics-list.md)**

    Lists show table records. They support Platform Analytics filters and drilling down from data visualizations by default.

-   **Rich text**

    Rich text elements hold text that you can format either as text or as html, including font selection, text size, highlighting, and hyperlinks. Note that to edit in HTML markup, you open the HTML editor in the Configuration panel, and select the code tag icon &lt; &gt;.

-   **Workbench**

    The workbench option is available if the property com.snc.pae.workbench\_enabled is set to true. Workbench elements are migrated from Core UI in iframes. Choose from existing workbench elements.They can only be created in Core UI and are added to Platform Analytics experience in iframes.

-   **Funnel**

    Dashboards can display [funnels that you created](../../../administer/user-exp-analytics/task/create-funnel.md#) in Usage Insights. Funnels can show conversion rates and trends in aggregate user behavior to uncover the reasons behind success or failure of a specific in-application user goal. Investigating a conversion funnel can help you measure and optimize the conversion rates of relevant processes within your application.


## Default element dimensions

Each element has a default height and width when you place it on the stage to configure. Select and drag an element's handlebar to resize it.

-   **Filter**

    Six columns by three rows

-   **List, Multipivot, and Indicator Scorecard visualizations**

    48 columns by 18 rows

-   **All other components**

    11 columns by 11 rows


**Parent Topic:**[Exploring Platform Analytics dashboards](../reference/ac-elements.md)

**Related topics**  


[Add visual elements to an in-line dashboard](../task/add-elements-to-a-dashboard.md)

