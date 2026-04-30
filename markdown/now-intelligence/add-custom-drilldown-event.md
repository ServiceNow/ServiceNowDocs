---
title: Add a drilldown event to a data visualization in a technical dashboard
description: Technical dashboards do not support preconfigured destinations for drilling down from a data visualization. If you want a viewer to open a more detailed view of the data when they interact with a visualization, configure a custom drilldown event.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
keywords: [Add a drilldown event to a data visualization in UI Builder, Add a drilldown event to a report in UI Builder]
breadcrumb: [Technical dashboards, Dashboards in Platform Analytics, Platform Analytics experience, Platform Analytics]
---

# Add a drilldown event to a data visualization in a technical dashboard

Technical dashboards do not support preconfigured destinations for drilling down from a data visualization. If you want a viewer to open a more detailed view of the data when they interact with a visualization, configure a custom drilldown event.

## Before you begin

This procedure assumes that you have already created a technical dashboard and populated it with a data visualization component.

Role required: ui\_builder\_admin, rights to edit a technical dashboard

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Locate and open the desired technical dashboard.

3.  Select **Edit in UI Builder**.

4.  In the UI Builder, select the desired data visualization in the dashboard.

5.  In the configuration panel for the data visualization, open the **Events** tab.

6.  Select **+ Add event mapping**.

    The Select an event dialog opens.

    ![The Select an event dialog in a data visualization.](../../par-for-workspace/image/db-events-vis-clicked.png)

7.  Select the **Visualization Clicked** event.

    A dialog opens with a list of available event handlers.

8.  Select the **Advanced dashboards - Redirect** event handler.

    The configuration fields for this event handler appear.

    ![Dialog for configuring the Advanced dashboards - Redirect event handler.](../../par-for-workspace/image/db-adv-db-redirect.png)

9.  Configure the event handler as follows.

    |Field|Description|
    |-----|-----------|
    |Context|The path of the experience where the destination page resides.|
    |Route|The route name of the destination page.|
    |Route fields|Required parameters for the destination page.|
    |Optional parameters|Optional parameters for the destination page.|

10. Select **Add**.


## Drilldown for a table data source

You have a vertical data visualization that shows the number of records on the Incident \[incident\] table grouped by Priority. When a viewer interacts with this visualization, you want it to open a list of Incident records in the Platform Analytics experience.

1.  You follow Steps 1-8 in the general procedure, so you now have the configuration open for the Advanced dashboards - Redirect event handler for your vertical bar visualization.
2.  In the Context field, you select **Edit**.

    ![The Edit control in the Context field.](../../par-for-workspace/image/db-adv-db-ex-edit-context.png)

3.  In the editing dialog, you select the object JSON type.

    ![Selecting the object JSON type for the Context.](../../par-for-workspace/image/db-adv-db-ex-json-object.png)

4.  You select **Add property** and enter `path` as the property name and `now/platform-analytics-workspace` as the property value. These values specify that the viewer drills down to the Platform Analytics experience.

    ![Setting the value of the Context.](../../par-for-workspace/image/db-adv-db-ex-context-value-table.png)

5.  You select **Apply** and move on to the next field.
6.  In the Route field, you enter `simplelist`. This route leads to the simplelist page in the Platform Analytics experience.
7.  For the Route fields, you first choose to bind data. ![Selecting to bind data.](../../par-for-workspace/image/bind-data.png)
8.  Then you add the property `{table: @payload.params.table}` to the field. This property passes the name of the table in your visualization to the simplelist page of the Platform Analytics experience.
    1.  You select the Event payload property `@payload.params.table`.

        ![Selecting the payload.params.table property in the data binding editor.](../../par-for-workspace/image/db-tech-adv-redirect-table-param.png)

    2.  You double-click, drag and drop, or select the arrow to add the property to the upper area of the editor.
    3.  Double-click on the property in the upper area of the editor to open it for editing.

        ![Double-clicking the property pill to open it for editing.](../../par-for-workspace/image/db-adv-event-edit-prop.gif)

    4.  You surround the `@payload.params.table`property with curly brackets and add the `table:` property.

        ![Completing the table property.](../../par-for-workspace/image/db-tech-event-complete-parm.gif)

    5.  You select **Apply**.
9.  Similarly, you choose to bind data for the Optional parameters field and set the values `{query: @payload.params.query, listTitle: @payload.title}`.
    1.  In the Optionals Parameters field, add `{query: @payload.params.query}` as you did for `{table: @payload.params.table}`, but do not select **Apply**.
    2.  Select the **Add another input** \(+\) button.
    3.  Add `listTitle: @payload.title` inside the curly brackets.

        ![Adding a second optional property.](../../par-for-workspace/image/db-tech-event-2-props.gif)

    4.  You select **Apply**.

The properties of your Advanced dashboards - Redirect event handler now appear as follows:

|Field|Value|
|-----|-----|
|Context|\{path:now/platform-analytics-workspace\}|
|Route|simplelist|
|Route fields|\{table:@payload.params.table\}|
|Optional parameters|\{query:@payload.params.query, listTitle:@payload.title\}|

In runtime, a user can interact with the visualization to open a list of Incident records.

![Opening a list of Incident records by clicking a Single Score visualization on a technical dashboard.](../../par-for-workspace/image/db-adv-ex-ddown-table.gif)

## Drilldown for an indicator data source

You have a Line data visualization for the indicator Number of open incidents. When a viewer interacts with this visualization, you want it to open the KPI Details page for that indicator.

1.  You repeat steps 1-5 from the Table data source example, because in this case too you are drilling down to a page on the Platform Analytics experience.
2.  For the Route, you enter `ac_kpi_details`.
3.  For the Route fields, you first choose to bind data ![Selecting to bind data.](../../par-for-workspace/image/bind-data.png). Then you enter `{uuid: @payload.params.indicatorSysid}`. This parameter passes the id of the indicator, in this case Number of open incidents, to the Platform Analytics experience KPI Details page.

    **Tip:** First use autocomplete to add the data parameter `@payload.params.indicatorSysid`, then surround that parameter with curly brackets and add `uuid:`.

    The properties of your Advanced dashboards - Redirect event handler now appear as follows:

    |Field|Value|
    |-----|-----|
    |Context|\{"path":"now/platform-analytics-workspace"\}|
    |Route|ac\_kpi\_details|
    |Route fields|\{uuid:@payload.params.indicatorSysid\}|

4.  No other parameters are necessary, so you select **Add** and then **Save** the UI Builder page.

In runtime, a viewer can interact with the visualization to open KPI Details for the Number of open incidents indicator.

![Opening KPI Details by clicking a Line visualization on a technical dashboard.](../../par-for-workspace/image/db-adv-ex-ddown-indicator.gif)

**Parent Topic:**[Technical dashboards](../../performance-analytics/concept/technical-dashboards.md)

**Related topics**  


[Technical dashboards compared to inline dashboards](../../performance-analytics/reference/technical-vs-in-line-dashboards.md)

[Create a technical dashboard in UI Builder](create-tech-db-in-ac.md)

[Configure an event handler for a Filter component](configure-event-handler-filter-lists-data-vis.md)

[Use a local data instance with a data visualization](dv-local-data-instance.md#)

