---
title: Configure Engagement Messenger
description: Create a Engagement Messenger module and configure its behavior, appearance, and styling. By creating a messenger module, you can customize the appearance and behavior according to your organizational branding and to suit your customer needs.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Set up Engagement Messenger, Enable communication channels, Configure, Customer Service Management]
---

# Configure Engagement Messenger

Create a Engagement Messenger module and configure its behavior, appearance, and styling. By creating a messenger module, you can customize the appearance and behavior according to your organizational branding and to suit your customer needs.

## Before you begin

-   [Install the Engagement Messenger application](install-engagement-center-app.md).
-   Gather or prepare the following items:
    -   Image files for your logo and messenger launcher icon. The images must be in .jpg, .png, .bmp, .gif, .jpeg, .ico, or .svg file format.
    -   Color names and hex codes for branding to configure the styling of the messenger user interface.
-   Role required: sn\_csm\_ec.ec\_admin

## Procedure

1.  Navigate to **All** &gt; **Engagement Messenger** &gt; **Modules**.

2.  Choose to create an Engagement Messenger module or edit an existing module.

    -   To create a module, select **New**.
    -   To edit an existing module, select **Edit** in the Edit module column of your messenger module.
    The guided configuration view is displayed.

3.  In the guided configuration view, navigate through Module, Appearance, Behavior, Features, and Implement.

4.  On the form, fill in the fields.

<table id="table_mxg_gyz_m4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Module

</td></tr><tr><td>

Module name

</td><td>

Unique name for your messenger module.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the messenger module.

</td></tr><tr><td class="sub-head" colspan="2">

Appearance

</td></tr><tr><td>

Logo

</td><td>

Logo that is displayed in the header of the messenger on your website.

 The recommended size and dimensions are:

-   Size \(in bytes\): approximately equal to 2 KB
-   Height \(in pixels\): 30–55
-   Width \(in pixels\): 30–55
 **Note:** If no logo is selected, the Home icon \(![Home icon.](../image/home-icon.png)\) is displayed as a default logo in the header of the messenger.

</td></tr><tr><td>

Launcher icon

</td><td>

Icon that is displayed as the messenger option on your website. On your website, selecting this icon launches the messenger.

The recommended size and dimensions are: -   Size \(in bytes\): approximately equal to 1 KB
-   Height \(in pixels\): 24–60
-   Width \(in pixels\): 24–60
-   Use a circular icon with a transparent background
 **Note:** The grid size range of a launcher icon is from 24X24 to 60X60. Any deviation from the defined range rescales automatically to fit the launcher icon size.

</td></tr><tr><td>

Launch icon position

</td><td>

Position of the messenger launch icon on your website.

</td></tr><tr><td>

Allow module to expand to full-height

</td><td>

Option for enabling the messenger module to expand to the full height of the browser tab.

</td></tr><tr><td>

Horizontal margin \(in pixels\)

</td><td>

Distance from the right or left of the browser tab for the placement of the messenger launcher icon.

 The distance is calculated from right or left based on your input for the field **Launch icon position**.

 For example, if you set the launch icon position as **Right** and the **Horizontal offset** as **50**, then the launch icon is placed at a distance of 50 px from the right of the browser tab.

 The maximum value for this field is 70 px.

</td></tr><tr><td>

Vertical margin \(in pixels\)

</td><td>

Distance from the bottom of the browser tab for the placement of the messenger launch icon.

 The maximum value for this field is 70 px.

</td></tr><tr><td>

Primary color

</td><td>

Primary color for styling the header or buttons in your messenger.

 For example, this color is used for user action buttons such as the **Submit**, **Yes**, or **OK**.

</td></tr><tr><td>

Primary font color

</td><td>

Text color that is used on UI elements that use the primary color.

</td></tr><tr><td>

Secondary color

</td><td>

Secondary color for styling your messenger.

 For example, this color is used for user action buttons such as **Cancel** or **No**.

</td></tr><tr><td>

Secondary font color

</td><td>

Text color that is used on UI elements that use the secondary color.

</td></tr><tr><td>

Tertiary color

</td><td>

Tertiary color for styling your messenger.

 For example, this color is used to mark customer cases with tags such as **Action required**.

</td></tr><tr><td>

Tertiary font color

</td><td>

Text color that is used on UI elements that use the tertiary color.

</td></tr><tr><td>

Theme

</td><td>

Theme for other styling options of the messenger.

 This field is automatically set to **CWF Engagement Messenger Theme**.

 If you want to select a different theme, ensure that the theme that you select here must match certain criteria. For more information, see [Engagement Messenger module theme requirements](../reference/engagement-messenger-theme-requirements.md).

</td></tr><tr><td colspan="2">

**Note:** If the value for the **Primary color**, **Secondary color**, or **Tertiary color** fields is set to color names, such as **Pink**, the Engagement Messenger UI doesn’t display these colors correctly. As a workaround, you can enter the hexadecimal values of these colors. For example, use \#FFC0CB for **Pink**.

</td></tr><tr><td class="sub-head" colspan="2">

Behavior

</td></tr><tr><td class="sub-head" colspan="2">

Notification

</td></tr><tr><td>

Enable notifications on launcher icon

</td><td>

Option to enable in-app pop-up notification alert message when a new message is received.

</td></tr><tr><td>

Enable sounds

</td><td>

Option to get the notification alert sound.

</td></tr><tr><td>

Enable notifications in browser tab

</td><td>

Option to get the notification alert on the browser tab when the concerned web page isn’t opened.

</td></tr><tr><td>

Enable user behavior tracking

</td><td>

Option for enabling the collection of user experience analytics from users of your Engagement Messenger.

 This option is available only if you activate the Service Portal Analytics plugin \(com.glide.service-portal.analytics\) in your ServiceNow instance.

 **Note:** If you update your Engagement Messenger module name after user behavior tracking is enabled, the User Experience Analytics dashboard would show the original module name, not the updated name.

</td></tr><tr><td colspan="2">

As an administrator, you can configure the Proactive Recommendations feature for Engagement Messenger. For more information, see [Proactive Recommendations configuration for Engagement Messenger](../reference/em-behav-recom.md).

</td></tr><tr><td class="sub-head" colspan="2">

Features

</td></tr><tr><td colspan="2">

See [Feature configuration for Engagement Messenger](configure-features-of-engagement-messenger.md).

</td></tr><tr><td class="sub-head" colspan="2">

Implement

</td></tr><tr><td>

Website URLs

</td><td>

Comma-separated list of URLs of the websites where you want to deploy the messenger.For example, `https://www.example.com, https://www.yourwebsiteurl.com`

</td></tr><tr><td>

Authentication type

</td><td>

Authentication type for this embedded messenger. Select one of the following options:

-   None
-   Security assertion markup language \(SAML\)-based
-   Open ID connect \(OIDC\)-based
 If you want to enable only the guest user experience for the messenger in your website, set this field to **None**.

 Ensure that you create an identity provider \(IdP\) for the authentication type you select in this field. For more information, see [Create an identity provider \(IdP\) for Engagement Messenger](../concept/create-identity-providers-for-engagement-messenger.md).

</td></tr><tr><td class="sub-head" colspan="2">

Advanced branding

</td></tr><tr><td>

Hyperlink text color

</td><td>

Text color used for hyperlinks in messenger.

</td></tr><tr><td>

Navigate-back icon

</td><td>

The icon appears in the messenger header that enables the user to navigate to the previous page. The icon size is 24X24.

</td></tr><tr><td>

Close icon

</td><td>

This icon appears in the messenger header that enables the user to close messenger. The icon size is 16X16.

</td></tr><tr><td>

List search icon

</td><td>

The icon appears in the messenger header that enables searching through a list. The icon size is 16X16.

</td></tr><tr><td>

Expand icon

</td><td>

The icon appears in the header that enables the user to expand the messenger to access information. The icon size is 16X16.

</td></tr><tr><td>

Collapse icon

</td><td>

The icon appears in the messenger header that enables the user to collapse an expanded messenger. The icon size is 16X16.

</td></tr><tr><td>

Start-chat icon

</td><td>

The icon appears in the messenger header that enables the user to start a chat with an agent regarding their ticket or technician visit. The icon size is 16X16.

</td></tr><tr><td>

Filter menu icon

</td><td>

The icon appears at the top of the list page that enables the user to apply filters to get desired result. The icon size is 24X24.

</td></tr><tr><td>

Applied-filters icon

</td><td>

The icon appears at the top of the list page and shows applied filters icon in messenger. The icon size is 24X24.

</td></tr><tr><td colspan="2">

**Note:** The advanced branding configuration is only available in the form view.

</td></tr></tbody>
</table>5.  Select **Save**.

6.  Select **Email instructions** to notify your security administrator to complete the following tasks:

    1.  [Create an identity provider \(IdP\) for Engagement Messenger](../concept/create-identity-providers-for-engagement-messenger.md).
    2.  [Configure a CORS rule for Engagement Messenger](create-cors-for-rest-api-ec.md).
    3.  [Create HTTP response headers for Engagement Messenger](create-http-response-headers-for-ec.md).
    **Note:** Engagement Messenger extends service portal capabilities that don’t support domain separation. For more information, see [Domain separation and Service Portal](https://www.servicenow.com/docs/access?context=domain-separation-service-portal&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US). However, other tables that are used in Engagement Messenger may support domain separation according to the configurations with which they're created.


## Result

A new messenger configuration is created and listed in the Modules module of the Engagement Messenger application.

## What to do next

1.  [Engagement Messenger properties](../reference/additional-config-for-engagement-messenger.md).
2.  [configure the features of Engagement Messenger](configure-features-of-engagement-messenger.md).
3.  Share the messenger module code with your developer using the **Email code** to embed Engagement Messenger in your website.
4.  Following are the advanced formatting changes that are available as an optional configuration in Engagement Messenger:
    -   [Engagement Messenger module theme requirements](../reference/engagement-messenger-theme-requirements.md) to reuse Service Portal theme to customize the visual appearance in Engagement Messenger.
    -   [Default font sizes for search result text in Engagement Messenger](modify-search-result-font-size-auto-spell-correction-text.md).

