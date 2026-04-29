---
title: Scripts
description: Learn how scripting extends CPQ beyond simple rules—understand where scripts run, what they return, and how to use them to model advanced configuration logic safely and efficiently.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CPQ, Configure, price, quote, Explore, Sales and Order Management]
---

# Scripts

Learn how scripting extends CPQ beyond simple rules—understand where scripts run, what they return, and how to use them to model advanced configuration logic safely and efficiently.

Scripting enhances CPQ when configuration logic requires more flexibility than simple rules. Administrators can use scripts to calculate complex values, evaluate conditions, or manipulate product data dynamically. Scripts are available in rule conditions, actions, and in blueprint enrichments for initialization, validation, or pricing.

Scripting complements, but does not replace, declarative options. Use standard rules, picklist extensions, and product pickers first. Reserve scripting for specialized scenarios.

## Where can you use scripts

-   Rule conditions: Return `true` or `false` to determine whether actions run.
-   Rule actions: Set field values, hide or display elements, or build product lists dynamically.
-   Blueprint enrichments: Initialize data, call external systems, or enrich configurations during “On Configure” or “Reconfigure” events.

Each script type requires a specific return value to ensure predictable results.

## Expected return values

<table id="table_iry_dsy_ghc"><thead><tr><th>

Script Type

</th><th>

Return Format

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Advanced condition

</td><td>

Boolean

</td><td>

`true` or `false`

</td></tr><tr><td>

Advanced hiding

</td><td>

String

</td><td>

`"field_to_hide"`

</td></tr><tr><td>

Field determination

</td><td>

Depends on field type

</td><td>

Number → `5`; Text → `"Red"`; Multi-select → ```
["Option1",
              "Option2"]
```

</td></tr><tr><td>

Inclusion and exclusion

</td><td>

Array

</td><td>

`["OptionA", "OptionB"]`

</td></tr><tr><td>

Product action

</td><td>

ProductList object

</td><td>

`ProductList.add({id:"123", qty:2})`

</td></tr><tr><td>

Enrichment

</td><td>

Updated configuration object

</td><td>

`return cfgRequest;`

</td></tr></tbody>
</table>## Configuration objects

Scripts interact with the following configuration objects:

-   `cfg`: A read-only snapshot of current field values used by rules.
-   `cfgRequest`: A writable object available in Enrichments; use `.set("value", x)` to modify fields.
-   `ProductList`: Used to add or modify items in the bill of materials \(BOM\).

You can reference properties using either dot or bracket notation \(`cfgRequest.fieldName` or `cfgRequest["fieldName"]`\).

## Working with external data

Use external data to enhance configurations dynamically:

-   Managed tables: Query data with `lookup()` to map results into fields or products.
-   External connections: Make approved calls \(for example, SOQL queries to Salesforce\) to populate sets or field values in Enrichments.

These techniques reduce hard-coded logic and centralize data management.

## Debugging and testing

The scripting interface includes built-in tools:

-   Code suggestions: Autocomplete for functions, variables, and fields.
-   Help panel: Lists all supported functions and parameters with examples.
-   Debugger: Accepts JSON input and displays output and `console.log()` results. Save common test inputs as comments for reuse.

## General guidelines

-   Prefer declarative rules when possible.
-   Keep scripts concise and focused on a single task.
-   Always return the expected data type.
-   Use clear variable names and comments.
-   Avoid nested or long conditional logic—use tables or external connections instead.

**Related topics**  


[Create scripts](scripting.md)

