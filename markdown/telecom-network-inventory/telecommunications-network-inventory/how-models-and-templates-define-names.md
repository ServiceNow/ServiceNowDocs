---
title: Models and templates name definition
description: Two layers shape how a configuration item \(CI\) is named when it is created in TNI inventory: the equipment model establishes default naming patterns, and the inventory template inherits and optionally overrides them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/how-models-and-templates-define-names.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 4
breadcrumb: [Naming patterns in inventory templates, Network inventory templates, Modeling your workflow, Explore, Telecommunications Network Inventory]
---

# Models and templates name definition

Two layers shape how a configuration item \(CI\) is named when it is created in TNI inventory: the equipment model establishes default naming patterns, and the inventory template inherits and optionally overrides them.

## The two layers

An equipment model represents a class of equipment — for example, a Cisco ASR 9006 router. The model captures the structural facts that apply to every device of that type: how many slots it has, what kinds of cards each slot accepts, and the default naming patterns that names of slots and interfaces should follow.

An inventory template represents a specific way of configuring that equipment for use in your environment. The template selects which card models occupy which slot positions, defines the related templates for sub-components, and carries naming patterns that apply when CIs are created from the template.

You can build more than one template from the same model. The same Cisco ASR 9006 model is the basis for the ASR9006 Edge Template and the ASR 9006 - Router Template — two configurations of the same physical equipment serving different roles in a network.

## How a template inherits naming patterns from its model

When you create inventory template based on an equipment model, the system auto-creates the related templates that match the model's structure. Each related template's Name Pattern field is pre-populated with the corresponding default from the model — slot related templates inherit the model's slot naming pattern, interface related templates inherit the interface naming pattern.

After creation, each related template owns its naming pattern independently. Changing the pattern on one related template has no effect on its siblings or on the model. To restore a related template's pattern to the model's default, you must edit the field manually.

## How overrides behave

Because each related template owns its own pattern after creation, you can edit any single related template's pattern without affecting the rest. This flexibility lets you handle exceptions — for example, a slot that needs a non-standard naming format for integration with an external tool.

Overrides are visible to anyone reading the Inventory Template Overview tab, where the resolved name produced by each related template's current pattern appears as the tree node label. Inconsistencies — for example, ten slots producing names like `Slot -1`, `Slot -2` and an eleventh slot producing `Slot-11` because of a manual edit — appear side by side in the tree, making them easy to spot before the template is used to create CIs.

## Who works at each layer

The role with permission to edit naming patterns at the model level differs from the role used to edit naming patterns at the template level:

-   The **Inventory Catalog Manager** role edits naming patterns at the equipment model level. Users with this role establish the organization's naming convention.

-   The **Inventory Template Manager** role creates and updates inventory templates, including editing the inherited naming patterns on related templates within those templates.


End users who create CIs from existing templates don't write or edit naming patterns — they consume the names that the patterns produce.

## What this two-layer model achieves

Separating model and template responsibilities lets you do two things in sequence rather than at once:

-   Define an organization-wide naming convention once, at the model level, so every template based on that model starts with the same defaults.

-   Adjust individual templates only where exceptions are necessary, without affecting any other templates that share the same model.


The Inventory Template Overview tab supports both activities by showing the resolved names produced by current patterns across the entire hierarchy, so you can verify a template's naming end-to-end before any CIs are created.

## Open items — confirm before publishing

-   Whether updates to model patterns propagate to existing templates after creation — not discussed in source material.

-   What model categories besides equipment models carry naming pattern fields — source material tentatively states "equipment models" only, no other category confirmed.

-   What happens when a template is created from scratch with no model — not discussed.

-   Specific UI for editing model patterns — not visually demonstrated in demo.

-   Whether the Define name pattern modal opens from the model record — stated verbally but not verified on demo instance.


**Related topics**  


[Naming patterns in inventory templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-patterns-in-inventory-templates.md)

[How inventory template names are generated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/how-inventory-template-names-are-generated.md)

[The Inventory Template Overview tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-template-overview-tab.md)

