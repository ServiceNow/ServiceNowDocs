---
title: Assign a view to Guided Tours
description: You can assign a list or form view to a step in a guided tour.
locale: en-US
release: zurich
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Guided Tours, Guided Tours, Adoption services, Configure user experiences]
---

# Assign a view to Guided Tours

You can assign a list or form view to a step in a guided tour.

## Before you begin

Role required: guided\_tour\_admin or admin

## About this task

To assign a view to a tour step, you must know the view name. The name you see in the context menu **View** option is the title of the view. Look up the view name before you assign it to a tour step.

![Context menu view options](../image/context-menu-view-titles.png "Context menu view options")

**Note:** You can add a view to only one step in a guided tour, and this is only possible if the step begins in the default view. When the tour is played and that step is executed, the user interface refreshes to display the new view.

## Procedure

1.  Complete the following steps to find the view name:

    1.  Navigate to **All** &gt; **System UI** &gt; **Views**.

        The first two columns are **Name** and **Title**.

    2.  Locate the view by its **Title**, and note the value in the **Name** column.

2.  Navigate to **All** &gt; **Guided Tours Designer** &gt; **Guided Tours**.

3.  Open the tour to be modified.

4.  Under Related Links, from the Guided Tour Steps, select the step you want to add a view.

    ![Guided Tour Steps related list](../image/guided-tour-steps-related-list.png "Guided Tour Steps related list")

5.  In the Tour Step tab, enter the view name in the **View** field.

    ![In the Tour Step tab enter a view name.](../image/gtd-tour-step-form.png "Tour Step form")

6.  Select **Update**.

7.  Complete the following steps to test the tour with the view:

    1.  In the Guided Tours form, select **Edit with Designer**.

    2.  In the Guided Tour Designer tab or window, select **Play**.

    3.  Verify that the step you modified displays the correct view.


**Parent Topic:**[Configuring Guided Tours](configure-guided-tours.md)

