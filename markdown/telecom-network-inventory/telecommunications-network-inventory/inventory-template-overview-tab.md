---
title: The Inventory Template Overview tab
description: The Inventory Template Overview tab is a design-time verification surface on inventory template records. It shows the full template hierarchy as a tree with each related template's resolved name as the node label, and runs validation against the resolved hierarchy. No configuration items \(CIs\) are created from the actions you take in this view.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/inventory-template-overview-tab.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 2
breadcrumb: [Naming patterns in inventory templates, Network inventory templates, Modeling your workflow, Explore, Telecommunications Network Inventory]
---

# The Inventory Template Overview tab

The Inventory Template Overview tab is a design-time verification surface on inventory template records. It shows the full template hierarchy as a tree with each related template's resolved name as the node label, and runs validation against the resolved hierarchy. No configuration items \(CIs\) are created from the actions you take in this view.

## Where the Overview tab fits

The Overview tab opens by default when you open an inventory template record. It is the first of three tabs:

-   **Overview** — the tree-based hierarchy view described in this topic.

-   **Details** — the inventory template's own header fields \(Name, Inventory model, Default field values, Version\).

-   **Related Templates** — the flat list of child related templates, with editable fields including Name Pattern.


The Overview tab is available in both the SOW workspace and the Network Inventory workspace.

## The two parts of the Overview

The Overview tab is split into two regions:

-   **The tree on the left** renders the inventory template at the root, with all related templates beneath it as expandable child nodes. Each node's label is the resolved name that the related template will produce when the template is instantiated.

-   **The detail pane on the right** shows the attributes of whichever tree node is currently selected — Name, Parent, Inventory model, Relationship type, Default field values, and Name Pattern where one is defined.


The detail pane is read-only. To edit any of the fields shown, use the View details button described in the task topic for defining a naming pattern.

## How the tree represents the hierarchy

The tree traverses the inventory template's full composition graph. Each related template that itself has related templates is rendered as an expandable node — selecting the chevron beside the node reveals its children, which may in turn be expandable.

The hierarchy can extend several levels deep. For example, the ASR9006 Edge Template expands to slots at the first level, which expand to card templates at the second level, which expand to sub-slots, which expand further to interface card templates, which expand to ports — five levels of nesting under the equipment root.

For performance, the tree loads only the first eight children of each expanded node. When a parent has more than eight children, the tree displays a **Show More** link beneath the visible children to load additional nodes.

## Where validation results appear

When the Overview evaluates the hierarchy, registered validation providers run against the resolved names. Any related template that fails validation displays a red **Error** badge on the right side of its tree node. Selecting an affected node also shows a red **Validation failed** banner beneath the detail pane that describes the specific error.

For full details on validation behavior, see [Naming pattern validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-pattern-validation.md).

**Related topics**  


[Naming patterns in inventory templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-patterns-in-inventory-templates.md)

[Naming pattern validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-pattern-validation.md)

[How inventory template names are generated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/how-inventory-template-names-are-generated.md)

