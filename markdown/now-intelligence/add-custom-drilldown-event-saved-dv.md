---
title: Add a drilldown event to a saved data visualization on a technical dashboard
description: Technical dashboards do not support preconfigured destinations for drilling down from a data visualization. If you want a viewer to open a more detailed view of the data when they interact with a visualization, configure a custom drilldown event.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 3
keywords: [Add a drilldown event to a data visualization in UI Builder, Add a drilldown event to a report in UI Builder]
breadcrumb: [Technical dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Add a drilldown event to a saved data visualization on a technical dashboard

Technical dashboards do not support preconfigured destinations for drilling down from a data visualization. If you want a viewer to open a more detailed view of the data when they interact with a visualization, configure a custom drilldown event.

## Before you begin

This procedure assumes that you have already created a technical dashboard and populated it with a data visualization component.

Role required: ui\_builder\_admin, rights to edit a technical dashboard

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Open the desired technical dashboard.

3.  Select **Edit in UI Builder**.

4.  In UI Builder, select the saved data visualization on the dashboard.

5.  In the configuration panel for the data visualization, select the **Events** tab.

6.  Select **Item clicked or View all** &gt; **Add handler**.

7.  Select the **Advanced dashboards - Redirect** event handler.

8.  Configure the event handler as follows.

    |Field|JSON types|Description|
    |-----|----------|-----------|
    |Context|object, with a string property named path|The path of the experience where the destination page resides.|
    |Route|none|The route name of the destination page.|
    |Route fields|object, with all parameters as strings|Required parameters for the destination page.|
    |Optional parameters| |Optional parameters for the destination page.|

9.  Select **Add**.


## Drilldown to a simple list component

You have a vertical data visualization that shows the number of records on the Incident \[incident\] table grouped by Priority. When a viewer interacts with this visualization, you want it to open a list of Incident records in the Platform Analytics experience.

**Note:** This example uses the Context of the Platform Analytics experience and default Route names to components therein.

1.  You follow Steps 1-8 in the general procedure, so you now have the configuration open for the Advanced dashboards - Redirect event handler for your vertical bar visualization.
2.  In the Context field, you type `{“path”:”now/platform-analytics-workspace"}`.

    This specifies that the viewer drills down to the Platform Analytics experience.

3.  In the Route field, you enter `simplelist`. This route leads to the simplelist page in the Platform Analytics experience.
4.  For the Route fields, you first choose to bind data. ![Selecting to bind data.](../../par-for-workspace/image/bind-data.png)
5.  Then you add the property `{table: @payload.payload.params.table}` to the field. This property passes the name of the table in your visualization to the simplelist page of the Platform Analytics experience.
6.  Similarly, you choose to bind data for the Optional parameters field and set the value `{query: @payload.payload.params.query, listTitle: @payload.payload.title}`.

The properties of your Advanced dashboards - Redirect event handler now appear as follows:

|Field|Value|
|-----|-----|
|Context|\{path:now/platform-analytics-workspace\}|
|Route|simplelist|
|Route fields|\{table:@payload.params.table\}|
|Optional parameters|\{query: @payload.payload.params.query, listTitle: @payload.payload.title\}|

In runtime, a user can interact with the visualization to open a list of Incident records.

![Opening a list of Incident records by clicking a Single Score visualization on a technical dashboard.](../../par-for-workspace/image/db-adv-ex-ddown-table.gif)

## Drilldown for an indicator data source

You have a Line data visualization for the indicator Number of open incidents. When a viewer interacts with this visualization, you want it to open the KPI Details page for that indicator.

1.  You repeat steps 1-5 from the Table data source example, because in this case too you are drilling down to a page on the Platform Analytics experience.
2.  For the Route, you enter `ac_kpi_details`.
3.  For the Route fields, you first choose to bind data ![Selecting to bind data.](../../par-for-workspace/image/bind-data.png). Then you enter `{uuid: @payload.payload.params.indicatorSysid}`. This parameter passes the id of the indicator, in this case Number of open incidents, to the Platform Analytics experience KPI Details page.

    **Tip:** First use autocomplete to add the data parameter `@payload.payload.params.indicatorSysid`, then surround that parameter with curly brackets and add `uuid:`.

    The properties of your Advanced dashboards - Redirect event handler now appear as follows:

    |Field|Value|
    |-----|-----|
    |Context|\{"path":"now/platform-analytics-workspace"\}|
    |Route|ac\_kpi\_details|
    |Route fields|\{uuid:@payload.payload.params.indicatorSysid\}|

4.  No other parameters are necessary, so you select **Add** and then **Save** the UI Builder page.

In runtime, a viewer can interact with the visualization to open KPI Details for the Number of open incidents indicator.

![Opening KPI Details by clicking a Line visualization on a technical dashboard.](../../par-for-workspace/image/db-adv-ex-ddown-indicator.gif)

**Parent Topic:**[Technical dashboards](../../performance-analytics/concept/technical-dashboards.md)

**Related topics**  


[More examples and information are available in KB2663434](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2663434)

