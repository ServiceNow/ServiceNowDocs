---
title: Test and publish an updated Android app for public distribution
description: After you have requested an updated Android app for public distribution, perform these steps to test and publish it.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Update a branded app, Request, test, &amp; publish, Custom branded apps, Configuring the Mobile Platform, Mobile Platform]
---

# Test and publish an updated Android app for public distribution

After you have requested an updated Android app for public distribution, perform these steps to test and publish it.

## Before you begin

Role required: admin

## Procedure

1.  Upload the AAB file directly to Google Play so you can use the Google Play internal testing tool.

    See [Google documentation](https://play.google.com/console/about/internal-testing/) for information about internal testing on Google Play.

2.  Check the following items on your app if they've changed from the original request:

    -   App has the correct name, icon, splash screen, branding, and theming. For more information, see [Create a theme with Theme Builder](https://www.servicenow.com/docs/access?context=tb-create-theme&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).
    -   App uses the default instance you specified for login if you selected the instance pre-fill option when you requested the branded app.
    -   EULA and privacy policy listed in the mobile app **Settings** tab under **Legal** link to the policies you specified.
3.  Set up your Android app:

    -   Set up push notifications by adding your Google Firebase Cloud Messaging HTTPv1 Oauth token to your app type's push application record.

        See [KB1639289](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sys_kb_id%3D68456c07471d86d030fba325126d43e5) for detailed instructions.

    -   \(Optional\) Test push notifications using an out-of-the-box push notification.

        See [KB0829093](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=b5e4111cdba5d010feb1a851ca961909) for detailed instructions.

    -   \(Optional\) Set up deep links for your app by configuring an `assetlinks.json` file on each instance.

        See [KB1648690](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1648690) for detailed instructions.

4.  Make sure the app meets your branding requirements:

    -   **Reject** the app to edit the branding, app name, app type, or any third-party information. Use the **Duplicate** option to copy information over to a new app request after you have rejected the app.
    -   **Approve** the build to move forward with publishing the app to your end users.
5.  Customize your app's workflows:

    Use Mobile App Builder to customize your app. See [Mobile App Builder](../concept/mab-concept.md) for detailed information about how you can customize your branded app.

6.  After you have tested your app, set it up, and customized its workflows, you are ready to publish your branded Android app for public distribution.

    Deploy your AAB file to the Google Play console, or your enterprise mobility management \(EMM\) provider:

    -   Upload your app to the Google Play console: to upload your public branded Android app to the Google, see [Google documentation](https://developer.android.com/studio/publish/upload-bundle). Also see [KB1157062](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=a2a066bedb5155d0d0dc3feb68961951) for ServiceNow guidance on creating your Google Play console listing metadata.
    -   BlackBerry Portal: to publish your public branded Android app to the BlackBerry Portal if you're using BlackBerry mobile application management \(MAM\), see [KB0813295](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0813295).
    -   Microsoft Intune: to sync your public branded Android app from Google to Microsoft Intune, see [Microsoft documentation](https://learn.microsoft.com/en-us/mem/intune/apps/apps-add-android-for-work).
7.  Update your app before you update your ServiceNow family version, or at least once per year to keep your push notifications working and to leverage the most up to date ServiceNow mobile features.

    For more information, see [Tested devices and supported versions for ServiceNow mobile apps](../reference/mobile-supported-devices.md).


**Parent Topic:**[Update a branded app](update-branded-app.md)

