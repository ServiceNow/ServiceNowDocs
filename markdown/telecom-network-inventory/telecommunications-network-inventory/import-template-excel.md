---
title: Import template Excel
description: Learn about the fields and structure of the Excel template used to define inventory template hierarchies and their relationships for bulk import.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/import-template-excel.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Import template Excel

Learn about the fields and structure of the Excel template used to define inventory template hierarchies and their relationships for bulk import.

## Overview of Excel template

The import template is a structured Excel file used to define the hierarchical relationships for bulk import into the application.

The import template is a structured Excel file used to define inventory template hierarchies and their parent-child relationships for bulk import into the application. The import template is a structured Excel file. It defines inventory template hierarchies and their parent-child relationships for bulk import into the application. Each row represents a component of the template hierarchy. Components link to their corresponding inventory model and parent template. The Excel template is created based on the Import template table \[sn\_ni\_adv\_import\_template\_template\]. An admin can customize and update the template as required. To download the template with sample data, select **Create Excel template** on the Import template request form.

The Excel template is created based on the Import model template table \[sn\_ni\_adv\_import\_model\_template\]. An administrator can customize and update the template as required.

|Field|Description|
|-----|-----------|
|Entity ID|Unique identifier for each row in the template. This field is used to establish parent-child relationships between template components using the Parent entity ID field.|
|Name|Display name of the inventory template component.|
|Inventory model display name|Name that links the template row to its corresponding inventory model in the application. The inventory model must already exist before the template is imported.|
|Relationship|Relationship between the template component and its parent template in the hierarchy.|
|Parent entity ID|The Entity ID of the parent template component. The ID establishes the hierarchical position of this template within the overall template structure.|
|Name pattern|Pattern that controls how the application automatically generates names for instantiated records created from this template.|
|Default Field|Default field that associates a default template containing pre-defined attribute values for the component. These values are applied to every inventory record|
|Values|Values that are instantiated from this template.|
|Version|Version details of the template.|

**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[Import templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/import-templates.md)

