---
title: Filter decision tables
description: Apply filters to both condition and result columns in the Decision Tables in Workflow Studio. Filters can enhance the usability and efficiency of managing large Decision Tables. This feature can be used to view, modify, and reorder a subset of rows directly within the Decision Tables, without exporting the table to Excel.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Decision Tables, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Filter decision tables

Apply filters to both condition and result columns in the Decision Tables in Workflow Studio. Filters can enhance the usability and efficiency of managing large Decision Tables. This feature can be used to view, modify, and reorder a subset of rows directly within the Decision Tables, without exporting the table to Excel.

## Filtering rules and conditions

-   Saving changes: Filtering only works after you save your changes. It doesn't work in case you have unsaved changes in the table. Row options are inactive in case filtering is applied to columns.
-   No support for dynamic operators: Filtering doesn't support dynamic operators \(relative/trend operators\). Dynamic operators only show when filtering on "is not empty" or when the filter is removed.
-   Supports "read-only" view: Filtering also works in the "read-only" view of the decision table.
-   Supports cell values: Filtering only considers cell values, not operators.

## Default behavior

The default filtering operator is "is", when no other filtering is applied.

The following image shows a table interface that includes filtering functionality.

![Decision Table Filter](../image/filtering-decision-table.png)

**Parent Topic:**[Exploring Decision Tables](decision-designer-overview.md)

