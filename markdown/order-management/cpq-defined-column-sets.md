---
title: Defined column set reference
description: Defined column sets organize fields in a fixed, table-based structure with explicit column configuration, used for structured layouts such as product pickers and e-commerce product grids.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/cpq-defined-column-sets.html
release: brazil
topic_type: reference
last_updated: "2026-08-29"
reading_time_minutes: 3
breadcrumb: [Set up layouts, CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Defined column set reference

Defined column sets organize fields in a fixed, table-based structure with explicit column configuration, used for structured layouts such as product pickers and e-commerce product grids.

## Defined Column Properties

-   **Number of Columns**

    Integer value between 1 and 5 \(inclusive\). Specifies how many columns the columnset will have.

-   **Column Width**
    -   **`auto`**

        Width is calculated automatically based on content and available space.

    -   **`pixel`**

        Exact width specified in pixels \(e.g., `100px`, `200px`\). Provides precise control but may overflow on small screens.

    -   **`percentage`**

        Width as a percentage of available container width \(e.g., `25%`, `50%`\). Scales with screen size.

-   **Column Alignment**

    Controls horizontal and vertical alignment of content within the column. Nine alignment options combine horizontal \(left, center, right\) and vertical \(top, middle, bottom\) positioning:

    -   top-left, top-center, top-right
    -   middle-left, center \(middle-center\), middle-right
    -   bottom-left, bottom-center, bottom-right
    Default alignment is top-left.

-   **Column Flow**
    -   **Stacked**

        Fields within the column appear one below the other in a vertical stack.

    -   **Inline wrap**

        Fields within the column appear on the same horizontal line and wrap to the next line if space is insufficient.


## YAML Reference

Defined column sets are configured in the layout YAML using the `columnSetType: defined` property.

```

columnSets:
  - variableName: productPickerColumns
    columnSetType: defined
    columns:
      - width: 100px
        alignment: center
        flow: stacked
      - width: 50%
        alignment: top-left
        flow: stacked
      - width: auto
        alignment: middle-center
        flow: stacked
    elements:
      - type: field
        variableName: txn.line.product.image
        columnOrder: 1
      - type: field
        variableName: txn.line.product.name
        columnOrder: 2
      - type: field
        variableName: txn.line.product.description
        columnOrder: 2
      - type: field
        variableName: txn.line.product.price
        columnOrder: 2
      - type: field
        variableName: txn.line.quantity
        columnOrder: 3
            
```

**Key properties:**

-   `columnSetType: defined` — Activates defined column mode \(omit or set to `responsive` for default behavior\).
-   `columns` — Array of column objects, each with `width`, `alignment`, and `flow`.
-   `columnOrder` — Integer \(1, 2, 3...\) assigned to each field to place it in the correct column.
-   `elements` — Array of fields and buttons; `columnOrder` determines which column each element occupies.

## Field Migration on Column Removal

If you reduce the number of columns after fields have been added, fields in the removed column\(s\) automatically migrate to the nearest previous column. For example:

-   If you have 3 columns with fields distributed across them, and you change to 2 columns, all fields previously in Column 3 move to Column 2.
-   If you remove Column 2 \(middle column\), fields in Column 2 move to Column 1, and fields in Column 3 move to Column 2.

**No data is lost.** All fields and their configurations are preserved during column reduction.

## Warnings and Limitations

-   **Mixed Width Units Warning**

    Do not mix percentage and pixel widths in the same columnset. When detected, a warning appears: “Columns with mixed percentage and pixel units. Manual column alignment is expected.” While the layout will function, runtime behavior may not match expectations. Use consistent width units \(all auto, all pixel, or all percentage\) across all columns.

-   **Loss of Responsiveness**

    Defined columns sacrifice mobile responsiveness for structural control. Content will not wrap or reflow when the window is resized or on narrow mobile screens. Content may be cut off or require horizontal scrolling.

-   **Maximum Column Count**

    The maximum number of columns is 5. If you need more columns, consider using multiple columnsets or switching to responsive mode.

-   **Accessibility Considerations**

    Test defined column layouts with keyboard navigation and screen readers, as fixed column structures may impact navigation order. Ensure alignment and flow settings do not obscure content or create confusing reading order.


## Best Practices

-   **Use for structured data:** Defined columns work best for layouts with fixed, predictable content \(e.g., product grids, comparison tables\).
-   **Test on mobile:** Since responsiveness is lost, always test defined column layouts on mobile devices to ensure content is not cut off.
-   **Consistent width units:** Avoid mixing percentage and pixel widths. Choose one approach per columnset.
-   **Consider responsive first:** Default to responsive columnsets unless you have a specific need for fixed column structure.
-   **Label columns clearly:** Use meaningful field labels and section headers so users understand column organization.

**Related topics**  


[Layout elements and hierarchy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/cpq-layout-elements.md)

[Configure defined column sets in layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-defined-column-sets.md)

[Set up layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/layout_csv_101.md)

