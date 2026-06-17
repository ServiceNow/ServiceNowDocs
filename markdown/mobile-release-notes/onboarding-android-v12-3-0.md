---
title: Mobile Onboarding for Android v12.3.0
description: The Android v12.3.0 release provides fixes for the application.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2021-07-22"
reading_time_minutes: 2
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for Android v12.3.0

The Android v12.3.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Google Play store](https://play.google.com/store/apps/details?id=com.servicenow.onboarding). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_rfk_ksd_gqb" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile Android \(non-classic\)

 PRB1473907

</td><td>

Talkback focus is not visible after selecting the **Caller** edit field

</td><td>

Talkback focus is not visible after entering a value in the **Caller** edit field. Focus should move back to the **Caller** field after selecting **Caller**.

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1488646

</td><td>

When there is more than one message, HTML tags and formatting are shown

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1490446

</td><td>

When a choice list UI parameter is mandatory, the user can submit the action when 'None' is selected

</td><td>

 

</td><td>

1.  In Studio, create a simple list and form applet that uses 'incident' as the table.
2.  Create an update action item.
3.  In this action item, create the item parameter 'contact type' and set the **Contact type** field to this item parameter using the data pill picker.
4.  Create a button with a record context, and choose the action item you created in step 2.
5.  Create a mandatory UI parameter of the choice list type, and point it to the **Contact type** field in the incident table.
6.  Map the UI parameter to the item parameter in the 'Action parameters mapping' tab under your button.
7.  Add this button to the form applet you created.

 Expected behavior: The button should open a page to let the user select the contact type. Because this UI parameter is mandatory, the user should not be allowed to submit the action when 'None' is selected, as 'None' represents an empty value.

 Actual behavior: The user is able to submit the action even when choosing 'None'.

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1497329

</td><td>

If the user exits before selecting an image when choosing or taking a photo in the Service Portal profile, the **Upload** button does not work

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Android \(non-classic\)

 PRB1501651

 [KB0963405](https://hi.service-now.com/kb_view.do?sysparm_article=KB0963405)

</td><td>

Embedded lists for the Android Agent mobile app do not work in offline mode

</td><td>

 

</td><td>

1.  Activate the ITSM Mobile plugin or ITSM Mobile Agent plugin.
2.  Log in as admin.
3.  Navigate to Studio.
4.  Create list applet incidents to show an incident.
5.  Create a parameterized list applet incident task to show tasks for the selected incident.
6.  Set the incident tasks applet as the embedded list for the incidents applet and set the relationship to **Incident Task** &gt; **Incident**.
7.  Add the list applet incidents to a section of an applet launcher.
8.  Set the applet launcher, incidents, and incident tasks applet 'Offline' to available.
9.  Open an incident record and add two incident tasks.
10. Log in via the Agent Mobile app on an Android device.
11. Access the incident record from step 9.

Notice the two incident task records in the embedded list.

12. Switch to offline mode.
13. Access the same incident record.

 Expected behavior: There should be two incident task records in the embedded list.

 Actual behavior: The selected incident record appears in the embedded list.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](../../now-support/now-support-available-versions.md)

