---
title: Now Support for Android v18.0.0
description: The Android v18.0.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2024-07-04"
reading_time_minutes: 7
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Now Support for Android v18.0.0

The Android v18.0.0 release provides fixes for the application.

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

 PRB1751431

 [KB1638841](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1638841)

</td><td>

The Agent Mobile App crashes when opening an applet

</td><td>

The Agent Mobile App crashes when opening an applet using a button in a card template referring to Next Experience CSS variables if Next Experience UI is disabled

</td><td>

1.  Set the system property 'glide.ui.polaris.experience' to false to disable the Next Experience UI.
2.  Log in to the Agent Mobile App.
3.  Navigate to **My work** &gt; **My tasks**.
4.  Tap to open a record.

 Expected behavior: The record should be opened successfully in the Agent Mobile App.

 Actual behavior: The record is opened but the Agent Mobile App crashes.

</td></tr><tr><td>

Mobile Android

 PRB1754838

</td><td>

Multiple barcode scans get appended instead of being processed separately using an external barcode scanner connected through Bluetooth

</td><td>

 

</td><td>

1.  Use Scan-To-Connect Utility App on Android device to pair the Zebra DS2278-SR via bluetooth.
2.  Select the 'Inventory' tab.
3.  Select the **Add asset multiscan** quick action.

Note that the first field is not automatically focused, the user has to tap.

4.  Scan barcodes using Zebra DS2278-SR.

 Expected behavior: Multiple barcode scans should be processed separately. After one barcode is scanned, the app should automatically move to scan for the next value instead of appending the next value to the first scan.

 Actual behavior: Multiple barcode scans get appended instead of being processed separately. This occurs for multiscan and groupscan.

</td></tr><tr><td>

Mobile Android

 PRB1771121

</td><td>

The user is unable to copy some fields on the details screen

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Android

 PRB1759490

</td><td>

The Activity Stream crashes if any comment contains HTML with an IMG tag that doesn't have a source link

</td><td>

A malformed image tag passes a null URL parameter to the code, which is not expecting a null. This results in a crash.

</td><td>

1.  Log in to the Agent mobile app.
2.  Search for a case record and open it.
3.  Navigate to the tab 'Activity Stream'.
4.  Scroll all the way down.

 Observe that the app crashes and closes.

</td></tr><tr><td>

Mobile Android

 PRB1735791

</td><td>

The **Back** button on an Android device sends the user to the main list rather than the previous screen

</td><td>

The behavior is different when using the **Back** button of the Now Mobile App and the **Back** button of the Android phone. If the user selects the back arrow on the upper left corner of the screen, they navigate back to the list of articles as expected. However, if they select the Android **Back** button, they are sent back to the main screen.

</td><td>

1.  Open the Now Mobile app.
2.  Navigate to the 'Support' tab in the lower part of the screen.
3.  In 'Browse all topics', select **See all**.
4.  Select IT5.
5.  Select any topics in IT topics.
6.  Choose any topic that is available.
7.  Select an article.
8.  Select the **Back** button of Android mobile.

 Expected behavior: The user should be navigated one step behind the current step.

 Actual behavior: It goes back to the **Browse all topics** &gt; **See all** screen.

</td></tr><tr><td>

Mobile Android

 PRB1749164

</td><td>

The **Cost** field on the Log Incidental Input form screen shows discrepancies in certain values between iOS and Android

</td><td>

This discrepancy only occurs during the creation process of logging an incidental. Once the user submits, the same value is displayed on both iOS and Android clients.

</td><td>

1.  Navigate to a Vancouver instance.
2.  Select **More** &gt; **Field Service** tab.
3.  Open any active wm\_task record from All tasks.
4.  Select the top menu function and then select **Log incidental**.
5.  Create one incidental Record:
    1.  Type: Mileage
    2.  Cost per mile: 0.34
    3.  Quantity: 10

 In iOS, the user observes the value 3.4 in the **Cost** field. In Android, the user observes the value 3.4000000000000004.

</td></tr><tr><td>

Mobile Android

 PRB1751891

</td><td>

Selecting the **Accept** footer button multiple times causes a server error

</td><td>

When the user selects the **Accept** or **Mark as complete** button, there is no indication to the user that the action was submitted. If the user selects one of these buttons again, an 'Insufficient privileges' error displays because the button was already selected.

</td><td>

1.  Navigate to 'Home'.
2.  Under the section 'My Onboarding', select any Open task.

Notice that the user is redirected to the 'Active set' page.

3.  Select **Post-Offer**.
4.  Select any task.
5.  Select **Accept**.

 Observe the 'Insufficient privileges' error.

</td></tr><tr><td>

Mobile Android

 PRB1744211

</td><td>

A comma character is not accepted in a **Number** input field in an Agent Mobile instance with the language set to German

</td><td>

In German, a comma is used instead of a period as a decimal separator. However, a comma character is not accepted in a Number field.

</td><td>

1.  Provision an instance with the language set to German.
2.  Navigate to the Meine Arbeit tab.
3.  Select the first work order task.
4.  Select the three dots and select the last option.
5.  In the **Gearbeitete Zeit** field, try to enter a comma.

 Observe that a comma is not allowed in the field.

</td></tr><tr><td>

Mobile Android

 PRB1761248

</td><td>

Offline related lists don't display multiple pages

</td><td>

Only the first 20 records in a related list are shown because multiple pages can't be loaded in offline mode.

</td><td>

1.  Provision a Vancouver instance.
2.  Create a related lists screen and mark it for offline.
3.  Ensure that the destination screen from the related list is marked for offline and has more than 20 records.
4.  Go offline.
5.  Open the related list while offline.

 Expected behavior: The user can scroll to view all records.

 Actual behavior: Only the first 20 records are returned and no additional pages are loaded.

</td></tr><tr><td>

Mobile Android

 PRB1703985

</td><td>

An indoor map crashes when there is no location to display or no floor selected

</td><td>

When the user tries to load a map by selecting the **Next** button, the app quits and loads again, taking the user to the home screen.

</td><td>

1.  Navigate to **Home ALP** &gt; **Quick actions \(+\)** &gt; **Make a reservation** &gt; **Desks** &gt; **Browse by neighborhood**.
2.  On the input form screen, select:
    1.  Neighborhood: WSD NH
    2.  Building: Building B, Floor 5
    3.  Toggle map view: on
    4.  Select the **Next** button.

 Expected behavior: Notice an empty state screen showing, 'Nothing matched your search/Try adjusting your search criteria'.

 Actual behavior: The app crashes \(but only the Parameter Activity. The Tabs Activity may still run in the background\).

</td></tr><tr><td>

Mobile Android

 PRB1756967

</td><td>

Delays in deactivating the **Submit / Next page** buttons on an input form screen with mandatory barcode input

</td><td>

If an input form is configured with a mandatory barcode input and the input is filled and then removed, there is a moment that the **Submit** \(or **Next page**\) button is still enabled. Users can proceed with form submission \(or proceed to the next page\), resulting in a skipped mandatory field in form submission.

</td><td>

1.  Configure an input form screen with a mandatory barcode input.
2.  Configure a function to open the input form screen.
3.  Log in to the instance on an Android device.
4.  Open the input form screen via the function.
5.  Fill the barcode input.

Observe the delays of activating the **Submit** button.

6.  Clear the input field.

Observe the delays from deactivating the **Submit** button.

7.  Fill in the input then clear the input, and immediately select the **Submit** button.

 Expected behavior: The **Submit** \(or **Next page**\) button should be activated/deactivated immediately with a reflection of the changes in the barcode input field.

 Actual behavior: There is a delay in activating/deactivating the **Submit** \(or **Next page**\) button. It allows user to submit \(or proceed to the next page\) by skipping the mandatory field.

</td></tr><tr><td>

Mobile Android

 PRB1768949

</td><td>

The WebRTC API doesn't work on Android

</td><td>

 

</td><td>

1.  Log in to a Now Mobile instance.
2.  On Home, select **My Call**.

This brings up the AWS calling feature.


 Observe the banner, 'Please allow your browser to access your microphone and camera.'

</td></tr><tr><td>

Mobile Android

 PRB1726816

</td><td>

Text color is hard to read

</td><td>

The light text color is too low contrast to read against the white background.

</td><td>

1.  Log in to an instance on the mobile app.
2.  Launch **Make a reservation** from the quick actions '**...**' floating button.
3.  Select a reservable module: Desk.
4.  Select **Browse all** under **See what's available**.
5.  Toggle **All-day** to On.

 Notice that the text is too low contrast to read.

</td></tr><tr><td>

Mobile Android

 PRB1748251

</td><td>

The 'Uploading' dialog is not dismissed

</td><td>

 

</td><td>

1.  Open **My work** &gt; **My Tasks** and select a task.
2.  Navigate to the 'Maintenance Checklist' related list and open the maintenance record.
3.  Select **Update**.
4.  Attach a couple of photos.
5.  Select **Submit**.

 Observe that the number of 'Uploading files' is incorrect.

</td></tr><tr><td>

Mobile Android

 PRB1735812

</td><td>

Selecting the **Back** button brings to the user to the wrong screen.

</td><td>

The **Back** button navigates the user to the Home tab and shows a different launcher tab.

</td><td>

1.  Open the Now Mobile app.
2.  Navigate to 'Support' or any other launcher tab except home.
3.  Select the **Back** button of the Android mobile \(not on the top left\).

Notice that the app closes.

4.  Open the app again.

Notice that on the 'Support' or other launcher tab screen, the 'Home' Tab is selected.


 Expected behavior: The **Back** button navigates to the 'Support' or another launcher tab screen.

 Actual behavior: The **Back** button navigates to the Home tab and shows a different launcher tab.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../now-support-available-versions.md)

