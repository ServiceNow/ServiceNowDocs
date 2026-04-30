---
title: View a task with an SLA
description: View all work order tasks associated with work orders that have SLAs.
locale: en-US
release: xanadu
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring SLAs for Field Service Management, Configuring work order templates, Configuring work orders, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# View a task with an SLA

View all work order tasks associated with work orders that have SLAs.

## Before you begin

Role required: wm\_admin, wm\_dispatcher

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Work Order** &gt; **Work Order Tasks With SLAs**.

    Tasks that are behind schedule are highlighted according to how delinquent they are.

2.  To view SLAs for a work order, select the **Task SLAs** related list in the Work Order form.

    The information in this list includes:

    |Information|Description|
    |-----------|-----------|
    |Actual elapsed time|Total running time of the SLA since it started, including any time that has passed since a breach.|
    |Actual elapsed percentage|Total percentage of the SLA time period that has elapsed. This value can rise above 100% after a breach and increases until the task is completed.|
    |Actual time left|Total time remaining until this SLA breaches. When the **Actual elapsed percentage** reaches 100%, this value is set to **0 seconds**.|
    |Business elapsed time|Amount of time that has elapsed for this SLA within the business calendar. For example, if the business calendar for this SLA is from 8am to 5pm on weekdays, then the running time for the SLA is computed between these hours only and not on weekends. If no business calendar is in effect, the business-elapsed time is the same as the actual elapsed time.|
    |Business elapsed percentage|Percentage of the SLA time period that has elapsed on the business calendar for this SLA. If no business calendar is in effect, the business-elapsed percentage is the same as the actual elapsed percentage.|
    |Business time left|Time remaining on the business calendar until this SLA is breached. If no business calendar is in effect, the business time left is the same as the actual time left. When the **Business elapsed percentage** reaches 100%, this value is set to **0 seconds**.|


