---
title: Inventory template naming patterns
description: A naming pattern is a JavaScript expression that defines how a CI \(configuration item\) is named when it is created from an inventory template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/naming-patterns-in-inventory-templates.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-07-09"
reading_time_minutes: 4
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Inventory template naming patterns

A naming pattern is a JavaScript expression that defines how a CI \(configuration item\) is named when it is created from an inventory template.

The naming patterns feature generates vendor-conforming names for network interfaces and slots within inventory templates. Telecom operators can define naming conventions that align with vendor-specific formats to maintain consistency across the network inventory. Accurate names for physical and logical network resources are essential for operational workflows such as alarm correlation, fault management, and device configuration.

## Where naming patterns apply

A naming pattern can be defined in two places:

-   On an equipment model. A model carries default naming patterns for the slots and interfaces it contains. The model pattern acts as the default for every template created based on that model.
-   On a related template within an inventory template. Each related template — a slot, sub-slot, or interface — carries its own naming pattern. The pattern starts as a copy of the model default and can be edited to override it for each template.

A related template that does not define a naming pattern, such as a card or module template, falls back to the inventory model name at instantiation. In the **Inventory Template Overview** tab, this fallback name appears as the tree node label. The label matches the name the CI carries after it is created.

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

Variables that the pattern references are read from the related template's context. Variables that cannot be resolved at design time are substituted with `?` in the Inventory Template Overview tree. For example, a top-level slot has no `parent_slot_name`. The tree displays `?` so you can identify the gap before using the template to create CIs.

## When naming patterns are evaluated

Naming patterns are evaluated at two distinct times:

-   At template definition time, when you open the Inventory Template Overview tab on an inventory template. The Overview evaluates every pattern in the template's hierarchy and displays the resolved name as each tree node's label. No CIs are created at template definition time. The Overview tab provides a preview.

-   When an inventory template is used to create CIs in the CMDB, the names that were resolved at design time are applied to the new CIs. If a naming pattern changes after CIs exist, an administrator must update the name on both the CI record and the template.


The Inventory Template Overview tab lets you verify naming end to end at design time, before any CIs are created. Without this verification, errors in patterns surface only after CIs exist in the CMDB.

-   **[Model and template naming](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/how-models-and-templates-define-names.md)**  
The equipment model establishes default naming patterns for CIs \(configuration items\). Inventory templates inherit those patterns and can override them per related template.
-   **[Inventory template name generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/how-inventory-template-names-are-generated.md)**  
When you instantiate an inventory template, each related template in the hierarchy produces a CI \(configuration item\). The CI's name comes from one of two sources, depending on whether the related template defines a naming pattern.
-   **[Inventory template hierarchy view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-template-overview-tab.md)**  
The Overview tab on an inventory template record shows the full template hierarchy as a tree. Use it to check resolved CI names and spot validation errors before deploying the template.
-   **[Name pattern validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-pattern-validation.md)**  
Name pattern validation runs twice: at save time to prevent errors, and when the Overview tab loads the hierarchy to catch issues specific to template relationships.
-   **[Extension point for custom name validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/extension-point-custom-naming-validation.md)**  
The custom name validation extension point validates resolved names in the **Inventory Template Overview** tab. Administrators can register custom validation rules to enforce organization-specific naming conventions, replacing or extending the default check.

**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[Model and template naming](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/how-models-and-templates-define-names.md)

[Inventory template name generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/how-inventory-template-names-are-generated.md)

[Inventory template hierarchy view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-template-overview-tab.md)

[Name pattern validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-pattern-validation.md)

