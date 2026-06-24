---
title: Configure container components for Work scheduler
description: Present information in an intuitive format using the Card Base Container component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/work-sched-card-based-container-wfo-cs.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a Work scheduler card using the Next Experience UI Builder, Setting up Work scheduler, Optimize workforce operations, Extend capabilities, Configure, Customer Service Management]
---

# Configure container components for Work scheduler

Present information in an intuitive format using the Card Base Container component.

## Before you begin

Role required: admin, workspace\_admin, or ui\_builder\_admin​

## About this task

For more information about the Card Base Container, see the [Components](https://horizon.servicenow.com/workspace/components) section in the Horizon design system website.

## Procedure

1.  In the **Content** section, select **+Add component**.

2.  In the **Components** pop-up screen select **Card Base Container**.

3.  In the **Config** tab, set the interaction and aria properties.

    -   From the **Interaction** menu, select **Click**.
    -   In the Accessibility section, select the Dynamic data binding icon \[Omitted image "dynamic-data-binding-icon.png"\] Alt text: Dynamic data binding icon
    -   From the **ARIA Properties** list, select **@state.cardProps.aria**.
4.  Select the **Events** tab.

5.  In the **Card clicked** menu, select **+Add a new event handler**.

    The Event handler preview pop-up screen appears.

6.  In the **Scripts** section, select **Handle card clicked**.

7.  Select **Add**.

8.  Select **Save**.

    Here's a demo on how to configure container components in Work scheduler.


## What to do next

[Configure a Work scheduler card heading component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/workforce-optimization-for-it-service-management/work-sched-card-based-header.md)

**Parent Topic:**[Create a Work scheduler card using the Next Experience UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/create-workscheduler-card-wfo-cs.md)

