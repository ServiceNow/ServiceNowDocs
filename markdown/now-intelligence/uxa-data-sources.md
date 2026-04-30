---
title: User Experience Analytics data sources for visualizations
description: You can show metrics related to User Experience Analytics in a data visualization component. The available metrics depend on the visualization type.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Data sources for data visualizations, Data visualizations in Platform Analytics, Platform Analytics]
---

# User Experience Analytics data sources for visualizations

You can show metrics related to User Experience Analytics in a data visualization component. The available metrics depend on the visualization type.

**Note:** Users require the admin, analytics\_admin, or analytics\_viewer role to add User Experience Analytics data sources to a visualization.

The User Experience Analytics PAR Integration application, available in the [ServiceNow® Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home), provides several KPIs that you can use as data sources.

-   **Events**

    This KPI tracks the events that are triggered on the application. When you select this KPI as a data source on a visualization, you also must select the application and the event. In a Bar or Pie/Donut visualization, use the **Group by** field to select an event property. You can then view the number of occurrences and the values distribution of that single event property.

-   **Sessions**

    This KPI tracks the number of sessions triggered on an application.

    When you select this KPI as a data source on a visualization, you also must select the application and the category. For Single Score visualizations only, you can select a condition as the category. You can add or edit conditions in the condition builder. Filters support only 90 days of data.

    -   All Sessions: Represents the number of all sessions created on the application.
    -   New Sessions: Represents the number of sessions that were created in the most recent time period.
    -   Returning Users: Users who have created more than one session.
    -   Loyal Users: Users who have created 5 or more sessions.
    -   Short sessions: Number of sessions shorter than 20 seconds.
    -   Long sessions: Number of sessions longer than 300 seconds.
    -   Custom: You define this category by creating at least one condition.
-   **Users**

    The number of active unique users using the application. When you select this KPI as a data source on a visualization, you also must select the application and the category of user. For Single Score visualizations only, you can select a condition as the category. You can add or edit conditions in the condition builder. Filters support only 90 days of data.

    -   Active Users: Represents the number of all users in the application.
    -   New Users: Represents the number of users who have performed their first session.
    -   Returning Users: Users who have created more than one session.
    -   Loyal Users: Users who have created 5 or more sessions.
    -   Never Returned Users: Users who have created only 1 session.
    -   Multi Device Users: Users who have created a session with more than 1 device.
    -   Custom: You define this category by creating at least one condition.

**Important:** You must specify the date range for all User Experience Analytics data sources on all visualization types.

The following data visualizations do not support User Experience Analytics data sources:

-   Calendar
-   Geomap
-   Heatmap
-   Simple List
-   Indicator Scorecard

The following data visualizations only support Events.

-   Pivot table
-   Pie/Donut
-   Bar

Time series and score data visualizations support all User Experience Analytics data sources.

<table id="table_g3k_3sh_h1c"><thead><tr><th>

Metric

</th><th>

Supported visualization type

</th><th>

Group by

</th><th>

Response

</th></tr></thead><tbody><tr><td>

Events

</td><td>

-   Scores \(Single score, dial, gauge\)
-   Time series
-   Bars, including Pareto
-   Pies and donuts
-   Pivot tables

</td><td>

Bars, Pivot tables, and Pies/donuts: Supported by the event's property

 Other visualization types: Not supported

</td><td>

Time series: Number of events in the date range

 Scores: Number of occurrences of the event

 Bars, Pie/Donut, Pivot: Breakdown of event in date range by property

</td></tr><tr><td>

Sessions

</td><td>

-   Time series
-   Scores

</td><td>

Not supported

</td><td>

Time series: Number of sessions in the date range

 Scores: Number of created sessions. Single score also allows responses filtered by conditions.

</td></tr><tr><td>

Users

</td><td>

-   Time series
-   Scores

</td><td>

Not supported

</td><td>

Time series: Number of active or new users in the date range

 Scores: Number of active or new users. Single score also allows responses filtered by conditions.

</td></tr></tbody>
</table>**Parent Topic:**[Data sources for data visualizations](../../par-for-workspace/reference/data-sources-visualizations.md)

**Related topics**  


[Indicator management and Performance Analytics](../../par-for-workspace/concept/indicator-data-sources-pa.md)

[Multiple data sources](../../par-for-workspace/reference/multiple-data-sources.md)

