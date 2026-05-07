---
title: Configure help popups for layouts
description: Implement buyside help popups in CPQ.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configure help popups for layouts

Implement buyside help popups in CPQ.

Help popups give the user more information about a field in a layout. They resemble the **tooltip** message display type, but differ in the following ways:

-   Tool tips appear only when the condition of a message rule is met, whereas help popups are always present on the layout
-   Tool tips display only plain text, whereas help popups can include hyperlinks, lists, italics, bold text, newlines, images, and dynamic text
-   Tool tips appear on hover, whereas help popup icons must be clicked to display messages

**Note:** To learn how to display a message that appears as the result of a message rule, see [Change how messages are displayed to the end user](can_i_change_how_messages_are_displayed_to_the_end_user.md).

## Popup appearance

The image below shows a popup message that appears when the user clicks its help icon. To illustrate dynamic text in a help popup, the second image shows additional text that appears as the result of a selected picklist option.

![Help message popup](../images/cpq-help-message-popups-1.png)

![Help message popup showing dynamic text](../images/cpq-help-message-popups-2.png)

To implement a message popup, add a column header called "help" in cell K1 of your CSV layout.

For a tier, columnset, or field, the format for a help popup is as follows:

```
{"content":"<help body>","heading":"<help heading>","trigger":{"type":"icon","url":"<image.url>”,“label”: “<Label>”}}
```

To assign the popup a button instead of an icon, use "type":"button". The button resembles the following: ![Keyboard icon](../images/cpq-help-message-popup-button.png)

If you don't specify an image URL, a question mark will appear: ![Question mark icon](../images/cpq-help-message-popup-default-icon.png)

If you don't specify a label, the default value is "Help."

## Formatting the popup contents

The following table shows how to control the formatting of the content of a message popup.

<table id="table_ozc_4by_g3c"><thead><tr><th>

Formatting option

</th><th>

Syntax

</th><th>

Output

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Bold

</td><td>

Bold text

</td><td>

\[text display in bold\]

</td><td>

Can use underscores instead of asterisks

</td></tr><tr><td>

Italic

</td><td>

`Italic text`

</td><td>

\[text displays in italics\]

</td><td>

Can use underscore instead of asterisk

</td></tr><tr><td>

Unordered list

</td><td>

`Item\r- Item\r- Item`

</td><td>

-   Item
-   Item
-   Item

</td><td>

 

</td></tr><tr><td>

Ordered list

</td><td>

`1.Item\r2. Item\r3. Item`

</td><td>

1.  Item
2.  Item
3.  Item

</td><td>

 

</td></tr><tr><td>

Newline

</td><td>

```
first line\nsecond line
```

</td><td>

first line

 second line

</td><td>

 

</td></tr><tr><td>

Link

</td><td>

`[link display text](https://www.google.com)`

</td><td>

\[link display text appears as a clickable link\]

</td><td>

Javascript will be sanitized

</td></tr><tr><td>

Image \(GIF\)

</td><td>

`![alt text](image url \"title text\")`

</td><td>

 

</td><td>

Quotes around the title text must be escaped

</td></tr><tr><td>

Dynamic text

</td><td>

`{{ fieldVariableName }}`

</td><td>

 

</td><td>

Outputs the value of the selected field in the text

</td></tr></tbody>
</table>