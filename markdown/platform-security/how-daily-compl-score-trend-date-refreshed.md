---
title: How Daily Compliance score, trend, and graph data is refreshed
description: Trend and graph data in the Instance Security Center is updated after the performance analytics job executes at 02:00 local time. It appears in the Daily Compliance Score tile, in the Event ribbon tiles, and in the KPI Details page detail.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Check the daily compliance score and configure security property settings, Instance Security Center, Platform Security]
---

# How Daily Compliance score, trend, and graph data is refreshed

Trend and graph data in the Instance Security Center is updated after the performance analytics job executes at 02:00 local time. It appears in the Daily Compliance Score tile, in the Event ribbon tiles, and in the KPI Details page detail.

The \[AppSec\] Daily Data Management job is a regularly scheduled job that runs nightly and performs the following tasks:

1.  Verifies if valid users have been assigned to the \[AppSec\] Daily Data Management and \[PA AppSec\] Daily Data Collection jobs when you first schedule them.
    -   If you entered a valid user into the **Run As** field, the job continues processing. A valid user is one that is not locked out of the instance and has an assigned admin role.
    -   If you entered an invalid user, an error message appears above the rotating security banner in the Instance Security Center.

        **Note:** To learn more about updating the assigned user when running scheduled jobs, see [Create or schedule a data collection job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/t_CreatASchedDataCollJob.md).

2.  Executes business logic to set the compliance state for the security properties you configure in the Hardening Compliance Configuration page. To learn more, see [Check the daily compliance score and configure security property settings](instance-sec-center-hardening.md).
3.  Runs the \[PA AppSec\] Daily Data Collection performance analytics job to collect compliance data and update the Daily Compliance Score.

## Manually refreshing the Daily Compliance Score

Alternately, if you have an assigned admin role, you can refresh and recalculate the Daily Compliance Score at any time by clicking **Refresh**.

**Note:** The **Refresh** button does not appear for users with an assigned security\_dashboard\_user role.

-   The Refresh function performs the same tasks as the Daily Data Collection performance analytics job but does it in real time, rather than in a batch process.
-   You typically use it when you want to perform updates to the Daily Compliance Score to immediately view the impact of instance security activities.
-   There may be a slight delay before the updated score appears.

**Note:** When you perform an upgrade \(for example, from London to Australia\), the Instance Security Center \(ISC\) plugin is automatically activated. A supplied fix script automatically assigns a custom user without any assigned roles.

**Parent Topic:**[Check the daily compliance score and configure security property settings](instance-sec-center-hardening.md)

