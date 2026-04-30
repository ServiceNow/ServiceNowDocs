---
title: Format an image as a static HTML block
description: An easy way to add an image to a CMS page is to use a static HTML block. After the block is created, you can reuse it throughout the site.
locale: en-US
release: yokohama
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure a static HTML block, Types of content blocks, Content blocks, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Format an image as a static HTML block

An easy way to add an image to a CMS page is to use a static HTML block. After the block is created, you can reuse it throughout the site.

## Before you begin

Role required: content\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Design** &gt; **Images**.

2.  Click **New**.

3.  Select a **Category** to help organize the images.

4.  Type the file name of the image, including the extension \(such as .png\).

5.  Upload the file by selecting **Click to add** and browsing for the image.

6.  Click **OK**.

7.  Click **Update**.

8.  Navigate to **Content Management** &gt; **Blocks** &gt; **Static HTML** and click **New**.

9.  Paste the following code into the HTML block, substituting the image name as uploaded in the previous step.

    The "x" at the end of the filename is required for image caching.

    ```
    <img src="<image_name>.gifx"/>
    ```

    Now the image is a static HTML block and you can add it to any content page. Use standard HTML code to alter the image in the content block.


**Parent Topic:**[Configure a static HTML block](t_StaticHTMLBlock.md)

**Related topics**  


[Content blocks](../concept/c_ContentBlocks.md)

[Configure a content block](t_CreateAContentBlock.md)

[Configure a header block](t_HeaderBlock.md)

