---
title: Portal Catalog Quick Links widget instance options form
description: The instance options enable you to configure the Portal Catalog Quick Links widget on a portal page.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configurable Portal widgets instance options, Configurable Portal Widgets reference, Reference, Customer Service Management]
---

# Portal Catalog Quick Links widget instance options form

The instance options enable you to configure the Portal Catalog Quick Links widget on a portal page.

<table id="table_csm_base_entities"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Catalog Item Table

</td><td>

Table from which the records shown as a card on the widget are selected.By default, this field is set to the Item \[sc\_cat\_item\)\] table.

</td></tr><tr><td>

Display Catalog Items

</td><td>

Displays catalog items according to the selection. The available options are:

-   Manually select
-   Dynamic query

The default selection is Dynamic query.

**Note:** Currently, if you select None, the selection is set to Dynamic query.

</td></tr><tr><td>

Manually Select Catalog Items

</td><td>

The catalog items to appear on the widget chosen manually from a set of predefined catalog items that are associated with the portal.This field applies only when **Manually select** is selected from **Display Articles**.

</td></tr><tr><td>

Dynamic Query

</td><td>

Query to filter catalog records to display on the widget. By default, this field is set to the Service Catalog items \[sc\_cat\_item\] table.

This field applies only when **Dynamic query** is selected from **Display articles**.

</td></tr><tr><td>

Sort by

</td><td>

Field in the Service Catalog items \[sc\_cat\_item\] table that determines the field by which records are sorted and displayed on the widget.This field applies only when **Manually select** or **Dynamic query** is selected from **Display articles**.

</td></tr><tr><td>

Sort Order

</td><td>

The order in which the catalog items appear on a widget.The default sort order is Z to A.

</td></tr></tbody>
</table>|Instance option|Description|
|---------------|-----------|
|Title|Required title of a Portal Catalog Quick Links widget. The default text is `Catalog Quick Links`.|

<table id="table_of3_sbz_2zb"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show Carousel

</td><td>

Option to switch between carousel view and grid view.

</td></tr><tr><td>

Max Quicklinks to Display

</td><td>

Number of catalog items to appear by default on the widget.The default value is 10.

</td></tr><tr><td>

Card Display Style

</td><td>

The display style of a card on the widget.The available options are:

-   Thumbnail
-   Icon on top
-   Icon on left
-   Simple text
-   Title only

The default display style is Thumbnail.

**Note:** Currently, if you select None, the display style is set to Thumbnail.

</td></tr><tr><td>

Catalog Item page

</td><td>

The Catalog item page that open when the catalog item is accessed.By default, this field is set to the Service Catalog items \[sc\_cat\_item\] page.

</td></tr></tbody>
</table>**Related topics**  


[Portal Catalog Quick Links widget](../concept/portal-catalog-widget.md)

[Add and configure the Portal Catalog Quick Links widget](../task/config-cat-quick-links-inst-optns.md)

