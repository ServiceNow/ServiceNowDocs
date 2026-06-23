---
title: Mobile Classic iOS v6.4
description: The Mobile Classic iOS v6.4 release provides problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/classic-ios-v6-4.html
release: mobile
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 1
breadcrumb: [Mobile Classic mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Classic iOS v6.4

The Mobile Classic iOS v6.4 release provides problem fixes.

## Download the latest Mobile Classic version

To download the latest release, visit the [Apple App Store](https://itunes.apple.com/us/app/servicenow/id1044428492?mt=8).

**Important:** There are several new ServiceNow mobile apps, including Mobile Agent, Now Mobile, Mobile Onboarding, and Now Support. Check out these new apps for the latest features and capabilities.

## Fixed in this release

<table id="tbl_AllFixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Mobile

 PRB1248669

 [KB0689525](https://support.servicenow.com/kb_view.do?sysparm_article=KB0689525)

</td><td>

Approval notifications are not cleared correctly

</td><td>

1.  Log in to the app using david.loo user and enable notifications. Make sure that approval request notifications are on.
2.  Log in to the desktop instance using the demo data user david.loo.
3.  Create a normal change request, submit it,and request approval.
4.  Use the UI actions on the change request. Make sure that David Loo is in the Approvers list.
5.  Check whether you have received an approval request notification on the mobile.
6.  Approve the record from the desktop. Make sure that the change's state moves to scheduled.
7.  Check your mobile and try to clear the notification.

 The notification is cleared but an error message is displayed: "Could not find a script to run this action."

</td></tr><tr><td>

Mobile

 PRB1347429

 [KB0694500](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694500)

</td><td>

When viewing the activity stream for a record and clicking an "email sent" entry, the page displayed is blank

</td><td>

1.  Navigate to Active incidents.
2.  Navigate to an incident record with an email as part of the activity stream.
3.  Click the "Email sent" link listed in the activity stream of the incident.

 You will be directed to a blank page.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile Classic mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/classic-available-versions.md)

