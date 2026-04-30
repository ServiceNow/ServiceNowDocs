---
title: Sets
description: Learn how sets organize repeatable field groups, simplify complex configurations, and enable data aggregation across repeated elements in ServiceNow CPQ.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-12"
reading_time_minutes: 3
breadcrumb: [ServiceNow CPQ Configurator, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Sets

Learn how sets organize repeatable field groups, simplify complex configurations, and enable data aggregation across repeated elements in ServiceNow CPQ.

A set is a reusable, repeatable collection of fields that lets administrators define multiple instances of similar configuration data—such as multiple products, components, or options—in a single blueprint.

Each row in a set represents one instance of a repeated group of fields, and each field in that row behaves independently. sets streamline configuration design, reduce duplication, and support advanced use cases that require tabular or list-based inputs.

Administrators use sets to present configuration options in structured, table-like layouts that customers can easily edit in the end-user interface.

Sets are designed to:

-   Simplify repeatable configurations. Instead of creating multiple fields and rules for each repetition, define once and reuse many times.
-   Provide intuitive, tabular data entry. End users can add, remove, or edit multiple product instances in a structured grid.
-   Support dynamic rules. Rules can reference values in the same row or aggregate data across all rows.
-   Enable advanced reporting and summaries. Aggregates summarize field values across rows \(for example, total quantity or total rack units\).

## How sets work

A set groups several configuration fields together and repeats that group for each item in the list.

Each set row is fully independent:

-   Fields in the same row can affect other fields in that row.
-   Fields in one row cannot directly affect fields in another row.
-   Fields outside a set can influence fields inside it, but not vice versa.

To affect fields outside a set, use:

-   Aggregates: Sum, count, average, maximum, or minimum values across all rows.
-   Product rules: Define logic that sets external field values based on set data.

A set can contain up to 2,000 rows.

## Display options

Sets can appear in the UI in several formats, depending on user experience requirements:

|Display type|Description|Example use case|
|------------|-----------|----------------|
|Table|Rows, columns, and cells with headers; ideal for detailed comparisons.|Configure multiple network devices.|
|List|Each row shown as a card; can support single-select or multi-select.|Select delivery slots or service packages.|
|Repeater|Displays one record at a time with navigation controls.|Edit configurations one-by-one in smaller layouts.|

Administrators control layout, alignment, and scrolling in the layout editor.

## Field relationships

|Relationship|Behavior|
|------------|--------|
|Inside → Inside|Fields in the same row can trigger each other through rules.|
|Inside → Outside|Not allowed directly; use Aggregates or Product Rules.|
|Outside → Inside|Allowed. Rules or field actions outside a set can change set field values.|

## Key properties

Sets include several configuration categories that shape how users interact with the table or list:

-   General settings: Orientation, maximum height, alignment, index labels.
-   Display type: Choose between Table and List views.
-   Inline settings: Show “Add Row” indicators, drop-down controls, or hover actions.
-   Size settings: Manage how users increase or decrease set rows \(numeric or slider field\).
-   Selection settings: Add single or multiple row selection with a Boolean selection field.
-   Search settings: Allow users to search values in a set \(for example, filter by available date\).
-   Message settings: Display validation messages or indicators in specific cells.

## Managing set data

Sets support importing and exporting data in CSV format.

-   Download set data: Exports only visible columns based on filters applied in the UI.
-   Upload set data: Adds or updates rows in the set using a structured CSV file.
    -   Rules run automatically on upload.
    -   New rows are appended; matching rows are updated.
    -   System-enforced limits apply \(25 visible columns recommended\).

Enable uploads/downloads by adding JSON properties in the set’s raw value:

```
{
  "uploadDetails": {
    "uploadButton": { "label": "Upload CSV", "visible": true },
    "downloadButton": { "label": "Download CSV", "visible": true }
  }
}

```

## Scripting with sets

To reference sets in rules or scripts, use the following syntax:

|Use case|Example syntax|
|--------|--------------|
|Access the set|`set.<setVarName>`|
|Access an aggregate field|`set.<setVarName>.<aggregateVarName>`|

For example:

```
if (set.networkDevices.totalRackUnits > 50) {
   field.requiresAdditionalCooling = true;
}

```

**Related topics**  


[Configure sets](sets.md)

