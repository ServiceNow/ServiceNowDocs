---
title: Organization Chart widget
description: The Organization Chart widget shows employees in a tree structure relative to their manager. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Example widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Organization Chart widget

The Organization Chart widget shows employees in a tree structure relative to their manager. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

## Using the widget

In the text input field, enter or select a user to see their manager and subordinates. The widget uses information from the User \[sys\_user\] record to display the organization hierarchy relative to the selected user.

![Organization Chart widget with David Loo selected and Bud Richman showing in the chart as David's manager. David is Alissa's manager.](../image/WidgetOrgChart.png)

Click a card to open the profile page for that user. To reconfigure the card link, change the **URL** or **Page** in the widget instance options.

You can drag individual cards to rearrange the chart.

You can zoom in or out of the chart view by clicking the magnifying glass icons or by scrolling.

## Instance options

Use the instance options to configure the Organization Chart widget for a portal page.

**Note:** There are no valid values for several instance options. By default, you can set only the following instance options:

-   User Background Color
-   Node Background Color
-   URL
-   Page

<table id="table_mtf_cyk_qjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Data

</td></tr><tr><td>

Card Fields

</td><td>

Fields from the user record that appear on each card. By default, each card displays the name, title, department, email, phone, and location of each user.

 There are no valid values that you can enter in this field.

</td></tr><tr><td class="sub-head" colspan="2">

Presentation

</td></tr><tr><td>

User Background Color

</td><td>

Color of the user card. Use color names or Hex codes. For example, you can enter `red` or `#ff0000`.

 ![User background color is red](../image/user-background-color.png)

 The user background color is **lightblue** by default.

</td></tr><tr><td>

Node Background Color

</td><td>

Color of cards that extend from the user card. Use color names or Hex codes. For example, you can enter `yellow` or `#ffff00`.

 ![Node background color is yellow](../image/node-background-color.png)

 The node background color is **azure** by default.

</td></tr><tr><td>

Table Layout

</td><td>

Size and margin of the content in each card.

 There are no valid values that you can enter in this field.

</td></tr><tr><td>

Row Layout

</td><td>

Alignment of the text in the card. The text is left-aligned by default.

 There are no valid values that you can enter in this field.

</td></tr><tr><td>

Line

</td><td>

Color of the lines that connect cards. The lines are black by default.

 There are no valid values that you can enter in this field.

</td></tr><tr><td>

Tree Layout

</td><td>

Size, spacing, and alignment of the chart.

 There are no valid values that you can enter in this field.

</td></tr><tr><td>

Picture Layout

</td><td>

Size of image space in each card. By default, the image space is 55x65 pixels. The user image is shrunk or stretched to fit the space.

 There are no valid values that you can enter in this field.

</td></tr><tr><td class="sub-head" colspan="2">

Behavior

</td></tr><tr><td>

URL

</td><td>

Web address of the page that opens when you click a card. Use the part of the portal URL that references the page ID. For example, to navigate to the Service Catalog, enter `?id=sc_category`.

 If left blank, clicking the card opens the page that is specified in the **Page** field. If the **Page** field is also blank, clicking the card opens the user profile page by default.

</td></tr><tr><td>

Page

</td><td>

Portal page that opens when you click a card. Use the page ID.

 If left blank, clicking the card opens the web address in the **URL** field. If the **URL** field is also blank, clicking the card opens the user profile page by default.

 **Note:** The **URL** field overwrites the **Page** field. To specify a page rather than a URL, leave the **URL** field blank.

</td></tr></tbody>
</table>**Parent Topic:**[Example widgets](sp-example-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

