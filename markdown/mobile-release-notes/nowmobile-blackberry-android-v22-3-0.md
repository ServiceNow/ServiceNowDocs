---
title: Now Mobile for BlackBerry for Android v22.3.0
description: The Android v22.3.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-blackberry-android-v22-3-0.html
release: mobile
topic_type: reference
last_updated: "2026-11-05"
reading_time_minutes: 5
breadcrumb: [Now Mobile for BlackBerry app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for BlackBerry for Android v22.3.0

The Android v22.3.0 release provides fixes for the application.

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

Mobile Android

PRB2086222

[KB3156993](https://hi.service-now.com/kb_view.do?sysparm_article=KB3156993)

</td><td>

Users on Android devices managed by Microsoft Intune are blocked from logging in to the mobile apps

</td><td>

Users on Android devices managed by Microsoft Intune are blocked from logging in to the mobile apps. This is because the administrator consent that was already granted in Intune for the iOS apps does not apply to the Android apps.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Android

PRB2084729

</td><td>

Some icons in the 'More' menu are displayed as error icons in the Now Mobile app

</td><td>

In the Now Mobile app, some icons that are assigned to tabs in the 'More' menu, for example, Score-List and Emoji-Smile Solid, are displayed as error icons. These icons are displayed correctly in the Mobile App Builder preview.

</td><td>

1.  In Mobile App Builder, change the icon of a tab in the 'More' menu of the Now Mobile app to the Emoji-Smile Solid icon.

Notice that the icon is displayed correctly in the Mobile App Builder preview.

2.  Log in to the Now Mobile app.
3.  Open the 'More' menu.

 Expected behavior: The Emoji-Smile Solid icon is displayed correctly.

 Actual behavior: An error icon is displayed instead of the Emoji-Smile Solid icon.

</td></tr><tr><td>

Mobile Android

PRB2082583

</td><td>

Starting travel or work on a work order task sometimes records an outdated location in the Agent mobile app on Android

</td><td>

In the Agent mobile app on Android, starting travel or starting work on a work order task sometimes records an outdated location. The same Global Positioning System \(GPS\) coordinates are recorded even after the user moves to a different location.

</td><td>

1.  On an Android device, log in to the Agent mobile app as a user who has work order tasks in the 'Assigned' state.
2.  Select the 'My Work' tab and scroll down to 'My Tasks'.
3.  Select a work order task in the 'Assigned' state.
4.  Select **Accept** &gt; **Start Travel** &gt; **Start Work**.
5.  Wait two to five minutes and physically move to a different location.
6.  Return to 'My Tasks', select a different work order task, and then select **Start Travel** and **Start Work**.
7.  Repeat steps five and six.

 Expected behavior: New GPS coordinates are recorded each time the user moves to a different location.

 Actual behavior: The same GPS coordinates are recorded even after the user moves to a different location.

</td></tr><tr><td>

Mobile Android

PRB2092800

</td><td>

The **Back** button stops responding on Field Service Management playbook pages in the Agent mobile app on Android

</td><td>

In the Agent mobile app on Android, the **Back** button stops responding after a user navigates to the Use a Part screen from a work order task. The user cannot return to the previous screen or the home page and must force close the app. This issue does not occur on iOS.

</td><td>

1.  On an Android device, log in to the Agent mobile app as a user who has assigned work order tasks.
2.  Navigate to **My Work** &gt; **All Tasks** &gt; **See All**.
3.  Open a work order task.
4.  Select **Start Work**.
5.  Select **Use Parts**, and then select **Use a Part**.
6.  Press the **Back** button.

 Expected behavior: The app returns to the screen where Use a Part was initiated, and the**Back** button remains responsive.

 Actual behavior: The**Back** button does not respond, and the app must be force closed.

</td></tr><tr><td>

Mobile Android

PRB2095006

</td><td>

Text in a string input is cleared when a choice is quickly selected from the choice input above it on Android

</td><td>

On an input form screen on Android, text that was entered in a string input is cleared when a user quickly selects a choice in the choice input directly above it. Selecting a second choice shortly afterward makes the text reappear. This issue does not occur on iOS.

</td><td>

1.  In Mobile App Builder, create an input form screen.
2.  In the input form screen settings, set the **Input form page display** field to 'Custom page and section setup'.
3.  Create a choice input with at least two options, and place it first in the order.
4.  Create a string input, and place it directly below the choice input.
5.  On an Android device, log in to the Now Mobile app or the Agent mobile app.
6.  Open the input form screen.
7.  Enter text in the string input.
8.  Quickly select one of the choices in the choice input.

 Notice that the text in the string input is cleared.

</td></tr><tr><td>

Mobile Android

PRB2095250

</td><td>

Knowledge articles opened from global search display a blank page in the Now Mobile app on Android

</td><td>

In the Now Mobile app on Android, opening a knowledge article from global search displays a blank page instead of the article. This occurs because the app opens an empty form that is attached to the search result instead of following the link to the article. The same article opens correctly on iOS and in the Service Portal.

</td><td>

1.  On an Android device, log in to the Now Mobile app.
2.  Select the Search icon in the app header.
3.  Search for a term that returns a knowledge article.
4.  In the search results, select the knowledge article.

 Expected behavior: The knowledge article opens.

 Actual behavior: A blank page is displayed instead of the knowledge article.

</td></tr><tr><td>

Mobile Android

PRB2089489

</td><td>

The mobile app crashes when syncing a large number of photos that were attached offline

</td><td>

After a user attaches a large number of photos to records on a legacy parameter screen while offline, the mobile app crashes when the device goes back online. This occurs because all pending photos are loaded into memory at the same time during offline sync, which uses up the available memory before the sync can complete.

</td><td>

1.  In Mobile App Builder, configure a legacy parameter input as a trailing swipe action for a list item, for example, a work order task.
2.  Open the mobile app and go offline.
3.  Across several records, attach approximately 100 images by using the legacy parameter input.
4.  Go back online.

 Expected behavior: The offline sync completes.

 Actual behavior: The app crashes.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile for BlackBerry app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-blackberry-available-versions.md)

