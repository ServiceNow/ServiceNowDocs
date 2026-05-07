---
title: Export hierarchy of models and templates as JSON
description: Learn how to export network equipment models, inventory templates, and their related records from an instance. Use this feature to promote validated configurations from a lower environment to production.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Import models and templates, Use, Telecommunications Network Inventory]
---

# Export hierarchy of models and templates as JSON

Learn how to export network equipment models, inventory templates, and their related records from an instance. Use this feature to promote validated configurations from a lower environment to production.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin / sn\_ni\_core.telco\_inventory\_catalog\_manager / sn\_ni\_core.inventory\_template\_manager

## About this task

The Export Hierarchy feature lets you download a selected inventory model or template along with all its related records as a single package. Instead of exporting each related record individually, Export Hierarchy captures the complete structure — the parent record and all child records in one operation, preserving the relationships between them.

## Procedure

1.  Navigate to Workspaces &gt; Network Inventory Workspace.

2.  Select the list icon \(☰\) and select a model or inventory template category.

3.  From the list, select the inventory model or template you want to export.

4.  In the record header, select the context menu icon \(⋮\) next to Normalize.

5.  Select Export Hierarchy.

    The Export request record opens and displays the export status. When the Status field shows Completed, the exported JSON file is available as an attachment. If the attachment is not visible even though the status shows Completed, refresh the page.

6.  On the right sidebar, click the attachment icon \(📎\) to download the exported JSON file.


## Result

The JSON file containing the selected model or template and all its related records is downloaded to your local system, ready to import into the target instance.

**Parent Topic:**[Import models and templates](../concept/import-models-and-templates.md)

**Related topics**  


[Export hierarchy of models and templates as JSON](export-hierarchy-of-models-and-templates-as-json.md)

