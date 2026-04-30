---
title: Embed video content in help topics
description: You can embed a link to video content in a custom embedded help topic. YouTube and Vimeo video content is supported.
locale: en-US
release: yokohama
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Embedded Help, Embedded Help, In-product help, Adoption services, Configure user experiences]
---

# Embed video content in help topics

You can embed a link to video content in a custom embedded help topic. YouTube and Vimeo video content is supported.

## Before you begin

Role required: embedded\_help\_admin or admin

## About this task

You cannot use the insert/edit video icon in the HTML editor to embed the video. You must enter the source code.

![Use the source code icon, not the insert video icon, to embed video.](../image/html-editor-video.png "HTML editor icons")

The administrator can disable the ability for users to see embedded video in the [Embedded Help system properties](../reference/embedded-help-sys-properties.md).

## Procedure

1.  Complete the following steps to obtain the embed code for the video.

    1.  Navigate to the location of the video on YouTube or Vimeo.

    2.  Open the **Share** option for the video.

        In YouTube, the text appears below the video. In Vimeo, click the share icon beside the video.

    3.  Under **Embed**, select the code and paste it into a text editor.

    4.  Modify the code to enclose it in a &lt;div&gt; and remove elements that do not get rendered in the embedded help content page.

        For example, here is the embed code for a YouTube video. The modified code also contains a title for the embedded video enclosed in a &lt;p&gt; tag.

        ```
        <iframe width="560" height="315" src="https://www.youtube.com/embed/bqh-5yew2yQ" 
        frameborder="0" allowfullscreen></iframe>
        ```

        After modification, the code looks like this.

        ```
        <div class="video"><iframe src="https://www.youtube.com/embed/bqh-5yew2yQ" 
        allowfullscreen=""></iframe>
        <p class="p">Video: Work at Now</p>
        </div>
        ```

        Vimeo embed code has more attributes. Strip them out so it looks like the following example. Notice the difference between YouTube and Vimeo for the **allowfullscreeen** attribute.

        ```
        <div class="video"><iframe src="https://player.vimeo.com/video/67392563" frameborder="0" 
        allowfullscreen></iframe>
        <p class="p">Video: Work at Now</p>
        </div>
        ```

        **Note:** As shown in the examples, enclose the `<iframe>` and the `<p>` tags within a `<div class="video">` tag. If the administrator disables the property to display video content, all content within the `<div class="video">` tag are hidden.

2.  Navigate to **Embedded Help** &gt; **Help Content**, and then open the custom help topic to embed a video.

3.  Click the source code icon \(**&lt;&gt;**\).

4.  Position your cursor at the end of the line above the location of the video.

5.  Press the Enter key to move to a blank line enter the embed code you modified.

6.  Click **OK**, and then click **Update**.

7.  To test that the video appears, open the page that displays the content you just updated, and then open the help panel.


**Parent Topic:**[Configuring Embedded Help](../concept/configuring-embedded-help.md)

