---
title: User Experience Analytics KPIs
description: You can import User Experience Analytics KPIs supported in UI Builder.
locale: en-US
release: xanadu
product: User Experience Analytics
classification: user-experience-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [User Experience Analytics reference, User Experience Analytics, Platform Analytics]
---

# User Experience Analytics KPIs

You can import User Experience Analytics KPIs supported in UI Builder.

## Supported KPIs

<table id="table_rll_xgy_xtb"><thead><tr><th>

KPI

</th><th>

Definition

</th><th>

Required fields

</th><th>

Visualization type supported

</th></tr></thead><tbody><tr><td>

Events

</td><td>

Events that are triggered on the application. When this KPI selected, you can view the number of occurrences and the values distribution of a single event property.

</td><td>

-   application
-   event name

</td><td>

-   single score
-   time series
-   bar chart
-   pie chart

</td></tr><tr><td>

Sessions

</td><td>

The number of sessions triggered on web or mobile applications. -   Web application: A session is defined as 30 minutes of inactivity or 4 hours of ongoing activity.
-   Mobile application: Whenever the application switches between the foreground and the background.

</td><td>

application

</td><td>

-   single score
-   time series

</td></tr><tr><td>

Users

</td><td>

The number of active unique users using the application. -   **Active Users**: Represents the number of all users in the application.
-   **New Users**: Represents the number of users who have performed their first session.

</td><td>

-   application
-   user type \(active or new users\)

</td><td>

-   single score
-   time series

</td></tr></tbody>
</table>**Parent Topic:**[User Experience Analytics reference](../content-framework/landing-page/user-experience-analytics-reference.md)

