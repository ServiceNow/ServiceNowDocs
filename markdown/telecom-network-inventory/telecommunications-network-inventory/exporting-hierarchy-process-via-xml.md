---
title: Exporting hierarchy via XML
description: Learn how to export a model or template and its related records as XML files for transfer to another ServiceNow instance.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Export hierarchy of models and templates, Explore, Telecommunications Network Inventory]
---

# Exporting hierarchy via XML

Learn how to export a model or template and its related records as XML files for transfer to another ServiceNow instance.

## Exporting hierarchy process overview

The XML export process operates as a two-stage interaction. In the first stage, the platform admin selects one or more models or inventory templates from a list view, or opens a single record from a form view, and selects Export Hierarchy. The system identifies every record related to or referenced by the selected models or templates and displays them as a consolidated list of related record links.

In the second stage, the administrator opens each related record link and exports its underlying table data as XML using the platform's standard Export action. The XML files are then transferred to the target instance and loaded using the platform's table import via XML feature. Loading the XML on the target instance recreates the model or template along with its complete hierarchy of related and referenced records.

When you export a model or template, the export includes the selected record, all of its ancestors, and all of its descendants. Sibling records at every level and their descendants are excluded.

To learn the step-by-step procedure for exporting a model or template hierarchy, see [Export hierarchy of models and templates](../task/export-hierarchy-of-models-and-template.md).

**Related topics**  


[Import model excel template](../reference/import-model-excel-template.md)

[Import template excel](../reference/import-template-excel.md)

