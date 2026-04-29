---
title: Cancel a Discovery from a Discovery Status
description: You can manually cancel a discovery while it is in progress from the Discovery Status record.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Discovery status, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Cancel a Discovery from a Discovery Status

You can manually cancel a discovery while it is in progress from the Discovery Status record.

## Before you begin

Role required: discovery\_admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Status**.

2.  Click a **Number** to open the status record.

3.  Click **Cancel Discovery** in the **Related Links**.

    **Cancel Discovery** is only available for an active Discovery.


## Result

When a Discovery status cancels, any associated sensor transactions are immediately terminated and any scheduled sensor jobs are deleted from the system. After cancellation, the cleanup Status shows the **Completed count** and the cancellation is logged in the Discovery log. In the Queue \[ecc\_queue\] table, any records belonging to sensors exceeding the Transaction Quota Rule are set to the **Error** state.

**Parent Topic:**[Discovery status](../concept/c_DiscoveryStatus.md)

