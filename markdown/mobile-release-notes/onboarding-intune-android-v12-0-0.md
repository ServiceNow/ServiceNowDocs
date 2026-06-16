---
title: ServiceNow Onboarding - Intune for Android v12.0.0
description: The Android v12.0.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-intune-android-v12-0-0.html
release: mobile
topic_type: reference
last_updated: "2021-04-15"
reading_time_minutes: 3
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for Android v12.0.0

The Android v12.0.0 release provides fixes for the application.

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

 PRB1457409

 [KB0957064](https://hi.service-now.com/kb_view.do?sysparm_article=KB0957064)

</td><td>

Translation on the Now Mobile Android app for **Add comments** does not work

</td><td>

An incident's 'Updates' screen section has a button for **Add comments**, which is not translated on Android devices.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1460396

</td><td>

AppAuth networking does not use GDSocket for BlackBerry

</td><td>

To enable mobile application management features, AppAuth's network calls need to use BlackBerry's GDSocket from their library. This issue occurs with Androids only.

</td><td>

1.  Set up the Now Mobile Blackberry app, so that the app logs into the instance with a proxy via Unified Endpoint Management \(UEM\).
2.  Log in to an instance.

 Observe in the node logs on the instance that there are two different VPNs, and the OAuth calls are from a different VPN than the rest of the app calls.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1478980

</td><td>

Virtual Agent choice list and reference options are truncated on the mobile app

</td><td>

Users can rotate the screen on iOS, which in some cases assists with truncation. On Android, it is not possible to rotate the screen.

</td><td>

1.  Create a topic with a choice list that has long value and a short second choice, so the choice option displays.
2.  Start Virtual Agent on mobile and show all topics.
3.  Select the new topic.

 The long choice label is truncated with '....'.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1476722

</td><td>

Talkback focus requires extra swipes on the 'My incidents' control while navigating using the swipe gesture

</td><td>

While navigating through incidents with Talkback turned on, focus for each button requires two swipes: first the icon, then the label.

</td><td>

1.  Launch the Agent app and log in to the instance.
2.  Select the 'Incidents' tab.
3.  Turn on Talkback and navigate to 'My Incidents'.

 Expected behavior: Each item should take focus once.

 Actual behavior: The swipe right focus occurs first on the icon. On a second swipe right, the icon label takes focus.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1476945

</td><td>

Approving approvals does not take the user to the previous screen

</td><td>

This issue occurs when the ITSM Mobile plugin is active.

</td><td>

1.  Log in to the Now Mobile app as any user who can approve \(for example, admin\).
2.  On a desktop UI, navigate to any RITM and navigate to related lists approvers.
3.  Click **Edit** and add the user in step 1 as the approver.

In the mobile app, a push notification is redirected.

4.  Tap on the push notification.

An applet screen opens.

5.  Click **Approve**.

 Expected behavior: The app should redirect to the previous screen.

 Actual behavior: The mobile app remains on the same screen.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1477213

</td><td>

Search suggestions do not display

</td><td>

 

</td><td>

1.  Log in to the Now Mobile app.
2.  Tap the information ALP.
3.  Tap the search icon.
4.  Begin typing a common search term, like 'pho'.

 Expected behavior: The search suggestions with an arrow appear. Tapping a suggestion executes the search, and tapping an arrow next to the suggestion pastes the string in the search bar.

 Actual behavior: No suggestions appear.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1477239

</td><td>

Force local login does not work for the first attempt

</td><td>

When users first try to log in to the instance, the app does not redirect to the local login.

</td><td>

1.  If the Now Mobile app is already installed on an Android device, uninstall and reinstall it.
2.  Enter and log in to the instance.

The app will redirect to an SSO page, not local login.

3.  Close the SSO page using the **X** button.
4.  Click **Cancel Authentication**.
5.  Click the newly added instance again.

 The app will redirect to the local login page. This should occur with first login attempt.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1483265

</td><td>

The activity stream for the day of the updated date is appended at the end of the time stamp

</td><td>

 

</td><td>

1.  Change the device language to English \(India\).
2.  Log in to the instance from an Android device in the Now Mobile app.
3.  Navigate to **For me** &gt; **My Request** and open any RITM record.
4.  Navigate to the 'Updates' tab.
5.  Check the activity stream.

 The timestamp in the activity stream does not work as expected.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/onboarding-intune-available-versions.md)

