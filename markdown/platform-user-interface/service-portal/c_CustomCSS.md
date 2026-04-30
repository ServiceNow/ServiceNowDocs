---
title: Create a portal theme
description: If you need more customization than Branding Editor can provide, you can create your own custom theme.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Defining portal styles, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Create a portal theme

If you need more customization than Branding Editor can provide, you can create your own custom theme.

Only users with an understanding of CSS should create custom themes.

1.  Navigate to **Service Portal** &gt; **Themes**, then select **New**.
2.  Complete the form fields and then from the form context menu, select **Save**.

<table id="table_anh_ljr_mz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your theme. Use this name to associate the theme with your portal. This name is not visible to users, you should know it to apply the correct theme to a portal.

</td></tr><tr><td>

Turn off SCSS compilation

</td><td>

Turns off compiling SCSS and sends the plain CSS file directly to the client.

</td></tr><tr><td>

Application

</td><td>

The record scope. The header menu record and the source table must have the same application scope.

</td></tr><tr><td>

Header

</td><td>

List of headers and footers from the sp\_header\_footer table that you can associate with a portal theme. Headers and footers are widgets and can be configured the same way.

</td></tr><tr><td>

Footer

</td><td>

List of headers and footers from the sp\_header\_footer table that you can associate with a portal theme.

</td></tr><tr><td>

Fixed header

</td><td>

Locks the header at the top of the page so that when a user scrolls the header remains on the screen.

</td></tr><tr><td>

Fixed footer

</td><td>

Locks the footer at the bottom of the page so that when a user scrolls the footer remains on the screen.

</td></tr><tr><td>

CSS variables

</td><td>

CSS custom properties that you can use to change the color and styles in a portal. For example, the stock theme uses some of the following variables:```
$sp-logo-margin-x: 		15px !default;
$sp-tagline-color:		$text-color !default;
$navbar-inverse-bg: 	#3a3f51 !default;
```

 **Note:** Use the CSS variables field to define CSS variables only. Use CSS Includes to define CSS rules. As of the Madrid release, Sass and LESS can be used within CSS Includes.

</td></tr></tbody>
</table>3.  To add a style sheet to the theme, in the **CSS Include** related list, select **New**.
4.  Complete the style sheet form fields and select **Submit**.

<table id="table_ew1_jjr_mz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the CSS Include. Remember this name to associate the CSS Include with the theme.

</td></tr><tr><td>

Application

</td><td>

The record scope. The header menu record and the source table must have the same application scope.

</td></tr><tr><td>

Source

</td><td>

Select one of the following options:-   **Style Sheet**: Add an internal style sheet that has been uploaded to the CSS table \[sp\_css\]. For example, ng-sortable.min.css. Internal style sheets use standard CSS in the CSS field.
-   **URL**: Link to an external style sheet. Use external style sheets to use the same CSS as a corporate website or other online resource.


</td></tr><tr><td>

Style sheet

</td><td>

An internal style sheet to associate with the theme.

</td></tr><tr><td>

CSS file URL

</td><td>

A URL to an external style sheet to associate with the theme.

</td></tr><tr><td>

Lazy Load

</td><td>

Option to load the CSS Include asynchronously to improve page load time. This option should be set to the same value for all CSS Includes of a theme. Enabling asynchronous loading for only some CSS Includes associated with a theme isn’t recommended.

 **Note:** Enabling **Lazy Load** isn’t recommended for portals with flashing of unstyled content.

 The CSS Includes with **Lazy Load** enabled are listed in the **Lazy load CSS includes** related list in the theme record.

</td></tr><tr><td>

RTL CSS file URL

</td><td>

A URL to an external style sheet for mirroring the direction of a portal when the session language is a right-to-left language, such as Hebrew.

 For information about support for right-to-left languages, see [Styling for right-to-left languages in portals](styling-right-to-left-languages.md).

</td></tr></tbody>
</table>5.  To add a JavaScript include to the theme, in the **JS Include** related list, select **New**.
6.  Complete the JS Include form fields and select **Submit**.

<table id="table_d4l_1bn_b1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the JS Include. Remember this name to associate the JS Include with the theme.

</td></tr><tr><td>

Application

</td><td>

The record scope. The header menu record and the source table must have the same application scope.

</td></tr><tr><td>

Source

</td><td>

Select one of the following options:-   **UI Script**: Add an internal UI script that has been uploaded to the UI script table \[sys\_ui\_script\]. UI scripts allow you to create client-side JavaScript and reuse it in multiple locations. For more information on UI scripts, see [UI scripts](https://www.servicenow.com/docs/access?context=c_UIScripts&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).
-   **URL**: Link to an external JavaScript file. Use external URLs to use the same JavaScript as a corporate website or other online resource.


</td></tr><tr><td>

UI Script or JS file URL

</td><td>

Associate an internal UI script or JavaScript file URL, depending on which option you select in the Source field.

</td></tr><tr><td>

Updated

</td><td>

Date and time that the JS Include was last updated

</td></tr><tr><td>

Package

</td><td>

The Service Portal package that the JS include is associated with. For example, Service Portal Configuration Pages. This field is populated by default.

</td></tr></tbody>
</table>
**Parent Topic:**[Defining portal styles](portal-css.md)

