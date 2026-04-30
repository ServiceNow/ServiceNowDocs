---
title: Configure a Work scheduler card heading component
description: Customize the Work scheduler heading component to display the title based on your needs.
locale: en-US
release: zurich
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a Work scheduler card using the Next Experience UI Builder, Setting up Work scheduler, Configure, Workforce Optimization for Customer Service, Customer Service Management]
---

# Configure a Work scheduler card heading component

Customize the Work scheduler heading component to display the title based on your needs.

## Before you begin

Role required: admin, workspace\_admin, or ui\_builder\_admin​

## About this task

For more information about the Card Base Header, see the [Components](https://horizon.servicenow.com/workspace/components) section in the Horizon design system website.

## Procedure

1.  In the **Content** section, select **+Add component**.

2.  In the **Components** pop-up screen select **Card Base Header**.

    The selected container displays in the right pane.

3.  Configure the header component.

    1.  In the **Config** tab, hover over the **Dropdowns** section and select the Dynamic data binding icon ![Dynamic data binding icon](../image/dynamic-data-binding-icon.png).

    2.  From the **Dropdowns** menu, select **@state.cardProps.dropdowns**.

    3.  Hover over the **Heading** section and select the Dynamic data binding icon ![Dynamic data binding icon](../image/dynamic-data-binding-icon.png).

    4.  From the **Heading** menu, select **@state.cardProps.heading**.

    5.  Hover over the **Tagline** section and select the Dynamic data binding icon ![Dynamic data binding icon](../image/dynamic-data-binding-icon.png).

4.  Add **Handle card action clicked** to the **Card header action clicked** event.

    1.  Select the **Events** tab.

    2.  In the **Card header action clicked** section, select **+Add a new event handler**.

    3.  From the **Tagline** menu, select **@state.cardProps.tagline**.

    4.  In the **Event handler preview** pop up screen, from the **Scripts** section, select **Handle card action clicked**.

    5.  Click **Add**.

5.  Click **Save**.

    Here's a demo on how to configure a Work scheduler card heading.Configure a Work Scheduler card heading component


## What to do next

[Configure a display type component for a Work scheduler card](https://www.servicenow.com/docs/access?context=work-sched-stacked-component&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)

**Parent Topic:**[Create a Work scheduler card using the Next Experience UI Builder](create-workscheduler-card-wfo-cs.md)

