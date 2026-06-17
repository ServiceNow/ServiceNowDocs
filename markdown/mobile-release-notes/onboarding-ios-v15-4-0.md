---
title: Mobile Onboarding for iOS v15.4.0
description: The iOS v15.4.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-ios-v15-4-0.html
release: mobile
topic_type: reference
last_updated: "2023-02-02"
reading_time_minutes: 3
breadcrumb: [Now Support app version history, Mobile app version history for iOS and Android]
---

# Mobile Onboarding for iOS v15.4.0

The iOS v15.4.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-agent/id1446951408). Users can launch a demo to try the Mobile Agent. You can use a demo account from the initial post-download screen or the instance list screen.

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

Mobile iOS

 PRB1449441

</td><td>

In the iOS Mobile Apps, a second scroll bar can appear in the HTML fields

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1618804

</td><td>

A searchlist ignores the previous selections after a user makes another search

</td><td>

SGSearchPickerViewController resets the list of selected items \(selectedModelIndexes\) every time a new search is performed.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1627185

</td><td>

From the 'Approve' function and the 'Acknowledgement' message, re-direction to the login page isn't working in iOS devices

</td><td>

In an iOS device, it doesn't work when navigating from the 'Acknowledgement' message pop-up.

</td><td>

1.  Log in to any Tokyo instance with the Now mobile plugin installed.
2.  Open the 'Approve RITM without comment' function.
3.  Set the pre-condition as 'Re-authentication'.
4.  Create a string field.
5.  In the form layout, add the sysapproval\_approver table to use as the acknowledgement message field.
6.  Open the function record again.
7.  Navigate to 'Acknowledgement' messages.
8.  Check the acknowledgement text.

Two fields appear in the **Acknowledgement** field.

9.  Confirm the label.
10. Select the **Acknowledgement** field as a newly created string field.
11. Enter any label in the label field.
12. Open any approval record available under the 'My tasks' section. If there are none, try submitting any catalog item.
13. Provide approver details.
14. Move the state to 'Requested'.
15. Log in as that approver to see the approval record.
16. Ensure the approval record has the newly created string field with a value.
17. Once the approval record is clicked, verify 'Approve', 'Approve', and 'Reject' display.
18. Click **Approve**.

Pop-ups display with data in the **Acknowledgement** field.

19. Confirm the label text.

 Once the 'Confirm label' text is clicked, it redirects to the login page in an Android device but in iOS does nothing.

</td></tr><tr><td>

Mobile iOS

 PRB1627769

</td><td>

There is an issue with platform's bookmarks in iOS

</td><td>

A user has created two new lists, one to show the user's bookmarks \[sys\_ui\_bookmark\] and one to show the resulting record. When a user clicks on a bookmark record, the URL is passed to the second list's data item as a redirection destination field on the navigation function. This functionality works as expected on Android devices, but it's not working on any iOS devices. On iOS, the second list shows all the records for that table.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

 PRB1627978

</td><td>

Trying to display map items with invalid latitude or longitude coordinates crashes the app

</td><td>

The iOS app currently has no protections against invalid location coordinate values. It causes an app crash.

</td><td>

1.  Install the Field Service Management plugin on an instance with demo data.
2.  Edit a 'WOT Location' so that it has invalid latitude and longitude values.
3.  Save the changes.
4.  Log in to the Agent mobile app as a user that is assigned to that WOT.
5.  On the 'My Work' tab, tap **My Task Map**.

 The app crashes after a few seconds, or if a user tries to swipe through the cards.

</td></tr><tr><td>

Mobile iOS

 PRB1628663

</td><td>

'glide.sg.block\_mobile\_attachments\_sharing' doesn't work on Now Mobile and Agent apps for iOS

</td><td>

Despite setting the property glide.sg.block\_mobile\_attachments\_sharing to true on any San Diego/Tokyo instance, users can still see an option to share PDF attachments from the Now Mobile/Agent app.

</td><td>

1.  Create an incident on the standard platform.
2.  Update a PDF file as an attachment to the incident.
3.  Access this incident on the Now Mobile or Agent app.
4.  Click to view the attachment on Activity Screen.

Users can see the **Share** button on the right top area.

5.  Set the system property 'glide.sg.block\_mobile\_attachments\_sharing' to true.
6.  Wait to flush the instance cache when possible to not affect connected users.
7.  Access the incident on the Now Mobile app.
8.  View the attachment on Active Screen again.

 Expected Result: Users shouldn't see an option to share PDF attachments.

 Actual Result: Users can still share PDF attachments.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Support app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-support-available-versions.md)

