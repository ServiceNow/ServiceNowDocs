---
title: Configure the flow for HR Service Delivery Integration with Cornerstone OnDemand
description: Specify the frequency and time at which you want to run the scheduled flow that pulls learning objects, users, and transcripts from the Cornerstone OnDemand application into the ServiceNow system.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, HR Service Delivery Integration with Cornerstone OnDemand, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure the flow for HR Service Delivery Integration with Cornerstone OnDemand

Specify the frequency and time at which you want to run the scheduled flow that pulls learning objects, users, and transcripts from the Cornerstone OnDemand application into the ServiceNow system.

## Before you begin

Role required: sn\_hr\_cornerstone.admin

## Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  Activate the **Trigger CSOD Sync** scheduled flow.

3.  Click **Trigger**.

    1.  Select a frequency such as daily or weekly or monthly. The default value is **Daily**.
    2.  Specify a time. The default value is **21:00:00**.

