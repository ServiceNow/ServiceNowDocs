---
title: How Usage Insights matches funnels
description: Learn how Usage Insights matches sequences of pages you anticipate users seeing before they reach a goal.
locale: en-US
release: australia
product: Usage Insights
classification: usage-insights
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Conversion funnels, Using Usage Insights, Usage Insights, Platform Analytics]
---

# How Usage Insights matches funnels

Learn how Usage Insights matches sequences of pages you anticipate users seeing before they reach a goal.

Usage Insights bases funnel matching on unique users, and not on sessions, so steps can be matched between sessions. For example, a user may start the first step of a funnel in their first session, and continue the next step in another session. Users are counted only once for a selected time range, and step completions are only counted once per user.

A funnel measures users who complete a funnel step within 30 days, so a user can complete step \#2 on January 1, then step \#3 on January 30, to be counted.

Funnels steps are loosely matched. Users can perform other steps between the steps that define the funnel. For example:

For the funnel A &gt; B &gt; C:

-   A &gt; B &gt; C are matched.
-   A &gt; B &gt; D &gt; C are also matched, where D can be any user action.
-   A &gt; B &gt; E are not matched—the user is considered to have completed only step B.

When matching duplicate steps, the funnel analysis selects the first occurrence that progresses the funnel, and ignores duplicate occurrences. For example, for the funnel A &gt; B &gt; C: With a user who performs A &gt; B &gt; B &gt; C, the second B is ignored.

When selecting a time range, the analysis shows only users who complete the entire funnel within the time range. If a user starts the first step before or after the selected time range, they are not counted.

Funnel analysis respects duplicate funnel entrances. For example, for the funnel A &gt; B &gt; C, a user performs the following actions:

`A (Sunday) > B (Monday) > A > (Tuesday) > B (Wednesday) > C (Thursday)`

The user is returned when selecting Sunday-Thursday, Monday-Thursday, Tuesday-Thursday, but not if they select Wednesday-Thursday.

This behavior is true both for reviewing individual sessions, and for the aggregated user count.

Usage Insights shows all sessions that progress through the funnel for the selected step, excluding ignored occurrences, and can show multiple sessions of a user.

When filtering by application versions, the analysis shows only the users who performed their first action from the selected version.

**Parent Topic:**[Funnel reports in Usage Insights](funnel-reports-uxa.md)

