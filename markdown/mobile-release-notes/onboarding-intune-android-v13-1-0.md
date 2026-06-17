---
title: ServiceNow Onboarding - Intune for Android v13.1.0
description: The Android v13.1.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-intune-android-v13-1-0.html
release: mobile
topic_type: reference
last_updated: "2021-11-18"
reading_time_minutes: 4
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for Android v13.1.0

The Android v13.1.0 release provides fixes for the application.

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

 PRB1524579

</td><td>

Now Chat Android experiences performance instability on an unknown contact menu item type, like a link or text

</td><td>

Now Chat Android currently only supports 'Phone', 'Email' and 'Chat' type contact menu items. Anything besides these three causes Now Chat to close.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1533354

</td><td>

The 'Notification' tab icon is always a question mark

</td><td>

The 'Notifications' tab has a question mark icon instead of the bell icon.

</td><td>

1.  Log in to any instance as an agent.
2.  Notice that the 'Notifications' tab has a question mark icon instead of a bell icon.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1529983

</td><td>

YouTube channel links do not work correctly in the Android version of the mobile apps

</td><td>

The link opens in the YouTube app, but a 'This video is unavailable' message displays. In iOS, the link directs to the YouTube channel page.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1527200

</td><td>

The error message does not contain the field that is incorrect and VoiceOver reads only the error, not the affected field

</td><td>

When using filters in catalogs, the error message does not outline the field that is invalid. The error message only says that there is an error. As a result, VoiceOver does not dictate which field is invalid.

</td><td>

1.  Start VoiceOver.
2.  In the mobile app, navigate to the information tab.
3.  Select any category under 'Browse'.
4.  Move the input focus to the **Filter** button and select it to invoke the filter.
5.  In the **From** field, enter '9999' and in the **To** field, enter '1'.
6.  Click **Apply**.

 Expected behavior: An error message contains the error of an invalid field and also lists the field that needs to be corrected.

 Actual behavior: The error message says 'Missing or incorrect values'.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1526197

</td><td>

Loading an image fails due to an access token expiration

</td><td>

The image link appears but it is corrupt until the agent's log out and log in action is performed.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1510546

 [KB0966929](https://hi.service-now.com/kb_view.do?sysparm_article=KB0966929)

</td><td>

The Agent mobile app on Android has performance instability if there are too many questions in the questionnaire

</td><td>

Users observe that the **Next** button becomes slower as more questions are answered. The Agent mobile app experiences performance instability after about 60 questions are answered.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1524184

</td><td>

Changing the mobile device orientation reloads the catalog item form

</td><td>

This issue is observed on Now Mobile for Android.

</td><td>

1.  Log in to Now Mobile on an Android device.
2.  Navigate to a request catalog.
3.  Open 'Create incident catalog item'.
4.  Complete all mandatory fields in portrait mode and switch to landscape mode.

 As soon as the orientation is switched, the page refreshes.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1523000

</td><td>

The .msg file association is not present on mobile apps

</td><td>

The .msg file type is not able to open or download through the mobile app. Previously, the app allowed the file to be opened directly as long as there is a compatible application installed.

</td><td>

1.  Log in to the instance with the Now Mobile app.
2.  Open the incident with a .msg file attached.
3.  Try to open the attachment.

 Expected behavior: You are prompted with either the app selection to view the file or the option to download the file.

 Actual behavior: You are presented with the message 'Could not find an app to open .msg file'.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1520063

 [KB0998157](https://hi.service-now.com/kb_view.do?sysparm_article=KB0998157)

</td><td>

The header in the link type bot response is truncated on Android

</td><td>

 

</td><td>

1.  Log in to an instance with the required plugins for Virtual Agent.
2.  Create a topic in the designer.
3.  Add a bot response of the type 'Link'.
4.  In the header, enter something long.
5.  In 'Link', paste a URL.
6.  Open the Now Mobile app on Android and initiate the Virtual Agent chat.
7.  Select the topic you created.

 Expected behavior: It should not truncate and should behave the same way as in iOS

 Actual behavior: The header is truncated.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1517985

 [KB0994745](https://hi.service-now.com/kb_view.do?sysparm_article=KB0994745)

</td><td>

The 'Saved' view is not present on URL applets

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1513568

</td><td>

The mobile card displays differently on iOS and Android

</td><td>

The mobile card template builder 'customTemplate' renders differently in iOS and Android.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1535559

</td><td>

Users notice a 'the file upload failed' error even if the attachment is uploaded successfully

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/onboarding-intune-available-versions.md)

