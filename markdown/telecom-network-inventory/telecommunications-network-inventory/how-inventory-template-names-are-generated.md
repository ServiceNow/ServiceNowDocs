---
title: Inventory template name generation
description: When you instantiate an inventory template, each related template in the hierarchy produces a CI \(configuration item\). The CI's name comes from one of two sources, depending on whether the related template defines a naming pattern.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/how-inventory-template-names-are-generated.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 1
breadcrumb: [Inventory template naming patterns, Reference, Telecommunications Network Inventory]
---

# Inventory template name generation

When you instantiate an inventory template, each related template in the hierarchy produces a CI \(configuration item\). The CI's name comes from one of two sources, depending on whether the related template defines a naming pattern.

## Two sources for a CI name

How a related template's CI gets its name depends on the related template's type:

-   Slot, sub-slot, and interface related templates all require a **Name Pattern** field. The pattern must resolve to a non-empty string; you cannot save the template without a valid pattern. When the template creates a CI, the system evaluates the pattern as a JavaScript expression. The resulting string is set to the CI name.
-   Card and module related templates do not include a **Name Pattern** field. When the template creates a CI, the system automatically builds the CI name from two values: the site name and the inventory model name. The name follows this format: `<site name>/<model name>`.

## How a Name Pattern resolves to a name

A naming pattern is a JavaScript expression that returns a string. Three syntactic forms cover the patterns used in inventory templates:

-   **A literal concatenated with a variable**

    ```
    "Slot -"+position
    ```

-   **A variable transformed with string methods**

    ```
    parent_slot_name.replace("Slot-","Slot/").replace("Slot/","Ge")
    ```

-   **A ternary expression used to choose between alternatives**

    ```
    position <2 ? "Tx" : "Rx"
    ```


These forms can be combined into longer patterns. When a related template is evaluated, the system reads the variables from the related template's context, executes the expression, and uses the resulting string as the CI name.

For an interface at position 1 whose parent slot is named `Slot-6/1`, the following composed pattern resolves to `Ge6/1 (Tx)`.

```
parent_slot_name.replace("Slot-","Slot/").replace("Slot/","Ge")+" (" + (position <2 ? "Tx" : "Rx") + ")"
```

**Parent Topic:**[Inventory template naming patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-patterns-in-inventory-templates.md)

**Related topics**  


[Inventory template naming patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-patterns-in-inventory-templates.md)

[Model and template naming](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/how-models-and-templates-define-names.md)

[Name pattern validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-pattern-validation.md)

