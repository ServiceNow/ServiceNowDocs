---
title: Configure a static HTML block
description: Use static blocks for text that does not change. For example, use a static block for a site footer with only the company or organization name. A static HTML block allows any HTML code to be run within a page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/content-management-system/t\_StaticHTMLBlock.html
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

Anyone who edits their own HTML, Jelly, or Javascript may find the HTML editor in the static block limited. The HTML editor can also add tags or formats that advanced coders find unnecessary. For more advanced options, use [dynamic blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_CreateADynamicBlock.md).

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Blocks** &gt; **Static HTML**.

2.  Click **New**.

3.  Complete the Static Content form.

    |Field|Input value|
    |-----|-----------|
    |Name|Type a unique name for the static HTML content block.|
    |Category|Select a category to provide organization for the static HTML block. The category also determines the detail page in which static HTML block links open. Detail pages often display information in different ways.|
    |Frame|Select a border styling for the static HTML block. For more information, see [Format a frame](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_Frame.md).|
    |Active|Select this check box to make the block available for use.|
    |Conditional|Enter any scripted conditions to be applied. If selected, adds a **Condition** script field and **Logged on** check box to the form.|
    |Static Content|Enter [HTML code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_UseHTMLFields.md) that determines the behavior of the static HTML block.|

4.  Click **Submit**.


-   **[Format an image as a static HTML block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_AddAnImageAsAStaticHTMLBlock.md)**  
An easy way to add an image to a CMS page is to use a static HTML block. After the block is created, you can reuse it throughout the site.

**Parent Topic:**[Types of content blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/r_TypesOfContentBlocks.md)

**Related topics**  


[Configure a header block]()

[Create a navigation menu block]()

[Configure dynamic blocks]()

[Customize the list block]()

[Configure Flash movie blocks]()

[Configure content links]()

[Configure iFrames]()

[Configure a detailed content block]()

[Content blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/c_ContentBlocks.md)

[Configure a content block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_CreateAContentBlock.md)

[View CMS block tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_CMSBlockTag.md)

