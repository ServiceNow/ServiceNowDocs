---
title: Exporting hierarchy process via JSON
description: Learn how to migrate models and templates between ServiceNow instances by exporting them with all their dependencies as a single JSON file, preserving system ID continuity between source and target.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Export hierarchy of models and templates, Explore, Telecommunications Network Inventory]
---

# Exporting hierarchy process via JSON

Learn how to migrate models and templates between ServiceNow instances by exporting them with all their dependencies as a single JSON file, preserving system ID continuity between source and target.

## Exporting hierarchy via JSON overview

The Export Hierarchy action produces a JSON file containing the selected record and its complete hierarchy, including the dependent reference data the records require. The JSON file can then be imported on a target ServiceNow instance to recreate the hierarchy with system ID continuity preserved between source and target.

## Components in JSON file

A JSON export packages the selected model or template along with everything it depends on:

-   The selected record and its child records: for example, when exporting an equipment model, all child records related to that model are included
-   Dependent reference data: any records the model or template references, such as manufacturer details, product information, model classifications, and currency or pricing data
-   Inventory templates and their referenced models, when exporting a template, the models the template depends on are included automatically

The dependent reference data is included because the models and templates can't function on the target instance without their references intact. For example, an exported equipment model for a Cisco router includes the Cisco manufacturer record so that the imported model on the target instance keeps its manufacturer link.

## Roles required for Export Hierarchy

The role required for JSON export depends on what's being exported:

|Action|Roles permitted|Result|
|------|---------------|------|
|Export a model and its hierarchy|sn\_ni\_core.inventory\_admin or sn\_ni\_core.telco\_inventory\_catalog\_manage|The exported JSON contains models, child records, referenced records and related records|
|Export an inventory template and its hierarchy \(including its referenced models\)|sn\_ni\_core.inventory\_admin or sn\_ni\_core.inventory\_template\_manager|The exported JSON contains the templates, the model it references and the related recorde of both.|

Inventory admin can perform either action. Catalog Manager can export models. Template Manager can export templates and the models those templates reference.

## How Export Hierarchy via JSON works

The JSON export process operates as a single-stage interaction. When the user initiates Export Hierarchy from a model or template record, the system identifies the selected record together with all its related and referenced records, and packages them into a single JSON file. The JSON file is generated as an attachment on the Export request record. Once the export status shows Completed, the user downloads the JSON file from the right sidebar.

The downloaded JSON file is then transferred to the target instance and loaded using the JSON import feature in the Network Inventory Workspace. Importing the JSON on the target instance recreates the model or template along with its complete hierarchy of related and referenced records, preserving system ID continuity between the source and target.

This is why JSON export is the recommended path for cross-instance migration: the file contains everything needed for the records to function on the target instance, not just the records themselves.

To learn the step-by-step procedure for exporting a model or template hierarchy as JSON, see [Import models and templates in JSON format](../task/import-models-templates-json.md).

**Related topics**  


[Export hierarchy of models and templates](../task/export-hierarchy-of-models-and-template.md)

