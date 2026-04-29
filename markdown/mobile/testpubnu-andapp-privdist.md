---
title: Test and publish a new branded Android app for private distribution
description: Learn the next steps to test and publish a new branded Android app for private distribution after you request it in Mobile Publishing.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Request private Android app, Request, test, &amp; publish, Custom branded apps, Configuring the Mobile Platform, Mobile Platform]
---

# Test and publish a new branded Android app for private distribution

Learn the next steps to test and publish a new branded Android app for private distribution after you request it in Mobile Publishing.

## 1. Test the app

After the build successfully completes and your app is ready for testing:

1.  Navigate to the Request details page by selecting **All** &gt; **Mobile Branding** &gt; **Manage Mobile Publishing Apps** &gt; **Your recent app requests**.
2.  Select the card for your mobile app build request. The Request details page appears.
3.  Select the **Android testing file** link and the APK file is downloaded to your local system for testing:

    ![Mobile Publishing UI showing the Android .apk file download link](../image/mob-pub-apk-download-link.png)

4.  Send the APK file to your testers via email so they can open the file on their Android device or in an emulator.

    See [KB0727776](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sys_kb_id%3D2f6ebf4047e7c250b7832920326d4347) for information about how to install a mobile simulator and APK file on your computer so you can test the Android testing file.

5.  Check the following items on your app:

    -   App has the correct name, icon, splash screen, branding, and theming. For more information, see [Create a theme with Theme Builder](https://www.servicenow.com/docs/access?context=tb-create-theme&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).
    -   App uses the default instance you specified for login if you selected the instance pre-fill option when you requested the branded app.
    -   EULA and privacy policy listed in the mobile app **Settings** tab under **Legal** link to the policies you specified.
    **Important:** The APK file that was used during testing should also be used for deployment.


## 2. Set up the app

After testing completes successfully, you can set up your app for use. These configurations are optional.

1.  Set up push notifications by adding your Google Firebase Cloud Messaging HTTPv1 Oauth token to your app type's push application record.

    See [KB1639289](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sys_kb_id%3D68456c07471d86d030fba325126d43e5) for detailed instructions.

2.  Test push notifications using an out-of-the-box push notification.

    See [KB0829093](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=b5e4111cdba5d010feb1a851ca961909) for detailed instructions.

3.  Set up deep links for your app by configuring an `assetlinks.json` file on each instance.

    See [KB1648690](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1648690) for detailed instructions.


## 3. Approve or reject the app

Once the status of your app is **Ready for testing**, you have 90 days to make sure the app meets your branding requirements:

-   **Reject** the app to edit the branding, app name, app type, or any third-party information. Use the **Duplicate** option to copy information over to a new app request after you have rejected the app.
-   **Approve** the build to move forward with publishing the app to your end users.

## 4. Customize your app's workflows

Use Mobile App Builder to customize your app. See [Mobile App Builder](mab-concept.md) for detailed information about how you can customize your branded app.

## 5. Publish and distribute your app

After you have tested your app, set it up, and customize its workflows, you are ready to publish your branded Android app for private distribution. Upload your APK file to your private distribution site, the managed Google Play Console, or your enterprise mobility management \(EMM\) provider:

-   **Google Play Console:**

    To publish your private branded Android app from the Google Play Console, see [Google documentation](https://support.google.com/a/answer/2494992?hl=en).

-   **BlackBerry Portal:**

    To publish your private branded Android app to the BlackBerry Portal if you are using BlackBerry mobile application management \(MAM\), see [KB0813295](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0813295).

-   **Microsoft Intune:**

    To sync your private branded Android app from Google to Microsoft Intune, see [Microsoft documentation](https://learn.microsoft.com/en-us/mem/intune/apps/apps-add-android-for-work).


## 6. Keep your app updated

Update your app before you update your ServiceNow® family version, or at least once per year to keep your push notifications working and to leverage the most up to date ServiceNow mobile features. For more information, see [Tested devices and supported versions for ServiceNow mobile apps](../reference/mobile-supported-devices.md).

