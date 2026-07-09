---
title: Import templates
description: Import inventory templates in bulk to define a complete template hierarchy with specific slot-to-card assignments, name patterns, and default field values in the Telecommunications Network Inventory
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/templates-import.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-07-09"
reading_time_minutes: 1
breadcrumb: [Import models and templates, Explore, Telecommunications Network Inventory]
---

# Import templates

Import inventory templates in bulk to define a complete template hierarchy with specific slot-to-card assignments, name patterns, and default field values in the Telecommunications Network Inventory

## Importing templates overview

Use the import template feature to load multiple inventory templates at once from a structured Excel file.

## Importing templates process

Import template is designed to define the complete template hierarchy with specific slot-to-card assignments, name patterns, and default field values.

The import template request is initiated by uploading an excel file where each row represents a component of the template hierarchy, linked to its corresponding inventory model and parent template.

When the template import runs, it does not duplicate the existing auto-generated templates from the model import. Instead, it creates a new parent template with enriched data such as default field values, updates existing slot templates with name patterns and default values, and inserts the slot-to-card template relationships that were missing from the model import auto-generation. Related templates such as slot templates for rack, equipment, or card templates are automatically generated during the import, provided the corresponding model relationships are already defined. If model relationships aren't defined, the system does not create the associated templates.

A detailed Import Results summary is produced. The summary shows total records processed and breaking them down into inserted, updated, skipped, ignored, and failed records. To learn the step-by-step process of importing templates, see [Import templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/import-templates.md)

**Related topics**  


[Import models and templates in JSON format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/import-models-templates-json.md)

[Export hierarchy of models and templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/export-hierarchy-of-models-and-template.md)

