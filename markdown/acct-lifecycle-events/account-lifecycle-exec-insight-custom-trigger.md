---
title: Configure a custom trigger
description: Create a custom trigger to capture a business signal that is specific to your organization and include it in the AI-generated engagement brief.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-exec-insight-custom-trigger.html
release: australia
topic_type: task
last_updated: "2026-08-31"
reading_time_minutes: 1
keywords: [custom trigger, Executive Insight Generator, Activity Subscription Framework, activity type, engagement signals]
breadcrumb: [Engagement brief, Engagement home page, Manage engagements, Customer success, Use, Customer Success Management]
---

# Configure a custom trigger

Create a custom trigger to capture a business signal that is specific to your organization and include it in the AI-generated engagement brief.

## Before you begin

-   Role required: admin
-   The Executive Insight Generator skill must be activated. See  for details.

## About this task

To configure a custom trigger, complete two tasks: define the signal and create the automation that detects it. First, create an activity type record that defines what signal you want to track. Then, write the script \(such as a business rule, scheduled job, or Performance Analytics indicator\) that watches for the condition and records when it occurs. When the script detects the condition, it creates an activity record that the Executive Insight Generator skill uses when it generates the next brief.

## Procedure

1.  Navigate to **All** &gt; **Activity Subscriptions** &gt; **Activities Data** &gt; **Activities** and create a new activity type record.

    **Note:** For more information about the Activity Subscription Framework, see the platform documentation for Activity Subscription.

2.  In the **Source mapping** related list, create a source mapping record that identifies the source table and sets the target to the engagement record.

3.  In the subscriber object fields, specify additional entities that should also receive this activity, such as the account.

    You can configure up to three subscriber objects per activity type.

4.  Create a business rule, scheduled job, or PA indicator that detects the condition you want to track.

    -   Use a business rule for event-based conditions, such as a field value changing on a record.
    -   Use a scheduled job for conditions that require comparing values over time, such as a health score that has declined over a 7-day window.
    -   Use a PA indicator for conditions derived from performance analytics metrics.
5.  Configure your script to log the activity when the condition is met.


## Result

When the condition is detected, an activity record is created. The Executive Insight Generator skill includes this signal in the engagement brief the next time the brief is generated or refreshed.

**Parent Topic:**[Engagement brief](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-exec-insight-gen.md)

**Related topics**  


[Engagement brief](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-exec-insight-gen.md)

[bundle-telmt.now-assist-tmt-exec-insight-gen]

