---
title: Create a portal
description: Create a portal for users to browse company resources, discover articles, and get help.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Create a portal

Create a portal for users to browse company resources, discover articles, and get help.

## Before you begin

Role required: admin or sp\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**, then click **New**.

2.  On the form, fill in the fields.

<table id="table_xrm_byw_hw"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name to define your portal. In the browser header and for bookmarks, the title appears as `<Page Title> - <Portal Title>`.

</td></tr><tr><td>

URL suffix

</td><td>

Value that appears appended to an instance URL when you access a portal. For example, if you use `sp`, the instance URL for that portal would be `<instance name>.service-now.com/sp`. Ensure that this value is unique and is not the same as any other portal. **Note:** Avoid using reserved words in your URL to prevent errors when navigating to your portal page. Avoid words such as `portal` and `cms`. Also avoid any JavaScript protected terms.

</td></tr><tr><td>

Homepage

</td><td>

Page that users see first after they sign in.

</td></tr><tr><td>

KB home page

</td><td>

Custom home page that users see when they go to a knowledge base.

</td></tr><tr><td>

Login page

</td><td>

Custom page to authenticate users.

</td></tr><tr><td>

Logo

</td><td>

Logo that appears in the page header. You can also configure the logo in the Branding Editor.

</td></tr><tr><td>

Icon

</td><td>

Icon that appears in the address bar for your portal. Each portal that you create can have a different icon.

</td></tr><tr><td>

Default

</td><td>

Portal to use as your main portal.

</td></tr><tr><td>

Application

</td><td>

Application scope of the portal. This field is uneditable and **Global** by default.

</td></tr><tr><td>

404 page

</td><td>

Default page that your users see whenever a page cannot load properly. You can also define a default 404 page using the **glide.service\_portal.default\_404\_page** system property.

</td></tr><tr><td>

Catalog home page

</td><td>

Custom page to represent the Service Catalog.

</td></tr><tr><td>

Catalog category home page

</td><td>

Page to display catalog categories in the portal.

</td></tr><tr><td>

Main menu

</td><td>

Reference to the menu in the Instances with Menu \[sp\_instance\_menu\] table that appears in the header.

</td></tr><tr><td>

Theme

</td><td>

Refers to a theme in the Themes \[sp\_theme\] table that defines the style and branding for the portal. The theme is the lowest level of style configuration. Any changes made in the Branding Editor or to specific portal components \(such as widget or container CSS\) override those styles.

</td></tr><tr><td>

Inactive

</td><td>

Turn off access to a portal that you no longer want users to visit and optionally redirect them to another portal. For more information, see [Deactivate a portal](deactivate-portal.md).

</td></tr><tr><td>

Quick start config

</td><td>

Schema that defines configuration items in the Branding Editor. In JSON format, you can define the fields and records used to generate your branding options.

 ```json
[{
	"tagline": {
		"table" : "sp_instance",
		"sys_id" : "34fe3d96cb20020000f8d856634c9cf4",
		"field" : "title"
	},
	"hero_background": {
		"table" : "sp_container",
		"sys_id" : "be98a8d2cb20020000f8d856634c9c63",
		"field" : "background_image"
	}
}]
```

</td></tr><tr><td>

CSS variables

</td><td>

Portal-specific Sass variables. You can overwrite existing theme variables here.**Note:** Use the CSS variables field to define CSS variables only. Use CSS Includes to define CSS rules. As of the Madrid release, Sass and LESS can be used within CSS Includes.

</td></tr><tr><td>

Hide portal name

</td><td>

Option to hide the portal name in the page title.

</td></tr><tr><td>

Support right-to-left languages

</td><td>

Option to mirror the direction of the portal when the session language is a right-to-left language, such as Hebrew. Selecting this option automatically generates the necessary CSS but you can also provide your own CSS for right-to-left languages that overrides the auto-generated CSS.

 To provide your own CSS for right-to-left languages, see [Create a portal theme](../concept/c_CustomCSS.md). For more information about support for right-to-left languages, see [Styling for right-to-left languages in portals](../concept/styling-right-to-left-languages.md).

</td></tr><tr><td>

Use portal-specific authentication

</td><td>

Option to set authentication for each portal. Selecting this option configures and applies portal-specific authentication for a portal. For example, set an authentication method, such as OKTA, for an internal employee portal, and set a different authentication method for an external vendor portal without having to customize the authentication.

</td></tr><tr><td>

Enable local login

</td><td>

Option to enable a local login.

</td></tr><tr><td>

Portal Identity Providers

</td><td>

Identity provider options: Okta and Microsoft Azure.

 If both options are selected, then both login options are present in the login page. If only one portal identity provider is configured, the user is directed to the login page for that provider.

</td></tr><tr><td>

Enable favorites

</td><td>

Option to enable the My favorites functionality in the portal.-   Displays the favorite icon \(![favorite icon](../image/favorite.png)\) for all catalog items and KB articles in the portal.
-   Displays the **My Favorites** menu item in the portal header. This menu item displays a list of all catalog items or KB articles that are bookmarked for quick reference.

**Note:**

    -   Only searchable catalog items or KB articles that are selected as favorites are displayed in this list.
    -   This is applicable only for Service Portal. For other portals, you can clone the **My Favorites** menu item.
 You may need to configure the form to add this check box.

</td></tr><tr><td class="sub-head" colspan="2">

AI Search

</td></tr><tr><td>

Enable AIS

</td><td>

Option to enable AI Search in your portal. For more information, see [AI Search in Service Portal](../concept/ai-search.md).

</td></tr><tr><td>

Search Application

</td><td>

Defines the search experience settings for your portal, such as the search engine, search results limit, and suggestions limit. For more information on defining a search application configuration, see Defining search application configurations.

</td></tr><tr><td>

Search Results Configuration

</td><td>

Defines how search results are displayed in the portal. For more information on defining a search results configuration, see Define a composite dataset.

</td></tr></tbody>
</table>3.  Save the form.

4.  In the Knowledge Bases related list, select **Edit** and then select which knowledge bases appear for the knowledge base page.

    For example, if you select **IT** and **Instance Security Center**, only the article categories defined for these knowledge bases appear in the [KB categories widget](../concept/kb-categories-widget.md).

5.  In the **Catalogs** related list, click **Edit** to select one or more catalogs listed in the sc\_catalog table to use in the portal.


-   **[Assign a homepage to a portal](assign-portal-homepage.md)**  
Edit your portal record to specify any page as your homepage.
-   **[Assign a default error page](../concept/create-a-default-404-page.md)**  
Create a default 404 error page for your portal using a system property.
-   **[Configure a portal header menu](configure-header-menu.md#)**  
Define the look and behavior of the portal header menu and assign menu items to appear in the header. The header menu is one of the primary navigation controls for Service Portal users.
-   **[Configure a catalog in Service Portal](associate-portal-catalog.md)**  
Associate a portal with multiple catalogs. By default, Service Portal is associated with Service Catalog.
-   **[Associate a portal with a knowledge base](associate-portal-knowledge.md)**  
You can associate a portal with any knowledge base. Multiple knowledge bases can be associated with a portal.
-   **[Configure Agent Chat in a portal](configure-va-in-sp.md#)**  
Your end users can initiate and maintain an Agent Chat conversation in any portal page. Write a script to pass portal-specific data to Agent Chat. For example, pass the name of your knowledge base to a Virtual Agent conversation.

**Parent Topic:**[Configuring Service Portal](../concept/configuring-service-portal.md)

