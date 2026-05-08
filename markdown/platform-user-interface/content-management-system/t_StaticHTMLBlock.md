---
title: Configure a static HTML block
description: Use static blocks for text that does not change. For example, use a static block for a site footer with only the company or organization name. A static HTML block allows any HTML code to be run within a page.
locale: en-US
release: australia
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Types of content blocks, Content blocks, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Configure a static HTML block

Use static blocks for text that does not change. For example, use a static block for a site footer with only the company or organization name. A static HTML block allows any HTML code to be run within a page.

## Before you begin

Role required: content\_admin or admin

## About this task

Anyone who edits their own HTML, Jelly, or Javascript may find the HTML editor in the static block limited. The HTML editor can also add tags or formats that advanced coders find unnecessary. For more advanced options, use [dynamic blocks](t_CreateADynamicBlock.md).

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Blocks** &gt; **Static HTML**.

2.  Click **New**.

3.  Complete the Static Content form.

    |Field|Input value|
    |-----|-----------|
    |Name|Type a unique name for the static HTML content block.|
    |Category|Select a category to provide organization for the static HTML block. The category also determines the detail page in which static HTML block links open. Detail pages often display information in different ways.|
    |Frame|Select a border styling for the static HTML block. For more information, see [Format a frame](t_Frame.md).|
    |Active|Select this check box to make the block available for use.|
    |Conditional|Enter any scripted conditions to be applied. If selected, adds a **Condition** script field and **Logged on** check box to the form.|
    |Static Content|Enter HTML code that determines the behavior of the static HTML block.|

4.  Click **Submit**.


-   **[Format an image as a static HTML block](t_AddAnImageAsAStaticHTMLBlock.md)**  
An easy way to add an image to a CMS page is to use a static HTML block. After the block is created, you can reuse it throughout the site.

**Parent Topic:**[Types of content blocks](../reference/r_TypesOfContentBlocks.md)

**Related topics**  


[Configure a header block](t_HeaderBlock.md)

[Create a navigation menu block](t_CreateNavigationMenuBlock.md)

[Configure dynamic blocks](t_CreateADynamicBlock.md)

[Customize the list block](t_DefineTheListBlock.md)

[Configure Flash movie blocks](t_FlashMovieBlock.md)

[Configure content links](t_ConfigureContentLinks.md)

[Configure iFrames](t_IFrame.md)

[Configure a detailed content block](t_DetailedContentBlock.md)

[Content blocks](../concept/c_ContentBlocks.md)

[Configure a content block](t_CreateAContentBlock.md)

[View CMS block tags](t_CMSBlockTag.md)

