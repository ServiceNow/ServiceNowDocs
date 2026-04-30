---
title: Modify schedule adherence and conformance formulas by using extension points
description: Configure and tweak the schedule adherence and conformance formulas using scripted extension points to customize them for your organization.
locale: en-US
release: zurich
product: Workforce Optimization for HR
classification: workforce-optimization-for-hr
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up Scheduling, Configure, Workforce Optimization overview, HR Service Delivery, Employee Service Management]
---

# Modify schedule adherence and conformance formulas by using extension points

Configure and tweak the schedule adherence and conformance formulas using scripted extension points to customize them for your organization.

## Before you begin

Role required: sn\_hr\_wfo.admin

## About this task

Use the `sn_shift_planning.ScheduleAdherenceExtPt` extension point and create an implementation to configure the formulas. You can create multiple implementations. However, the implementation with the lowest order number is executed.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Search for `sn_shift_planning.ScheduleAdherenceExtPt`.

3.  On the form banner, click the link **here** to edit the record.

4.  To create your extension point script, click **Create Implementation** in the related links.

5.  Modify the formulas for calculating the schedule adherence and conformance in the `getAdherencePercentage` and `getConformancePercentage` methods.

    ![Extension Script for Schedule Adherence.](../image/extension-script-adherence-wfo-hr.jpg)

6.  Click **Update**.


## Result

The schedule adherence and conformance calculations are based on the formulas in the implementation.

**Parent Topic:**[Setting up Scheduling for Workforce Optimization for HR](setup-scheduling-wfo-hr.md)

