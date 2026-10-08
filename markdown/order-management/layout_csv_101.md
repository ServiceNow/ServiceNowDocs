---
title: Set up layouts
description: Layouts in CPQ define the structure and appearance of the configuration interface. They organize fields into pages, tabs, and sections, shaping how users interact with configurations and view shopping cart details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/layout\_csv\_101.html
release: brazil
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [layouts]
breadcrumb: [CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up layouts

Layouts in CPQ define the structure and appearance of the configuration interface. They organize fields into pages, tabs, and sections, shaping how users interact with configurations and view shopping cart details.

A layout record defines the buyside user interface for a configuration experience. It consists of fields and the organizational structures—pages, tabs, sections, column sets, and headings—that govern how fields will be represented on the screen. It also describes how the shopping cart should be displayed, by default.

When a blueprint has more than one layout defined, the user can step through them. Use the alternate layout \(\[Omitted image "cpq-layout-alternate-layout-button.png"\] Alt text: Alternate layout icon\) button in the upper-right corner of the buyside UI.

CPQ layouts are defined in spreadsheets and uploaded via matrix loader. Refer to [CSV layout upload](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/csv_layout_upload.md) for detailed instructions.

## Layout element hierarchy

A layout is organized using a hierarchical structure of organizational elements, each playing a specific role:

-   **Pages**

    Top-level organizational boundaries within a layout. Pages divide content into major sections.

-   **Tabs and Vertical Tabs**

    Secondary organization within pages. Users can navigate between tabs to access different groups of fields.

-   **Tiers \(Sections\)**

    Container elements within pages and tabs. Tiers organize fields into logical groups and can be configured as collapsible sections, expandable containers, or simple headings.

-   **Column Sets**

    Arrange fields horizontally within a tier. Support two modes: **Responsive** \(fields wrap on resize; default\) and **Defined Columns** \(fixed number of columns, table-based structure\). See [Defined column set reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/cpq-defined-column-sets.md) for detailed configuration and when to use each mode.

-   **Fields and Buttons**

    Individual data input elements and action buttons placed within columnsets. Fields can display or collect data; buttons trigger events or actions.


## Column set modes: Responsive vs. Defined

|Responsive \(Default\)|Defined Columns|
|----------------------|---------------|
|Fields wrap automatically when space is limited|Fixed column structure; content does not wrap|
|No setup required; add fields freely|Requires specifying number of columns \(1–5\) and width/alignment per column|
|Recommended for standard forms|Recommended for e-commerce, product pickers, structured grids|
|Mobile-friendly; adapts to smaller screens|Less responsive on mobile; content may be cut off on narrow screens|

For full configuration details, see [Defined column set reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/cpq-defined-column-sets.md).

**Related topics**  


[Layout Wizard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/layout_wizard.md)

