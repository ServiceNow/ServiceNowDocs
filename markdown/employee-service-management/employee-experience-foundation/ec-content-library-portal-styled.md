---
title: Create customized media with styled content
description: Create banners, block/announcements, or videos using the styled content type to customize settings such as text color, text alignment, links, background colors, and images on Employee Center Pro.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [Portal content, Creating employee communications, Managing employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Create customized media with styled content

Create banners, block/announcements, or videos using the styled content type to customize settings such as text color, text alignment, links, background colors, and images on Employee Center Pro.

## Before you begin

Role required: sn\_cd.content\_manager

If you are creating video content, you must first upload the video: [Add or modify links to other content sources](ecpro-manage-link-content.md)

## About this task

This content type offers three options:

-   Banner: appears at the top of the page ![Banner containing header, heading, body text, and button content](../images/ec-rich-text-content.png)
-   Block: appears in a widget on the page ![Block content containing heading, body, and a button](../images/ec-block-styled.png)
-   Video: can appear anywhere on a page, including at the top in place of a banner

When creating or editing a banner using styled content, you can view and edit the background image rather than editing your image externally and then importing it.

The Form Context menu \(![Form Context menu](../images/ec-hamburger-menu.png)\) at the top, left of the form provides the ability to quickly accomplish tasks when creating content. Select the icon and the following choices appear:

-   Clone: duplicate the content record.
-   Delete: remove the content record and associated scheduled content records.
-   View content record: access and view the content record.

**Note:** You must save the underlying content record before the Form Context menu selections are activated.

## Procedure

1.  Navigate to **Content Publishing** &gt; **Content Library** &gt; **Create New**.

2.  Select **Portal** under the **Select the Platform** column.

3.  Select **Styled content** under the **Choose a content format** section.

4.  Select **Continue**.

5.  Fill in the fields in the **New content** form.

<table id="table_nc1_ttv_frb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content name

</td><td>

The name that describes the content you are creating or editing.

</td></tr><tr><td>

Order

</td><td>

The number that indicates the order in which the portal and styled content appears in the Content list.

</td></tr><tr><td>

Active

</td><td>

Indicates the content is active and available for use.

</td></tr><tr><td>

Content style

</td><td>

Identifies if your content is:-   Banner
-   Block
-   Video


</td></tr><tr><td colspan="2">

CONTENT

</td></tr><tr><td>

User reference table

</td><td>

Determines the variables you can use to personalize text for the block content.Select **HR Profile** to select variables from the sn\_hr\_core\_profile table.

**Note:** When the Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is activated, only **HR Profile** appears.

 Select **User** to select variables from the sys\_user table.

</td></tr><tr><td>

Headline

</td><td>

A title you want to appear for your content. This field is not required if you want your banner to show only a graphic.

**Note:** This field only appears when the Content Experience widget is used.

</td></tr><tr><td>

Heading text

</td><td>

Text that provides additional information or clarity to your headline.

</td></tr><tr><td>

Body text

</td><td>

The detailed message you want to appear over the banner.

</td></tr><tr><td>

User column

</td><td>

Together with the HR profile \[sn\_hr\_core\_profile\] table, filters users when evaluating a condition.This field only appears when you select **HR Profile** from the **User reference table** field.

</td></tr><tr><td>

Text color

</td><td>

Indicates if you want the body text to appear dark or light.**Note:** For the Banner content style, both dark and light are supported. For Block content style, only light is supported if the **Text over background** field is active \(green\).

</td></tr><tr><td>

Text alignment

</td><td>

Indicates how you want your text to appear. You can select left, center, or right justified.

</td></tr><tr><td>

Icon

</td><td>

Determines if you want an icon to appear. Slide right to choose an icon.Only appears when you select **Block** from **Content style**.

</td></tr><tr><td>

Pick an icon

</td><td>

Select the icon you want to appear.This field only appears when you turn the Icon field to green.

</td></tr><tr><td>

Icon size

</td><td>

Indicates the size of your icon.This field only appears when you turn the Icon field to green.

 The recommended size for icons are:

-   Topic icon: 56 x 56px
-   Sub-topic icon: 28 x28px


</td></tr><tr><td>

Call to action

</td><td>

Select if you want a button or link to appear.

</td></tr><tr><td>

Button title

</td><td>

The text that appears over the button.This field only appears when you select **Button**.

</td></tr><tr><td>

Button link

</td><td>

The link the user goes to when selecting the button.Select the down arrow to view a list of links.

 This field only appears when you turn the Icon field to green.

</td></tr><tr><td>

Link title

</td><td>

The text that appears for the link.This field only appears when you select **Link**.

</td></tr><tr><td>

Link

</td><td>

The link the user goes to when selecting the link.Select the down arrow to view a list of links.

 This field only appears when you select **Link**.

</td></tr><tr><td>

Video link

</td><td>

The link to the video you want to appear on your portal.This field only appears when you select **Video** from **Content style**.

**Note:** Only YouTube and Vimeo videos are supported at this time. Ensure you use the embedded video link.

</td></tr><tr><td colspan="2">

BACKGROUND

</td></tr><tr><td>

Background Color

</td><td>

The background color of the banner or block text. To define the color, you can use:-   Hex color codes

**Note:** For a list of hex color codes see [Hex color codes](https://www.color-hex.com/).

-   CSS color value and includes keywords, name, RGB decimal, or RGB hex number of the color.

**Note:** For more information, see [HTML Color Names \(W3CSchools\)](https://www.w3schools.com/tags/ref_colornames.asp).

</td></tr><tr><td>

Background image

</td><td>

Indicates that you want an image to appear as the background. Slide right to display additional image fields.

</td></tr><tr><td>

Image file \[Upload an image\]

</td><td>

Select the link to add an image.This field only appears when you activate **Background image**.

 The recommended size for banners are:

-   Home page banner: 1440 x 400px
-   Topic page: 1258 x 300px


</td></tr><tr><td>

![Edit image button](../images/ec-edit-image-button.png)

</td><td>

Allows you to edit your background image within the Content Library module.This field only appears after you upload a background image. A crop box appears over the image in the Image Editor Mode form.

 You can use the crop box by dragging the edges in or out to indicate what part of your image you want to display.

 After opening the image editor, the default mode is crop.

 When you upload and edit a .svg file, it is saved as a .png file.

**Note:** .gif files are not supported.

 The following icons and buttons appear to help edit your image:

 ![Edit image icons](../images/ec-image-editor-icons.png)

 Each icon allows you to edit the image you imported:

-   Reset to original ![Reset to original icon](../images/ec-reset-orig-icon.png)
    -   Activates after you make edits to your image.
    -   Select and the **Reset to original?** pop-up appears. Select the **Reset image** button to back out any edits you made to your image.

**Note:** After you select **Save**, you can no longer reset your image. You must upload the image again if you are not satisfied with your edits.

    -   If you do not want to keep your edits, select **Cancel**.
-   Move image mode ![Move image mode icon](../images/ec-drag-move-icon.png)
    -   Select your image in any place outside of the crop box and with your mouse, move your image.
    -   Use the points to resize the image.
    -   Press and hold your mouse to move the crop box.
-   Crop image mode ![Crop image mode icon](../images/ec-crop-icon.png)
    -   Select and your cursor is set to crop.
    -   Create a new crop box by holding and dragging your cursor.
    -   Hold and press your mouse to move the crop box.
    -   Resize the crop box using the points.
-   Zoom in ![Zoom in icon](../images/ec-zoom-in-icon.png)
    -   Click to make the image larger and closer.
    -   Continue clicking to incrementally zoom in on the image.
-   Zoom out ![Zoom out icon](../images/ec-zoom-out-icon.png)
    -   Click to make the image smaller and farther away.
    -   Continue clicking to incrementally zoom out on the image.
-   Move left 10 pixels ![Move icon](../images/ec-move-left-icon.png)
    -   Click to move the image to the left by 10 pixels.
    -   Continue clicking to move the image to the left in 10 pixel increments.
-   Move right 10 pixels ![Move icon](../images/ec-move-right-icon.png)
    -   Click to move the image to the right by 10 pixels.
    -   Continue clicking to move the image to the right in 10 pixel increments.
-   Move up 10 pixels ![Move up icon](../images/ec-move-up-icon.png)
    -   Click to move the image up by 10 pixels.
    -   Continue clicking to move the image up in 10 pixel increments.
-   Move down 10 pixels ![Move down icon](../images/ec-move-down-icon.png)
    -   Click to move the image down.
    -   Continue clicking to move the image down in 10 pixel increments.
-   Rotate left 45 degrees ![Rotate icon](../images/ec-rotate-left-icon.png)
    -   Click to rotate the image 45 degrees counter clockwise.
    -   Continue clicking to rotate the image counter clockwise in 45 degree increments.
-   Rotate right 45 degrees ![Rotate icon](../images/ec-rotate-right-icon.png)
    -   Click to rotate the image 45 degrees clockwise.
    -   Continue clicking to rotate the image clockwise in 45 degree increments.
-   Crop-short rectangle ![Crop-short rectangle icon](../images/ec-crop-short-rectangle-icon.png)
    -   Click to change the crop tool to a short rectangle shape.
    -   Use the square points of the rectangle to further crop your image.
-   Crop-tall rectangle ![Crop-tall rectangle icon](../images/ec-crop-tall-rectangle-icon.png)
    -   Click to change the crop tool to a tall rectangle shape.
    -   Use the square points of the rectangle to further crop your image.
-   Crop-square ![Crop-square icon](../images/ec-crop-square-icon.png)
    -   Click to change the crop tool to a square shape.
    -   Use the square points of the square to further crop your image.
-   Custom ![Custom crop and rotate](../images/ec-custom-crop-rotate-icon.png)
    -   Click to display the **Detail Editing** pop-up.
    -   You can define the size of the crop tool and the size of your image by pixels.
    -   You can also specify the angle you want your image rotated.
-   Preview ![Preview icon](../images/ec-preview-icon.png)
    -   Select to display a preview of your edited image.
    -   Enter location information similar to when you publish your content. This allows you to view your image where you want it to appear. For information on the fields, see [Create a publish plan for your content](ec-content-library-publish2.md).
-   Cancel and Save![Cancel and save buttons](../images/ec-cancel-crop-buttons.png)
    -   Select **Cancel** to exit editing your image and not save your changes.
    -   Select **Save** to save the edits you made to your image. You can select **Crop and continue** to continue editing.

**Note:** After you select the **Save and continue** your edits are saved and you cannot back out your edits.

</td></tr><tr><td>

Image size

</td><td>

How you want the image to appear.-   Fill width: Resize the image to cover the entire container, even if the image must be stretched or cut off on the edges.
-   Fit width: Resize the image to ensure it is entirely visible.
-   Original size: Use the original size of the image.
 This field only appears when you activate **Background image**.

</td></tr><tr><td>

Image position

</td><td>

The location you want your image to appear. Select a box to define the image position.This field only appears when you activate **Background image**.

</td></tr><tr><td>

Text over background

</td><td>

Indicates that you want the text to appear over the background image. If you leave unchecked, the text appears below the image.Slide right to select a gradient for your background.

</td></tr><tr><td>

Add gradient

</td><td>

Indicates that you want the text to include color gradient to make your text easier to read.Only appears when you activate the **Text over background** field.

</td></tr></tbody>
</table>6.  Select **Save** to save the record and remain on the **Design** tab.

7.  Or, select **Save and continue** to save the record and move to the **Publish** tab.


## What to do next

-   \(Optional\) Translate your content.

    Request language translation for your content. For more information, see [Multilingual support in the Content Library](../concept/ec-switch-language.md).

    **Note:** Only translate content after you are done modifying the content. For best results, we do not recommend that you add or remove components or change the formatting after translation.

    To create rich content that is formatted differently in different languages, duplicate the content and modify the formatting as needed. Then, use Audiences to target the content to users by language. See [Audiences](../concept/ecpro-audience.md)

-   Preview your content from the **Publish** tab.

    **Note:** Content Preview is designed to provide a general idea of how your content looks. Content may look different once published due to variations in device resolution, theme difference, or mobile app style configuration.

-   Configure a publish plan to control where the content is delivered, the audience, and the period of time it is available: [Create a publish plan for your content](ec-content-library-publish2.md).

