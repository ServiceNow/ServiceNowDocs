---
title: Naming patterns in inventory templates
description: A naming pattern is a JavaScript expression that defines how a configuration item \(CI\) is named when it is created from an inventory template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/naming-patterns-in-inventory-templates.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 3
breadcrumb: [Network inventory templates, Modeling your workflow, Explore, Telecommunications Network Inventory]
---

# Naming patterns in inventory templates

A naming pattern is a JavaScript expression that defines how a configuration item \(CI\) is named when it is created from an inventory template.

The Naming Patterns feature generates vendor-compliant names for network interfaces and slots within inventory templates.The Naming Patterns feature generates vendor-compliant names for network interfaces and slots within inventory templates. Telecom operators can define naming conventions that align with vendor-specific formats, ensuring consistency across the network inventory. Accurate names for physical and logical network resources are essential for operational workflows such as alarm correlation, fault management, and device configuration.

## Where naming patterns apply

A naming pattern can be defined in two places:

-   **On an equipment model.** A model carries default naming patterns for the slots and interfaces it contains. The model pattern acts as the default for every template that is created based on that model.

-   **On a related template within an inventory template.** Each related template — a slot, sub-slot, or interface — carries its own naming pattern. The pattern on a related template starts as a copy of the model's default and can be edited to override the default on a per-template basis.


A related template that does not define a naming pattern, such as a card or module template, falls back to the inventory model name at instantiation. In the Inventory Template Overview tab, this fallback name appears as the tree node label so that you see the same name that the CI will carry once it is created.

## What a naming pattern looks like

A naming pattern is a JavaScript expression that returns a string. The expression can reference variables that the system resolves at evaluation time, combine literal text with those variables, apply string methods, and use conditional logic.

A simple pattern concatenates a literal and a variable:

```
"Slot -"+position
```

For a related template at position 1, this pattern resolves to `Slot -1`.

A more complex pattern can use string methods and a ternary conditional:

```
parent_slot_name.replace("Slot-","Slot/").replace("Slot/","Ge")+" (\" + (position <2 ? \"Tx\" : \"Rx\") + \")\"
```

For an interface at position 1 whose parent slot is named `Slot-6/1`, this pattern resolves to `Ge6/1 (Tx)`.

Variables that the pattern references are read from the related template's context. Variables that cannot be resolved at design time — for example, a top-level slot has no parent slot and therefore no `parent_slot_name` — are substituted with `?` in the Inventory Template Overview tree so that you can identify the gap before the template is used to create CIs.

## Naming patterns are evaluation

Naming patterns are evaluated at two distinct times:

-   At template definition time, when you open the Inventory Template Overview tab on an inventory template. The Overview evaluates every pattern in the template's hierarchy and displays the resolved name as each tree node's label. No CIs are created at template definition time. — the Overview tab provides you the preview.

-   When an inventory template is used to create CIs in the CMDB, the names that were resolved at design time are applied to the new CIs. If a naming pattern changes after CIs exist, an agent must manually update the name on both the CI record and the template.


The Inventory Template Overview tab lets you verify naming end-to-end at design time so that names are correct before any CIs are created. Without this verification, errors in patterns surface only after CIs exist in the CMDB.

**Related topics**  


[Models and templates name definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/how-models-and-templates-define-names.md)

[How inventory template names are generated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/how-inventory-template-names-are-generated.md)

[The Inventory Template Overview tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-template-overview-tab.md)

[Naming pattern validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-pattern-validation.md)

