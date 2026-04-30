---
title: Create an ACC registration key
description: Set up an Agent Client Collector \(ACC\) by creating an agent registration key to identify and authenticate agents that are enabled to send data to the collector. The key helps promote the security and integrity of the data collected from the system.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Getting started, Configuring Digital End-User Experience, Digital End-User Experience, IT Service Management]
---

# Create an ACC registration key

Set up an Agent Client Collector \(ACC\) by creating an agent registration key to identify and authenticate agents that are enabled to send data to the collector. The key helps promote the security and integrity of the data collected from the system.

## Before you begin

Role required: sn\_dex.admin

## About this task

**Important:** By default, the registration key you generated expires in 90 days. Update the sn\_agent.registration\_key\_validity.days property to change the validity duration.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **Agent Registration Key**.

2.  Select **New**.

3.  In the **Name** field, enter a descriptive name for the registration key.

4.  To receive notifications when a registration key is soon to expire, select a group with a valid email address in the **Ownership Group** field.

    When keys are deleted via the Cleanup Agent Registration Keys scheduled job, the indicated group receives an email notification.

5.  Select **Submit**.


## What to do next

[Install ACC for DEX on Windows](install-acc-for-dex-windows.md) or [Install ACC for DEX on macOS](install-acc-for-dex-macos.md).

