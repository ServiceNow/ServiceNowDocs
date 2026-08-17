---
title: Now Mobile for iOS v22.0.0
description: The iOS v22.0.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/nowmobile-ios-v22-0-0.html
release: mobile
topic_type: reference
last_updated: "2026-08-06"
reading_time_minutes: 8
breadcrumb: [Now Mobile app version history, Mobile app version history for iOS and Android]
---

# Now Mobile for iOS v22.0.0

The iOS v22.0.0 release provides fixes for the application.

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

 PRB2025495

</td><td>

Push notifications screen redirections show 'No Data'

</td><td>

The screen opens and shows 'No data'.

</td><td>

1.  Navigate to the 'Notifications' screen.
2.  Select a notification.

 Expected behavior: The screen opens with record details.

 Actual behavior: The screen opens and shows no data.

</td></tr><tr><td>

iOS Mobile

 PRB2008268

</td><td>

Client doesn't properly honor a 'Multi-select' search facet

</td><td>

The client should honor the user's multi select choice selection when querying the BE search API. Instead a white screen displays.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1994139

</td><td>

An error is thrown when the user selects a chart from the ALP

</td><td>

When the user selects a chart, and error is thrown reading 'Content can't be displayed'.

</td><td>

1.  Log in into the mobile app,
2.  Navigate to **More** &gt; **Visualization** &gt; **Regression**.
3.  Select any of the charts from the ALP.

 Observe that an error is thrown reading: 'Content can't be displayed'.

</td></tr><tr><td>

iOS Mobile

 PRB2007663

</td><td>

The icon badge notification count is not cleared after notifications are read remotely

</td><td>

NotificationsService updates appBadgeCount in UserDefaults after each successful API response, but never posts unreadPushNotificationCountDidChange. As a result, the OS badge is never updated to reflect the server's badge count during an active session.

</td><td>

1.  Receive a push notification on the mobile device.

The app icon badge increments to 1.

2.  Read or dismiss the notification on another device or via the web interface.
3.  Open the mobile app and navigate to the Notifications screen.

 Notice that the server confirms 0 unread notifications and the list appears empty, but the badge remains at 1.

</td></tr><tr><td>

iOS Mobile

 PRB2022936

</td><td>

Firebase crash

</td><td>

The error reads, 'Fatal Exception: NSInternalInconsistencyException: closure \#2 in CalendarViewController.addSubscribers\(for:\)'.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2027666

</td><td>

The orientation of the images captured using the 'Take Photo' function in the Now Agent mobile app is getting changed from portrait to landscape

</td><td>

In iOS devices, the images captured using the 'Take Photo' function in the Now Agent mobile app render horizontally when the original capture orientation was vertical \(portrait\). Specifically, the issue occurs when a photo is taken directly within the app, whereas images selected from the camera roll or recent files upload correctly in portrait orientation.

</td><td>

1.  In the Now Agent app, navigate to **Mobile Dispatch tab** &gt; **Rad/US/PICC card** &gt; **Scan Documents**.
2.  Take a picture directly using the in-app camera \(do not select from camera roll or recent files\).

 Observe that the image captured in portrait orientation within the Agent app appears in landscape \(horizontal\) orientation when it arrives in DMS.

</td></tr><tr><td>

iOS Mobile

 PRB2003734

</td><td>

Smart routing of List, Form, and KB links to apps doesn't work

</td><td>

 

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1949448

</td><td>

Focus does not start at the beginning of the page when selecting a location

</td><td>

When user selects location card, the focus does not consistently start at the top of the page.

</td><td>

1.  Navigate to **Asset tab** &gt; **Location audits** &gt; **More options** &gt; **New Location Audit** &gt; **Select a location**.
2.  Navigate to the list of locations and submit a location.
3.  Select a location card.
4.  Navigate back to the 'Location audits' page and select the location card again.

 Expected behavior: Focus starts at the beginning of page.

 Actual behavior: Notice that the focus startslocation is inconsistent.

</td></tr><tr><td>

iOS Mobile

 PRB2032864

</td><td>

Auto-redirect to next task fails when the writeback response includes an 'Attachments' section

</td><td>

The user is returned to the previous task.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2023574

</td><td>

The SG Filter condition operator changes to 'On' but still exhibits default behavior

</td><td>

The **Filtered by Open State** field doesn't show a date image to allow date selection.

</td><td>

1.  Under 'My SIG Incidents', select **See All**.
2.  Select the filter option on the top right corner.

 Notice that 'Filter by Open Date' can't be modified, and the cases shown seem to reflect the default between range behavior.

</td></tr><tr><td>

iOS Mobile

 PRB2050550

</td><td>

NASS citation links do not work, especially after leaving that chat and returning

</td><td>

While using Chat in Now Requester Intune app version 21.4.0, the user is prompted to 'Create an incident' which then displays URL links. On selecting the links, nothing happens. When applying the same steps on Now Requester Intune app version 21.5.0, the links also work. However, when the user selects 'Done' to leave the chat and return to the chat screen, the links in the chat no longer work.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2020083

</td><td>

Mobile Questionnaires Details Text under the Question is cut off

</td><td>

When filling in a questionnaire on Mobile Agent app, the 'Details' text under the question is cut off. However, after the completed questionnaire is completed, the 'Details' text shows the full text.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2033864

</td><td>

Smart assessment attachment upload fails on first attempt and an unanswered question error appears on submission in the Now Mobile app

</td><td>

Two issues occur when completing smart assessments on NOW Mobile: Unanswered question error on submit even after all questions are answered - no indication of which question is missing. Attachment upload fails on first attempt, requiring re-upload before submission succeeds.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2012706

</td><td>

After the mobile agent app is installed, a blank screen is observed on login

</td><td>

Initial login fails with Error 50089. On retry, Azure AD authenticates successfully and issues a valid token. However, despite successful authentication, the Mobile Agent application does not navigate back to the app interface and instead presents a blank screen.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2004945

</td><td>

Users can't be mentioned in Japanese

</td><td>

Users can't be mentioned in the Activity Stream in Japanese in Now Mobile.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2052703

</td><td>

CallKit remains active for apps distributed to the China App Store, causing Apple Guideline 5 \(Legal\) rejections

</td><td>

A Mobile Publishing user's iOS app is rejected under Guideline 5 - Legal because the SpeakNow SDK's CallKitManager is active unconditionally with no gating based on App Store storefront/territory. Consequently, the app lists China as an available territory.

</td><td>

1.  Publish a Mobile Publishing \(whitelabel\) or mobilesky-based iOS app with Virtual Agent voice/calling enabled.
2.  List China as an available territory in App Store Connect.
3.  Submit the build for App Store review.

 Expected behavior: The app is approved.

 Actual behavior: Apple rejects the app under Guideline 5 - Legal, stating CallKit functionality is active while China is an available territory. The Chinese Ministry of Industry and Information Technology \(MIIT\) requires CallKit to be inactive for apps distributed through the China App Store. VoIP calling itself remains allowed, but must not use CallKit's system call UI there.

</td></tr><tr><td>

iOS Mobile

 PRB1954340

</td><td>

The user observes 'Error 153 Video player configuration error' when opening a Campaign

</td><td>

When the user opens a 'Campaign' with a YouTube video embedded, they observe an error.

</td><td>

1.  Open mobile \(requester\) app and log in to an instance.
2.  Select **More** &gt; **Campaigns**.

 Expected behavior: The video displays the play button and background image.

 Actual behavior: There is error Error 153 Video player configuration error.

</td></tr><tr><td>

iOS Mobile

 PRB2003508

</td><td>

The Checklist details screen for Mobile Agent is greyed out even if the 'Available offline' option is on

</td><td>

The checklist is not editable in offline mode in iOS.

</td><td>

1.  Toggle the app to 'Offline' in iOS.
2.  Open the checklist details details screen.

Observe that it is not editable.

3.  Open the same in Android and see that it is editable.

 Expected behavior: The checklist behavior should be the same as Android.

 Actual behavior: The checklist is not editable in offline mode in iOS.

</td></tr><tr><td>

iOS Mobile

 PRB2018263

</td><td>

Text difference between iOS and Android in the More menu of the Agent app in French

</td><td>

On the Mobile Agent application, the 'More' menu on the app \(the latest navigation button\) does not have the same header text between iOS and Android in French.

</td><td>

1.  Log in to an instance on Agent mobile in both Android and iOS.
2.  Navigate to 'Settings' and set both preferred language and instance language to French.

 Notice that the more applet launcher is translated to 'Autre' for iOS while being translated to 'Plus' for Android.

</td></tr><tr><td>

iOS Mobile

 PRB2030065

</td><td>

iPhone Cached Data Size information not available

</td><td>

Cached Data Size is not available on iPhone.

</td><td>

1.  Open Agent mobile app.
2.  Navigate to the **More** launcher page.
3.  Navigate to settings section.
4.  Select the **Offline** section and download cache.

 Expected behavior: Cached Data Size should be available on iPhone.

 Actual behavior: Cached Data Size is not available on iPhone.

</td></tr><tr><td>

iOS Mobile

 PRB2034884

</td><td>

Captured image attachments saved in Display P3 color space cause color shift in non-color-managed viewers

</td><td>

Images captured via the iOS app's camera/scan flow are uploaded in the Display P3 wide-gamut color space instead of standard sRGB. The pixel data is intact and renders correctly in color-managed viewers \(web browser, sys\_attachment preview\). But applications that are not color-managed misinterpret the embedded P3 ICC profile as sRGB, producing a visible color shift \(oversaturation / reddish-teal cast\).

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2030345

</td><td>

50000 error when using brokered authentication for Intune login

</td><td>

When the Microsoft Authenticator app is also installed, the user is redirected to Authenticator app for Intune login. On first try, after a successful login in the Authenticator app, the user is redirected back to the ServiceNow app where they observe a -50000 error.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2018049

</td><td>

The Question Circle icon doesn't display correctly

</td><td>

The mobile screen tab is configured to use the 'Question circle' icon, but it displays a different icon.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2034128

</td><td>

Submitting a secondary IFS causes attachments added to the original one to fail uploading

</td><td>

When a secondary IFS is submitted, it removes the temporary file storage used for attachments.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB1996440

</td><td>

Images captured by the Agent app camera or uploaded to a work order task / questionnaire have no geolocation data

</td><td>

When an Agent captures images using the mobile camera or uploads previously captured images directly on the work order task or its questionnaires, it strips geolocation data such as latitude or longitude.

</td><td>

 

</td></tr><tr><td>

iOS Mobile

 PRB2035814

</td><td>

Picker search bar requires double tap to focus and is hidden when paginationBreak is less than ten

</td><td>

PickerControlLargeView gates the search bar on model.items.count &gt;= 10, which only reflects how many options are in the first paginated page. On instances with a small paginationBreak \(&lt; 10\), the search bar is hidden even when totalOptionsCount is large. Fix: use model.totalOptionsCount instead of model.items.count. Additionally, the UISearchBar wrapped in UIViewRepresentable requires two taps to gain focus because SwiftUI's gesture system intercepts the first tap.

</td><td>

 

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[Now Mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/now-mobile-available-versions.md)

