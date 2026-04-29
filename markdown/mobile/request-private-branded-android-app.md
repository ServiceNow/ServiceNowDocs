---
title: Request a new branded Android app for private distribution
description: Request, test, and publish a custom Android app that has your unique company identity. Then make the app available for private distribution.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Request, test, &amp; publish, Custom branded apps, Configuring the Mobile Platform, Mobile Platform]
---

# Request a new branded Android app for private distribution

Request, test, and publish a custom Android app that has your unique company identity. Then make the app available for private distribution.

## Before you begin

Role required: admin

## About this task

Mobile Publishing enables you to request a branded Android app that you can distribute privately. After the request form is completed and the build is successful, you can download an Android Package file \(`.apk`\), and an Android App Bundle file \(`.aab`\). You can then upload the APK and AAB files to your MDM portal or Managed Google Play account. These files can also be hosted on a website for Android users to download the application directly onto their devices.

Ensure that images or text in icons you use are at least 550 pixels from the edge to account for the rounded corners in Android icons.

![Ensure logos are 550 pixels from the edge of the image to avoid a cut off appearance.](../image/logo-padding.png)

Images that don't follow this guideline may appear cut off, as shown in this example.

![Example with cut off logo and text.](../image/cut-off-icon.png)

## Procedure

1.  Navigate to **All** &gt; **Mobile Branding** &gt; **Manage Mobile Publishing Apps**.

2.  Select **Request a new app**.

3.  On the Add basic info form, fill in the fields.

<table id="table_zcb_nyf_2rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Your contact info

</td><td>

Enter the name and email address for the requester of the branded mobile app. The email address is used to send notifications about the build status of your request.

</td></tr><tr><td colspan="2">

**Your apps info**

</td></tr><tr><td>

App type

</td><td>

Select either **Now Mobile** or **Mobile Agent**.

 For more information about these mobile apps, see [Now Mobile app](../concept/now-mobile-app.md) or [Mobile Agent app](../concept/mobile-experience.md) documentation.

 In the Washington DC release and later, select customers can use custom app types. For more information, see [Create custom-type mobile apps with Mobile Publishing](../concept/mob-pub-about-custom-apps.md).

</td></tr><tr><td>

Distribution type

</td><td>

Type of distribution. Select **Private/Enterprise**.

</td></tr><tr><td>

Operating System \(OS\)

</td><td>

Mobile operating system for your mobile app. Select **Android only**.

 If you need to brand mobile apps for both operating systems, select **iOS and Android**.

</td></tr></tbody>
</table>4.  Select **Next**.

5.  On the Add app details form, fill in the fields.

<table id="table_gnz_xvm_d1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short name

</td><td>

Name of the app icon. The name can't exceed 13 characters. This name displays below the app icon on mobile devices.

</td></tr><tr><td>

Long name

</td><td>

Unique name for your app. The name can't exceed 30 characters and must be unique. This name displays for your app when asking for device permissions such as location or push notifications.

</td></tr><tr><td>

Package name

</td><td>

Based on what you entered for the app name and app type, this field auto-populates with the package name.

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

End-user license agreement \(EULA\) and privacy policy

</td><td>

EULA and privacy policy options.

 Select the toggle **Use ServiceNow's EULA and privacy policy** to turn on the default EULA and privacy policy.

</td></tr><tr><td>

EULA

</td><td>

URL where app users can view your custom end user license agreement from the mobile app settings. This option only displays when you don't select to use the default ServiceNow EULA.

</td></tr><tr><td>

Privacy policy

</td><td>

URL where app users can view your custom privacy policy from the mobile app settings. This option only displays when you don't select to use the default ServiceNow privacy policy.

</td></tr><tr><td>

Instances used for deep links**Note:** If you selected **iOS and Android** for your **Operating System** in the **Add basic info** form, this configuration section is named **Deep links and Universal links**. For more information about universal links, see [Universal linking for mobile](../concept/universal-links-mobile.md).

</td><td>

This table shows all ServiceNow instances used for your organization. Select the instance URLs that you want to be built into your app as a deep link.

 If you need to configure a deep link to a URL that isn't listed in the table, select **Add custom URL**, enter the URL, and then it's added to the table for selection.

 **Note:** Deep links can only be edited when you submit a new branded app request or when you update a branded app.

 To learn more about deep links, see [Deep linking for mobile](../concept/deep-link-mobile.md).

</td></tr><tr><td colspan="2">

**Login management**

</td></tr><tr><td>

Pre-populate instance

</td><td>

Turn on this toggle to build an instance URL into your branded app so end-users don't need to type the instance URL during login. Instead they only need to provide their login credentials.

 Enter a default app instance URL that is secure and uses Hypertext Transfer Protocol Secure \(https://\).

 **Note:**

-   This instance URL can only be added when you submit a new branded app request or when you update a branded app.
-   Don't select this option if you're using AppConfig to pre-configure a default instance URL through an EMM suite or an embedded MAM SDK app. For more information, see [AppConfig for Mobile Apps](../reference/appconfig.md).


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

7.  If you selected **iOS and Android** in the **Operating System** field on the **Add basic info** form in Step 3 above, see Step 7 in [Request a new branded iOS app for private distribution](request-private-branded-ios-app.md) for information about filling out the **Set up for iOS** form.

    After you complete the optional iOS configuration, return to Step 8 in this topic to complete your request for a private branded Android app.

8.  On the Set up for Android form, fill in the fields.

<table id="table_cpv_jxm_d1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Google account**

</td></tr><tr><td>

Firebase app ID

</td><td>

App ID of the Android app in your Google Firebase project. The ID is the unique identifier for the Firebase app across all Firebase projects. App IDs always contain the string `name :android:` within the ID.

 **Note:**

-   Each Firebase app ID is unique to the branded app request. If you request multiple apps, each app must have its own unique Firebase app ID.
-   The package name of the branded app defaults to `com.servicenow.b2b.<*app\_name\_long\_no\_spaces*>.<*client\_type&gt;*`.
 For more information, see the [Google Firebase documentation](https://firebase.google.com).

</td></tr><tr><td>

Firebase API key

</td><td>

API key of the Android app in your Google Firebase project. This key is a string that is used when calling Firebase APIs. For more information, see the [Google Firebase documentation](https://firebase.google.com).

</td></tr><tr><td>

Firebase project ID

</td><td>

ID of the Google Firebase project. This is a user-assigned unique identifier for your Firebase project. For more information, see the [Google Firebase documentation](https://firebase.google.com).

</td></tr><tr><td>

Opt-in to trust user-added certificate authorities

</td><td>

Option that enables you to opt in your app to the trusted user-added certificate authority \(CA\). By default, apps that target API level 24 don't honor user supplied CAs.

 Select the toggle to reduce the application attack surface and to encourage consistent handling of network and file-based application data.

</td></tr><tr><td colspan="2">

**Android icons and splash screen**

</td></tr><tr><td>

Use ServiceNow's icons and splash screens

</td><td>

Option that enables you to use the default ServiceNow branding and splash screens.

 **Note:** If you turn on the toggle to select this option, the customization options aren't available.

</td></tr><tr><td>

Adaptive icon foreground

</td><td>

Foreground launcher icon for your app. Select **Upload** to browse for the image file you want to use. The image file must meet the following requirements:

 -   File must be in the PNG format.
-   Image size must be 2048 px by 2048 px.
-   Image must be an icon of a company logo with no text. The icon must take up most of the image.
-   Image must be on a transparent background.


</td></tr><tr><td>

Adaptive icon background

</td><td>

Background launcher icon for your app. Select **Upload** to browse for the image file you want to use. The image file must meet the following requirements:

 -   File must be in the PNG format.
-   Image size must be 2048 px by 2048 px.
-   Image must have no logo or text.
-   Image must have no graphics.
-   Image must not have rounded corners.


</td></tr><tr><td>

Notification icon

</td><td>

Notification icon for your app. This icon is used as the push notification icon on the notification screen. Select **Upload** to browse for the image file you want to use. The image file must meet the following requirements:

 -   File must be in the PNG format.
-   Image size must be 2048 px by 2048 px.
-   Image must contain the company logo with no text on a transparent background.
-   Image must not have rounded corners.


</td></tr><tr><td>

Splash screen logo

</td><td>

Splash screen for your app. Select **Upload** to browse for the image file you want to use. The image file must meet the following requirements:

 -   File must be in the PNG format.
-   Image size must be 2048 px by 2048 px.
-   Image must contain the brand logo or graphic on a transparent background.


</td></tr><tr><td>

Splash screen background color

</td><td>

Colored box where you select a color for the splash screen background color for your app. Select the square and then select a color on the color picker. The associated hex color code is populated in the text box.

</td></tr></tbody>
</table>9.  Select **Next**.

10. In the Review and submit form, review the selections you made in Steps 1-8.

11. If all the selections are what you want, select **Submit** to submit your branded app build request.


## Result

After you complete the request form and submit it, your ServiceNow® instance builds the app.

To view the status of the build:

1.  Navigate to **All** &gt; **Mobile Branding** &gt; **Manage Mobile Publishing Apps**.
2.  In **Your recent app requests** section, select the card for your branded app request to view its status on the **Request details** page.

When it completes, you receive an email notification about the status of the build.

**Note:**

-   You can only submit one build at a time. You can't submit another build until the current build is canceled, failed, or completed.
-   Privately distributed Android apps usually take less than one week to be ready for testing. In many cases these apps are ready for testing within the same day that they are requested. However, ServiceNow can't expedite the timeline because it's determined by Google.

## What to do next

After the build successfully completes and your app is ready for testing, see [Test and publish a new branded Android app for private distribution](../concept/testpubnu-andapp-privdist.md).

