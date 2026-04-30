---
title: Create a data visualization based on multiple data sets
description: Here's a simple example of creating a report based on multiple datasets.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-07-30"
reading_time_minutes: 1
breadcrumb: [Data visualizations in Platform Analytics, Platform Analytics]
---

# Create a data visualization based on multiple data sets

Here's a simple example of creating a report based on multiple datasets.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. If you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../concept/report-view-access-control.md) and [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

2.  Select **New**.

3.  For the purposes of this example, create a Vertical bar visualization based on the Incident \[incident\] table.

    For more information, see [Create a horizontal or vertical bar data visualization](create-dv-bar-ac.md).

4.  Add two data sources: the Incident \[incident\] table and the Problem \[problem\] tables.

5.  For each data source, add the custom condition `Active is true`.

6.  In the Metric section, select the Count aggregation for both sources.

7.  Group the visualization by Assignment Group.

8.  Select Save and name the visualization `Incidents and Problems by Assignment Group`.

9.  To make the visualization easier to read, under **Chart variation**, select `Side-by-side`.


