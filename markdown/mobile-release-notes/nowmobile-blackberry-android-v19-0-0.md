---
title: Now Mobile for BlackBerry for Android v19.0.0
description: The Android v19.0.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2024-12-05"
reading_time_minutes: 3
breadcrumb: [Now Mobile for BlackBerry app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for BlackBerry for Android v19.0.0

The Android v19.0.0 release provides fixes for the application.

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

 PRB1793478

</td><td>

A barcode scanner value is not correctly processed when the scanner is opened from CellsFragment

</td><td>

The data for a scanned barcode is replaced by the data for the next barcode scanned.

</td><td>

1.  Log in to the Agent app.
2.  Navigate to **Jump to Barcode** under the Rounds section.
3.  Scan barcode1.png.
4.  Select **Healthy** / **Unhealthy** and submit \(if the buttons are not visible, skip this step\).
5.  Select **Jump to Next Barcode**.
6.  Scan barcode2.png.

 Expected behavior: The data for barcode 2 shows on the CellsFragment. Selecting the **Back** button shows the user the FormScreenFragment for barcode 1's data, and then selecting it again takes the user back to the ALP.

 Actual behavior: The data for barcode 2 shows on the CellsFragment, then is replaced by the data for barcode 1 after a few seconds \(when client refresh finishes\). Also, seleting the **Back** button takes the user to the ALP instead of back to a previous FormScreenFragment.

</td></tr><tr><td>

Mobile Android

 PRB1806088

</td><td>

Special characters such as '&lt;' '&gt;' and '&amp;' do not render/escape properly in the Activity Stream

</td><td>

The characters are rendered incorrectly in the output.

</td><td>

1.  Log in to Agent Mobile as a user assigned to a Work Order task \(or impersonate a user who is assigned to one\).
2.  Open a WOT record.
3.  Type &lt;&gt;&amp; into the Work Notes in the Activity Stream of the record.

 Notice that it renders as &amp;lt;&amp;gt;&amp;amp;.

</td></tr><tr><td>

Mobile Android

 PRB1815140

</td><td>

The **Close** button of the MESP catalog item page doesn't work when the link is opened from the Virtual Agent chat

</td><td>

When a Virtual Agent topic returns a link response node that opens an MESP catalog item page, the **Close** button doesn't work after submitting the catalog item.

</td><td>

1.  Enable chat in the Now Mobile homepage.
2.  Select the chat and initiate Virtual Agent chat.
3.  Select **Show me everything.**
4.  Select the topic created above.
5.  Select the link and open the MESP page.
6.  Fill in the form and submit.
7.  Select the **Close** button.

 Expected behavior: The MESP is closed and the user is returned to the VA interface.

 Actual behavior: Selecting the **Close** button does nothing.

</td></tr><tr><td>

Mobile Android

 PRB1794535

</td><td>

The user can't copy field values

</td><td>

The option to copy text from fields does not appear when the screen fields = 19 or more.

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1814112

</td><td>

A pre-filled instance URL is not populated when the optional **Nickname** field is empty

</td><td>

On a mobile publishing Android build, the instance URL should be populated regardless of whether the **Nickname** field is empty or not.

</td><td>

1.  Submit a mobile publishing Android build.
2.  In the Login Management section, fill in the **Default app instance** field but leave the optional **Nickname** field empty.
3.  Once the build is ready, install and check the pre-filled instance.

 Expected behavior: The instance is populated because the instance URL was provided.

 Actual behavior: The instance is not populated.

</td></tr><tr><td>

Mobile Android

 PRB1780908

</td><td>

The user observes a 'You are offline' message and an incorrect order of messages in the agent chat window

</td><td>

When chat is initiated and the user has left the chat for over one minute, the user observes a message reading 'You are offline', and the messages sent by Agent go out of order.

</td><td>

1.  Initiate a chat and make the app run in the background.
2.  Send messages to the user after waiting 30 seconds.
3.  Re-open the app by clicking the notification.

 Notice a message that reads 'You are offline' on top of the chat window. Also, the order of messages is sometimes incorrect.

</td></tr><tr><td>

Mobile Android

 PRB1822056

</td><td>

A page reload script doesn't work properly

</td><td>

A script that reloads a webpage when the user switches between tabs does not work on Android.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile for BlackBerry app version history](../nowmobile-blackberry-available-versions.md)

