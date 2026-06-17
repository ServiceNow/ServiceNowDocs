---
title: Mobile Onboarding for iOS v11.2.0
description: The iOS v11.2.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2020-12-10"
reading_time_minutes: 1
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for iOS v11.2.0

The iOS v11.2.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding/id1472486882). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_rbw_2jr_2jb"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile iOS \(non-classic\)

 PRB1418360

 [KB0853002](https://support.servicenow.com/kb_view.do?sysparm_article=KB0853002)

</td><td>

The 'Contact Agent' option is still available in the chat even when live chat is disabled

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1430543

</td><td>

The media section label is returning blank

</td><td>

 

</td><td>

1.  Create a media screen.
2.  Add a function instance to the media screen.
3.  Add a label in the function instance record.
4.  Log in to a New York instance using an iOS device.
5.  Navigate to the Applet Launcher which has the media screen.

 Expected behavior: The media section function instance label should be visible below the media screen image.

 Actual behavior: The media section function instance label is not visible.

 **Note:** The issue is replicated only in New York instances. The same is not replicated in Orlando instances.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1435736

</td><td>

Different spinner behavior when the Cabrillo web view completes loading

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1447561

</td><td>

VoiceOver does not announce the label 'Enter the instance address...' when the focus moves to its edit field

</td><td>

If the label 'Enter the instance address.....' is not announced by VoiceOver, screen reader users will be left unaware about the control and will not be able to perform the desired actions. This issue might hamper the task of the users.

</td><td>

1.  Enable VoiceOver and open the app. The login screen will appear.
2.  Navigate to the edit field 'example.service-now.com' via swipe gestures.

 Notice that VoiceOver does not announce the label 'Enter the instance address...'.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1448500

</td><td>

The chat in the app does not display the current session if users navigate to the app after locking the mobile screen

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>This version also contains other performance improvements and minor bug fixes.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

