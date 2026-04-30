---
title: Add a Video with the Rich Content Editor
description: Use the Rich Content Editor canvas to add videos in your content.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Rich Content Editor, Content Library, Creating employee communications with Content Publishing, Manage, Employee Center, Employee Service Management]
---

# Add a Video with the Rich Content Editor

Use the **Rich Content Editor** canvas to add videos in your content.

## Before you begin

Role required: sn\_cd.content\_manager

Fill in the New content form fields. See [Create rich content](ec-content-library-portal-rich-content.md)

Create the page layout using modules or columns.

-   Modules are predefined content layouts comprised of header, paragraph text, and images. See [Add predefined content layouts with the Rich Content Editor](add-modules-rich-content-editor.md)
-   Columns are containers that enable you to define a custom layout. See [Add columns with the Rich Content Editor](ec-rich-content-canvas.md)

## About this task

The **Rich Content Editor** supports the following types of video:

-   HTML5

    **Note:** Hover text or tooltips are not supported for HTML5 at this time.

-   YouTube
-   Vimeo
-   Video streaming service

    **Note:** You must configure a content provider to use videos from a video streaming service. See [Video hosting integrations framework](../concept/content-providers.md).


## Procedure

1.  Navigate to the canvas by selecting the **Open editor** button from the **Design** tab of the **New content** form.

2.  From the **Blocks** column, use a drag-and-drop method to move the **Video** block to your canvas.

3.  Navigate to **Settings** tab.

4.  Use any of the following styling settings:

<table id="table_zx2_tgw_jyb"><thead><tr><th>

Settings field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Styling

</td></tr><tr><td>

Horizontal align

</td><td>

Configure where the video appears in the container. Choose from the Right, Center, and Left icons.

</td></tr><tr><td colspan="2">

Advanced stylingWhen you insert a video into a container, by default the video is the full width of the container and the height auto-adjusts based on the video dimensions.

</td></tr><tr><td>

Width and Height

</td><td>

Specify the value by entering a number or dragging the sides of the video.Select the unit of measure:

-   px: pixel
-   %: percentage


</td></tr><tr><td>

Margin

</td><td>

Margin is the space between a row and another element/the canvas boundary. Specify the value for top, bottom, right, or left padding by entering a number.

</td></tr><tr><td colspan="2">

Properties

</td></tr><tr><td>

Title

</td><td>

Text that appears when a user hovers over the video.

</td></tr><tr><td>

Provider

</td><td>

Where the video is hosted. Choose from:-   HTML5 Source
-   Vimeo
-   Youtube
-   Video streaming content providers


</td></tr><tr><td>

Source/Video ID

</td><td>

The unique identification for the video you want to appear in your canvas.-   For HTML5, the source is the unique identification for the video you want to appear in your canvas.
-   For YouTube, the video ID is the text that appears after the v= in the URL string.
-   For Vimeo, the video ID are the numbers that appear at the end of the URL string.


</td></tr><tr><td>

Show controls \(Youtube and HTML5 Source\)

</td><td>

Check this box to display the video player controls that your users can interact with to start, stop, control volume, show closed captions, show the video full screen, or change the video settings.

</td></tr></tbody>
</table>5.  Select **Save** or **Save and Finish**.

    Selecting **Save** saves your content and you remain on the **Rich Content Editor** canvas. Selecting **Save and Finish** saves your record and returns you to the **New content** form.


## What to do next

-   \(Optional\) Translate your content.

    Request language translation for your content. For more information, see [Switch language for Content Publishing](../concept/ec-switch-language.md).

    **Note:** Only translate content after you are done modifying the content. For best results, we do not recommend that you add or remove components or change the formatting after translation.

    To create rich content that is formatted differently in different languages, duplicate the content and modify the formatting as needed. Then, use Audiences to target the content to users by language. See [Audiences](../concept/ecpro-audience.md)

-   Preview your content from the **Publish** tab.

    **Note:** Content Preview is designed to provide a general idea of how your content looks. Content may look different once published due to variations in device resolution, theme difference, or mobile app style configuration.

-   Configure a publish plan to control where the content is delivered, the audience, and the period of time it is available: [Create a publish plan for your content](ec-content-library-publish2.md).

