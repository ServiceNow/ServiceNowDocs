---
title: Dot-walking from reference fields in a data visualization
description: Dot-walking provides access to fields on extended, or related, tables, enabling you to create data visualizations on fields from those tables.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [related tables, extended tables, dot-walking]
breadcrumb: [Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Dot-walking from reference fields in a data visualization

Dot-walking provides access to fields on extended, or related, tables, enabling you to create data visualizations on fields from those tables.

You can access references on extended tables from the Metric, Group by/Stack by, column/row, or Trend by fields in the Configuration panel, or when you add custom conditions when you choose the data source. The Sorting option also enables you to configure the sort order of applicable reference fields on extended tables. Tables that reference other tables are denoted with an arrow \(![Expand icon for data visualizations](../../par-for-workspace/image/icon-dv-expand.png)\) icon.

Dot-walking references a field by building a chain of field names separated by dots \(periods\). For instance, **incident.assigned\_to.company** references the company of the user assigned to an incident. The recommended limit for chain length is three levels.

**Note:** Dot-walking applies only to visualizations of table data sources.

-   **[Dot walk fields in Visualization Designer](access-fields-ext-table-vis-des.md)**  
Learn how to dot walk table fields in a data visualization of table data. See how to start from a parent table, such as Task, and dot walk to include data from extended tables, such as Indicator and Problem.

**Parent Topic:**[Configure data visualizations](../../performance-analytics/concept/configure-data-visualizations.md)

**Related topics**  


[bundle-platux.dot-walking-examples]

