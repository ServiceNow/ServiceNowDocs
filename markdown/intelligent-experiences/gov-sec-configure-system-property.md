---
title: Update system property to limit records
description: Update the sn\_ai\_security.analyzer\_max\_record\_age\_hours system property to limit the age \(in hours\) of AI asset invocation records evaluated for AI asset security metrics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/gov-sec-configure-system-property.html
release: zurich
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Managing AI asset security, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Update system property to limit records

Update the sn\_ai\_security.analyzer\_max\_record\_age\_hours system property to limit the age \(in hours\) of AI asset invocation records evaluated for AI asset security metrics.

## Before you begin

Role required: admin

## About this task

Reducing the record age can prevent analyzing stale data, reduce unnecessary processing overhead, and focus the metric on more recent activity. Increasing the record age includes analysis of older records.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the **Name** column, use the search field to locate the sn\_ai\_security.analyzer\_max\_record\_age\_hours system property.

3.  Open the record.

4.  The default value is 4, which limits processing of AI asset invocation records to those records 4 hours old or newer.

5.  In the **Value** field, enter the age \(in hours\) of records you want to process for AI asset security metrics.

6.  Select **Update**.


**Parent Topic:**[Configuring security metrics in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configuring.md)

