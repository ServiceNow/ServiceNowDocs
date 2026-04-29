---
title: Viewing session analytics
description: The Usage Insights Sessions page in the Data Foundation module lists filterable application sessions you can drill down into for more detailed insights. Refine the sessions list to focus on data such as selected screens or events for your application.View statistics and timeline details for a specific user session.View overall session statistics for a user, and event timeline details for a user's specific sessions.
locale: en-US
release: australia
product: User Experience Analytics
classification: user-experience-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Usage Insights, Usage Insights, Platform Analytics]
---

# Viewing session analytics

The Usage Insights Sessions page in the Data Foundation module lists filterable application sessions you can drill down into for more detailed insights. Refine the sessions list to focus on data such as selected screens or events for your application.

To view the Sessions overview, navigate to **Platform Analytics** &gt; **Usage Insights**, select an application, and then select the **Data Foundation** &gt; **Sessions** module. Select a User ID in the Sessions list to view that user's sessions.

![sessions analysis screen](../image/uxa-session-analytics2-.png)

<table id="table_pxy_nzp_vjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Date

</td><td>

Date the session occurred.

</td></tr><tr><td>

Duration

</td><td>

Length of time the session lasted.-   **Note:** Usage Insights tracks a maximum session length of four \(4\) hours.

-   **Note:** On the legacy dashboard, session start times were based on the server clock, which applied uniformly. After the replatforming, session start times are based on the client clock, which can differ slightly between users \(for example, due to local time settings or sync delays\). This can cause a minor variation, typically less than 2%, in total session counts.


</td></tr><tr><td>

User ID

</td><td>

Automatically generated number assigned to each unique user of an application version. Can be used instead of an internal User ID. Select the User ID to view the user's sessions and Activity timeline.

</td></tr><tr><td>

Hashed User ID

</td><td>

Generated hashed `sys_id` value for each user. Actual user IDs are not displayed; instead they are automatically hashed via the SHA-256 hash function.**Note:** Users not logged into the portal are displayed as “Anonymous”.

</td></tr><tr><td>

Device

</td><td>

Specific device the user session occurred on.

</td></tr><tr><td>

Session ID

</td><td>

Unique session number for the user. A new, consecutive session number is tracked for the user each time they start a session.

</td></tr><tr><td>

Location

</td><td>

Location the user accessed the application from.

</td></tr><tr><td>

Pages

</td><td>

Number of screens visited or pages viewed during the session by the user.

</td></tr><tr><td>

Events

</td><td>

Number of actions the user performed during the session.

</td></tr></tbody>
</table>## Filter options

You can filter a Users list by date range, user type, and country by default. Using the **Add filter** option, you can filter on Locale, Department, Role, Group, and Manager.

**Note:** The Add filter options use a logical AND operator, meaning that the results must meet both the criteria in the default filters AND the criteria in the additional filters to be included in the visualizations.

## Session breakdown analysis

You can view a breakdown analysis of sessions by grouping them according to country, state, device type, hourly usage, and so on. The Geographic Analytics visualization, which was available until the Xanadu release, has been replaced by this Analysis Breakdown.

**Parent Topic:**[Using Usage Insights](../content-framework/concept/using-uxa.md)

## Session Details record

View statistics and timeline details for a specific user session.

### Before you begin

Role required: admin

### About this task

Access a Session Details record from a user sessions record.

### Procedure

1.  Navigate to **Platform Analytics** &gt; **Usage Insights**.

2.  Select an application.

3.  Select the **Sessions** module.

4.  Select a User ID in the Sessions list to view that user's sessions.

5.  Select a session.


## User sessions record

View overall session statistics for a user, and event timeline details for a user's specific sessions.

You can access a user sessions record from a sessions or users list screen. Select a hashed user ID to open the sessions record for that user. Select a session tile to view its Activity timeline. ![User sessions record showing the timeline for a single session with user details](../../../use/par-for-workspace/image/uxa-session-record-australia.png)

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

Shows a timeline of events for the user session. To see more detail for an event, click the Expand icon![](../../../reuse/icons/product-icons/chevron-down-outline-24.svg) next to an event on the timeline.

</td></tr><tr><td>

User Details

</td><td>

Relevant details associated with the user, including Role, Department, and whether the user is active.

</td></tr></tbody>
</table>**Related topics**  


[Session Details record](viewing-sessions.md#)

