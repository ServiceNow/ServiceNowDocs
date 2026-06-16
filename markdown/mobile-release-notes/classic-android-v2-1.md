---
title: Mobile Classic Android v2.1
description: The Mobile Classic Android v2.1 release provides problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/classic-android-v2-1.html
release: mobile
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 2
breadcrumb: [Mobile Classic mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Classic Android v2.1

The Mobile Classic Android v2.1 release provides problem fixes.

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

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile

 PRB718570

</td><td>

Users cannot open attached PDF files from Knowledge Management using the Android app

</td><td>

 

</td><td>

In an OOB Helsinki instance:

 1.  Ensure that you have a KB that has an attached PDF file.
2.  Connect to your test instance with the Android native app.
3.  Navigate to Knowledge Bases &gt; IT &gt; your test KB.

 Notice that the that clicking on the link does not download the PDF attachment or open the knowledge article. If you repeat the above steps with the iOS app or Mobile UI on Android, you are able to access the article.

</td></tr><tr><td>

Mobile

 PRB721868

</td><td>

In the Android app, tapping the email preview cell in an incident does not open up the email contents

</td><td>

This issue is not present for iPhone users.

</td><td>

1.  Open any incident that contains email messages in the correspondence section.
2.  Tap one of the email previews that includes 'Email Sent', Subject, To/From.

 Expected behavior: This should open up a new page that displays the email contents.

 Actual behavior: Nothing visual occurs.

</td></tr><tr><td>

Mobile

 PRB723229

</td><td>

On the Android app, reference fields on forms do not have a 'Clear' button like they do on the iPhone app

</td><td>

Without this 'Clear' button, there is no way to clear out reference fields.

</td><td>

1.  Open any incident.
2.  Find a reference field \(e.g. **Caller**\). If it is empty, add a caller.
3.  Open the field by clicking the magnifying glass.

 Note that there appears to be no way to clear out the field once it is no longer empty.

 Expected behavior: There should be a 'clear' button like there is on the iPhone app.

 Actual behavior: There is no 'clear' button.

</td></tr><tr><td>

Mobile

 PRB734628

</td><td>

Loading a user record on an Android tablet should open the user profile

</td><td>

Loading a user record on an Android tablet should open a profile view of that user, but clicking on a user record opens a record detail for the user on the native Android app.

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB734635

</td><td>

Fix Android application crashes reported via crash reporting tool

</td><td>

Various conditions can cause the Android application to crash.

</td><td>

The following example conditions do not always produce a crash, but these are the conditions where the crash may occur randomly:

 -   Enter invalid text into the Connect chat text box and tap **Send**.
-   Open a list that loads a large number of records. Scroll down to ensure a large number of the records are loaded into memory and then edit the Filter.
-   Load the navigator and quickly go back.
-   Hitting the back button can randomly cause a crash.
-   Any page loading a user avatar when the platform returns a space for the user's name.

</td></tr><tr><td>

Mobile

 PRB736838

</td><td>

Native mobile apps should support "Accept / Decline" push notification buttons

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Mobile Classic mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/classic-available-versions.md)

