---
title: Use exact times in SLA calculations
description: When business percentages are used for SLA calculations, they are rounded up to two decimal places.
locale: en-US
release: yokohama
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SLA calculation, Using Service Level Management, Service Level Management, IT Service Management]
---

# Use exact times in SLA calculations

When business percentages are used for SLA calculations, they are rounded up to two decimal places.

## Before you begin

Role required: admin

## About this task

As a result, breaches can occur when SLA calculations are rounded up to 100%. You can enable SLA calculations to instead use the business time or actual time left.

For example, a business percentage of 99.951% is rounded up to 100%, which causes a breach.

For more accurate SLA calculations, enable the SLA engine property for using the exact value of the business time left if a schedule is specified or the actual time left if the SLA has no schedule specified.

## Procedure

1.  Go to **Service Level Management** &gt; **Properties** &gt; **SLA Engine**.

2.  For the **Use field "business\_time\_left" to calculate breach time instead of "business\_percentage" field** property, select the **Yes** check box.

3.  Click **Save**.


**Parent Topic:**[SLA calculation](../reference/r_SLAAutomation.md)

