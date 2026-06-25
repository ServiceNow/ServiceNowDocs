---
title: Create a navigation menu block
description: Navigation menu blocks enable you to create a menu of links to different content pages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/content-management-system/t\_CreateNavigationMenuBlock.html
release: australia
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Types of content blocks, Content blocks, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Create a navigation menu block

Navigation menu blocks enable you to create a menu of links to different content pages.

## Before you begin

Role required: content\_admin or admin

## About this task

The following three objects define navigation menus.

-   Menu block: The menu block defines the entire menu block and how it displays.
-   Menu section: The menu sections define groups of links displayed within the block.
-   Menu item: The menu items define the links within each menu section.

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Navigation Menus**.

2.  Click **New**.

    A gallery of available navigation menu blocks displays.

    \[Omitted image "CMSMenuOptions.png"\] Alt text: Navigation menu blocks.

3.  Select the desired menu block style.

4.  Complete the Navigation Menu form to define the block.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique name for the block.|
    |Type|Select the type of navigation menu, which determines how the links are displayed.|
    |Frame|Select a border style for the navigation menu block.|
    |Conditional|Select this check box to enable the use of scripted conditions. If selected, the **Condition** and **Logged On** fields appear.|
    |Logged on|Select this check box to display the navigation menu block only if the user is logged on. This field appears only if **Conditional** is selected.|
    |Condition|Enter a script to define the conditions for the navigation menu block. This field appears only if **Conditional** is selected.|
    |Active|Select this check box to make the block available for use.|
    |Category|Select a category to provide organization for the navigation menu block. The category also determines the detail page in which menu links open.|


-   **[Configure menu sections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_ConfigureMenuSections.md)**  
Menu sections define groups of links displayed within the navigation menu block.
-   **[Menu types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/r_MenuTypes.md)**  
By changing the **Type** field on the navigation menu block, you can format the same menu in different ways.
-   **[Example menu items and content links](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/c_NavigationMenusAndContentLinks.md)**  
The method for choosing a link target \(current window, iFrame, or new window\) and referencing the item linked \(page, attachment, or URL\) are similar. Review examples of how to link within these elements.

**Parent Topic:**[Types of content blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/r_TypesOfContentBlocks.md)

**Related topics**  


[Configure a header block]()

[Configure dynamic blocks]()

[Customize the list block]()

[Configure a static HTML block]()

[Configure Flash movie blocks]()

[Configure content links]()

[Configure iFrames]()

[Configure a detailed content block]()

[Menu style customization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/c_CustomizeTheMenuStyle.md)

