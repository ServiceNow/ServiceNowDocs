---
title: Create a custom metric in AI Admin Center \(Lux UI\)
description: Create a custom metric by specifying event-based condition logic and testing it against live data before saving.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-admin-center-create-custom-metric.html
release: australia
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, custom metric, deflection, AI analytics, assistants]
breadcrumb: [Custom metrics \(Lux UI\), View AI assets usage and performance \(Lux UI\), Monitor, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# Create a custom metric in AI Admin Center \(Lux UI\)

Create a custom metric by specifying event-based condition logic and testing it against live data before saving.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for future deprecation and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

Role required: `ai_engmt_admin`

## About this task

Custom metrics let you specify the event criteria that count as a deflected assistant interaction in your organization. After creating a metric, edit it to map it to one or more AI assistants and activate it.

**Note:** This topic describes the AI Admin Center feature based on the Lux user experience \(UI\). There is no Next Experience UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center**.

2.  Select **Analytics** \(\[Omitted image "icon-aiac-lux-nav-monitor.png"\] Alt text: Analytics icon.\) in the side navigation panel.

3.  Select the **Custom Metric** tab.

4.  Select **New metric**.

    The Custom Metric editor opens.

    \[Omitted image "ai-admin-center-custom-metric-new-screen.png"\] Alt text: New metric page showing the Metric Details, Condition Groups, and Test Against Live Data sections.

5.  Enter a **Name** for the metric.

6.  Enter a **Description**.

7.  Build the condition logic in the condition builder.

    Add events and connect them with AND, OR, or NOT operators. Groups can be nested to form recursive logic. Each condition specifies an event type, a reference point, and an optional time window.

    Select from the following event types when building conditions: Response provided, Feedback, Event type, Conversation transferred to Live Agent, Request, and Response.

    For time-based conditions, select the unit \(Seconds, Minutes, or Hours\) from the duration unit picker next to the duration field. The picker defaults to the largest unit that the stored duration value divides evenly into.

    Hover over a column header in the condition builder for a description of that field.

8.  Select **Test against live data** to validate the condition logic before saving.

    Select a date and an assistant, then select **Run test**. The results show the number of requests that matched the metric's criteria for the selected day \(matching count\). The results also show the number of those requests counted as deflected under the metric \(deflected count\).

9.  Select **Save**.


## Result

The custom metric is added to the Custom Metrics list. To map the metric to AI assistants and activate it, see [Edit a custom metric in AI Admin Center \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-edit-custom-metric.md).

**Parent Topic:**[Custom metrics in AI Admin Center \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-custom-metric.md)

