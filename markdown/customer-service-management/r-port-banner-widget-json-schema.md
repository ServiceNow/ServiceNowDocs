---
title: Portal Banner widget JSON parameters
description: JSON parameters define aspects of the Portal Quick Links widget on the Portal Banner widget.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [JSON parameter in Configurable Portal Widgets, Configurable Portal Widgets reference, Reference, Customer Service Management]
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

Required title of the widget. The default text is `Quick Links`.

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

Option to switch between carousel view and grid view.

</td></tr><tr><td>

quick\_links

</td><td>

Name of the field in the presentation section. The default text is `Quick Links`.

</td></tr></tbody>
</table>