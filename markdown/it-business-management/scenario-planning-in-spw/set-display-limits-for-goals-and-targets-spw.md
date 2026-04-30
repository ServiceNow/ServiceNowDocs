---
title: Set display limit for goals and targets in Strategic Planning
description: Update system property value to set the display limit for goals on the Goals page in Strategic Planning.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-12-17"
reading_time_minutes: 1
breadcrumb: [Configuring goals in Strategic Planning, Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Set display limit for goals and targets in Strategic Planning

Update system property value to set the display limit for goals on the Goals page in Strategic Planning.

## Before you begin

Role required: sn\_gf.goal\_admin

## About this task

The default display limit for goals on the Goals page is 500.

**Important:** If the value of a system property exceeds its default value, the UI performance can degrade.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

    A list of all the properties in the System Properties \[sys\_properties\] table appears.

2.  Search for the **sn\_align\_ws.goal\_hierarchy.max\_records** system property and open it.

3.  In the **Value** field, enter the desired number of goals to display in the Goals view.

4.  Select **Update**.


**Parent Topic:**[Configuring goals in Strategic Planning](../concept/configuring-goal-framework-apw.md)

