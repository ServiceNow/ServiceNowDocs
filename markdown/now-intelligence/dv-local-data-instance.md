---
title: Use a local data instance with a data visualization
description: For finer grained control of the data source than you have with preconfigured data sources, create a local data instance. Then bind the local data instance to the dataPassthrough property of the data visualization.To enable a viewer to switch between which field values or breakdown elements they see in a data visualization, add filter components to the UI Builder page. For those filters to apply to a local data instance, configure that instance accordingly.To help reduce the load time of data visualizations, and if real time or very fresh data is not necessary, enable data caching on the data source.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Technical dashboards, Dashboards in Platform Analytics, Platform Analytics experience, Platform Analytics]
---

# Use a local data instance with a data visualization

For finer grained control of the data source than you have with preconfigured data sources, create a local data instance. Then bind the local data instance to the **dataPassthrough** property of the data visualization.

## Before you begin

**Important:** This is an advanced procedure. Consider carefully whether you need a local data instance or can use a standard data source.

Before proceeding, review [Dynamically expose data in UI Builder pages \(advanced feature\)](https://www.servicenow.com/docs/access?context=data-resources&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Role required: ui\_builder\_admin, admin

## Procedure

1.  Open the technical dashboard or other UI Builder page in UI Builder.

2.  In the Data and scripts drawer, under Data resources, select **+ Add data resource**.

    ![Add data resource link when there are no data resources yet.](../../par-for-workspace/image/add-data-resource.png)

3.  In the Select a data resource window, search for `Data visualization`.

    You get a selection of the data resources you can use.

    ![Selection of data resources for data visualizations.](../../par-for-workspace/image/select-data-resource.png)

4.  Select a data resource that matches the type of data you want to show.

5.  Read through the information pane and copy or take notes on the configuration details.

6.  Select **Add**.

7.  Complete the configuration options that you need for the type of visualization with which you plan to use this data instance.

    Create and configure a separate local data instance for every type of visualization that you want to use the same data. For example, if you plan to have a bar and a time series that show scores from the same indicator, create two local data instances: one each for bar and time series visualizations, but both on the same indicator.

    **Tip:** You can add the data visualization to the page and compare its configuration panel to the options for the local data instance.

8.  Copy the `@data` data bind for this data source.

    ![The @data reference for a data source, with the Copy button.](../../par-for-workspace/image/data-resource-reference.png)

9.  Add the desired data visualization component to the page.

10. In the configuration panel for that data visualization, in the Data sources section, turn on **Define data manually**.

11. For the **Data** field, select **Bind data or use scripts**.

    ![Bind data option for the Data field.](../../par-for-workspace/image/bind-data-use-scripts.png)

12. In the Bind data to Data dialog, under Data types, select **Data resource**.

13. Double-click in the Add a data output to this area section and paste the data bind to your local data instance into the blue box.

14. Append `.output.result` at the end of the data bind.

    For example, the completed data bind to the local data instance data\_visualization\_api\_for\_table\_data\_source\_1 is `@data.data_visualization_api_for_table_data_source_1.output.result`.

    ![Bind data to data dialog showing data resource binding to data_visualization_api_for_table_data_source_1.](../../par-for-workspace/image/bind-data-to-data.png)

15. Select **Apply**.


## Result

You have created a local data instance and bound it to a data visualization. You can now complete the configuration of your data visualization.

**Parent Topic:**[Technical dashboards](../../performance-analytics/concept/technical-dashboards.md)

**Related topics**  


[Technical dashboards compared to inline dashboards](../../performance-analytics/reference/technical-vs-in-line-dashboards.md)

[Create a technical dashboard in UI Builder](create-tech-db-in-ac.md)

[Add a drilldown event to a data visualization in a technical dashboard](add-custom-drilldown-event.md)

[Configure an event handler for a Filter component](configure-event-handler-filter-lists-data-vis.md)

## Enable filters to apply to a local data instance

To enable a viewer to switch between which field values or breakdown elements they see in a data visualization, add filter components to the UI Builder page. For those filters to apply to a local data instance, configure that instance accordingly.

### Before you begin

Role required: ui\_builder\_admin, admin

### About this task

To enable filters to apply to a local data source, you first have to create a client state parameter named `parFilters` and then add that state parameter to the local data instance.

### Procedure

1.  Open the UI Builder page with the local data instance and data visualizations you want to filter.

2.  In the Data and scripts drawer, select **Client state parameters**.

3.  Select **+ Add**.

4.  In the Edit client state parameters dialog, name the new parameter `parFilters`, assign it type JSON, and set the initial value of `{}`.

    ![parFilters client state parameter in the Edit client state parameters dialog.](../../par-for-workspace/image/parFilters-param.png)

5.  Close the Edit client state parameters dialog.

6.  In the Data and scripts drawer, under Data resources, select the desired local data instance.

7.  In the Edit &lt;name of local data instance&gt; dialog, scroll down to the **Filter configurations** field.

8.  Enter `@state.parFilters` into the **Filter configurations** field and close the data instance editor.

9.  In the configuration panel of a data visualization that uses this local data resource, turn on **Follow filters** in the Data update section.

10. Turn on **Show filter icon**.

11. Save the UI Builder page.


### What to do next

Add filter components to the UI Builder page and configure them for relevant values from the local data instance.

**Related topics**  


[Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md)

## Enable data caching for a local data instance

To help reduce the load time of data visualizations, and if real time or very fresh data is not necessary, enable data caching on the data source.

### Before you begin

Role required: ui\_builder\_admin, admin

### Procedure

1.  Open the UI Builder page with the local data instance whose data you want to cache.

2.  In the Data and scripts drawer, under Data resources, select the desired local data instance.

3.  Scroll down to **Use data cache** and turn it on.

    Any data visualization that uses this data source, uses the cache settings on the data source. The data cache settings on the visualization itself are removed from the configuration panel.

4.  Set other caching properties as needed.

    |Property|Description|
    |--------|-----------|
    |Cache expiration time|How long the cache, once created, is retained before being updated in the cache refresh job.|
    |Invalidate cache|Use this setting with extra logic you create to invalidate the cache and fetch fresh data. For example, you can add a Button component to the page and script its event handler to invalidate the cache.|
    |Additional key|Enter a string that will contribute to generating the unique hash key for each data cache created on this data instance. Use a unique additional key value for each local data instance.|


