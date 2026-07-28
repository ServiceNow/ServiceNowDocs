---
title: Use a local data instance with a data visualization
description: For finer grained control of the data source than you have with preconfigured data sources, create a local data instance. Then bind the local data instance to the dataPassthrough property of the data visualization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/dv-local-data-instance.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Technical dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Use a local data instance with a data visualization

For finer grained control of the data source than you have with preconfigured data sources, create a local data instance. Then bind the local data instance to the **dataPassthrough** property of the data visualization.

## Before you begin

**Important:** This is an advanced procedure. Consider carefully whether you need a local data instance or can use a standard data source.

Before proceeding, review .

Role required: ui\_builder\_admin, admin

## Procedure

1.  Open the technical dashboard or other UI Builder page in UI Builder.

2.  In the Data and scripts drawer, under Data resources, select **+ Add data resource**.

    \[Omitted image "add-data-resource.png"\] Alt text: Add data resource link when there are no data resources yet.

3.  In the Select a data resource window, search for `Data visualization`.

    You get a selection of the data resources you can use.

    \[Omitted image "select-data-resource.png"\] Alt text: Selection of data resources for data visualizations.

4.  Select a data resource that matches the type of data you want to show.

5.  Read through the information pane and copy or take notes on the configuration details.

6.  Select **Add**.

7.  Complete the configuration options that you need for the type of visualization with which you plan to use this data instance.

    Create and configure a separate local data instance for every type of visualization that you want to use the same data. For example, if you plan to have a bar and a time series that show scores from the same indicator, create two local data instances: one each for bar and time series visualizations, but both on the same indicator.

    **Tip:** You can add the data visualization to the page and compare its configuration panel to the options for the local data instance.

8.  Copy the `@data` data bind for this data source.

    \[Omitted image "data-resource-reference.png"\] Alt text: The @data reference for a data source, with the Copy button.

9.  Add the desired data visualization component to the page.

10. In the configuration panel for that data visualization, in the Data sources section, turn on **Define data manually**.

11. For the **Data** field, select **Bind data or use scripts**.

    \[Omitted image "bind-data-use-scripts.png"\] Alt text: Bind data option for the Data field.

12. In the Bind data to Data dialog, under Data types, select **Data resource**.

13. Double-click in the Add a data output to this area section and paste the data bind to your local data instance into the blue box.

14. Append `.output.result` at the end of the data bind.

    For example, the completed data bind to the local data instance data\_visualization\_api\_for\_table\_data\_source\_1 is `@data.data_visualization_api_for_table_data_source_1.output.result`.

    \[Omitted image "bind-data-to-data.png"\] Alt text: Bind data to data dialog showing data resource binding to data\_visualization\_api\_for\_table\_data\_source\_1.

15. Select **Apply**.


## Result

You have created a local data instance and bound it to a data visualization. You can now complete the configuration of your data visualization.

-   **[Enable filters to apply to a local data instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/enable-filters-local-data-instance.md)**  
To enable a viewer to switch between which field values or breakdown elements they see in a data visualization, add filter components to the UI Builder page. For those filters to apply to a local data instance, configure that instance accordingly.
-   **[Enable data caching for a local data instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/enable-caching-local-data-instance.md)**  
To help reduce the load time of data visualizations, and if real time or very fresh data is not necessary, enable data caching on the data source.
-   **[Local data instances for multiple data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/local-data-instance-multi-viz.md)**  
A special Data Visualization API data resource is available to fetch data for multiple data visualizations simultaneously. This data resource reduces the number of API calls and thus can speed up data fetching.

**Parent Topic:**[Technical dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/technical-dashboards.md)

