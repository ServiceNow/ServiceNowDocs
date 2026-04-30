---
title: NowWebTheme interface - Android
description: The NowWebTheme interface provides properties that enable you to override the colors used within web pages hosted on your ServiceNow instance in a native web view.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowWebTheme interface - Android

The NowWebTheme interface provides properties that enable you to override the colors used within web pages hosted on your ServiceNow instance in a native web view.

The NowWebTheme interface extends the NowUITheme interface and inherits the property **nowUIColoring**.

`val nowUIColoring: NowUIColoring?`

This property is used to reference color variables that NowWebTheme can use. For additional information on how to theme the UI, see [Use NowUIColoring to theme NowWebTheme and NowChatTheme](../../../../../../integrate/guides/mobile_sdk/mobile_sdk-android/reference/mobsdk-and-color-theming.md) in the Mobile SDK Developer Guide - Android.

<table id="id_mbs_ryc_pzb" class="parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

alertCritical0

</td><td>

Use for: -   error messages
-   snackbar background

Default value: \#F8C8CD

</td></tr><tr><td>

alertCritical3

</td><td>

Use for: -   error messages
-   snackbar border

Default value: \#B61C2D

</td></tr><tr><td>

alertPositive0

</td><td>

Use for: -   success messages
-   snackbar background

Default value: \#CADFC0

</td></tr><tr><td>

alertPositive3

</td><td>

Use for: -   success messages
-   snackbar border

Default value: \#266108

</td></tr><tr><td>

alertWarning0

</td><td>

Use for: -   warning messages
-   snackbar background

Default value: \#FBF7BF

</td></tr><tr><td>

alertWarning3

</td><td>

Use for: -   warning messages
-   snackbar border

Default value: \#B6AA00

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

Use for overflow menu background.Default value: \#F6F6F8

</td></tr><tr><td>

backgroundTertiaryActionable

</td><td>

Use for the background color for the topic dialog search and edit text.Default value: \#454D5B

</td></tr><tr><td>

brand

</td><td>

Use for the header background in the toolbar and tables.Default value: \#302F4B

</td></tr><tr><td>

notification

</td><td>

Use for new message indicator.Default value: \#B61C2D

</td></tr><tr><td>

primary

</td><td>

Use for:-   actionable text
-   button backgrounds

Default value: \#4F52BD

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

Default value: \#151920

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
</table>**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

