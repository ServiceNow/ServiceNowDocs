---
title: Portal Browse Taxonomy widget instance options form
description: Instance options enable you to configure the Portal Browse Taxonomy widget on the portal.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configurable Portal widgets instance options, Configurable Portal Widgets reference, Reference, Customer Service Management]
---

# Portal Browse Taxonomy widget instance options form

Instance options enable you to configure the Portal Browse Taxonomy widget on the portal.

<table id="table_csm_base_entities"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Records Per View

</td><td>

The number of catalog items and knowledge articles to appear by default on the widget. The default value is 9.

</td></tr><tr><td>

Glyph for Article Cards

</td><td>

The glyph to appear on the cards, which is chosen from a set of predefined glyphs.

</td></tr><tr><td>

Show Author

</td><td>

Option to display the author's name.

</td></tr><tr><td>

Show View Count

</td><td>

Option to display the total number of views of an article.

</td></tr><tr><td>

Show Last Updated

</td><td>

Option to display the date of the last changes made to an article.

</td></tr><tr><td>

Show Rating

</td><td>

Option to display the rating received on an article. The appearance of the star rating is defined by the \(**glide.knowman.show\_star\_rating**\) system property.

</td></tr><tr><td>

Article View Page

</td><td>

The article page that opens when the article card is accessed.By default, this field is set to the Knowledge Article View \(kb\_article\_view\) page.

</td></tr><tr><td>

Catalog Card Display Style

</td><td>

The display style of a catalog card inside the widget. The available choices are:

-   Icon: An image that appears next to a catalog item. Each catalog item can have its own image. This image is defined by the catalog item entry in the Catalog item \[sc\_catalog\_item\] table.
-   Glyph: Glyph that appears next to all catalog items.

The default display style is Icon.**Note:** Currently, if you select None, the display style is set to Icon.

</td></tr><tr><td>

Glyph for Catalog Items

</td><td>

Displays a window to select a symbol for a catalog items.**Note:** The value in this field is used only when Glyph is selected in the **Catalog Card Display Style** field.

</td></tr><tr><td>

Catalog Item Page

</td><td>

The Catalog item page that opens when the catalog item is accessed.By default, this field is set to the Catalog Item \[sc\_cat\_item\] table.

</td></tr><tr><td>

Display icon for topics

</td><td>

Option to display an icon for the taxonomy topics.

</td></tr><tr><td>

Catalog Order Guide Page

</td><td>

The Catalog Order Guide page that opens when the catalog order guide is accessed. For details, see [Order guides](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/c_ServiceCatalogOrderGuides.md)By default, this field is set to the Order guide \[sc\_cat\_item\_guide\] table.

</td></tr></tbody>
</table>**Related topics**  


[Portal Browse Taxonomy widget](../concept/browse-taxo-widget.md)

[Add and configure the Portal Browse Taxonomy widget](../task/config-portal-browse-taxo-widget.md)

