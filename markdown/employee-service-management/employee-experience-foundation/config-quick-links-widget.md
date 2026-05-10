---
title: Modify the Quick links widget display
description: Design and manage the appearance of the widget, such as the title, display style, tile size, and content alignment.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Quick links, Setup Employee Center browse experience features, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Modify the Quick links widget display

Design and manage the appearance of the widget, such as the title, display style, tile size, and content alignment.

## Before you begin

Role required: sp\_admin or admin

**Note:** These configuration options are only available for the Quick links widget, not the Quick links \(CD\) widget. To verify which widget is present in your portal, open the page in the Service Portal Designer [Create and edit a page using the Service Portal Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/t_ConfigureAPage.md). For more information on how to configure quick links, see [Create a quick link](create-quick-links.md)

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  On the Employee Center home page, press and hold the control key, right-click the Quick links widget, and then select **Instance Options**.

    ![Quick links widget instance options.](../images/quick-inst-opts.png "Quick links instance options")

3.  Configure the instance options.

<table><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Indicates the title of the widget.

</td></tr><tr><td>

Card Display Style

</td><td>

Indicates how you want the card tile to appear on the widget. The choices are:-   **Thumbnail**
-   **Simple**
 Default value: Thumbnail

</td></tr><tr><td>

Card Tile Size

</td><td>

Indicates the size of the card tile on the widget. The choices are:-   **Medium**
-   **Small**
Default value: Medium

</td></tr><tr><td>

Card Content Alignment

</td><td>

Indicates how you want to align the card content on the widget. The choices are:-   **Center**
-   **Default**
Default value: Default**Note:** When you support Right-to-Left languages, change the value to Right. Alternatively, use the center alignment to avoid issues.

</td></tr><tr><td>

Icon Image Display

</td><td>

Displays the icon image for the card tile. Valid only for:-   Thumbnail Center Medium Cards
-   Thumbnail Left Medium and Small Cards


</td></tr><tr><td>

Background Image Display

</td><td>

Displays the background image for the card tile. Valid only for Thumbnail Center Medium and Small Cards

</td></tr><tr><td>

Include Description

</td><td>

Option to include description for the card tile. Valid only for:-   Thumbnail Left Medium Cards
-   Simple Medium Cards


</td></tr><tr><td>

Tile Background Color

</td><td>

Background color of the card tile. The choices are:-   **Primary**
-   **Dark**
-   **Light**
-   **Accent**
-   **Hexcode**
Valid only for thumbnail cards.

</td></tr><tr><td>

Tile Background Color Hexcode

</td><td>

Specify a hex code for the tile background color. Enter a value in this field only if you select **Hexcode** in the **Tile Background Color** field.

</td></tr><tr><td>

Icon Overlay Display

</td><td>

Option to display a circular background for the icon. This option is displayed only when an icon is available.

</td></tr><tr><td>

Icon Overlay Color Hexcode

</td><td>

Option to specify a color for the circular background for the icon. Enter a value in this field after you select the **Icon Overlay Display** option. This field defaults to \#FFFFFF \(white color\) if you do not specify a value in this field.

</td></tr><tr><td>

Text Overlay Display

</td><td>

Option to display the text overlay. Valid only for Thumbnail Center Medium and Small Cards

</td></tr><tr><td>

Text Overlay Color Hexcode

</td><td>

Option to specify a color for the text overlay. Enter a value in this field after you select the **Text Overlay Display** option. This field defaults to \#FFFFFF \(white color\) if you do not specify a value in this field.

</td></tr><tr><td>

Custom Text Color

</td><td>

Indicates custom color for the text. Valid only for thumbnail cards.

</td></tr><tr><td>

Custom Text Color Hexcode

</td><td>

Specify a custom color for the text. Enter a value in this field after you select the **Custom Text Color** option. This field defaults to \#FFFFFF \(white color\) if you do not specify a value in this field.

</td></tr><tr><td>

Quick Links

</td><td>

Add or remove quick links that you want to appear in the widget. By default, you have three Quick Links, however you can add more based on your needs.**Note:** Defer load shows up to six loaders.

</td></tr><tr><td>

Load configuration

</td><td>

Order in which the page and widgets data loads. Select one of the following options:-   None
-   Asynchronous: First the page loads, then the widgets data loads. Users see content appear in the widgets as soon as each individual widget loads.
-   Synchronous: Page and widget data loads at the same time. The page remains blank until all the data loads.


</td></tr><tr><td>

Show empty state

</td><td>

Option to show the widget with empty state message.

</td></tr><tr><td>



</td><td>



</td></tr></tbody>
</table>4.  Click **Save**.


**Parent Topic:**[Quick links](../concept/emp-center-quick-link-config.md)

**Related topics**  


[Create a quick link](create-quick-links.md)

[Create an external link](create-external-links.md)

[Create a quick link](create-quick-links.md)

