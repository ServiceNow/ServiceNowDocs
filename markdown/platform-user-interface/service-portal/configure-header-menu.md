---
title: Configure a portal header menu
description: Define the look and behavior of the portal header menu and assign menu items to appear in the header. The header menu is one of the primary navigation controls for Service Portal users.Use the theme to add a header or footer to your portal.Create a menu with menu items to display in the header of a portal.Allow all users to select their language preferences by enabling the language selector in your portal header.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 5
breadcrumb: [Create a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Configure a portal header menu

Define the look and behavior of the portal header menu and assign menu items to appear in the header. The header menu is one of the primary navigation controls for Service Portal users.

## Before you begin

Role required: admin

## About this task

Configuring a portal header with a menu involves several steps.

## Procedure

1.  Create a header and add it to a theme.

    Until you add a theme with a header to a portal, the header menu does not display.

2.  Create a main menu with menu items and assign it to the portal.

    The main menu record is where you assign which navigation options appear in the header. For example, you can add a menu item that links to another page within your portal, such as the service catalog.


## Result

The main menu and header form a header menu when associated with a theme and a portal.

![Gif showing how the header menu and the stock header combine to form the portal menu](../image/HeaderMenu.png)

**Parent Topic:**[Create a portal](create-a-portal.md)

## Add a header or footer to a portal

Use the theme to add a header or footer to your portal.

### Before you begin

Role required: \(admin or none\)

### Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Portal Tables** &gt; **Themes** and then select the theme you want to add the header or footer to.

3.  In the header or footer field, select the header or footer you want to use for your portal.

    If you are just getting started, you can reuse the base system Stock Header or Sample Footer widgets.

4.  Select **Fixed Header** or **Fixed Footer** to lock the header or footer in one place so when users scroll up or down they remain in the same location on the page.

5.  To configure the appearance of the header, in the Service Portal configuration page, open the Branding Editor.

6.  Under the **Theme Colors** tab, use the color selectors in the Navbar section to control the colors in the header.


## Create a portal header menu

Create a menu with menu items to display in the header of a portal.

### Before you begin

Role required: \(admin or none\)

### Procedure

1.  From the Service Portal configuration page \(**Service Portal** &gt; **Service Portal Configuration**\), navigate to **Portal Tables** &gt; **Instance with Menu** and select **New**.

2.  Complete the fields in the menu form.

<table id="table_otc_4nx_tz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name of the header menu. You need to know this when you associate the menu with your portal.

</td></tr><tr><td>

Additional options, JSON format

</td><td>

Advanced configuration options. For example, use this field to enable the shopping cart in the header menu with the following code:```
{
	"enable_cart": {
		"displayValue": "true",
		"value": true
	}
}
```

</td></tr><tr><td>

Application

</td><td>

The record scope. The header menu record and the source table must have the same application scope.

</td></tr><tr><td>

Widget

</td><td>

The widget that the header menu is based on. Select a menu-type widget from the list. For example, the header menu widget that is included as a base system widget.

</td></tr></tbody>
</table>3.  Save the form, and then select **Menu Items** from the related lists.

4.  Select **New** and complete the menu item form.

<table id="table_sgf_yyp_2z"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Name that appears for the item in the menu

</td></tr><tr><td>

Parent menu

</td><td>

This field should already contain the name of the menu you are adding items to. You can change the value as needed to other menus

</td></tr><tr><td>

Parent menu item

</td><td>

Use this field to nest menu items within other menu items

</td></tr><tr><td>

Order

</td><td>

Value that determines where the item appears in the menu in relation to other menu items

</td></tr><tr><td>

Type

</td><td>

The kind of page the item links to. Form fields vary depending on the option that you select from this list. Choose from:-   Page: Link to another page in the Service Portal.
-   URL: Link to an external website. To have the URL open on a new browser tab or window, enter `_blank` in the **URL target** field.
-   Service Catalog: Link to the Service Catalog.
-   Catalog Category: Link to a specific catalog category within the Service Catalog.
-   Catalog Item: Link to a specific catalog item.
-   Knowledge Base: Link to the knowledge base that you previously configured as the portal's default knowledge base.
-   KB Topic: Link to a KB topic page.
-   KB Article: Link to a KB article by number.
-   KB Category: Link to a specific KB category within the knowledge base.
-   Filtered List: Set conditions to determine which page to link to.
-   Scripted List: Enter a script to determine which page to link to.


</td></tr><tr><td>

Page

</td><td>

Name of the portal page the item links to. This option is available if you select **Page** as the menu item type.

</td></tr><tr><td>

Condition

</td><td>

Determines what conditions are required for menu items to show in the header. For example, the condition `gs.hasRole("sp_admin")` restricts access to menu items to users with the sp\_admin role. Hide a menu item by setting this value to **false**. For more information on what conditions to use in the **Condition** field, see [Create a UI Action](https://www.servicenow.com/docs/access?context=t_CreateNewUIAction&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) .

</td></tr><tr><td>

Glyph

</td><td>

Icon that appears beside the menu item

</td></tr></tbody>
</table>5.  Select **Submit**.

6.  After you create a menu and menu items, add the menu to a portal.

    1.  Navigate to **Service Portal** &gt; **Portals**, then open the portal you want to add a menu to.

    2.  From the **Main menu** field, select the reference lookup icon, then select the appropriate menu by name.

    3.  Select **Save**.


### What to do next

Associate the menu you created with a portal, then create a header with a theme for your menu.

## Enable a language selector in portal headers

Allow all users to select their language preferences by enabling the language selector in your portal header.

### Before you begin

Active the languages your portal users need and configure a portal header menu. For more information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) and [Configure a portal header menu](configure-header-menu.md#).

Role required: admin

### About this task

For all portals except the Knowledge \(/kb\), Customer Support \(/csm\), and Customer Service \(/csp\) portals, the language selector is included but turned off by default. To display the language selector in the portal header for other portals, you must enable it according to this procedure.

In portal headers, the language selector displays the current language selection of the user and a menu of languages that the user can choose from. If region grouping is enabled, languages are displayed according to the configured region groups. For more information about grouping languages, see [Create regions for language selection in portals](https://www.servicenow.com/docs/access?context=create-regions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

### Procedure

1.  Navigate to **All**, and then enter `sys_properties.list` in the navigation filter.

2.  Open the **glide.sp.portals.language\_selector\_enabled** property.

3.  In the **Value** field, enter the sys\_ID of the portal to display the language selector widget.

4.  Select **Update**.


### Result

The language selector displays in the header menu for both authenticated and unauthenticated users.

