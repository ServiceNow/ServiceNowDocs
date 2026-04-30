---
title: Prepare base plugins
description: Prepare to restore the base functionality that is required for the problem state model you have modified.
locale: en-US
release: xanadu
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Migration job, Migration Utility, Configuring Problem Management, Problem Management, IT Service Management]
---

# Prepare base plugins

Prepare to restore the base functionality that is required for the problem state model you have modified.

## Before you begin

Role required: admin

## About this task

**Note:** You cannot move back to any earlier stage because in the previous stage you activated the Problem Management Best Practice — Madrid — State Model plugin \(com.snc.best\_practice.problem.madrid.state\_model\) on this instance and the old states are invalid.

## Procedure

1.  Resolve blocking modifications.

    1.  For each blocking modification, click **View Modification**.
    2.  Select the **Replace on upgrade** check box.

        **Note:** If this option is not available, add the **Replace on update** field to the form using **Configure** &gt; **Form Layout**.

    3.  Click **Update**.
    4.  Click **Back**.
2.  Click **Run Checks**.


## What to do next

[Restore base plugins](restore-base-plugins.md).

