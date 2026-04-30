---
title: Configure container components for Work scheduler
description: Present information in an intuitive format using the Card Base Container component.
locale: en-US
release: zurich
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a Work scheduler card using the Next Experience UI Builder, Setting up, Work scheduler, Workforce Optimization for ITSM, IT Service Management]
---

# Configure container components for Work scheduler

Present information in an intuitive format using the Card Base Container component.

## Before you begin

Role required: workspace\_admin or ui\_builder\_admin​

## Procedure

1.  In the **Content** section, select **+Add component**.

2.  In the **Components** pop-up screen select **Card Base Container**.

3.  In the **Config** tab, set the interaction and aria properties.

    -   From the **Interaction** menu, select **Click**.
    -   In the Accessibility section, select the Dynamic data binding icon ![Dynamic data binding icon](../image/dynamic-data-binding-icon.png)
    -   From the **ARIA Properties** list, select **@state.cardProps.aria**.
4.  Select the **Events** tab.

5.  In the **Card clicked** menu, select **+Add a new event handler**.

    The Event handler preview pop-up screen appears.

6.  In the **Scripts** section, select **Handle card clicked**.

7.  Select **Add**.

8.  Select **Save**.

    Here's a demo on how to configure container components in Work scheduler.Configure container components for Work Scheduler


## What to do next

[Configure a Work scheduler card heading component](work-sched-card-based-header.md)

**Parent Topic:**[Create a Work scheduler card using the Next Experience UI Builder](create-workscheduler-card-wfo-itsm.md)

**Previous topic:**[Define event mappings for Work scheduler](work-sched-event-mapping.md)

**Next topic:**[Configure a Work scheduler card heading component](work-sched-card-based-header.md)

