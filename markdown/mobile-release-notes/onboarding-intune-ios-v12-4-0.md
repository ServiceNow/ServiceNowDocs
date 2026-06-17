---
title: ServiceNow Onboarding - Intune for iOS v12.4.0
description: The iOS v12.4.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2021-08-19"
reading_time_minutes: 4
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v12.4.0

The iOS v12.4.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding/id1472486882). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

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

Mobile iOS \(non-classic\)

 PRB1447561

</td><td>

VoiceOver does not announce the label 'Enter the instance address...' when the focus moves to its edit field

</td><td>

If the label 'Enter the instance address.....' is not announced by VoiceOver, screen reader users will be left unaware about the control and will not be able to perform the desired actions.

</td><td>

1.  Enable VoiceOver and open the app.

The login screen appears.

2.  Navigate to the edit field 'example.service-now.com' via swipe gestures.

 Notice that VoiceOver does not announce the label 'Enter the instance address...'.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1497695

</td><td>

Characters like 'Æ', 'Ø' or 'Å' do not render properly in the attachment name in the activity stream in the Agent mobile app

</td><td>

 

</td><td>

1.  Attach any PDF with a name containing Æ, Ø or Å on any work order task or incident.
2.  Open the activity stream.

 Expected behavior: It should be rendered properly.

 Actual behavior: It is not rendered properly in the activity stream in the Agent mobile app.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1502747

</td><td>

Allow admin users to control the error message

</td><td>

When uploading an attachment, there are a few messages that may appear: business rules, error messages returned by the platform, and mobile messages. When an attachment is loaded from the activity stream, only the generic mobile message 'The file upload failed' is presented.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1504746

</td><td>

The instances list does not identify each control as a button

</td><td>

 

</td><td>

1.  Activate VoiceOver.
2.  Add an instance.
3.  Log in and log out.
4.  On the instances list, select the instance added in step 2.

 Expected behavior: The element should be described as a 'button'.

 Actual behavior: VoiceOver reads the name of the instance, the URL, and 'actions available'.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1505604

</td><td>

VoiceOver doesn't announce the**Enter the instance address.....** edit field as required when it receives focus while navigating using swipe gestures

</td><td>

Screen reader users are impacted if VoiceOver doesn't announce the **Enter the instance address.....** edit field as required when it receives focus while navigating using swipe gestures and they will not receive the correct information.

</td><td>

1.  Enable VoiceOver and open the ServiceNow Agent mobile app.

The login screen appears.

2.  Navigate to the edit field 'example.service-now.com' via swipe gestures.

 Expected behavior: VoiceOver should announce the **Enter the instance address.....** edit field as required" when it receives focus while navigating using swipe gestures.

 Actual behavior: VoiceOver doesn't announce the **Enter the instance address.....** edit field as required.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1509181

</td><td>

VoiceOver does not announce role for the **View** control while navigating via swipe gestures

</td><td>

As a result, screen reader users will not know the functionality of the control.

</td><td>

1.  Enable VoiceOver and open the Agent mobile app.

The login screen appears.

2.  Select the 'Try with a demo instance' link and choose 'Service desk agent' as the persona.
3.  Navigate to **My work** &gt; **My incident**.

The 'My incident' screen appears.

4.  Navigate to the **...** control via a swipe gesture and activate it.
5.  Activate the **New** control.

The 'New Button \(Incident\)' screen appears.

6.  Complete the required fields and activate the **Submit** control.

A confirmation message appears.

7.  Navigate via swipe gestures and observe whether VoiceOver announces the role for the **View** control.

 Expected behavior: VoiceOver should announce the role for the **View** control while navigating via swipe gestures. VoiceOver should announce it as 'View messages, button'.

 Actual behavior: VoiceOver does not announce the role for the **View** control while navigating via swipe gestures. VoiceOver announces it as 'View'.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1510166

</td><td>

Korean characters in attachment file names do not work as expected in iOS mobile apps

</td><td>

When checking a ticket with Korean documents attached on mobile, Android devices work as expected, but Korean characters do not work as expected in iOS devices.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1513730

</td><td>

PDF documents to sign or acknowledge for the Onboarding app do not load in iOS when a user is being impersonated

</td><td>

 

</td><td>

1.  In the Onboarding app on an iOS device, log in to the instance.
2.  Select **Settings**.
3.  Tap the profile icon and select **Impersonate User**.
4.  Search for a user and select a result.
5.  In the 'Welcome' tab, scroll to 'Day 2 Activities' and tap it.
6.  Open the first record in the list screen \(Review &amp; Sign Form\).

 Expected behavior: The PDF in the To-do section should load.

 Actual behavior: The PDF area says 'Content Unavailable'.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1513847

</td><td>

Incorrect navigation bar appearance for the modal browser screen

</td><td>

The incorrect colors are displayed in the navigation bar when a Cabrillo modal is launched from a URL browser. The navigation bar background color should be the brand color and the buttons and title should be white. However, the background color is white, so the buttons are not visible.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](../onboarding-intune-available-versions.md)

