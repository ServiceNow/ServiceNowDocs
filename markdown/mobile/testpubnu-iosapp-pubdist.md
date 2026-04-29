---
title: Test and publish a new branded iOS app for public distribution
description: Learn the next steps to test and publish a new branded iOS app for public distribution after you request it in Mobile Publishing.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Request public iOS app, Request, test, &amp; publish, Custom branded apps, Configuring the Mobile Platform, Mobile Platform]
---

# Test and publish a new branded iOS app for public distribution

Learn the next steps to test and publish a new branded iOS app for public distribution after you request it in Mobile Publishing.

## 1. Test the app

After the build successfully completes and your app is ready for testing:

1.  \(Optional\) If you use Microsoft Intune mobile application management \(MAM\), Microsoft requires that iOS apps be registered with Microsoft Entra ID before anyone can log into the iOS app. For more information, see the following ServiceNow® Knowledge Base articles:
    -   [KB1640759](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1640759)
    -   [KB1641110](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sys_kb_id%3D50a4ef5c47b98614c4e1a325126d4300)
2.  Navigate to the Request details page by selecting **All** &gt; **Mobile Branding** &gt; **Manage Mobile Publishing Apps** &gt; **Your recent app requests**.
3.  Select the card for your mobile app build request. The Request details page appears.
4.  Select the **iOS testing file** link and the file is downloaded to your local system for testing:

    ![Mobile Publishing UI showing the testing file download link](../image/mob-pub-file-download-link.png)

5.  Provision the app by doing the following:

    1.  Create an app ID and distribution certificate.
    2.  Edit and sign the XCArchive file.
    3.  Use XCode to upload the app to the App Store Connect.
    See [KB0997467](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0997467) for step-by-step instructions.

    **Note:** Don't miss the walkthrough video \("`Video Walkthrough.mp4`"\) that is attached to KB0997467. It contains a lot of helpful information.

6.  Your testers receive an email from Apple TestFlight with a link to test your branded app.

    **Note:** You must add your testers to a TestFlight group on your AppStoreConnect account and then publish the TestFlight build to the testing group. Only after you perform these steps, do your testers receive an email from TestFlight.

    Use TestFlight to check the following:

    -   App has the correct name, icon, splash screen, branding, and theming. For morning information, see [Create a theme with Theme Builder](https://www.servicenow.com/docs/access?context=tb-create-theme&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).
    -   App uses the default instance you specified for login if you selected the instance pre-fill option when you requested the branded app.
    -   EULA and privacy policy listed in the mobile app **Settings** tab under **Legal** link to the policies you specified.
    See [Apple documentation](https://developer.apple.com/testflight/) for information about using TestFlight.


## 2. Set up the app

After your Testflight testers have validated the branding and functionality of your app, you can set up your app for use. These configurations are optional.

1.  Set up push notifications by downloading the Apple push certificate \(`p12` file\) and uploading it to your app's push application record:
    1.  Create your push notification certificate \(`p12` file\). For instructions, see [KB1506609](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1506609). When you perform this step, you create a push certificate password that you must use in Step 1c. below.
    2.  Access the Push Applications table on your instance by navigating to **All** &gt; **Push Application**.
    3.  Configure your push applications. For instructions, see [Configure push applications for iOS branded apps using certificate based authentication](../task/sg-push-setup-ios.md).
    4.  \(Optional\) Test your push notifications by using out-of-the-box configurations. For more information, see [KB0829093](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0829093).
2.  \(Optional\) Set up deep links and universal links for your app by downloading the universal links file \(AASA\) in the **Your app's info** tab under the **App info** section.
    -   See [KB1273622](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=3c08eadcdb556154fd8d2b69139619b3) for more information about deep links and universal links.
    -   See [KB0831613](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0831613) for information about how to upload your universal link AASA file.

## 3. Approve or reject the app

Once your TestFlight testers have tested your app for branding requirements and functionality:

-   **Reject** the app to edit the branding, app name, app type, or any third-party information. Use the **Duplicate** option to copy information over to a new app request after you have rejected the app.
-   **Approve** the build to move forward with publishing the app to your end users.

## 4. Customize your app's workflows

Use Mobile App Builder to customize your app. See [Mobile App Builder](mab-concept.md) for detailed information about how you can customize your branded app.

## 5. Publish and distribute your app

After you have tested your app, set it up, customized its workflows, and approved it, you are ready to publish your branded iOS app for public distribution:

-   Fill out your Apple app store listing on App Store Connect and publish the app.
-   Apple conducts a final review before posting the app to the public App Store. Please file a Now Support case for any issues.

For instructions:

-   See [KB1649415 Mobile Publishing Public iOS Distribution - AppStoreConnect - App Store Listing Metadata \(App Privacy\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1649415).
-   See [Apple documentation](https://developer.apple.com/ios/submit/) about how to list a public app on the App Store.

## 6. Keep your app updated

Update your app before you update your ServiceNow family version, or at least once per year to keep your push notifications working and to leverage the most up to date ServiceNow mobile features. For more information, see [Tested devices and supported versions for ServiceNow mobile apps](../reference/mobile-supported-devices.md).

