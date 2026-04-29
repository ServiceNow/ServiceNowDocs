---
title: Pause a work order task
description: Record a break from a work order task in the Field Service application if you are unable to continue the work for any reason. You can resume the work order task when you start working on it again. The system automatically tracks and calculates the actual time taken to complete the task even though you worked at different intervals.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Recording time worked, Updating task status, Completing work orders on the web interface, Use, Field Service Management]
---

# Pause a work order task

Record a break from a work order task in the Field Service application if you are unable to continue the work for any reason. You can resume the work order task when you start working on it again. The system automatically tracks and calculates the actual time taken to complete the task even though you worked at different intervals.

## Before you begin

The system administrator can choose to enable the **work.management.allow.auto.timecard** property so that time cards are automatically created when you start working on a task. The data of the time cards is stored in \[metric\_instance\] table and is controlled by **work.management.allow.auto.metric\_cleanup** [system property](../../planning-and-policy/reference/r_InstalledWithFSM.md).

Role required: wm\_agent

## About this task

The work order task must be in the Work in Progress state to pause the timer.

## Procedure

1.  Navigate to the work order task that you want to pause.

2.  Click **Pause Work**.

    The button toggles to **Resume Work** automatically.

    ![pause work](../image/pause-work.png)

3.  Click **Resume Work** when you are ready to work on the activity again.


## Result

Each time you pause or resume work on the task, a timestamp is captured in the activity stream and the actual time you worked on the task is automatically calculated. An entry for the time worked is created in the **Time Worked** related list.

