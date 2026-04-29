---
title: Configure Community Service Portal header menus
description: Configure Community Service Portal header menus to create a consistent user experience across all your end-user facing service portals using a modern interface and a unified navigation menu structure.
locale: en-US
release: australia
product: Communities
classification: communities
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Community Service Portal, Configuring communities, Communities, Customer Service Management]
---

# Configure Community Service Portal header menus

Configure Community Service Portal header menus to create a consistent user experience across all your end-user facing service portals using a modern interface and a unified navigation menu structure.

## Before you begin

Role required: The admin role for your service portal, for example, sp\_admin.

## About this task

Add a theme and header menu to your service portal to define its look and behavior.

## Procedure

1.  Navigate to **All** &gt; **Service Portals** &gt; **Portals** and click the module for the portal you want to modify.

2.  In the information message on the Page form indicating that you have to change the current application to edit the record, select **here**.

    You have to be in the **Communities** application to edit.

3.  In the **Theme** field, enter `CSM Default`.

4.  In the **Main Menu** field, enter `CSM Unified Portal Header Menu`.

5.  Click the information icon next to the **Main menu** field and click **Open Record**.

6.  Click the Settings icon and **System Settings** &gt; **Developer**.

7.  Change the **Application** to **Customer Service Management Unified Theme** and click the Refresh icon.

    You only have to change this setting once.

    The **New** button is displayed next to **Menu Item**.

8.  To display the names of the menu items, personalize the Menu Items related list and add **Display name**.

9.  Click **New** from the Menu Items related list.

10. Fill in the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Label|Name that appears for the item in the menu.|
    |Parent Menu|This field should already contain the name of the menu you are adding items to. You can change the value as required to other menus.|
    |Parent Menu Item|Use this field to nest menu items within other menu items.|
    |Order|Value that determines where the item appears in the menu in relation to other menu items.|
    |Type|The kind of page the item links to. For example, you can link to another page in the portal, or an external URL. Form fields vary depending on the option you select from this list.|
    |Page|Name of the portal page the item links to.|
    |Condition|Determines what conditions are required for menu items to show in the header.|
    |Glyph|Icon that appears beside the menu item|

11. Select **Submit**.


**Parent Topic:**[Community Service Portal](../concept/community-service-portal.md)

