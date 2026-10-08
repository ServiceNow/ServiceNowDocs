---
title: Layout elements and hierarchy
description: Layouts use a hierarchical structure of organizational elements: pages, tabs, tiers \(sections\), column sets, and fields. Understanding how these elements nest and interact helps you design layouts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/cpq-layout-elements.html
release: brazil
topic_type: concept
last_updated: "2026-08-29"
reading_time_minutes: 4
breadcrumb: [Set up layouts, CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Layout elements and hierarchy

Layouts use a hierarchical structure of organizational elements: pages, tabs, tiers \(sections\), column sets, and fields. Understanding how these elements nest and interact helps you design layouts.

## Layout hierarchy overview

The layout element hierarchy from top to bottom is: Layout \(root\) → Pages \(top-level sections\) → Tabs or Tiers \(organization within pages\) → Column Sets \(horizontal arrangement\) → Fields and Buttons \(data/actions\)

Not all levels are required. For example, a simple layout may have only a page, a tier, a columnset, and fields. More complex layouts use multiple pages, tabs, and nested tiers to organize content.

## Element definitions

-   **Page**

    The top-level organizational boundary within a layout. A page is a distinct view or section of the configuration interface. Users navigate between pages using page tabs or buttons. Each page can contain multiple tabs and tiers.

-   **Tab and Vertical Tab**

    Secondary organization within a page. Tabs are displayed as a horizontal or vertical tab bar, allowing users to switch between different groups of content without leaving the page. Each tab can contain tiers and column sets.

-   **Tier \(Section\)**

    A container element that groups related fields and components. Tiers can be configured with different representation types \(for example, simple section, accordion, expandable container\) to control how content is displayed and interacted with. Tiers can be nested within other tiers to create multi-level hierarchies.

-   **Column Set**

    Arranges fields, buttons, and images horizontally within a tier. Column sets support two modes: Responsive \(fields wrap automatically; default\) and Defined Columns \(fixed column structure, table-based layout\). Multiple column sets in the same tier are stacked vertically. See [Defined column set reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/cpq-defined-column-sets.md) for details on both modes.

-   **Field**

    An individual data input or display element placed within a column set. Fields can be text inputs, dropdowns, radio buttons, checkboxes, or read-only text. Each field is associated with a configuration attribute or variable.

-   **Button**

    An action element placed within a column set. Buttons trigger events or navigate users to other views \(for example, a reconfigure button, a link to product picker, a validate button\).

-   **Heading**

    A text label or section title placed within a layout to organize and label content. Headings do not contain fields or interactive elements.


## Nesting rules and constraints

The following rules govern how layout elements can be nested:

-   Layout contains one or more Pages.
-   Page contains one or more Tabs/Vertical Tabs or Tiers.
-   Tab contains one or more Tiers.
-   Tier can contain:
    -   One or more Column Sets \(most common\), or
    -   Nested Tiers, or
    -   A Line Item Grid \(Quote Experience only; must be the only element in the tier\)
-   Column Set contains one or more Fields, Buttons, or Headings.
-   Multiple Column Sets in the same Tier are arranged vertically \(stacked\).

**Important:** A Line Item Grid \(Quote Experience layouts only\) must be the only element in its tier and cannot coexist with column sets or other elements in the same tier.

## Example layout structures

Simple Layout \(No Pages or Tabs\):

-   Layout → Tier \(Heading\) → Column Set → Fields
-   Use case: Basic configuration form with a single section.

Multi-Section Layout \(Multiple Tiers\):

-   Layout → Tier 1 \(General Info\) → Column Set → Fields ↓ Tier 2 \(Advanced Options\) → Column Set → Fields ↓ Tier 3 \(Summary\) → Column Set → Fields
-   Use case: Configuration with distinct logical groups \(General, Advanced, Summary\).

Tabbed Layout \(Horizontal Organization\):

-   Layout → Tab: "Basic" → Tier → Column Set → Fields ↓ Tab: "Advanced" → Tier → Column Set → Fields
-   Use case: Configuration with many options; tabs reduce cognitive load.

Complex Layout \(Nested Tiers + Defined Columns\):

-   Layout → Page: "Config" → Tier \(Accordion\) → Tier \(nested\) → Defined Column Set \(3 columns\) → Fields ↓ Page: "Summary" → Tier → Responsive Column Set → Fields
-   Use case: Multi-step configuration with product picker \(defined columns\) and summary view.

## Choosing between responsive and defined column sets

Most layouts use responsive column sets, which are the default. Choose defined columns when:

-   You need a fixed, table-based structure \(for example, product grid, comparison table\).
-   You want to control column widths and alignment explicitly.
-   You are designing an e-commerce or product picker interface.

Use responsive column sets when:

-   You want the layout to adapt to various screen sizes \(especially mobile\).
-   You are building standard forms or data entry interfaces.
-   You want minimal configuration effort.

For a detailed comparison, see [Defined column set reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/cpq-defined-column-sets.md).

## Layout design tips

-   Organize logically: Group related fields into tiers with meaningful labels.
-   Use tabs for many options: If a single tier contains too many fields, consider splitting them into tabs.
-   Test responsive behavior: Resize your browser and test on mobile to ensure layouts are usable on small screens.
-   Consistent alignment: Use consistent column structures within a tier to maintain visual coherence.
-   Avoid deep nesting: While nesting tiers is allowed, avoid nesting more than 2–3 levels deep, as it can become confusing.

**Related topics**  


[Set up layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/layout_csv_101.md)

[Defined column set reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/cpq-defined-column-sets.md)

[Quote transaction layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-layouts.md)

