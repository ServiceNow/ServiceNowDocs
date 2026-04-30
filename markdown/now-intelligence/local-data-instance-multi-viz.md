---
title: Local data instances for multiple visualizations
description: A special Data Visualization API data resource is available to fetch data for multiple data visualizations simultaneously. This data resource reduces the number of API calls and thus can speed data fetching.If your use case meets the criteria for a multiple visualization data resource, you can follow this procedure.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Use a local data instance with a data visualization, Technical dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Local data instances for multiple visualizations

A special Data Visualization API data resource is available to fetch data for multiple data visualizations simultaneously. This data resource reduces the number of API calls and thus can speed data fetching.

## When to use

You can use the “Data Visualization API for multiple data visualizations” data resource in the following scenarios:

-   Multiple data visualizations of the same type have the same data source. For example, you have five visualizations where the visualization type is Single Score and the data source is the Incident \[incident\] table with the filter `active=true`. If you have several groups of indicators with the same type and data source, you can create an instance of the same multiple visualization data resource for each group.
-   A data visualization has multiple data resources that reference the same data source. For example, you have a Line visualization with a data resource from the "Number of open incidents" indicator and another data resource from the "Average age of open incidents" indicator. Both of these indicators use the Incident.Open data source. For efficiency, you can convert this visualization to use only one data resource.

## When not to use

-   There is only one visualization on the UI Builder page.
-   The data visualizations on the page are likely to take a long time to load data. In that case, it's better to keep the data loading split between separate data resources.

## Set up a multiple visualization data resource

If your use case meets the criteria for a multiple visualization data resource, you can follow this procedure.

### Before you begin

Review the use case for a single data resource for multiple visualizations in [Local data instances for multiple visualizations](local-data-instance-multi-viz.md#).

Role required: ui\_builder\_admin, admin

### About this task

**Important:** This data resource merges multiple calls into a single one. The single call is executed as a single transaction on a single thread. Therefore, use this data resource with extra care, especially when handling a large amount of data, as in some cases this might lead to transaction timeouts. Depending on the quantity of the data, the setup of the page, and the targeted user experience, you might have better results by using separate data resources.

### Procedure

1.  Navigate to the technical dashboard or UIB page with the data visualizations.

2.  Verify that the data visualizations on the page meet the criteria in **When to use**.

    For example, you have several Dial visualizations on the Incident table data source, and the amount of data fetched is not too large.

3.  In the Data and scripts drawer, under Data resources, select **+ Add data resource**.

    ![Add data resource link when there are no data resources yet.](../../par-for-workspace/image/add-data-resource.png)

4.  In the Select a data resource window, search for `Data visualization`.

    You get a selection of the data resources you can use.

    ![Selection of Data Visualization API data resources, including the one for multiple data visualizations.](../../par-for-workspace/image/dv-multiviz-data-resource.png)

5.  Select "Data Visualization API for multiple data visualizations."

6.  Set the type as **Data configurations**.

7.  In the request field, fill in the JSON.

    See the Example at the end of this procedure.

8.  In each data visualization that you want to use this data resource, perform the following actions:

    1.  Select the data visualization.

    2.  Open the Configuration panel.

    3.  Turn on **Define data manually**.

    4.  Use data binding to bind a script to the Data field.


### Data resource for three Single score visualizations with the same data source

In this example, we start with a UIB page that contains three Data Visualization components. These components all are of the Single Score visualization type, and all use the same data source.

You follow the general procedure through Step 6. Now you have a Data Visualization API for multiple data visualizations on your Dashboards page.

Next you write the JSON for the request, as follows:

```json
[
    {
        "details": {
            "visualizationId": "vis_1",
            "followFilter": true
        },
        "configurations": {
            "dataConfigurations": [
                {
                    "sourceType": "table",
                    "dataCategory": "simple",
                    "order": 0,
                    "tableOrViewName": "incident",
                    "aggregateFunction": "COUNT"
                }
            ]
        }
    },
    {
        "details": {
            "visualizationId": "vis_2",
            "followFilter": true
        },
        "configurations": {
            "dataConfigurations": [
                {
                    "sourceType": "table",
                    "dataCategory": "simple",
                    "order": 0,
                    "tableOrViewName": "incident",
                    "aggregateFunction": "AVG",
                    "aggregateField": "business_duration"
                }
            ]
        }
    },
    {
        "details": {
            "visualizationId": "vis_3",
            "followFilter": true
        },
        "configurations": {
            "dataConfigurations": [
                {
                    "sourceType": "table",
                    "dataCategory": "simple",
                    "order": 0,
                    "tableOrViewName": "incident",
                    "aggregateFunction": "AVG",
                    "aggregateField": "priority"
                }
            ]
        }
    }
]
```

The request is an array of objects, one for each data visualization. Each visualization has a **details** property with an arbitrary value for the **visualizationId** and a boolean **followFilter** setting whether the visualization follows filter components on the page. In this case, all three visualizations follow filters.

Each visualization also has a **configurations** property, containing only a **dataConfigurations** array. Because all the visualizations are of the same type, Single Score, and this visualization type shows only a simple value, all three **dataCategory** properties are "simple." Similarly, all the visualizations use the same data source. Because the data source is the Incident \[incident\] table, all three visualizations have a **sourceType** of "table" and a **tableOrViewName** of "incident." The only place where the visualizations can vary is in the aggregates they use. Here you see the first one uses a COUNT aggregation, the second takes an AVG aggregate on the business\_duration field, and the third takes an AVG of the priority field.

The final configuration of the data resource looks like this:

![Complete configuration of dashboard data broker.](../../par-for-workspace/image/db-data-res-mult-viz-config.png)

Lastly, for each data visualization, you bind the following script to the data field. You use the arbitrary **visualizationId** value you gave each visualization as the `vizId` value in the script for that visualization.

```javascript
function evaluateProperty({api, helpers}) {
  const data = api.data.data_visualization_api_for_multiple_data_visualizations_1.output;
​
  if (!data) {
    return [];
  }
​
  const vizId = 'vis_1';
​
  const dataForViz = data.result.find(d => d.details.visualizationId === vizId);
​
    return dataForViz.dataResponses;
}
```

### Request JSON for an indicator

The request for a visualization on an indicator differs from the previous example, which was for a table. Here is the JSON for a time series visualization, which shows a trend over time, for the Number of open incidents indicator, grouped by the Priority breakdown:

```json
[
    {
        "details": {
            "visualizationId": "vis1",
            "followFilter": true
        },
        "configurations": {
            "dataConfigurations": [
                {
                    "sortBy": "choice",
                    "sortOrder": "asc",
                    "sourceType": "indicator",
                    "dataCategory": "trend",
                    "order": 0,
                    "splitView": false,
                    "numberOfGroups": 2,
                    "uuid": {
                        "indicator": "fb007202d7130100b96d45a3ce6103b4",
                        "breakdowns": []
                    },
                    "trendBy": "anything",
                    "trendInterval": "date",
                    "groupBy": [
                        "0df47e02d7130100b96d45a3ce610399"
                    ],
                    "removeMissingIntervalData": false
                }
            ]
        }
    }
]
```

The first and obvious differences are that the **sourceType** is "indicator" and the **dataCategory** is "trend." You also see that instead of a **tableOrViewName** property, you have a **uuid** object with the uuid of the Number of open incidents indicator and an empty array that could hold the uuid's of breakdowns for filtering that indicator. Because this visualization supports group-by values, you have a **groupBy** array that in this case contains only the uuid of the Priority breakdown. Having a group-by implies sorting, and here you see that the **sortBy** is "choice," reflecting the data type of the Priority breakdown, and the **sortOrder** is ascending.

