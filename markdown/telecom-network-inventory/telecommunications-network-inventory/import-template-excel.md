---
title: Import template excel
description: Learn about the fields and structure of the Excel template used to define inventory template hierarchies and their relationships for bulk import.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Import template excel

Learn about the fields and structure of the Excel template used to define inventory template hierarchies and their relationships for bulk import.

## Import excel template Overview

The import template is a structured Excel file used to define the hierarchical relationships for bulk import into the application.

The import template is a structured Excel file used to define inventory template hierarchies and their parent-child relationships for bulk import into the application. Each row in the template represents a component of the template hierarchy, linked to its corresponding inventory model and parent template. Entity ID uniquely identifies each row and acts as a key within the spreadsheet. Parent entity ID references these keys to establish the parent-child relationships between template components. Name provides the display name of the template, and Inventory model display name links each template row to its corresponding inventory model in the application. The inventory model must already exist in the system before the template is imported. Name pattern controls how instantiated records are automatically named, and Default Field Values associates a default template containing pre-defined attribute values for the component. These values are applied to every inventory record instantiated from the template. The Excel template is created based on the Import template \[sn\_ni\_adv\_import\_template\_template\] table. An admin can customize the template and update it as required. To download the template with sample data, select Create Excel template on the Import template request form.

The excel template is created based on the Import model template \[sn\_ni\_adv\_import\_model\_template\] table. An admin can customize the template and update it as required.

|Field|Description|
|-----|-----------|
|Entity ID|Unique identifier for each row in the template. Used to establish parent-child relationships between template components using the Parent entity ID field.|
|Name|Display name of the inventory template component.|
|Inventory model display name|Links the template row to its corresponding inventory model in the application. The inventory model must already exist before the template is imported.|
|Relationship|Defines how the template component relates to its parent template in the hierarchy.|
|Parent entity ID|The Entity ID of the parent template component. Establishes the hierarchical position of this template within the overall template structure.|
|Name pattern|Controls how the application automatically generates names for instantiated records created from this template.|
|Default Field|Associates a default template containing pre-defined attribute values for the component. These values are applied to every inventory record|
|Values|instantiated from this template.|
|Version|Captures the version details of the template.|

**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

**Related topics**  


[Import templates](../task/import-templates.md)

