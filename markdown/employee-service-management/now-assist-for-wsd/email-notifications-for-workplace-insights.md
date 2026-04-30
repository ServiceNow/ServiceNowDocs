---
title: Receive email notifications for Workplace Insights
description: Notify Space Planners, Reservation Managers, and Workplace Managers by email when new Workplace Insights are generated. The email notifications are sent to the users defined in the user criteria when the sn\_wsd\_ai\_agents.weekly\_insights event is triggered.
locale: en-US
release: zurich
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: task
last_updated: "2025-11-05"
reading_time_minutes: 1
breadcrumb: [Insight cards on the Workplace Central dashboard, Workplace Advisor Overview, Using AI agent workflows in Now Assist for WSD, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Receive email notifications for Workplace Insights

Notify Space Planners, Reservation Managers, and Workplace Managers by email when new Workplace Insights are generated. The email notifications are sent to the users defined in the user criteria when the sn\_wsd\_ai\_agents.weekly\_insights event is triggered.

## Before you begin

Role required: admin

## About this task

The **Generate Workplace Insights - Weekly** scheduled job runs and creates insights based on user criteria. The **Send Insight Notifications - Weekly** schedule job runs weekly and triggers an email notification to the relevant users. The email includes a summary of the latest insights and a link to the Workplace Central dashboard to access the latest insights.

**Note:** Changing the **run time** or **day** fields for this scheduled job may impact the notifications sent. Make sure that any updates are consistent with the **Generate Workplace Insights – Weekly** job to ensure uniformity.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  In the Name column, search for **Weekly**.

3.  Select **Weekly Workplace Insights**.


