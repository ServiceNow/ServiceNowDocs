---
title: Mobile Classic Android v4.2
description: The Mobile Classic Android v4.2 release provides problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/classic-android-v4-2.html
release: mobile
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 1
breadcrumb: [Mobile Classic mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Classic Android v4.2

The Mobile Classic Android v4.2 release provides problem fixes.

## Download the latest Mobile Classic version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.servicenow&hl=en).

**Important:** There are several new ServiceNow mobile apps, including Mobile Agent, Now Mobile, Mobile Onboarding, and Now Support. Check out these new apps for the latest features and capabilities.

## Fixed in this release

<table id="tbl_AllFixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mobile

 PRB1273375

</td><td>

When the session has timed out, opening a record from a push notification loads an incorrect view

</td><td>

Opening a push notification record when the user's session has expired can cause the record screen to load with the incorrect view, which persists throughout that session.

</td></tr><tr><td>

Mobile

 PRB1263738

</td><td>

SSO login can fail

</td><td>

This issue only affects the native Android application. When SSO for an instance is configured to utilize auth\_redirect.do on the native application, it can cause the Android application to prevent loading the IDP login page. In some instances, it will load the IDP login page, but still fail after entering a correct username and password.

</td></tr><tr><td>

Mobile

 PRB1298766

</td><td>

General difficulty with barcode scanner

</td><td>

When using the in-app barcode scanner, the barcode is inconsistent at scanning some or all barcodes. Symptoms include: -   Camera not focusing
-   When multiple barcodes in view, the incorrect barcode is selected
-   Inability to detect a barcode \(usually due to camera also not focusing\)

</td></tr><tr><td>

Mobile

 PRB1277667

</td><td>

The 'Forgot password' link tries to load

</td><td>

In the native Android application, clicking on Forgot Password may prompt the user to select the application to use - usually a browser and also the Android app. Selecting the ServiceNow app will not load the forgot password page.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile Classic mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/classic-available-versions.md)

