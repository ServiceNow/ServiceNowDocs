---
title: DashboardMessageHandler
description: Provides methods to define custom filtering logic for interactive filters.Instantiate a DashboardMessageHandler object with a given unique ID.Each DashboardMessageHandler object can publish a single filter.Apply a custom interactive filter to multiple tables.Removes the current filter published by this DashboardMessageHandler object from all reports on the dashboard.
locale: en-US
release: xanadu
product: Interactive Filters
classification: interactive-filters
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Custom interactive filters, Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# DashboardMessageHandler

Provides methods to define custom filtering logic for interactive filters.

For more information about interactive filters, see [reporting](../../../../../use/reporting/reference/reporting-landing-page.md) and [interactive filters](../../../../../use/dashboards/concept/c_HomepagePublishers.md).

**Parent Topic:**[Custom interactive filters](../../../../../use/dashboards/concept/c_CustomPublishers.md)

## DashboardMessageHandler - DashboardMessageHandler\(String id\)

Instantiate a DashboardMessageHandler object with a given unique ID.

|Name|Type|Description|
|----|----|-----------|
|Id|String|A unique ID for the filter. This ID allows report widgets to track which filter applied each filter. The ID does not need to be unique across all dashboards, but each dashboard cannot have multiple filters with the same ID.|

```
var my_dashboardMessageHandler = new DashboardMessageHandler("my_unique_id");
```

## DashboardMessageHandler - publishFilter\(String table, String encodedQuery\)

Each DashboardMessageHandler object can publish a single filter.

Publishing a new filter from the same object overwrites the original filter. Use multiple DashboardMessageHandler objects to publish multiple filters.

|Name|Type|Description|
|----|----|-----------|
|table|String|The table to filter, such as task.|
|encodedQuery|String|An encoded query that specifies the filter to publish.|

|Type|Description|
|----|-----------|
|void| |

```
var my_dashboardMessageHandler = new DashboardMessageHandler("my_unique_id");
<input id="onlyMine" type="button" value="Only mine" 
  onclick="my_dashboardMessageHandler.publishFilter('task','caller_idDYNAMIC90d1921e5f510100a9ad2572f2b477fe');"/>
```

## DashboardMessageHandler - publishMessage\(Array filters\)

Apply a custom interactive filter to multiple tables.

<table id="table_tgg_zjt_gtb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

filters

</td><td>

Array

</td><td>

Array of filter objects that define the tables to filter and the filter criteria.```
[
  {
    "table": String,
    "filter": String 
  }
]
```

</td></tr><tr><td>

filters.table

</td><td>

String

</td><td>

Name of the table to filter.

</td></tr><tr><td>

filters.filter

</td><td>

String

</td><td>

Encoded query containing the filter criteria to apply to the table.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This jelly script filters the Incident and Problem tables to return records where the assignment group is Problem solving.

```
<?xml version="1.0" encoding="utf-8" ?>
<j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
<script>
 var dmh = new DashboardMessageHandler("aha_dmh");
 var filter = "cmdb_ci.sys_idINcdafbfc9db8f570466e0a345ca96198a"; 
 //this is the encoded query string
 var fullFilter = dmh.getFilterMessage('change_request',filter); 
 //creates a JSON object

 SNC.canvas.interactiveFilters.setDefaultValue({id: dmh.aha_dmh, filters:[fullFilter],}, false);
 var published = dmh.publishMessage([fullFilter]);
</script>

</j:jelly>
```

## DashboardMessageHandler - removeFilter\(\)

Removes the current filter published by this DashboardMessageHandler object from all reports on the dashboard.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var my_dashboardMessageHandler = new DashboardMessageHandler("my_unique_id");
<input id="removeFilter" type="button" value="Remove filter" 
  onclick="my_dashboardMessageHandler.removeFilter();"/>
```

