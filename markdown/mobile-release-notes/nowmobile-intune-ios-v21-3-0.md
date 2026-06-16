---
title: Now Mobile - Intune for iOS v21.3.0
description: The iOS v21.3.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-intune-ios-v21-3-0.html
release: mobile
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 4
breadcrumb: [Now Mobile - Intune app version history, Mobile app version history for iOS and Android]
---

# Now Mobile - Intune for iOS v21.3.0

The iOS v21.3.0 release provides fixes for the application.

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

iOS Mobile

 PRB1991062

</td><td>

Default date in the reservation screen is set to yesterday instead of today

</td><td>

The default date automatically fills the **Date** field on the 'Make a reservation' screen with yesterday's date instead of today.

</td><td>

1.  In the action menu select Make a reservation.
2.  Navigate to **Desks** &gt; **Browse all**.
3.  Toggle all-day to On, check the **Date** field.

 Notice that the auto-filled date is not the current date.

</td></tr><tr><td>

iOS Mobile

 PRB2001344

</td><td>

The date shown on the mobile device is not the same one displayed in the platform

</td><td>

Scheduled start and Estimate end time is not the same between the Mobile Agent App on iPhone and the platform.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2006489

</td><td>

A NSGenericException Task gets created in a session that has been invalidated

</td><td>

File upload gets stuck or the app crashes while uploading files in impersonation mode.

</td><td>

1.  Log in to the Agent app.
2.  Impersonate an agent.
3.  Open **WOT** &gt; **Activity** &gt; **Stream**.
4.  Upload any attachment.

 Expected behavior: The upload should be successful.

 Actual behavior: The upload gets stuck and the app intermittently crashes.

</td></tr><tr><td>

iOS Mobile

 PRB2011334

</td><td>

The Agent app crashes on iOS devices

</td><td>

When the user has a badge count over a certain value, the initializer traps with a fatal integer overflow, causing the app to crash.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2006738

</td><td>

iOS writeback returns HTTP 500 when an action has a parameter screen and AutoRedirectDestinationId is configured

</td><td>

When an action has both a parameter screen \(ParameterData\) and an AutoRedirectDestinationId configured server-side, the iOS mobile client includes DestinationSubmittedForm in the writeback request alongside ParameterData. The server does not accept this combination and returns HTTP 500.

</td><td>

1.  Configure a WOT close action \(or any action with a parameter screen\) on a ServiceNow instance that has AutoRedirectDestinationId set in the action's redirection configuration.
2.  Open the iOS Agent app and navigate to a Work Order Task record.
3.  Select the **Close** button to open the parameter screen.
4.  Fill in the required inputs \(close code, actual quantity, work notes\).
5.  Select **Submit**.

 Expected behavior: The writeback request is submitted successfully. The server responds 200 and the WOT is closed.

 Actual behavior: The server returns HTTP 500 and the WOT close action fails.

</td></tr><tr><td>

iOS Mobile

 PRB2011561

</td><td>

Restore the last page when pulling to refresh or session timeout

</td><td>

When the user reactivates their hybrid webpage session after timeout \(due to inactivity, backgrounding, or locking\) or performs a pull-to-refresh, they are not returned to their last visited page.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2009678

</td><td>

**Submit**/**Cancel** buttons freeze after a writeback error on an action item form

</td><td>

When filling in an action item form \(for example, a labor action item on a case\), submission returns a server-side error. The error banner is shown correctly but the **Submit** and **Cancel** buttons on the form become completely unresponsive. The user cannot retry submission or dismiss the form — the only recovery is to force-close the app.

</td><td>

1.  Open a case in iOS Agent Mobile.
2.  Tap an action item \(for example, Log Labor\) to open the action item form \(SGFormViewController\).
3.  Fill in the form fields.
4.  Select **Submit**.

Observe that the server-side error banner appears at the top of the screen.

5.  Attempt to tap **Submit** again \(to retry\) or **Cancel** \(to dismiss\).

 Expected behavior: Selecting **Submit** retries the writeback. Selecting **Cancel** dismisses the form.

 Actual behavior: Both **Submit** and **Cancel** are completely unresponsive.

</td></tr><tr><td>

iOS Mobile

 PRB2004817

</td><td>

The **Filter** button on list screens is hidden when the initial page load returns only one item and never re-appears after more items load via pagination

</td><td>

The **Filter** button should be shown on the top-right of the list screen if more than one item is displayed, but it doesn't appear.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2011924

</td><td>

Change Instance Alert is shown to the user when a notification is tapped on in the 'Notifications' tab for the same instance

</td><td>

 

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2007442

</td><td>

A smart assessment crashes when a descriptive element is set as richText

</td><td>

The application crashes.

</td><td>

1.  Navigate to **My work** &gt; **My schedule** and select a date.
2.  Open a Work Order Task that is in 'Work in progress'.
3.  Select **Take Questionnaire**.
4.  Open the available questionnaire.

 1.  Expected behavior: The questionnaire opens.
2.  Actual behavior: The application crashes.

</td></tr><tr><td>

iOS Mobile

 PRB2008581

</td><td>

An offline new-defect form photo is not visible in the Attachments/Activity Stream until sync

</td><td>

When a new record is created offline via the New Defect Form, callAddAttachmentsScript \(CellsContainerTemplateHandler+Redirection.swift\) returns early without calling addParameterScreenAttachments, so the offline document cache is never updated with the form-input attachment.

</td><td>

1.  Put the device into airplane mode \(fully offline\).
2.  Open the app and navigate to the New Defect Form.
3.  Fill in the required fields and attach a photo from the camera or photo library.
4.  Submit the form.
5.  Open the newly created defect from the All Defects opened by me list.

Observe that the Attachments and Activity Stream sections show 'No data available' and the photo is not visible.

6.  For comparison, add a second photo directly from the Activity Stream \(still offline\).

This photo appears immediately.

7.  Restore network connectivity and allow the app to sync.

 Expected behavior: The form photo is visible in Attachments and Activity Stream immediately after the defect is created, without requiring sync.

 Actual behavior: The form photo is invisible until sync completes.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/nowmobile-intune-available-versions.md)

