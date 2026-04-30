---
title: Apply metrics
description: Refine your project visualization to show the KPIs and metrics that are more relevant to your process goals.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Filtering project data, Analyzing and getting process insights, Using Process Mining, Process Mining, Platform Analytics]
---

# Apply metrics

Refine your project visualization to show the KPIs and metrics that are more relevant to your process goals.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

**Note:** Duration metrics do not apply to activities, so aren't displayed for them.

## Procedure

1.  From the process map screen, select from the list the **Primary Metric** you want the map to show.

    |Metric|Description|
    |------|-----------|
    |**Total Occurrences**|Number of records that follow a route, including repetitions. Default option.|
    |**Unique Occurrences**|Number of records that follow a route, excluding repetitions.|
    |**Max Repeat Occurrences**|Maximum number of times an activity or connection repeated in the same route.|
    |**Min Duration**|Shortest time a record took to complete a route.|
    |**Max Duration**|Longest time a record took to complete a route.|
    |**Avg Duration**|Average time in days that records took to complete a route, from the time records were opened to closed.|
    |**Total Duration**|Sum total of all duration times, from the first to the last event, for all records that follow a route.|
    |**Std Deviation**|Variation from the route duration average value.|
    |**Med Duration**|Duration middle value, or average of two middle values.|

2.  Select a **Secondary Metric** to show.


## Result

The process map automatically refreshes showing the metric selection. The numbers on the metrics box \(![metrics-boxes](../image/metrics-boxes.png)\) on a route correspond to the metrics you selected.

**Parent Topic:**[Filtering project data](filter-project.md)

