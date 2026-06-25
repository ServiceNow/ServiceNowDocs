---
title: Import models and templates
description: Use the import feature to bring equipment models and templates into the system in bulk. You can import using Excel or JSON, and migrate components across instances while preserving system IDs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/network-inventory-import-model.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 2
breadcrumb: [Explore, Telecommunications Network Inventory]
---

# Import models and templates

Use the import feature to bring equipment models and templates into the system in bulk. You can import using Excel or JSON, and migrate components across instances while preserving system IDs.

## Import Overview

Equipment models and templates must exist in the system before you can define model relationships or instantiate network inventory records. The import feature lets you:

-   Bring in existing model data from manufacturer datasheets or external network management systems.
-   Create models and templates in bulk using a structured Excel file.
-   Import models and templates exported as JSON from anotheServiceNowr instance for cross-instance migration.

## Available paths for importing models and templates

You can import the following types of models and templates in different ways.

-   **Import models via Excel**

    Imports models in bulk using a structured Excel file. You can import the following physical hardware model types:

    -   Equipment Model
    -   Equipment Holder Model
    -   Card Model
    -   Facility model
    -   Interface Model
    To learn more, see [Import models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/import-inventory.md)

-   **Import templates via Excel**

    Imports inventory templates in bulk using a structured Excel file. To learn more, see [Import template Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/import-template-excel.md)

-   **Import models and templates via JSON**

    Imports both models and templates together in a single operation. This is primarily used for migrating models and templates from one instance to another. For example, from a JSON file produced by exporting from another ServiceNow instance. System ID continuity is preserved, such as by promoting validated content by exporting it from development and importing it to production. Images are not supported. To learn more see [Importing models and templates in JSON format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)


During an import, if a model, relationship, or template already exists in the system, the import does not create a duplicate. Existing records are updated depending on whether the imported data contains changes. The Import Results summary provides a breakdown of inserted, updated, skipped, ignored, and failed records so you can verify the outcome of each import.

If you're looking to export models and templates from one ServiceNow instance and import them into another, see [Exporting hierarchy of models and templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

**Related topics**  


[Import a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/import-models.md)

[Import templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/import-templates.md)

[Import models and templates in JSON format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/import-models-templates-json.md)

