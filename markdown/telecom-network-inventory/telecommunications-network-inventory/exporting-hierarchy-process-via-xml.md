---
title: Exporting hierarchy via XML
description: Learn how to export a model or template and its related records as XML files for transfer to another ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/exporting-hierarchy-process-via-xml.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Export hierarchy of models and templates, Explore, Telecommunications Network Inventory]
---

# Exporting hierarchy via XML

Learn how to export a model or template and its related records as XML files for transfer to another ServiceNow instance.

## Exporting hierarchy process overview

The XML export process operates as a two-stage interaction. In the first stage, the platform admin selects one or more models or inventory templates from a list view, or opens a single record from a form view, and selects Export Hierarchy. The system identifies every record related to or referenced by the selected models or templates. It displays them as a consolidated list of related record links.

In the second stage, the administrator opens each related record link. The administrator exports its underlying table data as XML using the platform's standard Export action. The XML files are then transferred to the target instance. They are loaded using the platform's table import via XML feature. LoWhen you export a model or template, the export includes the selectedFor the step-by-step procedure for exporting a model or template hierarchy, see record, all ancestors, and all descendants.c.

Sibling records at every level and their descendants are excluded.des the selected record, all of its ancestors, and all of its descendants. Sibling records at every level and their descendants are excluded.

To learn the step-by-step procedure for exporting a model or template hierarchy, see [Export hierarchy of models and templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/export-hierarchy-of-models-and-template.md).

**Related topics**  


[Import model Excel template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/import-model-excel-template.md)

[Import template Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/import-template-excel.md)

