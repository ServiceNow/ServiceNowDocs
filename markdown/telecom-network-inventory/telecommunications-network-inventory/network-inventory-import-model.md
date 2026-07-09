---
title: Import
description: Use the import feature to bring equipment models and templates into the system in bulk. You can import using Excel or JSON, and migrate components across instances while preserving system IDs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/telecom-network-inventory/telecommunications-network-inventory/network-inventory-import-model.html
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-07-09"
reading_time_minutes: 2
breadcrumb: [Explore, Telecommunications Network Inventory]
---

# Import

Use the import feature to bring equipment models and templates into the system in bulk. You can import using Excel or JSON, and migrate components across instances while preserving system IDs.

## Import Overview

Equipment models and templates must exist in the system before you can define model relationships or instantiate network inventory records. The import feature lets you bring in existing model data from manufacturer datasheets or external network management systems, create models and templates in bulk using a structured Excel file, or import models and templates exported as JSON from another ServiceNow instance for cross-instance migration.

## Available paths for importing models and templates

Import models via Excel: Imports models in bulk using a structured Excel file. Supports physical hardware model types: Equipment Model, Equipment Holder Model, Card Model, Facility model and Interface Model. To learn more see [Import models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/import-inventory.md)

Import templates via Excel: Imports inventory templates in bulk using a structured Excel file. To learn more see: [Import template Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/import-template-excel.md)

Import models and templates via JSON: Imports both models and templates together in a single operation. Primarily used for migrating models and templates from one instance to another, from a JSON file produced by exporting from another ServiceNow instance, while preserving system ID continuity, for example, promoting validated content by exporting it from development and importing it to production. Images aren't supported. To learn more see [Import template Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/import-template-excel.md)

During an import, If a model, relationship, or template already exists in the system, the import does not create a duplicate. Existing records are updated depending on whether the imported data contains changes. The Import Results summary provides a breakdown of inserted, updated, skipped, ignored, and failed records so you can verify the outcome of each import.

If you're looking to export models and templates from one ServiceNow instance and import them into another, see [Exporting hierarchy of models and templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/exporting-hierarchy-of-templates-and-models.md)

**Related topics**  


[Import a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/import-models.md)

[Import templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/import-templates.md)

[Import models and templates in JSON format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/import-models-templates-json.md)

