---
title: Import models
description: Learn how to bulk-import models and their hierarchical relationships into Telecommunications Network Inventory by uploading a structured Excel file. The import handles core hardware model types and auto-generates a first-level set of inventory templates.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [Import, Explore, Telecommunications Network Inventory]
---

# Import models

Learn how to bulk-import models and their hierarchical relationships into Telecommunications Network Inventory by uploading a structured Excel file. The import handles core hardware model types and auto-generates a first-level set of inventory templates.

## Importing models overview

The import model feature lets you import equipment models and their hierarchical relationships in bulk by uploading a structured Excel file. The import via the excel supports core physical hardware model types: Equipment Model, Equipment Holder Model, Card Model, Facility model and Interface Model.

## Importing models process

When you submit an import model request, the system processes each row in the Excel file and creates the following records in a single operation: equipment models, equipment holder models, card models, and network interface models based on the model class and model category specified in each row; and model relationships between these models based on the relationship type, parent entity ID, and root entity ID values in the spreadsheet. Model relationships are created only for the rows where the relationship type, parent entity ID, and root entity ID are defined in the Excel file. Any model relationships not defined in the spreadsheet must be created manually. To learn more, see [Model relationships](inventory-modeling-process.md). If a model already exists in the system, the record is matched and updated so that duplicates are not created.

During the import, the Integration Commons for CMDB plugin runs in the background, and normalization rules are applied to manufacturer and company names to keep your data clean and standardized. The normalization rules are applied only if the Normalization Data Service Client is installed. To learn more, see [Normalization data services](https://www.servicenow.com/docs/access?context=c_NormalizationOverview&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

![The image displays the export model flow](../image/import-model-flow.png)

The import also auto-generates a first-level set of inventory templates for every equipment and card model created. Related templates are auto generated under the parent equipment template based on the defined model relationships and the count values from the spreadsheet. The auto-generated templates provide a flat, first-level set of templates that can be enriched using the import template feature. To learn the step-by-step process of importing models, see [Import a model](../task/import-models.md).

A detailed Import Results summary is produced, showing total records processed and breaking them down into inserted, updated, skipped, ignored, and failed records.

**Related topics**  


[Importing models and templates in JSON format](import-templates-and-models-in-json-format.md)

[Import templates](templates-import-concept.md)

[Exporting hierarchy of models and templates](exporting-hierarchy-of-templates-and-models.md)

