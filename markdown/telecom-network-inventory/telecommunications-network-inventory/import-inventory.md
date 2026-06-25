---
title: Import models
description: Learn how to bulk-import models and their hierarchical relationships into Telecommunications Network Inventory by uploading a structured Excel file. The import handles core hardware model types and auto-generates a first-level set of inventory templates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/import-inventory.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 2
breadcrumb: [Import models and templates, Explore, Telecommunications Network Inventory]
---

# Import models

Learn how to bulk-import models and their hierarchical relationships into Telecommunications Network Inventory by uploading a structured Excel file. The import handles core hardware model types and auto-generates a first-level set of inventory templates.

## Importing models overview

You can import equipment models and their hierarchical relationships in bulk by uploading a structured Excel file. The Excel import supports these core physical hardware model types:

-   Equipment Model
-   Equipment Holder Model
-   Card Model
-   Facility model
-   Interface Model

.

## Importing models process

On import model request submission, the system processes each row in the Excel file and creates the following records in a single operation:

-   equipment models
-   equipment holder models
-   card models
-   network interface models

The models are based on the model class and model category specified in each row. Model relationships between these models are based on the relationship type, parent entity ID, and root entity ID values in the spreadsheet. Model relationships are created only for the rows where the relationship type, parent entity ID, and root entity ID are defined in the Excel file.

-   -   
You must manually create any model relationships not defined in the spreadsheet. To learn more, see [Modeling network inventory relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-modeling-process.md). If a model already exists in the system, the record is matched and updated to prevent duplicates.

During the import, the Integration Commons for CMDB plugin runs in the background. Normalization rules are applied to manufacturer and company names to keep your data clean and standardized. The normalization rules are applied only if the Normalization Data Service Client is installed. To learn more, see [Normalization data services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_NormalizationOverview.md).

The import also auto-generates a first-level set of inventory templates for every equipment and card model created. Related templates are auto generated under the parent equipment template based on the defined model relationships and the count values from the spreadsheet. The auto-generated templates provide a flat, first-level set of templates that can be enriched using the import template feature. To learn the step-by-step process of importing models, see [Import a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/import-models.md).

A detailed Import Results summary is produced. The summary shows total records processed, broken down into inserted, updated, skipped, ignored, and failed records.

**Related topics**  


[Importing models and templates in JSON format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Exporting hierarchy of models and templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

