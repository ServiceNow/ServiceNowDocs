---
title: Using the sidebar
description: Use the sidebar element to display persistent information—such as visualizations, product details, or alternate shopping carts—across tiers in a configuration. Define its position and content in the layout CSV to enhance visibility and user experience throughout the configuration process.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up layouts, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Using the sidebar

Use the sidebar element to display persistent information—such as visualizations, product details, or alternate shopping carts—across tiers in a configuration. Define its position and content in the layout CSV to enhance visibility and user experience throughout the configuration process.

In a layout, the sidebar element can be used to show persistent information to the end user across multiple tiers.

![Layout: Sidebar](../images/cpq-layout-sidebar.png)

**Note:** Currently, you cannot implement this feature using the CPQ layout editor. You must create the sidebar element in the layout CSV and then import the CSV file.

## Setup

When setting up the sidebar, you must define the sidebar element as a child of the entire layout. The cells to fill in are below together with an example of the sidebar section of the CSV file.

-   Type: sidebar
-   Path: /layout/sidebar
-   Value: `{"location":"right"}` or `{"location":"left"}`

|type|path|label|variablename|component display type|value|
|----|----|-----|------------|----------------------|-----|
|sidebar|/layout/sidebar| | | |`{"location":"right"}`|
|tierdef|/layout/sidebar/tiers| | |BasicContainer| |
|tier|/layout/sidebar/tiers|Tier|tier| | |

The **location** property determines whether the sidebar appears to the user on the left or right of the screen. This is where the sidebar exists during configuration, and unlike the shopping cart's similar property, it cannot be on the bottom of the configurator, nor can it be moved during configuration.

The child of the sidebar can only be a **tierdef** object. If you add a **tier** or a **columnset** element as a child, the layout fails. After a tierdef is defined in the CSV, you can then add the necessary tiers, columnsets, and fields as children as in any other tier.

Only one sidebar can exist on a layout. Adding another will result in their being combined into the same tier upon deployment.

## Use case: 3D visualizer

The sidebar can host the 3D visualization tools an organization uses during configuration. As shown in the example above, any changes to fields that are tied to updating the visualization are shown to end users no matter the tier they are currently on.

## Use case: product information

![Layout: Sidebar](../images/cpq-layout-sidebar-product-info.png)

The sidebar can host anything from the product or quote using the system or partner fields that you would like to make available to the end user throughout the configuration process.

[Example CSV file](https://drive.google.com/file/d/1lXUD_rRKlUub7Airg21tvHQfBuH3AYZD/view?usp=sharing)

## Use case: shopping cart

![Layout: Sidebar](../images/cpq-layout-sidebar-shopping-cart.png)

To show a product list other than the shopping cart to the end user, you can host it in the sidebar. This could be helpful if you need to list a separate manufacturing BOM type while only showing sales BOM types in the shopping cart.

[Example CSV](https://drive.google.com/file/d/1uB6SjfiHTjff-cI54zdffaEf6bUzSuNy/view?usp=sharing)

