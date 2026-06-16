---
title: ServiceNow Onboarding - Intune for iOS v15.2.0
description: The iOS v15.2.0 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/onboarding-intune-ios-v15-2-0.html
release: mobile
topic_type: reference
last_updated: "2022-12-01"
reading_time_minutes: 3
breadcrumb: [ServiceNow Onboarding - Intune app version history, Mobile app version history for iOS and Android]
---

# ServiceNow Onboarding - Intune for iOS v15.2.0

The iOS v15.2.0 release provides fixes for the application.

## Download the latest mobile app version

To download the latest release, visit the [Apple App Store](https://apps.apple.com/us/app/servicenow-onboarding/id1472486882). Users can launch a demo to try the Mobile Onboarding app. You can use a demo account from the initial post-download screen or the instance list screen.

## Fixed in this release

<table id="table_rbw_2jr_2jb"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile iOS \(non-classic\)

 PRB1611186

</td><td>

The 'Mark as complete' button isn’t enabled after playing a video in a 'View Video' HR Task

</td><td>

This issue is observed in iOS version 15.1 and older versions of the Now Mobile app.

</td><td>

1.  Create an onboarding case for new hire.
2.  Open the onboarding case on the platform.
3.  Click **Add task** in related links.
4.  Select the HR task type as 'View Video', URL as a YouTube URL link, and short description as 'Overview of platform architecture'. Assign the task to new hire.
5.  Log in to Now mobile with new hire login and password.
6.  Navigate to My Requests and open HR task.
7.  Refresh the task and click the video.

 Notice that the **Mark as complete** button isn’t enabled.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1620816

</td><td>

Now Mobile for Blackberry app crashes after upgrading to iOS 16.1.0

</td><td>

 

</td><td>

1.  On an iPhone that is running iOS 16.1, load the Now Mobile app for Blackberry v15.1.0.
2.  Use the app as normal.

 Observe that the app crashes while in use.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1610055

</td><td>

Agents appear offline on iOS devices even when an Agent is available

</td><td>

An error message reads 'No chat agent currently available'.

</td><td>

From Instance:

 1.  Log in to an instance as Admin.
2.  Impersonate a user to make an agent available on Workspace.

 From Now Mobile App:

 1.  Log in to the app.
2.  Open agent chat and click **Support options**.

 Expect behavior: 'Agent available' and the wait time are displayed.

 Actual behavior: The 'No chat agent currently available' message appears.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1611520

 [KB1182159](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1182159)

</td><td>

UI Rule does not apply on refresh of the record screen

</td><td>

The background color of the number on the record screen header card disappears.

</td><td>

1.  Create a List applet based on the incident table.
2.  Create a UI Rule to set the background colour of the P1 incident number to red on the Record Screen Header Card.
3.  Open a P1 incident record on the record screen.

The background color of the number on the Record Screen Header Card is red.

4.  Pull down to refresh the Record Screen.

 Expected behavior: The background color of the number on the Record Screen Header Card is red.

 Actual behavior: The background color of the number on the Record Screen Header Card is gone.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1597720

</td><td>

Auto-pilot Quick actions don't work properly in NowMobile

</td><td>

The conversation ends with an error message.

</td><td>

 

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1607670

</td><td>

Checklist items are not wrapped in the mobile app

</td><td>

When viewing checklists on a record screen in the mobile app, the test does not wrap, and instead is cut off.

</td><td>

1.  Navigate to a San Diego instance with ITSM mobile agent installed.
2.  Navigate to **Incident form** &gt; **Configure layout** and add a checklist to the form.
3.  Open an incident record that will be assigned to the test user in the mobile app.
4.  Add long strings of text as items to the checklist on the record and save.
5.  Open the incident record screen \(My incident\) and navigate to the 'details' embedded screen.
6.  Add a new screen checklist type field and save.
7.  Log in to the mobile app and open up the incident record.

 Expected behavior: Test wrap is visible.

 Actual behavior: Text is cut off.

</td></tr><tr><td>

Mobile iOS \(non-classic\)

 PRB1614861

</td><td>

Virtual Assistant stalls when the conversation is transferred to mobile.

</td><td>

 

</td><td>

1.  Get the NowMobile VA iOS app ready, but do not open it yet.
2.  Navigate to the Surf portal.
3.  Launch VA \(hosted at the right corner of the portal\).

Observe a greeting message, but don’t type or select anything.

4.  Open the NowMobile app and launch VA.

 Observe that VA is frozen and doesn't allow the user to type or select anything.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Onboarding - Intune app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/onboarding-intune-available-versions.md)

