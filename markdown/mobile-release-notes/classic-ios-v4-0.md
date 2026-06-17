---
title: Mobile Classic iOS v4.0
description: The Mobile Classic iOS v4.0 release provides problem fixes.
locale: en-US
release: mobile
topic_type: reference
last_updated: "2026-06-17"
reading_time_minutes: 2
breadcrumb: [Mobile Classic mobile app version history, Mobile app version history for iOS and Android]
---

# Mobile Classic iOS v4.0

The Mobile Classic iOS v4.0 release provides problem fixes.

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

 PRB709271

</td><td>

Attachment option in Live Feed does not work in the native iOS app

</td><td>

When clicking the paper clip icon in live feed to attach an image from the camera, photo library, or iCloud, the app returns to the homepage without giving the option to attach an image.

</td><td>

In the iOS app:

 1.  Open **Live Feed**.
2.  Click the red circle in the lower right to create a new live feed or comment in an existing feed.
3.  Click the **paperclip icon** to attach something.
4.  Click any of the options that pop up \(e.g. Camera, Photo Library, or iCloud\).

 Expected result: The user should get the option to attach an image, or bring up the camera interface to take an image.

 Actual result: The user is directed back to the home page. No option to select an image is shown. This seems to work as expected using Connect, but not in Live Feed.

</td></tr><tr><td>

Mobile

 PRB709786

</td><td>

In the iPhone app, related list query breadcrumbs are rendered as empty space, which looks like an error

</td><td>

Instead of blank space, the iOS app should contain information such as 'Related List condition.'

</td><td>

1.  In the desktop interface, create a module that displays a list of records, filtered by a related list query and at least one other condition. For example, create a module of the Problem list and add the following query to the **Arguments** field: **state=1^assigned\_toISNOTEMPTY^RLQUERY incident.problem\_id,&gt;=1^ENDRLQUERY**
2.  Add the module to your favorites so you can access it from the mobile UI.
3.  In the iPhone app, open the module.

 Note that the query breadcrumbs display as '**, Assigned to, State**'.

</td></tr><tr><td>

Mobile

 PRB712207

</td><td>

In Fuji, users are unable to access or download attachments on the iPhone mobile app

</td><td>

In Fuji, attachments cannot be accessed or downloaded in the iPhone mobile app.

</td><td>

In the iOS app:

 1.  Access a Fuji instance.
2.  Navigate to any incident that contains an attachment \(e.g. INC0000055\).
3.  Attempt to interact with the attachment.

 Expected result: The attachment is accessed or downloaded.

 Actual result: Nothing happens.

</td></tr><tr><td>

Mobile

 PRB713927

</td><td>

Native iOS app should ignore instance session timeout URLs during the SSO flow

</td><td>

The native iOS app should ignore instance session timeout URLs during the SSO flow. This will fix an issue where SSO would not work if the SSO flow redirected to a local session timeout page during the SSO log in flow.

</td><td>

1.  Attempt to log in via SSO.
2.  Get redirected to an external IDP, then to a local session timeout page, then back to the external IDP.

 Expected result: App should land on the external IDP page, and the user should be allowed to complete log in.

 Actual result: App fails to land on external IDP page, and the user is unable to log in.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile Classic mobile app version history](../classic-available-versions.md)

