---
title: Now Mobile for Android v20.1.0
description: The Android v20.1.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2025-07-10"
reading_time_minutes: 2
breadcrumb: [Now Mobile app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for Android v20.1.0

The Android v20.1.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.fulfiller). Users can launch a demo to try the ServiceNow Agent app. You can use a demo account from the initial post-download screen or the instance list screen.

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

Android Mobile

 PRB1892998

</td><td>

A notification without a link displays 'Error loading URL'

</td><td>

 

</td><td>

1.  Navigate to **sys\_user.list** &gt; **firstname.lastname**.
2.  Update one of the fields to trigger a push \(for example, 'Business phone'\).

The user receives a notification.

3.  Open the notification tab.

 Observe the 'Error loading URL' page. When the notification is opened from the in-app notification screen, the message should be marked as ready and not error page should be shown. When the notification is opened from the notification drawer, it should foreground or open the app and no error should be shown. 

</td></tr><tr><td>

Android Mobile

 PRB1891450

 [KB2180813](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2180813)

</td><td>

In the Agent mobile app on Android, the keyboard disappears on a string input field if the user is not typing for more than couple of seconds

</td><td>

When filling in some of the string input fields on a input form screen in the agent app, the keyboard disappears after one sec of 'inactive' typing.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Android Mobile

 PRB1894135

</td><td>

Cabrillo screen rotates endlessly

</td><td>

When a Cabrillo screen is launched on a tablet with wide screen that has landscape default rotation, the screen changes rotation and locks incorrectly. the screen also refreshes upon rotating.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1886120

</td><td>

The full-screen option for videos does not function properly in KB articles

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1883284

</td><td>

When a page loads, the user must manually click to start scanning

</td><td>

Additionally, the and focus is not automatically focused on the scan field.

</td><td>

 

</td></tr><tr><td>

Android Mobile

 PRB1886481

</td><td>

Informational messages are not displayed consistently in offline when saving action item to the Outbox

</td><td>

 

</td><td>

1.  Download offline cache.
2.  Navigate to offline mode.
3.  Select **Open tasks** and find a task that has a questionnaire.
4.  Take a question to launch the input form screen.
5.  Fill the required fields and submit.

 Expected behavior: An message displays about saving to the Outbox.

 Actual behavior: No message is displayed.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile app version history](../now-mobile-available-versions.md)

