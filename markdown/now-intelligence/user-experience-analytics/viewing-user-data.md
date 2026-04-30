---
title: Viewing user analytics
description: The Users module enables views of individual user journeys through your application, from the start of their session in the application to the time they end.
locale: en-US
release: xanadu
product: User Experience Analytics
classification: user-experience-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# Viewing user analytics

The Users module enables views of individual user journeys through your application, from the start of their session in the application to the time they end.

View user analytics and behavior, including taps and swipes, and other timeline actions. Select the users you want to see, set filters, and drill down into individual user sessions for closer insights.

![Users list](../image/users-list.png)

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

List Filter

</td><td>

Property options to filter the users list.

</td></tr><tr><td>

Total Users

</td><td>

Total number of users for the selected application version and filter options.

</td></tr><tr><td>

User Index

</td><td>

Automatically generated number assigned to each unique user of an application version. Can be used instead of an internal User ID.

</td></tr><tr><td>

Hashed User ID

</td><td>

Generated hashed `sys_id` value for each user. Actual user IDs are not displayed, and instead are automatically hashed via the SHA-256 hash function.**Note:** Users not logged into the portal are displayed as “Anonymous”.

</td></tr><tr><td>

Instance Name

</td><td>

The instance’s friendly display name.

</td></tr><tr><td>

Sessions

</td><td>

Total number of sessions the user has performed across all versions and devices.

</td></tr><tr><td>

First Session

</td><td>

Date and time when the user first accessed the application.

</td></tr><tr><td>

Last Session

</td><td>

Date and time when the user last began a session.

</td></tr><tr><td>

Time in App/Time on Site

</td><td>

Average time the user spent in the application across all versions and devices.

</td></tr><tr><td>

Devices

</td><td>

All web or mobile devices the user has installed the application on.

</td></tr><tr><td>

Last Location

</td><td>

Last location from where the user accessed the application.

</td></tr><tr><td>

Indicators

</td><td>

Shows indicators and tags associated with a session or user record.

</td></tr></tbody>
</table>**Note:** Users lists can only be reordered by user index.

## Filter options

You can filter a Users list by these properties:

-   App Versions
-   Browsers
-   Browser Version
-   Countries
-   Device Count
-   Device Types
-   Favorite
-   First Session Time
-   Hashed User ID
-   Last Session Time
-   Locale
-   Operating Systems
-   Sessions Count
-   Session Exists
-   Tags
-   Time on Site
-   User Index
-   Custom Properties

-   **[View a users list](../task/view-users-list.md#)**  
View pre-filtered user lists, and search for users by more user or session properties.
-   **[View a session event timeline](../task/view-session-event-timeline.md)**  
View a user session timeline to see listed event times that show how long into the session a user interacted with elements on the page.

**Parent Topic:**[Using User Experience Analytics](use-user-exp-analytics.md)

