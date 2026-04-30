---
title: Synchronize Group by and Stack by elements in filters
description: Synchronize Group by and Stack by elements in an interactive analysis when filters are added to the filter panel and when they are removed from the filter panel. You can also remove a filter without synchronizing group by and stack by elements.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Interactive Analysis, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Synchronize Group by and Stack by elements in filters

Synchronize Group by and Stack by elements in an interactive analysis when filters are added to the filter panel and when they are removed from the filter panel. You can also remove a filter without synchronizing group by and stack by elements.

## Before you begin

Role required: none

You must have access to the list of records that you want to analyze.

## Procedure

1.  Navigate to the table that you want to analyze.

2.  Right-click on the header of the column you want to analyze and select **Launch Interactive Analysis**.

3.  In the **Filters** panel, click **Add Filters** and add a new filter.

4.  Click **Apply Filters**.

    The new filter element appears in the **Group by** and **Stack by** lists.

5.  [Remove the filter from the interactive analysis](remove-filter-from-ia.md) to remove the filter from the **Filters** panel.

    ![Remove filter with option to Remove element from Group by and Stack by](../../reporting/image/remove-filter-gb-sb.png)

6.  Select **Remove element from Group by and Stack by**.

    The option **Remove element from Group by and Stack by** is not shown if:

    -   There is another filter on the **Filters** panel that has the same target field as the filter you are removing.
    -   You have personalized the source list before launching interactive analysis. You cannot synchronize **Group by** and **Stack by** elements by adding or removing a filter if the column is part of a personalized list.

**Parent Topic:**[Interactive Analysis](../concept/interactive-analysis.md)

