---
title: The sidebar
description: Use the sidebar element to display persistent information, such as visualizations, product details, or alternate shopping carts, across tiers in a configuration. Define its position and content in the layout CSV file.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/layout\_sidebar.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Set up layouts, ServiceNow CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# The sidebar

Use the sidebar element to display persistent information, such as visualizations, product details, or alternate shopping carts, across tiers in a configuration. Define its position and content in the layout CSV file.

In a layout, the sidebar element can be used to show persistent information to the end user across multiple tiers.

\[Omitted image "cpq-layout-sidebar.png"\] Alt text: Sidebar displayed on the configuration layout

**Note:** This feature is not available in the ServiceNow CPQ layout editor. You must create the sidebar element in the layout CSV and then import the CSV file.

## Setup

When setting up the sidebar, define the sidebar element as a child of the entire layout. The following table lists the cells to fill in, with an example of the sidebar section of the CSV file.

-   Type: sidebar
-   Path: /layout/sidebar
-   Value: `{"location":"right"}` or `{"location":"left"}`

|type|path|label|variablename|component display type|value|
|----|----|-----|------------|----------------------|-----|
|sidebar|/layout/sidebar| | | |`{"location":"right"}`|
|tierdef|/layout/sidebar/tiers| | |BasicContainer| |
|tier|/layout/sidebar/tiers|Tier|tier| | |

The **location** property determines whether the sidebar appears to the user on the left or right of the screen. The sidebar appears in this position during configuration and, unlike the shopping cart, cannot be placed at the bottom of the configurator or moved during configuration.

The child of the sidebar can only be a **tierdef** object. If you add a **tier** or a **columnset** element as a child, the layout is invalid. After a tierdef is defined in the CSV, you can then add the necessary tiers, columnsets, and fields as children as in any other tier.

Only one sidebar can exist in a layout. If you add another, both are combined into the same tier upon deployment.

## Control the sidebar pin

Add the **pinned** property to the sidebar value to control whether the pin button appears to the end user and whether the sidebar is pinned or unpinned by default. Set this property in the `value` cell of the sidebar element in the layout CSV file.

|Value|Description|
|-----|-----------|
|`{"pinned":"PINNED"}`|Hides the pin button and renders the sidebar as pinned.|
|`{"pinned":"UNPINNED"}`|Hides the pin button and renders the sidebar as unpinned.|
|`{"pinned":"DEFAULT"}`|Shows the pin button and renders the sidebar as pinned. The sidebar also uses this behavior when you omit the **pinned** property.|

## Set the sidebar width

Add width properties to the sidebar value to define how wide the sidebar component appears to the end user. Specify each width value in pixels \(`px`\) or viewport width \(`vw`\) units, and set the properties in the `value` cell of the sidebar element in the layout CSV file.

|Property|Description|
|--------|-----------|
|**width**|Sets the default width of the sidebar component. For example, `{"width":"400px"}`.|
|**minWidth**|Sets the minimum width of the sidebar component. For example, `{"minWidth":"300px"}`.|
|**maxWidth**|Sets the maximum width of the sidebar component. For example, `{"maxWidth":"600px"}`.|

## Use case: 3D visualizer

The sidebar can host 3D visualization tools used during configuration. Any changes to fields tied to the visualization are visible to end users regardless of the tier they are on. For more information, see [Integrating ServiceNow CPQ with visualization tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/logik-io-integration-wtih-visualization-tools.md).

## Use case: product information

\[Omitted image "cpq-layout-sidebar-product-info.png"\] Alt text: Sidebar showing product information fields during configuration

The sidebar can display product or quote information — including system or partner fields — throughout the configuration process.

[Example CSV file](https://drive.google.com/file/d/1lXUD_rRKlUub7Airg21tvHQfBuH3AYZD/view?usp=sharing)

## Use case: shopping cart

\[Omitted image "cpq-layout-sidebar-shopping-cart.png"\] Alt text: Sidebar showing a shopping cart in a configuration layout

To show a product list other than the shopping cart to the end user, you can host it in the sidebar. Use this option to list a separate manufacturing BOM type while showing only sales BOM types in the shopping cart.

[Example CSV](https://drive.google.com/file/d/1uB6SjfiHTjff-cI54zdffaEf6bUzSuNy/view?usp=sharing)

