---
title: Configure content links
description: Use content links to create navigational links to information outside your instance. Content links are the predecessors to navigation menus.
locale: en-US
release: yokohama
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Types of content blocks, Content blocks, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Configure content links

Use content links to create navigational links to information outside your instance. Content links are the predecessors to navigation menus.

## Before you begin

Role required: content\_admin or admin

## About this task

After the content link is configured, it must be defined in a list block. List blocks use content links to reference information outside of your CMS.

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Specialty Content** &gt; **Content Links**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Type a unique name for the content link|
    |Redirect to|Select the location of the external link|
    |Category|Select a category to provide organization for the list content block.|
    |URL|Click the lock icon to open the edit field, then enter the site URL to open when the link is clicked. This field is available only if **Redirect to** is set to **The specified URL**.|
    |Open in|Select the behavior of the clicked link.|
    |Detail page|Select the page where the link opens when it is clicked. This field is available only if **Redirect to** is set to **A content page**.|
    |iFrame|Enter the name of the iFrame where the link opens when it is clicked. Make sure that there is an iFrame on the page where the link opens. This field is available only if **Open In** is set to **Named iFrame**.|

4.  Click **Submit**.

5.  From **Content Management** &gt; **Blocks** &gt; **Lists**, create a list block that references the content links by selecting **Content Link** in the table field.

6.  Create a query to determine which external links display on the page.

    For example, the query `Category is Search` displays any external links that have a category defined as **Search**.

7.  Click **Update**.


**Parent Topic:**[Types of content blocks](../reference/r_TypesOfContentBlocks.md)

**Related topics**  


[Configure a header block](t_HeaderBlock.md)

[Create a navigation menu block](t_CreateNavigationMenuBlock.md)

[Configure dynamic blocks](t_CreateADynamicBlock.md)

[Customize the list block](t_DefineTheListBlock.md)

[Configure a static HTML block](t_StaticHTMLBlock.md)

[Configure Flash movie blocks](t_FlashMovieBlock.md)

[Configure iFrames](t_IFrame.md)

[Configure a detailed content block](t_DetailedContentBlock.md)

