---
title: Mobile Agent for iOS v22.2.1
description: The iOS v22.2.1 release provides fixes for the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile-release-notes/agent-ios-v22-2-1.html
release: mobile
topic_type: reference
last_updated: "2026-10-13"
reading_time_minutes: 2
breadcrumb: [ServiceNow Agent mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Agent for iOS v22.2.1

The iOS v22.2.1 release provides fixes for the application.

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

PRB2054052

</td><td>

The app is unresponsive when Face ID and access PIN are enabled

</td><td>

The app becomes unresponsive.

</td><td>

1.  From 'Settings', enable Face ID and access PIN.
2.  Close and reopen the app.

 Notice that the app becomes unresponsive.

</td></tr><tr><td>

Mobile iOS

PRB1940360

</td><td>

The on-tap function on the list screen navigates the user to the top of the list

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile iOS

PRB2056008

</td><td>

'No data available' after first relaunch

</td><td>

After relaunching the app, an empty screen displays with a message reading, 'No data available'.

</td><td>

1.  Log in to Now Mobile app.
2.  Close the app without selecting **Log out**.
3.  Relaunch the app.

 Expected behavior: The home screen displays.

 Actual behavior: Empty screen with 'No data available'.

</td></tr><tr><td>

Mobile iOS

PRB2056032

</td><td>

NASS citation links don't work in the Now Intune app

</td><td>

In the Now Requestor Intune app, when a user asks Chat to 'Create an incident' the response displays URL links. Selecting these links does nothing.

</td><td>

 

</td></tr><tr><td>

Mobile iOS

PRB2061018

</td><td>

MSAL login loop issue with single tenant setup

</td><td>

The app-owned MSAL instance requests tokens against the multi-tenant authority.

</td><td>

1.  Register a branded build against an Entra app registration configured as single-tenant \('Accounts in this organizational directory only'\).
2.  Install the branded 22.0.0 build and launch it for the first time.
3.  Select **Sign in**.

Microsoft Authenticator opens and shows the account list.

4.  Select the account.

 Expected behavior: Control returns to the app, MSAL acquires the token, the account is enrolled with Intune, and the user proceeds into the app.

 Actual behavior: Control returns to the app, but the Intune sign-in is immediately re-triggered and Authenticator reopens with the account list. The loop repeats on every selection; the user can never complete enrollment.

</td></tr><tr><td>

Mobile iOS

PRB2062382

</td><td>

**Mandatory File Attachment** Field Validation on Mobile Agent App fails

</td><td>

After deleting the mandatory attachment, the **Submit** button remains enabled, allowing the user to submit the form even though the required attachment field is empty.

</td><td>

1.  Log in to Mobile Agent app.
2.  Open a WOT task that contains a mandatory attachment field. If one does not exist, create a mandatory attachment field.
3.  Fill in the form without uploading the mandatory attachment.

Observe that the **Submit** button remains disabled.

4.  Upload the mandatory attachment.

The **Submit** button becomes enabled.

5.  Before submitting the form, delete the uploaded mandatory attachment.

 Expected behavior: When a mandatory attachment is removed, the**Submit** button should be disabled immediately, preventing the user from submitting the form until all required attachment fields are populated.

 Actual behavior: After deleting the mandatory attachment, the**Submit** button remains enabled, allowing the user to submit the form even though the required attachment field is empty.

</td></tr></tbody>
</table>This version also includes other minor bug fixes and performance improvements.

**Parent Topic:**[ServiceNow Agent mobile app version history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/mobile/markdown/mobile-release-notes/agent-available-versions.md)

