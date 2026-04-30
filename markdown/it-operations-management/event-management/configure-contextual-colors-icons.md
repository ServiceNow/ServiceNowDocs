---
title: Configure contextual colors and icons
description: Use the Contextual colors and icons form to configure color, text, and icons to have different default or custom contexts, identified by a context ID.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure email for severity changes, Application services in Event Management, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure contextual colors and icons

Use the **Contextual colors and icons** form to configure color, text, and icons to have different default or custom contexts, identified by a context ID.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

You can customize the colors or icons of elements in the **Contextual colors and icons** form to affect the displayed colors or icons of severities in related Event Management screens, either when accessibility mode is off or on. For more information about accessibility, see [Accessibility features](https://www.servicenow.com/docs/access?context=knowledge-management-service-portal&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) .

In each color selection field, you have the option of entering the value of the color as any of the following Cascading Style Sheet \(CSS\) formats that determine how HTML elements should be displayed:

-   Name: predefined color names, for example, red, green, olive, blue, darkblue, or lightblue
-   RGB decimal: RGB\(102, 153, 204\)
-   RGB hex: \#223344

See the following websites for information about CSS color declarations \(including hex or RGB notation\):

-   [HTML Colors \(W3CSchools\)](http://www.w3schools.com/html/html_colors.asp) for more information on hex and RGB notation.
-   [HTML Color Names \(W3CSchools\)](http://www.w3schools.com/tags/ref_colornames.asp) for valid color names.

The context IDs that are provided with the base instance are:

-   information\_severity
-   warning\_severity
-   minor\_severity
-   major\_severity
-   critical\_severity
-   topology\_connection

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Contextual colors and icons**.

2.  Click **New** or modify an existing configuration.

3.  Configure the following fields.

<table id="table_otm_wvm_2bb"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Context details**

</td></tr><tr><td>

Context ID

</td><td>

Enter a unique ID for the context, for example, clear\_severity.

</td></tr><tr><td>

Context Name

</td><td>

Readable name for the context. This text is available to be read out by screen readers.

</td></tr><tr><td>

Batch

</td><td>

The batch that this context is a member of.

</td></tr><tr><td>

Description

</td><td>

Description of uses for the context.

</td></tr><tr><td colspan="2">

**Colors** **Note:** For each entry in the color fields, after you enter a color code, a block appears to the right of the field showing the specified color. Use of invalid color codes triggers an appropriate error notification.

</td></tr><tr><td>

CSS Color

</td><td>

The corresponding CSS color code for the context color name.

</td></tr><tr><td>

CSS Color on Interaction

</td><td>

CSS color code that appears on hover or focus.

</td></tr><tr><td>

Accessible CSS Color

</td><td>

Accessible CSS color code that appears when accessibility mode is enabled.

</td></tr><tr><td>

Accessible CSS Color on Interaction

</td><td>

Accessible CSS color code that appears on hover or focus.

</td></tr><tr><td colspan="2">

**Icons**

</td></tr><tr><td>

Icon

</td><td>

Icon that is displayed when the context includes an icon.

</td></tr><tr><td>

Accessible Icon

</td><td>

Icon that is displayed when the context includes an icon and when accessibility mode is enabled. To add your own icon, or to see a list of available icons, see [Upload one or more images](https://www.servicenow.com/docs/access?context=upload-multiple-images&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Configure email notification on application service severity change](t_EMCreateEmailNotificationBusinessService.md)

