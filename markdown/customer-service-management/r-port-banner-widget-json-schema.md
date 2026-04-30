---
title: Portal Banner widget JSON parameters
description: JSON parameters define aspects of the Portal Quick Links widget on the Portal Banner widget.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Customer Service Management reference, Customer Service Management]
---

# Portal Banner widget JSON parameters

JSON parameters define aspects of the Portal Quick Links widget on the Portal Banner widget.

**Note:** This information assumes that you’re familiar with the JSON code format.

<table id="table_csm_base_entities"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

widget\_title

</td><td>

Required title of the widget. The default text is `Quick Links`.The available configurations are:

-   value: The string value of the **displayValue** parameter.
-   displayValue: Name of the widget\_title field to appear in the presentation section. The default text is `Title`.

</td></tr><tr><td>

card\_display\_style

</td><td>

The style of a card tile for quick links inside the Portal Banner widget.The available options are:

-   Thumbnail
-   Icon on top
-   Icon on left
-   Title &amp; description only
-   Title only

The default display style is Thumbnail.

**Note:** Currently, if you select None, the style is set to Thumbnail.

</td></tr><tr><td>

show\_carousel

</td><td>

Option to switch between carousel view and grid view.The available configurations are:

-   value: The string value of the **displayValue** parameter.
-   displayValue: Name of the show\_carousel field to appear in the presentation section. The default text is `Show Carousel`.

</td></tr><tr><td>

quick\_links

</td><td>

Name of the field in the presentation section. The default text is `Quick Links`.value: The reference value from a table from which the catalog items, knowledge articles, or URL are shown as quick links on the widget. By default, this field is set to the Quick Links \[sn\_ex\_sp\_quick\_link\] table.

</td></tr></tbody>
</table>