---
title: How inventory template names are generated
description: When you instantiate an inventory template, each related template in the hierarchy produces a configuration item \(CI\). The CI's name comes from one of two sources, depending on whether the related template defines a naming pattern.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/how-inventory-template-names-are-generated.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Naming patterns in inventory templates, Network inventory templates, Modeling your workflow, Explore, Telecommunications Network Inventory]
---

# How inventory template names are generated

When you instantiate an inventory template, each related template in the hierarchy produces a configuration item \(CI\). The CI's name comes from one of two sources, depending on whether the related template defines a naming pattern.

## Two sources for a CI name

How a related template's CI gets its name depends on the related template's type:

-   **Slot, sub-slot, and interface related templates** have a Name Pattern field, and the pattern is mandatory. A non-empty naming pattern is required to create the related template; you cannot save a slot, sub-slot, or interface related template without a valid pattern that resolves to a non-empty string. At instantiation, the pattern is evaluated as a JavaScript expression and the resulting string becomes the CI name.

-   **Card and module related templates** do not have a Name Pattern field. At instantiation, the CI name is built from the site that the equipment belongs to and the inventory model name, in the form `<site name>/<model name>`.


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

For an interface at position 1 whose parent slot is named `Slot-6/1`, this composed pattern:

```
parent_slot_name.replace("Slot-","Slot/").replace("Slot/","Ge")+" (" + (position <2 ? "Tx" : "Rx") + ")"
```

resolves to `Ge6/1 (Tx)`.

**Related topics**  


[Naming patterns in inventory templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-patterns-in-inventory-templates.md)

[Models and templates name definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/how-models-and-templates-define-names.md)

[Naming pattern validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/naming-pattern-validation.md)

