---
title: Add Text or a Text section with the Rich Content Editor
description: Use the Rich Content Editor canvas to add Text or a Text section in your content.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Rich Content Editor, Content Library, Creating employee communications with Content Publishing, Manage, Employee Center, Employee Service Management]
---

# Add Text or a Text section with the Rich Content Editor

Use the Rich Content Editor canvas to add **Text** or a **Text section** in your content.

## Before you begin

Role required: sn\_cd.content\_manager

Create the page layout using modules or columns.

-   Modules are predefined content layouts comprised of header, paragraph text, and images. See [Add predefined content layouts with the Rich Content Editor](add-modules-rich-content-editor.md)
-   Columns are containers that enable you to define a custom layout. See [Add columns with the Rich Content Editor](ec-rich-content-canvas.md)

## About this task

-   **Text** provides the tools to format and arrange text.
-   **Text section** provides the tools to format and arrange text and an area to add a headline.

    **Note:** For **Text section**, the headline, text, and container settings are configured separately.


When you copy and paste formatted content into the Rich Content Editor, the content retains its original formatting and appears in a new text box. Alternatively, you can use the browser toolbar option **Edit** &gt; **Paste and Match Style** to paste the content as plain text, matching the formatting of the destination text box.

Pasting behavior:

-   Clicking into the text box and pasting: The content appears at the cursor's position.
-   Selecting the entire text box and pasting: The content appears in a new text box underneath

## Procedure

1.  Navigate to the canvas by selecting the **Open editor** button from the **Design** tab of the **New content** form.

2.  From the **Blocks** column, use a drag-and-drop method to move a **Text** or **Text section** block to your canvas.

3.  Enter text or text and a headline depending on what component you dropped into the column.

4.  Navigate to **Settings** tab.

5.  Use any of the following styling settings:

<table id="table_zx2_tgw_jyb"><thead><tr><th>

Settings field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Styling

</td></tr><tr><td>

Text style

</td><td>

Allows you to quickly change the look of your text by selecting a pre-formatted choice. You can select different headlines or paragraph styles.Headline 1-6 corresponds to h1 - h6 HTML tags.

 Selecting a text style pulls from your portal theme text settings in order to sync with it. For more information, see [Portal configuration](portal-config.md).

</td></tr><tr><td>

Text color

</td><td>

Use this drop-down to change the color of your text.Selecting a text color pulls from your portal theme text settings in order to sync with it. The values are defined as part of the portal theme. Your company can customize the portal theme to have different colors. For more information, see [Portal configuration](portal-config.md).

 Your choices are:

-   Primary: The primary color defined by your portal theme.
-   Muted: The color defined by your portal theme.
-   White: Changes the color of your text to white. This is useful when using a background color other than white.
 Text color assigns predefined CSS classes for text color.

</td></tr><tr><td>

Display

</td><td>

Configure the appearance of multiple components within the same column, such as an image and a text component. Select from the following options:-   **Top and bottom** \(default\): Image appears above the other component.
-   **Side by side**: Image appears with the other component next to it.
**Note:** For best results, set the same display for the components. For example, if you have an image and text components in a column and want the image to appear on the left and the text to appear at the right, change the **Display** settings for both components to **Side by side**.

</td></tr><tr><td>

Text alignment

</td><td>

Determines the horizontal alignment of your text. Choose from:-   Left justify
-   Center justify
-   Right justify
-   Justify \(text is aligned with both margins\)


</td></tr><tr><td colspan="2">

Advanced styling

</td></tr><tr><td>

Padding

</td><td>

Sets the spacing between the text and the border of the text container in pixels or as a percentage of the total text container.Specify the padding for the top, right, bottom, and left sides.

</td></tr><tr><td>

Font name

</td><td>

Defines the font face used to render characters.Click the drop-down arrow to select a different font.

</td></tr><tr><td>

Font size

</td><td>

Sets the size of the font.

</td></tr><tr><td>

Font weight

</td><td>

Determines how bold or light your text appears.Click the drop-down arrow to select a different weight.

</td></tr><tr><td>

Line height

</td><td>

Sets the vertical distance between two lines of text.

</td></tr><tr><td>

Font color

</td><td>

Overrides the font color from your portal theme.To select a color, enter the hex code or click the color picker \(grey square to the right of the font color\) and select a color from the color palette.

</td></tr><tr><td colspan="2">

Properties

</td></tr><tr><td>

ID

</td><td>

A unique ID that identifies the HTML element.

</td></tr><tr><td>

Title

</td><td>

Text that appears when a user hovers over the component.

</td></tr></tbody>
</table>6.  Select **Save** or **Save and Finish**.

    Selecting **Save** saves your content and you remain on the **Rich Content Editor** canvas. Selecting **Save and Finish** saves your record and returns you to the **New content** form.


## What to do next

-   \(Optional\) Translate your content.

    Request language translation for your content. For more information, see [Switch language for Content Publishing](../concept/ec-switch-language.md).

    **Note:** Only translate content after you are done modifying the content. For best results, we do not recommend that you add or remove components or change the formatting after translation.

    To create rich content that is formatted differently in different languages, duplicate the content and modify the formatting as needed. Then, use Audiences to target the content to users by language. See [Audiences](../concept/ecpro-audience.md)

-   Preview your content from the **Publish** tab.

    **Note:** Content Preview is designed to provide a general idea of how your content looks. Content may look different once published due to variations in device resolution, theme difference, or mobile app style configuration.

-   Configure a publish plan to control where the content is delivered, the audience, and the period of time it is available: [Create a publish plan for your content](ec-content-library-publish2.md).

