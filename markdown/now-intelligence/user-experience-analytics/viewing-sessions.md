---
title: Viewing session analytics
description: The User Experience Analytics Sessions module lists filterable application sessions you can drill down into for more detailed insights.
locale: en-US
release: xanadu
product: User Experience Analytics
classification: user-experience-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# Viewing session analytics

The User Experience Analytics Sessions module lists filterable application sessions you can drill down into for more detailed insights.

![Sessions list](../image/sessions-list.png)

<table id="table_pxy_nzp_vjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Refresh

</td><td>

Refreshes the sessions list with selected filters and updated session data.

</td></tr><tr><td>

List Filter

</td><td>

Property options to filter the sessions list.

</td></tr><tr><td>

Date

</td><td>

Date the session occurred.

</td></tr><tr><td>

Total Sessions

</td><td>

Total number of sessions available for the selected platform, application version, date range, and filter options.

</td></tr><tr><td>

Duration

</td><td>

Length of time the session lasted.**Note:** User Experience Analytics tracks a maximum session length of four \(4\) hours.

</td></tr><tr><td>

Version

</td><td>

Mobile application version.

</td></tr><tr><td>

User Index

</td><td>

Automatically generated number assigned to each unique user of an application version. Can be used instead of an internal User ID.

</td></tr><tr><td>

Hashed User ID

</td><td>

Generated hashed `sys_id` value for each user. Actual user IDs are not displayed, and instead are automatically hashed via the SHA-256 hash function.**Note:** Users not logged into the portal are displayed as “Anonymous”.

</td></tr><tr><td>

Session

</td><td>

Unique session number for the user. A new, consecutive session number is tracked for the user each time they start a session.

</td></tr><tr><td>

Device

</td><td>

Specific device the user session occurred on.

</td></tr><tr><td>

Location

</td><td>

Location the user accessed the application from.

</td></tr><tr><td>

Screens/Pages

</td><td>

Number of screens visited or pages viewed during the session by the user.

</td></tr><tr><td>

Actions

</td><td>

Number of actions the user performed during the session.

</td></tr><tr><td>

Details

</td><td>

Opens the Session Details record for the selected mobile session.

</td></tr><tr><td>

Indicators

</td><td>

Shows indicators and tags associated with a session or user record.

</td></tr><tr><td>

User sessions record pane

</td><td>

Provides overview of and lets you navigate to further details of an individual session. The record pane is located below the sessions list.

</td></tr></tbody>
</table>**Note:** Sessions lists can only be reordered by session date.

## Filter options

You can filter a Sessions list by these properties:

-   Action
-   App Killed
-   Browser Types
-   Browser Versions
-   Cities
-   Connectivity
-   Countries
-   Devices
-   Device types
-   Duration
-   Events
-   Hashed User ID
-   Locales
-   Offline
-   Operating Systems
-   Operating System Versions
-   Pages
-   Screens
-   Session \#
-   States/Regions
-   Tags
-   User Index

-   **[View a sessions list](../task/view-a-sessions-list.md#)**  
View pre-filtered session lists, and search for session by additional properties.
-   **[Filter a sessions list](../task/filter-session-list.md)**  
Refine a sessions list to focus on data such as selected screens or events for your application.
-   **[Sessions and users list indicators](../reference/session-indicators.md)**  
You can view and filter indicators and tags on a Sessions or Users list.

**Parent Topic:**[Using User Experience Analytics](use-user-exp-analytics.md)

**Related topics**  


[Session Details record](../reference/session-details-record.md)

