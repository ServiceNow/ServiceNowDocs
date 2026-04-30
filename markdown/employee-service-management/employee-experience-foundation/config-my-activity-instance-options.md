---
title: Modify Active items widget display
description: You can configure the instance options to control the appearance of the widget, such as the title, number of topics, display size, and border color.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-02-26"
reading_time_minutes: 1
breadcrumb: [My active items widget configuration, Setup task management, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Modify Active items widget display

You can configure the instance options to control the appearance of the widget, such as the title, number of topics, display size, and border color.

## About this task

On the Employee Center home page, press and hold the control key, right-click the My active items widget, and then select **Instance Options**. By default, only 4 cards for the primary activity are displayed in the list view. You can configure the instance options to view more cards.

## Before you begin

Role required: sp\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

    The Employee Center home page is displayed.

2.  Press and hold the control key, right-click the widget, and then select **Instance Options**.

    ![instance options](../images/my-active-instance-opts.png "My items instance options")

3.  Update the following options:

    -   In the **List View Count** field, select **5** to view five cards and click **Save**.
    -   In the **Load Configuration** field, select **Synchronous** or **Asynchronous** to configure the widget load preferences.
    -   In the **Card Behaviour** field, select one of the following options
        -   Select **Wrap** to view five cards as a list.
        -   Select **Single** to view five cards as a carousel or card view.

            **Note:** Ensure you mark the activity name such as **Tasks** as Primary = true and select **Single** from instance options.

    ![My active items widget showing the summary view at the top and the list view at the bottom of the widget.](../images/my-active-items-widget.png "My active items widget items")

4.  Click **Save**.

    **My Active Items Widget Layout Guidance**

    The My Active Items widget is designed for optimal display and usability when configured using a column size of 3 or greater. This layout ensures that information presented within the widget remains readable and visually consistent across Employee Center topics.

    **Note:** The My Active Items widget does not support column sizes less than 3. If you use a column size below 3, the widget is not guaranteed to display correctly for all screen widths. Currently, there are no plans to improve support for smaller column sizes. We suggest you use a column size of 3 or higher moving forward.


**Related topics**  


[My active items widget configuration](../concept/my-activity-config.md)

