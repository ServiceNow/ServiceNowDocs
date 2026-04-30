---
title: Use a view with a guided tour
description: You can assign a list or form view to a guided tour step if you are changing from the Default view view to a different view, such as Self-Service.
locale: en-US
release: yokohama
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Guided Tours, Guided Tours, Adoption services, Configure user experiences]
---

# Use a view with a guided tour

You can assign a list or form view to a guided tour step if you are changing from the **Default view** view to a different view, such as **Self-Service**.

## Before you begin

Role required: guided\_tour\_admin or admin

## About this task

To assign a view to a tour step, you must know the view name. The name you see in the context menu **View** option is the title of the view. Look up the view name before you assign it to a tour step.

![Context menu view options](../image/context-menu-view-titles.png "Context menu view options")

**Note:** You can add a view to only one tour step in a guided tour, and only if the step starts on the default view. When the tour is played and the step is executed, the UI page refreshes with the new view.

## Procedure

1.  Complete the following steps to locate the view name:

    1.  Navigate to **System UI** &gt; **Views**.

        The first two columns are **Name** and **Title**.

    2.  Locate the view by its **Title**, and note the value in the **Name** column.

2.  Navigate to **Guided Tours Designer** &gt; **Guided Tours**.

3.  Open the tour to be modified with a view.

4.  In the **Guided Tour Steps** related list, select the step you wish to add a tour for.

    ![Guided Tour Steps related list](../image/guided-tour-steps-related-list.png "Guided Tour Steps related list")

5.  In the Tour Step form section, enter the view name in the **View** field.

    ![Tour Step form](../image/gtd-tour-step-form.png "Tour Step form")

6.  Click **Update**.

7.  Complete the following steps to test the tour with the view.

    1.  In the Guided Tour form, click **Edit with Designer**.

    2.  In the Guided Tour Designer tab or window, click **Play** below the list of steps.

    3.  Verify that the step you modified displays the correct view.


