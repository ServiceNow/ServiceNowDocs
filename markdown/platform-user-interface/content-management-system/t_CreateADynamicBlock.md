---
title: Configure dynamic blocks
description: Use dynamic blocks to use scripting or to pull information from the system. Dynamic blocks are where most of your content resides.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/content-management-system/t\_CreateADynamicBlock.html
release: australia
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2026-03-12"
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

For information about Apache Jelly, see Jelly tags.

**Note:** Dynamic Content Blocks in Content Management System are not automatically escaped. These blocks must implement their own content escaping \(e.g., to protect against potential Cross Site Scripting attacks\). For more information, see Jelly escaping types.

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Dynamic**.

2.  Click **New**.

3.  Complete the Dynamic Content form.

    |Field|Description|
    |-----|-----------|
    |Name|Type a unique name for the dynamic content block.|
    |Category|Select a category to provide organization for the dynamic block. The category also determines the detail page in which dynamic block links open.|
    |Frame|Select a border styling for the dynamic block. For more information, see [Format a frame](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_Frame.md).|
    |Active|Select this check box to make the block available for use.|
    |Conditional|Enter any scripted conditions to be applied. If selected, adds a Condition script field to the form.|
    |Two phase|Select this check box to allow two phase Extensions to Jelly syntax.|
    |Dynamic content|Enter the XML script field that determines the behavior of the dynamic block.|


-   **[Catalog cart block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/c_CatalogCartBlock.md)**  
The catalog cart block is a dynamic block provided in the base system.

**Parent Topic:**[Types of content blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/r_TypesOfContentBlocks.md)

**Related topics**  


[Configure a header block]()

[Create a navigation menu block]()

[Customize the list block]()

[Configure a static HTML block]()

[Configure Flash movie blocks]()

[Configure content links]()

[Configure iFrames]()

[Configure a detailed content block]()

[Content blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/c_ContentBlocks.md)

[Configure a content block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_CreateAContentBlock.md)

[View CMS block tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_CMSBlockTag.md)

[Customize the list block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_DefineTheListBlock.md)

[Format an image as a static HTML block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_AddAnImageAsAStaticHTMLBlock.md)

