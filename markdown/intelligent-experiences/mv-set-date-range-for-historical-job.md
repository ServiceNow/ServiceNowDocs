---
title: Set look back date range for unmanaged AI systems
description: Change how many days of missing value data AI Control Tower fills in when you mark an unmanaged AI system as managed again.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mv-set-date-range-for-historical-job.html
release: brazil
topic_type: task
last_updated: "2026-10-09"
reading_time_minutes: 1
breadcrumb: [Value, Configure, Measure AI system, Measure AI systems, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Set look back date range for unmanaged AI systems

Change how many days of missing value data AI Control Tower fills in when you mark an unmanaged AI system as managed again.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

While an AI system is unmanaged, its value data doesn't appear on the value dashboard. When you mark the AI system as managed again, the AI Control Tower fills in the data for the period it was unmanaged. Thus ensuring there are no gaps in the dashboard numbers.

By default, AI Control Tower fills in up to 30 days of value data. If an AI system was unmanaged for longer than 30 days, increase the date range so the dashboard shows the full period. For example, if an AI system was unmanaged for 6 weeks, set the date range to 45 days.

This setting applies to all AI systems that you mark as managed again. It also covers AI systems that were set to unmanaged automatically when you upgraded with a ServiceNow SKU.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home**.

2.  Navigate to **Settings** &gt; **Rules and Templates** &gt; **Templates** &gt; **Value controls**.

3.  Select **look\_back\_data\_value\_calc**.\[Omitted image "mv-historical-jobs-date-range.png"\] Alt text: Value controls page in AI Control Tower Rules and templates, with the look\_back\_data\_value\_calc control selected and its details panel open.

4.  In the **Value** field, enter the number of days of value data to fill in.

    AI Control Tower supports 30, 45, and 60 days.

5.  Select **Update**.


## Result

The next time AI Control Tower fills in value data for an AI system you have marked as managed, it uses the date range you entered.

**Related topics**  


[Value tracking for managed and unmanaged AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mv-value-tracking-for-managed-and-unmanaged-ai-systems.md)

