---
title: Configure a display type component for a Work scheduler card
description: Add the Label value stacked display work item fields within the card.
locale: en-US
release: zurich
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a Work scheduler card using the Next Experience UI Builder, Setting up, Work scheduler, Workforce Optimization for ITSM, IT Service Management]
---

# Configure a display type component for a Work scheduler card

Add the **Label value stacked** display work item fields within the card.

## Before you begin

Role required: workspace\_admin or ui\_builder\_admin​

## Procedure

1.  In the **Content** section, navigate to **Body\(Flex\)** &gt; **Card Base Container \(Flex\)** &gt; **Card Base Header**.

2.  Right-click **Card Base Header** and select **Add component after**.

3.  In the pop-up screen, select the **Label value stacked** component.

4.  In the left pane, select **Label value stacked**.

5.  In the right pane, select the **Config** tab and configure the size, alignment, and items.

    1.  In the Alignment menu, select **Horizontal-equal**.
    2.  In the Size menu, select **Small**.
    3.  Hover over **Items**and select the Dynamic data binding icon ![Dynamic data binding icon](../image/dynamic-data-binding-icon.png).
    4.  In the **Items** menu, enter **@state.cardProps.content**.
    5.  In the **Item min, width** field, enter `75 px`.
    6.  Enable **Wrap text** and **Truncated** options.
    7.  Click **Save**.
    Here's a demo on how to configure a display type component for a Work scheduler card.Configure a display type component for a Work Scheduler card


## What to do next

[Configure an avatar component for Work scheduler](work-sched-avatar-component.md)

**Parent Topic:**[Create a Work scheduler card using the Next Experience UI Builder](create-workscheduler-card-wfo-itsm.md)

**Previous topic:**[Configure a Work scheduler card heading component](work-sched-card-based-header.md)

**Next topic:**[Configure an avatar component for Work scheduler](work-sched-avatar-component.md)

**Related topics**  


[Configure UI Builder workspace experiences](https://www.servicenow.com/docs/access?context=ui-builder-workspace-settings&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

