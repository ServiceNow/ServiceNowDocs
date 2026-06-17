---
title: Mobile Onboarding for Android v11.5.0
description: The Android v11.5.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2021-03-10"
reading_time_minutes: 5
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v11.5.0

The Android v11.5.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.onboarding). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_mwt_yjc_s4b" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile Android \(non-classic\)

 PRB1461022

</td><td>

Talkback does not announce a role for the 'My incidents' control

</td><td>

Users are unable to identify the purpose of the control. This issue can be replicated for all the controls present throughout the application on an Android device.

</td><td>

1.  Install the ServiceNow Agent application on the device.
2.  Enable Talkback and open the above app.

The login screen appears.

3.  Navigate to **Service Desk agent** &gt; **Launch Demo**.
4.  Navigate to the **My incidents** control using the swipe gesture.

 Observe whether Talkback announces role for 'My incidents' control.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1462783

</td><td>

Service Portal in the Now Mobile Android app has a Favorite/Ribbon icon that does not work as expected

</td><td>

It displays the error 'Error adding screen to favorites'.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1472982

</td><td>

The app has performance instability due to exceeding the parcelable 1MB buffer when creating a ParamsActivity

</td><td>

ParamsActivity cannot start because the size of the extras in the intent is too large.

</td><td>

1.  Log in to the Mobile Agent app.
2.  Navigate to 'All Service Request Tickets'.
3.  Navigate to the **Create a Ticket** function located at the top-right in the ellipsis icon.

 Expected behavior: The user should be able to create a ticket.

 Actual behavior: The application crashes.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1472364

</td><td>

Talkback does not announce 'EUSE Mobile' as a heading

</td><td>

Android Agent doesn't announce the page header as a header. The issue does not exist in the iOS client, only the Android client.

</td><td>

1.  Launch the Agent app.
2.  Select **Try with a demo account**.
3.  Select **Service Desk Agent**.
4.  Select **Launch Demo**.
5.  Turn on Talkback.
6.  Swipe left to 'Hello, \[Name\]'.

 Expected behavior: Talkback should announce 'Hello, \[Name\]. Header'.

 Actual behavior: Talkback announces 'Hello, \[Name\]'.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1463087

</td><td>

Talkback does not announce the confirmation message after activating the **Clear** control

</td><td>

Users will not get the information about the action performed by activating the **Clear** button.

</td><td>

1.  Launch the Agent app.
2.  Select **Try with a demo account**.
3.  Select **Service Desk Agent**.
4.  Select **Launch Demo**.
5.  Next to 'My Incidents', select **See All**.
6.  Turn on Talkback using the shortcut key.
7.  Double tap the filter icon.
8.  Enter any search criteria.

This activates the **Clear** button.

9.  Double tap the **Clear** button.

 Expected behavior: Talkback should announce something like 'Cleared Successfully'.

 Actual behavior: The entries you made will clear, and the **Clear** button will become inactive. Talkback does not read out a status message.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1422908

</td><td>

Choice lists do not work in offline mode

</td><td>

When the offline mode plugin is enabled, and applets and their functions have been deemed to be available offline, any UI parameters in the functions that reference other fields do not return any data.

</td><td>

1.  Log in to an instance with ITSM Mobile Agent and offline mode is enabled.
2.  Make the incident launcher, the group incident section, the 'unassigned by priority' applet, and the corresponding functions available offline \(specifically the **Edit** function\).
3.  Open the incident in the Agent Mobile app for Android, download the cache, and switch to offline mode.
4.  Open a record via the incident launcher, the group incident section, the 'unassigned by priority' applet, and click into one of the records to open the form screen.
5.  Click the **Edit** top menu function.
6.  Try to change 'Category' and update 'Subcategory'.

 'Category' and 'Subcategory' are not updating properly and their values match the choice field on the platform incident table for the edited record. After changing the inputs offline, they are synced properly when going back online.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1458769

</td><td>

The Appsee Open Applet event can have a null title

</td><td>

Appsee requires a title for the Open Applet event. In some cases, there isn't a title to send.

</td><td>

1.  Log in to the instance.
2.  Navigate **Analytics** &gt; **Event** &gt; **Open applet**.

 Observe that the applet name is missing for 'My approval', and only for the data coming from an Android device.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1452827

</td><td>

In Virtual Agent in the Mobile app, attachments are not added to incidents created from the chat

</td><td>

They are, however, being added to the sys\_cs\_ conversation\_task table.

</td><td>

1.  Configure the instance for Virtual Agent Chat.
2.  Initiate Virtual Agent Chat.
3.  Select the 'Report a problem' topic.
4.  Complete the required fields.
5.  Upload an image.

 Expected behavior: Navigate to platform and validate the attachment is added to the newly created incident.

 Actual behavior: The attachment is in the sys\_conversation\_task table, but not in the incident table.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1451988

</td><td>

Color contrast issues on the clear cache/offline mode pages

</td><td>

 

</td><td>

1.  Navigate to 'My work'.
2.  Have accessibility scanner tool enabled on Android.

 Color contrast issues are seen on several pages, like offline mode/clear cache. Notice that clear cache/offline mode does not have sufficient color contrast of 3:1, since they are large text.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1447554

</td><td>

'Provide Virtual Agent Feedback' loops when trying to enter extra information

</td><td>

This issue is observed while using Now Mobile on an Android device. When the 'Provide Virtual Agent Feedback' agent topic is present to a user, if the user selects **Bad** and tries to enter a reason, the topic loops and they are asked for a reason again. This issue does not happen in a browser or on iOS. There are no errors, just a message that Virtual Agent does not understand the entered text.

</td><td>

1.  Install Glide Virtual Agent and ITSM Mobile Experience.
2.  Enable the chat on an applet launcher.
3.  Use Now Mobile on Android to access the instance and select **Chat**.
4.  Select 'Virtual Agent Feedback' from the list of topics.
5.  Select **Bad**.
6.  Try to enter a reason after the prompt.

The prompt is displayed again.


 Expected behavior: The topic should accept the text and close the chat.

 Actual behavior: The topic loops.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1473743

</td><td>

The SearchList UI parameter does not update the screen when no results are found

</td><td>

When searching a SearchList, if the search returns no result, the screen does not refresh appropriately on an Android and the 'Total Found' count still displays.

</td><td>

1.  Select **My Inventory**.
2.  Select **Available Parts**.
3.  Search for a string that will return no results.

 On iOS, you see 'No results found', which is correct. On Android, you see nothing on the main screen, and under the search dialog the 'Total Found: xxx' text is still there showing the total record count, which is incorrect.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

