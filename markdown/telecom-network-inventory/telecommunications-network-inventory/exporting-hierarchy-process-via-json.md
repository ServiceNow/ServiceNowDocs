---
title: Exporting hierarchy process via JSON
description: Learn how to migrate models and templates between ServiceNow instances by exporting them with all their dependencies as a single JSON file. The export preserve system ID continuity between source and target.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/exporting-hierarchy-process-via-json.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 2
breadcrumb: [Export hierarchy of models and templates, Explore, Telecommunications Network Inventory]
---

# Exporting hierarchy process via JSON

Learn how to migrate models and templates between ServiceNow instances by exporting them with all their dependencies as a single JSON file. The export preserve system ID continuity between source and target.

## Exporting hierarchy via JSON overview

The Export Hierarchy action produces a JSON file containing the selected record and its complete hierarchy. This includes the dependent reference data the records require. You can import the JSON file on a target ServiceNow instance to recreate the hierarchy. System ID continuity is preserved between source and target.

## Components in JSON file

A JSON export packages the selected model or template along with everything it depends on:

-   -   Dependent reference data: Any records the model or template references, such as manufacturer details, product information, model classifications, and currency or pricing data.
-   Inventory templates and their referenced models: When you export a template, the models the template depends on are included automatically

The dependent reference data is included because the models and templates can't function on the target instance without their references intact. For example, an exported equipment model for a Cisco router includes the Cisco manufacturer record. This ensures the imported model on the target instance keeps its manufacturer link.

## Roles required for Export Hierarchy

The role required for JSON export depends on what's being exported:

|Action|Roles permitted|Result|
|------|---------------|------|
|Export a model and its hierarchy|sn\_ni\_core.inventory\_admin or sn\_ni\_core.telco\_inventory\_catalog\_manage|The exported JSON contains models, child records, referenced records and related records|
|Export an inventory template and its hierarchy \(including its referenced models\)|sn\_ni\_core.inventory\_admin or sn\_ni\_core.inventory\_template\_manager|The exported JSON contains the templates, the model it references and the related recorde of both.|

Inventory admin can perform either action. Catalog Manager can export models. Template Manager can export templates and the models those templates reference.

## How Export Hierarchy via JSON works

The JSON export process operates as a single-stage interaction. When you initiate the Export Hierarchy function from a model or template record, the system identifies the selected record together with all its related and referenced records. The system packages them into a single JSON file. The JSON file is generated as an attachment on the Export request record. After the export status shows Completed, you can download the JSON file from the right sidebar.

You can transfer the downloaded JSON file to the target instance. Load it using the JSON import feature in the Network Inventory Workspace. Importing the JSON on the target instance recreates the model or template along with its complete hierarchy. System ID continuity is preserved between the source and target.

This is why JSON export is the recommended path for cross-instance migration. The file contains everything needed for the records to function on the target instance, not just the records themselves.

To learn the step-by-step procedure for exporting a model or template hierarchy as JSON, see [Import models and templates in JSON format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/import-models-templates-json.md).

**Related topics**  


[Export hierarchy of models and templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/export-hierarchy-of-models-and-template.md)

