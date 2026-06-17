---
title: Mobile Onboarding for Android v15.5.0
description: The Android v15.5.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2023-03-02"
reading_time_minutes: 3
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v15.5.0

The Android v15.5.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.onboarding). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## New feature

Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

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

Mobile Android

 PRB1635680

</td><td>

Read-only fields are lighter in color, causing issues for the user in bright conditions

</td><td>

 

</td><td>

Configure an instance with an input screen with a disabled Text field.

 Open in the app and notice that the disabled field color is not easily readable.

</td></tr><tr><td>

Mobile Android

 PRB1634452

 [KB1222988](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1222988)

</td><td>

Performance degradation when launching the app, starting in v15.3.0

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Android

 PRB1635831

</td><td>

Empty Android notification remains after deleting all notifications from the in-app notifications tab

</td><td>

Deleting all notifications one by one from the in-app notifications tab leaves an empty summary notification in the phone notifications that has to be manually cleared.

</td><td>

1.  Navigate to **Inventory** &gt; **My Recent SCO's** &gt; **My Supply Chain Order**.
2.  Select any SCO in Draft state and click submit order. Wait a few moments to see the notification arrive in both the in-app notifications tab as well as the Android notification bar.
3.  Repeat steps 1 and 2 to create another notification.
4.  Verify that the Android notifications bar has two notifications.
5.  From the in-app notifications tab, swipe the first notification left and **Delete** it.

Notice that the notification disappears and there’s only one left in the Android notifications bar.

6.  From the in-app notifications tab, swipe the notification left and **Delete** the remaining one.

 Notice that the last notification deleted is replaced by what looks like an empty notification.

</td></tr><tr><td>

Mobile Android

 PRB1640523

</td><td>

Stockroom numbers aren’t correct on the map while swiping the cards from left to right and right to left

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1639315

</td><td>

The user is immediately forced to log out if unable to refresh the access token

</td><td>

The user is logged out even though they have a valid refresh token.

</td><td>

1.  Optional: In the oauth\_entity table, open the record for Agent or NOW \(whichever one will be used\) and modify the Access Token Lifespan to be short \(e.g. 30\).
2.  Set up the app's network calls to go through a certain user.
3.  Use the app chosen in step 1 to log in to an instance.
4.  Look at oauth\_token.do response and verify that 'expires\_in' occurs soon \(for example, the value might be 20 if the access token lifespan was set to 30 in step 1\).
5.  Set a breakpoint on the oauth\_token.do call in the certain user.
6.  After the access token has expired, force the app to make a network call \(for example, pull to refresh\).
7.  Use the user selected in step 2 to force the oauth\_token.do network call to fail \(for example, abort the network call\).

 Observe that the user is logged out even though they have a valid refresh token.

</td></tr><tr><td>

Mobile Android

 PRB1637456

</td><td>

App crashes after updating due to a SQLCipher error

</td><td>

 

</td><td>

1.  Install 15.3.0 Now App \(Intune v8.3\).
2.  Launch the Now App 15.3.0.
3.  Install the Company Portal.
4.  Launch the Now app again.

Observe the performance instability.

5.  Update to 15.4.0 \(Intune v9.1.0\).
6.  Relaunch.

 Expected behavior: The user is able to upgrade to the 15.4.0 version and log in to the app with no issues.

 Actual behavior: The users observes SQLCipher exceptions when upgrading.

</td></tr><tr><td>

Mobile Android

 PRB1630050

</td><td>

The input form screen shows the keypad even though focus is removed from the fields

</td><td>

 

</td><td>

1.  Log in to any Tokyo instance with the Field Service Management and Field Service Management for Mobile Plug-in installed.
2.  Impersonate any user with a work order task in Agent Mobile.
3.  Open any work order task in WIP and from the top menu options, select **Log incidental**.
4.  Set **Type**'to **Mileage**.
5.  Focus on **Cost per mile** and then scroll

 Observe that the screen focus is removed from cost per mile but the keypad still appears.

 Or

 1.  Open an action screen from a function where there is a high number of UI parameters \(fields on the action screen\).
2.  Focus on a text field.
3.  Scroll up or down.

Notice that the control is gone from the text field.


 Notice that the TextPad is still present on the action screen.

</td></tr><tr><td>

Mobile Android

 PRB1633686

</td><td>

Mobile 15.3.0 crashes on Offline Background Sync

</td><td>

The Agent Mobile app closes or asks the user to clear cache.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

