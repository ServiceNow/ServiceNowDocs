---
title: ServiceNow Onboarding - Intune for Android v12.4.0
description: The Android v12.4.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-intune-android-v12-4-0.html
release: mobile
topic_type: reference
last_updated: "2021-08-19"
reading_time_minutes: 4
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for Android v12.4.0

The Android v12.4.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.onboarding). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="AllOtherFixes" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile Android \(non-classic\)

 PRB1444666

</td><td>

Push notifications are not received on the Agent and Now Mobile BlackBerry apps after quitting

</td><td>

The app receives the push notifications, but there is a check if the user is authorized, which determines if the notifications should be shown to the user. For the Now Mobile app, the authorization check is always successful. However, in the Now Mobile BlackBerry app, the authorization check fails if the notification is received when the app is not running.

</td><td>

1.  Install and log in to the Now Mobile Intune app.
2.  Order an item from the catalog.
3.  Remove the app from 'Recents'.
4.  Trigger a push notification.

 Expected behavior: The push notification should be shown in the app.

 Actual behavior: You don't see the push notification in the app. Check the logs and notice that the push notification message was received.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1476745

</td><td>

Talkback does not announce the label 'Enter the instance address.....' when focus moves to its edit field

</td><td>

 

</td><td>

1.  Launch the Agent app.
2.  Turn on Talkback.
3.  Tap the '+' icon to add an instance.

 Expected behavior: Talkback should announce the label field 'Enter the instance address' when you edit a text field.

 Actual behavior: Talkback announces 'Editing example.servicenow.com'.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1499412

</td><td>

The attachment question type does not work properly for native mobile surveys for Android

</td><td>

Users observe that when navigating through the **Next** button in the mobile UI for survey questionnaires, attachments do not auto-save.

</td><td>

1.  Log in to the Now Mobile app.
2.  Navigate to **My Tasks** &gt; **Attachment question issue task**.
3.  Click the short description 'Attachment question issue task'.

A survey opens.

4.  Answer the questions and add an attachment for the attachment type question.
5.  Submit the survey.

Observe that submitting does not work if you click the **Previous** button. Returning to the attachment question, the attachment that you selected is not present. Because the attachment question was mandatory, the survey is not submitted.

6.  Add an attachment again, click the **Next** button, and submit the survey.

 This time, it works as expected. The issue is that the attachment response is removed when you answer the next question after the attachment question.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1503249

</td><td>

Talkback does not announce the correct role for the tab and the position count for the 'Applications' control through the 'My approvals' control

</td><td>

The same issue is observed for all controls present throughout the application on Android devices.

</td><td>

1.  Enable Talkback and open the app.

The log in screen appears.

2.  Enter an instance and try with the demo account.
3.  Navigate to **Service Desk agent** &gt; **Launch Demo**.
4.  Navigate to the 'Applications' control through the 'My approvals' control.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1504811

</td><td>

Talkback does not announce the role as a 'button' for the control under the 'Instance' screen

</td><td>

 

</td><td>

1.  Activate TalkBack.
2.  Add an instance.
3.  Log in and log out.
4.  On the instances list, select the instance added in step 2.

 Expected behavior: The element should be described as a 'button'.

 Actual behavior: Talkback reads the name of the instance, the URL, and the list.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1507052

 [KB0965723](https://hi.service-now.com/kb_view.do?sysparm_article=KB0965723)

</td><td>

Users cannot submit a survey in the Agent Mobile app for Android when a survey field is mandatory but hidden based on previous options

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1509370

</td><td>

The function condition does not work for the 'Media' section functions

</td><td>

Android mobile apps ignore the condition in the function when the function is added to the 'Media' section.

</td><td>

1.  Create a function \(sys\_sg\_button\).
2.  Add the condition as '!gs.hasRole\('itil'\)' to the function.
3.  Create a 'Media' section for any applet launcher on the Now Mobile app.
4.  Add a function instance to the 'Media' section using the function created in step 1.
5.  Log in to the Now Mobile app as an ITIL user on an Android device.

Notice that the function instance appears.

6.  Log in to the Now Mobile app on an iOS device.

The function instance does not appear.


 Expected behavior: The function instance should not appear for the ITIL user on the Android device.

 Actual behavior: The function instance in the 'Media' section ignores the function condition.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1512300

</td><td>

Null pointer exception performance instability in the UI policy controller

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1513151

</td><td>

YouTube playlist links are rendered broken in the Now Mobile and Onboarding apps

</td><td>

The issue is observed when YouTube playlist links are used in an onboarding task or comments on a RITM. When users click the link, it opens YouTube with the error 'This video is unavailable'.

</td><td>

1.  Open a Paris base instance.
2.  Raise any request from the service catalog and enter a YouTube link in the RITM comments.
3.  Log in to Now Mobile as the user that the RITM is requested for.
4.  Click the 'For Me' tab.
5.  From the 'My request' list, navigate to the RITM created in step 2.
6.  Navigate to the updates tab and click the YouTube link.

 The link takes you to the YouTube app and an error is observed: 'This video is unavailable'. The same issue occurs on the Onboarding app, when using sn\_hr\_core\_template with a YouTube playlist link. When the resulting task is accessed, the Onboarding app gives the same error.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/onboarding-intune-available-versions.md)

