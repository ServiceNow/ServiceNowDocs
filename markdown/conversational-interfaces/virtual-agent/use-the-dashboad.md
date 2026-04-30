---
title: Legacy - Set the date range of the data
description: Set the Start and End dates at the top of the Overview tab to specify the date range of the data summarized on a page. The date range set on this tab applies to all the other tabs on the Virtual Agent Analytics dashboard.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-11-12"
reading_time_minutes: 2
keywords: [Virtual Agent, Overview, Legacy, Set, date range, Analytics, dashboard]
breadcrumb: [Legacy - Using the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Set the date range of the data

Set the **Start** and **End** dates at the top of the Overview tab to specify the date range of the data summarized on a page. The date range set on this tab applies to all the other tabs on the Virtual Agent Analytics dashboard.

## Before you begin

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](../concept/VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

Role required: Chat Analytics Viewer \(chat\_analytics\_viewer\)

## About this task

![Virtual Agent chat data ranges shown by start and end dates in year-month-day format.](../images/dashboard-top-dates.png)

All dates and times on the dashboard are UTC. Even though the conversation table lists conversation dates and times in different time zones, Virtual Agent \(VA\) converts them to UTC when displaying them on the dashboard. Additionally, if you select a preset date range, such as last week, the dates might be different from what you expect.

You can set the date range in two ways.

## Procedure

1.  Navigate to **All** &gt; **Conversational Analytics** &gt; **Dashboard**.

2.  Use the **Start** and **End** dates to set the date range.

    1.  Select the **Start** calendar icon ![Calendar icon](../images/dashboard-calendar-icon.png).

    2.  Double-select the start date on the calendar.

    3.  Select **OK**.

    4.  Select the **End** calendar icon ![Calendar icon](../images/dashboard-calendar-icon.png).

    5.  Double-select the end date on the calendar.

    6.  Select **OK**.

        The data displayed on the dashboard adjusts according to the data in the new date range.

3.  Use the **Start** date calendar to set the date range.

    1.  Select the **Start** calendar icon ![Calendar icon](../images/dashboard-calendar-icon.png).

    2.  Double-select the start date of the date range.

    3.  While holding down the control-key on the keyboard, double-select the end date.

        The dashboard highlights the range of dates.

        ![Calendar showing highlighted start-to-end dates.](../images/dashboard-calendar-start-drag.png)

    4.  Select **OK**.

    The data displayed on the dashboard adjusts according to the new date range.


**Parent Topic:**[Legacy - Using the Conversational Analytics Dashboard](../concept/use-the-dashboard-overview.md)

