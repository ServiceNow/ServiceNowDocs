---
title: Activate parallel jobs for data anonymization
description: Use parallel jobs to reduce your anonymization job execution time.
locale: en-US
release: australia
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data anonymization, Data privacy, Data Privacy, Platform Privacy]
---

# Activate parallel jobs for data anonymization

Use parallel jobs to reduce your anonymization job execution time.

## Before you begin

Role required: admin

## Procedure

1.  By default data class and user based anonymization jobs run using a single thread. Multiple threads may be activated for data class and user based jobs. In addition, federated jobs used during cloning uses parallel jobs with 3 workers by default.
2.  In the navigation filter enter `sys_properties.list`.

3.  Create the property `com.glide.data_privacy.max_parallel_workers`

4.  To adjust the number of federated job parallel workers, edit the `dp.max_concurrent_clone_item_workers` property.

5.  Verify the **Type** is `integer`.

6.  **Important:** It is recommended to start with a small number of workers per node\(2 or 3\).

    Enter the number of parallel job workers in the **Value** field up to 5.


