---
title: Change how messages are displayed to the end user
description: Control how messages appear in CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/can\_i\_change\_how\_messages\_are\_displayed\_to\_the\_end\_user.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Change how messages are displayed to the end user

Control how messages appear in CPQ.

You can show messages to the end user in different formats.

By default, the messages shown for fields on a layout when messaging rules are fired are shown below the field.

\[Omitted image "cpq-messages-below.png"\] Alt text: Field showing the default message style

However, you can override this behavior, such as to show an icon which can be hovered over to display the message \("tooltip"\).

\[Omitted image "cpq-messages-tooltip.png"\] Alt text: Field showing the tooltip message style

In the layout editor, add `{“messageDisplayType”: “<type>”}` to the raw value in the field properties \(the gear icon\) of the element where you want to add the custom message display type.

Accepted type values are `above`, `below`, `popup`, and `tooltip`. The following table provides more information.

<table id="table_pd1_dnf_lkc"><thead><tr><th>

Message display type

</th><th>

Supported on fields

</th><th>

Supported on product picker grid

</th><th>

Supported on fields in set grid

</th><th>

Supported on layout components

</th><th>

Description

</th></tr></thead><tbody><tr><td>

below

</td><td>

Yes \(Default type\)

</td><td>

Yes \(Default type\)

</td><td rowspan="3">

Messages are displayed in a summary container above or below the grid, or as a hover tooltip. You can include an optional indicator on the cell. For more information, see [Using sets in layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/layouts-sets.md)

</td><td>

Yes

</td><td>

Messages are displayed below the target.

</td></tr><tr><td>

above

</td><td>

No

</td><td>

No

</td><td>

Yes \(Default type\)

</td><td>

Messages are displayed above the target.

</td></tr><tr><td>

tooltip

</td><td>

Yes

</td><td>

Yes

</td><td>

Yes

</td><td>

Messages are displayed in a tooltip, visible when hovering the corresponding icon.

</td></tr><tr><td>

popup

</td><td>

Yes

</td><td>

Yes

</td><td>

No

</td><td>

Yes

</td><td>

Messages are displayed within a popup. Once dismissed, the popup won't appear again until additional messages are triggered on the element.

</td></tr></tbody>
</table>The following image shows a popup message \(`{“messageDisplayType”: “popup”}`\).

\[Omitted image "cpq-messages-popup.png"\] Alt text: Field showing the popup message style

