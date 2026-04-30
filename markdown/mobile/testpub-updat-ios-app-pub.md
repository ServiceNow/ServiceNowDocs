---
title: Test and publish an updated iOS app for public distribution
description: After you have requested an updated iOS branded mobile app for public distribution, perform these steps to test and publish it.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-02-12"
reading_time_minutes: 4
breadcrumb: [Update a branded app, Request, test, and publish a branded mobile app, Publish mobile apps with custom branding, Configuring the Mobile Platform, Mobile Platform]
---

# Test and publish an updated iOS app for public distribution

After you have requested an updated iOS branded mobile app for public distribution, perform these steps to test and publish it.

## Before you begin

Role required: admin

## Procedure

1.  When the build status of your app becomes **Ready for testing**, you can download the XCArchive file, edit it and sign it, and then use XCode to upload it to App Store Connect.

    **Note:**

    -   After you upload the XCArchive file and the new build is published to your TestFlight testers group, then your testers receive an email with a link to test your branded app.
    -   You don't need to create a new Apple iOS Distribution Certificate or a provisioning profile for apps that already exist and you're only updating the version number. For example, updating version 17.5 to 18.0. However, if your certificate has expired per your Keychain Access program on your Mac, see [KB0997467](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0997467) for instructions.
2.  When your testers receive an email from Apple TestFlight with a link to test your branded app, use TestFlight to check the following if they've changed from your original request:

    -   App has the correct name, icon, splash screen, branding, and theming. For more information, see [Create a theme with Theme Builder](https://www.servicenow.com/docs/access?context=tb-create-theme&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).
    -   App uses the default instance you specified for login if you selected the instance pre-fill option when you requested the branded app.
    -   EULA and privacy policy listed in the mobile app **Settings** tab under **Legal** link to the policies you specified.
    See [Apple documentation](https://developer.apple.com/testflight/) for information about using TestFlight.

3.  Set up your branded iOS app for public distribution:

    -   Set up push notifications by downloading the Apple push certificate \(`p12` file\) and uploading it to your app's push application record:
        -   Create your push notification certificate \(`p12` file\). For instructions, see [KB1506609](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1506609).
        -   Access the Push Applications table on your instance by navigating to **All** &gt; **Push Application**.
        -   Configure your push applications. For instructions, see [Configure push applications for iOS branded apps using certificate based authentication](sg-push-setup-ios.md).
        -   \(Optional\) Test your push notifications by using out-of-the-box configurations. For more information, see [KB0829093](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0829093).
    -   If you updated your universal links table with new instance URLs, you must upload the new universal links file to each of those instances:

        Download the universal links file \(AASA\) in the **Your app's info** tab under the **App info** section and follow the instructions in the following KBs:

        -   See [KB1273622](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=3c08eadcdb556154fd8d2b69139619b3) for more information about deep links and universal links.
        -   See [KB0831613](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0831613) for information about how to upload your universal link AASA file.
4.  Once your TestFlight testers have tested your app for branding requirements and functionality:

    -   **Reject** the app to edit the branding, app name, app type, or any third-party information. Use the **Duplicate** option to copy information over to a new app request after have rejected the app. See the FAQ on the home page of the Mobile Publishing app for information about what you can change without having to create a new branded app request.
    -   **Approve** the build to move forward with publishing the app to your end users.
5.  Customize your app's workflows:

    Use Mobile App Builder to customize your app. See [Mobile App Builder](../concept/mab-concept.md) for detailed information about how you can customize your branded app.

6.  Publish your updated iOS branded app for public distribution.

    Your app store listing definition remains the same as your previous version of this app. Update the "What's new" field in the app store listing and submit for Apple's approval. Apple conducts a final review before posting the app to the public App Store. If you have problems, file a ServiceNow Support case.

    -   See [KB1649415](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1649415) for ServiceNow's Apple App Store listing guidance.
    -   See [Apple documentation](https://developer.apple.com/ios/submit/) that explains how to list a public app on the Apple App Store.
    -   For information about ServiceNow mobile apps version history and changes, see:
        -   [Now Mobile](https://www.servicenow.com/docs/bundle/mobile-rn/page/release-notes/mobile-apps/now-mobile/now-mobile-available-versions.html)
        -   [ServiceNow Agent](https://www.servicenow.com/docs/bundle/mobile-rn/page/release-notes/mobile-apps/agent/agent-available-versions.html)
        -   [Custom app](https://www.servicenow.com/docs/bundle/mobile-rn/page/release-notes/mobile-apps/mobile-apps.html)
7.  Update your app before you update your ServiceNow family version, or at least once per year to keep your push notifications working and to leverage the most up to date ServiceNow mobile features.

    For more information, see [Tested devices and supported versions for ServiceNow mobile apps](../reference/mobile-supported-devices.md).


**Parent Topic:**[Update a branded app](update-branded-app.md)

