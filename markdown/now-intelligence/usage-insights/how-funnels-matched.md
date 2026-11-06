---
title: Funnel matching
description: Usage Insights matches funnel steps based on unique users, not sessions, allowing steps to span multiple sessions within a 30-day window.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/usage-insights/how-funnels-matched.html
release: australia
product: Usage Insights
classification: usage-insights
topic_type: concept
last_updated: "2026-10-20"
reading_time_minutes: 2
breadcrumb: [Conversion funnels, Using Usage Insights, Usage Insights, Platform Analytics]
---

# Funnel matching

Usage Insights matches funnel steps based on unique users, not sessions, allowing steps to span multiple sessions within a 30-day window.

Usage Insights bases funnel matching on unique users, and not on sessions, meaning steps can be matched between sessions. For example, a user may start the first step of a funnel in their first session, and continue the next step in another session. Users are counted only after for a selected time range, and step completions are only counted after per user.

A funnel measures users who complete a funnel step within 30 days. A user can complete step 2 on January 1, then step 3 on January 30, to be counted.

Funnel steps are loosely matched. Users can perform other steps between the steps that define the funnel. For example:

For the funnel A &gt; B &gt; C:

-   A &gt; B &gt; C are matched.
-   A &gt; B &gt; D &gt; C are also matched, where D can be any user action.
-   A &gt; B &gt; E aren't matched—the user is considered to have completed only step B.

When matching duplicate steps, the funnel analysis selects the first occurrence that progresses the funnel, and excludes duplicate occurrences. For example, for the funnel A &gt; B &gt; C: With a user who performs A &gt; B &gt; B &gt; C, the second B is ignored.

When selecting a time range, the analysis shows only users who complete the entire funnel within the time range. If a user starts the first step before or after the selected time range, they aren't counted.

Funnel analysis respects duplicate funnel entrances. For example, for the funnel A &gt; B &gt; C, a user performs the following actions:

A \(Sunday\) &gt; B \(Monday\) &gt; A &gt; \(Tuesday\) &gt; B \(Wednesday\) &gt; C \(Thursday\)

The user is returned when selecting Sunday-Thursday, Monday-Thursday, Tuesday-Thursday, but not if they select Wednesday-Thursday.

This behavior is true both for reviewing individual sessions, and for the aggregated user count.

Usage Insights shows all sessions that progress through the funnel for the selected step, excluding ignored occurrences, and can show multiple sessions of a user.

When filtering by application versions, the analysis shows only the users who performed their first action from the selected version.

**Parent Topic:**[Funnel reports in Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/usage-insights/funnel-reports-uxa.md)

