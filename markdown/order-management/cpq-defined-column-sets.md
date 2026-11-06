---
title: Defined column set reference
description: Defined column sets organize fields in a fixed, table-based structure with explicit control over column count, width, alignment, and flow. Use them for structured layouts such as product pickers and e-commerce product grids.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/cpq-defined-column-sets.html
release: australia
topic_type: reference
last_updated: "2026-08-29"
reading_time_minutes: 6
breadcrumb: [Set up layouts, ServiceNow CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Defined column set reference

Defined column sets organize fields in a fixed, table-based structure with explicit control over column count, width, alignment, and flow. Use them for structured layouts such as product pickers and e-commerce product grids.

## Defined columns compared with responsive columnsets

Defined column sets differ from responsive columnsets in that you explicitly control the number, width, and alignment of columns. While responsive columnsets automatically wrap fields as space is available, defined column sets maintain a fixed structure.

|Feature|Responsive columnsets|Defined column sets|
|-------|---------------------|-------------------|
|Layout behavior|Fields wrap to new lines automatically based on available space|Content stays in assigned columns with fixed positions|
|Configuration|Default behavior with no setup required|Requires explicit column configuration|
|Column control|System determines column count and width dynamically|You specify exact number, width, and alignment of columns|
|Mobile display|Adapts to screen size automatically|Fixed structure may cause content to be cut off on narrow screens|
|Best for|Standard forms and flexible layouts that adapt to different screen sizes|Product grids, ecommerce layouts, and structured data requiring precise alignment|

Defined columns sacrifice responsiveness for structural control. Content does not wrap or reflow when the window is resized.

## Defined column properties

-   **Number of columns**

    Integer value between 1 and 5 \(inclusive\). Specifies how many columns the columnset has.

-   **Column width**
    -   **`auto`**

        Width is calculated automatically based on content and available space.

    -   **`pixel`**

        Exact width specified in pixels \(for example, `100px` or `200px`\). Provides precise control but may overflow on small screens.

    -   **`percentage`**

        Width as a percentage of available container width \(for example, `25%` or `50%`\). Scales with screen size.

-   **Column alignment**

    Controls horizontal and vertical alignment of content within the column. Nine options combine horizontal \(left, center, right\) and vertical \(top, middle, bottom\) positioning:

    -   top-left, top-center, top-right
    -   middle-left, center \(middle-center\), middle-right
    -   bottom-left, bottom-center, bottom-right
    Hover over each alignment icon to see its tooltip. Default alignment is top-left.

-   **Column flow**
    -   **Stacked**

        Fields within the column appear one below the other in a vertical stack.

    -   **Inline wrap**

        Fields within the column appear on the same horizontal line and wrap to the next line if space is insufficient.


## Configure defined columns in a layout

Role required: admin

1.  In the layout editor, select the columnset you want to configure.
2.  Click the **settings** \(cog\) icon in the columnset header. The Column Set Settings panel opens.
3.  Under **Column Type**, select **Defined Columns**. Configuration options appear for column count, width, alignment, and flow.
4.  Set the number of columns by entering a value between 1 and 5. The maximum is 5 columns. The live preview on the right updates to show your column structure.
5.  For each column, configure the following properties:
    -   **Width**: Choose **auto** \(calculated from content\), **pixel** \(an exact width such as 150px or 200px\), or **percentage** \(a share of available width such as 25% or 50%\).
    -   **Alignment**: Choose one of the nine horizontal and vertical alignment options. The default is top-left.
    -   **Flow**: Choose **Stacked** \(fields one below the other\) or **Inline wrap** \(fields on the same line, wrapping when space runs out\).
6.  Observe the **Live Preview** pane to see how the layout appears at runtime. Field names appear in the preview after you add fields to the columnset.
7.  Click **Save** to apply the column settings. If a warning appears about mixed percentage and pixel widths, use consistent units across all columns. See [Warnings and limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/cpq-defined-column-sets.md).
8.  To add fields, select **Add Element** &gt; **Field**. Fields are assigned to columns in the order they are added. Use the Copy and Paste functions to rearrange fields.
9.  Deploy the blueprint to test the layout at runtime.

Your columnset now displays in a fixed, table-based structure with defined columns at runtime in the Quote Experience.

## YAML reference

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

-   `columnSetType: defined`: Activates defined column mode. Omit or set to `responsive` for default behavior.
-   `columns`: Array of column objects, each with `width`, `alignment`, and `flow`.
-   `columnOrder`: Integer \(1, 2, 3, and so on\) assigned to each field to place it in the correct column.
-   `elements`: Array of fields and buttons. `columnOrder` determines which column each element occupies.

## Field migration on column removal

If you reduce the number of columns after fields have been added, fields in the removed columns automatically move to the nearest previous column. No data is lost. For example:

-   If you have 3 columns and change to 2, all fields previously in Column 3 move to Column 2.
-   If you remove Column 2 \(the middle column\), fields in Column 2 move to Column 1, and fields in Column 3 move to Column 2.

No data is lost. All fields and their configurations are preserved during column reduction.

## Warnings and limitations

-   **Mixed width units warning**

    Don't mix percentage and pixel widths in the same columnset. If some columns use percentage and others use pixels, a warning appears: “Columns with mixed percentage and pixel units. Manual column alignment is expected.” The layout still functions, but runtime behavior may not match your expectations. Use consistent width units across all columns in a columnset \(all auto, all pixel, or all percentage\).

-   **Loss of responsiveness**

    Defined columns sacrifice mobile responsiveness for structural control. Content does not wrap or reflow when the window is resized or on narrow mobile screens, so it may be cut off or require horizontal scrolling.

-   **Maximum column count**

    The maximum number of columns is 5. If you need more columns, consider using multiple columnsets or switching to responsive mode.

-   **Accessibility considerations**

    Test defined column layouts with keyboard navigation and screen readers, because fixed column structures can affect navigation order. Make sure alignment and flow settings do not obscure content or create a confusing reading order.


## Example use cases

Product picker layout \(3 columns\):

-   Column 1: Product image \(100px width, auto flow\), centered vertically
-   Column 2: Product name, description, and price \(50%, stacked flow\)
-   Column 3: Quantity field \(auto width, centered\), middle-center alignment

E-commerce product grid \(2 columns\):

-   Column 1: Product details \(60%, stacked flow\)
-   Column 2: Price and add-to-cart button \(40%, centered\)

Service configuration \(4 columns\):

-   One column per tier of attributes: Tier 1, Tier 2, Tier 3, and Price/Total
-   Each column uses stacked flow for vertical field arrangement

## Best practices

-   Use for structured data: Defined columns work best for layouts with fixed, predictable content, such as product grids and comparison tables.
-   Test on mobile: Because responsiveness is lost, always test defined column layouts on mobile devices to make sure content is not cut off.
-   Consistent width units: Avoid mixing percentage and pixel widths. Choose one approach per columnset.
-   Consider responsive first: Default to responsive columnsets unless you have a specific need for a fixed column structure.
-   Label columns clearly: Use meaningful field labels and section headers so users understand the column organization.

**Related topics**  


[Layout elements and hierarchy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/cpq-layout-elements.md)

[Set up layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/layout_csv_101.md)

[Quote transaction layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/quote-tm-layouts.md)

