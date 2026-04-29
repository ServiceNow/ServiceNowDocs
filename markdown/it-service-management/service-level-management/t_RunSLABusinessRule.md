---
title: Run the 2011 SLA engine asynchronously
description: By default in the 2011 SLA engine, the SLA processing is performed by the Run SLAs business rule. This business rule runs synchronously and is the suggested configuration.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SLA calculation, Using Service Level Management, Service Level Management, IT Service Management]
---

# Run the 2011 SLA engine asynchronously

By default in the 2011 SLA engine, the SLA processing is performed by the **Run SLAs** business rule. This business rule runs synchronously and is the suggested configuration.

## Before you begin

Role required: sla admin, admin

## About this task

SLA processing runs asynchronously. For example, you can run this for performance reasons, such as to avoid delays when a user saves a new incident record. While the SLA engine is running asynchronously, there can be a short delay before the Task SLA records are available after updating a Task. Refresh the form to see the updated Task SLAs.

Use synchronous processing to get the best user experience. Asynchronous processing mode is used only when there a performance issues.

**Note:** In the 2010 engine, the **Process SLAs** business rule runs the asynchronous processing.

## Procedure

1.  Navigate to **All** &gt; **Service Level Management** &gt; **Properties** &gt; **SLA Engine**.

2.  Select **Yes** for the **Execute the 2011 SLA Engine asynchronously** \(**com.snc.sla.engine.async**\) property.

3.  Click **Save**.


**Parent Topic:**[SLA calculation](../reference/r_SLAAutomation.md)

