---
title: Request a new branded iOS app for public distribution
description: Request, test, and publish a custom iOS app that has your unique company identity. Then make the app available for public distribution on the Apple store.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Request, test, and publish a branded mobile app, Publish mobile apps with custom branding, Configuring the Mobile Platform, Mobile Platform]
---

# Request a new branded iOS app for public distribution

Request, test, and publish a custom iOS app that has your unique company identity. Then make the app available for public distribution on the Apple store.

## Before you begin

Role required: admin

## About this task

Mobile Publishing enables you to request a new branded iOS app that can be distributed on the public Apple Store. After you complete the request form, your ServiceNow® instance builds the app and provides a link from where you can download an XCode archive file \(`.xcarchive`\). Then you download the XCode archive file, update it, and re-sign it to generate an iOS application archive file \(`.ipa`\). After the `.ipa` file is generated, you upload it to Apple Connect for testing. When testing is completed, you approve the build and can deploy your branded app with the public Apple Store.

**Note:** Publicly distributed iOS app builds take one week from submission to be ready for testing. ServiceNow can't expedite this time line because it's determined by Apple.

Images that do not follow the guidelines listed below might appear cut off in your branded app, as shown in this example.

![Example icon with cut off logo and text](../image/cut-off-icon.png)

## Procedure

1.  Navigate to **All** &gt; **Mobile Branding** &gt; **Manage Mobile Publishing Apps**.

2.  Select **Request a new app**.

3.  On the Add basic info form, fill in the fields.

<table id="table_acp_hsl_2rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Your contact info

</td><td>

Enter the name and email address for the requester of the branded mobile app. The email address is used to send notifications about the build status of your request.

</td></tr><tr><td colspan="2">

**Your app's info**

</td></tr><tr><td>

App type

</td><td>

Select either Now Mobile or Mobile Agent.

 For more information about these mobile apps, see [Now Mobile app](../concept/now-mobile-app.md) or [Mobile Agent app](../concept/mobile-experience.md) documentation.

 In the Washington DC release and later, select customers can use custom app types. For more information, see [Create custom-type mobile apps with Mobile Publishing](../concept/mob-pub-about-custom-apps.md).

</td></tr><tr><td>

Distribution type

</td><td>

Type of distribution. Select **Public**, and then select **Accept** in the Public distribution terms and conditions dialog box.

</td></tr><tr><td>

Operating System \(OS\)

</td><td>

Mobile operating system for your mobile app. Select **Android only**.

 If you need to brand mobile apps for both operating systems, select **iOS and Android**.

</td></tr></tbody>
</table>4.  Select **Next**.

5.  On the Add app details form, fill in the fields.

<table id="table_jtg_zqt_d1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short name

</td><td>

Name of the app icon. The name can't exceed 13 characters. This name displays below the app icon on mobile devices.

</td></tr><tr><td>

Bundle ID

</td><td>

Based on what you entered for the app name and app type, this field auto-populates with the bundle ID.

 You can select the copy icon \(![Copy icon](../image/mob-pub-copy-icon.png)\) to copy this name to your system clipboard.

</td></tr><tr><td>

Mobile Application Management \(MAM\)

</td><td>

Whether you want to use a MAM vendor with your apps. For more information, see [Mobile application management \(MAM\) integration](../concept/sg-mam.md).

 To enable a MAM vendor, select the **Use Mobile Application Management** toggle.

</td></tr><tr><td>

Mobile Application Management vendor

</td><td>

Select one of the following MAM vendors form the list:

 -   **Blackberry**
-   **Intune**
 This field is only visible if you select the **Mobile Application Management \(MAM\)** toggle.

</td></tr><tr><td>

End-user license agreement

 \(EULA\) and privacy policy

</td><td>

EULA and privacy policy options.

 Select the toggle **Use ServiceNow's EULA and privacy policy** to turn on the default EULA and privacy policy.

</td></tr><tr><td>

EULA

</td><td>

URL where app users can view your custom end user license agreement from the mobile app settings. This option only displays when you do not select to use the default ServiceNow EULA.

</td></tr><tr><td>

Privacy policy

</td><td>

URL where app users can view your custom privacy policy from the mobile app settings. This option only displays when you do not select to use the default ServiceNow privacy policy.

</td></tr><tr><td>

iOS Universal links**Note:** If you selected **iOS and Android** for your **Operating System** in the **Add basic info** form, this configuration section is named **Deep links and Universal links**. For more information about deep links, see [Deep linking for mobile](../concept/deep-link-mobile.md).

</td><td>

This table shows all ServiceNow instances used for your organization that can be built into your app as iOS Universal links. Select the URLs that you want to use as Universal links.

 If you need to configure a deep link to a URL that isn't listed in the table, select **Add custom URL**, enter the URL, and then it's added to the table for selection.

 **Note:**

-   This functionality can only be edited when you submit a new branded app request or when you update a branded app.
-   You must download the Apple App Site Association \(AASA\) JSON file after you submit this request and install the file on all instances in the URL list.
To learn more about mobile deep links and universal links, see [Mobile URLs](../concept/mobile-urls.md).

</td></tr><tr><td colspan="2">

**Login management**

</td></tr><tr><td>

Pre-populate instance

</td><td>

Turn on this toggle to build an instance URL into your branded app so end-users don't need to type the instance URL during login. Instead they only need to provide their login credentials. Enter a default app instance URL that is secure and uses Hypertext Transfer Protocol Secure \(https://\).

 **Note:**

-   This instance URL can only be added when you submit a new branded app request or when you updated a branded app.
-   Do not select this option if you are using AppConfig to pre-configure a default instance URL through an EMM suite or an embedded MAM SDK app. For more information, see [AppConfig for Mobile Apps](../reference/appconfig.md).


</td></tr><tr><td>

Default app instance

</td><td>

Enter the secure default app instance URL.

 This field is only visible if you select the **Pre-populate instance** toggle.

</td></tr><tr><td>

Nickname

</td><td>

\(Optional\) Enter a nickname for the **Default app instance** URL that displays on the mobile app for your end-users.

 This field is only visible if you select the **Pre-populate instance** toggle.

</td></tr></tbody>
</table>6.  Select **Next**.

7.  On the Set up for iOS form, fill in the fields.

<table id="table_dfq_nrt_d1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**iOS icon and splash screen**

</td></tr><tr><td>

Use ServiceNow's icons and splash screens

</td><td>

Option that enables you to use the default ServiceNow branding and splash screens.

 If you turn on the toggle to select this option, the customization options are not available.

</td></tr><tr><td>

App icon

</td><td>

Foreground launcher icon for your app. Select **Upload** to browse for the image file you want to use. The image file must meet the following requirements:

 -   File must be in the PNG format.
-   Image size must be 1024 px by 1024 px.
-   Image must be an icon of a company logo with no text. The icon must take up most of the image.
-   Image must have flattened layers.
-   Image must be on a solid background.
-   Image must not have rounded corners.


</td></tr><tr><td>

Splash screen logo

</td><td>

Splash screen for your app. Select **Upload** to browse for the image file you want to use. The image file must meet the following requirements:

 -   File must be in the PNG format.
-   Image size must be 2048 px by 2048 px.
-   Image must contain the company name and logo on a transparent background.


</td></tr><tr><td>

Splash screen background color

</td><td>

Colored box where you select a color for the splash screen background color for your app. Select the square and then select a color on the color picker. The associated hex color code is populated in the text box.

</td></tr><tr><td>

Internal iOS app testers

</td><td>

Testers for the iOS app. For iOS branding, users are required to receive notifications from Apple TestFlight. Select **Add** and enter the **First name**, **Last name**, and **Email** address for each tester. For more information on TestFlight, see the [Apple documentation](https://developer.apple.com/testflight/).

 **Note:** To add additional testers or different testers after you have submitted your branded app request, open a ticket with ServiceNow Support.

</td></tr></tbody>
</table>8.  Select **Next**.

9.  If you selected **iOS and Android** in the **Operating System** field on the **Add basic info** form in Step 3 above, see Step 8 in [Request a new branded Android app for public distribution](request-public-branded-android-app.md) for information about filling out the **Set up for Android** form.

    After you complete the optional Android configuration, return to Step 10 in this topic to complete your request for a public branded iOS app.

10. In the Review and submit form, review the selections you made in Steps 1-9.

11. If all the selections are what you want, select **Submit** to submit your branded app request.


## Result

After you complete the request form, and submit it, your ServiceNow instance builds the app.

To view the status of the build:

1.  Navigate to **All** &gt; **Mobile Branding** &gt; **Manage Mobile Publishing Apps.**
2.  In **Your recent app requests** section, select the card for your branded app request to view its status on the **Request details** page.

When the app is ready for testing, you receive an email notification about the status of the build and also includes a link from where you can download an XCode archive file \(`.xcarchive`\).

**Note:**

-   You can only submit one build at a time. You can't submit another build until the current build is canceled, failed, or completed.
-   It usually takes about 1 week to build the iOS app for public distribution. If you are on a tight timeline, submit your publicly distributed Android first so that you can test it while you submit and wait for the iOS app build to complete. ServiceNow can't expedite this timeline because it's determined by Apple.

## What to do next

**Note:** For public branded iOS apps that are managed by Microsoft Intune, you must register the app in your Microsoft tenant after the build is created, but before the app is distributed. For more information, see [Microsoft Entra ID App Registration Mandate for iOS Intune Mobile App - Mobile Publishing \(KB1640759\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1640759). \(You must have an account and log in to view this ServiceNow KB.\)

After the build successfully completes and your app is ready for testing, see [Test and publish a new branded iOS app for public distribution](../concept/testpubnu-iosapp-pubdist.md).

