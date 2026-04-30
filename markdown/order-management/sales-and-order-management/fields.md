---
title: Fields
description: Learn how fields provide the foundational data model for ServiceNow CPQ configurations—what they are, how they relate to blueprints, rules, and layouts, and how to choose the right type and display for reliable, reusable experiences.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 4
breadcrumb: [ServiceNow CPQ Configurator, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Fields

Learn how fields provide the foundational data model for ServiceNow CPQ configurations—what they are, how they relate to blueprints, rules, and layouts, and how to choose the right type and display for reliable, reusable experiences.

Fields are the smallest unit of the ServiceNow CPQ configuration model and represent a single piece of data \(for example, a quantity, a choice, or a note\). They power the user experience \(what the user sees and edits\), the logical model \(what rules read and act on\), and downstream outputs \(what is written to the bill of materials or passed to external systems\). Because fields are global in an environment, the same field can be reused across blueprints, rules, and layouts to ensure consistency and reduce duplication.

Fields become part of a specific configuration only when they are associated with a blueprint. When all fields referenced by a rule are associated to a blueprint, the rule is intrinsically related to the blueprint—no extra linking step is required.

## How fields fit into the configuration model

-   Blueprints: Declare which global fields participate in a configuration. Association enables reuse without cloning.
-   Rules: Read field values as inputs and perform actions on fields \(determine values, show/hide, validate, filter options, add products\).
-   Layouts: Place fields visually and select a Component display type to control how the user interacts with each field.
-   BOM/product list: field values can be mapped to product attribution or extended properties for downstream processing.

## Field scope and life cycle

Fields are created once and available globally. Their life cycle is lightweight and designed for reuse:

1.  Create: Define the field type, name, and unique variable name \(global identifier\).
2.  Associate: Add the field to one or more blueprints to make it available in those configurations.
3.  Place Display: Choose the appropriate Component display type in a layout \(for example, grid, visual picker, slider, read-only\).
4.  Orchestrate: Apply rules to read or set field values, control visibility, present messages, and drive product actions.

## Choosing the right field type

Selecting the correct type ensures valid data and simpler rules:

-   Text: Free-form string input \(up to 2000 characters\), with optional length constraints and default.
-   Number: Numeric input with optional min/max; layout-level options can enforce step or precision and formatting \(currency/percent/read-only currency\).
-   Boolean: True/False with customizable labels and default state.
-   Picklist \(single or multi-select\): Constrained choices with definable options, defaults, and picklist extensions for rich, columnar option data and implicit filtering.
-   Product Picker: A picker specialized for products that can add items to the BOM and map additional data to Product List fields—often removing the need for separate rules.
-   Sets: Tabular collections where each row’s subfields interact row-locally \(ideal for calendar-like or line-item scenarios\).

**Note:** Prefer constrained types \(number, picklist, product picker\) when possible. Clear constraints reduce validation logic and improve end-user guidance.

## Data model vs. display model

The field type defines the data model and specifies what values are valid. The Component display type defines how users interact with the field in a layout \(for example, radio, menu, or grid\). A single field can be rendered differently across layouts while preserving a consistent data model.

Examples:

-   Number: shown as number input, number-with-submit, slider, read-only text/currency, or formatted number.
-   Picklist: shown as traditional menu, vertical radio buttons or check boxes, visual tiles, or grid \(with picklist extension columns\).
-   Product Picker: shown as a grid or visual tile experience with subfields and aggregates.

## Association and reuse

Because fields are global, reuse is the default. Associate a field with any blueprint that needs it; the field is then available to the blueprint’s layouts and rules. If all referenced fields in a rule are associated with the blueprint, the rule is automatically considered related to the blueprint.

This model avoids cloning, reduces drift, and simplifies maintenance across products and experiences.

## Governance and naming

-   Variable names: Use clear, stable, names \(with words separated by underscores, as in shipping\_method\) to make rule scripts expressive and durable.
-   Descriptions: Document intent and valid ranges \(minimum and maximum, semantic meaning\) to aid future reuse.
-   Defaults: Set only when the business logic expects a starting state; otherwise, let rules determine values contextually.

## Accessibility and internationalization

-   Prefer display types that make choices obvious \(radios/tiles\) when option sets are small.
-   Provide human-readable labels and help text; use read-only text with Markdown for structured guidance.
-   Use layout-level formatting for numbers and currency to respect locale conventions.

## Performance and reliability tips

-   Choose the simplest field type that satisfies the requirement. Fewer rules and validations mean faster run times.
-   Use picklist extensions or product pickers to encapsulate rich option data and reduce rule count.
-   Reserve “always-on” determination rules for true system defaults; prefer contextual conditions elsewhere.

## When to use bulk operations

For larger changes or environment migrations, use Matrix Loader to bulk-create and edit fields and field options. The spreadsheet artifact doubles as documentation and accelerates flow from dev to test to production.

**Related topics**  


[Configure fields](fields_101.md)

