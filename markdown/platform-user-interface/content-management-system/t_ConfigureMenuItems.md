---
title: Configure menu items
description: Menu items are the links that appear within each menu section.
locale: en-US
release: xanadu
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure menu sections, Create a navigation menu block, Types of content blocks, Content blocks, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Configure menu items

Menu items are the links that appear within each menu section.

## Before you begin

Role required: content\_admin or admin

## About this task

Not all navigation menu sections require menu items. Use menu items to link users to other pages or additional information. These steps use the ESS sample portal site as an example.

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Blocks** &gt; **Navigation Menus** and select a navigation menu.

    For example, select the **Documentation Menu**.

2.  From the **Menu Sections** related list, select a menu section.

    For example, select **Getting Started**.

3.  From the **Menu Items** related list, click **New**.

4.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Name|Type a unique name for the menu item.|
    |Menu section|Select the menu section in which this item appears.|
    |Redirect to|Select what appears when the menu item name and icon are clicked.|
    |URL|Click the lock icon to open the edit field, then enter the URL to open when the menu item title and icon are clicked. This field is available only if **Redirect to** is set to **The specified URL**.|
    |Detail page|Select the content page to open when the name or icon is clicked. This field is available only if **Redirect To** is set to **A content page**.|
    |Image|Select an icon to appear with the name.|
    |Active|Select this check box to make the menu item available for use.|
    |Order|Enter a number to indicate where this item appears on the menu relative to other menu items.|
    |Logged on|Select this check box to display the menu item only if the user is logged on.|
    |Roles|Click the lock to open a list, then select the roles that can access this menu item to restrict access by role.|
    |Category|Select the category in which the menu item belongs.|
    |Open in|Select the behavior of clicked links.|
    |iFrame|Type the name of the iFrame where the link opens when a user clicks the menu item name and icon. Make sure that there is an iFrame on the page. This field is available only if **Open In** is set to **Named iFrame**.|

5.  Click **Submit**.


**Parent Topic:**[Configure menu sections](t_ConfigureMenuSections.md)

**Related topics**  


[Menu types](../reference/r_MenuTypes.md)

[Menu style customization](../concept/c_CustomizeTheMenuStyle.md)

