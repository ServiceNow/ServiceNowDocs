---
title: Mobile Classic iOS v2.0.2
description: The Mobile Classic iOS v2.0.2 release provides problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/classic-ios-v2-0-2.html
release: mobile
topic_type: reference
last_updated: "2026-06-17"
reading_time_minutes: 2
breadcrumb: [Mobile Classic mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Classic iOS v2.0.2

The Mobile Classic iOS v2.0.2 release provides problem fixes.

## Download the latest Mobile Classic version

To download the latest release, visit the [Apple App Store](https://itunes.apple.com/us/app/servicenow/id1044428492?mt=8).

**Important:** There are several new ServiceNow mobile apps, including Mobile Agent, Now Mobile, Mobile Onboarding, and Now Support. Check out these new apps for the latest features and capabilities.

## Fixed in this release

<table id="tbl_AllFixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile

 PRB655317

</td><td>

Web session information is being retained between logins

</td><td>

 

</td><td>

1.  Log in as admin.
2.  Navigate to an existing form for an incident.
3.  Log out.
4.  Log in as itil.
5.  Navigate to a form for an incident
6.  Change the state on the incident.
7.  Navigate back to the task detail page.

Note that admin updated the state \(instead of itil\).

</td></tr><tr><td>

Mobile

 PRB664865

</td><td>

On tables extended form sys\_user, attachments made in the new mobile app appear only when viewing the record in the mobile app

</td><td>

When an attachment is added to a record on a table extended from sys\_user using the new mobile app, the attachment is not visible when viewing the same record in the desktop UI. The also happens in the reverse, meaning attachments made in the desktop UI are not visible in the mobile app. This does not appear to happen for other extended tables, we were only able to reproduce this issue extending from sys\_user. When looking at sys\_attachment records, it appears that the attachment is attached to the sys\_user table table rather than the extended.

</td><td>

1.  Create a new table extended from the sys\_user table. You will need to update the table record for sys\_user to make this extendable.
2.  Create a new record on the extended table.
3.  Open the record created in step 2 in the Mobile App.
4.  Using the mobile app, attach a file to the record.
5.  Back in the desktop UI, view the same record. Note that the attachment is not visible.
6.  Open sys\_attachment list and look for the attachment \(it should be the most recently created one\).

Note that it shows sys\_user as the table rather than the extended table.

</td></tr><tr><td>

Mobile

 PRB666692

</td><td>

When a user selects a participant that they do not have access to, the screen shows loading indefinitely

</td><td>

 

</td><td>

1.  Log in as a customer with incidents.
2.  Navigate to an incident.
3.  Open participants.
4.  Select one that you do not have access to.

Notice that the page never loads.

</td></tr><tr><td>

Mobile

 PRB667105

</td><td>

Mobile app should go to the record activity stream before going to the form for all lists

</td><td>

Related lists are not shown: if a user skipped showing the activity stream for a record, there would be no way to view related lists for that record.

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB667570

</td><td>

Push notifications should be able to be actionable and support linking to a web path

</td><td>

Push notifications for users cannot be actionable and support linking to a web path simultaneously.

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB668492

</td><td>

Native app should support initial form values from query

</td><td>

The iOS app does not forward query values provided by form UI actions.

</td><td>

 

</td></tr><tr><td>

Mobile

 PRB668615

</td><td>

Mobile app should be able to refresh expired OAuth tokens for SSO users

</td><td>

The Client Secret is not being saved during the SSO authentication flow.

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Mobile Classic mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/classic-available-versions.md)

