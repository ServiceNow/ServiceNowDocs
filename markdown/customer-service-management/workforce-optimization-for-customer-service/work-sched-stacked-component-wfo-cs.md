---
title: Configure a display type component for a Work scheduler card
description: Add the Label value stacked display work item fields within the card.
locale: en-US
release: xanadu
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a Work scheduler card using the Next Experience UI Builder, Setting up Work scheduler in Workforce Optimization for Customer Service, Configuring Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Configure a display type component for a Work scheduler card

Add the **Label value stacked** display work item fields within the card.

## Before you begin

Role required: admin, workspace\_admin, or ui\_builder\_admin​

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

[Configure an avatar component for Work scheduler](https://www.servicenow.com/docs/access?context=work-sched-avatar-component&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)

**Parent Topic:**[Create a Work scheduler card using the Next Experience UI Builder](create-workscheduler-card-wfo-cs.md)

**Related topics**  


[Manage the visual style of UI Builder experiences](https://www.servicenow.com/docs/access?context=manage-the-visual-style-of-ui-builder-experiences&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

