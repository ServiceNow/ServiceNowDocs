---
title: Layout: a deeper dive
description: Learn advanced layout concepts in CPQ, including tiers, column sets, and product list layouts. Understand how to structure pages, tabs, and sections in CSV files to create dynamic, responsive configuration interfaces with organized and intuitive user experiences.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Set up layouts, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Layout: a deeper dive

Learn advanced layout concepts in CPQ, including tiers, column sets, and product list layouts. Understand how to structure pages, tabs, and sections in CSV files to create dynamic, responsive configuration interfaces with organized and intuitive user experiences.

## Tiers and tierDef

Tiers define the sections of the page.

Each tier and subtier needs a tierDef that defines the component display type \(column F\). Each tier has the following options: Tab, ExpandableSection, Pages, Accordion, AccordionWithNavigation, and VerticalTab. Each of the examples below shows the same configuration with different tier structures.

-   Tabs:

    ![Tiers and tierDef](../images/cpq-layout-deeper-dive-tiers-tabs.png)

-   ExpandableSection \(this makes the layout more vertical\)
-   Pages:

    ![Tiers and tierDef](../images/cpq-layout-deeper-dive-tiers-pages.png)


You also can have subtiers inside tiers.

Tab tier with an ExpandableSection subtier:

![Tiers and tierDef](../images/cpq-layout-deeper-dive-tiers-tabtier.png)

A screenshot of the CSV file used to create this two-tiered layout is shown below. The highlighted cells show how the different tiers are flagged. Because rows 9 and 10 have the same path as the top row tierDef in row 8, the cells are displayed in a tab layout.

![Tiers and tierDef](../images/cpq-layout-deeper-dive-tiers-final-example.png)

Do not define label or variablename at the tierDef level \(row 8 in the image\). They are applied at the tier level \(rows 9 and 10\).

## Label column

For both fields and tiers, the text entered in the label column is the text that appears on screen in the layout. The label for the yellow rows appears as the label for each tab. The label column is also used for fields.

![Tiers and tierDef](../images/cpq-layout-deeper-dive-labelcolumn.png)

## variablename

Variables are used to define the path and call specific fields created in CPQ. In row 9 of the following image, the variablename **background** is defined in column E. In rows 25-29, **background** is added to the path \(column B\). This lets CPQ know that those go in the **background** tier.

![Tiers and tierDef](../images/cpq-layout-deeper-dive-variablename-1.png)

Variables pertaining to layout must be different than variables defined in CPQ for fields or rules. This is because variables defined in CPQ are also used in the layout CSV. The variables names assigned to a field in CPQ UI are used to add the field to the layout. The following images show the CSV file referencing a field variable \(variablename=**desiredIrons**\) that was created in CPQ resulting in the field appearing in the layout.

![Tiers and tierDef](../images/cpq-layout-deeper-dive-variablename-2.png)

![Tiers and tierDef](../images/cpq-layout-deeper-dive-variablename-3.png)

![Tiers and tierDef](../images/cpq-layout-deeper-dive-variablename-4.png)

## Column set types

Column sets help define the vertical positioning of objects in a tier. The layout is responsive to the width of the browser \(which can change\), so CPQ uses column sets to help the Admin identify an intentional row breakpoint.

If the user is using a smaller window where the whole column set does not fit on one row, columns will continue onto the next row. The end of the column set always triggers a new row.

In the following images, the **user** field is part of 1 column set, while the fields **leftHanded** and **bag** are part of a second column set. If the browser window becomes too small for all three pictures \(picklist options for **user**\), the column set continues on the next row. Even though there is room for the **leftHanded** field next to the third image, it is on a new row.

![Tiers and tierDef](../images/cpq-layout-deeper-dive-columnsettypes-1.png)

![Tiers and tierDef](../images/cpq-layout-deeper-dive-columnsettypes-2.png)

![Tiers and tierDef](../images/cpq-layout-deeper-dive-columnsettypes-3.png)

## Column order

The **columnorder** column in the CSV file changes the order of the columns in the same column set. Fields do not have to be added to the CSV in order, as seen in the following image.

![Tiers and tierDef](../images/cpq-layout-deeper-dive-columnorder.png)

## Product list layouts

The product list is how the shopping cart feature of configurations are customized. To add items to the product list, a new product rule is created. When the user selects **Simple**, the following fields are available:

![Tiers and tierDef](../images/cpq-layout-deeper-dive-product-list-1.png)

If the user wants the field to be displayed in the layout, they would add a column to the layout CSV for the field. \(The user would use the values in the**ProductList.&lt;param&gt;** column of the linked table as the variable name. See note 1 for the following image.\)

The following is a screen shot of the product list section of the layout CSV.

![Tiers and tierDef](../images/cpq-layout-deeper-dive-product-list-2.png)

A few things to note:

1.  The variables in this column match the values in the productList.&lt;param&gt; column \{hauss- extList and List are missing\}. This tells CPQ to add the user inputs to the table.
2.  To adjust the alignment of the text in the individual columns add the class **slds-text- align\_left**, **slds-text-align\_right**, or **slds-text-align\_center**. To add multiple class names, separate them with a space.
3.  **price**, **list**, and **extList** always align right so the numbers align nicely.
4.  To save space on the screen, select **modal** for **location**.

## Tier components

Use these tier component property names in the component column of a CSV layout.

<table id="table_uqd_f32_dhc"><thead><tr><th>

Component

</th><th>

Property name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Basic container

</td><td>

**BasicContainer**

</td><td>

Tier container with no decoration or navigation

</td></tr><tr><td>

Expandable sections

</td><td>

**ExpandableSection**

</td><td>

Display tiers in expandable sections with gray bar as section header

 Value setting for initial state: `defaultState: delay | collapsed`

 To lazy-load the tier, use “delay”, which will open the section after other sections have begun rendering

</td></tr><tr><td>

Accordion

</td><td>

**Accordion**

</td><td>

Similar to expandable sections, but only one is expanded

</td></tr><tr><td>

Accordion with navigation

</td><td>

**AccordionWithNavigation**

</td><td>

Similar to expandable sections, but only one is expanded, and next/previous buttons are included

</td></tr><tr><td>

Tabs

</td><td>

**Tab**

</td><td>

Display tiers in a horizontal tab group

</td></tr><tr><td>

Vertical tabs

</td><td>

**VerticalTab**

</td><td>

Display tiers in a vertical tab group \(tabs are on the left\)

</td></tr><tr><td>

Pages

</td><td>

**Pages**

</td><td>

Display tiers as pages with a progress nav bar at the top \(tier names are displayed on hover\)

</td></tr><tr><td>

Pages with labels

</td><td>

**PagesWithLabels**

</td><td>

Display tiers as pages with a progress nav bar at the top, including labels that truncate as needed \(no hover display\)

</td></tr></tbody>
</table>