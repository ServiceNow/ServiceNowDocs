---
title: Run a partial CMDB query
description: You can run a partial query in the CMDB Query Builder by defining a section of a query, and then running it.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Run a partial CMDB query

You can run a partial query in the CMDB Query Builder by defining a section of a query, and then running it.

## Before you begin

Role required: cmdb\_query\_builder \(contained for itil, itil\_admin, and asset\)

## About this task

While building a query or reviewing a saved query, you can run only a section of the query. On the canvas in the CMDB Query Builder, highlight a section of the query which contains the nodes and relationships of the partial query that you want to run. You can then examine the results of the partial query, and update the query if needed.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Query Builder**.

2.  On the CMDB Query Builder page, select a tile to open an existing query.

3.  Select the selection tool under the [navigation tool](../reference/navigation-cmdb-query-builder.md) to switch to a section selection mode.

4.  Border a section of the query:

    1.  Select the upper left corner of the section.

    2.  Drag and release at the bottom right corner of the section that you want to create.

        As the cursor moves, the selected section is highlight in light blue. The query nodes that are included in the partial query, appear with a blue border.

5.  Select **Run**.

6.  In the Pick Starting Node dialog box, select the starting node for the partial query and then select **Confirm**.


## Result

The results of the partial query appear in the Results pane.

