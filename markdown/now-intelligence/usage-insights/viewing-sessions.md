---
title: Viewing session analytics
description: The Usage Insights Sessions page in the Data Foundation module lists filterable application sessions you can drill down into for more detailed insights. Refine the sessions list to focus on data such as selected screens or events for your application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/usage-insights/viewing-sessions.html
release: australia
product: Usage Insights
classification: usage-insights
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Usage Insights, Usage Insights, Platform Analytics]
---

# Viewing session analytics

The Usage Insights Sessions page in the Data Foundation module lists filterable application sessions you can drill down into for more detailed insights. Refine the sessions list to focus on data such as selected screens or events for your application.

To view the Sessions overview, navigate to **Platform Analytics** &gt; **Usage Insights**, select an application, and then select the **Data Foundation** &gt; **Sessions** module. Select a User ID in the Sessions list to view that user's sessions.

\[Omitted image "uxa-session-analytics2-.png"\] Alt text: sessions analysis screen

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

-   **[Session Details record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/session-details-record.md)**  
View statistics and timeline details for a specific user session.
-   **[User sessions record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/user-sessions-record.md)**  
View overall session statistics for a user, and event timeline details for a user's specific sessions.
-   **[Page properties analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/page-properties-analytics.md)**  
Page properties are metadata attributes that describe a page, such as the page name, owning team, language, or category. By enriching pages with properties, you can segment usage data by attributes that are meaningful to your organization instead of by page identifier alone.

**Parent Topic:**[Using Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/using-uxa.md)

