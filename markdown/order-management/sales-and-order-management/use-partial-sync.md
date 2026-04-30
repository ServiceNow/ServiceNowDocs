---
title: Use Partial sync
description: Partial sync enables callers to specify only the portions of the structure that matter. The system then populates only the requested types, maintains the full structure \(the skeleton remains intact\), and preserves empty arrays for omitted types to help prevent downstream errors.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-01-10"
reading_time_minutes: 1
breadcrumb: [Explore Partial sync, Lead to Cash Core, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Use Partial sync

Partial sync enables callers to specify only the portions of the structure that matter. The system then populates only the requested types, maintains the full structure \(the skeleton remains intact\), and preserves empty arrays for omitted types to help prevent downstream errors.

Partial sync applies recursive filtering, which means the filter is applied at every level of the hierarchy, not just at the top level.

## allowedContextTypes

`allowedContextTypes` is an array of string identifiers that tells the system which child types to populate.

Example:

```
allowedContextTypes = ["Header", "LineItems"]
```

|allowedContextTypes|Behavior|
|-------------------|--------|
|\[\] \(empty\)|No filtering, full object returned|
|Contains valid types|Only specified types are populated|
|Missing required types|Error returned from `createInstance`|
|Contains invalid types|Ignored, object still returned with empty children|
|Parent matches, child doesn’t|Child remains empty, structure preserved|

## Scenarios

1.  **No filtering**

    If `allowedContextTypes` is empty:

    -   All child types are fully populated.
    -   A proper full json file is returned.
    -   Output matches legacy behavior This scenario serves as the baseline.
2.  **Header only \(or any valid subset\)**

    If `allowedContextTypes` contains only some child types:

    Example:

    ```
    allowedContextTypes:["header","lineItems"]
    ```

    -   Only Header and LineItems are populated.
    -   Other child arrays \(for example, ramps, RelatedParties\) exist but stay empty.
    -   The structure remains intact, no missing arrays.
3.  **Invalid or unrecognized types**

    If the array contains a mix like:

    ```
    allowedContextTypes = ["Header", "XYZ"]
    ```

    -   The system doesn’t crash.
    -   Only Header is populated.
    -   Other child areas remain empty.
    -   Filtering falls back.
4.  **Recursive filtering**

    Filtering applies recursively:

    -   Parent can be included.
    -   Sub-children are evaluated independently.
    -   If a parent is allowed but a sub-child type isn’t, that sub-child stays empty.
    -   Empty arrays are explicitly preserved to maintain consistency.
5.  **Mandatory context rules**

    Header required:

    For scenarios involving header data:

    -   Header must be present in `allowedContextTypes`.
    -   If not, the system throws a validation error:

        ```
        Cannot process without header in allowedContextTypes
        ```

    LineItems required for no Header:

    If the use case excludes the header entirely:

    -   LineItems are required
    -   Missing it produces:

        ```
        Cannot process without line items in allowedContextTypes
        ```


