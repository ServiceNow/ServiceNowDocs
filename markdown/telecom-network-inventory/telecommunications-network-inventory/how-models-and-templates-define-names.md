---
title: Model and template naming
description: The equipment model establishes default naming patterns for CIs \(configuration items\). Inventory templates inherit those patterns and can override them per related template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/how-models-and-templates-define-names.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 2
breadcrumb: [Inventory template naming patterns, Reference, Telecommunications Network Inventory]
---

# Model and template naming

The equipment model establishes default naming patterns for CIs \(configuration items\). Inventory templates inherit those patterns and can override them per related template.

## Equipment models and inventory templates

An equipment model defines a class of equipment, capturing structural facts like slot count, card types, and naming patterns for slots and interfaces.

An inventory template represents a way to configure equipment for your environment, selecting card models for slots, defining sub-component templates, and carrying naming patterns for CIs.

One model supports multiple templates. For example, the Cisco ASR 9006 model is the basis for both the Edge Template and the Router Template — two configurations serving different network roles.

## Inheriting naming patterns from models

When you create an inventory template, the system generates related templates matching the model's structure automatically. Name Pattern fields are pre-populated with the corresponding model defaults — slot and interface related templates inherit the model's naming patterns.

After creation, each related template owns its naming pattern independently. Changing the pattern on one related template has no effect on its siblings or on the model. To restore a related template's pattern to the model's default, you must edit the field manually.

## Customizing individual template patterns

After you create related templates, each template owns its own Name Pattern field. You can edit any template's pattern independently without affecting others. This lets you customize naming conventions for exceptions—for example, when a slot requires non-standard naming to integrate with an external tool.

When you override a Name Pattern in a related template, the **Inventory Template Overview** tab displays the resolved name for each template as a tree node label. Inconsistencies appear together. For example, ten slots following the standard pattern produce `Slot -1`, `Slot -2`, and so on, while an eleventh slot edited manually shows `Slot-11`. Review these differences to identify naming problems before the template creates CIs.

## Roles and permissions

The role required to edit naming patterns differs by layer:

-   The Inventory Catalog Manager role edits naming patterns at the equipment model level and establishes the organization's naming convention.
-   The Inventory Template Manager role creates and updates inventory templates, including editing the inherited naming patterns on related templates.

Users who create CIs from existing templates do not write or edit naming patterns — they use the names the patterns produce.

## Benefits of the two-layer model

Separating model and template responsibilities lets you:

-   Define an organization-wide naming convention once, at the model level, so every template based on that model starts with the same defaults.
-   Adjust individual templates only where exceptions are necessary, without affecting any other templates that share the same model.

**Parent Topic:**[Inventory template naming patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-patterns-in-inventory-templates.md)

**Related topics**  


[Inventory template naming patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-patterns-in-inventory-templates.md)

[Inventory template name generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/how-inventory-template-names-are-generated.md)

[Inventory template hierarchy view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-template-overview-tab.md)

