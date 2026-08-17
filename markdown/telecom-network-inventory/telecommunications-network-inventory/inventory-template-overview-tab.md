---
title: Inventory template hierarchy view
description: The Overview tab on an inventory template record shows the full template hierarchy as a tree. Use it to check resolved CI names and spot validation errors before deploying the template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/inventory-template-overview-tab.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Inventory template naming patterns, Reference, Telecommunications Network Inventory]
---

# Inventory template hierarchy view

The Overview tab on an inventory template record shows the full template hierarchy as a tree. Use it to check resolved CI names and spot validation errors before deploying the template.

## Inventory template tabs

The Overview tab opens by default when you open an inventory template record. It is the first of three tabs:

-   **__Overview__**

    The tree-based hierarchy view.

-   **__Details__**

    The inventory template's own header fields: Name, Inventory model, Default field values, and Version.

-   **__Related Templates__**

    The flat list of child related templates, with editable fields including **Name Pattern**.


The Overview tab is available in both the SOW workspace and the Network Inventory workspace.

## Overview tab components

The Overview tab is split into two regions:

-   The tree renders the inventory template at the root, with all related templates beneath it as expandable child nodes. Each node label is the resolved name that the related template displays when the related template is applied.
-   The detail pane shows the attributes of the selected tree node: **Name**, **Parent**, **Inventory model**, **Relationship type**, **Default field values**, and **Name Pattern** where one is defined.

The detail pane is read-only. To edit any of the fields shown, open the related template record by selecting **View details**.

## Hierarchy tree behavior

The tree displays the full structure of the inventory template. Related templates that contain child templates are rendered as expandable nodes. Selecting the chevron beside a node reveals its children, which may also be expandable.

The hierarchy can extend several levels deep. For example, a chassis device template may have five levels of nesting: slots, card templates, sub-slots, interface card templates, and ports.

For performance, the tree loads only the first eight children of each expanded node. When a parent has more than eight children, the tree displays a **Show More** link beneath the visible children to load additional nodes.

## Validation error indicators

When the Overview evaluates the hierarchy, registered validation providers run against the resolved names. Any related template that fails validation displays a red **Error** badge on its tree node. Selecting an affected node also shows a red **Validation failed** banner in the detail pane that describes the specific error.

For full details on validation behavior, see [Name pattern validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-pattern-validation.md).

**Parent Topic:**[Inventory template naming patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-patterns-in-inventory-templates.md)

**Related topics**  


[Inventory template naming patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-patterns-in-inventory-templates.md)

[Name pattern validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-pattern-validation.md)

[CI name generation for inventory templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/how-inventory-template-names-are-generated.md)

