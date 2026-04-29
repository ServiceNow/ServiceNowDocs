---
title: Activate parallel jobs for Data Discovery
description: Use parallel jobs to reduce your Data Discovery job execution time.
locale: en-US
release: australia
product: Data Discovery
classification: data-discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Discovery jobs, Exploring Data Discovery \(Classic\), Data Discovery, Platform Privacy]
---

# Activate parallel jobs for Data Discovery

Use parallel jobs to reduce your Data Discovery job execution time.

## Before you begin

Role required: admin

## Procedure

1.  By default Data Discovery runs jobs using a single thread. Multiple threads may be activated for Data Discovery full scans.
2.  In the navigation filter enter `sys_properties.list`.

3.  Create the property `com.glide.data_discovery.max_concurrent_item_workers`

4.  Verify the **Type** is `integer`.

5.  **Important:** It is recommended to start with a small number of workers per node\(2 or 3\).

    Enter the number of parallel job workers in the **Value** field up to 5.


