---
title: Configure logo, colors, and system defaults for Core UI
description: You can use the Basic Configuration Core UI module to brand your instance with your company logo and colors and set basic system defaults. This place is the best starting point if you are setting up your instance for the first time or if you have recently enabled Core UI.The La Jolla theme is the new brand theme for ServiceNow. When you upgrade to Madrid, your theme is automatically upgraded to the La Jolla theme. Any customizations you have made to the system theme will not be upgraded. Use the styles in the list below to upgrade or revert any styles to the new or old theme.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Customizing instance appearance, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Configure logo, colors, and system defaults for Core UI

You can use the Basic Configuration Core UI module to brand your instance with your company logo and colors and set basic system defaults. This place is the best starting point if you are setting up your instance for the first time or if you have recently enabled Core UI.

## Before you begin

Gather the following:

-   Obtain the company banner image to use in the header. The image can be high resolution, but when it displays it’s scaled based on the aspect ratio. It scales to a maximum of 20 px high.
-   Get the brand color hex or RGB numbers of your company, typically from your marketing department. Use them to decide how to configure the UI background colors.

Role required: admin

## About this task

Each color selection option provides a color picker to select a color. The text box beside the color picker lets you enter the value of the color as any of the following CSS formats:

-   Name: predefined color names, such as red, green, or blue
-   RGB decimal: RGB \(102, 153, 204\)
-   RGB hex: \#223344

Refer to [HTML Color Names \(W3CSchools\)](http://www.w3schools.com/tags/ref_colornames.asp) for information about HTML color names.

**Note:** This information is only applicable for instances that do not have Next Experience enabled. For theming information for Next Experience, see [Working with themes in Next Experience](../concept/next-experience-theming.md).

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Basic Configuration UI16**.

2.  Complete the configuration by changing any of the following settings:

<table id="table_n1g_xty_pt"><thead><tr><th>

Label

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Page header caption

</td><td>

glide.product.description

</td><td>

Change the text that appears next to your logo.

</td></tr><tr><td>

Browser tab title

</td><td>

glide.product.name

</td><td>

Change the text that appears on the browser tab.

</td></tr><tr><td>

System timezone for all users unless overridden in the user's record

</td><td>

glide.sys.default.tz

</td><td>

Select the time zone in the list.Select **Configure available time zones** to select the time zones that your users can select from in user preferences.

</td></tr><tr><td>

Banner image for Core UI

</td><td>

glide.product.image.light

</td><td>

Select **+** next to the image and upload your logo.

</td></tr><tr><td>

Date formatTime format

</td><td>

glide.sys.date\_formatglide.sys.time\_format

</td><td>

Select the date and time format from the choice lists.

</td></tr><tr><td>

Header background color

</td><td>

css.$navpage-header-bg

</td><td>

Select or enter the color.![Header background](../image/HeaderBGColor.png)

This color is also used as part of the theme preview on the Themes tab under system settings.

</td></tr><tr><td>

Banner text color

</td><td>

css.$navpage-header-color

</td><td>

Select or enter the color.![Banner text color](../image/BannerTextColor.png)

This color is also used as part of the theme preview on the Themes tab under system settings.

</td></tr><tr><td>

Header divider stripe color

</td><td>

css.$navpage-header-divider-color

</td><td>

Select or enter the color.![Header divider striper](../image/BannerDividerColor.png)

</td></tr><tr><td>

Navigation header/footer

</td><td>

css.$navpage-nav-bg

</td><td>

Select or enter the color. ![Navigation](../image/NavigationBGColor.png)

</td></tr><tr><td>

Navigation background expanded items

</td><td>

css.$subnav-background-color

</td><td>

Select or enter the color.![Application with expanded modules to show the difference in color](../image/ExpandedBackgroundColor.png)

</td></tr><tr><td>

Module text color for the Core UI application navigator

</td><td>

css.$navpage-nav-color-sub

</td><td>

Select or enter the color. ![Favorites, Connect list](../image/ModuleTextColor.png)

</td></tr><tr><td>

Navigation selected tab background color

</td><td>

css.$navpage-nav-selected-bg

</td><td>

Select or enter the color. ![Selected tab](../image/NavigationSelectedTabBGColor.png)

</td></tr><tr><td>

Navigation selected tab divider bar color

</td><td>

css.$nav-highlight-bar-active

</td><td>

![Application navigator with the All Applications tab selected and an arrow indicating the fact that the line under the tab is blue](../image/NavBarActive.png)

This color is also used as part of the theme preview on the Themes tab under system settings.

</td></tr><tr><td>

Navigation unselected tab divider bar color

</td><td>

css.$nav-highlight-bar-inactive

</td><td>

![Application navigator with the All Applications tab selected and an arrow point to the other tabs to indicate that the line is a different color](../image/NavBarInactive.png)

</td></tr><tr><td>

Navigation separator color

</td><td>

css.$nav-hr-color

</td><td>

Select or enter the color. ![Separators](../image/NavigationSeparatorColor.png)

</td></tr><tr><td>

Background for navigator and sidebars

</td><td>

css.$navpage-nav-bg-sub

</td><td>

Select or enter the color. ![Navigator, sidebars](../image/FavoritesConnectBGColor.png)

</td></tr><tr><td>

Currently selected Navigation tab icon color for Core UI

</td><td>

css.$navpage-nav-selected-color

</td><td>

Select or enter the color. ![Navigation icon](../image/NavigationIconColor.png)

</td></tr><tr><td>

Unselected navigation tab icon and favorite icons color

</td><td>

css.$navpage-nav-unselected-color

</td><td>

Select or enter the color.![Unselected favorites icon](../image/UnselectedNavIconColor.png)

</td></tr><tr><td>

Border color for Core UI

</td><td>

css.$navpage-nav-border

</td><td>

Select or enter the color. Also affects the border of the **Filter conversations** search box in the Connect Chat sidebar.![Filter navigator](../image/BorderColor.png)

</td></tr><tr><td>

Selected base theme

</td><td>

glide.ui.base\_theme.selected\_theme

</td><td>

Switches the main content \(everything other than the application navigator and the header\) between the La Jolla and Cobalt themes.

</td></tr></tbody>
</table>    For most of the settings, as you make changes, the page refreshes with a preview of the change. Only you see these changes. Some settings require you to log out and log back in again to see the change.

3.  Select **Save** at the top or bottom of the page.


## Result

After you save the configuration changes, all users who select the **System** theme in their UI personalization options see the new configuration colors.

**Parent Topic:**[Customizing instance appearance](../reference/customizing-instance-appearance.md)

## La Jolla and cobalt theme comparison

The La Jolla theme is the new brand theme for ServiceNow. When you upgrade to Madrid, your theme is automatically upgraded to the La Jolla theme. Any customizations you have made to the system theme will not be upgraded. Use the styles in the list below to upgrade or revert any styles to the new or old theme.

Make changes to any of these styles by navigating to **System Properties** &gt; **Basic Configuration UI16**.

<table id="table_jhh_yv5_yfb"><thead><tr><th>

Property

</th><th>

La Jolla style

</th><th>

Cobalt style

</th></tr></thead><tbody><tr><td>

Header background color css.$navpage-header-bg

</td><td>

\#ffffff

</td><td>

\#303a46

</td></tr><tr><td>

Header divider stripe color css.$navpage-header-divider-color

</td><td>

\#5a7f71

</td><td>

\#455464

</td></tr><tr><td>

Navigation header/footer css.$navpage-nav-bg

</td><td>

\#293e40

</td><td>

\#303A46

</td></tr><tr><td>

Navigation background expanded itemscss.$subnav-background-color

</td><td>

\#213234

</td><td>

\#303a46

</td></tr><tr><td>

Module text color for UI16 css.$navpage-nav-color-sub

</td><td>

\#bec1c6

</td><td>

\#bec1c6

</td></tr><tr><td>

Navigation selected tab background colorcss.$navpage-nav-selected-bg

</td><td>

\#2f4fe

</td><td>

\#4b545f

</td></tr><tr><td>

Navigation selected tab divider bar colorcss.$nav-highlight-bar-active

</td><td>

\#82c9b8

</td><td>

\#278efc

</td></tr><tr><td>

Navigation unselected tab divider bar colorcss.$nav-highlight-bar-inactive

</td><td>

\#213234

</td><td>

\#81878e

</td></tr><tr><td>

Navigation separator color css.$nav-hr-color

</td><td>

\#293e40

</td><td>

\#303a46

</td></tr><tr><td>

Background for navigator and sidebarscss.$navpage-nav-bg-sub

</td><td>

\#293e40

</td><td>

\#455464

</td></tr><tr><td>

Currently selected Navigation tab icon color for UI16 css.$navpage-nav-selected-color

</td><td>

\#82c9b8

</td><td>

\#ffffff

</td></tr><tr><td>

Unselected navigation tab icon and favorite icons color css.$navpage-nav-unselected-color

</td><td>

\#bec1c6

</td><td>

\#bec1c6

</td></tr><tr><td>

Border color for UI16 css.$navpage-nav-border

</td><td>

\#7a828a

</td><td>

\#ddd

</td></tr><tr><td>

Selected Base Themeglide.ui.base\_theme.selected\_theme

</td><td>

La Jolla SysID: c92c1ee153002300dda1ddeeff7b125b

</td><td>

Cobalt SysID: 6f3c9ae153002300dda1ddeeff7b124a

</td></tr></tbody>
</table>