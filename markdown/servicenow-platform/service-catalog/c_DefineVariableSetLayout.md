---
title: Variable set layout
description: Variable sets can have one of many layouts. You can define the order of the variables for each item.You can set the order value on a per item basis.The following example demonstrates the layout of variables when variable sets and item variables are associated with an item under different scenarios.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Service catalog variable sets, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Variable set layout

Variable sets can have one of many layouts. You can define the order of the variables for each item.

-   **1 column wide**: Variables appear in a single vertical column, ordered from top to bottom. This column is a simple way to display information, but can result in empty space to the right of questions. This order is the default layout.
-   **2 columns wide, alternating sides**: Variables are laid out in two columns with variables placed alternately in the left and right columns.
-   **2 columns wide, one side, then the other**: The first half of the variable set is laid out sequentially in the left column and the second half is laid out sequentially in the right column.

**Note:** Variables with several possible choices defined, such as multiple choice variables, are considered a single entity in layouts. All choices are displayed as a single, contiguous unit.

## Variable set order

A variable set is a discrete unit with an order number by default. All variables within the set are included wherever the set is included.

For example, if you set the following order for some example variables and a variable set:

-   Variable A \(100\)
-   Variable B \(200\)
-   Variable C \(300\)
-   Variable Set 1 \(250\) - containing three variables \(VS1, VS2, VS3\) with incremental order values \(150, 250, 350\)

The variables are displayed in this order:

-   Variable A \(100\)
-   Variable B \(200\)
-   Variable Set 1 \(250\): Variable VS1 \(150\)
-   Variable Set 1 \(250\): Variable VS2 \(250\)
-   Variable Set 1 \(250\): Variable VS3 \(350\)
-   Variable C \(300\)

## Additional layout options

For additional layout options, you can also add container variables to a variable set.

For example, create the following variables and orders:

<table id="table_n4s_n3m_xq"><thead><tr><th>

Variable

</th><th>

Order

</th></tr></thead><tbody><tr><td>

Alfa

</td><td>

100

</td></tr><tr><td>

Bravo

</td><td>

200

</td></tr><tr><td>

Charlie

</td><td>

300

</td></tr><tr><td>

Delta

</td><td>

400

</td></tr><tr><td>

Echo

</td><td>

500

</td></tr><tr><td>

Foxtrot

</td><td>

600

</td></tr></tbody>
</table><table id="table_of2_1km_xq"><thead><tr><th>

1 Column Wide

</th><th>

2 Columns Wide, alternating sides

</th><th>

2 Columns Wide, 1 side, then the other

</th></tr></thead><tbody><tr><td>

Alfa

 Bravo

 Charlie

 Delta

 Echo

 Foxtrot

</td><td>

Alfa Bravo

 Charlie Delta

 Echo Foxtrot

</td><td>

Alfa Delta

 Bravo Echo

 Charlie Foxtrot

</td></tr></tbody>
</table>**Parent Topic:**[Service catalog variable sets](c_ServiceCatalogVariableSets.md)

## Set an item-specific order

You can set the order value on a per item basis.

### Before you begin

Role required: admin

### About this task

When a variable set is used by more than one catalog item, you can define item-specific ordering to provide more flexibility in the layout. You do this using the catalog variable set record associated with the item.

Use the **Order** field in this catalog variable set record to set this order value on a per-item basis, overriding the default value defined in the variable set.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **Maintain Items**.

2.  Open the catalog item to edit.

3.  Navigate to the Variable Sets related list.

4.  Click the reference icon for the variable set.

    ![catalog variable set](../image/SC_Catalog_Variable_Set_Order.png "Catalog variable set")

5.  Set the order value as required.

    The catalog variable set order is specific to the link between the item and the variable set. It overrides the default order defined on the variable set itself.

    ![variable set order](../image/SC_Variable_Set_Order.png "Variable set order")


## Examples of variable set orders

The following example demonstrates the layout of variables when variable sets and item variables are associated with an item under different scenarios.

The order for display of the variables and variable sets is specified using the Information icon in the Related Lists.

![order of variables and variable sets](../image/SC_Variable_Set_Example.png "Order of variables and variable sets")

-   In Layout 1, order values are specified for both Variable Set A and Variable Set B at the Related Lists level and those order values always takes precedence. Hence, the layout is organized based on the order value specified for the variable sets at the Related Lists level.
-   In Layout 2, an order value is not specified for Variable Set A whereas an order value is specified for Variable Set B at the Related Lists level. In this case, the empty value for Variable Set A is considered as zero. Hence, the layout is organized based on the order value of 0 for Variable Set A and 300 for Variable Set B.
-   In Layout 3, order values are not specified for both Variable Set A and Variable Set B at the Related Lists level. In this case, the order values specified within the variable sets are considered. Hence, the layout is organized based on the order value of 400 for Variable Set A and 150 for Variable Set B.

