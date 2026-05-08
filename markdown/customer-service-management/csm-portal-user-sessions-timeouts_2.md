---
title: Portal usage calculation
description: Portal usage enables you to track how your customers and employees are using the portal. The Customer Portal Usage dashboard provides information about portal visits resulting in session counts.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Portal reference, Reference, Customer Service Management]
---

# Portal usage calculation

Portal usage enables you to track how your customers and employees are using the portal. The Customer Portal Usage dashboard provides information about portal visits resulting in session counts.

To view the Customer Portal Usage dashboard, navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Portal Usage**.

**Note:** You can ignore the bot session usage that is captured as part of this dashboard.

**Note:** This definition tracks usage for customer service portals based on the user roles and ignores usage for non CSM portals or roles. Sessions are tracked for the following roles:

-   External roles: sn\_esm\_user, sn\_customerservice.requester, sn\_communities.community\_user
-   Internal roles: sn\_customerservice.self\_contributor

A user session is a period of activity on the Customer or Consumer Service Portal by any of the following session types:

-   Guest session: Session where the user isn't logged in
-   Bot session: Separate count of sessions generated due to bots and crawlers
-   External session: Session where the user is an external user, typically a customer, or consumer who is logged in

The aggregate session count is based on the following calculations:![The infographic displays the calculation for aggregate session count by subtracting guest sessions and bot sessions, and then adding external sessions.](../image/aggregate-session-count-csp.png).

A user session times out after a specific period of inactivity.

User access to the self-service portals is tracked as follows: per session, per day, and per portal. If the same user logs in from multiple browsers or devices, each login is counted as a separate visit. Each first call of a portal page starts a session and, the usage metrics are calculated for the 24 hours window.

The default session timeout is 30 minutes. This setting can be adjusted using a system property. For more information about modifying the session timeout setting, see Manage user sessions.

## Site visit calculation examples

A user logs in, logs out, and then logs in again.

|Step|User activity|Billable count incremented|
|:---|:------------|:-------------------------|
|1|User visits the portal as an anonymous or guest user|Yes|
|2|User logs in|No|
|3|User logs out|No|
|4|User logs in immediately after logging out|Yes|

A user logs in and continues the session past midnight:

|Step|User activity|Billable count incremented|
|:---|:------------|:-------------------------|
|1|User visits the portal as an anonymous or guest user|Yes|
|2|User logs in|No|
|3|User session continues past midnight|**Yes**|
|4|User logs out|No|

