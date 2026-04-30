---
title: Configure dynamic blocks
description: Use dynamic blocks to use scripting or to pull information from the system. Dynamic blocks are where most of your content resides.
locale: en-US
release: yokohama
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Types of content blocks, Content blocks, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Configure dynamic blocks

Use dynamic blocks to use scripting or to pull information from the system. Dynamic blocks are where most of your content resides.

## Before you begin

Role required: content\_admin or admin

## About this task

A good use of dynamic blocks is job postings. Store the postings in knowledge articles and display the postings with a dynamic block.

Several dynamic blocks are predefined, including the following items.

-   **New Content**: Each of the new content blocks allows for creating blocks while editing content pages.
-   **Clean Login**: The default login page requesting user name and password, which includes a "Remember Me" check box. After the user logs in, this block triggers login rules.
-   **Login**: An area that allows a logged out user to log in and a logged in user to log out. This block is especially useful on publicly available content pages.
-   **Search**: The global text search field. Currently, global text search is the only form of search that can be included in a content page.
-   **Search Results**: An area for displaying global text search results.

For information about Apache Jelly, see [Jelly tags](https://www.servicenow.com/docs/access?context=r_JellyTags&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

**Note:** Dynamic Content Blocks in Content Management System are not automatically escaped. These blocks must implement their own content escaping \(e.g., to protect against potential Cross Site Scripting attacks\). For more information, see [Jelly escaping types](https://www.servicenow.com/docs/access?context=r_JellyEscapingTypes&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Dynamic**.

2.  Click **New**.

3.  Complete the Dynamic Content form.

    |Field|Description|
    |-----|-----------|
    |Name|Type a unique name for the dynamic content block.|
    |Category|Select a category to provide organization for the dynamic block. The category also determines the detail page in which dynamic block links open.|
    |Frame|Select a border styling for the dynamic block. For more information, see [Format a frame](t_Frame.md).|
    |Active|Select this check box to make the block available for use.|
    |Conditional|Enter any scripted conditions to be applied. If selected, adds a Condition script field to the form.|
    |Two phase|Select this check box to allow two phase [Extensions to Jelly syntax](https://www.servicenow.com/docs/access?context=c_ExtensionsToJellySyntax&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|
    |Dynamic content|Enter the XML script field that determines the behavior of the dynamic block.|


-   **[Catalog cart block](../concept/c_CatalogCartBlock.md)**  
The catalog cart block is a dynamic block provided in the base system.

**Parent Topic:**[Types of content blocks](../reference/r_TypesOfContentBlocks.md)

**Related topics**  


[Configure a header block](t_HeaderBlock.md)

[Create a navigation menu block](t_CreateNavigationMenuBlock.md)

[Customize the list block](t_DefineTheListBlock.md)

[Configure a static HTML block](t_StaticHTMLBlock.md)

[Configure Flash movie blocks](t_FlashMovieBlock.md)

[Configure content links](t_ConfigureContentLinks.md)

[Configure iFrames](t_IFrame.md)

[Configure a detailed content block](t_DetailedContentBlock.md)

[Content blocks](../concept/c_ContentBlocks.md)

[Configure a content block](t_CreateAContentBlock.md)

[View CMS block tags](t_CMSBlockTag.md)

[Customize the list block](t_DefineTheListBlock.md)

[Format an image as a static HTML block](t_AddAnImageAsAStaticHTMLBlock.md)

