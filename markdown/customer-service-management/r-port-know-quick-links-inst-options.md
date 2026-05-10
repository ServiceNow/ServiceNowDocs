---
title: Portal Knowledge Quick Links widget instance options form
description: The instance options enable you to configure the Portal Knowledge Quick Links widget on a portal page.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configurable Portal widgets instance options, Configurable Portal Widgets reference, Reference, Customer Service Management]
---

# Portal Knowledge Quick Links widget instance options form

The instance options enable you to configure the Portal Knowledge Quick Links widget on a portal page.

<table id="table_csm_base_entities"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge Table

</td><td>

Table from which the records shown as a card on the widget are selected. By default, this field is set to the Knowledge \[kb\_knowledge\] table.

</td></tr><tr><td>

Display Articles

</td><td>

Displays knowledge articles from the associated knowledge base. The available options are:

-   Manually select: Displays knowledge articles chosen in the **Manually Select Articles** field.
-   Dynamic query: Displays knowledge articles that meet the condition of a query in the Knowledge \[kb\_knowledge\] table defined in the **Dynamic Query** field. If no query is provided, all knowledge articles are displayed in the widget. For more information, see[Generate an encoded query string through a filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/t_GenEncodQueryStringFilter.md)
-   Criteria based: Displays knowledge article based on the criteria Most viewed, Most useful, and Featured. The criteria is determined by the **View** field in the Knowledge \[kb\_knowledge\] table.

The default selection is Criteria based.

**Note:** Currently, if you select None, the selection is set to Criteria based.

</td></tr><tr><td>

Manually Select Articles

</td><td>

The knowledge base articles to appear on the widget that are chosen manually from a set of predefined articles associated with the portal using the knowledge base ID of the article. This field applies only when **Manually select** is selected from **Display Articles**.

</td></tr><tr><td>

Dynamic Query

</td><td>

Query to filter the records to display on the widget

</td></tr><tr><td>

Criteria Based

</td><td>

Displays articles on the widget based on the selected criteria.The available options are:

-   Most Viewed
-   Most Useful
-   Featured

This field applies only when **Criteria based** is selected from **Display articles**.

**Note:** Currently, if you select None, the criteria is set to Most Viewed.

</td></tr><tr><td>

Sort by

</td><td>

Determines the field in the Knowledge \[kb\_knowledge\] table by which quick links are sorted and displayed on the widget. The default value is View Count.

This field applies only when **Manually select** or **Dynamic query** is selected from **Display articles**.

</td></tr><tr><td>

Sort Order

</td><td>

The order in which knowledge articles appear on the widget. By default, the order is z to aThe available options are:

-   z to a
-   a to z

This field applies only when **Manually select** or **Dynamic query** is selected from **Display articles**.

**Note:** Currently, if you select None, the order is set to z to a.

</td></tr></tbody>
</table>|Instance option|Description|
|---------------|-----------|
|Title|Required title of a Portal Knowledge Quick Links widget. The default text is `Article Quicklinks`.|

<table id="table_njh_qkv_2zb"><thead><tr><th>

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

Number of knowledge article quick links to appear by default on the widget.**Note:**

The default value is 10.

</td></tr><tr><td>

Glyph

</td><td>

Glyph to appear on all cards chosen from a set of predefined glyphs.

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

Option to display the rating received on an article.The appearance of the star rating is defined by the \(**glide.knowman.show\_star\_rating**\) system property.

</td></tr><tr><td>

Article View Page

</td><td>

The article page that opens when the article card is accessed.By default, this field is set to the Knowledge Article View \(kb\_article\_view\) page.

</td></tr></tbody>
</table>**Related topics**  


[Portal Knowledge Quick Links widget](../concept/portal-know-quick-links-widget.md)

[Add and configure the Portal Knowledge Quick Links widget](../task/config-portal-know-quick-links-widget-inst-optns.md)

