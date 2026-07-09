---
title: Name pattern validation
description: Name pattern validation runs twice: at save time to prevent errors, and when the Overview tab loads the hierarchy to catch issues specific to template relationships.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/telecom-network-inventory/telecommunications-network-inventory/naming-pattern-validation.html
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-07-09"
reading_time_minutes: 3
breadcrumb: [Inventory template naming patterns, Network inventory models, Model your workflow, Explore, Telecommunications Network Inventory]
---

# Name pattern validation

Name pattern validation runs twice: at save time to prevent errors, and when the Overview tab loads the hierarchy to catch issues specific to template relationships.

-   **Save-time validation**

    Evaluates whether the pattern is a valid expression that produces a non-empty string.

-   **Hierarchy render validation**

    Evaluates cross-template rules registered as validation providers — for example, duplicate names among siblings.


## Save-time validation

When you create or edit a pattern in the **Define name pattern** modal, the modal validates the pattern before letting you apply it. Two outcomes are visible in the modal:

-   Pattern accepted: A green message appears beneath the input: `Valid name pattern. Preview: <resolved name>`. The resolved name in the preview is a sample evaluation. The **Apply** button is enabled.
-   Pattern invalid or produces an empty result: A red message appears: `Name pattern results in empty name. Please try again.` The **Apply** action is blocked. The same message appears if the pattern has invalid JavaScript, references a variable that does not exist, or produces an empty string when evaluated.

The pattern is committed to the record only when you select **Apply** on a valid pattern and then save the underlying record. If you close the modal or close the record without saving, the pattern is not persisted.

## Hierarchy render validation

When the **Inventory Template Overview** tab evaluates the hierarchy, registered validation providers run against the resolved names of related templates. Each provider evaluates siblings under a single parent at one tree level at a time and records validation results for any related template that fails its rule.

The application includes a default duplicate-name check that flags two or more siblings whose patterns resolve to the same name. For example, if two slots at the same level both resolve to `Slot -5`, both slots are flagged. The check is scoped to direct siblings of the same parent and does not compare names across different branches.

You can extend or replace this default check by registering additional validation providers. For more information, see [Extension point for custom naming validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/extension-point-custom-naming-validation.md).

## Multiple validation rules

When multiple validation rules flag the same related template, the Overview tab combines their outputs:

-   The **Validation failed** banner concatenates the error descriptions from all providers that flagged the related template, separated by `;` \(semicolon and space\). All errors are visible in one banner.
-   The **Error** badge on the tree shows only one label. When multiple providers each write a badge label, the badge displayed on the node is set by the last provider to flag the related template.

The following banner shows output when a related template fails both a custom check and the default duplicate-name check.

```
Validation failed: Slot name exceeds maximum length: Slot -4; Duplicate name at same level: Slot -4
```

## Unresolvable variables in resolved names

Patterns can reference variables that have no value in a particular related template's context. For example, a top-level slot directly under an equipment template has no parent slot, so the variable `parent_slot_name` cannot be resolved for it.

When the **Inventory Template Overview** encounters an unresolvable variable, it substitutes `?` for the variable in the resolved name on the tree node label. The `?` substitution is a signal that the pattern is using variables that do not fit the related template's position in the hierarchy.

**Note:** The `?` substitution does not raise an **Error** badge or a **Validation failed** banner. It is a display-only indicator in the tree node label.

**Related topics**  


[Inventory Template Overview tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/inventory-template-overview-tab.md)

[Extension point for custom naming validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/extension-point-custom-naming-validation.md)

[Inventory template naming patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/naming-patterns-in-inventory-templates.md)

