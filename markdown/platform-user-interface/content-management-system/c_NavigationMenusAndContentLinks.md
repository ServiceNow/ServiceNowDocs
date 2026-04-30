---
title: Example menu items and content links
description: The method for choosing a link target \(current window, iFrame, or new window\) and referencing the item linked \(page, attachment, or URL\) are similar. Review examples of how to link within these elements.
locale: en-US
release: xanadu
product: Content Management System
classification: content-management-system
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a navigation menu block, Types of content blocks, Content blocks, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Example menu items and content links

The method for choosing a link target \(current window, iFrame, or new window\) and referencing the item linked \(page, attachment, or URL\) are similar. Review examples of how to link within these elements.

-   A content page reference helps you select the desired page. For example, the value `home.do` links to the site homepage.
-   An attachment reference allows you to reference a single file attached to the menu item or section record. If there is more than one attachment, only the first attachment is referenced. The link is then generated automatically and displays a **Browser File Save** prompt.
-   The specified URL reference allows you to link to a full URL string in your instance or from another system. For example, `com.glideapp.servicecatalog_cat_item_view.do?sysparm_id=66c313e7c0a8016b008ebe1a8e3d97f5&sysparm_nameofstack=b654d15bef921000914304167b225638` links to the **Ask a Question** record producer. Use this reference to link to a page in an existing intranet system.

Menu items can be seen as featured links from each section. There are many choices in URL definitions and link options. Links within the ESS Portal open content pages within the site. In turn, each page has an iFrame or set of blocks that houses the corresponding data. This method is useful for rapid prototyping, but consider where to create dynamic detail pages and use the available linking options.

![Menu item example](../image/MenuItem.png "Menu item")

Menu items are similar to content links except they are called by the list block, not as part of a navigation menu block. Menu items and content links function the same as far as how they are defined and the options available for linking to items. Content links are meant to be called through a list block that calls the Content Link \[content\_link\] table. Content links do not have the **Logged in** field or the **Roles** option used to control the UI experience for various roles.

![Content link example](../image/ContentLink.png "Content link")

-   **[View menu and list examples](../task/t_ExampleMenuSection.md)**  
Menu sections define groups of links and how the links behave.

**Parent Topic:**[Create a navigation menu block](../task/t_CreateNavigationMenuBlock.md)

**Related topics**  


[View links between system elements and URLs](../task/t_LinkToContent.md)

