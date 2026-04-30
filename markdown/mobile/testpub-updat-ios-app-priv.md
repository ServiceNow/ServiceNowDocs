---
title: Test and publish an updated iOS app for private distribution
description: AFter you have requested an updated iOS app for private distribution, perform these steps to test and publish it.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Update a branded app, Request, test, &amp; publish, Custom branded apps, Configuring the Mobile Platform, Mobile Platform]
---

# Test and publish an updated iOS app for private distribution

AFter you have requested an updated iOS app for private distribution, perform these steps to test and publish it.

## Before you begin

Role required: admin

## Procedure

1.  Your testers receive an email from Apple TestFlight with a link to test your branded app.

    Use TestFlight to check the following if they've changed from your original request:

    -   App has the correct name, icon, splash screen, branding, and theming. For more information, see [Create a theme with Theme Builder](https://www.servicenow.com/docs/access?context=tb-create-theme&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).
    -   App uses the default instance you specified for login if you selected the instance pre-fill option when you requested the branded app.
    -   EULA and privacy policy listed in the mobile app **Settings** tab under **Legal** link to the policies you specified.
    See [Apple documentation](https://developer.apple.com/testflight/) for information about using TestFlight.

2.  Set up your iOS app:

    **Note:** The following configurations are needed only if the push certificate has expired or if you didn't configure these in your original request. Push notification certificates typically expire every 13 months. Our system sends multiple email notifications alerting you when your push certificate will expire.

    -   Set up push notifications by downloading the Apple push certificate \(`p12` file\) from your app's **Build History** and upload it to your app's push application record:
        1.  Access the Push Applications table on your instance by navigating to **All** &gt; **Push Application**.
        2.  Configure your push applications. For instructions, see [Configure push applications for iOS branded apps using certificate based authentication](sg-push-setup-ios.md).

            **Note:** The push certificate password is sent in the email from Apple TestFlight that contains a link to test your branded app.

        3.  \(Optional\) Test your push notifications by using out-of-the-box configurations. For more information, see [KB0829093](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0829093).
    -   Set up deep links and universal links for your app by downloading the universal links file \(AASA\) in the **Your app's info** tab under the **App info** section.
        -   See [KB1273622](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=3c08eadcdb556154fd8d2b69139619b3) for more information about deep links and universal links
        -   See [KB0831613](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0831613) for information about how to upload your universal link AASA file.
3.  Once the status of your app is **Ready for testing**, you have 90 days to make sure the app meets your branding requirements:

    -   **Reject** the app to edit the branding, app name, or any third-party information. Use the **Duplicate** option to copy information over to a new app request after you have rejected the app.
    -   **Approve** the build to move forward with publishing the app to your end users.
4.  Customize your app's workflows:

    Use Mobile App Builder to customize your app. See [Mobile App Builder](../concept/mab-concept.md) for detailed information about how you can customize your branded app.

5.  After you have tested your app, set it up, customized its workflows, and approved it, you are ready to publish your branded iOS app for private distribution.

    Apple conducts a final review where your build status will show **Deployment in progress** after which ServiceNow® automatically sends the app to your Apple Business Manager \(ABM\) account.

    If you are using a mobile application management \(MAM\) provider, your MAM can assist in the distribution process from your ABM account.

    For instructions:

    -   See [KB1649495](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1649495) for information about distributing your iOS with redemption codes by using Apple Business Manager.
    -   If you are using the Microsoft Intune MAM, see [Sync your branded iOS app to Intune](https://www.servicenow.com/community/mobile-apps-platform-articles/mobile-publishing-sync-your-branded-ios-app-to-intune/ta-p/2301831) on the ServiceNow Community website.
    -   If you are using the BlackBerry MAM, see [KB0821154](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0821154) for information about adding your iOS branded app to BlackBerry.
6.  Update your app before you update your ServiceNow family version, or at least once per year to keep your push notifications working and to leverage the most up to date ServiceNow mobile features.

    For more information, see [Tested devices and supported versions for ServiceNow mobile apps](../reference/mobile-supported-devices.md).


**Parent Topic:**[Update a branded app](update-branded-app.md)

