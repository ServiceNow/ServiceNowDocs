---
title: View Usage Insights Events
description: View user analytics event occurrences to help you analyze core steps within your business processes.These event KPIs are tracked for web and mobile platforms.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/usage-insights/view-events.html
release: zurich
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Usage Insights, Platform Analytics]
---

# View Usage Insights Events

View user analytics event occurrences to help you analyze core steps within your business processes.

## Before you begin

Role required: user

## About this task

Usage Insights automatically detects all screens, gestures, and user actions in your applications. You can view occurrences of user-triggered events including menu selection, button clicking, and swiping.

\[Omitted image "uxa-event-properties.png"\] Alt text: Analytics module - Events screen

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **User Experience Analytics**.

2.  Select the application for which you want to analyze events.

3.  Select the search icon \[Omitted image "IconSearch.png"\] Alt text: Search icon. to open the Search field and type the name of the event to filter in the Events list, or scroll to search the Events list.

    To view events across all applications, select **All Applications** from the applications list and then select **Events**.


## What to do next

For more information about viewing events, read [SNAnalytics APIs](https://developer.servicenow.com/dev.do#!/reference/api/zurich/client/SNAnalyticsClientAPI).

## User Analytics Events KPIs

These event KPIs are tracked for web and mobile platforms.

|KPI|Event logs when:|
|---|----------------|
|App Launch External|User launches application from a notification or deep link.|
|User Login|User successfully logs in.|
|Open App/ALP|User taps ALP/screen.|
|Open Applet|User opens an applet.|
|Voice Search Tapped|User taps the Microphone icon.|
|Contact Support Tapped|User taps the Contact Support icon.|
|Field Action|User taps a button, such as **Call** or **Email**.|
|Search Start|Search action starts.|
|Search Complete|Search action completes. This time is recorded in milliseconds.|

