---
title: Prerequisites for Mobile Publishing
description: Before submitting your first branded app request with Mobile Publishing, it's important to set up some prerequisite tools.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Publish mobile apps with custom branding, Configuring the Mobile Platform, Mobile Platform]
---

# Prerequisites for Mobile Publishing

Before submitting your first branded app request with Mobile Publishing, it's important to set up some prerequisite tools.

## ServiceNow instance requirements

Regardless of the distribution method or app provider that you choose, your ServiceNow instance requires the following configurations to use Mobile Publishing:

-   A cloud-connected production instance is required to request a Mobile Publishing build. Once you have the Mobile Publishing build, you can use the mobile app on any single instance.
-   The Mobile Publishing plugin \(com.glide.sn-mobile-whitelab\) must be installed on your production instance. The Mobile Publishing plugin is a paid plugin that can be installed from the ServiceNow® Store, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)
-   Instances must be able to download the following file types: zip, apk, p12, aab, xcarchive, svg, and png.

    To add file types that can be downloaded by your instance:

    1.  Navigate to **All** &gt; **System Properties** &gt; **Security**.
    2.  Scroll down the page to the **Attachment limits and behavior** section.
    3.  Make sure the zip, apk, p12, aab, xcarchive, svg, and png file types are included in the file types that can be downloaded as static content from an instance.
    4.  Select **Save**.

## Third-party prerequisites by distribution type

Make sure that you have the following third-party applications to request, test, and publish branded mobile apps.

-   **Private distribution prerequisites**

    To request a branded app for private distribution, you must have access to the following:

    -   Google Firebase account

        -   Generates the Firebase App ID, Firebase API Key, and the Firebase project ID.
        -   Sets up push notifications to Android devices.
        For more information about Google Firebase, see the [Google Firebase documentation](https://firebase.google.com/).

    -   Apple Business Manager \(ABM\)

        -   Generates the Apple DEP ID/Org ID and the org name.
        -   Distributes private iOS apps.
        For more information about Apple Business Manager, see the [Apple Business Manager User Guide](https://support.apple.com/guide/apple-business-manager/welcome/web).

        **Important:** Be sure to enable the "Custom Apps" setting in your ServiceNow instance. This enables you to publish the iOS branded apps into ABM.

    -   Names and email addresses for your iOS app testers.
    -   Apple TestFlight account, which is used to test your iOS account.

        **Note:** The Apple TestFlight account isn't required to request a branded app for private distribution but is required to complete the process.

-   **Public distribution prerequisites**

    To request a branded app for public distribution, you must have access to the following:

    -   Google Firebase account

        -   Generates the Firebase App ID, Firebase API Key, and the Firebase project ID.
        -   Sets up push notifications to Android devices.
        For more information about Google Firebase, see the [Google Firebase documentation](https://firebase.google.com/).

    -   \* Apple Connect account, which is used to test your iOS app.
    -   \* Apple Developer account, which is required to upload and distribute the app to Apple's public store.
    -   \* Managed Google Play account, which is used to upload and distribute your Android app.
    -   \* XCode software \(Mac\), which is required to compile the iOS branded applications for public distribution.
    -   \* Microsoft Entra ID app registration for iOS Microsoft Intune mobile apps.

        Microsoft requires iOS Intune apps be registered with Microsoft Entra ID \(formerly Microsoft Azure AD\) in the second half of the calendar year 2024. Apps that are not registered will fail the Microsoft Intune login flow. For more information, see the following resources:

        -   [Microsoft website explaining the requirement and the timeline](https://learn.microsoft.com/en-us/mem/intune/fundamentals/whats-new#wrapped-ios-apps-and-ios-apps-using-the-intune-app-sdk-will-require-azure-ad-app-registration).
        -   [Microsoft Entra ID App Registration Mandate for iOS Intune Mobile Apps - Mobile Publishing \(KB1640759\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1640759). \(You must have an account and log in to view this ServiceNow KB.\)
    \* These items are not required to request the branded app for public distribution, but they are required to complete the process.


**Parent Topic:**[Publish mobile apps with custom branding](mobile-publishing.md)

