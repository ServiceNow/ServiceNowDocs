---
title: Create a quote transaction layout
description: Create a layout in ServiceNow Quote Experience to define the quote interface for a stage in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-create-layout.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 4
breadcrumb: [Quote transaction layouts, Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create a quote transaction layout

Create a layout in ServiceNow Quote Experience to define the quote interface for a stage in ServiceNow CPQ.

## Before you begin

The stages the layout maps to must exist. For more information, see .

Role required: admin

## About this task

A layout's variable name determines which stage it is associated with. The variable name cannot be changed after the layout is saved — to change it, delete the layout and create a new one. An existing layout can be copied using the **Save As** function in the layout editor. For a description of layout elements and their properties, see [Quote transaction layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-layouts.md).

## Procedure

1.  Navigate to **All** &gt; **CPQ Administration** &gt; **Transaction**.

2.  Select **Layouts** in the left menu, then select **+ Add Layout**.

3.  In the **Name** field, enter the layout name.

    To associate the layout with a specific stage, enter the stage variable name as the layout name. A layout named `layout` applies to all stages with no specific layout assigned. To create a Line Detail layout for a stage, append `_linedetail` to the stage variable name — for example, `draft_linedetail`.

    The visual layout editor opens with a default layout containing the main tier, a line item grid, and a product search capability.

4.  Add tiers to the layout to organize the quote header sections.

    Select the tier type and depth on the Tier Definition tab. Tier types include Accordion, Expandable, Tabs, Vertical tabs, Headings, and Pages. A line item grid must be the only element in its tier.

5.  Add columnsets within tiers to arrange fields and events horizontally.

    Fields and events are arranged vertically using multiple columnsets in the same tier. Add fields, images, text, and buttons within each columnset.

6.  To add an event button in a columnset, use substeps to: add a button, enable the **Event Button** setting, and select the event from the Event picklist.

7.  In the line item grid header section, add buttons to appear above the grid at runtime.

    To add a product search button, add a button and set its UI effect to **Product Search**. Configure target as a slideout or modal, **Show Products**, **Show Favorites**, and **Action Location** in the button properties. For more information about UI effect properties, see [ServiceNow Quote Experience layout UI effects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-ui-effects.md).

8.  In the line item grid column section, add, remove, and order the fields that appear as columns in the grid.

    For each column field, set **Column Width**, **Alignment**, **Enable Sorting**, and **Enable Long Text Popover** in the field properties.

9.  In the line level buttons section, add buttons to appear on each individual line in the grid.

    To add an icon to a line-level button, define the `icon` property in YAML using a value from the SLDS Utility library. For available icon values, see [Quote transaction layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-layouts.md).

10. To enable line numbering, switch to YAML view and add the `showLineNumbers: true` property to the line item grid definition.

    For a comparison of line numbering options including `txn.line.orderNumber` and `txn.line.number` system fields, see [Quote transaction layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-layouts.md).

11. Select the gear icon in the layout subheader and configure the available layout-level settings.

    Settings include **Currency Display**, **Allow selecting disabled options**, **Highlight field changes**, and **Hide Header**.

12. To customize the visual appearance of the layout, open the Customize Theme tab and configure theme properties.

    For the full theme property reference, see [ServiceNow Quote Experience layout UI effects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-ui-effects.md).

13. Select the view toggle in the subheader to switch to YAML view and edit the layout directly.

    If errors exist in the YAML, the **Save** button is disabled. Select the error messages button in the subheader to identify errors, or check the YAML editor for red error indicators. YAML reference snippets are available in [Quote transaction layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-layouts.md).

14. Select **Save**.

    The layout is saved. The blueprint must be deployed for the layout to take effect at runtime.


## What to do next

Deploy the blueprint to apply the updated layout at runtime.

