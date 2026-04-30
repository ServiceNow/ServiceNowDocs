---
title: View widget performance metrics
description: View the metrics provided by the performance window to identify which widgets take the longest to load data.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-10-23"
reading_time_minutes: 1
breadcrumb: [Improve portal performance, Manage, Employee Center, Employee Service Management]
---

# View widget performance metrics

View the metrics provided by the performance window to identify which widgets take the longest to load data.

## Before you begin

Role required: sp\_admin

To track the performance of a custom widget, add a hotspot to the script: [Add hotspots to track custom widget performance](add-hotspots-track-custom-widget-performance.md)

## About this task

The **Performance Details** window provides comprehensive tracking of each widget on a page, enabling better assessment of the user experience. You can view load times, customization status, and display visibility for each widget.

![The Performance detailswindow displays widget performance metrics](../images/performance-details.jpg)

**Note:** Performance tracking is not supported for widgets with asynchronous data loading enabled.

## Procedure

1.  Navigate to **All** &gt; **Employee Center**.

2.  Select the clock icon to open the **Performance details** window.

    The clock ![the clock icon to access the performance details page](../images/clock-icon.jpg) icon is located at the bottom-left corner of the screen.

3.  Click **Enable Performance Stats**.

4.  Click **Close**.

5.  Impersonate a user to enable the system to capture widget load times for that user.

    1.  Click on your profile image.

    2.  Click **Impersonate**.

        ![Impersonate button](../images/ec-impersonate.png)

    3.  Select the user to impersonate.

    4.  Click on your profile image and **End impersonation**.

        ![End impersonation button](../images/ec-end-impersonation.png)

6.  Select the clock icon to open the **Performance details** window.

7.  In the **Search for user** field, select the user that you impersonated.

8.  Review the **Server time** column to identify which widgets have the longest load times.

9.  Export the data as an Excel file.

10. Click **Close** when you are done.


**Parent Topic:**[Improve portal performance](../concept/improve-manage.md)

