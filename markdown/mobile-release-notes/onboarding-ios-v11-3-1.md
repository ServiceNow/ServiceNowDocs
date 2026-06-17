---
title: Mobile Onboarding for iOS v11.3.1
description: The iOS v11.3.1 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2021-01-25"
reading_time_minutes: 3
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for iOS v11.3.1

The iOS v11.3.1 release provides fixes for the application.

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

 PRB1449993

</td><td>

Issue with the 'Clear All' function within the Notification section

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1459475

</td><td>

The app crashes when launching

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1416381

</td><td>

Dependency field issue with choices

</td><td>

The dependent field is not clearing out if the choice is changed when the action item type is set to 'Script'.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1454492

 [KB0868589](https://support.servicenow.com/kb_view.do?sysparm_article=KB0868589)

</td><td>

The error 'User Not Authenticated' appears when navigating in the app

</td><td>

Users are getting the following error when navigating in the app: "error":\{"message":"User Not Authenticated","detail":"Required to provide Auth information"\},"status":"failure".

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1454452

</td><td>

The 'Assigned to' field is not cleared out after the 'Assignment group' field is changed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1453396

</td><td>

When scrolling down on the list, the text jumps to the right of the screen

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1452364

</td><td>

The notification records under the 'Notifications' screen are displayed twice for the assigned incident when users upgrade the app

</td><td>

 

</td><td>

1.  Install an older version of the mobile app and log in as the ITIL user.
2.  On the platform, search for Incident in the Filter Navigator.
3.  Select **All**, and then assign 1 or 2 incidents to the ITIL user and wait for the push notification to be received on the device.

**Note:** Do not tap to open these notifications, else the issue cannot be reproduced. Also make sure this notification is received while the app is in the background.

4.  Upgrade the app to the latest release version.
5.  Open the app to navigate to the Notifications screen and verify that there should be a single record for each incident assigned.

 Notice that there are 2 entries for each assigned incident.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1451090

</td><td>

The system property glide. security.csrf\_previous.allow needs to be set to 'True' in order to upload images in VA

</td><td>

 

</td><td>

1.  In the instance, start a new Virtual Agent chat.
2.  Select the topic 'ACME File Upload' and select 'Take a picture'.

Notice that the image will be stuck at 'uploading...'.


 Expected behavior: When the system property glide. security.csrf\_previous.allow is 'False', Virtual Agent should still be allowed to upload images.

 Actual behavior: When the system property glide. security.csrf\_previous.allow is 'False', the image will be stuck at 'uploading...' when uploading the image in VA.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1448917

</td><td>

Can't input Kanji Japanese characters in comments on iOS devices

</td><td>

 

</td><td>

1.  Add the Japanese language to the keyboard on an iOS device.
2.  Log in to the instance on the mobile app.
3.  Open any incident record.
4.  Try to add comments by changing the keyboard to Kanji Japanese language.
5.  Try typing 'sa-basaikidou' for example.

 Expected behavior: As users type 'sa-basaikidou', the characters should get auto translated to Kanji Japanese language.

 Actual behavior: The characters are not translated to Kanji Japanese language.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1444878

</td><td>

The iOS mobile app does not have auto-correct

</td><td>

 

</td><td>

1.  Navigate to the mobile app on iOS.
2.  Open an incident through any applet.
3.  Open the Add comment function from the top three-dot menu.

 Notice that typing the work note and additional comments does not prompt the suggestions.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1420536

</td><td>

The dashboard preview is not clickable until the chart screen is loaded

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1456900

</td><td>

The last Korean character is broken on mobile apps

</td><td>

 

</td><td>

Type the content in Korean and submit.

 Notice that the last consonant or vowel entered is separated from the previous character.

 **Note:** It appears that the issue occurs when you type and there is no space after the text.

</td></tr></tbody>
</table>This version also contains fixes for several accessibility-related issues and UI issues with iOS 14, as well as other performance improvements and minor bug fixes.

**Note:** This version is compatible with Quebec Early Availability instances.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

