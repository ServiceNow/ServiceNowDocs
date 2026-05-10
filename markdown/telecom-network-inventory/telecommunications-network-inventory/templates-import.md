---
title: Import templates
description: Learn how to import inventory templates in bulk to define a complete template hierarchy with specific slot-to-card assignments, name patterns, and default field values in the Telecommunications Network Inventory
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Import, Explore, Telecommunications Network Inventory]
---

# Import templates

Learn how to import inventory templates in bulk to define a complete template hierarchy with specific slot-to-card assignments, name patterns, and default field values in the Telecommunications Network Inventory

## Importing templates overview

An inventory template defines the attribute values, business rules, and relationships for a network asset. Building inventory templates manually requires following a specific sequence starting with a default template, then creating equipment, card, interface, and slot templates in the correct order to establish proper relationships. Since this can be time-intensive, the import template feature lets you bring multiple inventory templates into the application at once using a structured Excel file.

## Importing templates process

The template import is designed for when you want to define a complete template hierarchy with specific slot-to-card assignments, name patterns, and default field values. The import template request is initiated by uploading an Excel file where each row represents a component of the template hierarchy, linked to its corresponding inventory model and parent template.

When the template import runs, it does not duplicate the existing auto-generated templates from the model import. Instead, it creates a new parent template with enriched data such as default field values, updates existing slot templates with name patterns and default values, and inserts the slot-to-card template relationships that were missing from the model import auto-generation. Related templates such as slot templates for rack, equipment, or card templates are automatically generated during the import, provided the corresponding model relationships are already defined. If model relationships are not defined, the system does not create the associated templates.

![The image displays the import templates workflow](../image/import-template-flow.png)

A detailed Import Results summary is produced, showing total records processed and breaking them down into inserted, updated, skipped, ignored, and failed records. To learn the step-by-step process of importing templates, see [Import templates](../task/import-templates.md)

**Related topics**  


[Import models and templates in JSON format](../task/import-models-templates-json.md)

[Export hierarchy of models and templates](../task/export-hierarchy-of-models-and-template.md)

