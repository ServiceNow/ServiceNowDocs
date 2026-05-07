---
title: Layouts
description: Layouts define how the configuration experience looks and feels for your users. They control where fields appear, how steps are grouped, and how the product list \(shopping cart\) is presented—turning a blueprint’s logic and data into an intuitive, guided UI in CPQ.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [The CPQ Configurator, CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Layouts

Layouts define how the configuration experience looks and feels for your users. They control where fields appear, how steps are grouped, and how the product list \(shopping cart\) is presented—turning a blueprint’s logic and data into an intuitive, guided UI in CPQ.

A layout is the presentation layer of a configuration experience. Where a blueprint brings together fields, rules, layouts, and configurable products, the layout focuses on how those elements are displayed:

-   Which fields appear on each page or tab
-   How sections are grouped and labeled
-   How sets, product pickers, and messages are arranged
-   How the product list is rendered alongside the configuration

Layouts are defined per blueprint. A single blueprint can have one or more layouts, giving you flexibility to support different personas, channels, or demo experiences without duplicating configuration logic.

When a blueprint has multiple layouts, end users can rotate through them using the alternate layout control in the upper-right corner of the configurator UI.

## How layouts fit into the configuration model

Layouts are placed at the presentation layer of the CPQ configuration stack:

-   Fields collect and display data.
-   Rules control behavior \(visibility, messaging, calculations, product inclusion, and more\).
-   Blueprints tie fields, rules, layouts, and configurable products into a single configuration experience.
-   Layouts define the buyside interface—pages, tabs, sections, and product list—without changing the underlying logic.

Because layouts reference field variable names and product list parameters, you can safely iterate in the layout \(for example, reorganizing tiers or changing display types\) without modifying rules or data structures.

## Layout building blocks

Layouts are composed of reusable structural and visual elements that you define in a layout CSV file and refine in the Layout Wizard or the layout editor.

Tiers: pages, tabs, and sections: Tiers define the major structural areas of the configuration experience. Each tier has a tierDef that describes how it behaves:

-   Pages \(PagesWithLabels\): Break the configuration into discrete steps with progress navigation.
-   Tabs \(VerticalTab\): Group related content horizontally or vertically for quick switching.
-   Accordion \(AccordionWithNavigation\): Show one expanded section at a time for long or complex content.
-   ExpandableSection: Allow users to expand or collapse content as needed.
-   BasicContainer: Provide an unstyled container for simple grouping.

You can nest tiers to build multilevel layouts—for example, pages that contain tabs, or tabs that contain expandable sections.

## Layout definition and tools

Layouts are authored and maintained using a combination of CSV files and in-product tools:

-   CSV layout upload
    -   Primary definition format for layouts
    -   Built in a spreadsheet tool and exported to a CSV file
    -   Supports full control over tiers, column sets, fields, product list, and component properties
-   Layout Wizard
    -   Helps you quickly generate an initial layout from a blueprint’s fields
    -   Provides a visual preview of tiers and major groupings
    -   Acts as a starting point; fine-tuning is done via CSV file or the layout editor
-   Layout editor
    -   Allows you to edit an existing layout directly in the Admin UI
    -   Supports arranging tiers and column sets, editing labels, adjusting display types, and updating extended properties
    -   Provides keyboard shortcuts and visual cues for missing or partially supported elements

Regardless of which tool you use, the layout is ultimately stored as a structured definition that can be exported, versioned, and replaced as your configuration experience evolves.

## Sets and repeatable content

Layouts also control how sets are presented:

-   As tables \(rows and columns with headers\)
-   As lists \(card-style rows with optional selection and search behavior\)
-   In repeaters that focus the user on one set index at a time

Set-specific layout properties—such as expand direction, size controls, message indicators, inline add/remove controls, and upload/download behavior—are configured in the layout via extended properties and raw value JSON.

The product list section of a layout defines how the shopping cart is displayed:

-   Which product list parameters appear as columns \(for example, name, quantity, price, extended attributes\)
-   How columns are labeled and aligned
-   Whether the product list is inline or in a window

Product list columns are driven by the layout CSV file using the `productlist` and `productlistcolumn` types and by referencing `ProductList.<param>` values defined in the product rules and underlying tables.

**Related topics**  


[Set up layouts](layout_csv_101.md)

[Layout Wizard](layout_wizard.md)

[Layout: a deeper dive](layout_deeper_dive.md)

