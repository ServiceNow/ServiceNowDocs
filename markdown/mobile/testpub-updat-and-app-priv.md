---
title: Test and publish an updated Android app for private distribution
description: After you have requested an updated Android branded mobile app for private distribution, perform these steps to test and publish it.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-02-12"
reading_time_minutes: 2
breadcrumb: [Update a branded app, Request, test, and publish a branded mobile app, Publish mobile apps with custom branding, Configuring the Mobile Platform, Mobile Platform]
---

# Test and publish an updated Android app for private distribution

After you have requested an updated Android branded mobile app for private distribution, perform these steps to test and publish it.

## Before you begin

Role required: admin

## Procedure

1.  Download the APK file and upload it directly to a device.

2.  Send an email to the APK testers, asking them to open the app on their Android phones or to drag-and-drop the app onto an emulator.

    For more information, see [KB0727776](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sys_kb_id%3D2f6ebf4047e7c250b7832920326d4347).

3.  Check the following items on your app if they've changed from your original request:

    -   App has the correct name, icon, splash screen, branding, and theming. For more information, see [Create a theme with Theme Builder](https://www.servicenow.com/docs/access?context=tb-create-theme&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).
    -   App uses the default instance you specified for login if you selected the instance pre-fill option when you requested the branded app.
    -   EULA and privacy policy listed in the mobile app **Settings** tab under **Legal** link to the policies you specified.
4.  Once the status of your app is **Ready for testing**, you have 90 days to make sure the app meets your branding requirements if changed from your original request:

    -   **Reject** the app to edit the branding, app name, app type, or any third-party information. Use the **Duplicate** option to copy information over to a new app request after you have rejected the app. See the FAQ on the homepage of the Mobile Publishing app for details about what you can change without creating a new app request.
    -   **Approve** the build to move forward with publishing the app to your end users.
5.  Customize your app's workflows:

    Use Mobile App Builder to customize your app. See [Mobile App Builder](../concept/mab-concept.md) for detailed information about how you can customize your branded app.

6.  Publish and distribute your Android app for private distribution by uploading your APK file to your private distribution site, managed Google Play site, or your EMM \(enterprise mobility management\) provider:

    -   See [Google documentation](https://support.google.com/a/answer/2494992?hl=en) for information about how to publish private apps from the Google Play Console.
    -   If you are using the BlackBerry mobile application management \(MAM\), see [KB0813295](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0813295).
    -   If you are using the Microsoft Intune MAM, see [Microsoft documentation](https://learn.microsoft.com/en-us/mem/intune/apps/apps-add-android-for-work).
    -   For information about ServiceNow® mobile apps version history and changes, see:
        -   [Now Mobile](https://www.servicenow.com/docs/bundle/mobile-rn/page/release-notes/mobile-apps/now-mobile/now-mobile-available-versions.html)
        -   [ServiceNow Agent](https://www.servicenow.com/docs/bundle/mobile-rn/page/release-notes/mobile-apps/agent/agent-available-versions.html)
    -   Update your app before you update your ServiceNow family version, or at least once per year to keep your push notifications working and to leverage the most up to date ServiceNow mobile features. For more information, see [Tested devices and supported versions for ServiceNow mobile apps](../reference/mobile-supported-devices.md).

**Parent Topic:**[Update a branded app](update-branded-app.md)

