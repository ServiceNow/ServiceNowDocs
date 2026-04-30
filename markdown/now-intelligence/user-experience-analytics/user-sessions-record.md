---
title: User sessions record
description: View overall session statistics for a user, and event timeline details for a user's specific sessions.
locale: en-US
release: xanadu
product: User Experience Analytics
classification: user-experience-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Viewing user and session details, Using User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# User sessions record

View overall session statistics for a user, and event timeline details for a user's specific sessions.

You can access a user sessions record from a sessions or users list screen.

-   From the sessions list screen, click on a timeline event.
-   From the users list screen, click on a user record from the list.

![User sessions details record.](../image/user-session-details-record.png)

<table id="table_awj_gp4_gkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User ID

</td><td>

Generated hashed `sys_id` value for each user. Actual user IDs are not displayed, and instead are automatically hashed via the SHA-256 hash function.**Note:** Users not logged into the portal are displayed as “Anonymous”.

</td></tr><tr><td>

Add tag

</td><td>

Enter a text label name to associate with a user's record. You can view assigned tags on individual records in the Users or Sessions list.

</td></tr><tr><td>

Search

</td><td>

Opens the Sessions list filtered for all sessions performed by the user.

</td></tr><tr><td>

First Session

</td><td>

Date and time the user first accessed the application.

</td></tr><tr><td>

Last Session

</td><td>

Date and time the user last began a session.

</td></tr><tr><td>

Time in App/Time on Site

</td><td>

Average time the user spent on the site or in the application across all versions and devices, and total number of sessions performed by the user.

</td></tr><tr><td>

Locales

</td><td>

Language the user viewed the application in, and country they accessed from.

</td></tr><tr><td>

App Versions

</td><td>

All application versions the user has installed across all devices.

</td></tr><tr><td>

Devices &amp; Installations

</td><td>

Shows browser type, device and device version used by the user, along with a list of date ranges in which the user was active per installation. Every time a user reinstalls the app, a new date range appears.

</td></tr><tr><td>

Locations

</td><td>

List of locations the user accessed sessions from.

</td></tr><tr><td>

Custom Properties

</td><td>

Opens available SDK API Reference documentation providing information on adding custom properties.

</td></tr><tr><td>

Instance ID

</td><td>

The instance’s unique identifier.

</td></tr><tr><td>

Instance Name

</td><td>

The instance’s friendly display name.

</td></tr><tr><td>

Language

</td><td>

The preferred language a user's device was set to in which they performed the session.

</td></tr><tr><td>

Login Count

</td><td>

The number of times a user has logged in to the app by entering their email and password.

</td></tr><tr><td>

Sessions window

</td><td>

Shows the following session details:-   Date - Date the session occurred.
-   Index - Sequential number of session for the user.
-   Duration - How long the session lasted.
-   Version - Mobile application version the session occurred on.
-   Device - Mobile device the user performed the session on.
-   Search - Navigates to the Sessions list specific to sessions for the selected user.

 You can reorder sessions by date, index number, session duration, or app version.

</td></tr><tr><td>

Timeline

</td><td>

Shows a timeline of events for the user session. To see more detail for an event, click the Expand icon ![](../image/plus-expand-icon.png) next to an event on the timeline.

</td></tr><tr><td>

Session Details

</td><td>

Displays the Session Details record for the selected session.

</td></tr></tbody>
</table>**Parent Topic:**[Viewing user and session details](../task/view-user-sessions-log.md)

**Related topics**  


[Session Details record](session-details-record.md)

