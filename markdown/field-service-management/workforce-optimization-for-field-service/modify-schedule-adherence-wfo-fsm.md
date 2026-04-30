---
title: Modify schedule adherence and conformance formulas by using extension points
description: Configure and adjust the schedule adherence and conformance formulas using scripted extension points so that you can customize their calculations for your organization.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up scheduling in Workforce Optimization for Field Service, Configuring Workforce Optimization for Field Service, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Modify schedule adherence and conformance formulas by using extension points

Configure and adjust the schedule adherence and conformance formulas using scripted extension points so that you can customize their calculations for your organization.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Search for `sn_shift_planning.ScheduleAdherenceExtPt`.

3.  On the form banner, click the link here to edit the record.

4.  To create your extension point script, click Create Implementation in the related links.

5.  To create your extension point script, click **Create Implementation** in the related links.

6.  Modify the formulas for calculating the schedule adherence and conformance in the `getAdherencePercentage` and `getConformancePercentage` methods.

7.  Click **Update**.


## Result

The schedule adherence and conformance calculations are based on the formulas in the implementation.

