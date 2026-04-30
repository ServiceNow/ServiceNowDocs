---
title: Create a branded landing page for single instances
description: Create a branded pre-login landing page with a ServiceNow mobile login button or mobile deep links. These elements redirect users either to a specific area within the ServiceNow mobile app or to the login screen.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-25"
reading_time_minutes: 4
breadcrumb: [Branded landing page, Mobile instances, Configuring the Mobile Platform, Mobile Platform]
---

# Create a branded landing page for single instances

Create a branded pre-login landing page with a ServiceNow mobile login button or mobile deep links. These elements redirect users either to a specific area within the ServiceNow mobile app or to the login screen.

## Before you begin

Role required: admin

## About this task

A branded landing page is a public web page displayed to users before they log in to their ServiceNow mobile app. This pre-login page contains a login button or a deep link that navigates users to a specified area of a ServiceNow mobile app, bypassing the need to select an instance. The login button can be configured as part of the header in the mobile app, as an integral element embedded directly within the web page itself or both these options.

The default is for the login button to be contained within the header, however you can override this option by adding a line within the JSON script. In this case, you must create a button that will be an integral part of your web page. For more information, see [Deep linking for mobile](../concept/deep-link-mobile.md).

**Note:** This feature is supported from ServiceNow mobile app version 19.0 and earlier.

**Note:** For the Xanadu version and earlier, this functionality is supported using the property **sys\_extension\_point** with the API name global.CustomPreAuthProperties. From Yokohama, you can use the **preLoginLandingPage** property and remove the property **sys\_extension\_point** with the API name global.CustomPreAuthProperties from the existing script.

The **sys\_extension\_point** with the API name global.CustomPreAuthProperties still works in the Yokohama version, even if the **preLoginLandingPage** property isn’t defined. However, if both properties are defined, the property **preLoginLandingPage** takes precedence. For more information about creating a branded landing page in the Xanadu version and earlier, see [Configure advanced app allowance with links to permitted apps](config-advanced-app-allow.md).

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

    The Mobile Properties list displays.

2.  Select **New** to create a mobile property record.

3.  Enter the name `preLoginLandingPage` in the **Name** field.

4.  Select **JSON** in the **Type** field.

5.  In the **Value** field, enter the URL to be displayed to the user.

    Enter the following script, `{“url”:”<URL>”}`

    For example, the script would look as follows when using the ServiceNow home page: `{“url”:”https://www.servicenow.com/”}`

    **Note:** The URL must be a publicly accessible web page. These URLs include both ServiceNow and non-ServiceNow domains.

6.  To configure a different button label name other than the default name, Log in, do the following.

    1.  In the **Value** field, enter the following script after the landing page URL, `“loginLabelTranslationKey”:”<button label key>”`

    2.  Copy one of the following predefined button label keys:

    **Note:** The predefined button key is translated according to the users preferred language settings on the app.

    |Predefined button label key|Displayed button label name|
    |---------------------------|---------------------------|
    |`login_label_txt`|Log in|
    |`sign_in_label_txt`|Sign in|
    |`enter_label_txt`|Enter|
    |`access_account_label_txt`|Access account|
    |`continue_label_txt`|Continue|
    |`get_started_label_txt`|Get started|
    |`proceed_label_txt`|Proceed|

    For example, the script would look as follows when using the ServiceNow home page with a button labeled Access account:`{“url”:” https://www.servicenow.com/”,“loginLabelTranslationKey”:”access_account_label_txt”}`

7.  To override the option to display the login button in the header enter the following text `“hideHeaderLoginButton”:true`, as shown in the example.

    ```
    { 
    "url": "https://url.com”,
    "loginLabelTranslationKey": 
    "login_label_txt", "hideHeaderLoginButton": "true"
     }
    ```

    **Note:** As the login button is not displayed in the header, you must create a login button to be an integral part of your webpage. For more information, see [Deep linking for mobile](../concept/deep-link-mobile.md).

8.  Select the **Active** field if you want this mobile property to be active.

9.  Select the **Is Public** check box to make the web page available for public access.

    **Note:** The **Mobile App Config** field disappears when you select the **Is Public** option.

10. In the **Mobile Application** field, select which mobile apps are to display the branded landing page.

    Enter either `Agent`, `Request`, or the name of a custom app type created by users of Mobile Publishing. Leave the field empty to display the same branded landing page for all supported app types or variants.

    **Note:** You can define the **preLoginLandingPage** property for different mobile apps, by creating additional mobile property records for each of the mobile apps. In each of these different **preLoginLandingPage** property records, you define specific values according to the requirement of each app.

11. Select **Submit**.


## What to do next

You may want to change the login page to be compatible with the style of the branded landing page. For more information, see [Publish mobile apps with custom branding](../concept/mobile-publishing.md) and [Next Experience theming for mobile](../concept/explore-ne-theming.md).

For more information on using deep links, see [Navigation links within a branded landing page](../reference/branded-landing-page-links.md) and [Deep linking for mobile](../concept/deep-link-mobile.md).

