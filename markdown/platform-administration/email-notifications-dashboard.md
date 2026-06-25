---
title: Email notifications dashboard
description: The email notification dashboard provides visibility into key metrics and enables admins to configure the dashboard to enable access to other users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/email-notifications-dashboard.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email notifications dashboard

The email notification dashboard provides visibility into key metrics and enables admins to configure the dashboard to enable access to other users.

To access Email notifications dashboard, navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Email notifications dashboard**

The dashboard enhances visibility and supports proactive management of email notifications, and includes highlights about:

-   Email notification insights
-   Active notifications
-   Notification trends
-   Top 10 email notifications by usage, users, and tables

\[Omitted video\] Description: Email notifications dashboard

Data collection is triggered by configuring and executing jobs. For more information, see [Configure jobs for email notifications dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-jobs-email-dashboard.md).

**Note:** Configuration of jobs is required for data to be displayed on the dashboard.

## Key insights

Email notification insights highlights and shows the system notification sent over emails for the selected time period.

\[Omitted image "email-noti-insights.png"\] Alt text: Email notifications insights

<table id="table_m2g_lmw_12c"><thead><tr><th>

UI component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Date

</td><td>

Select the time period for the data that you want to view. -   Last 3 months
-   Last month
-   Last quarter
-   Last week
-   Yesterday

</td></tr><tr><td>

Most triggered notification

</td><td>

\[Omitted image "dashboard-most-triggered.png"\] Alt text: Example for most triggered notification

The most triggered notification in the selected time period. In the above example the Asset Restocking notification has been triggered 99 times.Clicking on **Most triggered notification** gives more insight into the notification overview for the selected period which includes:

-   Triggered count: Comparison for the selected period
-   Opted out overview: The overview of the fraction of users who have opted out from a notification and the total number of users who have received at least once
-   Total unsubscribed count: Highlights the total number of users who unsubscribed after subscribing through custom notifications
-   Conditions: View the notification details and condition set
-   Activate or Deactivate: Option to activate or deactivate the notification

</td></tr><tr><td>

Most opted-out notification

</td><td>

\[Omitted image "dashboard-most-optout.png"\] Alt text: Most opt-out notification.

The overview of all recipients receiving the notification vs. the users who opted out of the notification. In the above example 120 users were receiving the notification and out of the 120 users, 78 users have chosen to opt out from receiving the notification.Clicking on **Most opted-out notification** gives the notification overview for the selected period which includes:

-   Triggered count: Comparison for the selected period and the prior period \(for example, the same month or the previous month or quarter\)
-   Opted out overview: The overview of the fraction of users who have opted out from a notification and the total number of users who have received at least once
-   Total unsubscribed count: Highlights the total number of users who unsubscribed after subscribing through custom notifications
-   Conditions: View the notification details and condition set
-   Activate or Deactivate: Option to activate or deactivate the notification

</td></tr><tr><td>

Most used category

</td><td>

\[Omitted image "dashboard-most-used-category.png"\] Alt text: Most used category.

Notification category of the that was most triggered in the selected time period. Clicking on **Most used category** displays the top 100 most used notification categories with:

-   Triggered count \(times\)
-   Opted-out count \(users\)
-   Category name
-   Table name

</td></tr><tr><td>

Total unused notification

</td><td>

\[Omitted image "dashboard-total-unused.png"\] Alt text: Total unused notifications.

Total number of notifications that weren't triggered during the selected time period. Clicking on **Most unused notification** displays the top 100 most unused notifications with:

-   Triggered count \(times\)
-   Opted-out count \(users\)
-   Category name
-   Table name

</td></tr></tbody>
</table>**Example for deeper insights into a notification**

\[Omitted image "email-not-overview.png"\] Alt text: Example for deeper insights into a notification

## Active notifications

Active notifications shows the number of total notifications where true represents the number of active notifications and false represents the number of inactive notifications.

\[Omitted image "email-dashboard-active.png"\] Alt text: Example for active notifications

## Notifications trend

Monitor notifications trend on triggered counts and newly created notifications. It shows the trend for the selected time period, comparing the current triggered count to the previous period \(for example, the same month or the previous month or quarter\). It also provides an overview of how the triggered count has evolved over time, with a graphical representation for better visualization of the trend. You can view the email notification trends by:

-   Triggered count

    \[Omitted image "email-dashboard-monthly-trigger.png"\] Alt text: Example for Triggered count shown in monthly email notifications trend

-   Newly created notifications

    \[Omitted image "email-dashboard-monthly-created.png"\] Alt text: Example for Newly created notifications shown in monthly email notifications trend


## Top email notifications

\[Omitted image "email-dashboard-top-noti.png"\] Alt text: Example for Top 10 email notifications by usage

The top 10 email notifications can be viewed by:

-   Usage
-   Users
-   Tables

You can select **Show more** to view up the top 100 notifications.

\[Omitted image "email-dashboard-100.png"\] Alt text: Example for top notifications by usage

The top 100 notifications for Most triggered, Last triggered, Most opted-out and Unused notifications can be filtered and viewed by Date, Category, Table, and State.

To view all the email notifications, select **View all email notifications**.

-   **[Configure jobs for email notifications dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-jobs-email-dashboard.md)**  
Configure data collection jobs for the email notification dashboard.

**Parent Topic:**[Email and SMS notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_EmailNotifications.md)

**Related topics**  


[Create notification categories]()

[Create an email notification]()

[Email diagnostics dashboard]()

[Email templates]()

[Email layouts]()

[Email retention]()

[Watermarks on notification emails]()

[Parse an email thread]()

[Email digests]()

[Domain separation and Notifications]()

[Email FAQs and troubleshooting notification emails]()

