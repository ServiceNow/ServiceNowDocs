---
title: NowWebTheme interface - Android
description: The NowWebTheme interface provides properties that enable you to override the colors used within web pages hosted on your ServiceNow instance in a native web view.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/cllent-mobile-api-reference/NowWebThemeAndroidInterface.html
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowWebTheme interface- Android

The NowWebTheme interface provides properties that enable you to override the colors used within web pages hosted on your ServiceNow instance in a native web view.

The NowWebTheme interface extends the NowUITheme interface and inherits the property **nowUIColoring**.

`val nowUIColoring: NowUIColoring?`

This property is used to reference color variables that NowWebTheme can use. For additional information on how to theme the UI, see [Use NowUIColoring to theme NowWebTheme and NowChatTheme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/mobsdk-and-color-theming.md) in the Mobile SDK Developer Guide - Android.

The default colors use the Coral theme.

<table id="nowUItheme-properties-table" class="parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

alertCritical0

</td><td>

Use for: -   error messages
-   snackbar background

Default value: \#F9C8CE

</td></tr><tr><td>

alertCritical3

</td><td>

Use for: -   error messages
-   snackbar border

Default value: \#E52239

</td></tr><tr><td>

alertPositive0

</td><td>

Use for: -   success messages
-   snackbar background

Default value: \#C7DCB5

</td></tr><tr><td>

alertPositive3

</td><td>

Use for: -   success messages
-   snackbar border

Default value: \#3E8600

</td></tr><tr><td>

alertWarning0

</td><td>

Use for: -   warning messages
-   snackbar background

Default value: \#ECE5BF

</td></tr><tr><td>

alertWarning3

</td><td>

Use for: -   warning messages
-   snackbar border

Default value: \#B29800

</td></tr><tr><td>

backgroundPrimary

</td><td>

Use for: -   card background
-   choice picker
-   input background
-   neutral background

Default value: \#FFFFFF

</td></tr><tr><td>

backgroundSecondary

</td><td>

Use for overflow menu background.Default value: \#F5F6F7

</td></tr><tr><td>

backgroundTertiaryActionable

</td><td>

Use for the background color for the topic dialog search and edit text.Default value: \#37444A

</td></tr><tr><td>

brand

</td><td>

Use for the header background in the toolbar and tables.Default value: \#032D42

</td></tr><tr><td>

notification

</td><td>

Use for new message indicator.Default value: \#E52239

</td></tr><tr><td>

primary

</td><td>

Use for:-   actionable text
-   button backgrounds

Default value: \#00566E

</td></tr><tr><td>

screenHeaderText

</td><td>

Use for text and icon elements with a fixed color that appear on top of the brand color \(screen header/toolbar\).Default value: \#FFFFFF

</td></tr><tr><td>

textActionable

</td><td>

Use for: -   highlighted background
-   text on action buttons

Default value: \#FFFFFF

</td></tr><tr><td>

textPrimary

</td><td>

Use for: -   alert dialog messages
-   card header text
-   chat bubble text
-   picture title and description
-   topic text

Default value: \#10171A

</td></tr><tr><td>

webPageThemeId

</td><td>

Sys\_id of the theme to apply to the ServiceNow web pages loaded by NowWeb. Default value: Configured default theme

Table: UX Theme \[sys\_ux\_theme\] table.

</td></tr><tr><td>

webPageThemeVariantId

</td><td>

Sys\_id of the theme variant to apply to the ServiceNow web pages loaded by NowWeb. Default value: Configured default theme variant

Table: UX Style \[sys\_ux\_style\] table.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/MobileSDKAndroidAPI.md)

