---
title: Configure defined column sets in layouts
description: Defined column sets enable you to organize fields in a fixed, table-based structure with explicit column widths and alignment, ideal for product pickers and ecommerce layouts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-defined-column-sets.html
release: brazil
topic_type: task
last_updated: "2026-08-29"
reading_time_minutes: 4
breadcrumb: [Layouts, ServiceNow Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configure defined column sets in layouts

Defined column sets enable you to organize fields in a fixed, table-based structure with explicit column widths and alignment, ideal for product pickers and ecommerce layouts.

## Before you begin

Role required: admin

## About this task

Defined column sets differ from responsive columnsets in that you explicitly control the number, width, and alignment of columns. While responsive columnsets automatically wrap fields as space is set to available, defined column sets maintain a fixed structure.

|Feature|Responsive columnsets|Defined column sets|
|-------|---------------------|-------------------|
|Layout behavior|Fields wrap to new lines automatically based on available space|Content stays in assigned columns with fixed positions|
|Configuration|Default behavior with no setup required|Requires explicit column configuration|
|Column control|System determines column count and width dynamically|You specify exact number, width, and alignment of columns|
|Mobile display|Adapts to screen size automatically|Fixed structure may cause content to be cut off on narrow screens|
|Best for|Standard forms and flexible layouts that adapt to different screen sizes|Product grids, ecommerce layouts, and structured data requiring precise alignment|

Defined columns sacrifice responsiveness for structural control. Content does not wrap or reflow when the window is resized.

## Procedure

1.  In the layout editor, select the columnset you want to configure.

2.  Click the **settings** \(cog\) icon in the columnset header.

    The Column Set Settings panel opens.

3.  Under **Column Type**, select **Defined Columns**.

    Configuration options appear for column count, width, alignment, and flow.

4.  Set the number of columns by entering a value between 1 and 5.

    The maximum is 5 columns. The live preview on the right updates to show your column structure.

5.  For each column, configure the following properties:

    1.  **Width:** Choose one of three options:

        -   **auto** — Column size is calculated automatically based on content.
        -   **pixel** — Specify an exact width in pixels \(e.g., 150px, 200px\).
        -   **percentage** — Specify a percentage of available width \(e.g., 25%, 50%\).
    2.  **Alignment:** Choose horizontal and vertical alignment from 9 options \(top-left, top-center, top-right, middle-left, center, middle-right, bottom-left, bottom-center, bottom-right\).

        Hover over each icon to see a tooltip showing the alignment. Default is top-left.

    3.  **Flow:** Select how fields within the column are arranged:

        -   **Stacked** — Fields appear one below the other \(vertical stack\).
        -   **Inline wrap** — Fields appear on the same line and wrap if space runs out.
6.  Observe the **Live Preview** pane on the right to see how your layout will appear at runtime.

    The preview updates in real time as you adjust column settings. Field names appear in the preview once you add fields to the columnset.

7.  Click **Save** to apply the column settings.

    If a warning appears about mixed percentage and pixel widths, resolve it by using consistent units across all columns. See the "Warning: Mixed width units" section for details.

8.  To add fields, select **Add Element** &gt; **Field**.

    Fields are assigned to columns in the order they are added. You can drag fields between columns to rearrange them.

9.  Deploy the blueprint to test the layout at runtime.

    The defined column layout is now visible to users in the Quote Experience.


## Result

Your columnset now displays in a fixed table-based structure with defined columns at runtime.

## What to do next

Field migration when removing a column: If you later reduce the number of columns \(e.g., from 3 to 2\), fields in the removed column\(s\) are automatically moved to the nearest previous column. For example, if you remove Column 3, all fields in Column 3 migrate to Column 2. No data is lost.

**Warning:**

Don't mix percentage and pixel widths in the same columnset. If some columns use percentage and others use pixels, a warning appears: Columns with mixed percentage and pixel units. Columns manually align is expected.

While the layout will still function, runtime behavior may not match your expectations. Recommendation: Use consistent width units across all columns in a columnset \(all auto, all pixel, or all percentage\).

Example use cases:

Product Picker Layout \(3 columns\):

-   Column 1: Product image \(100px width, auto flow\) — centered vertically
-   Column 2: Product name, description, price \(50%, stacked flow\)
-   Column 3: Quantity field \(auto width, centered\) — middle-center alignment

Ecommerce Product Grid \(2 columns\):

-   Column 1: Product details \(60%, stacked\)
-   Column 2: Price and add-to-cart button \(40%, centered\)

Service Configuration \(4 columns\):

-   One column per tier of attributes: Tier 1, Tier 2, Tier 3, Price/Total
-   Each column uses stacked flow for vertical field arrangement

**Related topics**  


[Quote transaction layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-layouts.md)

[Defined column set reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/cpq-defined-column-sets.md)

[ServiceNow Quote Experience layout UI effects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-ui-effects.md)

