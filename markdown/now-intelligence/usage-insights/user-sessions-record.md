---
title: User sessions record
description: View overall session statistics for a user, and event timeline details for a user's specific sessions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/usage-insights/user-sessions-record.html
release: australia
product: Usage Insights
classification: usage-insights
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Viewing session analytics, Using Usage Insights, Usage Insights, Platform Analytics]
---

# User sessions record

View overall session statistics for a user, and event timeline details for a user's specific sessions.

You can access a user sessions record from a sessions or users list screen. Select a hashed user ID to open the sessions record for that user. Select a session tile to view its Activity timeline. \[Omitted image "uxa-session-record-australia.png"\] Alt text: User sessions record showing the timeline for a single session with user details

<table id="table_awj_gp4_gkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User ID

</td><td>

 

</td></tr><tr><td>

Hashed User ID

</td><td>

Generated hashed `sys_id` value for each user. Actual user IDs are not displayed, and instead are automatically hashed via the SHA-256 hash function.**Note:** Users not logged into the portal are displayed as “Anonymous”.

</td></tr><tr><td>

First Session

</td><td>

Date and time the user first accessed the application.

</td></tr><tr><td>

Last Session

</td><td>

Date and time the user last began a session.

</td></tr><tr><td>

Date range

</td><td>

Choose a range of dates to display in the sessions list.

</td></tr><tr><td>

Locales

</td><td>

The country, language, and region the user viewed the application in.

</td></tr><tr><td>

Devices

</td><td>

Shows browser type, device and device version used by the user.

</td></tr><tr><td>

Sessions

</td><td>

Shows the following session details:-   Relative time since the session occurred.
-   Duration - How long the session lasted.
-   Operating system, version, platform, and browser used for the session.
-   Search - Navigates to the Sessions list specific to sessions for the selected user.

 You can reorder sessions by date, index number, session duration, or app version.

</td></tr><tr><td>

Activity timeline

</td><td>

Shows a timeline of events for the user session. To see more detail for an event, click the Expand icon\[Omitted image "chevron-down-outline-24.svg"\] next to an event on the timeline.

</td></tr><tr><td>

User Details

</td><td>

Relevant details associated with the user, including Role, Department, and whether the user is active.

</td></tr></tbody>
</table>**Parent Topic:**[Viewing session analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/viewing-sessions.md)

**Related topics**  


[Session Details record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/session-details-record.md)

