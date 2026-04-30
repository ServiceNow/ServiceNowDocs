---
title: Customizing instance appearance
description: An administrator can change global CSS or system properties to alter the look and feel of the default instance interface. Functionality is not affected.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Customizing instance appearance

An administrator can change global CSS or system properties to alter the look and feel of the default instance interface. Functionality is not affected.

For example, organizations often use multiple instances to separate development, testing, and production activities. To help users avoid accidentally changing the wrong instance, administrators can configure each with a visually distinct theme. Several approaches are available for defining an instance theme.

## CSS Properties

Navigate to **System Properties** &gt; **CSS**.

The following properties are available through CSS Properties.

**Note:** Colors are specified using predefined [color names](https://www.w3schools.com/css/css_colors.asp), RGB decimals, or RGB hexadecimals.

-   Banner text color
-   Banner and list caption background color
-   Font used in forms and lists \(this is a global font setting\)
-   Button styles \(background color, border color, border width, text color\)
-   Field status indicator colors \(including the indicators for Changed, Mandatory Populated, Mandatory Unpopulated, and Read-only\)
-   List cell vertical alignment
-   Navigator menu styles \(text font size, background color, text color\)
-   Header font name and size
-   List and form caption color override
-   Global text search background color \(both for catalog results and knowledge base results\)

## UI properties

Navigate to **System Properties** &gt; **UI Properties**.

The following properties are available through UI Properties.

-   Icons used in the activity formatter
-   Background colors for Additional Comments and Work Notes
-   Button placement on forms
-   Icons used in the Task Activity formatter
-   Background colors for Incident Additional Comments and Work Notes

## CSS class support

In Core UI \(UI16\), CSS properties and how they affect the platform UI change depending on the release.

<table id="table_xxt_5bk_11b"><thead><tr><th>

CSS class

</th><th>

Description

</th><th>

How to configure

</th><th>

Affected area

</th></tr></thead><tbody><tr><td>

$navpage-header-bg

</td><td>

Header background color

</td><td>

Navigate to **System Properties** &gt; **Basic Configuration UI16** &gt; **Header background color**

</td><td>

![Header background](../image/HeaderBGColor.png)

</td></tr><tr><td>

$navpage-header-color

</td><td>

Color for header text and the global search icon

</td><td>

Navigate to **System Properties** &gt; **Basic Configuration UI16** &gt; **Banner text color**

</td><td>

![Banner text color](../image/BannerTextColor.png)

</td></tr><tr><td>

$navpage-header-button-color

</td><td>

Color for logged in user name text, and the global search Connect, Help, and settings icons

</td><td>

Add the CSS property to the CSS field of a theme. For more information, see [Create or customize a theme](../task/t_CreateOrCustomizeATheme.md).

</td><td>

![Header with User name and Connect, Help, and settings icons highlighted](../image/HeaderButtonColor.png)

</td></tr><tr><td>

$navpage-header-divider-color

</td><td>

Header divider color

</td><td>

Navigate to **System Properties** &gt; **Basic Configuration UI16** &gt; **Header divider stripe color**

</td><td>

![Header divider striper](../image/BannerDividerColor.png)

</td></tr><tr><td>

$navpage-button-color

</td><td>

Color for the following icons in the sidebars-   Expand/collapse
-   Create a conversation \(in the Connect sidebar\)
-   Open Connect workspace

</td><td>

Add the CSS property to the CSS field of a theme. For more information, see [Create or customize a theme](../task/t_CreateOrCustomizeATheme.md).

</td><td>

![Connect sidebar with arrow pointing to the plus icon](../image/ButtonColor.png)

</td></tr><tr><td>

$navpage-button-color-hover

</td><td>

Color for the following icons when a user points to the control:-   Global search
-   Help
-   Settings
-   Clear text icon in the navigation filter

</td><td>

Add the CSS property to the CSS field of a theme. For more information, see [Create or customize a theme](../task/t_CreateOrCustomizeATheme.md).

</td><td>

![Point to the Help icon to show that it is blue when a user points to it](../image/ButtonHoverColor.png)![Point to Clear option in the Application Navigator to show that it is also blue on point to](../image/ButtonColorHover2.png)

</td></tr><tr><td>

$search-text-color

</td><td>

Color of the search text, both in the navigation filter and the global search fields

</td><td>

Add the CSS property to the CSS field of a theme. For more information, see [Create or customize a theme](../task/t_CreateOrCustomizeATheme.md).

</td><td>

![Search in application navigator showing "incident" in white](../image/SearchTextColor.png)

</td></tr><tr><td>

$navpage-nav-border

</td><td>

Border color for the navigation filter and the conversation filter

</td><td>

Navigate to **System Properties** &gt; **Basic Configuration UI16** &gt; **Border color for UI16**

</td><td>

![Filter navigator](../image/BorderColor.png)

</td></tr><tr><td>

$nav-highlight-main

</td><td>

Highlights the module after the user has clicked it. In the Connect workspace, highlights the selected conversation.

</td><td>

Add the CSS property to the CSS field of a theme. For more information, see [Create or customize a theme](../task/t_CreateOrCustomizeATheme.md).

</td><td>

![Selected conversation in the Connect Workspace showing the correct color](../image/HighlightMain.png)

</td></tr><tr><td>

$subnav-background-color

</td><td>

Background for expanded navigation items

</td><td>

Navigate to **System Properties** &gt; **Basic Configuration UI16** &gt; **Navigation background expanded items**

</td><td>

![Application with expanded modules to show the difference in color](../image/ExpandedBackgroundColor.png)

</td></tr><tr><td>

$navpage-nav-bg

</td><td>

Header and footer for navigator and sidebars.

</td><td>

Navigate to **System Properties** &gt; **Basic Configuration UI16** &gt; **Navigation header/footer**

</td><td>

![Navigation](../image/NavigationBGColor.png)

</td></tr><tr><td>

$navpage-nav-bg-sub

</td><td>

Background for navigator and sidebars

</td><td>

Navigate to **System Properties** &gt; **Basic Configuration UI16** &gt; **Background for navigators and sidebars**

</td><td>

![Navigator, sidebars](../image/FavoritesConnectBGColor.png)

</td></tr><tr><td>

$navpage-nav-color-sub

</td><td>

Text color for modules in the main navigation

</td><td>

Add the CSS property to the CSS field of a theme. For more information, see [Create or customize a theme](../task/t_CreateOrCustomizeATheme.md).

</td><td>

![Application navigator with Incident open and the modules beneath incident showing the text color is white](../image/NavColorSub.png)

</td></tr><tr><td>

$navpage-nav-mod-text-hover

</td><td>

Text color when hovering over items in the main navigation

</td><td>

Not supported

</td><td>

Not supported

</td></tr><tr><td>

$nav-hr-color

</td><td>

Navigator separator color

</td><td>

Navigate to **System Properties** &gt; **Basic Configuration UI16** &gt; **Navigation separator color**

</td><td>

![Separators](../image/NavigationSeparatorColor.png)

</td></tr><tr><td>

$nav-highlight-bar-active

</td><td>

Line under the active tab in the application navigator. This color is also used as part of the theme preview on the Themes tab under system settings.

</td><td>

Navigate to **System Properties** &gt; **Basic Configuration UI16** &gt; **Navigation selected tab divider bar color**

</td><td>

![Application navigator with the All Applications tab selected and an arrow indicating the fact that the line under the tab is blue](../image/NavBarActive.png)

</td></tr><tr><td>

$nav-highlight-bar-inactive

</td><td>

Line under the inactive tabs in the application navigator

</td><td>

Navigate to **System Properties** &gt; **Basic Configuration UI16** &gt; **Navigation unselected tab divider bar color**

</td><td>

![Application navigator with the All Applications tab selected and an arrow point to the other tabs to indicate that the line is a different color](../image/NavBarInactive.png)

</td></tr><tr><td>

$navpage-nav-selected-bg

</td><td>

Navigation selected tab background color

</td><td>

Navigate to **System Properties** &gt; **Basic Configuration UI16** &gt; **Navigation selected tab background color**

</td><td>

![Selected tab](../image/NavigationSelectedTabBGColor.png)

</td></tr><tr><td>

$navpage-nav-selected-color

</td><td>

Currently selected Navigation tab icon color

</td><td>

Navigate to **System Properties** &gt; **Basic Configuration UI16** &gt; **Currently selected Navigation tab color for UI16**

</td><td>

![Navigation icon](../image/NavigationIconColor.png)

</td></tr><tr><td>

$navpage-nav-unselected-color

</td><td>

Unselected navigation tab icon and favorite icons color

</td><td>

Navigate to **System Properties** &gt; **Basic Configuration UI16** &gt; **Unselected navigation tab icon and favorite icons color**

</td><td>

![Favorite icon color](../image/UnselectedNavIconColor.png)

</td></tr><tr><td>

$connect-latest-message

</td><td>

Color of the currently selected message in Connect

</td><td>

Add the CSS property to the CSS field of a theme. For more information, see [Create or customize a theme](../task/t_CreateOrCustomizeATheme.md).

</td><td>

![Connect sidebar with selected message pointed out by arrow](../image/LatestMessageColor.png)

</td></tr><tr><td>

$nav-timeago-header-color

</td><td>

Timestamp header backgrounds in History tab

</td><td>

Not supported

</td><td>

Not supported

</td></tr><tr><td>

$navpage-nav-app-text

</td><td>

Core content text color for items such as applications and the empty state text for the Connect sidebar.

</td><td>

Add the CSS property to the CSS field of a theme. For more information, see [Create or customize a theme](../task/t_CreateOrCustomizeATheme.md).

</td><td>

![Application navigator with arrow pointing at Service Desk to show that the text is white](../image/MainNavText.png)

</td></tr><tr><td>

$navpage-nav-app-text-hover

</td><td>

Text color for a selected module

</td><td>

Add the CSS property to the CSS field of a theme. For more information, see [Create or customize a theme](../task/t_CreateOrCustomizeATheme.md).

</td><td>

![Incidents > Open module selected to show the selected color](../image/SelectedModuleTextColor.png)

</td></tr></tbody>
</table>-   **[Configure logo, colors, and system defaults for Core UI](../task/t_ConfigureLogoColorsSysDfltsUI16.md#)**  
You can use the Basic Configuration Core UI module to brand your instance with your company logo and colors and set basic system defaults. This place is the best starting point if you are setting up your instance for the first time or if you have recently enabled Core UI.
-   **[Select a theme in Core UI](../task/t_SelectATheme.md)**  
You can switch between different themes for the user interface.
-   **[Customize menu categories](../task/customize-menu-categories.md)**  
Use menu categories to apply CSS styles to application labels.
-   **[Change survey question header colors](../task/t_ChangeSurveyQuesHeaderColors.md)**  
The Classic Environment uses a header color from the base color, which allows theming from CSS properties.
-   **[CSS theme support](../concept/c_CSSThemeSupport.md)**  
Themes give the user interface a specific look and feel by using different color combinations.

**Parent Topic:**[User interface configuration](../../core-configuration/concept/p_NavigationAndUIConfiguration.md)

