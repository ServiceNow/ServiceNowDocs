---
title: Publicly distributed apps
description: Public distribution can be used to distribute iOS or Android branded applications on public app stores.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Distribution, Custom branded apps, Configuring the Mobile Platform, Mobile Platform]
---

# Publicly distributed apps

Public distribution can be used to distribute iOS or Android branded applications on public app stores.

**Important:**

-   If you select **iOS &amp; Android** as your **Operating System \(OS\)** when you request your branded mobile app, all builds are delivered to you at the same time. This means that both your Android and iOS apps are delivered to you within the publicly distributed iOS delivery timeline of 1 week.
-   If you have an implementation date deadline within days, it's suggested that you request the Android app first, test it, and approve its branding. Then submit your iOS app request.
-   Another way to expedite delivery of your branded app is to test the mobile workflows and functions using the mobile apps that are available on the ServiceNow® Store while your branded app is being built. Your branded app uses all the same workflows and mobile app functions as the apps that are available on the ServiceNow Store. Then when your branded app is available, you only need to test the branding, the login flow for pre-filled instance URLs, push notifications, and the app store listings.

## iOS branded apps for public distribution

The ServiceNow® branding program complies with the suggested practices from Apple for branded app releases. Mobile Publishing enables you to request a branded iOS app that can be distributed on the public Apple Store. After you complete the request form, your ServiceNow instance builds the app and provides a link from where you can download an XCode archive file \(`.xcarchive`\). Then you download the XCode archive file, update it, and re-sign it to generate an iOS application archive file \(`.ipa`\). After the `.ipa` file is generated, you upload it to Apple Connect for testing. When testing is completed, you approve the build and can deploy your branded app with the public Apple Store.

The following image summarizes the workflow. It usually takes about 1 week to build the iOS app for public distribution.

![Public publishing process for iOS branded apps.](../image/mobile-ios-public-brand-app-process.png "iOS branded app publishing process for public distribution")

## Android branded apps for public distribution

The ServiceNow branding program also complies with the suggested practices from Google for branded app releases. Use Mobile Publishing to request a branded Android app that you can upload and distribute with the Google Play Store. After you complete the branded app request form in Mobile Publishing, your ServiceNow instance builds the app. Then it provides a link from where you can download an Android App Bundle file \(`.aab`\). Download the AAB file and test it. If the tests are successful, you approve the build and can deploy your app with the Google Play Store.

The following image summarizes the workflow. It usually takes about a week or less to build the Android branded application. Sometimes it might take only a few hours.

![Public publishing process for Android branded apps.](../image/mobile-android-public-brand-app-proc.png "Android branded app publishing process for public distribution")

**Parent Topic:**[Distributing your mobile app](mobile-distribution.md)

