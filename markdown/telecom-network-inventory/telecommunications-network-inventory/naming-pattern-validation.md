---
title: Naming pattern validation
description: The TNI Naming Application validates naming patterns at two distinct moments — once when you save a pattern, and again when the Inventory Template Overview tab renders the resolved hierarchy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/naming-pattern-validation.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 3
breadcrumb: [Naming patterns in inventory templates, Network inventory templates, Modeling your workflow, Explore, Telecommunications Network Inventory]
---

# Naming pattern validation

The TNI Naming Application validates naming patterns at two distinct moments — once when you save a pattern, and again when the Inventory Template Overview tab renders the resolved hierarchy.

## Two validation moments

The two moments are independent. A pattern that passes save-time validation can still produce results that fail Overview-render validation, because Overview-render checks compare patterns across multiple related templates, while save-time checks evaluate one pattern at a time.

## Save-time validation

When you author or edit a pattern in the Define name pattern modal, the modal validates the pattern before letting you apply it. Two outcomes are visible in the modal:

-   **Pattern accepted.** A green message appears beneath the input: `Valid name pattern. Preview: <resolved name>`. The resolved name in the preview is a sample evaluation. The **Apply** button is enabled.

-   **Pattern invalid or produces an empty result.** A red message appears: `Name pattern results in empty name. Please try again.` The **Apply** action is blocked. The same message appears whether the pattern has invalid JavaScript, references a variable that doesn't exist, or produces an empty string when evaluated.


The pattern is committed to the record only when you click **Apply** on a valid pattern and then save the underlying record. If you close the modal or close the record without saving, the pattern is not persisted.

## Overview-render validation

When the Inventory Template Overview tab evaluates the hierarchy, registered validation providers run against the resolved names of related templates. Each provider examines the related templates at one tree level at a time — the siblings under a single parent — and writes validation results back to any related template that fails its rule.

A single validation provider ships with the application by default: a duplicate-name check that flags two or more siblings whose patterns resolve to the same name. For example, if two slots at the same level both resolve to `Slot -5`, both slots are flagged. The check is scoped to direct siblings of the same parent — it does not compare a slot's name against a sub-slot's name in a different branch.

Customer administrators can extend, augment, or replace this default check by registering additional validation providers. For more information, see [Extension point for custom naming validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/extension-point-custom-naming-validation.md).

## How multiple validation rules combine

When multiple validation rules flag the same related template, the Overview tab combines their outputs:

-   The **Validation failed** banner concatenates the error descriptions from all providers that flagged the related template, separated by `;` \(semicolon and space\). All errors are visible in one banner.

-   The **Error** badge on the tree shows only one label. When multiple providers each write a badge label, the badge displayed on the node is set by the last provider to flag the related template.


Example: a related template that fails both a custom check and the default duplicate-name check shows this banner:

```
Validation failed: This is a slot fake error: Slot -4; Duplicate name at same level: Slot -4
```

## Unresolvable variables in resolved names

Patterns can reference variables that have no value in a particular related template's context. For example, a top-level slot directly under an equipment template has no parent slot, so the variable `parent_slot_name` cannot be resolved for it.

When the Inventory Template Overview encounters an unresolvable variable, it substitutes `?` for the variable in the resolved name on the tree node label. The `?` substitution is a signal that the pattern is using variables that do not fit the related template's position in the hierarchy.

**Note:** The `?` substitution does not raise an **Error** badge or a **Validation failed** banner. It is a display-only indicator in the tree node label.

**Related topics**  


[The Inventory Template Overview tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-template-overview-tab.md)

[Extension point for custom naming validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/extension-point-custom-naming-validation.md)

[Naming patterns in inventory templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-patterns-in-inventory-templates.md)

