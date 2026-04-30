---
title: SummaryTableWriter - Global
description: The SummaryTableWriter script include enables the creation of summary sets for reports that can be generated with standard queries and trending.Produces a summary set for the COUNT of all incidents grouped by category.Creates the summary set of records for reports.Defines the query to use to load the data for the summary record set.Defines the column on which to stack the incident records.Sets the title of the summary set, which is also the chart title.Sets the time field used for the X axis or stacking field; can also set the time interval used to calculate the trend.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SummaryTableWriter- Global

The SummaryTableWriter script include enables the creation of summary sets for reports that can be generated with standard queries and trending.

This script include provides methods that enable you to customize the output of the summary sets for reports, such as adding a title, defining a query on which to base the report data, and specifying the stack column and X axis.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SummaryTableWriter - SummaryTableWriter\(String tableName, String columnName\)

Produces a summary set for the COUNT of all incidents grouped by category.

The custom chart definition table contains a field named **Table** that is hidden by default. If the field is set, which it is in some of the base custom charts, then, no matter what is defined within the custom chart scripts, clicking on the chart points you to this table.

For example, if you create a custom chart against the `[task]` table through a script, but you copied the custom chart from a custom chart that contains Table = incident, then clicking on any bar in the custom script will go to incident.do rather than to task.do.

To check the value of the **Table** field, click the additional actions icon and select **Configure** &gt; **Form Layout** and move the **Table** field from **Available** to **Selected**. Open the custom chart definition and set the **Table** field to **none**.

<table id="table_tlc_qjv_qx" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

tableName

</td><td>

String

</td><td>

Table used in the query to generate the data.

</td></tr><tr><td>

columnName

</td><td>

String

</td><td>

Field that is used to determine the X axis values.

</td></tr></tbody>
</table>```
var summarySet = new SummaryTableWriter('incident', 'category');
summarySet.generate();
```

## SummaryTableWriter - generate\(\)

Creates the summary set of records for reports.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var opened = new SummaryTableWriter('incident', '');
opened.generate();
```

## SummaryTableWriter - setQuery\(String query\)

Defines the query to use to load the data for the summary record set.

|Name|Type|Description|
|----|----|-----------|
|query|String|Query to use to load the summary data.|

|Type|Description|
|----|-----------|
|void| |

```
var summarySet = new SummaryTableWriter('incident', 'category');
summarySet.setQuery("active=true");
summarySet.generate();
```

## SummaryTableWriter - setStackOn\(String column\)

Defines the column on which to stack the incident records.

|Name|Type|Description|
|----|----|-----------|
|column|String|Column that is used to stack the incident records.|

|Type|Description|
|----|-----------|
|void| |

```
var summarySet = new SummaryTableWriter('incident', 'category');
summarySet.setQuery("active=true");
summarySet.setStackOn('priority');
summarySet.generate();
```

## SummaryTableWriter - setTitle\(String title\)

Sets the title of the summary set, which is also the chart title.

|Name|Type|Description|
|----|----|-----------|
|title|String|Title given to the summary set that is used as the chart title. Also used as the key field for chart generators to determine whether the data was generated.|

|Type|Description|
|----|-----------|
|void| |

```
var opened = new SummaryTableWriter('incident', '');
opened.setTitle("Trend of Open Incidents");
opened.setTrend('opened_at', 'month');
opened.generate();
```

## SummaryTableWriter - setTrend\(String field, String interval\)

Sets the time field used for the X axis or stacking field; can also set the time interval used to calculate the trend.

|Name|Type|Description|
|----|----|-----------|
|field|String|Time field that is used for X axis values if grouping is not used. If grouping is used, then this is the stacking field.|
|interval|String|Time interval that is used to calculate the trend.|

|Type|Description|
|----|-----------|
|void| |

```
var opened = new SummaryTableWriter('incident', '');
opened.setTitle("Trend of Open Incidents");
opened.setTrend('opened_at', 'month');
opened.generate();
```

