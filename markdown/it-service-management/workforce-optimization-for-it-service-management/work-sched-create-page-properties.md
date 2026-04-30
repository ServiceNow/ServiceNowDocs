---
title: Define the workItem property in the Work scheduler page configuration
description: Add the workItem property to the Work scheduler page configuration to receive the workItem object provided by the work queue.
locale: en-US
release: yokohama
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a Work scheduler card using the Next Experience UI Builder, Setting up Work scheduler in Workforce Optimization for ITSM, Work scheduler in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Define the workItem property in the Work scheduler page configuration

Add the **workItem** property to the Work scheduler page configuration to receive the **workItem** object provided by the work queue.

## Before you begin

Role required: workspace\_admin or ui\_builder\_admin​

## Procedure

1.  In the **Page configuration** section, select the **Config** tab.

2.  In the **Properties** section, select **Edit**.

3.  In the **Edit properties** pop-up window, select **+Add**.

4.  In the **Property name** field, enter **workItem**.

5.  From the **Type** menu, select **JSON**.

6.  Select **Add**.

7.  Select **Save**.

    The **workItem** property is created.

8.  Hover over the **workItem** property and select the Dynamic data binding icon \(![Dynamic data binding icon](../image/dynamic-data-binding-icon.png)\).

9.  In the **workItem** field, type **@state.workItem**.

10. Click **Save**.

    Here's a demo on how to define the workItem property in the Work scheduler page configuration.Define the work item property in the Work Scheduler page configuration


## What to do next

[Define event mappings for Work scheduler](work-sched-event-mapping.md)

**Parent Topic:**[Create a Work scheduler card using the Next Experience UI Builder](create-workscheduler-card-wfo-itsm.md)

**Previous topic:**[Create page scripts for Work scheduler](work-sched-create-page-scripts.md)

**Next topic:**[Define event mappings for Work scheduler](work-sched-event-mapping.md)

