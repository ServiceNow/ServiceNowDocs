---
title: Product lists in layouts
description: Define and customize product lists in CPQ layouts to display data from bills of materials \(BOMs\) and product details. Configure list placement, columns, and display settings in the layout CSV file or the layout editor to present clear, structured product and pricing information to end users.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Set up layouts, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Product lists in layouts

Define and customize product lists in CPQ layouts to display data from bills of materials \(BOMs\) and product details. Configure list placement, columns, and display settings in the layout CSV file or the layout editor to present clear, structured product and pricing information to end users.

In CPQ, layout definition is accomplished via CSV file. Product lists are components that can show products and related information in the bill of materials \(BOM\). There are 2 types of columns in the layout to control the product list component: **productlist** and **productlistcolumns**. Multiple product lists can be included in a layout to display products of different BOM types.

## Defining a product list

In the layout CSV file, define your product list row with the following column guidelines:

-   Type \(column A in the layout CSV file\) for the product list is defined as **productlist**
-   Path \(column B in the layout CSV file\) is not required for the product list. When left blank, this places the product list in the standard position. To place the product list in a tier, specify the path relative to the tier. For example, `/layout/tiers/myTier/myProductList`

A product list has many properties that can be controlled by setting the value field in JSON format.

Example:

```
{
  "location": "right",
  "type": "sales",
  "totalLocation": "bottom",
  "hierarchyColumn": "displayName",
  "displayZeroPriceAs": "On Request",
  "displayNullPriceAs": ""
}
```

## Available options

-   `location` indicates where you want the product list component to display in the layout. The value can be **right** \(default\), **left**, **bottom**, or **modal**.
-   `type` determines which products are included in this product list, based on the **bomType** field in the product. Values can be **sales**, **manufacturing**, or any custom type specified in the products by the admin. Multiple BOM types can be included. For example, `type: sales, customBOMTypeA, customBOMTypeB`, `type: all`
-   `totalLocation` determines where the cart total is shown. Valid values are **bottom**, **top**, **both**, and **none**.
-   `hierarchyColumn` determines which column shows an expand arrow or collapse arrow when a product has child products.
-   `displayZeroPriceAs` and `displayNullPriceAs` determine how to display zero and null prices in the product list. The display value can be any string, such as “On Request”. If 0 \(zero\) is provided, a zero price is shown with locale and symbol or code \(for example, USD 0.00\). Blank is the default, and will be the behavior if not specified.

## Product list columns

Product list columns are children of the product list and define what columns of data are displayed, with the data coming from the products that are displayed in the BOM. For each column of product data you want to display, create a product list column.

In the layout CSV file, define your product list column rows with the following column guidelines:

-   **type** \(column A in the layout CSV file\) for the product list column rows are defined as **productlistcolumn**.
-   **path** \(column B in the layout CSV file\) for product list columns are defined relative to the product list. For example, /productList/columns.
-   **variablename** \(column E in the layout CSV file\) determines what data to display based on the matching field from the product. Extended product list values can be displayed by putting `extended.columnName` in the **variablename** column. For example, `extended.taxExempt` displays the value of `ProductList.extended.taxExempt`.
-   **classname** \(column H in the layout CSV file\) can be set to `allow-wrap` to allow content in that column in the layout to wrap. **value** \(column I in the layout CSV file\) defines the visual styling of the column in the layout.
    -   The **value** column can specify a width. For example: `{"width":"10%"}`.
    -   If specifying a width, using a percentage is recommended for a modal or bottom-docked product list.
    -   The use of fixed units such as **px** \(pixels\) is recommended for left-docked or right-docked product lists, since the width of the product list is fixed. Using **ch** is not recommended.

## Layout editor

The product list and its properties can be edited by using the layout editor in the CPQ UI. The product list layout element is at the bottom of the page:

![Product lists in layouts](../images/cpq-layout-editor-product-list.png)

You can edit this part of the layout by clicking the gear that appears in the top right of the product list layout element when you move your mouse into it. The product list has a settings screen that contains all the properties referenced earlier.

![Product lists in layouts](../images/cpq-layout-editor-product-list-settings.png)

For more information, see [Displaying multiple product lists in layouts](displaying_multiple_productlists_in_layouts.md).

